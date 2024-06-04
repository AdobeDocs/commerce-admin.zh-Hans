---
title: 电子邮件模板
description: 了解电子邮件模板以及如何使用它们支持与客户的通信并强化您的品牌。
exl-id: dfe28c77-607e-41e4-b872-3a07bcd67962
feature: Communications, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 0%

---

# 电子邮件模板

电子邮件模板定义从应用商店发送的自动邮件的布局、内容和格式。 它们称为事务性电子邮件，因为每个电子邮件都与特定类型的事务或事件关联。

Commerce包括一组响应式电子邮件模板，这些模板由商店运营期间发生的各种事件触发。 每个模板都针对任意屏幕大小进行了优化，并且可以从桌面、平板电脑和移动设备上查看。 您可以准备各种与客户活动、销售、产品警报、管理员操作和系统消息相关的电子邮件模板 [自定义](email-template-custom.md) 以反映您的品牌。

Commerce电子邮件可以由HTML和纯文本电子邮件客户端渲染。 客户端之间对电子邮件的呈现方式可能存在一些差异。

## 准备您的电子邮件徽标

徽标可以保存为以下任意文件类型。 具有透明背景的徽标可以保存为。GIF或.PNG文件。

- JPG/JPEG
- GIF
- PNG

在标题模板中指定了维度。 但是，为确保您的徽标在高分辨率设备上呈现得好，上传的图像大小应为此大小的三倍。 通常，原始徽标图稿会创建为矢量图像，因此可以对其进行缩放而不会丢失分辨率。 然后可以将图像保存为支持的位图图像格式之一。

<!-- ![Logo 3X display size](./assets/email-logo-third-size.png)-->

要利用标题中有限的垂直空间，请确保裁切图像以消除顶部或底部任何浪费的空间。 在编辑图像时，请注意保留徽标的外观比例，这样可以按比例调整高度和宽度。

通常，您可以使图像比原始图像小，但不会丢失分辨率而增大。 拍摄小图像并在照片编辑器中将其放大会降低图像分辨率。 例如，如果徽标的显示尺寸在标题模板中为168像素宽x 48像素高，则上传的图像应为504像素宽x 144像素高。

| 徽标Dimension | 1个（显示大小） | 3 x（图像大小） |
|----------|----|----|
| 宽度： | 168像素 | 504像素 |
| 高度： | 48像素 | 144像素 |

{style="table-layout:auto"}

## 配置电子邮件模板

