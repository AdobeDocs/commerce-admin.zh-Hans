---
title: '[!UICONTROL Customers] &amp；gt； [!UICONTROL Customer Configuration]'
description: 查看Commerce管理员的[!UICONTROL Customers] &amp；gt； [!UICONTROL Customer Configuration]页面上的配置设置。
exl-id: 596359d7-3891-4e0c-9604-3647032188fd
feature: Configuration, Customers
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1890'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Customer Configuration]

{{config}}

## [!UICONTROL Account Sharing Options]

![帐户共享选项](./assets/customer-configuration-account-sharing-options.png)<!-- zoom -->

<!-- [Account Sharing Options](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customer-accounts/customer-account-scope) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Share Customer Accounts] | 全局 | 确定商店层次结构中客户帐户的范围。 选项： <br/>**`Global`**— 与Commerce安装中的每个网站和商店共享客户帐户信息。<br/>**`Per Website`** — 客户帐户信息仅限于创建帐户的网站。 |

{style="table-layout:auto"}

## [!UICONTROL Online Customers Options]

![联机客户选项](./assets/customer-configuration-online-customers-options.png)<!-- zoom -->

<!-- [Online Customers Options](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customers-menu/now-online) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Online Minutes Interval] | 全局 | 确定管理员可访问客户在线活动的时长。 留空则使用15分钟的默认间隔。 |
| [!UICONTROL Customer Data Lifetime] | 全局 | 确定客户输入的未保存数据过期之前经过的分钟数。 默认情况下，未保存的数据将在60分钟后过期。 |

{style="table-layout:auto"}

## [!UICONTROL Create New Account Options]

![创建新帐户选项](./assets/customer-configuration-create-new-account-options.png)<!-- zoom -->

![创建新帐户选项（增值税字段）](./assets/customer-configuration-create-new-account-options-vat.png)<!-- zoom -->

<!-- [Create New Account Options (VAT Fields)](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customer-accounts/configure/login-landing-page) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Automatic Assignment to Customer Group] | 商店视图 | 确定是否自动将客户分配给默认客户组。 若要显示店面中的增值税编号，请设置店面中的显示增值税编号，选择`Yes`。 选项： <br/>**`Yes`**— 系统不会自动验证客户VAT ID，也不会更改客户组。<br/>**`No`** — 系统行为与往常一样，可以在“默认组”字段中设置默认客户组。 |
| [!UICONTROL Default Group] | 商店视图 | 标识在创建帐户时分配的初始客户组。 |
| [!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID] | 全局 | （仅当当前配置范围设置为`Default Group`时可用。） 选择默认情况下是启用还是禁用根据增值税标识自动更改客户组。 可以在产品级别覆盖设置。 该设置会影响以下情况中的系统行为： <br/> — 客户默认地址或整个默认地址的VAT ID发生更改。 <br/> — 对于以前没有保存地址的注册客户或在结账期间注册的客户，在结账期间模拟客户组更改。 <br/>如果启用了自动组更改，则第一种情况下客户组会自动更改，第二种情况下将临时模拟的客户组分配给客户。 如果禁用了自动组更改，则分配的客户组永远不会更改，除非管理员手动更改它。 |
| [!UICONTROL Show VAT Number on Storefront] | 网站 | 确定商店中的客户是否看到增值税号。 选项： `Yes` / `No` <br/>仅影响常规非B2B客户帐户。 公司帐户拥有自己的增值税编号字段。 |
| [!UICONTROL Default Email Domain] | 商店视图 | 标识存储区的默认电子邮件域。 例如： `mystore.com` |
| [!UICONTROL Default Welcome Email] | 商店视图 | 标识用于默认&#x200B;_欢迎_&#x200B;电子邮件的电子邮件模板。 |
| [!UICONTROL Default Welcome Email Without Password] | 商店视图 | 一个备用的欢迎电子邮件模板，用于管理员创建的新客户帐户，这些帐户尚未分配密码。 |
| [!UICONTROL Email Sender] | 商店视图 | 标识显示为欢迎电子邮件发件人的商店联系人。 |
| [!UICONTROL Require Emails Confirmation] | 网站 | 确定创建帐户的请求是否需要客户的确认。 选项： `Yes` / `No`。<br/><br/> _&#x200B;**注意：**&#x200B;_&#x200B;从2.4.7版开始，客户必须在电子邮件确认后重新输入其电子邮件和密码以登录其帐户，而不考虑浏览器。 |
| [!UICONTROL Confirmation Link Email] | 商店视图 | 标识用于确认电子邮件的电子邮件模板。 默认模板： `New account confirmation key` |
| [!UICONTROL Welcome Email] | 商店视图 | 标识用于确认帐户后发送的欢迎消息的电子邮件模板。 |
| [!UICONTROL Generate Human-Friendly Customer ID] | 全局 | 确定店面中是否显示用于输入和存储VAT ID号的字段。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Password Options]

