---
title: 存储URL
description: 了解商店URL以及如何配置基本URL和存储代码。
exl-id: dd7a6317-b0cf-4d0c-9b31-a963c467026b
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '1519'
ht-degree: 0%

---

# 存储URL

Adobe Commerce或Magento Open Source安装中的每个网站都有一个分配给店面的基本URL，以及一个分配给管理员的URL。 Adobe使用变量来定义与基本URL相关的内部链接，这使得在不更新链接的情况下将整个存储从一个位置移动到另一个位置成为可能。 标准基本URL的开头为 `http`，安全基本URL的开头为 `https`.

- **基本URL** — `http://www.yourdomain.com/magento/`
- **安全基础URL** — `https://www.yourdomain.com/magento/`
- **包含IP地址的URL** — `http://###.###.###.###/magento/` 或 `https://###.###.###.###/magento/`

>[!IMPORTANT]
>
>请勿更改管理员URL的默认基本URL配置。 要更改管理员URL或路径，请参阅 [使用自定义管理员URL](#use-a-custom-admin-url).

## 使用安全协议

商店的基本URL最初是在Adobe Commerce安装期间设置的。 如果当时有安全证书可用，则可以指定 `HTTPS` 用于商店、管理员或两者的URL。 如果您的Adobe Commerce安装包含多个商店，或者您计划稍后添加更多商店，则可以在URL中包含商店代码。 所有Adobe资源和操作都可以通过安全协议使用。

如果在安装时安全证书不可用于域，请确保在启动存储之前更新配置。 在为域建立安全证书后，您可以将两个基本URL中的任意一个配置为使用加密的安全套接字层(SSL)运行，或者将两个基本URL都配置为使用加密的安全套接字层(SSL)运行，并且 [传输层安全性][1] (TLS)协议。

>[!IMPORTANT]
>
>Adobe强烈建议使用安全协议传输生产站点的所有页面，包括内容和产品页面。

可以将Adobe Commerce和Magento Open Source配置为跨渠道交付所有页面 `HTTPS` 默认情况下。 如果您的存储已使用标准协议运行，则可以通过启用 [HTTP严格传输安全][2] (HSTS)和升级任何不安全的页面请求。 HSTS是一种选择加入协议，可阻止浏览器渲染标准 `HTTP` 使用指定域的不安全协议传输的页面。 因为搜索引擎可能已使用standard索引了存储区的每个页面 `HTTP` URL后，您可以配置Commerce以将任何不安全的页面请求升级到 `HTTPS` 自动，这样您就不会丢失任何流量。 当Commerce配置为对店面和管理员使用安全URL时，会显示两个额外的字段，允许您启用 `HSTS`.

## 配置基本URL

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 下 _常规_ 在左侧面板中，选择 **[!UICONTROL Web]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Base URL]** 部分。

   - **[!UICONTROL Base URL]**  — 输入商店的完全限定的基本URL。 请确保以正斜杠结束URL，以便可以使用存储中的其他URL密钥进行扩展。 例如： `http://yourdomain.com/`

     >[!NOTE]
     >
     >请勿更改中的占位符 _[!UICONTROL Base Link URL]_字段。 它是用于创建基本URL的相对链接的占位符。

   - **[!UICONTROL Base URL for Static View Files]**  — （可选）通过输入以下占位符开头的路径，为静态视图文件的基本URL指定替代位置：

     \{\{unsecure_base_url}}

   - **[!UICONTROL Base URL for User Media Files]**  — （可选）通过输入以下占位符开头的路径，为用户媒体文件的基本URL指定替代位置：

     \{\{unsecure_base_url}}

     对于典型安装，无需更新静态视图文件或媒体文件的路径，因为它们是相对于基本URL的。

   ![常规配置 — Web基本URL](../configuration-reference/general/assets/web-base-urls.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >用双大括号括起来的占位符是变量的标记标记。

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 配置安全基本URL

如果您的域具有有效的安全证书，则可以配置店面和管理员的URL以通过安全(https)渠道传输数据。 如果没有有效的安全证书，您的存储将无法使用安全(SSL/TLS)协议运行。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 _[!UICONTROL Base URLs (Secure])_ 部分并执行以下操作：

   ![常规配置 — 安全基本URL](../configuration-reference/general/assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - **[!UICONTROL Secure Base URL]**  — 输入完整的安全基本URL，后跟正斜杠。 例如： `https://yourdomain.com/`

   - **[!UICONTROL Secure Base Link URL]**  — 请勿更改安全基本链接URL字段中的占位符。 它用于创建指向安全基础URL的相对链接。

   - **[!UICONTROL Secure Base URL for Static View Files]**  — （可选）通过输入以下占位符开头的路径，为静态视图文件的安全基本URL指定替代位置：

     \{\{secure_base_url}}

   - **[!UICONTROL Secure Base URL for User Media Files]**  — （可选）通过输入以下占位符开头的路径，为用户媒体文件的安全基本URL指定替代位置：

     \{\{secure_base_url}}

1. 要增强安全性，请将以下两个选项设置为 `Yes`.

   - **[!UICONTROL Use Secure URLs on Storefront]**
   - **[!UICONTROL Use Secure URLs in Admin]**

1. 对象 _[!UICONTROL Enhanced Security Settings]_，请执行以下操作：

   - **[!UICONTROL Enable HTTP Strict Transport Security (HSTS)]**  — 如果您希望商店仅显示安全HTTPS页面请求，请将设置为 `Yes`.

   - **[!UICONTROL Upgrade Insecure Requests]**  — 要将任何对标准无安全HTTP页面的请求升级为安全HTTPS，请将设置为 `Yes`.

1. 设置 **[!UICONTROL Offloader Header]** 用于您的服务器。

   大多数Commerce安装使用默认值 `X-Forward-Proto` 将协议标识为 `HTTP` 或 `HTTPS`. 如果您的服务器配置使用不同的offloader_header，请在此处输入它。

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 在URL中包含商店代码

>[!NOTE]
>
>当 _将存储代码添加到URL_ 选项设置为 `Yes`中，您必须在浏览器URL中包含存储代码。 此设置可以确保URL重写正确映射并且成功打开所有页面，而无需 _“404页面未找到”_ 错误。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 下 _[!UICONTROL General]_在左侧面板中，选择&#x200B;**[!UICONTROL Web]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL URL Options]** 部分。

1. 设置 **[!UICONTROL Add Store Code]** 根据您的喜好：

   - **[!UICONTROL URL with Store Code]**: `http://www.yourdomain.com/magento/[store-code]/index.php/url-identifier`
   - **[!UICONTROL URL without Store Code]**: `http://www.yourdomain.com/magento/index.php/url-identifier`

   ![常规配置 — Web URL选项](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Config]**.

1. 单击 **[!UICONTROL Cache Management]** 工作区顶部消息中的链接。 然后，按照说明刷新缓存。

   ![缓存管理消息](./assets/msg-cache-management.png)

## URL疑难解答

如果按照配置说明操作，某些页面将继续使用不安全URL提供服务(`http://`)，请执行以下操作：

- 将（不安全）基本URL更改为安全HTTPS URL。
- 在服务器上，编辑 `.htaccess` 文件（或负载平衡器），以便将非安全URL重定向到安全URL。

## 使用自定义管理员URL

作为 [安全最佳实践](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf)，Adobe建议您使用唯一的管理员URL，而不是默认URL _管理员_ 或常用术语，例如 _后端_. 尽管它不会直接保护您的网站免受确定性错误行为者的攻击，但它可以减小试图获得未经授权访问的脚本的暴露程度。

>[!NOTE]
>
>在实施自定义管理员URL之前，请咨询您的托管提供商。 某些托管提供程序需要标准URL才能符合防火墙保护规则。

在典型安装中，管理员URL和路径紧跟在基本URL之后。 管理路径是根目录下的一个目录。

- **默认基本URL**： `http://yourdomain.com/magento/`
- **默认管理路径**： `admin`
- **默认管理员URL和路径**： `http://yourdomain.com/magento/admin`

尽管可以将管理员URL和路径更改为其他位置，但任何错误都会删除对管理员的访问权限，必须从服务器进行更正。

>[!NOTE]
>
>作为预防措施，除非您知道如何编辑服务器上的配置文件，否则请不要尝试自己更改管理员URL。

### 方法1：从管理员更改

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Advanced]** 并选择 **[!UICONTROL Admin]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Admin Base URL]** 部分。

