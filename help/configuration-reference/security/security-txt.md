---
title: '[!UICONTROL Security] &amp；gt； [!UICONTROL Security.txt]'
description: 查看Commerce管理员的[!UICONTROL Security] &amp；gt； [!UICONTROL Security.txt]页面上的配置设置。
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

有关更改这些配置设置的详细信息，请参阅[安全问题报告](../../systems/security-issue-reporting.md)。

{{config}}

## [!UICONTROL General]

![常规](./assets/txt-general.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable] | 网站 | 启用后，将保存一个`security.txt`文件，其中包含安全研究人员报告潜在漏洞所需的信息。 选项：<br />**`Yes`**— 根据&#x200B;_联系人信息_和&#x200B;_其他信息_部分中输入的信息创建`security.txt`文件。<br />**`No`** - （默认）不创建`security.txt`文件。 |

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![联系信息](./assets/txt-contact-info.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Email] | 网站 | 可发送安全报告的电子邮件地址。 |
| [!UICONTROL Phone] | 网站 | 可用于报告安全问题的电话号码。 |
| [!UICONTROL Contact Page] | 网站 | 网站上列出安全联系人的页面的URL，或&#x200B;_联系我们_&#x200B;页面。 示例： <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{style="table-layout:auto"}

## [!UICONTROL Other information]

![其他信息](./assets/txt-other-info.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Encryption] | 网站 | 一个URL，指向安全研究人员可用于发送加密通信的加密密钥的位置。 _&#x200B;**请勿在此字段中输入加密密钥。**&#x200B;_ <br/><br/>研究人员有责任验证密钥是否来自可信来源。 研究人员不能假定密钥与用于生成数字签名的密钥相同。 示例：<br />来自Web服务器的OpenPGP密钥 — `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | 网站 | 指向存储中确认安全研究人员的页面的URL，如`https://mystore.com/hall-of-fame.html`。 为了防止将来的攻击，请仅提供一般性描述，而不显示有关漏洞问题的特定信息。 示例：<br />我们要感谢以下研究人员：<br />(yyyy/mm/dd) Justin Thyme - SQL注入 |
| [!UICONTROL Preferred Languages] | 网站 | 指定至少一种首选安全报告语言。 用逗号分隔多个双字符[语言代码](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)。 所有指定语言都具有相同的优先级。 例如，要指定英语、西班牙语和法语，请输入`en, es, fr`。 |
| [!UICONTROL Hiring] | 网站 | 网站上列出安全相关职位的URL。 示例： `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | 网站 | 描述安全策略和漏洞报告实践的页面的URL。 示例： `https://mystore.com/security-reporting.html`默认值： `https://mystore.com/security` |
| [!UICONTROL Signature] | 网站 | 数字签名文件的链接。 数字签名必须从命令行生成，并保存在服务器上的`.well-known`文件夹中。 有关详细信息，请参阅GitHub上的[Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md)。 示例： `https://mystore.com/.well-known/security.txt.sig` |

{style="table-layout:auto"}