![密码选项](./assets/customer-configuration-password-options.png)<!-- zoom -->

<!-- [Password Options](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customer-accounts/configure/password-options) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Password Reset Protection Type] | 商店视图 | 确定用于重置客户帐户密码的方法。 选项： <br/>**`By IP and Email`**— 从发送到与管理员帐户关联的电子邮件地址的重置通知收到响应后，可以联机重置密码。<br/>**`By IP`** — 密码可以在线重置。 <br/>**`By Email`**— 可以通过响应发送到与管理员帐户关联的电子邮件地址的电子邮件通知来重置密码。<br/>**`None`** — 密码只能由存储管理员重置。 |
| [!UICONTROL Max Number of Password Reset Requests] | 商店视图 | 限制每小时的密码重置请求数。 对于无限制的请求，输入零(0)。 |
| [!UICONTROL Min Time Between Password Reset Requests] | 商店视图 | 确定密码重置请求之间的分钟数。 对于请求之间无延迟，请输入零(0)。 |
| [!UICONTROL Forgot Email Template] | 商店视图 | 标识客户忘记密码时使用的电子邮件模板。 默认模板： `Forgot Password` |
| [!UICONTROL Remind Email Template] | 商店视图 | 标识客户收到密码提醒或提示时使用的电子邮件模板。 默认模板： `Remind Password` |
| [!UICONTROL Reset Password Template] | 商店视图 | 确定客户重置密码时使用的电子邮件模板。 |
| [!UICONTROL Password Template Email Sender] | 商店视图 | 确定显示为密码相关电子邮件发件人的商店联系人。 |
| [!UICONTROL Recovery Link Expiration Period (hours)] | 全局 | 指定密码恢复链接到期前的小时数。 |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | 网站 | 确定登录/忘记密码表单上是否启用了自动完成。 选项： `Yes` / `No` |
| [!UICONTROL Number of Required Character Classes] | 全局 | 确定密码中必须包含的不同字符类（小写、大写、数字和特殊字符）的数量。 |
| [!UICONTROL Maximum Login Failures to Lockout Account] | 全局 | 确定在锁定客户帐户之前失败的登录尝试次数。 对于无限制的尝试，输入零(`0`)。 |
| [!UICONTROL Minimum Password Length] | 全局 | 确定密码中允许的最小字符数。 数字必须大于零(`0`)。 |
| [!UICONTROL Lockout Time (minutes)] | 全局 | 确定在尝试登录失败次数过多后客户帐户被锁定的分钟数。 |

{style="table-layout:auto"}

## [!UICONTROL Account Information Options]

![帐户信息选项](./assets/customer-configuration-account-info-options.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Change Email Template] | 商店视图 | 标识客户更改其电子邮件地址时使用的默认电子邮件模板。 |
| [!UICONTROL Change Email and Password Template] | 商店视图 | 标识客户更改其电子邮件地址和密码时使用的默认电子邮件模板。 |

{style="table-layout:auto"}

## [!UICONTROL Name and Address Options]

### Magento Open Source选项

{{ce-feature}}

![名称和地址选项 — 打开Source](./assets/customer-configuration-name-address-options-ce.png)<!-- zoom -->