该配置确定默认标题模板中显示的徽标，以及任何自定义徽标 [标题](email-template-custom.md#header-template) 和 [页脚](email-template-custom.md#footer-template) 要用于从商店发送的事务型电子邮件的模板。

![事务性电子邮件设计](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

有关配置设置的详细列表，请参阅 [_事务性电子邮件_](../content-design/configuration.md) 在 _内容和设计指南_.

## 步骤1. 上传您的徽标

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 查找要配置的商店视图，然后单击 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_列。

1. 下 _[!UICONTROL Other Settings]_，展开 ![扩展选择器](../assets/icon-display-expand.png) 该&#x200B;**[!UICONTROL Transactional Emails]**部分。

1. 上传您准备的 **[!UICONTROL Logo Image]**，单击 **[!UICONTROL Upload]** 并从系统中选择文件。

1. 对象 **[!UICONTROL Logo Image Alt]**，输入替换文本以标识图像。

1. 输入 **[!UICONTROL Logo Width]** 和 **[!UICONTROL Logo Height]** 以像素为单位。

   将每个值输入为数字，不使用 `px` 缩写。 这些值是指标题中徽标的显示尺寸，而不是图像的实际大小。

## 步骤2. 选择页眉和页脚模板

如果您拥有适用于商店或不同商店的自定义页眉和页脚模板，则可以根据 [范围](../getting-started/websites-stores-views.md#scope-settings) 配置中。 否则，将使用默认模板。 要了解更多信息，请参阅 [自定义电子邮件模板](email-template-custom.md).

1. 选择 **[!UICONTROL Header Template]** 用于所有事务性电子邮件。

1. 选择 **[!UICONTROL Footer Template]** 用于所有事务性电子邮件。

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 电子邮件模板列表

电子邮件模板列表按模块按字母顺序组织。

### [!DNL Amazon_Payment]

| 模板 | 配置路径 |
|--- |--- |
| `Hard-declined Authorization` | 不适用 |
| `Soft-declined Authorization` | 不适用 |

{style="table-layout:auto"}

### [!DNL Magento_Checkout]

| 模板 | 配置路径 |
|--- |--- |
| `Payment Failed` | **页面：** [!UICONTROL Sales] > [[!UICONTROL Checkout]](../configuration-reference/sales/checkout.md)<br/>**部分：** [!UICONTROL Payment Failed Emails]<br/>**字段：** [!UICONTROL Payment Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_Company]

![Adobe Commerce B2B](../assets/b2b.svg) (仅适用于Adobe Commerce B2B)

| 模板 | 配置路径 |
|--- |--- |
| `Assign Company Admin` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**部分：** [!UICONTROL Customer-Related Emails]<br/>**字段：** [!UICONTROL Default 'Assign Company Admin' Email] |
| `Assign Company to Customer` | **页面：** [!UICONTROL Customers] > [公司配置&#x200B;](../configuration-reference/customers/company-configuration.md)<br/>**部分：** [!UICONTROL Customer-Related Emails] <br/>**字段：** [!UICONTROL Default 'Assign Company to Customer' Email] |
| `Company Admin Changed to Member` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**部分：** [!UICONTROL Customer-Related Emails]<br/>**字段：** [!UICONTROL Default 'Company Admin Changed To Member' Email] |
| `Company Admin Set Inactive` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**部分：** [!UICONTROL Customer-Related Emails]<br/>**字段：** [!UICONTROL Default 'Customer Status Inactive' Email] |
| `Company Invite` | 不适用 |
| `Company Registration Request` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**部分：** [!UICONTROL Email Options - Company Registration]<br/>**字段：** [!UICONTROL Default Company Registration Email] |
| `Company Status Active1` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**部分：** [!UICONTROL Company Status Change]<br/>**字段：** [!UICONTROL Default 'Company Status Change To Active 1" Email] |
| `Company Status Active2` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**部分：** [!UICONTROL Company Status Change]<br/>**字段：** [!UICONTROL Default 'Company Status Change To Active 2" Email] |
| `Company Status Blocked` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**部分：** [!UICONTROL Company Status Change]<br/>**字段：** [!UICONTROL Default 'Company Status Change To Blocked" Email] |
| `Company Status Pending Approval` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**部分：** [!UICONTROL Company Status Change]<br/>**字段：** [!UICONTROL Default 'Company Status Change To Pending Approval" Email] |
| `Company Status Rejected` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**部分：** [!UICONTROL Company Status Change]<br/>**字段：** [!UICONTROL Default 'Company Status Change To Rejected" Email] |
| `Customer Status Active` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**部分：** [!UICONTROL Customer-Related Emails]<br/>**字段：** [!UICONTROL Default 'Customer Status Active' Email] |
| `Customer Status Inactive` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**部分：** [!UICONTROL Customer-Related Emails]<br/>**字段：** [!UICONTROL Default 'Company Admin Inactive' Email] |
| `Sales Representative Assigned to Company` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**部分：** [!UICONTROL Customer-Related Emails]<br/>**字段：** [!UICONTROL Default 'Sales Rep Assigned' Email] |

{style="table-layout:auto"}

### [!DNL Magento_CompanyCredit]

![Adobe Commerce B2B](../assets/b2b.svg) (仅适用于Adobe Commerce B2B)

| 模板 | 配置路径 |
|--- |--- |
| `Credit Limit Allocated` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**部分：** [!UICONTROL Company Credit]<br/>**字段：** [!UICONTROL Allocated Email Template] |
| `Credit Limit Updated` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**部分：** [!UICONTROL Company Credit]<br/>**字段：** [!UICONTROL Updated Email Template] |
| `Credit Reimbursed` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**部分：** [!UICONTROL Company Credit]<br/>**字段：** [!UICONTROL Reimbursed Email Template] |
| `Order Refunded to Company Credit` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**部分：** [!UICONTROL Company Credit]<br/>**字段：** [!UICONTROL Refunded Email Template] |
| `Order Reverted to Company Credit` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**部分：** [!UICONTROL Company Credit]<br/>**字段：** [!UICONTROL Reverted Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Contact]

| 模板 | 配置路径 |
|--- |--- |
| `Contact Form` | **页面：** [!UICONTROL General] > [[!UICONTROL Contacts]](../configuration-reference/general/contacts.md)<br/>**部分：** [!UICONTROL Email Options]<br/>**字段：** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Customer]

| 模板 | 配置路径 |
|--- |--- |
| `Change Email` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**部分：** [!UICONTROL Account Information Options]<br/>**字段：** [!UICONTROL Change Email Template] |
| 更改电子邮件和密码 | **页面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**部分：** [!UICONTROL Account Information Options]<br/>**字段：** [!UICONTROL Change Email and Password Template] |
| `Forgot Password` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**部分：** [!UICONTROL Password Options]<br/>**字段：** 忘记电子邮件模板 |
| `New Account` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**部分：** [!UICONTROL Create New Account Options]<br/>**字段：** 默认欢迎电子邮件 |
| `New Account (Magento/luma)` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**部分：** [!UICONTROL Create New Account Options]<br/>**字段：** 默认欢迎电子邮件 |
| `New Account Confirmation Key` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**部分：** [!UICONTROL Create New Account Options]<br/>**字段：** 确认链接电子邮件 |
| `New Account Confirmed` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**部分：** [!UICONTROL Create New Account Options]<br/>**字段：** 欢迎电子邮件 |
| `New Account Without Password` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**部分：** [!UICONTROL Create New Account Options]<br/>**字段：** 默认欢迎电子邮件（无密码） |
| `Remind Password` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**部分：** [!UICONTROL Password Options]<br/>**字段：** 提醒电子邮件模板 |
| `Reset Password` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**部分：** [!UICONTROL Password Options] <br/>**字段：** 重置密码模板 |

{style="table-layout:auto"}

### [!DNL Magento_CustomerBalance]

![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)

| 模板 | 配置路径 |
|--- |--- |
| `Store Credit Update` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**部分：** [!UICONTROL Store Credit Options]<br/>**字段：** [!UICONTROL Store Credit Update Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Directory]

| 模板 | 配置路径 |
|--- |--- |
| `Currency Update Warnings` | **页面：** [!UICONTROL General] > [[!UICONTROL Currency Setup]](../configuration-reference/general/currency-setup.md)<br/>**部分：** [!UICONTROL Scheduled Import Settings]<br/>**字段：** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Email]

| 模板 | 配置路径 |
|--- |--- |
| `Footer` | 不适用 |
| `Footer (Magento/luma)` | 不适用 |
| `Header` | 不适用 |

{style="table-layout:auto"}

### [!UICONTROL Magento_GiftCard]

![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)

| 模板 | 配置路径 |
|--- |--- |
| `Gift Card(s) Purchase` | **页面：** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**部分：** [!UICONTROL Gift Card Email Settings]<br/>**字段：** [!UICONTROL Gift Card Notification Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftCardAccount]

| 模板 | 配置路径 |
|--- |--- |
| `Gift Card Code/Balance` | **页面：** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**部分：** [!UICONTROL Email Sent from Gift Card Account Management]<br/>**字段：** [!UICONTROL Gift Card Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftRegistry]

| 模板 | 配置路径 |
|--- |--- |
| `New Registry` | **页面：** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**部分：** [!UICONTROL Owner Notification]<br/>**字段：** [!UICONTROL Email Template] |
| `Registry Sharing` | **页面：** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**部分：** [!UICONTROL Gift Registry Sharing]<br/>**字段：** [!UICONTROL Email Template] |
| `Registry Update` | **页面：** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**部分：** [!UICONTROL Gift Registry Update]<br/>**字段：** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_InventoryInStorePickupSales]

| 模板 | 配置路径 |
|--- |--- |
| `Order is Ready for Pickup` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL Order Ready For Pickup in Store]<br/>**字段：** [!UICONTROL Order Ready For Pickup Email Template] |
| `Order is Ready for Pickup For Guest` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL Order Ready For Pickup in Store]<br/>**字段：** [!UICONTROL Order Ready For Pickup Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_Invitation]

| 模板 | 配置路径 |
|--- |--- |
| `Customer Invitation` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Invitation]](../configuration-reference/customers/invitations.md)<br/>**部分：** [!UICONTROL Email]<br/>**字段：** [!UICONTROL Customer Invitation Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_NegotiableQuote]

![Adobe Commerce B2B](../assets/b2b.svg) (仅适用于Adobe Commerce B2B)

| 模板 | 配置路径 |
|--- |--- |
| `Declined Quote` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL Quote]<br/>**字段：** [!UICONTROL Declined Quote Template (to Buyer)] |
| `Expiration Date Reset` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL Quote]<br/>**字段：** [!UICONTROL Expiration Date Reset] | **页面：** [!UICONTROL Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL Quote]<br/>**字段：** [!UICONTROL Order Ready For Pickup Email Template] |
| `Expiration Warning` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL Quote]<br/>**字段：** [!UICONTROL Quote Expiration (in 48 hrs)] |
| `Expiration Warning1` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL Quote]<br/>**字段：** [!UICONTROL Quote Expiration (in 24 hrs)] |
| `New Quote` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL Quote]<br/>**字段：** [!UICONTROL New Quote Template (to Seller)] |
| `Updated Quote` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL Quote]<br/>**字段：** [!UICONTROL Updated Quote Template (to Seller)] |

