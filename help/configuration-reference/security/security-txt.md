---
title: ’[!UICONTROL Security] &gt； [!UICONTROL Security.txt]’
description: 查看 [!UICONTROL Security] &gt； [!UICONTROL Security.txt] 商务管理员页面。
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

有关更改这些配置设置的详细信息，请参阅 [安全问题报告](../../systems/security-issue-reporting.md).

{{config}}

## [!UICONTROL General]

![常规](./assets/txt-general.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable] | 网站 | 启用时， `security.txt` 保存的文件包含安全研究人员报告潜在漏洞所需的信息。 选项：<br />**`Yes`**— 创建 `security.txt` 文件输入的信息 _联系信息_ 和 _其他信息_ 部分。<br />**`No`**  — （默认）不创建 `security.txt` 文件。 |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL Contact information]

![联系信息](./assets/txt-contact-info.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Email] | 网站 | 可发送安全报告的电子邮件地址。 |
| [!UICONTROL Phone] | 网站 | 可用于报告安全问题的电话号码。 |
| [!UICONTROL Contact Page] | 网站 | 网站上列出安全联系人的页面的URL，或者 _联系我们_ 页面。 示例: <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL Other information]

![其他信息](./assets/txt-other-info.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Encryption] | 网站 | 一个URL，指向安全研究人员可用于发送加密通信的加密密钥的位置。 _**请勿在此字段中输入加密密钥。**_ <br/><br/>研究人员有责任确认密钥来自可信赖的来源。 研究人员不能假定密钥与用于生成数字签名的密钥相同。 示例：<br />来自Web服务器的OpenPGP密钥 —  `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | 网站 | 指向您商店中确认安全研究人员所在页面的URL，例如`https://mystore.com/hall-of-fame.html`. 为了防止将来的攻击，请仅提供一般性描述，而不显示有关漏洞问题的特定信息。 示例：<br />我们感谢以下研究人员：<br />(yyyy/mm/dd)贾斯汀·百里香 — SQL注入 |
| [!UICONTROL Preferred Languages] | 网站 | 指定至少一种首选安全报告语言。 分隔多个双字符 [语言代码](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) 用逗号隔开。 所有指定语言都具有相同的优先级。 例如，要指定英语、西班牙语和法语，请输入 `en, es, fr`. |
| [!UICONTROL Hiring] | 网站 | 网站上列出安全相关职位的URL。 示例： `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | 网站 | 描述安全策略和漏洞报告实践的页面的URL。 示例： `https://mystore.com/security-reporting.html` 默认： `https://mystore.com/security` |
| [!UICONTROL Signature] | 网站 | 数字签名文件的链接。 数字签名必须从命令行生成，并保存在 `.well-known` 个文件夹。 有关更多信息，请参阅 [安全性.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) 在GitHub上。 示例： `https://mystore.com/.well-known/security.txt.sig` |

{：style=&quot;table-layout：auto&quot;}
