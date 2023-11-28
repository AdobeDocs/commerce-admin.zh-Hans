---
title: 的发行说明 [!DNL Page Builder]
description: 查看发行说明，了解所有 [!DNL Page Builder] 版本发布。
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
source-git-commit: addc34aeb4418aa3a1a9c2fc3adca738352ef94f
workflow-type: tm+mt
source-wordcount: '2747'
ht-degree: 0%

---

# 的发行说明 [!DNL Page Builder]

以下发行说明介绍了 [!DNL Page Builder] 并包括：

![新建](../assets/new.svg) 新增功能

![修复的问题](../assets/fix.svg) 修复和改进功能

![已知问题](../assets/bug.svg) 已知问题

>[!IMPORTANT]
>
>从2.4.3版本开始， [!DNL Page Builder] 现已作为Magento Open Source中的捆绑扩展提供。 它现在是Adobe Commerce和Magento Open Source的默认内容编辑工具，可以使用任何第三方模块替换WYSIWG编辑器。

## 1.7.2 for Commerce 2.4.5

![新建](../assets/new.svg) **新包装器实体 —  [!DNL Columns] 为列布局引入的容器**  — 以前，用户只能将列添加到其他容器/包装器内容类型中，例如 [!DNL Tab] 或 [!DNL Row]. 现在， [!DNL Column] 具有自己的包装器，可以直接添加到舞台上。 此外， [!DNL Columns] 容器具有设置元素，用户可以在其中指定此包装实体的配置。<!--- PB-500-->

![新建](../assets/new.svg) **用于复制、隐藏和删除列组的新菜单选项**  — 使用这些新选项，用户可以复制、隐藏和删除 [!DNL Columns] 组 — 就像他们对内容类型所做的那样。<!--- PB-507-->

![新建](../assets/new.svg) <!-- Issue 594 -->**新增的多行列支持已添加到列组中**  — 通过添加此项，用户可以操作一个列中的多行列 [!DNL Columns] 组以帮助使列布局更加灵活。<!--- PB-108-->

请参阅 [布局 — 列](./column.md) 有关使用新的 [!DNL Columns] 组。

## 1.7.1 for Commerce 2.4.4

![修复的问题](../assets/fix.svg) Page Builder现在与PHP 8.1兼容。<!--- AC-1300-->

![修复的问题](../assets/fix.svg) 商家现在可以添加替换文本(`alt_text`)到图像（图像、横幅、幻灯片），以增强内容可访问性。<!--- PB-1193-->

![修复的问题](../assets/fix.svg) 权限受限于“仅内容编辑”的管理员用户在使用页面生成器将产品小组件添加到CMS页面时，不会再看到错误。 Page Builder还在小组件设置页面上显示准确的产品计数。 以前，页面生成器需要在检索产品计数时具有目录模块的权限并显示此错误： `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`. <!--- MC-42779-->

![修复的问题](../assets/fix.svg) 页面生成器格式菜单的显示问题现已通过TinyMCE 5库升级得到解决。 <!--- AC-446-->

![修复的问题](../assets/fix.svg) 您现在可以使用鼠标编辑 **要显示的文本** 插入链接弹出窗口中的值。 <!--- AC-982-->

![修复的问题](../assets/fix.svg) Page Builder现在按预期在“字体大小选项”菜单上显示所有选项。 以前，不会显示所有选项。 <!--- AC-1056-->

![修复的问题](../assets/fix.svg) 已升级 `phpgt/dom` 的编辑器依赖项 `magento/magento2-page-builder` 到最新版本的扩展。 <!--- magento/magento2-page-builder/pull/779-->

![修复的问题](../assets/fix.svg) 在小列中显示滑块时，页面生成器不再调整插入链接和插入图像对话框的大小。 <!--- AC-973-->

![修复的问题](../assets/fix.svg) Page Builder的“表属性”菜单现在按预期显示。 <!--- AC-407-->

