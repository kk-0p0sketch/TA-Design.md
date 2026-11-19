---
version: "2.5"
name: AI Adoption Portal · 视觉规范
description: 员工 Portal 浅色界面。Geist Sans 搭配 Lucide 线性图标。宽屏左侧为工作内容，右侧显示当前页面的互动。链接使用墨色，亮紫用于当前导航短线和键盘焦点环，搜索使用文字控件。
scope: portal
review:
  confirmed: [ink-primary-action, single-layer-controls, ink-links-and-bright-purple-indicators, text-only-search, white-divided-directory, geist-sans-latin, lucide-icons, wide-desktop-shell-and-columns]
  proposed: [simplified-chinese-font, typography, rounded, discovery-resource-grid, control-sizes]
colors:
  surface: "#FFFFFF"
  canvas: "#F7F8F8"
  ink: "#242628"
  secondary: "#5D6265"
  divider: "#DCE0E1"
  control-outline: "#81878A"
  action: "#242628"
  on-action: "#FFFFFF"
  action-hover: "#35383A"
  action-pressed: "#151718"
  accent: "#BF63F3"
  link: "{colors.ink}"
  focus: "{colors.accent}"
  selected-text: "{colors.ink}"
  selected-surface: "transparent"
  disabled-surface: "#EDF0F0"
  disabled-text: "#62696D"
  success-ink: "#086E66"
  success-surface: "#E3F4EF"
  warning-ink: "#925424"
  warning-surface: "#FFF0DD"
  error-ink: "#963E35"
  error-surface: "#FCEDEB"
fonts:
  latin: "Geist Sans"
  zh-Hans-recommended: "Noto Sans SC"
  zh-Hans-system: '"PingFang SC", "Microsoft YaHei UI", "Microsoft YaHei", sans-serif'
  proposed-stack: '"Geist Sans", "Noto Sans SC", "PingFang SC", "Microsoft YaHei UI", "Microsoft YaHei", sans-serif'
typography:
  feature-title: {fontSize: "40px", lineHeight: "48px", fontWeight: 600}
  feature-title-mobile: {fontSize: "32px", lineHeight: "40px", fontWeight: 600}
  page-title: {fontSize: "28px", lineHeight: "36px", fontWeight: 600}
  page-title-mobile: {fontSize: "24px", lineHeight: "32px", fontWeight: 600}
  section-title: {fontSize: "20px", lineHeight: "28px", fontWeight: 600}
  item-title: {fontSize: "16px", lineHeight: "24px", fontWeight: 500}
  body: {fontSize: "14px", lineHeight: "20px", fontWeight: 400}
  reading: {fontSize: "16px", lineHeight: "24px", fontWeight: 400}
  meta: {fontSize: "12px", lineHeight: "16px", fontWeight: 400}
rounded:
  tag: "4px"
  control: "6px"
  resource-card: "8px"
  dialog: "12px"
grid:
  headerRuleWidth: "100%"
  mobile: {minWidth: "0px", insetStart: "20px", insetEnd: "16px", layout: stacked}
  tablet: {minWidth: "600px", insetStart: "40px", insetEnd: "40px", layout: stacked}
  compact: {minWidth: "776px", insetStart: "40px", insetEnd: "40px", gap: "16px"}
  wide: {minWidth: "1200px", below: "1280px", insetStart: "40px", insetEnd: "32px", gap: "24px"}
  desktop:
    minWidth: "1280px"
    shellMaxWidth: "1232px"
    marginInline: "auto"
    gap: "24px"
    workColumns: "minmax(0, 2fr) minmax(0, 1fr)"
  compactWorkColumns:
    minWidth: "776px"
    below: "1280px"
    value: "minmax(0, 1fr) clamp(258px, calc(258px + (100vw - 1024px) * .46), 448px)"
  railMinViewport: "776px"
  directoryTwoTierBelowPane: "620px"
  discoveryTrackCountByPane:
    - {minWidth: "0px", columns: 4, gap: "12px", resourceColumns: 1}
    - {minWidth: "480px", columns: 8, gap: "16px", resourceColumns: 2}
    - {minWidth: "720px", columns: 12, gap: "24px", resourceColumns: 3}
  railOnNarrowScreens: "after-main"
  chineseReadingMaxWidth: "40em"
spacing:
  base: "4px"
  inline: "8px"
  row-block: "12px"
  row-inline: "16px"
  group: "24px"
  section: "32px"
  page-start: {stacked: "24px", twoColumn: "32px"}
  page-end: {stacked: "32px", twoColumn: "48px"}
  search-to-result-heading: "24px"
controls:
  small: "32px"
  medium: "36px"
  large: "40px"
  touch-target: "44px"
  portal-search: "48px"
icons:
  library: "Lucide"
  viewBox: "0 0 24 24"
  strokeWidth: 2
  linecap: "round"
  linejoin: "round"
  color: "currentColor"
  size: {inline: "16px", navigation: "20px"}
  gap: "{spacing.inline}"
  navigation: {home: House, directory: LayoutGrid, compare: GitCompareArrows}
  availability: {available: CircleCheck, restricted: LockKeyhole}
  action: {enter: ArrowRight, explain: Info, external: ExternalLink}
