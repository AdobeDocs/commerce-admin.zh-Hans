---
title: 标记标记
description: 了解标记标记，标记中包含用于引用商店中对象的代码片段。
exl-id: 0d6f5a9b-983d-473e-b641-0dceba40974f
feature: Page Content, Communications, Variables
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 0%

---

# 标记标记

标记标记是一个指令，其中包含代码片段，该代码片段具有对存储中对象（如变量、URL、图像或块）的相对引用。 标记标记标记可在编辑器可用的任何位置使用，并可合并到的HTML中 [电子邮件](email-templates.md) 和 [新闻稿](../merchandising-promotions/newsletter-template.md) 模板以及其他类型的 [内容](../content-design/introduction.md#content).

标记标记用大括号括起来，可以用小组件工具生成，也可以直接在HTML内容中键入。 例如，您可以使用标记标记来表示商店URL，而不是对页面的完整路径进行硬编码。 以下示例中的标记标记包括：

{{$include /help/_includes/directives-caution.md}}

## 自定义变量

变量标记标记可用于插入 [自定义变量](variables-custom.md) 嵌入到电子邮件模板、块、新闻稿和内容页面中。

\{\{CustomVar code= &quot;my_custom_variable&quot;}}

## 商店URL

商店URL标记表示网站的基本URL，用作完整URL（包括域名）第一部分的替换。 此标记标记有两种版本：一种直接转到您的商店，另一种使用正斜杠(`/`)，在添加路径时使用的路径。

\{\{store url=&#39;apparel/shoes/womens&#39;}}

## 媒体URL

dynamic media URL标记标记表示存储在内容交付网络(CDN)上的图像的位置和文件名。 标记可用于将图像放置在页面、块、横幅或电子邮件模板上。

\{\{media url=&#39;shoe-sale.jpg&#39;}}

## 块ID

块ID标记标记是最易于使用的标记之一，可用于将块直接放置在CMS页面上，甚至嵌套在另一个块内。 您可以使用此技术为不同的促销活动或语言修改块。 块ID标记标记通过块的标识符引用块。

\{\{block id=&#39;block-id&#39;}}

## 模板标记

模板标记引用PHTML模板文件，并可用于在CMS页面或静态块上显示块。 可将以下示例中的代码添加到页面或块以显示“联系我们”表单。

\{\{block class=&quot;Magento\Contact\Block\ContactForm&quot; name=&quot;contactForm&quot; template=&quot;Magento_联系人：：form.phtml&quot;}}

下例中的代码可以添加到页面或块中，以显示特定类别中的产品列表（按类别ID）。

\{\{block type=&quot;catalog/product_list&quot; category_id=&quot;22&quot; template=&quot;catalog/product/list.phtml&quot;}}

## 构件代码

构件工具可用于根据产品ID显示产品列表或插入复杂链接，例如转到特定产品页面的链接。 生成的代码包括块引用、代码模块的位置和相应的PHTML模板。 生成代码后，您可以将其从一个位置复制并粘贴到另一个位置。

可将以下示例中的代码添加到页面或块以显示新产品列表。

\{\{widget type=&quot;catalog/product_widget_new&quot; display_type=&quot;new_products&quot; products_count=&quot;10&quot; template=&quot;catalog/product/widget/new/content/new_grid.phtml&quot;}}

可以将下例中的代码添加到页面或块中，以按产品ID显示指向特定产品的链接。

\{\{widget type=&quot;catalog/product_widget_link&quot; anchor_text=&quot;我的产品链接&quot; title=&quot;我的产品链接&quot; template=&quot;catalog/product/widgetlink/link_block.phtml&quot; id_path=&quot;product/31&quot;}}

## 在链接中使用标记标记

您可以将标记标记与HTML锚点标记结合使用，并直接链接到商店中的任何页面。 链接可以合并到内容页面、块或电子邮件和新闻稿模板中。 您还可以使用此技术将图像链接到特定页面。

### 步骤1. 标识目标URL

如果可能，请导航到要链接到的页面，然后从浏览器的地址栏复制完整的URL。 您需要的URL部分位于 `.com/`. 否则，从要用作链接目标的CMS页面中复制URL密钥。

#### 类别页面的完整URL

`https://mystore.com/apparel/shoes/womens`
`https://mystore.com/apparel/shoes/womens.html`

#### 产品页面的完整URL

`https://mystore.com/apparel/shoes/womens/nine-west-pump`
`https://mystore.com/apparel/shoes/womens/nine-west-pump.html`

#### CMS页面的完整URL

`https://mystore.com/about-us`

### 步骤2. 将标记添加到URL

商店URL标记表示网站的基本URL，可用作商店URL的HTTP地址部分的替代项，包括域名和 `.com`. 根据要实现的结果，您可以使用以下两个版本的标记。

`store direct_url`  — 直接链接到页面。

`store url`  — 在末尾放置正斜杠，以便可附加其他引用作为路径。

在以下示例中，URL键用单引号括起来，并且整个标记标记用双大括号括起来。 与锚标记一起使用时，标记标记将放置在锚的双引号中。 为避免混淆，可以对每个嵌套引号集使用单引号和双引号。

如果您以完整URL开头，请删除HTTP地址(`http://` 或 `https://`)部分，向上至并包括 `.com/`. 在其位置，输入商店URL标记标记，通过开头的单引号向上显示。

#### 存储URL标记标记

`https://mystore.com/apparel/shoes/womens`

`{{store url='apparel/shoes/womens'}}`

否则，请输入商店URL标记标记的第一部分，并粘贴您之前复制的URL密钥或路径。

### 使用URL键存储URL标记标记

`{{store url=`

要完成标记标记，请输入右双引号和双大括号。

`{{store url='apparel/shoes/womens'}}`

### 步骤3. 完成锚点标记

使用标记标记（而不是目标URL）将完成的标记标记包裹在锚标记中。 然后，添加链接文本和结束锚点标记。

#### 锚点标记中的标记

\&lt;a href=&quot;\{\{markup tag goes here}}&quot;>链接文本\&lt;/a>

将完成的锚点标记粘贴到您希望在其中显示链接的任何CMS页面、块、横幅或电子邮件模板的代码中。

### 包含标记的完整链接

\&lt;a href=&quot;\{\{store url=&amp;#39;apparel/shoes&amp;#39;}}&quot;>鞋类销售\&lt;/a>