{style="table-layout:auto"}

### [!DNL Magento_Newsletter]

| 模板 | 配置路径 |
|--- |--- |
| `Subscription Confirmation` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**部分：** [!UICONTROL  Subscription Options]<br/>**字段：** [!UICONTROL Confirmation Email Template] |
| `Subscription Success` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**部分：** [!UICONTROL  Subscription Options]<br/>**字段：** [!UICONTROL Success Email Template] |
| `Unsubscription Success` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**部分：** [!UICONTROL  Subscription Options]<br/>**字段：** [!UICONTROL Unsubscription Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_ProductAlert]

| 模板 | 配置路径 |
|--- |--- |
| `Cron Error Warning` | **页面：** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**部分：** [!UICONTROL Product Alerts Run Settings]<br/>**字段：** [!UICONTROL Error Email Template] |
| `Price Alert` | **页面：** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**部分：** [!UICONTROL Product Alerts]<br/>**字段：** [!UICONTROL Price Alert Email Template] |
| `Stock Alert` | **页面：** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**部分：** [!UICONTROL Product Alerts]<br/>**字段：** [!UICONTROL Stock Alert Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_PurchaseOrder]

| 模板 | 配置路径 |
|--- |--- |
| `Approved Purchase Order` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL Purchase Order Approval]<br/>**字段：** [!UICONTROL Approved Purchase Order] |
| `Approved, requires payment` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL Purchase Order Approval]<br/>**字段：** [!UICONTROL Approved, requires payment details (to Buyer)] |
| `Comment added to Purchase Order` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL Purchase Order Approval]<br/>**字段：** [!UICONTROL Comment added to Purchase Order] |
| `Created and Auto-approved Purchase Order` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL Purchase Order Approval]<br/>**字段：** [!UICONTROL Created and Automatically approved Purchase Order (to Buyer)] |
| `Created and automatically approved, requires payment details` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL Purchase Order Approval]<br/>**字段：** [!UICONTROL Created and automatically approved, requires payment details (to Buyer)] |
| `Created and requires Approval Purchase Order` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL Purchase Order Approval]<br/>**字段：** [!UICONTROL Created and requires Approval Purchase Order (to Buyer)] |
| `Error creating Order from Purchase Order` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL Purchase Order Approval]<br/>**字段：** [!UICONTROL Error creating Order from Purchase Order (to Buyer)] |
| `Purchase Order requires Approval` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL Purchase Order Approval]<br/>**字段：** [!UICONTROL Purchase Order requires Approval (to Approver)] |
| `Rejected Purchase Order` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL Purchase Order Approval]<br/>**字段：** [!UICONTROL Rejected Purchase Order (to Buyer)] |

