# refine codemod

`@refinedev/codemod` refine projects को breaking changes के बीच migrate करने वाला code transformation tool है। यह project files parse करके जरूरी बदलाव automate करता है, ताकि major version upgrades के दौरान manual edits कम हों।

## Usage

Available options देखने के लिए:

```sh
npx @refinedev/codemod --help
```

Project root में codemod चलाने के लिए:

```sh
npx @refinedev/codemod
```

यह tool migrations को repeatable बनाता है और refine upgrades के समय common API changes लागू करने में मदद करता है।

अधिक जानकारी के लिए refine release notes और migration documentation देखें।