![修复的问题](../assets/fix.svg) 当鼠标不悬停在滑块上时，“插入”链接或图像模式中不再显示滑块点。 <!--- AC-406-->

![修复的问题](../assets/fix.svg) 已优化用于显示“表”菜单选项的字体大小。 <!--- AC-396-->

![修复的问题](../assets/fix.svg) 更正了“插入/编辑图像”和“插入/编辑链接”对话框的位置异常。 <!--- AC-397-->

![修复的问题](../assets/fix.svg) 单击时，页面生成器不再引发错误 **文本编辑器** 标语。 <!--- AC-398-->

![修复的问题](../assets/fix.svg) 在升级期间，Page Builder不再将所有动态块转换为一种语言。 <!--- MC-42265-->

## 适用于Adobe Commerce 2.4.2的1.6.0

![新建](../assets/new.svg) <!-- Issue 558 -->**新建 [!DNL Page Builder] 样式** - [!DNL Page Builder] 对内容的样式进行了大量改进。 现在，通过所做的更改，可以轻松创建简单的CSS选择器以覆盖现有的内容类型样式。 通过这些更改，您可以创建 [!DNL Page Builder] 所有内容类型均具有丰富响应性的主题。

![新建](../assets/new.svg) <!-- Issue 429 -->**行容器现在为可选**  — 您现在可以在中创建内容 [!DNL Page Builder] 而不需要Row容器。 除了行之外，现在还可以直接在舞台上拖放以下内容类型：HTML、块、动态块、列和选项卡。

![新建](../assets/new.svg) <!-- Issue 636 -->**新的响应式视区切换器**  — 您现在可以预览 [!DNL Page Builder] 使用舞台上方新的管理员视区切换器按钮时，不同设备宽度（断点）上的内容。 视区切换器使用不同的设备模拟内容在店面中显示时的样式设置方式。

![新建](../assets/new.svg) <!-- Issue 637 -->**新的特定于断点的表单字段**  — 内容类型字段值现在可以设置为特定的视区断点。 字段旁边的图标指示器显示内容类型字段值应用到的视区。

![新建](../assets/new.svg) <!-- Issue 559 -->**已删除预定义的表单字段条目**  — 边距、填充和边框相关属性（边框、边框宽度和边框半径）的高级表单设置现在设置为 `default`，以便可由模块的CSS定义值。

![新建](../assets/new.svg) <!-- Issue 635, 557,  -->**已添加舞台间距**  — 现在，行和列在舞台上包含的内容类型周围提供了额外的间距许可，但店面中没有。 额外的舞台间距使得更容易访问容器和所包含内容类型的鼠标悬停选项菜单。

![修复的问题](../assets/fix.svg) <!-- MC-37348 -->**修复了自动滚动到审核的问题**  — 现已修复自动滚动到店面上的产品评论的问题。

![修复的问题](../assets/fix.svg) <!-- MC-36227 -->**固定裁剪的内容**  — 不再裁切冗长的类别和产品描述。

![修复的问题](../assets/fix.svg) <!-- MC-35402 -->**固定全宽、全出血类别内容**  — 类别内容现在可以全宽或全出血布局显示。

![修复的问题](../assets/fix.svg) <!-- MC-37989 -->**安全性增强**

## 适用于Adobe Commerce 2.4.1的1.5.1-p1

![修复的问题](../assets/fix.svg) <!-- PB-1140, MC-38812 -->**错误显示**  — 修复了以下问题 [!DNL Page Builder] 在管理员中添加目录子类别时显示错误。

## 适用于Adobe Commerce 2.4.1的1.5.0

![新建](../assets/new.svg) <!-- Issue 510, 511, 512, 513 -->**沉浸式全屏编辑**  — 编辑 [!DNL Page Builder] 现在，对于由控制的所有区域，内容均采用全屏显示 [!DNL Page Builder]. 此更改包括CMS页面、产品和类别页面、块以及动态块。 全屏编辑将焦点放在您的内容上，并提供与店面用户体验更匹配的视图。

