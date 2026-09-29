# 纸间 · 小票生成器

**把每一笔，整理成一张好看的小票。**

[在线使用](https://pomecro.github.io/zhijian-receipt/) · [项目仓库](https://github.com/Pomecro/zhijian-receipt)

纸间是一款简洁的小票制作工具。自由编辑项目、金额与票面内容，自动计算总额，即时预览并导出高清 PNG。无需注册。

## 功能亮点

- **实时双栏预览**：同时查看完整小票与可独立滚动的票面细节。
- **自动计算金额**：添加、编辑或删除项目时自动更新小计与总额，支持负数抵扣和自定义加急倍数。
- **自定义折扣**：填写 0–10 折，最多两位小数，默认 0。折扣系数为填写值 ÷ 10，例如 8 折乘以 0.8、10 折乘以 1、0 折乘以 0。「显示」位于「加急费前折扣」左侧。默认关闭「显示」：折扣不参与计算、不出现在小票中，右侧按钮变灰不可用；开启后启用并显示折扣。勾选「加急费前折扣」时，仅对加急前的项目小计打折，加急费按原价计算；未勾选时，对含加急费的总价打折。例如原价 100、加急倍数 1.2、5 折：勾选时为 100 × 0.5 + 20 = 70；未勾选时为 120 × 0.5 = 60。每一步均四舍五入至两位小数。小票始终先显示加急费，再显示折扣，明细与合计一致。关闭加急费时，两种模式均只对项目小计打折。
- **物体「件」单位**：在「货币与语言」中选择 **物体 · 简体中文（件）**，界面使用简体中文，输入框、项目明细、小计、加急费、折扣和最终合计均使用「件」，按 `100.00 件` 显示，金额栏改为数量栏。允许两位小数；切换单位保留原有数值，不进行换算。
- **八种货币选项与地区语言**：人民币（CNY / ¥，简体中文）、新台币（TWD / NT$，台湾繁体中文）、港币（HKD / HK$，香港繁体中文）、FF14 简中服金币（GIL / 金币，简体中文）、FF14 繁中服 gil（GIL / gil，繁体中文）、美元（USD / $，English）、日元（JPY / ¥，日本語）和韩元（KRW / ₩，한국어）。首次打开和重置时默认人民币。切换时，界面、提示、小票固定文字，以及尚未自行修改的默认抬头、项目和备注都会使用对应语言；货币符号与缩写也会同步更新。台湾与香港分别采用「上传／上载」「社群媒体／社交媒体」「宽度／阔度」「急件费／特快处理费」等地区用语，不会只替换繁简字形。金额数值不变，不进行汇率换算。自行填写的抬头、副标题、项目、备注和页脚，以及上传图片中的文字均保留原样。GIL 是游戏内货币的显示单位，不是 ISO 法定货币代码；两个 FF14 服务器分别以 FF14_CN 和 FF14_TW 储存。
- **自由编辑内容**：自定义抬头、时间范围、项目、备注、页脚，以及大标题下方的副标题；副标题默认为 `RECEIPT`，也可改成任意文字或留空隐藏。
- **顶部与尾部图片**：分别上传图片，按比例适配票宽，不裁剪。
- **自动本地暂存**：在同一浏览器和网址下恢复编辑内容、所选货币与图片；兼容较早版本的暂存数据。
- **高清 PNG 导出**：完整导出票面，不受预览缩放或滚动位置影响。
- **一键重置与响应式布局**：恢复人民币和默认票面内容，并适配桌面与手机浏览器。

## 如何使用

1. 打开网站，选择货币与语言，并填写小票抬头、副标题和时间范围。
2. 添加项目名称与金额（「件」模式为数量），按需开启加急费、折扣的「显示」和备注。
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
- **Custom discount:** Enter 0–10 with up to two decimal places; the default is 0. The multiplier is the entered value divided by 10. “Show” appears to the left of “Discount on pre-rush price”. With “Show” off, the discount is inactive and hidden, and the other checkbox is disabled. When enabled, selecting “Discount on pre-rush price” discounts only the original subtotal, keeping the rush fee calculated from the original price. Leaving it unchecked discounts the total including the rush fee. For a subtotal of 100, a rush multiplier of 1.2, and a discount value of 5, the selected mode gives 100 × 0.5 + 20 = 70; the unselected mode gives 120 × 0.5 = 60. Each step is rounded to two decimal places. The receipt always prints the rush fee before the discount. Both modes discount only the subtotal when rush fees are disabled.
- **Object count unit:** Choose **物体 · 简体中文（件）** in Currency & language for a Simplified Chinese interface using 件 on every input and printed amount, including line items, subtotal, rush fee, discount, and total. Values appear as `100.00 件`, and the amount column becomes a quantity column. Two decimal places remain supported. Switching preserves numeric values without conversion.
- **Eight currency options and regional languages:** CNY / ¥ (Simplified Chinese), TWD / NT$ (Taiwan Traditional Chinese), HKD / HK$ (Hong Kong Traditional Chinese), FF14 Simplified Chinese server gold / 金币 (GIL, Simplified Chinese), FF14 Traditional Chinese server gil (GIL, Traditional Chinese), USD / $, JPY / ¥, and KRW / ₩. CNY is selected on a fresh visit and after reset. Switching updates the interface, messages, fixed receipt labels, untouched examples, currency symbol, and display code. Taiwan and Hong Kong use distinct regional wording rather than a script-only conversion. User-entered titles, subtitles, items, notes, and footer text remain unchanged, as does text within uploaded images. Numeric amounts stay the same; no exchange-rate conversion is performed. GIL is an in-game currency label, not an ISO fiat code. The two server options are stored separately as FF14_CN and FF14_TW.
- **Editable receipt text:** Customize the title, service period, line items, notes, footer, and subtitle beneath the main title. The subtitle defaults to `RECEIPT`; enter your own text or leave it blank to hide it.
- **Header and footer images:** Upload separate images; each scales proportionally to the receipt width without cropping.
- **Automatic local drafts:** Restore your content, selected currency, and images in the same browser at the same address. Earlier draft formats are supported.
- **High-resolution PNG export:** Export the full receipt regardless of preview zoom or scroll position.
- **One-click reset and responsive layout:** Restore the default Chinese receipt in CNY, and use the app on desktop or mobile browsers.

## How to use

1. Open the app, select a currency and language, and enter the receipt title, subtitle, and service period.
2. Add item names and amounts (quantities in 件 mode); enable the rush fee, discount “Show”, or notes as needed.
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
