---
title: 安全问题报告
description: 了解如何配置联系信息和安全相关链接，安全研究人员可以使用这些链接来报告有关您网站的安全问题。
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# 安全问题报告

此 `security.txt` 文件包含联系信息和与安全相关的链接，安全研究人员可以使用这些链接来报告有关您网站的安全问题。 如果您的安全信息会随着时间的推移而改变，请确保 `security.txt` 文件是最新的。

**_要配置security.txt，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中的 _[!UICONTROL Security]_，单击&#x200B;**[!UICONTROL Security.txt]**.

1. 在 _[!UICONTROL General]_部分，设置&#x200B;**[!UICONTROL Enable]**到 `Yes`.

   ![常规安全配置](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. 下 _[!UICONTROL Contact Information]_，输入以下内容：

   - 为您的商店管理安全问题的人员的电子邮件地址和电话号码。

   - 您商店的 **[!UICONTROL Contact Page]**. 此页面可以是商店安全联系人的列表，也可以是您的 _联系我们_ 页面。

   ![联系人信息配置](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. 下 _[!UICONTROL Other Information]_，输入以下内容：

   - 您的公众的URL **[!UICONTROL Encryption]** 键。 例如： `https://example.com/pgp-key.txt`

   - URL **[!UICONTROL Acknowledgments]** 一个页面，在该页面上，安全研究人员代表您的商店所做的工作得到了认可。

   - 您的 **[!UICONTROL Preferred Languages]** 用于与安全相关的通信。 输入标准的双字符 [语言代码](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) ，以逗号分隔。 例如，要指定英语、西班牙语和法语，请输入 `en, es, fr`. 所有指定的语言都具有相同的优先级，无论其外观顺序如何。

   - 的URL **[!UICONTROL Hiring]** 列出您商店中与安全相关的就业机会的页面。

   - 您的安全性的URL **[!UICONTROL Policy]** 页面。

   - 数字的URL **[!UICONTROL Signature]** 保存在服务器上的文件。 例如： `https://mystore.com/.well-known/security.txt.sig`

   必须从服务器的CLI（命令行界面）设置数字签名。 要了解更多信息，请参阅 [安全性.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) 在GitHub上。

   ![其他信息](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Config]**.