{style="table-layout:auto"}

### [!DNL Magento_Reminder]

![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)

| 模板 | 配置路径 |
|--- |--- |
| `Promotion Notification/Reminder` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Promotions]](../configuration-reference/customers/promotions.md)<br/>**部分：** [!UICONTROL Automated Email Reminder Rules]<br/>**字段：** [!UICONTROL Reminder Email Sender] |

{style="table-layout:auto"}

### [!DNL Magento_Reward]

![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)

| 模板 | 配置路径 |
|--- |--- |
| `Balance Update` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**部分：** [!UICONTROL Email Notification Settings]<br/>**字段：** [!UICONTROL Balance Update Email] |
| `Points Expiry Warning` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**部分：** [!UICONTROL Email Notification Settings]<br/>**字段：** [!UICONTROL Reward Points Expiry Warning Email] |

{style="table-layout:auto"}

### [!DNL Magento_Rma]

![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)

| 模板 | 配置路径 |
|--- |--- |
| `New RMA` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL  RMA]<br/>**字段：** [!UICONTROL RMA Email Template] |
| `New RMA for Guest` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL  RMA]<br/>**字段：** [!UICONTROL RMA Email Template for Guest] |
| `RMA Admin Comments` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL  RMA Admin Comments]<br/>**字段：** [!UICONTROL RMA Comment Email Template] |
| `RMA Admin Comments for Guest` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL  RMA Admin Comments]<br/>**字段：** [!UICONTROL RMA Comment Email Template for Guest] |
| `RMA Authorization` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL  RMA Authorization]<br/>**字段：** [!UICONTROL RMA Authorization Email Template] |
| `RMA Authorization for Guest` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL  RMA Authorization]<br/>**字段：** [!UICONTROL RMA Authorization Email Template for Guest] |
| `RMA Customer Comments` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**部分：** [!UICONTROL RMA Customer Comments]<br/>**字段：** [!DNL RMA Comment Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sales]