1. 为自定义URL设置配置选项：

   ![高级配置 — 管理员基本URL](../configuration-reference/advanced/assets/admin-admin-base-url.png){width="600" zoomable="yes"}

   如有需要，清除 **[!UICONTROL Use system value]** 复选框以更改设置。

   - 设置 **[!UICONTROL Use Custom Admin URL]** 到 `Yes`.

   - 输入 **[!UICONTROL Custom Admin URL]**： `http://yourdomain.com/magento/`

     >[!NOTE]
     >
     >管理员URL必须位于同一Commerce安装中，并且具有与店面相同的文档根。

   - 设置 **[!UICONTROL Custom Admin Path]** 到 `Yes`.

   - 对象 **[!UICONTROL Custom Admin Path]**，输入用作自定义管理文件夹名称的路径。

     示例： `sample_custom_admin`

1. 完成后，单击 **[!UICONTROL Save Config]**.

1. 保存更改后，注销管理员并使用新的管理员URL和路径重新登录。

### 方法2：从服务器命令行更改管理路径

1. 打开 `app/etc/env.php` 文件，并将 `frontName` 的参数 `backend` 部分。 然后，保存文件。

   确保仅使用小写字符。

   >[!NOTE]
   >
   >   此方法允许您更改管理员路径，但不能更改管理员URL。

   >[!TIP]
   >
   >对于云基础架构上的Adobe Commerce，您可以使用 `ADMIN_URL` 变量。 请参阅 [管理变量主题](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html) 在 _云基础架构上的Commerce指南_.

   - **默认管理路径**

     ```php?start_inline=1
     'backend' => [
      'frontName' => 'admin'
     ],
     ```

   - **新建管理路径**

     ```php?start_inline=1
     'backend' => [
         'frontName' => 'backend'
     ],
     ```

