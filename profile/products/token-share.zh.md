[← 返回 zuuzii](https://github.com/zuuzii-org) · [官网 ↗](https://zuuzii.com) · [English](token-share.md) · **中文**

# 🔀 Token Share

**本地网关 —— 任意客户端接任意模型。**

![状态](https://img.shields.io/badge/状态-已上线-brightgreen)
![平台](https://img.shields.io/badge/平台-本地-444444)
[![访问](https://img.shields.io/badge/访问-token__share-3c5a3a)](https://zuuzii.com/productions/token-share/)

<img alt="Token Share —— 本地 LLM API 网关" src="../assets/products/token-share/cover.png" width="100%">

---

## 这是什么

Token Share 是一个完全本地运行的 LLM API 网关:把任意客户端指向一个本地端点,就能访问任意厂商和模型。它在 OpenAI 与 Anthropic 两套协议之间实时互译,让为某一种 API 格式开发的工具也能无缝调用另一种格式。流式输出全程畅通,而且一切都在你自己的机器上运行——API 密钥永远不会离开本地。它专为同时在多个模型、多个客户端之间切换的开发者打造,用一个稳定的本地地址统管全部。

## 为什么做它

如今的开发者手里跑着十几个客户端,还要追着不断更新的模型清单,但每个工具说着不同的协议、要不同的密钥,连"换个模型"都变成了重写配置的苦差事。Token Share 把这种混乱收敛成一个本地端点,实时完成协议互译。它的存在,是为了让你在几秒内切换厂商或模型,无需改动代码,也无需把密钥交到第三方手里。

## 功能特性

- **通用协议桥接** — 在 OpenAI 与 Anthropic 格式之间实时互译,任意客户端都能调用任意厂商,无需改动一行代码。
- **单一本地端点** — 把所有客户端指向一个自托管地址,就能触达背后的每一个模型——一个 URL 统管你的整套 LLM 技术栈。
- **密钥永不出门** — 全程本地运行,API 密钥始终留在你的机器上,绝不接触任何第三方服务器。
- **端到端流式** — 逐 token 的流式输出从厂商一路畅通到客户端,完整保留应用所依赖的实时响应体验。
- **秒级切换厂商** — 只需在网关侧改一处配置,即可在几秒内切换模型或厂商,无需逐个重构你的客户端。
- **任意客户端任意模型** — 工具与模型自由组合,为某种 API 开发的客户端,如今可以驱动另一个生态里的模型。
- **生于自托管** — 完全运行在你自己的基础设施上,带来完全掌控、零厂商锁定,数据不出边界。

## 使用场景

- 用它让只懂 OpenAI API 的客户端调用 Anthropic 模型——或反过来——且无需改动代码。
- 用它在网关处切换模型,即可对同一条提示词做跨厂商 A/B 测试,而不必逐个应用改配置。
- 用它把请求路由到多个云端 LLM 厂商,同时让 API 密钥始终保留在本地。
- 用它为整支工具与 IDE 插件团队提供一个稳定的本地端点,告别一堆各自为政的客户端配置。
- 用它将代码库从一个厂商逐步迁移到另一个,无需提前重写客户端集成。
- 用它通过单一代理逐 token 地流式传输长回复,任何客户端都能直接消费。

## 适合谁

- 同时在多个 LLM 模型与客户端之间周旋、想用一个端点统管全部的开发者。
- 工具锁定在某一种 API 格式、却需要触达另一种格式模型的工程师。
- 注重隐私、坚决不让 API 密钥离开本机的构建者。
- 在对比厂商与模型、希望切换时无需重写集成的团队。
- 想对 LLM 路由层拥有完全本地掌控权的自托管爱好者。

## 为什么选它

Token Share 的独到之处,在于把 OpenAI-Anthropic 实时协议互译与严格的本地化部署合二为一:你既获得跨协议的自由,又无需把密钥交给托管中间商。相比云端的 LLM 代理与路由服务,Token Share 全程自托管,请求数据与凭证都不会离开你的机器。它最适合那些需要"任意客户端调用任意模型",又想在一个网关里同时拥有流式、简洁与隐私的开发者。

## 常见问题

<details><summary>Token Share 是什么?</summary><br>Token Share 是一个本地、自托管的 LLM API 网关。把任意客户端指向一个本地端点,它就在 OpenAI 与 Anthropic 协议之间实时互译,让任意客户端触达任意厂商和模型。</details>
<details><summary>我的 API 密钥会离开本机吗?</summary><br>不会。Token Share 完全本地运行,你的 API 密钥永远留在自己的机器上,绝不会发送到任何第三方服务器。</details>
<details><summary>它支持流式输出吗?</summary><br>支持。流式全程贯通,逐 token 的回复从厂商一路畅通地传到你的客户端。</details>
<details><summary>只支持 OpenAI 的客户端能用 Anthropic 模型吗?</summary><br>可以,这正是它的核心用途。Token Share 实时在 OpenAI 与 Anthropic 格式之间互译,为一种协议开发的客户端也能调用说另一种协议的模型。</details>
<details><summary>我该如何切换厂商或模型?</summary><br>你只需在网关侧改配置,而不必逐个客户端修改。由于所有客户端都已指向同一个本地端点,切换厂商或模型只需几秒,且无需改动代码。</details>
<details><summary>Token Share 适合谁?</summary><br>它专为同时在多个模型与客户端之间切换的开发者打造,用一个本地 LLM 网关统一协议、守护隐私,并让切换厂商变得轻而易举。</details>
<details><summary>Token Share 是自托管的吗?</summary><br>是的。Token Share 是一个完全运行在你自己机器上的自托管 LLM 网关,让你拥有完全的本地掌控,数据与凭证都不会离开你的环境。</details>

<br>

<img alt="Token Share —— 概览" src="../assets/products/token-share/promo.png" width="100%">

<sub>**关键词** · 本地 LLM 网关, OpenAI Anthropic 协议互译, LLM API 代理, 任意客户端任意模型, 自托管 LLM 网关, 切换 LLM 厂商, 本地 LLM 端点, LLM 协议桥接, 流式 LLM 代理, API 密钥隐私</sub>

---

<sub>**[zuuzii](https://github.com/zuuzii-org)** 旗下 · [zuuzii.com](https://zuuzii.com) · hi@zuuzii.com</sub>
