---
title: "Inferencer Integration Guide | Refine v5"
display_title: "Inferencer"
sidebar_label: "Inferencer"
description: "Refine v5 में @refinedev/inferencer package, inferred fields और generated CRUD views समझने के लिए Hindi guide।"
---

`@refinedev/inferencer` एक package है जो data structure के आधार पर resources के लिए views automatically generate करने का तरीका देता है। इसका लक्ष्य resource views बनाने में लगने वाला समय घटाना है, ताकि code automatically generate हो और फिर आसानी से customize किया जा सके।

यह package UI package scopes के अंदर **List**, **Show**, **Create** और **Edit** views के components export करता है। उदाहरण के लिए, `@refinedev/inferencer/antd`, `@refinedev/antd` package के components export करता है।

## Installation

<InstallPackagesCommand args="@refinedev/inferencer"/>

## Available UI Inferencers

- [Ant Design](/core/docs/ui-integrations/ant-design/components/inferencer/)
- [Material UI](/core/docs/ui-integrations/material-ui/components/inferencer/)
- [Mantine](/core/docs/ui-integrations/mantine/components/inferencer/)
- [Chakra UI](/core/docs/ui-integrations/chakra-ui/components/inferencer/)
- [Headless](/core/docs/core/components/inferencer/)

:::simple Good to know

`@refinedev/inferencer` एक experimental package है और अभी development के शुरुआती चरण में है। हम package को बेहतर बनाने और नई features जोड़ने पर काम कर रहे हैं।