| 模板 | 配置路径 |
|--- |--- |
| `Credit Memo Update` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Credit Memo Contents]<br/>**字段：** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update (Magento/luma)` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Credit Memo Comments]<br/>**字段：** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update for Guest` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Credit Memo Comments]<br/>**字段：** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Credit Memo Update for Guest (Magento/luma)` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Credit Memo Comments]<br/>**字段：** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Invoice Update` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Invoice Comments]<br/>**字段：** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update (Magento/luma)` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Invoice Comments]<br/>**字段：** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update for Guest` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Invoice Comments]<br/>**字段：** [!UICONTROL Invoice Comment Email Template for Guest] |
| `Invoice Update for Guest (Magento/luma)` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Invoice Comments]<br/>**字段：** [!UICONTROL Invoice Comment Email Template for Guest] |
| `New Credit Memo` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Credit Memo]<br/>**字段：** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo (Magento/luma)` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]]../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Credit Memo]<br/>**字段：** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo for Guest` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Credit Memo]<br/>**字段：** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Credit Memo for Guest (Magento/luma)` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Credit Memo]<br/>**字段：** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Invoice` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Invoice]<br/>**字段：** [!UICONTROL Invoice Email Template] |
| `New Invoice (Magento/luma)` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Invoice]<br/>**字段：** [!UICONTROL Invoice Email Template] |
| `New Invoice for Guest` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Invoice]<br/>**字段：** [!UICONTROL Invoice Email Template for Guest] |
| `New Invoice for Guest (Magento/luma)` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Invoice]<br/>**字段：** [!UICONTROL Invoice Email Template for Guest] |
| `New Order` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Order]<br/>**字段：** [!UICONTROL New Order Confirmation Template] |
| `New Order (Magento/luma)` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Order]<br/>**字段：** [!UICONTROL New Order Confirmation Template] |
| `New Order for Guest` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Order]<br/>**字段：** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Order for Guest (Magento/luma)` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Order]<br/>**字段：** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Shipment` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Shipment]<br/>**字段：** [!UICONTROL Shipment Email Template] |
| `New Shipment (Magento/luma)` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Shipment]<br/>**字段：** [!UICONTROL Shipment Email Template] |
| `New Shipment for Guest` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Shipment]<br/>**字段：** [!UICONTROL Shipment Email Template for Guest] |
| `New Shipment for Guest (Magento/luma)` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Shipment]<br/>**字段：** [!UICONTROL Shipment Email Template for Guest] |
| `Order Update` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Order Comments]<br/>**字段：** [!UICONTROL Order Comment Email Template] |
| `Order Update (Magento/luma)` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Order Comments]<br/>**字段：** [!UICONTROL Order Comment Email Template] |
| `Order Update for Guest` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Order Comments]<br/>**字段：** [!UICONTROL Order Comment Email Template for Guest] |
| `Order Update for Guest (Magento/luma)` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Order Comments]<br/>**字段：** [!UICONTROL Order Comment Email Template for Guest] |
| `Shipment Update` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Shipment Comments]<br/>**字段：** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update (Magento/luma)` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Shipment Comments]<br/>**字段：** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update for Guest` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Shipment Comments]<br/>**字段：** [!UICONTROL Shipment Comment Email Template for Guest] |
| `Shipment Update for Guest (Magento/luma)` | **页面：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**部分：** [!UICONTROL Shipment Comments]<br/>**字段：** [!UICONTROL Shipment Comment Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_ScheduledImportExport]