1. 使用以下方法之一清除缓存：

   - 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**. 然后，单击&#x200B;**[!UICONTROL Flush Magento Cache]**.
   - 在服务器上，执行以下命令：

     ```terminal
     php bin/magento cache:flush
     ```

   >[!NOTE]
   >
   >使用方法1所做的更改优先于在 `app/etc/env.php` 文件。

### 方法3：使用Commerce CLI更改管理员路径

您可以使用CLI `setup:config:set` 命令更改管理员路径。 以下示例使用 `--backend-frontname` 用于将路径从Commerce根目录更改为新的管理员路径的选项：

```terminal
bin/magento setup:config:set --backend-frontname="backend_front_name"
```

此命令更新 `backend` > `frontName` 中的配置选项 `app/etc/env.php` 文件。

## 恢复默认的管理员URL和管理员路径

如果您设置了无效的管理员URL或管理员路径并且无法访问后端，可以通过命令行修复它。

1. 要还原到默认的管理URL，请执行以下命令：

   ```terminal
   php bin/magento config:set admin/url/use_custom 0
   ```

1. 还原到默认管理路径(在 `app/etc/env.php` 如方法2)中所述，执行此命令：

   ```terminal
   php bin/magento config:set admin/url/use_custom_path 0
   ```

1. 使用以下方法之一清除缓存：

   - 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**. 然后，单击&#x200B;**[!UICONTROL Flush Magento Cache]**.
   - 在服务器上，执行以下命令：

     ```terminal
     php bin/magento cache:flush
     ```


[1]: https://en.wikipedia.org/wiki/Transport_Layer_Security
[2]: https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
