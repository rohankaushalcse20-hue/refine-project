---
title: "Forms गाइड | Refine v5"
display_title: "Forms"
sidebar_label: "Forms"
description: "Refine में form handling, useForm और library integrations का Hindi overview।"
---

Forms लगभग हर user-facing application का मुख्य हिस्सा होते हैं। Refine form workflows को सरल बनाने के लिए data fetching और mutations को एक structured pattern में जोड़ता है।

## useForm क्या करता है

`useForm` hook internally `useOne`, `useCreate` और `useUpdate` जैसे hooks को orchestrate करता है।

- edit या clone में existing record fetch किया जाता है
- create flow में नया record submit किया जाता है
- update flow में mutation trigger होती है

इससे form state और server interaction को अलग-अलग manually wire करने की जरूरत कम हो जाती है।

## Library integrations

Refine का core `useForm` headless है, लेकिन इसे अलग-अलग libraries के साथ उपयोग किया जा सकता है:

- `@refinedev/core`
- `@refinedev/react-hook-form`
- `@refinedev/antd`
- Material UI, Mantine और दूसरी integrations

## कब उपयोगी है

`useForm` खास तौर पर तब मददगार है जब आपको CRUD forms, default values, save actions, loading states और validation-aware submit flows को एक consistent pattern में संभालना हो।
