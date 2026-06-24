[← 返回 zuuzii](https://github.com/zuuzii-org) · [官网 ↗](https://zuuzii.com) · [English](token-share.md) · **中文**

# 🔀 Token Share

**本地网关 —— 任意客户端接任意模型。**

![状态](https://img.shields.io/badge/状态-已上线-brightgreen)
![平台](https://img.shields.io/badge/平台-本地-444444)
[![访问](https://img.shields.io/badge/访问-token__share-3c5a3a)](https://zuuzii.com/productions/token-share/)

<img alt="Token Share —— 本地 LLM API 网关" src="../assets/products/token-share/cover.png" width="100%">

---

## 一句话说明

**Token Share 是一个完全本地运行的 LLM API 网关:它对外只暴露一个端点,实时在 OpenAI 与 Anthropic 两套协议之间互译,让任意客户端都能调用任意服务商或模型——而你的 API 密钥永远不会离开本机。**

把工具指向 `localhost`,剩下的交给 Token Share。

## 问题在哪

每个客户端只会说一种方言,每个服务商又说另一种。你的编辑器想发 OpenAI 格式的请求,而你真正想用的模型却只认 Anthropic——或者反过来。于是你只能维护一抽屉的适配器、转换脚本和脆弱的代理程序,把同一份密钥反复粘进五个配置文件,还得祈祷它别泄露。换模型就得换工具,换工具就得把一切重新接线。

Token Share 把这一团乱麻收敛成一次本地跳转。

## 改造前 / 改造后

| 没有 Token Share | 有了 Token Share |
| --- | --- |
| 每个客户端被锁死在某一服务商的协议上 | 一个端点同时会说 OpenAI 和 Anthropic |
| API 密钥粘进每个应用的配置里 | 密钥集中存放,永不离开本机 |
| 换模型 → 客户端重新接线 | 换模型 → 改一行就够 |
| 协议不匹配 = 集成直接报废 | 实时互译填平协议鸿沟 |
| 流式输出在适配器间断裂 | 流式输出端到端完整保留 |

## 能力清单

- **协议实时互译。** OpenAI ⇄ Anthropic 的请求与响应结构即时转换,不攒批、不假装缓冲。
- **一个端点,通吃所有客户端。** 编辑器、命令行、脚本、Agent 全部指向同一个本地 URL。
- **服务商无关路由。** 任意客户端都能触达网关后面任意受支持的服务商或模型。
- **端到端流式。** 逐 token 的输出穿过翻译层依旧完好。
- **本地优先设计。** 网关跑在你自己的机器上,凭证与流量都留在本地。
- **零锁定。** 切换模型或服务商,完全不必动客户端配置。

## 规格速览

| | |
| --- | --- |
| **协议** | OpenAI ⇄ Anthropic,实时互译 |
| **客户端** | 任意兼容 OpenAI 或 Anthropic 的工具 |
| **流式** | 端到端支持 |
| **部署** | 完全本地——运行在你自己的机器上 |
| **API 密钥** | 永不离开本机 |
| **适用人群** | 在多模型、多客户端之间来回切换的开发者 |

## 开发者真正会问的问题

<details><summary>我的 API 密钥会离开本机吗?</summary><br>不会。网关完全本地运行,密钥在本机存储和使用,流量经由你自己的进程转发,不会被送往任何第三方中继。</details>

<details><summary>只支持 OpenAI 的客户端能用上 Anthropic 模型吗?</summary><br>能——这正是它存在的意义。Token Share 实时在两套协议之间互译,只会说 OpenAI 的客户端可以触达 Anthropic 模型,反之亦然。</details>

<details><summary>经过网关后,流式还正常吗?</summary><br>正常。流式输出端到端保留,token 边到达边穿过翻译层,而不是等整段响应落地后才吐出。</details>

<details><summary>客户端里我要改什么?</summary><br>只改 base URL。把它指向本地的 Token Share 端点,而不是服务商地址。大多数兼容 OpenAI 或 Anthropic 的工具改这一处就够了。</details>

<details><summary>换模型需要把所有东西重新配一遍吗?</summary><br>不需要。因为客户端始终只跟那一个本地端点对话,底层服务商或模型怎么换,都不会反向波及你的工具。</details>

<sub>Token Share 是面向开发者的本地 LLM API 网关与协议桥。它不存储你的流量,也不会把 API 密钥传出本机。</sub>

<img alt="Token Share —— 概览" src="../assets/products/token-share/promo.png" width="100%">

<sub>**关键词** · 本地 LLM API 网关, OpenAI Anthropic 协议互译, 本地 LLM 代理, API 密钥本地隐私, 多模型客户端路由, 流式 LLM 网关, 开发者 LLM 工具, 一键切换模型</sub>

---

<sub>**[zuuzii](https://github.com/zuuzii-org)** 旗下 · [zuuzii.com](https://zuuzii.com) · hi@zuuzii.com</sub>
