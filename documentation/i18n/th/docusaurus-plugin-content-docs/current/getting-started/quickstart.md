---
title: "Quickstart | Refine v5"
display_title: "คู่มือเริ่มต้นอย่างรวดเร็ว"
sidebar_label: "เริ่มต้นอย่างรวดเร็ว"
description: "สร้างโปรเจกต์ Refine แรกของคุณด้วย browser scaffolder หรือ CLI."
displayed_sidebar: mainSidebar
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import { Playground } from "@site/src/components/playground";

**Refine** ทำงานได้ในทุก environment ที่รัน **React** ได้ รวมถึง _Vite, Next.js, Remix และ CRA(Legacy)_

คุณสามารถตั้งค่า environment และติดตั้ง package ของ **Refine** เองได้ แต่ทางที่เร็วที่สุดคือใช้ [Browser-based Scaffolder](https://refine.dev/?playground=true) หรือ **CLI-based Scaffolder** ทั้งสองแบบให้คุณเลือก framework, UI, data provider, authentication และ i18n ก่อนสร้างโปรเจกต์

## ใช้ CLI

ใช้ `create-refine-app` เพื่อ bootstrap โปรเจกต์ **Refine** ใหม่อย่างรวดเร็ว พร้อมตัวเลือกหลายแบบให้เข้ากับงานของคุณ

```sh
npm create refine-app@latest
```

<figure>
   <img className="w-full rounded-lg border border-solid border-zinc-200 dark:border-zinc-700" src="https://refine.ams3.cdn.digitaloceanspaces.com/website/static/assets/refine-vite-mui-rest-auth-screenshot.webp" alt="Example result" />
    <figcaption className="text-center">แอป Refine ที่สร้างด้วย CLI โดยใช้ Vite + Material UI + REST API + Custom Auth Provider</figcaption>
</figure>

## ใช้เบราว์เซอร์

Browser-based scaffolder ของ Refine มีตัวเลือกชุดเดียวกับ CLI เหมาะสำหรับตั้งค่าโปรเจกต์ใหม่ ดู preview ก่อน แล้วจึงดาวน์โหลดโค้ด

<Playground />

## ขั้นตอนถัดไป

ไปที่ [Tutorials](/core/tutorial) เพื่อพัฒนาโปรเจกต์ตัวอย่างให้เป็นแอป CRUD ที่สมบูรณ์

ดู [ตัวอย่างจากงานจริง](/core/templates) ที่สร้างด้วย **Refine**

อ่าน [General Concepts](/core/docs/guides-concepts/general-concepts/) และ [Data Fetching](/core/docs/guides-concepts/data-fetching/) เพื่อเริ่มเข้าใจพื้นฐานของ Refine
