[← zuuzii](https://github.com/zuuzii-org) · [Website ↗](https://zuuzii.com) · **English** · [中文](token-share.zh.md)

# 🔀 Token Share

**Local gateway — any client, any model.**

![status](https://img.shields.io/badge/status-LIVE-brightgreen)
![platform](https://img.shields.io/badge/platform-Local-444444)
[![Open](https://img.shields.io/badge/Open-token__share-3c5a3a)](https://zuuzii.com/productions/token-share/)

<img alt="Token Share — local LLM API gateway" src="../assets/products/token-share/cover.png" width="100%">

---

## What it is

Token Share is a fully local LLM API gateway that lets you point any client at a single local endpoint and reach any provider or model. It translates between the OpenAI and Anthropic protocols in real time, so a tool built for one API format can talk seamlessly to the other. Streaming works end-to-end, and because everything runs on your own machine, your API keys never leave it. It is built for developers who juggle multiple models and multiple clients and want one stable address to rule them all.

## Why it exists

Modern developers run a dozen clients and chase a moving target of models, but every tool speaks a different protocol and expects a different API key, turning "just switch the model" into a config rewrite. Token Share collapses that chaos into one local endpoint that translates protocols on the fly. It exists so you can change providers or models in seconds without changing your code, and without ever shipping your keys to a third party.

## Features

- **Universal Protocol Bridge** — Translates between OpenAI and Anthropic formats in real time, so any client can talk to any provider without rewriting a single line of code.
- **One Local Endpoint** — Point every client at a single self-hosted address and reach every model behind it — one URL to rule your entire LLM stack.
- **Keys Never Leave Home** — Everything runs locally, so your API keys stay on your machine and never touch a third-party server.
- **End-to-End Streaming** — Token-by-token streaming flows cleanly from provider to client, preserving the responsive, real-time feel your apps depend on.
- **Instant Provider Switching** — Swap models or providers in seconds by changing config at the gateway, not by re-engineering every client you own.
- **Any Client, Any Model** — Mix and match tools and models freely — a client built for one API can now drive a model from an entirely different ecosystem.
- **Self-Hosted by Design** — Runs entirely on your own infrastructure, giving you full control, zero vendor lock-in, and no data leaving your perimeter.

## Use cases

- Use it to drive an Anthropic model from a client that only speaks the OpenAI API — or vice versa — with zero code changes.
- Use it to A/B test the same prompt across providers by switching the model at the gateway instead of in every app.
- Use it to keep your API keys fully local while still routing requests to multiple cloud LLM providers.
- Use it to give a whole team of tools and IDE plugins one stable local endpoint instead of a tangle of per-client configs.
- Use it to migrate a codebase from one provider to another gradually, without rewriting client integrations up front.
- Use it to stream long completions token-by-token through a single proxy that any client can consume.

## Who it's for

- Developers juggling multiple LLM models and clients who want one endpoint to manage them all.
- Engineers building tools locked to one API format who need to reach models on the other.
- Privacy-conscious builders who refuse to let their API keys leave their own machine.
- Teams comparing providers and models who want to switch without rewriting integrations.
- Self-hosting enthusiasts who want full local control over their LLM routing layer.

## Why choose it

What sets Token Share apart is the combination of real-time OpenAI-Anthropic protocol translation and a strictly local footprint: you get cross-protocol freedom without surrendering your keys to a hosted middleman. Compared with cloud-based LLM proxies and routers, Token Share keeps everything self-hosted, so no request data and no credentials ever leave your machine. It is best for developers who need any client to talk to any model and want streaming, simplicity, and privacy in one gateway.

## FAQ

<details><summary>What is Token Share?</summary><br>Token Share is a local, self-hosted LLM API gateway. You point any client at one local endpoint and it translates between the OpenAI and Anthropic protocols in real time, letting any client reach any provider or model.</details>
<details><summary>Do my API keys leave my machine?</summary><br>No. Token Share runs fully locally, so your API keys never leave your own machine and are never sent to any third-party server.</details>
<details><summary>Does it support streaming responses?</summary><br>Yes. Streaming is supported end-to-end, so token-by-token completions flow from the provider all the way through to your client.</details>
<details><summary>Can an OpenAI-only client use an Anthropic model?</summary><br>Yes. That is the core purpose. Token Share translates between OpenAI and Anthropic formats on the fly, so a client built for one protocol can call a model that speaks the other.</details>
<details><summary>How do I switch providers or models?</summary><br>You change the configuration at the gateway rather than in each client. Because every client already points at the same local endpoint, switching providers or models takes seconds and requires no code changes.</details>
<details><summary>Who is Token Share for?</summary><br>It is built for developers juggling multiple models and clients who want a single local LLM gateway to unify protocols, preserve privacy, and make switching providers effortless.</details>
<details><summary>Is Token Share self-hosted?</summary><br>Yes. Token Share is a self-hosted LLM gateway that runs entirely on your own machine, giving you full local control with no data or credentials leaving your environment.</details>

<br>

<img alt="Token Share — overview" src="../assets/products/token-share/promo.png" width="100%">

<sub>**Keywords** · local LLM gateway, OpenAI Anthropic protocol translation, LLM API proxy, any client any model, self-hosted LLM gateway, switch LLM providers, local LLM API endpoint, LLM protocol bridge, streaming LLM proxy, API key privacy</sub>

---

<sub>Part of **[zuuzii](https://github.com/zuuzii-org)** · [zuuzii.com](https://zuuzii.com) · hi@zuuzii.com</sub>