![新建](../assets/new.svg) <!-- Issue 544 -->**[!DNL Page Builder] 内容预览&#x200B;**— 默认情况下， [!DNL Page Builder] 现在不仅为CMS页面、块和动态块提供内容预览，而且还为产品和类别页面提供内容预览。 您可以使用新的配置为“产品”和“类别”页面打开或关闭此功能 [!DNL Page Builder] 内容预览设置，可通过商店配置中的内容管理>高级内容工具访问。

![新建](../assets/new.svg) <!-- Issue 543 -->**改进了对产品简短描述的访问**  — 默认情况下，产品简短描述现在显示在更长的描述之前。 此更改将导致与店面上显示的顺序匹配，并避免需要滚动较长的描述内容才能访问简短描述。

![新建](../assets/new.svg) <!-- Issue 419 -->**横幅和幻灯片中阻止的嵌套链接**  — 将链接同时添加到横幅和幻灯片的内容和外部元素，会创建在店面无法正确显示或操作的嵌套链接。 要解决此问题，无法再向添加链接 *两者* “消息文本”区域和“横幅和幻灯片的链接”属性。

![修复的问题](../assets/fix.svg) <!-- Issue 421 --> 修复了在选项卡项上设置空边框半径导致错误并破坏选项卡项内容的问题。

![修复的问题](../assets/fix.svg) <!-- Issue 422 --> 修复了将某些条件组合添加到产品条件过滤器时导致无法保存产品表单的错误问题。

![修复的问题](../assets/fix.svg) <!-- Issue 425 -->修复了禁用无限循环设置时，Slider内容类型无法正常工作的问题。

![修复的问题](../assets/fix.svg) <!-- Issue 426 -->修复了最低广告价格，使其现在可以正常工作 [!DNL Page Builder].

![修复的问题](../assets/fix.svg) <!-- Issue 436 -->修复了Safari和IE 11中阻止将图像拖放到横幅和幻灯片中上传区域的问题。

![修复的问题](../assets/fix.svg) <!-- Issue 525 -->修复了滑块内容类型在Firefox中无响应的问题。

![修复的问题](../assets/fix.svg) <!-- Issue 567 -->修复了构件配置在DOM中为不同外观创建错误选择器的问题。

![修复的问题](../assets/fix.svg) <!-- Issue 609 -->修复了标题工具栏隐藏内容类型的选项菜单的问题，该问题会阻止访问表单和其他选项。

![修复的问题](../assets/fix.svg) <!-- Issue 612, 613 -->修复了在切换全屏模式多次后，使用视差背景的滑块和多行无法正确呈现的问题。

![修复的问题](../assets/fix.svg) <!--MC-35220-->修复了尝试将内容从标题内容类型复制到文本内容类型时受阻的问题 [!DNL Page Builder] 以阻止保存。

![修复的问题](../assets/fix.svg) <!-- MC-34620 -->修复了文本内容类型以正确处理和保存非拉丁语–1字符。

![修复的问题](../assets/fix.svg) <!-- MC-34679 -->固定 [!DNL Page Builder] 导致Safari 13.1无法正确呈现Luma主题的Site菜单的CSS样式（适用于小型视图端口和移动设备屏幕）。

![修复的问题](../assets/fix.svg) <!-- MC-34848 -->修复了HTML内容类型，以便在店面中正确显示嵌入构件，如“Order by SKU”。

## 适用于Adobe Commerce 2.4.0的1.4.1-p1

![新建](../assets/new.svg) <!-- PB-590 --> 升级至TinyMCE 4。 已移除TinyMCE 3以提高安全性。

## 适用于Adobe Commerce 2.4.0的1.4.0

![新建](../assets/new.svg) <!-- PB-494 -->添加了对PHP 7.4的支持。

![修复的问题](../assets/fix.svg) <!-- MC-31247 -->修复了将条件设置为价格时， Products内容类型不显示可配置产品的问题。

