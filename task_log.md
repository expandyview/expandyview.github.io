# 任务日志

## 2024-03-27

1. 创建了网页下载脚本 `download_webpage.py`
   - 使用 requests 和 BeautifulSoup4 库
   - 实现了下载指定 URL 的 HTML 内容功能
   - 处理了 SSL 证书验证问题
2. 创建了 `requirements.txt` 文件并安装了必要的依赖
3. 成功下载了目标网页 (https://zzzura-secure.duckdns.org/amazon) 的 HTML 内容到 `downloaded_page.html`
4. 按照 `downloaded_page.html` 的风格，将 `index.html` 文件中标题、作者、单位等部分替换为红色大背景的 header 风格，内容保留 ExpandyGauss 相关信息，并加入了 share 按钮和二维码。
5. 对 header 部分进行了进一步优化：
   - 放大了 ACLab logo (max-width 从 180px 调整为 280px)
   - 缩小了标题字号 (font-size 从 2.5rem 调整为 2.2rem)并增加了两侧边距 (margin 从 10px 0 0 0 调整为 10px 60px 0 60px)
   - 将作者名字颜色从金色 (#ffe082) 改为白色
6. 修复了 ACLab logo 显示问题：
   - 移除了白色背景和圆角边框，保留 logo 原始形状
   - 修复了页面结构中重复的标题和作者信息
7. 从页面中移除了 share 功能：
   - 删除了 Share 按钮及其样式
   - 删除了二维码展示容器
   - 删除了相关的 JavaScript 代码
8. 进一步放大了 ACLab logo，将 max-width 从 280px 增加到 350px，后续调整到 400px
9. 添加了高斯散射初始化视频 (initialization.mp4)：
   - 初始添加在 figure1 视频下方
   - 随后调整位置至 figure1 的 caption 下方和 Demo on Synthesis Data 标题上方
   - 设置适当的上下边距和标题样式
10. 在 Gaussian Splatting Initialization 视频下方添加了 newResult.png 图片：
    - 设置适当的上边距和最大宽度
    - 添加了图片说明文字，标记为 Figure 2
    - 保持与页面整体风格一致的布局

## 2024-03-28

1. 修改了网页标题和布局：
   - 将标题更改为"Classification of Infant Sleep–Wake States from Natural Overnight In-Crib Sleep Videos"
   - 修改了标题字体为 serif 风格
   - 调整了红色背景色从 #bf0000 为 #b10000，更贴近图片中的颜色
   - 更改了作者列表为 "Shaotong Zhu, Le Jiang and ACLab Associates"
   - 简化了作者注解为 "Equal contribution"
   - 调整了按钮样式，使用圆角并更改为深灰色背景
   - 简化了按钮数量，只保留 Paper 和 Code 两个按钮
2. 删除了作者部分的脚注信息：
   - 移除了所有作者名字旁边的上标标记（<sup>1\*</sup>等）
   - 删除了"Northeastern University"所在行
   - 删除了"Equal contribution"所在行
3. 进一步优化了网页 header：
   - 删除了"BMVC 2025"标识
   - 将所有文字字体改为 serif，使其与图片中保持一致
   - 将 Paper 和 Code 按钮移至红色 header 内部
   - 调整了按钮样式（深灰色背景、白色文字、圆角边框）
   - 设置了按钮字体为 serif、字重为 normal，使其与图片中保持一致
   - 调整了按钮大小和边距，使整体布局更协调
4. 下载了参考页面供进一步修改：
   - 使用 curl 下载了https://shaydamoezzi.github.io/InfantSleepWakeClassification/的HTML内容
   - 保存为 downloaded_infantsleep.html 文件以供分析和参考
5. 根据下载的参考页面修改 header 样式：
   - 更新了页面结构，使用与参考页面相同的 section 和嵌套 div 结构
   - 引入了 Google Fonts（Castoro、Noto Sans 等字体）
   - 修改了背景色为更精确的红色 rgb(176, 35, 24)
   - 调整了 ACLab logo 的大小为 max-height: 120px
   - 更新了标题样式，使用 Castoro 字体、600 字重
   - 调整了作者文本样式，使用 1.4rem 字号、Castoro 字体
   - 重新设计了按钮，使用白底黑字设计，与参考页面保持一致
   - 添加了 target="\_blank" 属性到链接
   - 优化了按钮的内边距、边框和字体
6. 完善了 header 样式并使红色背景延展到页面两侧：
   - 修改了页面整体布局，移除了 body 的 max-width 限制
   - 创建了新的 .content-container 类用于内容区域居中
   - 设计了新的 .hero 类使红色背景延展到页面两侧
   - 调整了 ACLab logo 尺寸为 max-width: 400px
   - 修改了标题的字号为 2.5rem，与参考图片保持一致
   - 优化了按钮样式，使用 .paper-button 和 .code-button 类
   - 调整了字体和间距，使整体更加美观
7. 重新设计了 Abstract 部分样式：
   - 将原有的 div.abstract 转换为 section.section.hero 结构
   - 使用与参考页面相同的内嵌布局（container、columns、column）
   - 添加了卡片式设计，包括圆角边框、内边距和阴影效果
   - 修改了标题样式，从 h3 改为 h2.title.is-3
   - 增加了 .has-text-justified 类以保持文本两端对齐效果
   - 添加了必要的 CSS 样式支持新结构
   - 保持了原有的内容文本不变

## 2024-03-29

1. 调整了 `index.html` 中 Abstract 部分的样式：
   - 确保文字内容正确显示。
   - 调整了方框的样式，使其居中并且宽度合适。
   - 更新了相关的 CSS 样式以支持这些更改。

## 2023 年 4 月 28 日

### 实现视频轮播功能

成功为网页添加了视频轮播功能，展示"initialization_real.mp4"和"initialization_synDM.mp4"两个视频。

具体实现：

1. 采用纯 HTML、CSS 和 JavaScript 实现视频轮播，不依赖外部库
2. 设置视频宽度为 110%，居中显示
3. 添加左右导航按钮，实现视频切换功能
4. 配置视频自动播放、静音和循环播放（与 figure1.mp4 保持一致的设置）
5. 一次只显示一个视频，点击导航按钮切换显示

实现效果：

- 视频宽度扩展到 110%，使内容更醒目
- 确保视频在页面加载后自动播放（添加 muted 属性以支持自动播放）
- 简洁的导航按钮，便于用户切换视频
- 去除多余标题和装饰，专注于视频内容展示

### 添加图片轮播功能

在视频轮播下方添加了图片轮播功能，展示"newResult_real.png"和"newResult_synDM.png"两张图片。

具体实现：

1. 采用与视频轮播相同的交互方式，确保用户体验一致
2. 设置图片宽度为 110%，居中显示
3. 添加左右导航按钮，实现图片切换功能
4. 使用相同的按钮样式和交互逻辑，保持界面的统一性

实现效果：

- 保持与视频轮播一致的用户体验
- 图片宽度为 110%，与视频保持相同的视觉比例
- 使用左右导航按钮进行图片切换
- 简洁的界面设计，专注于展示图片内容

### 整合 Demo 部分并实现视频轮播

将原有的"Demo on Synthesis Data"和"Demo on Real-world Data"两个部分整合为单一的"Demo Results"部分，并使用轮播功能展示两个视频。

具体实现：

1. 合并原有的两个标题和文字描述，创建一个综合的介绍
2. 采用与前面相同的轮播实现方式，展示"presentvideo.mp4"和"presentvideo2.mp4"
3. 使用独立的 ID（demo-1, demo-2 等）和控制器，避免与其他轮播组件冲突
4. 保持统一的视觉风格和交互模式

实现效果：

- 更紧凑的页面布局，减少了冗余的标题和描述
- 为用户提供一致的浏览体验，所有视频和图片都使用相同的交互方式
- 改善了页面的整体流畅性和内容组织结构
- 保持了视频的原有内容和功能，仅优化了展示方式

### 优化 Demo Results 部分的样式

将 Demo Results 部分改为与 Pipeline 部分相同的文本框风格，提升页面的视觉一致性。

具体实现：

1. 将简单的文本说明改为带背景、阴影和圆角的精美文本框
2. 保持与页面其他部分（如 Pipeline、SynDM Dataset 等）一致的视觉风格
3. 将原有的单一段落拆分为三个段落，分别介绍总体效果、合成数据集结果和真实场景结果
4. 添加了醒目的小标题（Synthesis Data、Real-world Data），使内容结构更清晰

实现效果：

- 提升了页面的视觉一致性，所有主要内容部分使用统一的设计语言
- 美化了文本展示效果，使用白色背景、阴影和圆角边框增强可读性
- 内容组织更加清晰，通过分段和小标题突出不同类型的演示结果
- 保持了文字描述的精确性，同时提高了整体的美观度

### 调整 Demo Results 的内容和视频展示顺序

根据需求调整了 Demo Results 部分的内容顺序和视频展示顺序，优先展示真实场景结果。

具体实现：

1. 调整文本框中段落顺序，将 Real-world Data 部分移至 Synthesis Data 部分之前
2. 交换了视频轮播中视频的顺序，先展示真实场景视频(presentvideo2.mp4)，再展示合成数据集视频(presentvideo.mp4)
3. 保持视频 ID 和脚本逻辑不变，只调整了视频源文件的引用顺序
4. 确保按钮和交互逻辑正常工作，用户可以顺畅切换视频

实现效果：

- 优先展示真实场景应用结果，更符合用户关注重点
- 内容顺序与视频展示顺序一致，提供更连贯的浏览体验
- 保持了页面的整体风格和交互方式不变
- 改善了内容的组织逻辑，使信息展示更有条理

### 添加新的"Application"文本框

- 位置在"Demo Results"部分之后，Demo 视频轮播之前
- 样式与"Overall Pipeline"相匹配（白色背景、圆角、阴影等）
- 包含两个主要应用领域：机器人感知与导航、人体运动捕捉与体育分析
- 每个领域提供了具体的应用示例

### 删除多余的"Application"部分

- 删除了位于"Demo Results"部分前的重复"Application"部分
- 保留了位于 Demo 视频轮播后的"Application"部分
- 确保页面布局更加合理，避免内容重复

### 在 Application 部分添加图片

- 在 Application 文本框下方添加了图片 application.png
- 设置图片宽度为 100%，最大宽度为 800px，保持与其他内容一致的视觉效果
- 添加了适当的上下边距（margin-top: 30px; margin-bottom: 60px）使布局更加协调
- 确保图片居中显示，增强页面美观度和内容关联性

### 统一图片展示风格

- 修改了 applications.png 图片的格式，使其与 gaussDiagram.png 的样式保持一致
- 将图片宽度从 100% 调整为 140%，使图片更加醒目
- 移除了 max-width: 800px 的限制，改为 max-width: none，允许图片按比例扩展
- 添加了 margin-left: -20% 的负边距，使图片能够向两侧延伸，呈现更完整的视觉效果
- 移除了 margin: 0 auto 居中设置，统一使用负边距扩展的展示方式
- 保留了 overflow: visible 属性，确保图片不会被容器剪裁

### 修复文本框中缺少黑点的列表项

- 检查并修复了所有文本框中未正确显示黑点的列表项
- 将 "Novel View Feature Optimization" 部分的文本正确格式化为列表项
- 修复了 "Limitations of NeRF-based Methods" 和 "Advantages of Gaussian Splatting" 部分的列表结构，确保每个列表项前都有黑点
- 将 Application 部分的 "Example" 文本从普通段落改为正确的列表格式
- 为所有 `<ul>` 标签添加 `list-style-type: disc` 属性，确保列表项前显示黑点
- 确保列表结构正确，即 `<ul>` 标签不嵌套在 `<p>` 标签内，而是作为并列元素
- 保持了列表的其他样式（行距、字体大小、对齐方式等）不变
