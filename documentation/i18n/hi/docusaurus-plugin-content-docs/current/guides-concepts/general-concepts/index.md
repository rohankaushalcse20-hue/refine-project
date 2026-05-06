---
title: "General Concepts | Refine v5"
display_title: "General Concepts"
sidebar_label: "General Concepts"
description: "Refine में headless architecture, resources, providers, hooks और meta को समझें।"
---

Refine तेज़ी से web applications बनाने के लिए एक extensible framework है। इसकी architecture **hooks**, प्लग होने वाले **providers** और भरोसेमंद data/state handling पर आधारित है।

## Headless concept

Refine आपको किसी एक fixed UI component set तक सीमित नहीं करता। यह `hooks`, `components`, `providers` और utilities देता है, जबकि business logic को presentation layer से अलग रखता है।

इससे आप custom design system, Tailwind CSS, Ant Design, Material UI, Mantine या Chakra UI के साथ काम कर सकते हैं और `@refinedev/core` के benefits बनाए रख सकते हैं।

## Resource

**Resource** आपकी app की किसी entity को दर्शाता है, जैसे `products`, `blogPosts` या `orders`. Resource routes, CRUD operations, menus और providers को एक समझने योग्य structure में जोड़ता है।

## Providers

Providers data, authentication, authorization, notifications, i18n, realtime, routing और audit logs जैसी ज़िम्मेदारियों को संभालते हैं। आप built-in providers का उपयोग कर सकते हैं या अपने custom providers बना सकते हैं।

## Hooks

Refine के hooks headless हैं और किसी UI library पर निर्भर नहीं होते। `useGo`, `useCan` और `useTranslate` जैसे hooks navigation, permissions और translations के लिए एक consistent API देते हैं।

## Meta

`meta` property providers और hooks तक अतिरिक्त जानकारी पहुँचाती है, जैसे headers, विशेष parameters, field selection, multi-tenancy या GraphQL query generation.
