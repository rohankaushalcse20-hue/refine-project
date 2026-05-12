---
title: "Quickstart | Refine v5 快速上手"
display_title: "快速开始指南"
sidebar_label: "快速开始指南"
description: "通过浏览器 scaffolder 或 CLI 创建 Refine v5 项目，并进入后续学习路径。"
displayed_sidebar: mainSidebar
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import { Playground } from "@site/src/components/playground";

**Refine** 可以运行在任何支持 **React** 的环境中，包括 Vite、Next.js、Remix、CRA 等。

你当然可以手动安装依赖并自行搭建项目，但最快的入门方式通常是使用浏览器版 scaffolder 或 CLI。两种方式都可以在生成项目之前选择 framework、UI、data provider、authentication 和 i18n 方案。

## 使用 CLI

运行 `create-refine-app` 以交互式创建新的 **Refine** 项目。

```sh
npm create refine-app@latest
```

回答提示问题后，进入生成的目录，按需要安装依赖，并根据 CLI 给出的命令启动开发服务器。

## 使用浏览器

浏览器版 scaffolder 提供与 CLI 类似的核心选项，并且可以在下载前预览最终项目结构和界面效果。

<Playground />

## 下一步

前往 [Tutorial](/core/tutorial) 将起始项目扩展为完整 CRUD 应用，也可以浏览 [实战模板](/core/templates)，并继续阅读 [General Concepts](/core/docs/guides-concepts/general-concepts/) 与 [Data Fetching](/core/docs/guides-concepts/data-fetching/) 指南。
