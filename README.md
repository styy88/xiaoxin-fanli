# 💰 xinxin-fanli (xinxin返利)

[![AstrBot](https://img.shields.io/badge/AstrBot-v4.x-blue)](https://github.com/AstrBotDevs/AstrBot)
[![Python](https://img.shields.io/badge/Python-3.8+-yellow)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

这是一个专为 [AstrBot](https://github.com/AstrBotDevs/AstrBot) 框架开发的电商返利插件。完美适配 **`openclaw-weixin` (个人微信官方通道)** 和常规 QQ 平台。

只需向机器人发送包含淘宝或京东的商品文案、口令或链接，机器人便会自动解析，并极速返回带有你专属推广位的优惠信息与返利链接！

## ✨ 核心特性

- 🛍️ **双端平台支持**：支持淘宝/天猫（基于折淘客API）与京东（基于折京客 + 京推推API）。
- 💬 **微信个人号专属优化**：完美兼容 `openclaw-weixin` 通道，内置事件拦截（`stop_event`）机制。一旦识别到商品链接，返回返利信息后自动截断，**防止后端的 LLM (大语言模型) 出现乱回答或幻觉**。
- ⚙️ **全可视化配置**：无需手动修改代码或 JSON 文件！采用 AstrBot V4 最新标准，直接在 WebUI 管理面板中填写 API 秘钥，保存即时生效。
- ⚡ **异步极速响应**：底层采用 `aiohttp` 异步网络请求，附带严谨的超时处理，绝不卡死主线程，保证微信回复的及时性。

## 📦 安装指南

1. 进入你的 AstrBot 插件目录：
   ```bash
   cd AstrBot/data/plugins
