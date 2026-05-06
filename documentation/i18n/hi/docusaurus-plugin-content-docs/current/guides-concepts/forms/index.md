---
title: "Forms | Refine v5"
display_title: "Forms"
sidebar_label: "Forms"
description: "Refine, UI integrations और server validation के साथ CRUD forms बनाएँ।"
---

Forms लगभग हर user-facing application का महत्वपूर्ण हिस्सा हैं। Refine ऐसे hooks और components देता है जो fields, data providers, validation और mutations को एक साथ जोड़ते हैं।

## सामान्य तरीका

आप Ant Design, Material UI, Mantine, Chakra UI या React Hook Form का उपयोग कर सकते हैं। Refine की logic UI से अलग रहती है, इसलिए product के अनुसार library चुनना आसान होता है।

## Create और edit

`useForm`, `useModalForm`, `useDrawerForm` और `useStepsForm` create, edit और multi-step flows को संभालने में मदद करते हैं।

```tsx
const { formProps, saveButtonProps } = useForm({
  resource: "products",
  action: "edit",
});
```

## Relations और validation

`useSelect` related resources से options लाता है। बेहतर multilingual अनुभव के लिए local validation, server errors और i18n-based messages को साथ में उपयोग करें।