<!-- [Name and Address Options - Open Source](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customer-accounts/configure/name-address-options) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Number of Lines in a Street Address] | 网站 | 确定街道地址中的行数。 街道地址由`1`到`4`行组成。 如果字段为空，则使用三行(`3`)的默认街道地址。 |
| [!UICONTROL Show Prefix] | 网站 | 确定客户名称的开头是否包含前缀，例如Mr和Ms. Options： `No` / `Optional` / `Required` |
| [!UICONTROL Prefix Dropdown Options] | 网站 | 定义前缀选项的列表。 用分号分隔各个值。 在第一个值前放置分号，以在列表顶部显示空值。 |
| [!UICONTROL Show Middle Name (initial)] | 网站 | 确定是否将中间首字母作为客户名称的一部分包括在内。 如果使用中间首字母，则为可选字段。 选项： `Yes` / `No` |
| [!UICONTROL Show Suffix] | 网站 | 确定客户名称在末尾是否包含后缀，例如Jr.、Sr.和III。 选项： `No` / `Optional` / `Required` |
| [!UICONTROL Suffix Dropdown Options] | 网站 | 定义后缀选项的列表。 用分号分隔各个值。 在第一个值前放置分号，以在列表顶部显示空值。 |
| [!UICONTROL Show Date of Birth] | 网站 | 确定名称和地址表单中是否包含客户出生日期。 选项： `No` / `Optional` / `Required` <br><br>**_重要信息：_**&#x200B;为遵循当前安全和隐私最佳实践，请注意任何与客户的完整出生日期（月、日、年）和其他个人标识符的存储相关的潜在法律和安全风险。 建议限制存储客户的完整出生日期，并建议使用客户出生年份作为替代方法。 |
| [!UICONTROL Show Tax/VAT Number] | 网站 | 确定名称和地址表单中是否包含税或[VAT编号](../../stores-purchase/vat.md)。 选项： `No` / `Optional` / `Required` |
| [!UICONTROL Show Gender] | 网站 | 确定名称和地址表单中是否包含性别。 选项： `No` / `Optional` / `Required` |
| [!UICONTROL Show Telephone] | 网站 | 确定名称和地址表单中是否包含客户的电话号码。 选项： `No` / `Optional` / `Required` |
| [!UICONTROL Show Company] | 网站 | 确定名称和地址表单中是否包含客户的公司。 选项： `No` / `Optional` / `Required` |
| [!UICONTROL Show Fax] | 网站 | 确定名称和地址表单中是否包含客户的传真号码。 选项： `No` / `Optional` / `Required` |

{style="table-layout:auto"}

### Adobe Commerce选项

{{ee-feature}}

![名称和地址选项 — Commerce](./assets/customer-configuration-name-address-options-ee.png)<!-- zoom -->

<!-- [Name and Address Options - Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customer-accounts/configure/name-address-options) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Prefix Dropdown Options] | 网站 | 定义前缀选项的列表。 用分号分隔各个值。 在第一个值前放置分号，以在列表顶部显示空值。 |
| [!UICONTROL Suffix Dropdown Options] | 网站 | 定义后缀选项的列表。 用分号分隔各个值。 在第一个值前放置分号，以在列表顶部显示空值。 |
| [!UICONTROL Show Telephone] | 网站 | 确定名称和地址表单中是否包含客户的电话号码。 选项： `No` / `Optional` / `Required` |
| [!UICONTROL Show Company] | 网站 | 确定名称和地址表单中是否包含客户的公司。 选项： `No` / `Optional` / `Required` |
| [!UICONTROL Show Fax] | 网站 | 确定名称和地址表单中是否包含客户的传真号码。 选项： `No` / `Optional` / `Required` |

{style="table-layout:auto"}

## [!UICONTROL Store Credit Options]

{{ee-feature}}

![存储点数选项](./assets/customer-configuration-store-credit-options.png)<!-- zoom -->

<!-- [Store Credit Options](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customer-accounts/store-credit/credit-configure) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Store Credit Functionality] | 全局 | 确定是否启用商店点数。 禁用它将会从客户帐户和“管理员管理客户”页面中删除“商店信用”。 选项： `Yes` / `No`。 |
| [!UICONTROL Show Store Credit History to Customers] | 网站 | 确定余额历史记录是否显示在客户帐户中。 选项： `Yes` / `No`。 |
| [!UICONTROL Refund Store Credit Automatically] | 全局 | 确定是否自动发放商店退款。 选项： `Yes` / `No` |
| [!UICONTROL Store Credit Update Email Sender] | 商店视图 | 确定显示为发送给客户的信用更新通知发送者的商店标识。 |
| [!UICONTROL Store Credit Update Email Template] | 商店视图 | 确定用于信用更新的电子邮件模板。 |

{style="table-layout:auto"}

## [!UICONTROL Login Options]

![登录选项](./assets/customer-configuration-login-options.png)<!-- zoom -->

<!-- [Login Options](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customer-accounts/configure/login-landing-page) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Redirect Customer to Account Dashboard after Logging in] | 网站 | 确定客户登录其帐户后发生的情况。 要将客户重定向到他们的帐户信息板，请选择`Yes`。 选项： <br/>**`Yes`**— 客户登录其帐户时将显示帐户仪表板。<br/>**`No`** — 客户在登录到其帐户后可以继续购物。 |

{style="table-layout:auto"}

## [!UICONTROL Address Templates]

![地址模板](./assets/customer-configuration-address-templates.png)<!-- zoom -->

<!-- [Address Templates](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customer-accounts/attributes/address-templates) -->