![修复的问题](../assets/fix.svg) <!-- PB-179 -->修复了产品对齐配置，以便仅定位产品容器本身，而不定位产品容器的内容，如产品名称、价格、按钮、图像和其他元素。

![修复的问题](../assets/fix.svg) <!-- MC-33556 -->性能改进。

![修复的问题](../assets/fix.svg) 安全性增强。

## 适用于Adobe Commerce 2.3.6-p1的1.3.3-p1

![修复的问题](../assets/fix.svg) 安全性增强。

## 适用于Adobe Commerce 2.3.6的1.3.3

![修复的问题](../assets/fix.svg) <!-- MC-32766 -->修复了文本内容类型，以正确保存添加到html属性的变量指令。

![修复的问题](../assets/fix.svg) <!-- MC-34590 -->修复了文本内容类型以正确处理和保存非拉丁语–1字符。

![修复的问题](../assets/fix.svg) <!-- MC-34677 -->固定 [!DNL Page Builder] 导致Safari 13.1无法正确呈现Luma主题的Site菜单的CSS样式（适用于小型视图端口和移动设备屏幕）。

![修复的问题](../assets/fix.svg) <!-- MC-34846 -->修复了HTML内容类型以正确显示嵌入构件，如 _按SKU排序_ 在店面。

![修复的问题](../assets/fix.svg) 修复了有时会阻止用户保存内容类型表单的错误。 错误(&quot;[!DNL Page Builder] （渲染了5秒且未释放锁定），导致加载程序图标在尝试保存表单后无限旋转。

## 适用于Adobe Commerce 2.3.5-p2的1.3.2

![新建](../assets/new.svg) 安全性增强。

## 适用于Adobe Commerce 2.3.5的1.3.1-p1

此版本的 [!DNL Page Builder] 只是Adobe Commerce 2.3.5-p1的版本号更新。 1.3.0版本中描述的所有功能也适用于此版本。

## 适用于Adobe Commerce 2.3.5的1.3.0

![新建](../assets/new.svg) **模板** - [!DNL Page Builder] 现在，提供了可从现有内容创建并应用于新内容区域的模板。 [!DNL Page Builder] 模板可保存现有页面、块、动态块、产品属性和类别描述的内容和布局。 例如，您可以保存现有的 [!DNL Page Builder] CMS页面作为模板，然后应用该模板（包括其所有内容和布局）以快速为您的站点创建CMS页面。 此处记录了该新功能： [模板](templates.md).

![新建](../assets/new.svg) **行、横幅和滑块的视频背景** - [!DNL Page Builder] 行、横幅和滑块现在可以使用视频了解其背景。 此处记录了这些新增功能： [行](row.md)， [横幅](banner.md)， [滑块](slider.md).

![新建](../assets/new.svg) **视频支持新增功能和增强功能** - [!DNL Page Builder] 现在支持更广泛的视频格式。 除了YouTube和Vimeo视频之外，视频内容类型和视频背景现在还支持指向以下视频格式的视频URL链接 `.mp4` 和其他浏览器支持的格式。 视频内容类型还添加了自动播放功能。 此处记录了这些新增功能： [视频内容类型](video.md).

![新建](../assets/new.svg) **全高行、横幅和滑块** - [!DNL Page Builder] 现在，行、横幅和滑块可以使用具有任何CSS单位(px、%、vh、em)的数字或单位之间的计算(100vh - 237px)将其高度设置为页面的完整高度。 此处记录了这些新增功能： [行](row.md)， [横幅](banner.md)， [滑块](slider.md).

![新建](../assets/new.svg) **内容类型升级库**  — 开发人员现在可以创建版本的 [!DNL Page Builder] 内容类型，而不会导致早期版本出现向后兼容的问题。 在此版本之前，对内容类型配置的重大更改会导致出现显示和数据丢失问题，且以前已保存 [!DNL Page Builder] 内容类型。 新的升级库消除了这些问题。 该库旨在升级保存到数据库的内容类型的早期版本，以便它们与新版本中的配置更改相匹配。 [!DNL Page Builder] 根据新版本的需要，在本机内容类型上运行升级库。 此更改可确保内置 [!DNL Page Builder] 内容类型始终升级，以匹配对较新版本的内容类型所做的任何更改。

>[!IMPORTANT]
>
>如果已创建用于存储的其他数据库实体 [!DNL Page Builder] 内容，您 _必须_ 将这些实体添加到您的 `etc/di.xml`. 否则， [!DNL Page Builder] 存储在您实体中的内容未更新，从而导致潜在的数据丢失和显示问题。 例如，如果您已创建了一个博客实体，该实体存储 [!DNL Page Builder] 内容，您必须将博客实体添加到 `etc/di.xml` 文件作为 `UpgradableEntitiesPool` 键入，以便升级库可以更新 [!DNL Page Builder] 您的博客中使用的内容类型。 有关使用升级库的更多信息和说明，请参阅 [升级内容类型](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/) 在 _Page Builder开发人员指南_.

![新建](../assets/new.svg) **有关添加新外观的文档**  — 现在发布的开发人员信息关于 [添加外观](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/) 用于现有或自定义内容类型。

![修复的问题](../assets/fix.svg) **各种修复**

- <!-- PB-50 -->修复了复制幻灯片的父容器时，幻灯片内容的TinyMCE菜单出现在其他内容类型下方的问题。
- <!-- PB-166 -->已更新 [!DNL Page Builder] 实施销毁方法，以防止某些情况下的内存泄漏。
- <!-- PB-170 -->改进了在管理阶段使用多个实例时的TinyMCE性能。
- <!-- PB-252 -->修复了当顶行标记为隐藏时，动态块内容类型无法在Admin阶段呈现的问题。
- <!-- PB-273 -->通过从各种UI控件中删除200毫秒延迟，改进了“管理”阶段的鼠标悬停事件。 此更改使在舞台上处理嵌套内容项变得更轻松。
- <!-- PB-294 -->修复了货币符号在“管理”阶段的“块/动态块”内的“产品列表”小部件中转义不正确的问题。
- <!-- PB-296 -->修复了上的产品总计问题 [!DNL Page Builder] 编辑面板不适用于自定义MSI Stock产品。
- <!-- PB-317 -->修复了保存以下内容的问题 [!DNL Page Builder] 在Microsoft Edge上具有背景图像的内容不会在店面中呈现这些图像。
- <!-- PB-390 -->修复了嵌套的问题 [!DNL Page Builder] 如果用户在页面完全呈现之前单击保存按钮，则内容保存失败。
- <!-- PB-418 -->修复了cron作业中由于以下原因引发的异常错误： [!DNL Page Builder] 分析。

## 适用于Adobe Commerce 2.3.4-p2的1.2.2

![新建](../assets/new.svg) 安全性增强。

## 适用于Adobe Commerce 2.3.4的1.2.1-p1

![新建](../assets/new.svg) 安全性增强。

## 适用于Adobe Commerce 2.3.4的1.2.0

![新建](../assets/new.svg)  **[!DNL Page Builder]与PWA Studio集成**  — 已添加 [!DNL Page Builder] 内容呈现到Venia应用程序的PWA Studio。 [!DNL Page Builder] 现在可以在PWA StudioVenia应用程序中查看内容。 请参阅 [!DNL Page Builder] 中的文档 [PWA Studio] 以了解有关此新功能的所有信息。

![新建](../assets/new.svg) **已添加产品轮播** - <!-- PB-77, PB-173, PB-175 -->现在，“产品”内容类型提供了一个选项，可用于以轮盘/滑块格式显示您的产品，包括用于根据您的需求自定义轮盘的多个选项。

![新建](../assets/new.svg) **添加了产品SKU排序** - <!-- PB-69 -->产品内容类型现在提供了一个选项，可用于按SKU将产品添加到管理员列表中的顺序对产品进行排序。

![新建](../assets/new.svg) **添加了产品类别排序** - <!-- PB-181 -->. 产品内容类型现在提供了一个选项，可用于按类别对产品进行排序 _position_，以它们在商务目录中的显示顺序显示。

![新建](../assets/new.svg) **添加了产品选择总计** - <!-- PB-107 -->. 产品内容类型管理员编辑器现在显示与您的产品选择选项匹配的产品总数。

![修复的问题](../assets/fix.svg) **各种修复**

- <!-- PB-237 -->安全性增强。
- <!-- PB-41 -->修复了UI中的搜索“选择组件”，以便每个搜索词仅生成一个AJAX请求。
- <!-- PB-76, PB-84-->更新了管理员中的产品预览以匹配店面，包括产品的星级、颜色和大小选项（如果相关）。
- <!-- PB-169 -->修复了以下问题 [!DNL Page Builder] 在Commerce中启用JavaScript缩小和捆绑时无法保存。
- <!-- PB-241 -->修复了产品、块和动态块的管理员预览，以便在为管理员和前端定义不同URL的Commerce安装上正确呈现。
- <!-- PB-238 -->修复了产品、块和动态块的管理预览，以便在安装带有B2B的Commerce上正确呈现 _仅登录_ 选项已启用。 在进行此修复之前， [!DNL Page Builder] 预览会导致页面重定向到客户帐户登录。
- <!-- PB-239 -->修复了在中预览大页面时可能发生的会话错误 [!DNL Page Builder] 管理员。
- <!-- PB-248 -->已更新 [!DNL Page Builder] 较少的样式，以防止店面样式重复。

## 适用于Adobe Commerce 2.3.3的1.1.1-p1

![新建](../assets/new.svg) 安全性增强。

## 适用于Adobe Commerce 2.3.3的1.1.0

![新建](../assets/new.svg) <!-- MC-15250 -->向“产品”内容类型添加了明确的产品排序。

![新建](../assets/new.svg) <!-- MC-17823 -->添加了用于在HTML内容类型中插入图像、小部件和变量的按钮。

![修复的问题](../assets/fix.svg) 已改进 [!DNL Page Builder] 安全性。

![修复的问题](../assets/fix.svg) <!-- MC-1805 -->已更新 [!DNL Page Builder] 以支持PHP版本7.3。

![修复的问题](../assets/fix.svg) <!-- MC-4137 -->已将TinyMCE更新到版本4.9.5。此更新以及其他改进修复了若干TinyMCE内联编辑器问题：

- 将添加变量、图像和图像链接来放置光标。
- 表格和表格单元格可以居中对齐。
- 复制/粘贴现在将内容粘贴到光标位置。
- 可将链接应用于所选文本。
- 项目符号已正确对齐。
- 无需先单击编辑器外部即可保存内联编辑器中的更改。

![修复的问题](../assets/fix.svg) <!-- MC-3880 -->修复了每个内容类型的编辑面板上的部分之间最小高度和垂直对齐不一致的问题。

![修复的问题](../assets/fix.svg) <!-- MC-14994 -->修复了首次将标题内容类型中的工具栏放置到舞台上时错误的问题。

![修复的问题](../assets/fix.svg) <!-- MC-15742 -->修复了Slider和Video内容类型中的硬编码边距。

![修复的问题](../assets/fix.svg) <!-- MC-16241 -->修复了表单字段上两次显示所需星号符号的问题。

## 适用于Adobe Commerce 2.3.2的1.0.3-p2

![新建](../assets/new.svg) 安全性增强。

## 适用于Adobe Commerce 2.3.2的1.0.2-p1

![新建](../assets/new.svg) 安全性增强。

## 适用于Adobe Commerce 2.3.2的1.0.1

![新建](../assets/new.svg) 确保与Adobe Commerce 2.3.2兼容。

## 适用于Adobe Commerce 2.3.1的1.0.0

![新建](../assets/new.svg) 正式发布版本


[PWA Studio]: https://developer.adobe.com/commerce/pwa-studio/
