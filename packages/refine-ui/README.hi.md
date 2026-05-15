# registry-template

आप `shadcn` CLI का उपयोग करके अपनी component registry चला सकते हैं। अपनी registry चलाने से आप custom components, hooks, pages और अन्य files को किसी भी React project में distribute कर सकते हैं।

> [!IMPORTANT]
> यह template Tailwind v4 का उपयोग करता है। Tailwind v3 के लिए [registry-template](https://github.com/shadcn-ui/registry-template) देखें।

## Getting Started

यह Next.js का उपयोग करके custom registry बनाने के लिए एक template है।

- Template components और उनकी files define करने के लिए `registry.json` file का उपयोग करता है।
- Registry build करने के लिए `shadcn build` command का उपयोग होता है।
- Registry items `public/r/[name].json` के अंदर static files के रूप में serve होते हैं।
- Template में registry items serve करने के लिए route handler भी शामिल है।
- हर registry item `shadcn` CLI के साथ compatible है।
- हमने `Open in v0` api का उपयोग करके v0 integration भी जोड़ा है।

## Documentation

पूरा documentation देखने के लिए [shadcn documentation](https://ui.shadcn.com/docs/registry) पर जाएं।
