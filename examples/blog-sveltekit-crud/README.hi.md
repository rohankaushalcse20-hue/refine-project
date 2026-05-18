# create-svelte

[`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte) से चलने वाला Svelte project बनाने के लिए जरूरी मूल setup यहां दिया गया है।

## Project बनाना

अगर आप यह README देख रहे हैं, तो यह step संभवतः पहले ही पूरा हो चुका है।

```bash
# current directory में नया project बनाएं
npm create svelte@latest

# my-app में नया project बनाएं
npm create svelte@latest my-app
```

## Development

Project बनाने और dependencies को `npm install` (या `pnpm install` / `yarn`) से install करने के बाद development server शुरू करें:

```bash
npm run dev

# या server शुरू करके app को नए browser tab में खोलें
npm run dev -- --open
```

## Build

Production version बनाने के लिए:

```bash
npm run build
```

Production build को `npm run preview` से preview किया जा सकता है।

> Deploy करने के लिए target environment के अनुसार [adapter](https://kit.svelte.dev/docs/adapters) install करना पड़ सकता है।