focus-ring: {width: "2px", offset: "3px", color: "{colors.focus}"}
motion: {state-duration: "150ms", easing: "ease-out", reduced-duration: "0ms"}
elevation: {page: "none", modal-backdrop: "rgb(0 0 0 / 36%)"}
components:
  button-primary: {backgroundColor: "{colors.action}", textColor: "{colors.on-action}", height: "{controls.medium}", rounded: "{rounded.control}"}
  button-primary-hover: {backgroundColor: "{colors.action-hover}"}
  button-primary-pressed: {backgroundColor: "{colors.action-pressed}"}
  button-disabled: {backgroundColor: "{colors.disabled-surface}", textColor: "{colors.disabled-text}"}
  search: {backgroundColor: "{colors.surface}", textColor: "{colors.ink}", height: "{controls.portal-search}", rounded: "{rounded.control}"}
  search-clear: {label: "清除", accessibleName: "清除搜索词", width: "50px", height: "{controls.touch-target}"}
  current-navigation: {textColor: "{colors.selected-text}", indicatorColor: "{colors.accent}", indicatorWidth: "24px", indicatorHeight: "2px"}
  current-filter: {textColor: "{colors.selected-text}"}
  result-row: {backgroundColor: "{colors.surface}", textColor: "{colors.ink}", padding: "12px 16px", compactPadding: "12px 0 8px"}
  result-action: {textColor: "{colors.link}", textDecoration: underline, underlineOffset: "4px"}
  result-action-hover: {underlineThickness: "2px"}
  secondary-action-hover: {backgroundColor: "{colors.canvas}"}
  secondary-action-pressed: {backgroundColor: "{colors.divider}"}
  resource-card: {backgroundColor: "{colors.surface}", rounded: "{rounded.resource-card}"}
---

# AI Adoption Portal 视觉规范

团队同事在工作间隙打开 Portal 通常想找一个能立刻使用的工具，或者看别人如何用 AI 完成一件事。工具目录把名称、用途、访问条件和下一步排在同一条记录里。宽屏把案例或操作放在左侧主栏，右侧显示该页的浏览、收藏与反馈。窄屏先读完主内容，再进入互动区。各页共用白色工作面、墨色主按钮、紫色交互标记与同一套中英文字阶。

