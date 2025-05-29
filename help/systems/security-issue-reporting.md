---
title: 安全问题报告
description: 了解如何配置联系信息和安全相关链接，安全研究人员可以使用这些链接来报告有关您网站的安全问题。
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# 安全问题报告

`security.txt`文件包含联系人信息和安全相关链接，安全研究人员可以使用这些链接来报告有关您网站的安全问题。 如果安全信息随时间变化，请确保`security.txt`文件中的信息是最新的。

**_配置security.txt：_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中的&#x200B;_[!UICONTROL Security]_下，单击&#x200B;**[!UICONTROL Security.txt]**。

1. 在&#x200B;_[!UICONTROL General]_部分中，将&#x200B;**[!UICONTROL Enable]**设置为`Yes`。

   ![常规安全配置](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL Contact Information]_下，输入以下内容：

   - 为您的商店管理安全问题的人员的电子邮件地址和电话号码。

   - 您商店的&#x200B;**[!UICONTROL Contact Page]**&#x200B;的URL。 此页面可以是商店安全联系人的列表，也可以是您的&#x200B;_联系我们_&#x200B;页面。

   ![联系人信息配置](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL Other Information]_下，输入以下内容：

   - 您的公共&#x200B;**[!UICONTROL Encryption]**&#x200B;密钥的URL。 例如： `https://example.com/pgp-key.txt`

   - **[!UICONTROL Acknowledgments]**&#x200B;页面的URL，在该页面上，安全研究人员代表您的商店所做的工作将得到认可。

   - 您用于安全相关通信的&#x200B;**[!UICONTROL Preferred Languages]**。 为每个支持的语言输入标准的双字符[语言代码](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)，用逗号分隔。 例如，要指定英语、西班牙语和法语，请输入`en, es, fr`。 所有指定的语言都具有相同的优先级，无论其外观顺序如何。

   - **[!UICONTROL Hiring]**&#x200B;页面的URL，该页面列出了您商店中与安全相关的就业机会。

   - 您的安全&#x200B;**[!UICONTROL Policy]**&#x200B;页面的URL。

   - 保存在服务器上的数字&#x200B;**[!UICONTROL Signature]**&#x200B;文件的URL。 例如： `https://mystore.com/.well-known/security.txt.sig`

   必须从服务器的CLI（命令行界面）设置数字签名。 要了解更多信息，请参阅GitHub上的[Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md)。

   ![其他信息](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。
