<br/>

<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img src="https://refine.ams3.cdn.digitaloceanspaces.com/refine_logo.png"   style="width:250px;" align="center" />
</a>
<br />
<br />

<div align="center">
    <a href="https://refine.dev">Home Page</a> |
    <a href="https://discord.gg/refine">Discord</a> |
    <a href="https://refine.dev/examples/">Examples</a> |
    <a href="https://refine.dev/blog/">Blog</a> |
    <a href="https://refine.dev/docs/">Documentation</a>
</div>
</div>

<br />

<div align="center"><strong>बिना constraints के अपनी <a href="https://reactjs.org/">React</a>-based CRUD applications बनाएं।</strong><br>Flexibility को ध्यान में रखकर बनाया गया open source, headless web application framework।

<br />
<br />

[![Discord](https://img.shields.io/discord/837692625737613362.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/refine)
[![Twitter Follow](https://img.shields.io/twitter/follow/refine_dev?style=social)](https://twitter.com/refine_dev)

<a href="https://www.producthunt.com/posts/refine-3?utm_source=badge-top-post-badge&utm_medium=badge&utm_souce=badge-refine&#0045;3" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/top-post-badge.svg?post_id=362220&theme=light&period=daily" alt="refine - 100&#0037;&#0032;open&#0032;source&#0032;React&#0032;framework&#0032;to&#0032;build&#0032;web&#0032;apps&#0032;3x&#0032;faster | Product Hunt" style="width: 250px; height: 54px;" width="250" height="54" /></a>

</div>

<div align="center">

[![Awesome](https://github.com/refinedev/awesome-refine/raw/main/images/badge.svg)](https://github.com/refinedev/awesome-refine)
[![npm version](https://img.shields.io/npm/v/@refinedev/core.svg)](https://www.npmjs.com/package/@refinedev/core)
[![npm](https://img.shields.io/npm/dm/@refinedev/core)](https://www.npmjs.com/package/@refinedev/core)
[![](https://img.shields.io/github/commit-activity/m/refinedev/refine)](https://github.com/refinedev/refine/commits/main)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.0-4baaaa.svg)](CODE_OF_CONDUCT.md)

</div>

## What is refine?

**refine** web applications की तेज development के लिए React-based framework है। यह **CRUD** operations में आने वाले repetitive tasks हटाता है और **authentication**, **access control**, **routing**, **networking**, **state management**, और **i18n** जैसे critical parts के लिए industry-standard solutions देता है।

**refine** _headless by design_ है, इसलिए styling और customization के लिए unlimited options देता है।

## What do you mean by "headless"?

Pre-styled components के सीमित set की जगह, **refine** helper `hooks`, `components`, और `providers` का collection है। ये _UI components_ और _business logic_ से decoupled हैं, इसलिए ये आपको अपनी _UI_ customize करने या अपना flow code करने से नहीं रोकते।

**refine** किसी भी **custom design** या आपके पसंदीदा **UI framework** के साथ smoothly काम करता है। Convenience के लिए इसमें [Ant Design System](https://ant.design/), [Material UI](https://mui.com/material-ui/getting-started/overview/), [Mantine](https://mantine.dev/), और [Chakra UI](https://chakra-ui.com/) के ready-made integrations मिलते हैं।

## Use cases

**refine** _data-intensive_ applications जैसे **admin panels**, **dashboards**, और **internal tools** में विशेष रूप से उपयोगी है। Built-in **SSR support** की वजह से **refine** _customer-facing_ applications जैसे **storefronts** को भी power कर सकता है।

## Key Features

- **Single CLI command** के साथ zero-config, one-minute setup
- [REST API](https://github.com/refinedev/refine/tree/main/packages/simple-rest), [GraphQL](https://github.com/refinedev/refine/tree/main/packages/graphql), [NestJs CRUD](https://github.com/refinedev/refine/tree/main/packages/nestjsx-crud), [Airtable](https://github.com/refinedev/refine/tree/main/packages/airtable), [Strapi](https://github.com/refinedev/refine/tree/main/packages/strapi), [Strapi v4](https://github.com/refinedev/refine/tree/main/packages/strapi-v4), [Supabase](https://github.com/refinedev/refine/tree/main/packages/supabase), [Hasura](https://github.com/refinedev/refine/tree/main/packages/hasura), [Appwrite](https://github.com/refinedev/refine/tree/main/packages/appwrite), [Firebase](https://firebase.google.com/), [Nestjs-Query](https://github.com/refinedev/refine/tree/main/packages/nestjs-query), और [Directus](https://directus.io/) सहित **15+ backend services** के connectors
- **Next.js** या **Remix** के साथ **SSR support**
- आपकी API data structure से auto-generated **CRUD** UIs
- **React Query** के साथ state management और mutations
- किसी भी router library के साथ **advanced routing**
- **authentication** और **access control** flows के लिए providers
- Live / real-time applications के लिए out-of-the-box support
- Audit logs और document versioning
- किसी भी **i18n** framework के लिए support

## Quick Start

**refine** शुरू करने का सबसे तेज तरीका `create refine-app` project starter tool का उपयोग करना है:

```sh
npm create refine-app@latest -- --preset refine-antd
```

Setup पूरा होने के बाद project folder में जाएं और project start करें:

```sh
npm run dev
```

आपकी **refine** application [http://localhost:3000](http://localhost:3000) पर उपलब्ध होगी।