[打开 Portal 视觉规范](Portal视觉规范.html) · [1440 px 桌面定稿对照（右图）](桌面正式栅格对照.png) · [390 px 手机样张](工具目录-手机.png) · [查看 Lucide 图标规范](Portal视觉规范.html#icons) · [查看首页案例征文](产品样张.html#home) · [试用工具目录](产品样张.html#tools) · [试用表格版本对比](产品样张.html#table-compare)

**适用范围**　员工 Portal 的浅色首页、发现区、工具目录、案例／工具详情及其中的表单与弹窗。

**已确认**　Geist Sans 负责拉丁字符和数字。导航和工具目录使用 Lucide 线性图标，搜索与清除使用文字。目录采用单层白底、细分隔线。配色为「墨字配亮紫」，墨色用于主按钮、当前导航文字和列表行动，亮紫只用于当前导航下方的短线和键盘焦点环。宽屏页面栅格已定稿。1280 px 起，顶栏内容与工作区共用 1232 px 的居中宽度，主副栏按 2∶1 分配，栏间距 24 px。1440 px 下左右各留 104 px。中文优先试用 Noto Sans SC。

## 1. 界面气质与页面组成

| 场景 | 先看到什么 | 如何形成层级 |
|---|---|---|
| 首页／案例征文 | 征文标题、导语、案例图和正文 | 在左侧从标题自然读到征文内容和入口。右侧汇总当前征文的互动，主文与辅栏共用顶部起点。 |
| 工具目录 | 一行页面标题、一句用途、搜索、数量、工具记录 | 标题、搜索框和列表外边线共用左侧起点。工具名与用途成组，访问条件和行动分列。右侧互动属于目录页。 |
| 工具／案例详情 | 名称、适用任务、使用条件，然后是示例或操作 | 用区块标题划分步骤。工具输入与输出相邻，案例正文保持易读行长。 |

**阅读顺序。** 一个页面一个可访问的一级标题。页内多个独立操作并存时，墨色按钮归给当前任务的提交动作。浏览类入口用文字链接。一个条目若既可看详情又可操作，分别给出具体的动词，例如「查看示例」「比较版本」。

**语言。** 名称优先呈现同事知道的业务对象，例如「表格版本对比」。用途说明交代输入和结果，例如「按项目核对两张表，列出新增、删除和修改」。访问条件直接写「可用」「需申请」。中英文混排保留产品名原拼写。示范字体时可对照两种语言，实际页面按用户选定语言呈现。

## 2. 颜色、语义与选择

### 基础色与交互色

以下对比度按 sRGB 相对亮度计算，除禁用组合外均以白底为基准。边界、正文、反馈各有自己的角色。色值只在主题层定义一次。

| 角色／CSS 变量 | 值 | 放置位置与验收要点 |
|---|---|---|
| 页面／控件白底 `--surface` | `#FFFFFF` | 导航、页头、搜索、目录、弹窗共享工作面。 |
| 中性浅面 `--canvas` | `#F7F8F8` | 表头、次操作悬停。主列表每行默认白底。 |
| 主要信息／主操作 `--ink`、`--action` | `#242628` | 标题、条目名和主按钮。按钮白字对比度 15.19∶1。 |
| 次要文本 `--secondary` | `#5D6265` | 说明、日期、占位语。白底 6.18∶1。 |
| 结构线 `--divider` | `#DCE0E1` | 1 px 顶栏或行分隔。白底 1.33∶1，只承担分组。 |
| 控件边界 `--control-outline` | `#81878A` | 输入框、描边按钮的 1 px 可识别边界。白底 3.64∶1。 |
| 主操作悬停／按下 | `#35383A`／`#151718` | 保持白字及控件尺寸。按下后执行一次。 |
| 禁用底／字 | `#EDF0F0`／`#62696D` | 两者组合 4.87∶1。附近说明禁用原因或解锁条件。 |
| 链接与当前项 `--link`、`--selected-text` | 墨色 `#242628` | 白底对比度 15.19∶1。正文链接、列表行动常显同色下划线，当前导航文字与图标同为墨色。 |
| 交互标记 `--accent`、`--focus` | 亮紫 `#BF63F3` | 当前导航 24 × 2 px 短线，以及键盘焦点 2 px 外环。白底对比度 3.34∶1。 |

亮紫取自团队提供的人像参考图圆底，以网页 sRGB 值保存。白底上的导航短线和焦点环达到 3∶1 的界面标记对比度。白底小字按至少 4.5∶1 验收，链接和当前栏目名沿用墨色。

### 反馈与访问资格

| 角色 | 前景／可选浅底 | 例子 | 提示位置 |
|---|---|---|---|
| 成功／可用 | `#086E66`／`#E3F4EF` | 「可用」「对比完成」 | 目录内直接排状态文字。操作结果写在操作区下方。 |
| 警示／需申请 | `#925424`／`#FFF0DD` | 「需申请」「仅指定团队可用」 | 资格与下一步相邻。说明链接仍可获得焦点。 |
| 错误 | `#963E35`／`#FCEDEB` | 「第 2 行缺少项目值」 | 错在某个字段时跟随该字段。整项服务失败时出现在对应的结果区。 |

工具目录将 Lucide 状态图标和「可用」「需申请」文字排在一起，颜色作辅助。浅底留给需单独读的一整条反馈，密集目录用白底文字。正文链接与行尾行动使用墨色，文字默认带下划线。图标跟随文字颜色，箭头表示进入任务，信息图标表示打开说明。

## 3. 字体、行高与数字

西文和数字使用 Geist Sans。简体中文优先 Noto Sans SC，苹果设备后备 PingFang SC，Windows 后备 Microsoft YaHei UI／Microsoft YaHei。页面声明 `lang="zh-CN"`。同一句里的「Excel」「2.0」保留 Geist 字形。首次部署自托管字体时覆盖实际内容与用户输入，样张中只覆盖示范文字的字体子集仅供评审。[Geist Sans](https://vercel.com/font) · [Noto Sans SC](https://fonts.google.com/noto/specimen/Noto+Sans+SC) · [中文字体实样](中文字体对照.png)

| 角色 | ≥600 px 字号／行高 | <600 px 字号／行高 | 字重 | 适用内容 |
|---|---|---|---:|---|
| 专题标题 | 40／48 | 32／40 | 600 | 首页故事或一则重点案例，只用在专题开场。 |
| 页面标题 | 28／36 | 24／32 | 600 | 工具目录、案例或工具详情。 |
| 区块标题 | 20／28 | 20／28 | 600 | 工具目录分区、对比结果。 |
| 条目名 | 16／24 | 16／24 | 500 | 工具、资源、人物或案例名。 |
| 正文／说明 | 14／20 | 14／20 | 400 | 条目用途、错误说明、短字段说明。 |
| 长文 | 16／24 | 16／24 | 400 | 使用步骤、访谈与案例方法。 |
| 控件文案 | 14／20 | 14／20 | 500–600 | 默认文字选项 500，墨色主按钮或明确当前项可 600。 |
| 可编辑输入 | 14／20 | 16／24 | 400 | 单行输入。专题搜索可用 16／24。 |
| 注释 | 12／16 | 12／16 | 400 | 日期、非关键来源。访问条件使用可扫读的正文层级。 |

以上规格的单位均为 CSS px。中文与双语内容保持默认字距（额外字距 0），允许整词换行。工具名较长时一行增高，关键信息不以省略号代替。并列数字、结果数量、版本差异表启用 `font-variant-numeric: tabular-nums`，正文维持字体默认数字。中文案例段落使用 `max-width: min(100%, 40em)`。16 px 正文最长约 640 px，或约 40 个全宽汉字。桌面继续扩宽时，目录、表单与图表仍可使用整个主栏。单行占位、按钮和标签垂直居中。含两行正文的条目自然增高。

## 4. 组件几何与交互状态

### 常用组件

| 组件 | 尺寸与构造 | 行为 |
|---|---|---|
| 主／次按钮 | S 32、M 36、L 40 px。圆角 6 px。常规文案 14／20，横向内边距可从 12 px 起，长按钮让文案决定宽度。 | 一个操作区优先一个墨色提交按钮。次按钮白底、1 px 控件边。触屏上有效目标至少 44 × 44 px，并留出独立的点击区域。 |
| 单行输入／搜索 | 常规表单 36 px，较大的常规输入 40 px。目录主搜索高 48 px，1 px 控件边，圆角 6 px。文字从左内边距 12 px 开始。字段有值时，右内边距增至 60 px，容纳 50 × 44 px 的「清除」按钮。 | 输入框与墨色「搜索」按钮并排，相隔 8 px，各自一层。空输入只显示占位提示。输入后显示文字「清除」，清除后焦点回到输入框。Enter 与点击「搜索」行为一致。 |
| 文本域 | 最小高度 144 px，内边距 12 × 16 px，圆角 6 px。标签与输入间 8 px，错误说明紧随字段。 | 比较表格时，主栏宽度达到 620 px 并排「原版」「新版」，低于 620 px 纵排。允许粘贴多行、调整高度及复制有效输入。 |
| 导航／筛选 | 顶栏采用 20 px Lucide 配 14／20 栏目名。当前项图标与文字为墨色，下方亮紫短线宽 24 px、高 2 px。文字筛选在白底上单层排布，以墨色和字重标出选项。 | 页面链接用 `aria-current="page"`。独占选择用单选或按钮选中语义，键盘焦点另画外环。宽度不足时整项换行。 |
| 工具目录行 | 主栏 ≥620 px 时，上下 12 px、左右 16 px，四栏依次为名称与用途、类型、资格、操作。主栏 <620 px 时，上 12 px、下 8 px、左右 0，名称与用途独占第一层。 | 工具名 16／24、说明 14／20，间隔 4 px。窄行第二层依次为类型、资格、右对齐操作，列缝 12 px，行尾可点范围至少 44 px 高。相邻记录之间保留 1 px 分隔。 |
| 状态／标签 | 目录访问资格使用 16 px 状态图标，紧跟短文字。独立标签圆角 4 px。 | 状态文字提供完整含义。链接或按钮承担下一步。产品分类沿用中性色。 |
| 发现区资源／预览 | 标题在图下，独立预览裁切可用 8 px 圆角。相邻资源采用同一裁切比例，保留主体。 | 缺图时直接排标题、任务与来源。标题链接承担导航，图片替代文本说明图里的有效信息。 |
| 结果表 | 14／20，数字等宽，1 px 行线。桌面单元格可用 12 px 内边距。 | 表格带列标题。原版、新版和变更类型并排，写出「新增」「移除」「修改」。很长的名称／数值允许换行。 |
| 模态弹窗 | 最宽 480 px，左右最小留白 16 px，内边距 24 px，圆角 12 px。内容高于视口时在弹窗内滚动。 | 有可访问标题，点击「关闭」或 Escape 返回触发入口。用原生 dialog 或等价的焦点管理。 |

### Lucide 功能图标

本表中的英文名称对应 `lucide-react` 的命名导出。图标采用 24 × 24 原稿，原稿线宽 2 单位，线端、转角均取圆形。尺寸按比例缩放，16 px 和 20 px 下的名义线宽分别约为 1.33 和 1.67 CSS px。使用 `currentColor` 跟随同一控件的文字颜色。行内图标保留固定尺寸，与相邻文字垂直居中，相距 8 px。[图标与目录实样](Portal视觉规范.html#icons) · [Lucide React](https://lucide.dev/guide/packages/lucide-react)

| 放置位置 | 图标与尺寸 | 用户看到的效果 |
|---|---|---|
| 顶栏栏目 | `House` 首页、`LayoutGrid` 工具目录、`GitCompareArrows` 表格对比，均为 20 px | 图标在栏目名前。当前项图文使用墨色，下方亮紫短线标记所在页面。窄屏继续显示栏目名。 |
| 目录搜索 | 纯文字输入、文字「清除」及「搜索」按钮 | 输入内容后显示「清除」，可访问名称为「清除搜索词」。按下后焦点回到输入框。 |
| 目录资格 | `CircleCheck` 可用、`LockKeyhole` 需申请，均为 16 px | 图标与资格文字共用成功色或警示色，状态独立于右侧可点击行动。 |
| 目录行动 | `ArrowRight` 进入任务、`Info` 打开示例说明或权限说明，均为 16 px | 目录示例中「试用示例」进入表格对比，「查看示例」「申请说明」在原位打开说明。 |
| 外部入口 | `ExternalLink`，16 px | 资源会跳转至外部站点或另开窗口时，图标紧邻有意义的链接文字。 |

有可见文字时，SVG 设置 `aria-hidden="true"`、`focusable="false"`，由原生链接或按钮承担单一焦点。纯图标按钮必须有明确的可访问名称。触屏上的操作命中区至少 44 × 44 px。独立焦点环画在整个操作边界。悬停、选中和禁用按宿主控件的状态变色，图形大小与图文间距保持稳定。[试用目录搜索和工具行](产品样张.html#tools)

### 状态矩阵

| 状态 | 主／次按钮 | 输入与搜索 | 列表、导航与结果 |
|---|---|---|---|
| 默认 | 主按钮墨底白字，次按钮白底墨字 | 白底 1 px 控件边，可访问标签持续存在 | 当前栏目墨色图文加亮紫短线。行尾行动的墨色动词常显下划线，线距文字 4 px。 |
| 悬停 | 主按钮切至 `#35383A`，次按钮或搜索清除键用 `#F7F8F8` | 可编辑边框加深到 `#242628`，错误字段保留错误边 | 非当前栏目与互动按钮以墨字加下划线响应。行尾行动的墨色下划线加粗至 2 px，整行保持白底。 |
| 按下 | 主按钮切至 `#151718`，次按钮、清除键切至 `#DCE0E1` | 光标进入字段 | 当前栏目保留亮紫短线。收藏后图标填充墨色，文字变为「已收藏」，计数增加，`aria-pressed="true"`。再按一次撤销。 |
| 键盘焦点 | 2 px 亮紫外环，偏移 3 px | 同一外环，文本插入光标仍可见 | 当前项与焦点可同时出现。被聚焦条目滚入可见区。 |
| 禁用／只读 | 禁用使用独立底／字颜色，阻止重复触发 | 只读值可以聚焦、选中和复制。禁用字段说明原因。 | 需申请的条目仍可打开「申请说明」。 |
| 提交／加载 | 保留按钮宽度、文案和焦点，可附进度图标。阻止重复提交 | 保留已输入内容与选项 | 结果区设置 `aria-busy`。首次加载按条目高度预留空间，已有结果可以保留到更新完成。 |
| 无匹配／空 | 提供与原因对应的恢复动作 | 保留原查询，清除后焦点返回输入 | 无匹配写「没有找到匹配的工具」，显示清除搜索或取消筛选。首次没有内容时解释怎样开始。 |
| 错误／恢复 | 服务失败后允许重试 | 字段边及说明使用错误色，设置 `aria-invalid` 并关联错误文本 | 说明哪一步失败及如何重试。重试沿用当前查询或输入。 |
| 成功／完成 | 恢复可操作状态 | 保留有效输入便于复核 | 结果数量、完成或错误消息由状态区域播报一次。呈现操作产生的具体结果。 |

### 论坛组件如何落到 Portal

| 论坛访客界面的实测细节 | Portal 对应组件与取舍 |
|---|---|
| 帖子卡片内缩 24 px、内部组距 16 px、圆角 8 px。Filters 控件高 36 px、内边距 6 × 12 px、圆角 4 px。 | 搜索与结果标题之间取 24 px，紧凑工作栏之间取 16 px。工具行保留白底细线。搜索和按钮沿用 Portal 的 6 px 圆角，主搜索高 48 px。 |
| 帖子入口默认文字为 `#292A2E`，悬停变为 `#1868DB`；Filters 悬停时背景变为 `#F8F8F8`，边界加深。 | 非当前导航和互动文字悬停时使用墨色和下划线。白底次按钮悬停用中性浅面，输入边框加深。墨色主操作独立保留自己的悬停、按下颜色。 |
| 实按 Tab 后，链接和 Filters 均显示 2 px 的 `#4688EC` 焦点环；链接外偏移 0 px，Filters 外偏移 2 px。按 Escape 关闭面板后，焦点回到 Filters。 | 键盘焦点使用 2 px 亮紫外环，外移 3 px。按 Escape 关闭「申请说明」后焦点回到该行按钮。收藏常驻状态以墨色实心书签、「已收藏」和计数表示。 |

[论坛采样记录](Atlassian论坛视觉采样.md) · [Portal 真实组件状态图](组件状态实测.png)

中文输入法选词期间的 Enter 用于完成组合输入。提交后，在原查询及当前筛选下更新结果与数量。打开详情再返回目录，应恢复查询、列表位置与原入口焦点。[可操作的目录与任务样张](产品样张.html)

## 5. 间距、对齐与典型页面

| 间距 | 角色 | Portal 中的落点 |
|---:|---|---|
| 4 px | 同一条信息 | 工具名与用途、字段与短错误说明。 |
| 8 px | 同一操作组 | 搜索框与提交按钮、图标与文字、标签与输入。 |
| 12 px | 密集内容 | 常规行上下内边距、区块标题至列表。窄行顶部沿用 12 px，底部为 8 px。 |
| 16 px | 控件与紧凑栏距 | 手机导语至搜索、常规目录行左右内边距、紧凑双栏间距。 |
| 24 px | 同页分组 | 桌面导语至搜索、各宽度搜索至结果标题、宽屏栏间距。 |
| 32 px | 页面起止 | 双栏页题与顶栏底线之间、单栏主内容结束至互动区之间。 |
| 48 px | 双栏页尾 | 主内容底部留白。主搜索控件高度也为 48 px。 |

**页面左右空间。** 顶栏底线铺满视口，品牌、页题、搜索和列表外沿共享左起点。在 1280 px 及以上，顶栏内容与工作区居中对齐，共享 1232 px 宽度。主栏和互动栏之间留 24 px，剩余空间按 2∶1 分配。两栏标题顶部对齐。视口不足 776 px 时，互动接在主内容之后。各档位的页边与栏宽见第 8 节。[桌面定稿对照（右图）](桌面正式栅格对照.png) · [手机样张](工具目录-手机.png)

**首页征文。** 左栏展示案例征文「用 AI 把会议记录变成行动清单」。先读标题和导语，再看案例图和正文。标题、导语和正文起点对齐。中文段落限宽 40em，配图随所在主栏缩放。右栏顶部与主内容对齐，显示这篇征文的阅读与反馈。发现区如增加资源，卡片只在主栏内部排 1／2／3 列。[征文实样](产品样张.html#home)

**页级互动。** 首页、工具目录和表格任务页按各自页面记录浏览、收藏、有帮助及最近互动。样张起始数字和活动属于示例数据。一次会话首次阅读某页，在该页示例浏览量上加 1，再次切回沿用该值。收藏和有帮助都是可切换的个人状态，控件用文字与 `aria-pressed` 区分，计数随选择和撤销同步。浏览器允许时使用本地存储保留两个选择，存储受限时在当前页面会话中保留。线上接入前，样张中的计数仅代表本机演示。小屏将同一份互动内容排到主栏之后，焦点和读屏顺序均为先主内容、后互动。

**目录。** 顶栏桌面最小高 72 px。手机上，品牌与导航分两行，每个栏目保留至少 44 px 的操作高度。「查看互动」在单栏目录和任务页移到页题行右端。导语至搜索在手机上留 16 px，其余视口 24 px；搜索至结果标题 24 px，标题至列表边线 12 px。宽行内缩 16 px；窄行的工具名与页题齐左，提高长中文名称的可读空间。[目录样张](产品样张.html#tools)

**详情／任务。** 页面标题说明做什么，下一段给输入格式和访问条件。将字段标签放在内容上方，将提交／恢复操作放在相关字段之后，将结果放在操作区下方。比较两个版本时共享一张有列标题的结果表。案例详情可沿用相同标题与正文层级，正文按「任务、做法、结果」组织。[表格对比样张](产品样张.html#table-compare)

## 6. 表面、圆角、焦点与动效

| 层级 | 如何画 | 何时出现 |
|---|---|---|
| 页面／目录 | 白底、直角、无阴影。结构边界 1 px，分组可直接用留白。 | 导航、搜索所在区域、工具行和普通区块。 |
| 独立控件 | 输入与按钮圆角 6 px。输入或次按钮沿自身轮廓画一条边。 | 用户可以输入、选择或提交的边界。下划线选项直接排在页面上。 |
| 资源／菜单 | 独立资源和菜单圆角 8 px。图片按预览轮廓裁切。浮动菜单通过与正文分离的边界或轻影识别。 | 发现区预览、临时可选项。菜单在触发项附近展开，避免被视口裁切。 |
| 模态层 | 弹窗圆角 12 px，遮罩黑色 36%。工具说明实样使用单层阴影 `0 12px 32px rgb(32 32 36 / 18%)`。页面原位保留。 | 需要集中阅读访问说明或完成一步短任务。焦点留在模态层中，关闭后归还。 |
| 焦点 | 2 px 亮紫实线，向外偏移 3 px。 | `:focus-visible`。轮廓与组件本身的边界、当前选中短线可以分辨。 |

悬停和按下以背景、文字色或下划线反馈。颜色过渡建议 150 ms、ease-out。栏目选中线与键盘焦点即时更新。减少动态偏好开启时关闭非必要过渡，加载状态以文字持续可读。加载、禁用、焦点的切换不得挤动相邻操作。静态列表与按钮默认无阴影。

## 7. 复核界面时观察什么

| 在实样里观察 | 常见偏差 | 调整 |
|---|---|---|
| 同一行先读到工具名，再决定是否可用 | 每个字块都有紫底和轮廓，标签比名称更突出 | 简化为标题、白底状态文字和一条行分隔。 |
| 看到当前栏目，同时知道 Tab 移到了哪里 | 焦点和选中都只靠字色 | 当前项保留 2 px 短线，焦点另画 2 px 外环。 |
| 截图能读出「需申请」及其下一步 | 用灰掉的按钮承载所有权限信息 | 写明访问条件，提供可操作的说明入口。 |
| 在中文、英文和长工具名下仍能逐条对比 | 固定行高导致文字被裁切，表格数字上下跳动 | 允许自然增高，数值列对齐并启用等宽数字。 |
| 清除搜索后可以继续输入 | 返回时查询消失或焦点落在页面开头 | 清除后聚焦输入，从详情返回时聚焦原入口。 |

样张默认打开征文页，文末的「会议纪要整理」可查看文中对应的工具示例。顶部「工具目录」和「表格对比」均可直接访问。

## 8. 响应式与边界

### 页面栅格

用视口决定互动栏的位置，用主栏的实际可用宽度决定工具行、输入区和发现资源的排法。这样 776 px 的窄双栏仍能容纳完整的中文操作。

| CSS 视口宽度 | 左／右页边 | 列缝 | 主栏与互动区 |
|---|---:|---:|---|
| <600 px | 20／16 px | — | 单列；互动接在主内容之后。 |
| 600–775 px | 40／40 px | — | 单列；页题行可直接跳到互动。 |
| 776–1199 px | 40／40 px | 16 px | 左侧工作，右侧互动。至 1024 px，右栏保持 258 px。 |
| 1200–1279 px | 40／32 px | 24 px | 沿用紧凑双栏的宽度公式，右栏约 339–375 px。 |
| ≥1280 px | 两侧各为（视口宽 − 1232 px）÷ 2 | 24 px | 顶栏内容和主工作区居中。减去栏间距后，主栏与互动栏按 2∶1 分配。 |

776–1279 px 时，互动栏按 `clamp(258px, calc(258px + (100vw - 1024px) * .46), 448px)` 计算，主栏占余宽。1280 px 起，1232 px 内容区扣除 24 px 栏距，留给两栏共 1208 px。主栏约 805.33 px，互动栏约 402.67 px。此后视口每增加 2 px，两侧页边各增加 1 px。

| 视口 | 主栏起点／宽 | 栏间距 | 互动起点／宽 | 右页边 |
|---:|---:|---:|---:|---:|
| 390 px | 20／354 | — | 20／354，在列表之后 | 16 |
| 768 px | 40／688 | — | 40／688，在列表之后 | 40 |
| 776 px | 40／422 | 16 | 478／258 | 40 |
| 1024 px | 40／670 | 16 | 726／258 | 40 |
| 1200 px | 40／约 765 | 24 | 约 829／339 | 32 |
| 1279 px | 40／约 807.70 | 24 | 约 871.70／375.30 | 32 |
| 1280 px | 24／约 805.33 | 24 | 约 853.33／402.67 | 24 |
| 1440 px | 104／约 805.33 | 24 | 约 933.33／402.67 | 104 |
| 1920 px | 344／约 805.33 | 24 | 约 1173.33／402.67 | 344 |

### 主栏内的适配

- **工具目录和表单**以主栏为尺寸查询容器（`container: work / inline-size`）。不足 620 px 时，工具行分为上下两层，表单的两个文本域纵排。达到 620 px 后，目录四栏并排，表单恢复两列。
- **发现资源**按主栏宽选择列数。小于 480 px 用 4 列底栅格、12 px 列缝、每行 1 个资源；480–719 px 用 8 列、16 px、每行 2 个；720 px 起用 12 列、24 px、每行最多 3 个。可在规范的「栅格」中切换视口验证。
- **征文**的段落最长 40em，图片按主栏缩放。所有宽度只保留一份互动区，DOM 顺序、收藏和键盘焦点随同一个控件保留。

### 样张验收

1440 × 900 下，品牌、页题和列表外沿都从 x=104 起，工作区右缘在 x=1336。24 px 栏间距两侧是约 805 px 的主栏和约 403 px 的互动栏。2026-11-19 的定稿对照中，左图是 v2.3 的 40／32 px 外页边，右图是本版正式采用的 104／104 px。[桌面定稿对照](桌面正式栅格对照.png) · [正式工具目录](产品样张.html#tools) · [交互栅格图](Portal视觉规范.html#layouts)

390 × 844 沿用 v2.3 手机布局。目录页在顶部、使用默认示例数据时，搜索框位于 y=211，首条记录高 113 px，互动区从 y=695 开始，行尾操作的点击高度为 44 px。[手机样张](工具目录-手机.png)

回归时覆盖 320 px、599／600、775／776、1023／1024、1199／1200 和 1279／1280 px，兼看长中英文、搜索无匹配、弹窗、键盘 Tab 与返回焦点。200% 缩放按实际 CSS 视口重新排版。

## 9. 实现与交付

### 主题接线

正常链接和当前导航文字继承墨色。导航短线和键盘焦点环共用亮紫。成功、警示、错误各自绑定状态语义色。

```css
:root {
  --ink: #242628;
  --accent: #bf63f3;
  --link: var(--ink);
  --selected-text: var(--ink);
  --focus: var(--accent);
}
.tool-row .action {
  color: var(--link);
  text-decoration: underline;
  text-underline-offset: 4px;
}
.page-nav [aria-current="page"] {
  position: relative;
  color: var(--selected-text);
}
.page-nav [aria-current="page"]::after {
  content: "";
  position: absolute;
  inset-inline-start: 0;
  bottom: 4px;
  width: 24px;
  height: 2px;
  background: var(--accent);
}
:focus-visible {
  outline: 2px solid var(--focus);
  outline-offset: 3px;
}
```

### 可交给设计师或生成工具的任务描述

> 做一个员工工具目录。在 1280 px 及以上使用 1232 px 的居中工作区，栏距 24 px，主副栏按 2∶1 分配。1440 px 视口的左右页边各为 104 px。左侧排工作内容，右侧排浏览、收藏和有帮助。390 px 手机上左留 20 px、右留 16 px，互动接在完整目录之后。标题用 28/36、600，窄屏用 24/32。标题后放纯文字搜索框和墨色「搜索」按钮，输入后显示「清除」。在单层白底上用 1 px 细线分隔工具。行尾行动用带下划线的墨字与 Lucide 图标。亮紫 `#BF63F3` 用在当前导航短线和键盘焦点环。展示一个可用工具、一个需申请工具和一个无匹配状态。让 390 px 与 1440 px 上的同一条记录具有相同阅读顺序。

> 做「表格版本对比」任务页。用 Geist Sans 配中文字体，先给输入示例，再放原版和新版两个文本域。说明每行填写项目名和值，验证失败时定位到对应字段。桌面并排、手机纵排。点击比较后在原位显示按项目列出的差异，用列标题和文字表示变更类型。

**交付时核对。** 用实际中英文工具名跑通搜索、文字清除、无匹配、受限说明、表单错误与恢复。在默认状态下，查看行尾行动的墨色下划线与当前栏目的亮紫短线。按 Tab，确认亮紫环跟随键盘焦点。用手机宽度、断点边缘与桌面宽度核对列、行高、行尾行动和文字换行，并检查 Enter、Escape 的焦点去向。

### 来源与沿用范围

| 参考 | 在本规范中采用的部分 |
|---|---|
| getdesign.md 的 Vercel 页面 | 视觉规范通过真实字号、色样和组件并排显示，读者可以直接判断组合效果。[可视呈现参考](https://getdesign.md/vercel/design-md) |
| design-bites 的 Vercel DESIGN.md | 各角色列出数值、用途与例外，组件按状态拆开，单列动效、断点、可复用的任务描述。原文记录 Vercel 网站的观测值，本文数值对应 Portal。[文档颗粒度参考](https://github.com/educlopez/design-bites/blob/main/design-mds/vercel.com/DESIGN.md) |
| Figma Community／Figma 栅格课程 | 学习按类别浏览资源、切换为比较列表，使用列、页边与列间距组织宽度。4／8／12 列及其断点是本 Portal 建议。[Community 导览](https://help.figma.com/hc/en-us/articles/360038510693-Guide-to-the-Figma-Community) · [栅格课程](https://help.figma.com/hc/en-us/articles/14552740206743-Lesson-2-Define-your-design-system) |
| Atlassian Community Forums | 从访客态的 Recent Posts 与 Quick Links 读取布局栏边、子标题与组件状态。1440 px 的帖子流／辅助栏宽 813／395 px，实际栏缝 24 px；1024 与 776 px 为 16 px，775 px 堆叠。Portal 沿用 1232 px 宽屏居中工作区、栏间距和双栏切换点，宽屏列宽按团队确认的 2∶1 分配。[论坛](https://community.atlassian.com/forums) · [原始测量与组件状态](Atlassian论坛视觉采样.md) · [采样 JSON](Atlassian论坛视觉采样.json) |
| Atlassian 官网采样与官方产品规范 | 官网采样提供专题字阶参考。官方规范提供文字角色、按控件用途分配圆角、按浮层关系使用阴影的方法。Portal 为中文标题放宽了行高。[DesignMD 官网采样](https://designmd.me/discover/atlassian) · [排版](https://atlassian.design/foundations/typography) · [圆角](https://atlassian.design/foundations/radius) · [表面层级](https://atlassian.design/foundations/elevation/) |
| Vercel Geist 组件 | 借鉴按钮、输入及状态的呈现，Portal 桌面常用尺寸定为 32／36／40 px，主搜索 48 px。[按钮](https://vercel.com/geist/button) · [输入框](https://vercel.com/geist/input) |
| Lucide | 团队选定的 Portal 功能图标库。样张图形取自项目已锁定的 `lucide-react@1.6.0`。React 按图标名静态导入，离线 HTML 仅随样张嵌入所用图形和许可。[图标目录](https://lucide.dev/icons/) · [许可证](https://lucide.dev/license) |
| 团队 Portal 实验版 | 延续文字导航下划线、同事案例与工作示例。原实验版的字体和按钮可从项目资料追溯，本稿规定新样张采用的 Geist、墨色主操作与紫色交互角色。[实验版设计记录](../../AI_Adoption_Portal_Experimental_Mac_20261012/DESIGN.md) |

本轮使用 [Design System Extractor 固定版本](https://github.com/KunalKumarkkr01/design-system-extractor/tree/1d75a8af6d3aab020dc7d694d0ef728eef8865be/skills/design-system-extractor) 与 Chrome DevTools MCP，对公开页面读取实际元素边界、计算样式和交互状态。早期字体和栅格探索保存在[研究附录](Portal视觉参考.html#faces)。当前样张见[Portal 视觉规范](Portal视觉规范.html)。
