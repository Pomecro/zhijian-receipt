# 纸间 · 小票生成器

**把每一笔，整理成一张好看的小票。**

[在线使用](https://pomecro.github.io/zhijian-receipt/) · [项目仓库](https://github.com/Pomecro/zhijian-receipt)

纸间是一款简洁的小票制作工具。自由编辑项目、金额与票面内容，自动计算总额，即时预览并导出高清 PNG。无需注册。

## 功能亮点

- **实时双栏预览**：同时查看完整小票与可独立滚动的票面细节。
- **自动计算金额**：添加、编辑或删除项目时自动更新小计与总额，支持负数抵扣和自定义加急倍数。
- **四种货币与语言**：人民币（CNY，简体中文）、美元（USD，English）、日元（JPY，日本語）和韩元（KRW，한국어），默认人民币。切换时同步更新界面与小票上的固定文字、货币符号和代码；不会进行汇率换算，金额数值保持不变。
- **自由编辑内容**：自定义抬头、时间范围、项目、备注、页脚，以及大标题下方的副标题；副标题默认为 `RECEIPT`，也可改成任意文字或留空隐藏。
- **顶部与尾部图片**：分别上传图片，按比例适配票宽，不裁剪。
- **自动本地暂存**：在同一浏览器和网址下恢复编辑内容、所选货币与图片；兼容较早版本的暂存数据。
- **高清 PNG 导出**：完整导出票面，不受预览缩放或滚动位置影响。
- **一键重置与响应式布局**：恢复人民币和默认票面内容，并适配桌面与手机浏览器。

## 如何使用

1. 打开网站，选择货币与语言，并填写小票抬头、副标题和时间范围。
2. 添加项目名称与金额，按需开启加急费和备注。
3. 按需上传顶部图片或尾部图片。
4. 检查预览，点击 **保存小票 PNG**。

支持 PNG、JPG、WebP 图片；单张不超过 20 MB，高度不超过宽度的 8 倍。

## 本地暂存与隐私

小票文字保存在浏览器 `localStorage`，图片保存在 `IndexedDB`。小票内容和导入图片都在浏览器本地处理，不会由应用上传到服务器。

暂存不会跨设备、跨浏览器或跨网址同步。清除网站数据、使用隐私浏览或受到浏览器存储限制时，暂存内容可能无法恢复。需要长期保存的小票，请导出 PNG。

## 文件结构

| 文件 | 用途 |
| --- | --- |
| `index.html` | 完整静态网页，包含界面、样式、语言切换、图片处理和 PNG 导出 |
| `README.md` | 项目介绍与功能说明 |

## 技术实现

使用原生 HTML、CSS、JavaScript 与 Canvas。无需构建步骤或第三方运行时依赖。网页绘制、图片处理和 PNG 导出均在浏览器本地完成。

## 作者

[Pomecro](https://github.com/Pomecro)

---

# Paper · Receipt Generator

**Turn every line item into a beautifully finished receipt.**

[Open the app](https://pomecro.github.io/zhijian-receipt/) · [Source repository](https://github.com/Pomecro/zhijian-receipt)

Paper is a simple receipt maker. Edit line items, amounts, and receipt text; totals update automatically. Preview the receipt as you work and export a high-resolution PNG. No account is required.

## Features

- **Live two-panel preview:** See the complete receipt and scroll through its details independently.
- **Automatic totals:** Add, edit, or remove line items and see the subtotal and total update instantly. Negative amounts can be used for deductions, and the rush multiplier is adjustable.
- **Four currencies and languages:** Chinese yuan (CNY, Simplified Chinese), US dollar (USD, English), Japanese yen (JPY, Japanese), and Korean won (KRW, Korean). CNY is selected by default. Changing the selection updates the interface, fixed receipt labels, currency symbol, and code. Amounts are not converted and their numeric values stay the same.
- **Editable receipt text:** Customize the title, service period, line items, notes, footer, and subtitle beneath the main title. The subtitle defaults to `RECEIPT`; enter your own text or leave it blank to hide it.
- **Header and footer images:** Upload separate images; each scales proportionally to the receipt width without cropping.
- **Automatic local drafts:** Restore your content, selected currency, and images in the same browser at the same address. Earlier draft formats are supported.
- **High-resolution PNG export:** Export the full receipt regardless of preview zoom or scroll position.
- **One-click reset and responsive layout:** Restore the default Chinese receipt in CNY, and use the app on desktop or mobile browsers.

## How to use

1. Open the app, select a currency and language, and enter the receipt title, subtitle, and service period.
2. Add item names and amounts; enable the rush fee or notes as needed.
3. Add a header or footer image if desired.
4. Review the preview and select **Save receipt PNG**.

PNG, JPG, and WebP images are supported. Each image must be under 20 MB, and its height must not exceed eight times its width.

## Local drafts and privacy

Receipt text is saved in browser `localStorage`; images are saved in `IndexedDB`. Receipt content and imported images are processed locally in the browser and are not uploaded to a server by the app.

Drafts do not sync across devices, browsers, or website addresses. Clearing site data, using private browsing, or browser storage restrictions may prevent drafts from being restored. Export a PNG to keep a receipt long term.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | Complete static app, including the interface, styles, language switching, image handling, and PNG export |
| `README.md` | Project introduction and feature guide |

## Implementation

Built with vanilla HTML, CSS, JavaScript, and Canvas. No build step or third-party runtime dependencies are required. Receipt rendering, image handling, and PNG export run locally in the browser.

## Author

[Pomecro](https://github.com/Pomecro)
