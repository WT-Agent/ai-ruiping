<div align="center">

# [网腾无限AI - AI锐评与毒舌分析]

**[一个支持神评打卡与五种特色吐槽流派的 AI 犀利锐评与现象解构工具，具备深色玻璃拟态自适应交互与微信端 H5 体验]**

[Vue 3] · [TypeScript] · [Vite] · [Vanilla CSS] · [开源协议 MIT]

[![GitHub stars](https://img.shields.io/github/stars/WT-Agent/ai-ruiping?style=social)](https://github.com/WT-Agent/ai-ruiping)
[![GitHub license](https://img.shields.io/github/license/WT-Agent/ai-ruiping)](https://github.com/WT-Agent/ai-ruiping/blob/main/LICENSE)

[在线演示](#在线演示) · [快速启动](#快速启动) · [参与贡献](#参与贡献) · [支持一下](#支持一下)

</div>

## 关于我们

团队成员均来自 C9 等顶尖学府，在字节、腾讯、阿里的工程师组成，全职创业研发开源 AI 应用产品，让所有人感受 AI 的魅力。

本项目旨在为职场黑话吐槽、网红现象解构、当代青年消费主义剖析及情感乱象评论群体提供高品质的 AI 锐评与毒舌分析服务。用户只需输入锐评对象与现象表现，AI 即可根据多维科学度看板自动输出毒舌金句定性、深层心理剖析、表情包梗图构想及反转解药建议。页面内置了支持搞笑蜂鸣发声的“神评加冕”打卡印章，供用户在解压吐槽时增加互动体验。

**我们不搞概念，不卖课，只写能跑起来的代码。**

欢迎 Star、Fork、提 Issue，一起让这个项目变得更好用。

核心特性：
- **极简自适应交互**：提供毛玻璃质感的深色玻璃拟态自适应 Web 界面，高度适配移动端 H5 微信浏览器与 PC 体验。
- **神评加冕印章 (Roast Stamp)**：基于前端 Web Audio API 动态合成搞笑蜂鸣发声，点击印章即可累积神评打卡次数并伴随渐隐上升动画。
- **五大锐评吐槽流派**：
  - **毒舌脱口秀**：金句频出、爆笑梗连连、节奏感极强，像脱口秀现场般一针见血戳中要害。
  - **互联网梗王**：大量融入当代网民梗、热词、社交名场面，幽默诙谐且极具网络传播力。
  - **哲学深度批判**：运用解构主义、社会学名词与深刻洞察，降维打击虚浮现象。
  - **战术级夸夸关怀**：先反向毒舌吐槽，随后出人意料地反转为温暖治愈的硬核肯定与鼓励。
  - **疯狂吐槽暴走**：情绪拉满、高能暴走吐苦水，节奏飞快、酣畅淋漓地宣泄情感。
- **AI 锐评质量看板**：自动提取 AI 回复中的共识数据，以简洁的单轨进度条在前端直观展示毒舌指数、幽默逗趣、洞察深度、梗度密集及反转张力。
- **演示案例与分享卡片**：内置 30 条不同主题的 AI 锐评与吐槽精彩演示样例，并支持一键卡片化截图分享。
- **一键零成本部署**：纯前端静态网页结构，支持零成本部署于 Vercel、GitHub Pages 或 CDN/OSS 静态托管服务。
- **安全开发代理**：本地开发支持使用个人 API 密钥发起代理请求，密钥由 Vite 服务器中转，无需担心前端泄露。
- **裂变解锁与留存**：内置微信朋友圈扫码分享拦截与额度重置机制，提升流量转化与留存。

## 快速启动

### 1. 克隆项目
```bash
git clone https://github.com/WT-Agent/ai-ruiping.git
cd ai-ruiping
```

### 2. 安装依赖
项目强制使用 pnpm 作为包管理器：
```bash
pnpm install
```

### 3. 配置本地开发环境变量
复制并修改环境变量配置文件：
```bash
cp .env.example .env
```
根据微应用的功能类型，在 `.env` 中配置您的开发者密钥：
- `DEEPSEEK_API_KEY`: 您的 DeepSeek 开发者 API 密钥（用于文本生成任务）
- `DASHSCOPE_API_KEY`: 您的通义千问/通义万相开发者 API 密钥（用于多模态与生图任务）

### 4. 启动本地开发服务
```bash
pnpm dev
```
启动成功后在浏览器访问控制台输出的地址即可。

### 5. 生产构建打包
```bash
pnpm build
```
打包后生成的 `dist` 目录即为纯静态网页资源，可直接上传部署。

## 脚手架集成说明

本模板由私有总控仓库 `ai.wuxian.xyz` 中的 `@wuxian/cli` 脚手架统一管理，支持以下批量运维操作：

### 初始化或更新单个子项目

```bash
node bin/cli.js ai-ruiping
```

脚手架将自动：
1. 读取子仓库的 `README.md` 首行作为 Prompt 主题。
2. 注入 Vue 3 静态页面结构及标准配置文件。
3. 保留原有的 `.git` 配置与 `README.md`，不覆盖个性化内容。

### 批量同步所有子项目

```bash
node bin/cli.js all
```

将模板 the latest 变更（如 SSO 逻辑、额度控制）一键同步至全部 31 个子项目。

### Agent 配置维护接口

```bash
# 读取子项目配置
node bin/cli.js get ai-ruiping

# 写入/更新配置（支持热更新 prompt、model、title、temperature 等）
node bin/cli.js set ai-ruiping prompt "你是一个顶级脱口秀主咖、互联网金句王兼犀利的社会学毒舌评论家..."
node bin/cli.js set ai-ruiping model deepseek-chat
```

## 联系方式

- GitHub Issues: [提交反馈](https://github.com/WT-Agent/ai-ruiping/issues)
- 邮箱: us@wuxian.xyz

## 打赏支持

如果本项目对您有帮助，欢迎请作者喝杯咖啡。您的支持是持续维护与更新的动力。

<div align="center">

**微信支付** | **支付宝**
:---:|:---:
<img src="./asset/tenpay.png" width="200" alt="微信支付"> | <img src="./asset/alipay.png" width="200" alt="支付宝">

</div>

## 版权与许可

本项目基于 MIT License 开源协议。

Copyright (c) 2026. All rights reserved.
