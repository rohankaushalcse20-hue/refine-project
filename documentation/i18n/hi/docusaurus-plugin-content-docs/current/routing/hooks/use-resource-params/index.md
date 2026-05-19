---
title: "useResourceParams Hook | Refine v5"
display_title: "useResourceParams"
sidebar_label: "useResourceParams"
description: "Refine v5 में current resource, id, action और formAction parameters पढ़ने के लिए useResourceParams hook का Hindi परिचय।"
source: packages/core/src/hooks/use-resource-params
---

`useResourceParams` current resource से जुड़े parameters, जैसे `resource`, `id` और `action`, तक access देने के लिए उपयोग होता है। यह form action तय करने के लिए `formAction` और अलग state रखे बिना `id` programmatically set करने के लिए `setId` भी देता है। इसके अलावा यह `<Refine />` में defined `resources` array लौटाता है।

यदि आप `useResourceParams` को कोई resource name या identifier pass करते हैं, तो यह matching `resource` object लौटाएगा। Match न मिलने पर दिए गए name या identifier से एक temporary `resource` बनाया जाएगा।

## Usage

```tsx
const {
  id?, // ID of the record
  setId, // Function to set the ID
  resource?, // Resource object
  action?, // Passed action or inferred from the route
  identifier?, // Identifier value of the resource
  formAction?, // Form action derived from the action
} = useResourceParams({
  id?, // ID to set explicitly. Inferred from the route if not provided
  action?, // Action to set explicitly. Inferred from the route if not provided
  resource?, // Resource object to set explicitly. Inferred from the route if not provided
});
```

### Route से `id` infer करना

जब `id` explicit रूप से pass नहीं किया जाता, तो इसे route से infer किया जा सकता है। Route से inference केवल कुछ conditions में संभव है:

- यदि कोई explicit `resource` value set नहीं है।
- यदि explicit `resource` value set है और वह current route जैसी ही है।

यह check इसलिए जरूरी है ताकि `id` किसी अलग resource से infer न हो।

यदि explicit `id` value नहीं है, route में `id` नहीं है, या `resource` और route के बीच mismatch है, तो `id` को `undefined` set किया जाएगा।

### Route से `formAction` infer करना

`formAction`, `action` value से infer होता है।

- यदि `action` एक valid form action (`create`, `edit` या `clone`) है, तो `formAction` को वही `action` set किया जाएगा।
- अन्यथा `formAction` को `create` set किया जाएगा।

यह form की action को अधिक convenient तरीके से तय करने के लिए किया जाता है।

## Return Values

### resource

`resource` object।

### identifier

Current resource के लिए identifier value। यह resource की `identifier` property या `name` property हो सकती है।

### id

Actions में उपयोग होने वाला `id` parameter।

### setId

`id` को programmatically set करने वाला function।

### action

Perform किया जाने वाला current action। इसे `action` parameter से explicit pass किया जा सकता है या route से infer किया जा सकता है।

### formAction

`action` value से अलग, `formAction` केवल `create`, `edit` या `clone` हो सकता है। यदि `action` इनमें से नहीं है, तो convenience के लिए `formAction` को `create` set किया जाएगा।

### resources

`<Refine>` में defined resources का array।

### select

यह function resource `name` या `identifier` देकर matching `resource` object और matched `identifier` लौटाने देता है। Default रूप से, यदि दिए गए `name` या `identifier` का match नहीं मिलता, तो function उसी provided value से जुड़ा `resource` object और `identifier` लौटाएगा।

यदि आप `useResource` को कोई parameter नहीं देते, तो यह current route से `resource` infer करने की कोशिश करेगा। Match न मिलने पर `resource` और `identifier` `undefined` होंगे।

Function दूसरा parameter `force` भी स्वीकार करता है, जिसकी default value `true` है। यदि इसे `false` set किया जाए, तो match न मिलने पर यह `resource` object और `identifier` नहीं लौटाएगा।

## API Reference

### Properties

<PropsTable module="@refinedev/core/useResourceParams"  />

### Return value

| Description | Type                                                                                                                      |
| ----------- | ------------------------------------------------------------------------------------------------------------------------- |
| resource    | `IResourceItem` \| `undefined`                                                                                            |
| identifier  | `string` \| `undefined`                                                                                                   |
| id          | [`BaseKey` \| `undefined`](/core/docs/core/interface-references#basekey)                                                  |
| setId       | `(id: BaseKey) => void`                                                                                                   |
| action      | `undefined` \| `"list"` \| `"create"` \| `"edit"` \| `"show"` \| `"clone"`                                                |
| formAction  | `"create"` \| `"edit"` \| `"clone"`                                                                                       |
| select      | `(resourceName: string, force?: boolean) => { resource: IResourceItem` \| `undefined, identifier: string` \| `undefined}` |
| resources   | [`IResourceItem[]`](#interfaces)                                                                                          |
