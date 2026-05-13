# @refinedev/core

`@refinedev/core` คือฐาน headless ของ Refine package นี้มี component `<Refine />`, provider contracts, data hooks, resource handling, mutation modes และ integration ที่จำเป็นสำหรับสร้างแอป CRUD โดยไม่ผูกกับ UI library ใด

## Package นี้มีอะไร?

- การตั้งค่า `resources` สำหรับ action `list`, `create`, `edit`, `show` และ `clone`
- Data hooks เช่น `useList`, `useOne`, `useCreate`, `useUpdate` และ `useDelete`
- Contract สำหรับ `dataProvider`, `authProvider`, `accessControlProvider`, `notificationProvider`, `i18nProvider` และ router provider
- กลไก state, cache และ mutation ที่ UI integrations ของ Refine ใช้

## ใช้เมื่อใด?

ใช้ `@refinedev/core` เมื่อคุณต้องการควบคุมชั้น UI เอง หรือสร้าง integration กับ component library ที่เลือกเอง ชื่อ API, import และ command สำหรับติดตั้งไม่ควรถูกแปล
