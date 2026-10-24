# 前端 / 跨端 UI 引擎

11 年开发经验。主线是一套自研 UI 内核：信号驱动的 **mve** 为核，向上长出类 React 的 **better-react**，向下移植到 **Kotlin + Skia** 与 **Rust + Vello**——同一套响应式模型与布局思路，在三个语言上各实现一遍。另有独立技术线：自研对象消息语言 **ooc**。

## 内核

- **[mve](https://github.com/wy2010344/mve)** — 信号驱动 UI 内核：最小响应式核心（批量更新）+ DOM 渲染 + 函数式组件模型；配套 50+ 交互 demo
- **[better-react](https://github.com/wy2010344/better-react)** — 内核之上的类 React 语义层：函数式、无 JSX，统一组件与 hooks
- **[wy-helper-kotlin](https://github.com/wy2010344/wy-helper-kotlin)** — mve 的 Kotlin + Skia 移植，自研 Flex / Stack 布局与文字排版，292 tests · CI 全绿
- **[rust-mve](https://github.com/wy2010344/rust-mve)** — mve 的 Rust + Vello 移植，自研一维布局（零 Taffy 依赖）+ `rsx!` 声明式宏

## 独立技术线

- **[ooc](https://github.com/wy2010344/ooc)** — 自研对象消息语言 + 完整工具链（解析 / 解释器 / 类型检查 / LSP / 代码生成 / 浏览器运行时），含在线 Playground 与行情终端 Demo

## 工程与微前端

- **[es-pseudo-monorepo](https://github.com/wy2010344/es-pseudo-monorepo)** — pnpm + turbo + changesets 多包底座，npm 发布 30+ 包
- **[module-federation-demo](https://github.com/wy2010344/module-federation-demo)** — Module Federation 循环依赖验证，3 个线上 demo

TypeScript · Rust · Kotlin · Java · Dart ｜ React / Vue / Flutter / 微信小程序 ｜ Canvas / Skia / GPU 渲染 ｜ 桌面端（Rust·iced / Kotlin Multiplatform）
