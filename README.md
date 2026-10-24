# 前端 / 跨端 UI 引擎

11 年开发经验。长期从零实现 UI 框架的底层：两条**完全独立**的框架路线——**mve**（信号驱动、细粒度更新）与 **better-react**（React 式更新、函数式无 JSX），除工具库 wy-helper（单仓两包：`wy-helper` / `wy-dom-helper`）外不共用任何实现；mve 再移植到 **Kotlin + Skia** 与 **Rust + Vello**。另有独立技术线：自研对象消息语言 **ooc**，通过 ooc-mve-bridge 以 mve 为 UI 运行时。

## 两条独立的框架路线

- **[mve](https://github.com/wy2010344/mve)** — 信号驱动 UI 框架（独立实现）：最小响应式核心 + 批量更新 + DOM 渲染 + 函数式组件模型；配套 50+ 交互 demo
- **[better-react](https://github.com/wy2010344/better-react)** — React 式更新 UI 框架（独立实现）：函数式、无 JSX，组件级重渲染
- **唯一复用层**：[wy-helper](https://github.com/wy2010344/wy-helper)（单仓两包：`wy-helper` / `wy-dom-helper`。纯工具库，无框架语义）

## 跨语言移植（mve）

- **[wy-helper-kotlin](https://github.com/wy2010344/wy-helper-kotlin)** — Kotlin + Skia 移植，自研 Flex / Stack 布局与文字排版，292 tests · CI 全绿
- **[rust-mve](https://github.com/wy2010344/rust-mve)** — Rust + Vello 移植，自研一维布局（零 Taffy 依赖）+ `rsx!` 声明式宏

## 独立技术线

- **[ooc](https://github.com/wy2010344/ooc)** — 自研对象消息语言 + 完整工具链（解析 / 解释器 / 类型检查 / LSP / 代码生成 / 浏览器运行时）；通过 ooc-mve-bridge 以 mve 为 UI 运行时，含在线 Playground 与行情终端 Demo

## 工程与微前端

- **[es-pseudo-monorepo](https://github.com/wy2010344/es-pseudo-monorepo)** — pnpm + turbo + changesets 多包底座，npm 发布 30+ 包
- **[module-federation-demo](https://github.com/wy2010344/module-federation-demo)** — Module Federation 循环依赖验证，3 个线上 demo

TypeScript · Rust · Kotlin · Java · Dart ｜ React / Vue / Flutter / 微信小程序 ｜ Canvas / Skia / GPU 渲染 ｜ 桌面端（Rust·iced / Kotlin Multiplatform）