| 模板 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Text] | 商店视图 | 模板用于打印的所有地址。 |
| [!UICONTROL Text One Line] | 商店视图 | 此模板定义客户购物车通讯簿列表中地址实体的顺序。 结账期间的进度。 |
| [!UICONTROL HTML] | 商店视图 | 此模板定义位于“管理”面板([!UICONTROL Customers] > [!UICONTROL Manage Customers])中&#x200B;_客户地址_&#x200B;区域下的地址字段的顺序。 当客户在其帐户页面上创建账单或送货地址时，这也会影响&#x200B;_添加新地址_&#x200B;页面上的那些地址。 |
| [!UICONTROL PDF] | 商店视图 | 模板定义在打印的发票、发运和贷项通知单中显示的开单地址和发运地址。 |

{style="table-layout:auto"}

## [!UICONTROL Customer Segments]

{{ee-feature}}

![客户区段](./assets/customer-configuration-customer-segments.png)<!-- zoom -->

<!-- [Customer Segments](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/segments/customer-segments) -->

| 模板 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Customer Segment Functionality] | 全局 | 确定客户区段是否可用于创建目标促销活动。 选项： `Yes` / `No` |
| [!UICONTROL Real-time Check if Customer is Matched by Segment] | 全局 | 确定是否实时验证客户区段。 选项： <br/>**[!UICONTROL Yes]**— 实时验证客户区段（默认值）。<br/>**[!UICONTROL No]** — 客户区段由单个组合条件SQL查询验证。 如果系统中存在许多客户区段，这会提高区段验证的性能。 但是，当拆分数据库或没有注册客户时，验证将不起作用。 |

{style="table-layout:auto"}

## [!UICONTROL CAPTCHA]

![验证码](./assets/customer-configuration-captcha.png)<!-- zoom -->

<!-- [CAPTCHA](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/captcha/security-captcha) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable CAPTCHA on Storefront] | 网站 | 在与Commerce网站关联的商店中启用验证码。 选项： `Yes` / `No` |
| [!UICONTROL Font] | 网站 | 确定用于显示验证码的字体。 要添加您自己的字体，请将该字体文件放在与Commerce安装相同的目录中，并将声明添加到位于`app/code/Magento/Captcha/etc`的`config.xml`文件中。 |
| [!UICONTROL Forms] | 网站 | 确定使用CAPTCHA的表单。 选项： <br />`Applying Coupon Code` <br />`Checkout/Placing Order`<br />`Create user` <br />`Login` <br />`Forgot password` <br />`Contact Us` <br />`Change password` <br />`Share Wishlist Form` <br />`Send to Friend Form` <br />`Payflow Pro` （请参阅[安全修补程序](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html)） <br />`Add Gift Card Code` ![Adobe Commerce](../../assets/adobe-logo.svg) <br />`Create company` ![Adobe Commerce](../../assets/adobe-logo.svg) <br /><br />_&#x200B;**注意：**&#x200B;_&#x200B;选中后，始终启用“创建用户”、“忘记密码”和“Payflow Pro”表单。 |
| [!UICONTROL Displaying Mode] | 网站 | 确定验证码的出现时间。 选项： <br/>**`Always`**— 登录始终需要CAPTCHA。<br/>**`After number of attempts to login`** — 此选项仅适用于管理员登录表单。 选中后，将显示&#x200B;_[!UICONTROL Number of Unsuccessful Attempts to Login]_&#x200B;字段。 输入要允许的登录尝试次数。 `0` （零）的值类似于将[!UICONTROL Displaying Mode]设置为`Always`。<br/>_&#x200B;**注意：**&#x200B;_要跟踪失败的登录尝试次数，每次尝试使用一个电子邮件地址和一个IP地址登录都会被计入。 允许从同一IP地址登录的最大次数是1,000。 此限制仅在启用CAPTCHA时适用。 |
| [!UICONTROL Number of Unsuccessful Attempts to Login] | 网站 | 指定帐户锁定前客户可以尝试登录的次数。 |
| [!UICONTROL CAPTCHA Timeout (minutes)] | 网站 | 确定当前CAPTCHA的生命周期。 验证码过期后，用户必须重新加载页面。 |
| [!UICONTROL Number of Symbols] | 网站 | 确定验证码中显示的符号数（最多8个）。 您还可以指定范围，例如5-8。 |
| [!UICONTROL Symbols Used in CAPTCHA] | 网站 | 确定验证码中显示的字母（a-z和A-Z）和数字(0-9)。 很难与其他符号（如`i`、`l`或`1`）区分的符号不包含在默认验证码符号集中。 |
| [!UICONTROL Case Sensitive] | 网站 | 确定验证码字符是否区分大小写。 选项： `Yes` / `No` |

{style="table-layout:auto"}