यदि आपके पास suggestions या feedback हैं, तो कृपया [**GitHub Discussions**](https://github.com/refinedev/refine/discussions/3046) में बताएं।

`@refinedev/inferencer` components development environments में उपयोग के लिए हैं। इन्हें production environments में उपयोग करने के लिए नहीं बनाया गया है।

:::

## How it works?

सरल रूप से, `@refinedev/inferencer` `<Refine/>` component के `dataProvider` से resource data fetch करके data structure के आधार पर views और code generate करता है।

### Data कैसे प्राप्त होता है?

`edit` और `show` actions के लिए हम `resource` और `id` के साथ request भेजते हैं। `list` और `create` actions के लिए हम `resource` के साथ list request भेजते हैं और view generate करने के लिए items में से एक item उपयोग करते हैं। ये actions आपके app में perform होंगे।

### Fields कैसे infer होते हैं?

Field types infer करते समय हम functions का एक set उपयोग करते हैं। हर function field को किसी specific type के लिए check करता है और inferred type लौटाता है। ये functions एक `priority` field भी लौटा सकते हैं, जिसका उपयोग field type तय करने में होता है। उदाहरण के लिए, यदि `created_at` property में string value है, तो इसे `date` type और `text` type दोनों के रूप में infer किया जा सकता है। ऐसे case में हम field का type तय करने के लिए `priority` field उपयोग करते हैं। Priority जितनी अधिक होगी, type उतना अधिक accurate माना जाएगा।

Multiple values वाली properties को `array` type के रूप में पहचाना जाता है, लेकिन उनके values का type तय करने के लिए वही process दोहराया जाता है। `object` type properties के लिए भी यही होता है। दोनों return value में `accessor` field रख सकते हैं, जिससे property के values access किए जाते हैं और view व code बनाते समय उनका उपयोग होता है।

यदि property `object` type है, तो हम उस property को represent करने के लिए कोई key चुनने की कोशिश करते हैं। उदाहरण के लिए, यदि `category` field का type `{ label: string; id: string; }` है, तो property represent करने के लिए हम `label` key चुनते हैं। ऐसे `object` fields, जिनके पास उन्हें represent करने वाली keys होती हैं, return value में `fieldable` property को `true` रखते हैं।

#### Available field types and functions

```ts
type Types =
  | "relation"
  | "array"
  | "object"
  | "date"
  | "email"
  | "image"
  | "url"
  | "richtext"
  | "text"
  | "number"
  | "boolean"
  | "unknown"
  | `custom_${string}`;
```

`custom_${string}` UI packages के inferencer components द्वारा तब उपयोग होता है जब उनके पास custom representations हों। फिलहाल users inferencer components में custom types और functions pass नहीं कर सकते।

#### `object` type properties को represent करने वाली keys

```ts
type PresentationalKeys =
  | "name"
  | "label"
  | "title"
  | "count"
  | "content"
  | "username"
  | "nickname"
  | "login"
  | "firstName"
  | "lastName"
  | "url";
```

### Relations कैसे determine होते हैं?

किसी field को `relation` माना जा सकता है या नहीं, यह तय करने से पहले हम कुछ conditions देखते हैं। ये checks resources पर कोई API calls trigger नहीं करते।

- यदि property name `id` या `ids` पर end होता है। camelCase, PascalCase, snake_case, kebab-case, UPPER_CASE और lower_case सभी supported हैं, array brackets ([]) के साथ या बिना।
- यदि property single `id` property वाला object है।
- यदि property single `id` property वाले objects की array है या UUID compatible strings या numbers की array है।
- यदि property string या number है और property name known resources (singular या plural) में से किसी से match करता है।

इनमें से कोई condition पूरी होने पर हम property को `relation` type मानते हैं और related resource determine करने की कोशिश करते हैं।

Relations determine करने के लिए:

- पहले हम property name (singular या plural) से match होने वाला resource खोजते हैं।
- यदि `resources` array में match वाला resource मिलता है, तो उसे related resource की तरह उपयोग करते हैं।
- Resource न मिलने पर हम `default` `dataProvider` को दो requests भेजते हैं: एक singular property name के साथ और एक plural property name के साथ। यदि `id` suffixes हों, तो उन्हें हटाया जाता है।
- Resource मिलने पर हम वही resource और उसका `dataProvider` (यदि specified हो) उपयोग करते हैं और property value के साथ API call करते हैं।
- यदि इनमें से कोई request `200` status code से succeed होती है, तो हम property को `relation` type मानते हैं और resource को related resource set करते हैं।
- यदि कोई request succeed नहीं होती, तो property से `relation` mark हटा दिया जाता है और उसे normal field माना जाता है। यदि यह `object` type है, तो इसे represent करने के लिए सबसे suitable property खोजी जाएगी।

:::simple Manually setting relations and resources

यदि आपके `dataProvider` और `resources` का काम करने का तरीका ऐसा है कि Inferencer `relation` resources नहीं खोज पाता, तो आप `fieldTransformer` function से inferred fields manually modify कर सकते हैं। इसके बारे में अधिक जानकारी [**Modifying the inferred fields**](#modifying-the-inferred-fields) section में मिलती है।

:::

### Components कैसे render होते हैं और code कैसे generate होता है?

Components render करने के लिए हम Typescript support वाले [`react-live`](https://github.com/FormidableLabs/react-live) package के [fork](https://github.com/aliemir/react-live) का उपयोग करते हैं।

Fields determine होने के बाद, components के लिए code बनाने के लिए हम `renderer` functions उपयोग करते हैं और वही code view में components render करने के लिए भी उपयोग होता है। `renderer` functions action type और UI package के अनुसार construct होते हैं। इसका मतलब है कि `@refinedev/inferencer/antd` और अन्य UI scopes में `list`, `show`, `edit` और `create` actions के लिए अलग `renderer` functions होते हैं।

`renderer` function एक `string` लौटाता है जिसमें component का code होता है। यह user को अपने project में copy-paste करने के लिए दिखाया जाता है। वही code view में component render करने के लिए भी उपयोग होता है।

Component name active `resource` element और active action से determine होता है। यदि resource में `option.label` field है, तो उसे component name का हिस्सा बनाया जाएगा। अन्यथा `resource.name` उपयोग होगा। उदाहरण के लिए, यदि resource name `categories` है और action `list` है, तो component name `CategoryList` होगा।

### GraphQL backends और `meta` values के साथ usage

Refine अपने data hooks में `meta` properties का उपयोग करके GraphQL backends handle करता है। Inferencer आपको single prop में resources और methods के लिए meta values define करने देता है और code generate तथा fields infer करते समय उनका उपयोग करता है। Data hooks की `meta` property के विपरीत, Inferencer components nested structure वाली `meta` property उपयोग करते हैं, जिससे आप resource और action के अनुसार `meta` values define कर सकते हैं।

Inferencer components में `meta` values define करने का syntax:

```tsx
<AntdListInferencer
    meta={{
        [resourceNameOrIdentifier: string]: {
            [methodName: "default" | "getList" | "getMany" | "getOne" | "update"]: Record<string, unknown>,
        }
    }}
/>
```

`default` सभी methods के लिए default `meta` value है। किसी resource में किसी method के लिए specific `meta` value न होने पर `default` value उपयोग होगी।

यह structure इसलिए design किया गया है ताकि users एक साथ multiple resources और actions के लिए `meta` values दे सकें, क्योंकि Inferencer relations खोज सकता है और जरूरी data fetch करने के लिए hooks उपयोग करने की कोशिश कर सकता है।

#### Example Usage

```tsx
<AntdListInferencer
  meta={{
    posts: {
      getList: {
        fields: ["id", "title", "content", "category_id", "created_at"],
      },
    },
    categories: {
      default: {
        fields: ["id", "title"],
      },
    },
  }}
/>
```

### Inferred fields modify करना

यदि आप Inferencer output customize करना चाहते हैं, जैसे `object` type fields के लिए custom `accessor` property set करना, field का `type` बदलना या `relation` type के लिए `resource` बदलना, तो Inferencer components में `fieldTransformer` prop उपयोग कर सकते हैं। यह function field को argument के रूप में लेता है और modified field लौटाता है। यदि `undefined | false | null` return किया जाता है, तो field preview और code, दोनों output से हट जाएगा।

### Code Viewer और Development Warning छिपाना

यदि आप code viewer और warning components छिपाना चाहते हैं, तो `hideCodeViewerInProduction` prop उपयोग कर सकते हैं। यह केवल production mode में काम करेगा। Development mode में code viewer और information block हमेशा visible रहेंगे।

ध्यान रखें कि Inferencer components production में उपयोग के लिए नहीं हैं। वे development mode में components के लिए code generate करने में मदद करने के लिए बनाए गए हैं।