![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)

| 模板 | 配置路径 |
|--- |--- |
| `Export Failed` | **页面：** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**部分：** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**字段：** [!UICONTROL Export Failed Template] |
| `File History Clean Failed` | **页面：** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**部分：** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**字段：** [!UICONTROL Error Email Template] |
| `Import Failed` | **页面：** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**部分：** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**字段：** [!UICONTROL Import Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_SendFriend]

| 模板 | 配置路径 |
|--- |--- |
| `Send Product Link to Friend` | **页面：** [!UICONTROL Catalog] > [[!UICONTROL Email to a Friend]](../configuration-reference/catalog/email-to-a-friend.md)<br/>**部分：** [!UICONTROL Email Templates]<br/>**字段：** [!UICONTROL Select Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sitemap]

| 模板 | 配置路径 |
|--- |--- |
| `Sitemap Generation Settings` | **页面：** [!UICONTROL Catalog] > [[!UICONTROL XML Sitemap]](../configuration-reference/catalog/xml-sitemap.md)<br/>**部分：** [!UICONTROL Generation Settings]<br/>**字段：** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_TwoFactorAuth]

| 模板 | 配置路径 |
|--- |--- |
| `2FA Configuration Required by User` | 不适用 |
| `2FA Configuration Required for the Application` | 不适用 |

{style="table-layout:auto"}

### [!DNL Magento_User]

| 模板 | 配置路径 |
|--- |--- |
| `Forgot Admin Password` | **页面：** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**部分：** [!UICONTROL Admin User Emails]<br/>**字段：** 忘记密码电子邮件模板 |
| `User Notification` | **页面：** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**部分：** [!UICONTROL Admin User Emails]<br/>**字段：** 用户通知模板 |
| `New User Notification` | **页面：** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**部分：** [!UICONTROL Admin User Emails]<br/>**字段：** [!UICONTROL New User Notification Template] |

{style="table-layout:auto"}

### [!DNL Magento_Wishlist]

| 模板 | 配置路径 |
|--- |--- |
| `Magento Wish List Sharing` | **页面：** [!UICONTROL Customers] > [[!UICONTROL Wish List]](../configuration-reference/customers/wishlist.md)<br/>**部分：** [!UICONTROL Share Options]<br/>**字段：** [!UICONTROL Email Template] |

{style="table-layout:auto"}
