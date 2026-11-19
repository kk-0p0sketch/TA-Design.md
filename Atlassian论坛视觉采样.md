# Atlassian Community Forums · 栅格、留白与组件状态

2026-11-19 在 Chrome 的隔离访客配置中打开论坛首页，通过已安装的 **Design System Extractor** 与官方 **Chrome DevTools MCP 1.13.0** 读取实际渲染结果。论坛主内容为英文，浏览器语言为中文。测量前关闭可选 Cookie 提示，等待帖子、快捷入口与字体加载完成。[论坛首页](https://community.atlassian.com/forums) · [本次测量 JSON](Atlassian论坛视觉采样.json) · [Portal 规范](DESIGN.md)

## 左右空间

1440 px 桌面的工作区最大宽度为 **1232 px**，居中后两侧各留 **104 px**。帖子主栏宽 813 px，辅助栏宽 395 px。两栏实际相隔 **24 px**。帖子标题和卡片组比主栏左缘再向右 4 px，快捷入口标题与辅助栏对齐，因此从两个标题盒边缘量出的距离是 20 px。区分这两组数字，可以同时还原页面栅格与内容的视觉对齐。

| 视口 W × H | 工作区 x / 宽 | 主栏 x / 宽 | 辅助栏 x / 宽 | 栏间净距 | 标题左缘 主 / 辅 |
|---|---:|---:|---:|---:|---:|
| 1440 × 960 | 104 / 1232 | 104 / 813 | 941 / 395 | 24 | 108 / 941 |
| 1280 × 900 | 24 / 1232 | 24 / 813 | 861 / 395 | 24 | 28 / 861 |
| 1024 × 900 | 36 / 952 | 36 / 678 | 730 / 258 | 16 | 40 / 730 |
| 776 × 900 | 36 / 704 | 36 / 430 | 482 / 258 | 16 | 40 / 482 |
| 775 × 900 | 36 / 703 | 36 / 703 | 36 / 703，移到下方 | — | 40 / 36 |
| 768 × 900 | 36 / 696 | 36 / 696 | 36 / 696，移到下方 | — | 40 / 36 |
| 390 × 844 | 16 / 358 | 16 / 358 | 16 / 358，移到下方 | — | 20 / 16 |

单位均为 CSS px，x 从视口左边缘起算。两栏共同父级使用 flex，其 computed `gap` 为 `normal`。表中栏距来自辅助栏左缘减去主栏右缘。在同一窗口按 775、776、775、776 px 切换，四次结果均符合上表。手机的 390 × 844 是固定 CSS 视口，启用触摸输入并核对了截图自身的像素尺寸。

桌面和手机均滚到帖子区，保持 “Recent Posts” 出现在屏幕同一纵向位置。副栏包含欢迎模块、快捷入口和热门标签，单列时整体排到帖子之后。[桌面原站](Atlassian论坛-桌面.png) · [手机原站](Atlassian论坛-手机.png)

## 元素、尺寸与纵向留白

| 取样元素 | 桌面 1440 px | 手机 390 px |
|---|---|---|
| 页面专题 H1 | Charlie Display 字体栈，56/64 px、700，颜色 `#292A2E` | 24/32 px、700 |
| 帖子分区 H2 | 20/28 px、653 | 20/28 px、653 |
| 第一条帖子标题 | 24/32 px、600 | 20/24 px、600 |
| 首帖白色表面 | 圆角 8 px，内边距 24 px，内部纵向 gap 16 px | 圆角 8 px、内边距 24 px、内部 gap 16 px |
| 欢迎模块 | 白底，圆角 8 px、内边距 24 px。辅助栏内各模块之间 gap 32 px | 圆角 6 px，内边距 24 px |
| 搜索输入文字 | Inter 字体栈，16/24 px、400，`#172B4D` | 16/24 px、400 |
| “Filters” 控件 | 高 36 px，圆角 4 px，内边距 6 px × 12 px，内间距 6 px | 高 36 px，圆角 4 px，内边距 6 px × 12 px |

桌面 “Recent Posts” 标题盒底部与筛选按钮顶端相隔 16 px，筛选按钮底部到第一张帖子卡顶端相隔 16 px。字号/行高取自计算样式；表中空间取自实际盒边缘。两者分开读取，因为字形裁切会让标题的实际外框小于 CSS 行高。

## 组件状态

| 操作 | 浏览器中的反馈 |
|---|---|
| 指针停在帖子标题上 | 文字从 `#292A2E` 变为 `#1868DB`，保持无下划线。指针移到同一张卡片的正文，标题恢复墨色。两次观测中卡片均保持白底与原有阴影。 |
| 键盘 Tab 到达帖子标题 | 链接获得焦点，出现 2 px 实线 `#4688EC`，offset 0 px。 |
| Filters 默认 → 悬停 | 默认透明背景、1 px 边框 `rgba(11,18,14,.14)`。悬停背景变为 `#F8F8F8`，边框变为 `#7D818A`。 |
| 键盘 Tab 到达 Filters | 控件出现 2 px 实线 `#4688EC`，offset 2 px。 |
| 点击 Filters | 打开名为 “Filter Posts” 的模态框，尺寸 375 × 365 px，白底、8 px 圆角，焦点进入标题。包含 Post Type、Post Status、Tags 三项条件以及 Clear All、Apply。 |
| 按 Escape | 关闭模态框，焦点返回 Filters，键盘焦点环可见。 |

焦点记录同时检查 `document.activeElement` 和 `:focus-visible`。原站按钮没有提供 `aria-expanded`，所以用可访问性树中模态框的出现和消失验证开合。[筛选展开截图](Atlassian论坛-筛选.png) · [逐状态色值和边界](Atlassian论坛视觉采样.json)

## 如何应用到 Portal

用“先主内容、后辅助信息”的阅读顺序安排工具列表和右栏，用实际栏距来实现栅格，再在列表内部统一图标与正文的起点。触摸视口上，搜索和工具名称优先占满可用宽度。色彩只借用角色分工，链接、选中态与键盘焦点使用 Portal 紫色，主行动保持墨色；文字用 Geist Sans，导航、搜索、工具条目用 Lucide。Portal 的断点、行高、圆角及交互取值以团队规范为准。[Portal 规范](DESIGN.md)

## 复测方法

1. 通过 Chrome DevTools MCP 的 `navigate_page`、`wait_for` 和 `take_snapshot` 定位 “Recent Posts” 与 “Quick Links”，取两者最近的共同祖先为工作区，取各自最近的 `.panelArea` 为主栏与辅助栏。
2. 使用 `resize_page` 与 `emulate` 指定视口；读取 `innerWidth`、`innerHeight` 与 DPR。字体稳定后，在 scrollY = 0 通过 `evaluate_script` 读取元素 `getBoundingClientRect()` 与 `getComputedStyle()`。
3. 用 `hover`、`press_key`、`click` 触发真实交互，再读取颜色、轮廓与焦点归属。桌面和手机的 “Recent Posts” 均距截图上边 140 px，页面滚动量分别为 504、575 px。分区截图使用 `take_screenshot`，DPR 为 1。内容排序、登录状态或站点更新可能改变帖子高度与副栏纵向位置。[所用 Skill](https://github.com/KunalKumarkkr01/design-system-extractor/blob/1d75a8af6d3aab020dc7d694d0ef728eef8865be/skills/design-system-extractor/SKILL.md) · [采样函数](https://github.com/KunalKumarkkr01/design-system-extractor/blob/1d75a8af6d3aab020dc7d694d0ef728eef8865be/skills/design-system-extractor/references/extraction-snippets.md)

## 可复用的 GitHub 采样 Skill

| Skill | 用在什么环节 | 已核查的实现与交付 |
|---|---|---|
| **Design System Extractor · KunalKumarkkr01** | **首选。** 从公开论坛量出栏宽、边距、字阶与组件状态 | 依赖 Chrome DevTools MCP。读取浏览器计算样式、CSS 变量与元素矩形，在桌面和手机截图，整理为 `design.md` 与截图。栅格示例会选页面第一个 grid，分析论坛时应分别指定左区、正文和辅助区。固定提交 `1d75a8a`，MIT。[Skill](https://github.com/KunalKumarkkr01/design-system-extractor/blob/1d75a8af6d3aab020dc7d694d0ef728eef8865be/skills/design-system-extractor/SKILL.md) · [测量代码](https://github.com/KunalKumarkkr01/design-system-extractor/blob/1d75a8af6d3aab020dc7d694d0ef728eef8865be/skills/design-system-extractor/references/extraction-snippets.md#L145-L176) · [完整示例](https://github.com/KunalKumarkkr01/design-system-extractor/tree/1d75a8af6d3aab020dc7d694d0ef728eef8865be/examples/pico-css) |
| **Design System Extractor · simonbloom** | 将采样结果整理成团队可看的视觉规范 | 支持 Codex。URL 采样脚本调用 designlang，文档同时支持本地代码和截图。仓库样例包含 `DESIGN.md`、HTML 视觉预览、CSS/JSON 设计变量与采样笔记。固定提交 `1055785`。[Skill](https://github.com/simonbloom/design-system-extractor-skill/blob/1055785011c9488ad2588ebf2a964f475727eae9/skills/design-system-extractor/SKILL.md) · [URL 采集入口](https://github.com/simonbloom/design-system-extractor-skill/blob/1055785011c9488ad2588ebf2a964f475727eae9/skills/design-system-extractor/scripts/url-extract-designlang.sh) · [视觉预览样例](https://github.com/simonbloom/design-system-extractor-skill/tree/1055785011c9488ad2588ebf2a964f475727eae9/examples/bloomindesign) |
| **Taste · senlindesign** | 把参照站点反复出现的布局取舍转述成团队原则 | Playwright MCP 截图，采集脚本读取元素矩形、计算样式和网格，输出 Markdown 与 JSON。默认视口为 1440 × 900，移动端需另做一轮。对设计意图的解释应保留为推断。固定提交 `6dce223`。[Skill](https://github.com/senlindesign/taste-skill/blob/6dce223f2f5665d3636ca9a44ec3a7aa1322a9b8/SKILL.md) · [DOM 采样代码](https://github.com/senlindesign/taste-skill/blob/6dce223f2f5665d3636ca9a44ec3a7aa1322a9b8/references/extract.js) |
