---
title: '[!DNL Adobe Commerce B2B]发行说明'
description: 请查看发行说明以了解有关 [!DNL Adobe Commerce B2B] 发行版中的更改的信息。
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: 0b7200331b9b7aa59636a0ff6fd6b98194054a32
workflow-type: tm+mt
source-wordcount: '7820'
ht-degree: 0%

---

# [!DNL Adobe Commerce B2B]发行说明

B2B扩展的这些发行说明捕获了Adobe在发行周期中添加的额外功能和修复，包括：

![新](../assets/new.svg)新功能
![已修复问题](../assets/fix.svg)修复和改进
![已知问题](../assets/bug.svg)已知问题

>[!NOTE]
>
>有关可用Adobe Commerce版本支持的B2B Commerce扩展版本的信息，请参阅[产品可用性](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html)。


## B2B 1.5.0

*2024年10月30日*

[!BADGE 支持]{type=Informative tooltip="支持"}
与Adobe Commerce版本2.4.8-beta1、2.4.7到2.4.7-p2、2.4.6到2.4.6-p7兼容。

Adobe Commerce B2B版本1.5.0也与PHP 8.3兼容，并支持[GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server)。

B2B v1.5.0版本包括新增功能、质量改进和错误修复。

>[!NOTE]
>
> 通过查看[向后不兼容的更改](backward-incompatible-changes.md)主题中的亮点和参考信息，了解B2B 1.5.0版本中引入的向后不兼容更改(BIC)。

### 公司管理

![新](../assets/new.svg) **公司管理**<!--B2B-2901--> — 商户现在可以将公司分配给指定的母公司，以层次结构形式查看和管理Adobe Commerce公司。 将公司分配给父公司后，父公司管理员可以管理公司帐户。 只有授权管理员用户可以添加和管理公司分配。 有关详细信息，请参阅[管理公司层次结构](manage-company-hierarchy.md)。

- 从管理员的&#x200B;*[!UICONTROL Company Account]*&#x200B;页面上的新&#x200B;*[!UICONTROL Company Hierarchy]*&#x200B;部分添加和管理公司分配。

- 按新的&#x200B;*[!UICONTROL Company Type]*&#x200B;设置对公司进行排序和筛选。 在公司网格中，*[!UICONTROL Company Type]*&#x200B;列指示公司是单个公司还是组织层次结构（父项或子项）的一部分。

![新建](../assets/new.svg) **大规模管理公司配置**<!--B2B-2849--> — 现在从&#x200B;*[!UICONTROL Companies]*&#x200B;或&#x200B;*[!UICONTROL Company Hierarchy]*&#x200B;网格管理公司时，可使用&#x200B;*[!UICONTROL Change company setting]*&#x200B;批量操作快速更改选定公司的公司配置设置。 例如，如果您为一组公司创建新的共享目录，则可以在单个操作中更改共享目录配置，而不是单独编辑每个公司。

![新](../assets/new.svg) API开发人员可以使用新的公司关系REST API终结点`/V1/company/{parentId}/relations`创建、查看和移除公司分配。 请参阅&#x200B;*Web API开发人员指南*&#x200B;中的[管理公司对象](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/)。

### 公司帐户

![新建](../assets/new.svg)<!--B2B-2828--> **多公司分配** — 通过将用户分配给多个公司来简化公司用户的公司帐户访问权限。 例如，如果您的一个采购员从多个公司地点订购，请创建一个帐户，并将与该采购员合作的所有公司分配给该帐户。 然后，买家可以一次性登录，并通过从店面中选择公司来切换公司帐户。

>[!NOTE]
>
>可以将一个公司用户分配给多个公司，但他们只能是一个公司的公司管理员。

![新建](../assets/new.svg)<!--B2B-2747--> **公司范围选择器** — 为分配到多个公司的公司用户提供更改店面公司的功能。 当范围被切换时，数据会更新以根据新的公司上下文显示信息。 例如，如果新公司使用不同的共享目录，则公司用户会根据新的共享目录查看产品、价格和其他信息。 与订单、报价和报价模板相关的内容也会根据所选公司的上下文进行更新。

>[!NOTE]
>
>如果公司用户将购物车中具有商品的公司切换为其他公司，请更新购物车，以根据新的公司上下文反映产品分类、定价和促销折扣。

![已修复问题](../assets/fix.svg)<!--ACP2E-1933-->公司管理员现在可以从店面添加公司用户。 以前，当管理员用户尝试添加新用户时，Commerce会记录一个错误： `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`。

### 报价和报价模板

报价功能的改进有助于买方和卖方更有效地管理报价和报价洽谈。

![新](../assets/new.svg) **报价模板**—<!--B2B-3367-->买方和卖方现在可以通过创建可重复使用且可自定义的报价模板来简化报价流程。 使用报价模板，报价洽谈流程可以完成一次，采购员可以为经常性订单生成预批准的链接报价，而不是针对每张订单完成报价洽谈流程。 报价模板通过添加以下高级功能来扩展现有报价功能：

- **订单阈值**&#x200B;允许卖方设置最小和最大订单承诺，确保买方遵守商定的购买量。
- **设置最小和最大物料订单数量**&#x200B;使采购员能够灵活地调整链接报价上的订单数量，而无需新模板或进一步洽谈。
- **跟踪已生成并成功完成订单的链接报价单数**，以了解协议协议的履行情况。
- **链接报价**&#x200B;是预批准的报价，采购员通过有效报价模板生成这些报价，以根据报价模板中协商的条款提交重复订单。

![新](../assets/new.svg) **对现有报价功能的改进**

- **更新的Commerce访问控制列表(ACL)规则**&#x200B;允许B2B管理员和主管管理下属用户的报价和报价模板。 单独的规则支持用于查看、编辑和删除访问权限的粒度配置。

- **将报价另存为草稿**<!--B2B-2566--> — 从购物车创建[报价请求](quote-request.md)时，购买者现在可以将报价另存为草稿，以便在启动与卖方的报价洽谈过程之前对其进行复查和更新。 草稿报价没有到期日期。 购买者可以从其帐户仪表板的[!UICONTROL My Quotes]部分查看和更新草稿报价。

- **重命名报价**<!--B2B-2596--> — 购买者现在可以通过选择&#x200B;**[!UICONTROL Rename]**&#x200B;选项从[报价详细信息](account-dashboard-my-quotes.md#quote-actions)页面更改报价名称。 授权购买者在编辑报价时可以使用此选项。 名称更改事件记录在报价历史记录日志中。

- **重复报价**<!--B2B-2701--> — 买方和卖方现在可以通过复制现有报价创建新的报价。 通过在Admin或[店面](account-dashboard-my-quotes.md#quote-actions)的[报价详细信息视图](quote-price-negotiation.md#button-bar)中选择&#x200B;**[!UICONTROL Create Copy]**，从“报价详细信息”视图中创建了一个副本。

- **将报价项移至请购单列表**<!--B2B-2755--> — 采购员现在可以灵活地从报价中删除产品，并将其保存到请购单列表中（如果他们决定不将其包含在报价洽谈流程中）。

- **从报价中删除多个产品**<!--B2B-2881--> — 在包含大量产品的报价上，购买者现在可以通过选择多个产品并使用报价详细信息页面上&#x200B;*[!UICONTROL Actions]*&#x200B;控件中的&#x200B;*[!UICONTROL Remove]*&#x200B;选项从报价中删除多个产品。 在以前的版本中，购买者必须一次删除一个产品。

- **行项目折扣锁定**<!--B2B-2597--> — 在报价洽谈期间，销售商可以使用行项目折扣锁定以在报价洽谈过程中应用折扣时获得更大的灵活性。 例如，卖方可以对物品应用特殊行物品折扣，并锁定该物品以防止进一步折扣。 锁定项目时，如果应用报价级别折扣，则无法更新项目价格。 请参阅[为购买者](sales-rep-initiates-quote.md)启动报价。

![已修复问题](../assets/fix.svg)**现有报价功能的修复**

- 现在，系统会提示商家在Admin的Quote detail视图中单击&#x200B;*[!UICONTROL Print]*&#x200B;按钮以将报价另存为PDF。 以前，商家会被重定向到包含报价详细信息的页面。<!--ACP2E-1984-->

- 以前，在发送具有`0`百分比的客户报价并更改数量时，管理员会引发异常但保存了数量。 进行此修复后，将引发包含消息的`0 percentage`相应异常。<!--ACP2E-1742-->

- 在报价洽谈期间，卖方现在可以在“洽谈报价报价”折扣字段中指定`0%`折扣，然后将报价发回给买方。 以前，如果卖方输入0%的折扣并将报价发回给买方，管理员会返回`Exception occurred during quote sending`错误消息。<!--ACP2E-1742-->

- 现在，当将ReCaptcha V3配置为店面结账时，ReCaptcha验证在B2B报价的结账过程中可正常工作。 以前，验证失败并显示`recaptcha validation failed, please try again`错误消息。 <!--ACP2E-2097-->

### 采购订单

![修复了问题](../assets/fix.svg) <!--ACP2E-1825-->在公司被阻止后，与公司关联的用户无法再下达采购订单。 以前，与公司关联的用户可以在公司被阻止时下达采购订单。

## B2B v1.4.2-p3

*2024年10月8日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新](../assets/new.svg)添加了与Adobe Commerce 2.4.7-p3+和2.4.6-p8+安全修补程序版本的兼容性。

![已修复问题](../assets/fix.svg)包括[安全公告APSB24-73](https://helpx.adobe.com/security/products/magento/apsb24-73.html)中记录的安全修复。

>[!IMPORTANT]
>
>Adobe Commerce B2B版本1.4.2+与PHP 8.2兼容。如果将Commerce实例升级到版本2.4.7+，请确保该实例使用PHP版本8.2来保持与Adobe Commerce B2B版本的兼容性。 此外，B2B 1.4.2+版本不支持[GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server)。

## B2B v1.4.2-p2

[!BADGE 支持]{type=Informative tooltip="支持"}

![新](../assets/new.svg)添加了与Adobe Commerce 2.4.7-p2+和2.4.6-p7+安全修补程序版本的兼容性。

![已修复问题](../assets/fix.svg)包括安全公告xxxx中记录的安全修复。

>[!IMPORTANT]
>
>Adobe Commerce B2B版本1.4.2+与PHP 8.2兼容。如果将Commerce实例升级到版本2.4.7+，请确保该实例使用PHP版本8.2来保持与Adobe Commerce B2B版本的兼容性。 此外，B2B 1.4.2+版本不支持[GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server)。

## B2B v1.4.2-p1

*2024年8月9日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新](../assets/new.svg)添加了与Adobe Commerce 2.4.7-p1+和2.4.6-p6+安全修补程序版本的兼容性。

>[!IMPORTANT]
>
>Adobe Commerce B2B版本1.4.2+与PHP 8.2兼容。如果将Commerce实例升级到版本2.4.7+，请确保该实例使用PHP版本8.2来保持与Adobe Commerce B2B版本的兼容性。 此外，B2B 1.4.2+当前不支持[GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server)。

## B2B v1.4.2

*2023年10月10日*

[!BADGE 支持]{type=Informative tooltip="支持"}

B2B v1.4.2版本包括质量改进和错误修复。

![已修复问题](../assets/fix.svg) <!--B2B-2897-->如果卖方创建的买方报价包含在与买方公司关联的共享目录中不可用的产品SKU，则系统将显示错误消息`The SKU you entered is not available in the shared catalog. Please check the SKU and try again`。  在销售商删除不可用的产品之前，他们无法保存报价。 以前，报价保存时包含不可用的SKU，并且无法在店面中加载报价。

>[!IMPORTANT]
>
>Adobe Commerce B2B版本1.4.2+与PHP 8.2兼容。如果将Commerce实例升级到版本2.4.7+，请确保该实例使用PHP版本8.2来保持与Adobe Commerce B2B版本的兼容性。 此外，B2B 1.4.2+当前不支持[GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server)。

## B2B v1.4.1

*2023年8月7日*

[!BADGE 支持]{type=Informative tooltip="支持"}[Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html)。 与Adobe Commerce 2.4.7-beta1兼容。

B2B v1.4.1版本包括质量改进和错误修复。

![修复了问题](../assets/fix.svg) <!--ACP2E-1825-->在公司被阻止后，与公司关联的用户无法再下达采购订单。 以前，与公司关联的用户可以在公司被阻止时下达采购订单。

![已修复问题](../assets/fix.svg) <!--ACP2E-1943-->店面现在可正确显示产品延交状态。 以前，可发运的产品被错误地标识为延期交货。

![已修复问题](../assets/fix.svg) <!--ACP2E-1862-->如果公司注册表单包含客户文件类型属性，则在公司创建后，注册过程中上传的文件现在会包含在公司管理员的帐户信息中。 以前，缺少附件。

![已修复问题](../assets/fix.svg) <!--ACP2E-1793-->可配置产品的样本选择器现在按预期显示在申请列表项配置页面中。 以前，样本选择器显示为申请列表项配置页面中的下拉字段。

![已修复问题](../assets/fix.svg) <!--ACP2E-1968-->使用[公司GraphQL查询](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure)返回公司详细信息时，结果现在已成功返回且没有错误。

## B2B v1.4.0

*2023年6月13日*

[!BADGE 支持]{type=Informative tooltip="支持"}[Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html)。 与Adobe Commerce 2.4.7-beta1兼容

此版本包括针对B2B议价报价和多个错误修复的新功能和增强功能。

![新](../assets/new.svg)添加了与Adobe Commerce 2.4.7-beta1的兼容性。

![新](../assets/new.svg) **卖方启动的报价** — 卖方现在可以直接从“管理员”中的“报价”和“客户”网格为买方启动报价。 此功能简化了报价流程，降低了客户的复杂性。 如果客户尚未起动订单，则卖方可以代表客户快速创建报价并开始洽谈流程。 以前，报价只能由买方从店面创建，或由以客户身份登录的卖方创建。

![新](../assets/new.svg) **行项目折扣和洽谈**—<!--B2B-2440-->在报价中，B2B买方和卖方现在可以在行项目层进行洽谈，在达成协议之前应用折扣和交换票据。 备注创建和更新包含在行项目和报价历史记录中，以跟踪通信。 以前，买方和卖方只能交换票据并在报价级别应用折扣。

![修复了问题](../assets/fix.svg)在启用“采购订单”选项并选择使用PayPal付款选项创建的虚拟报价单后，Adobe Commerce现在会在付款期间显示正确的详细信息。 以前，在这些条件下，总数显示为零。

![修复了问题](../assets/fix.svg) <!--ACP2E-1504-->当您尝试保存信用额度超过999的公司时，不会再出现验证错误。 以前，对于大于999的公司信用限制，Adobe商务插入逗号分隔符，这会导致验证错误，阻止保存更新。

![已修复问题](../assets/fix.svg) <!--ACP2E-1474-->现在，当您使用可转让报价下订单时，所选的送货地址保持不变。 以前，在您下订单时，选定的送货地址已更改为默认送货地址。

![修复了问题](../assets/fix.svg) <!--ACP2E-1429-->在B2B功能的存储配置设置中，**[!UICONTROL Enable Shared Catalog direct products price assigning]**&#x200B;字段现在自动禁用。 在店面，当&#x200B;**[!UICONTROL Enable Company]**&#x200B;设置或&#x200B;**[!UICONTROL Enable Shared Catalog]**&#x200B;设置设置为&#x200B;**[!UICONTROL No]**&#x200B;时隐藏。

![已修复问题](../assets/fix.svg) <!--ACP2E-1683-->从店面创建公司帐户时，Commerce现在会在处理公司注册之前验证电子邮件地址。 如果电子邮件地址无效，则操作将失败，并且不会处理任何帐户更新。 以前，即使创建公司帐户的请求由于电子邮件地址无效而失败，也会创建客户帐户。

![修复了问题](../assets/fix.svg) <!--ACP2E-1664-->共享目录和定价结构中包含双引号的产品SKU不会再导致管理员中出现错误。

![已修复问题](../assets/fix.svg) <!--ACP2E-1498-->已更新Commerce应用程序的Varnish配置以防止来宾用户看到来自其他客户组的数据。

### 已知问题

如果在[Adobe Commerce版本2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html)上安装或升级B2B 1.4.0，则会出现以下错误：

```
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

通过为带有[稳定性标记](https://getcomposer.org/doc/04-schema.md#package-links)的B2B安全包添加手动依赖项，可以为B2B安全包添加手动依赖项来解决此问题。 有关说明，请参阅[Adobe Commerce知识库](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html)。

## B2B v1.3.5-p8

*2024年10月8日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新](../assets/new.svg)添加了与Adobe Commerce 2.4.6-p8安全修补程序版本的兼容性。

![已修复问题](../assets/fix.svg)包括[安全公告APSB24-73](https://helpx.adobe.com/security/products/magento/apsb24-73.html)中记录的安全修复。

## B2B v1.3.5-p7

*2024年8月9日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新](../assets/new.svg)添加了与Adobe Commerce 2.4.6-p7安全修补程序版本的兼容性。

## B2B v1.3.5

*2023年3月14日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新](../assets/new.svg)发布了B2B版本1.3.5-p2，以支持与Adobe Commerce 2.4.6-p2的兼容性。

![新](../assets/new.svg)发布了B2B版本1.3.5-p1，以支持与Adobe Commerce 2.4.6-p1的兼容性。

>[!NOTE]
>
>将Commerce从2.4.6升级到[最新版本](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6)后，请确保更新到支持的B2B 1.3.5修补程序版本。 或者，将B2B扩展从版本1.3.5升级到版本1.4.0或更高版本，以获取最新功能。

![新](../assets/new.svg)添加了对Adobe Commerce 2.4.6的支持。

![修复了问题](../assets/fix.svg) <!--- ACP2E-689-->在启用“采购订单”选项并选择使用PayPal付款选项创建的虚拟报价单后，Adobe Commerce现在会在付款期间显示正确的详细信息。 以前，在这些条件下，总数显示为零。

![已修复问题](../assets/fix.svg) <!--- ACP2E-609--> **允许浏览类别**&#x200B;设置的客户组列表不再包含与共享目录相关的客户组。

![已修复问题](../assets/fix.svg) <!--- ACP2E-1244-->税号/增值税编号客户属性现在可按预期与管理员和店面的公司管理员帐户配合使用。 创建公司帐户不再需要自定义税/VAT属性。 以前，当商家创建具有自定义税务/增值税属性的公司帐户时，Adobe Commerce会在店面和管理员上引发验证错误。

![修复了问题](../assets/fix.svg) <!--- ACP2E-1236-->在特定范围上禁用共享目录功能现在可以正常工作。 以前，当商家保存共享目录配置时，Adobe Commerce设置的范围无效。

![修复了问题](../assets/fix.svg) <!--- ACP2E-1203-->管理员用户现在可以为公司用户保存客户自定义属性值。 以前，无法保存公司用户的客户自定义属性。

![修复了问题](../assets/fix.svg) <!--- ACP2E-1221-->当已经分配了许多公司权限时，通过GraphQL提供的公司权限验证功能解决了性能问题。

![修复了问题](../assets/fix.svg) <!--- ACP2E-1242-->当使用快速订购添加的产品数量超过可用库存量时，Adobe Commerce不再在购物车页面上引发错误。

![已修复问题](../assets/fix.svg) <!--- ACP2E-1090--> `SELECT`公司权限操作的性能已得到改进。

![已修复问题](../assets/fix.svg) <!--- ACP2E-2456-->当查询的类别没有明确设置的类别权限时，类别查询现在会根据商店配置设置返回产品价格。

![修复了问题](../assets/fix.svg) <!--- ACP2E-6829-->在用批准的报价请求完成购买时，**[!UICONTROL Place Order]**&#x200B;按钮现在可按预期工作。 可协商的报价`negotiableQuoteCheckoutSessionPlugin`插件的问题已得到解决。

## B2B v1.3.4-p10

*2024年10月9日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新](../assets/new.svg)添加了对Adobe Commerce 2.4.5-p10的支持。

![已修复问题](../assets/fix.svg)包括[安全公告APSB24-73](https://helpx.adobe.com/security/products/magento/apsb24-73.html)中记录的安全修复。

## B2B v1.3.4

*2022年8月9日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新](../assets/new.svg)添加了对Adobe Commerce 2.4.5的支持。

![修复了问题](../assets/fix.svg) <!--- ACP2E-453-->Adobe Commerce不再在API调用更新现有公司时发送电子邮件通知。 现在，仅当创建公司时才发送电子邮件。

![已修复问题](../assets/fix.svg) <!--- ACP2E-406-->启用&#x200B;**[!UICONTROL Enable Cross Border Trade]**&#x200B;计税设置后，Adobe Commerce现在可以正确计算可转让报价的总计。

![修复的问题](../assets/fix.svg) <!--- ACP2E-322-->启用&#x200B;**[!UICONTROL Move out of stock to the bottom]**&#x200B;设置后，库存更新后，可配置产品现在移至产品列表中的最后一个位置。 实施新的自定义数据库查询以确保Elasticsearch索引排序顺序现在遵循启用管理员的排序顺序。 以前，启用此设置时，可配置产品及其子产品不会移到列表的底部。

![已修复问题](../assets/fix.svg) <!--- ACP2E-308-->采购订单电子邮件现在遵循多站点部署中每个网站的电子邮件发送设置。 **[!UICONTROL Disable Email Communications]**&#x200B;设置的检查已添加到电子邮件队列的自定义逻辑中。 以前，Adobe Commerce不遵守辅助网站的电子邮件发送设置。

![修复了问题](../assets/fix.svg) <!--- ACP2E-302-->为清楚起见，已更改快速订购页面SKU字段的标题。

![已修复问题](../assets/fix.svg) <!--- ACP2E-543-->当购物者在&#x200B;**输入SKU或产品名称**&#x200B;字段中输入无效的SKU时，Adobe Commerce现在显示信息更丰富的错误消息。

![修复了问题](../assets/fix.svg) <!--- ACP2E-1753-->在保存公司后，公司管理员的&#x200B;**[!UICONTROL Account Created in]**&#x200B;字段现在会保留其预期值。

![已修复问题](../assets/fix.svg) <!--- ACP2E-722 -->在检索按`uid`筛选的申请列表时，`customer`查询不再返回空结果。

![修复了问题](../assets/fix.svg) <!--- ACP2E-210 -->在`collectQuoteTotals`调用之前添加了一个插件，以确保仅应用一次商店积分。

![已修复问题](../assets/fix.svg) <!--- ACP2E-665 -->管理员从管理员中删除客户的帐户后，这些客户现在会被重定向到登录页面。 以前，Adobe Commerce会引发错误。 插件(`SessionPlugin`)代码块现在位于`try…catch`块中。 以前，此代码不会封装在通用异常处理块中。

![已修复问题](../assets/fix.svg) <!--- ACP2E-661 -->在移动设备模式下的“快速订购”页面上，输入有效的产品名称或SKU后按&#x200B;**Enter**&#x200B;会立即将购物者转到下一个预期字段。

![已修复问题](../assets/fix.svg) <!--- ACP2E-607 -->公司名称现在在签出工作流的帐单和送货地址部分中按预期可见。

![已修复问题](../assets/fix.svg) <!--- ACP2E-375 -->在禁用&#x200B;**[!UICONTROL Zero Subtotal Checkout]**&#x200B;付款方式时，存储点数现在不可用。 以前，商店积分复选框在管理员下订单期间不起作用。 应用程序没有用商店点数下订单，并显示此错误： `The requested Payment Method is not available`。

## B2B v1.3.3

*2022年8月9日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新](../assets/new.svg)添加了对Adobe Commerce 2.4.4的支持。

![修复了问题](../assets/fix.svg) <!--- MC-41985-->在具有100,000多个公司角色的部署中，从Adobe Commerce 2.3.x升级到Adobe Commerce 2.4.x所需的时间已大大减少。

![已修复问题](../assets/fix.svg) <!--- MC-42153-->启用&#x200B;**[!UICONTROL Payment on Account]**&#x200B;付款方法后，POST`V1/order/:orderId/invoice`请求现在支持创建部分发票。 以前，Adobe Commerce引发此错误： `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`。 [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![已修复问题](../assets/fix.svg) <!--- MC-41975-->当客户的购物车包含其他产品时，PayPal Payflow Pro现在可与B2B可协商报价一起按预期工作。 Adobe Commerce现在可成功处理订单，并按预期向客户发送电子邮件。 以前，Adobe Commerce会引发致命错误，并向客户发送一封包含零值的确认电子邮件。

![修复了问题](../assets/fix.svg) <!--- MC-41819-->在排除共享目录中的某些产品后，目录搜索结果页面上现在可正确显示分页。

![修复了问题](../assets/fix.svg) <!--- MC-42886-->在Admin中创建或保存公司用户时，客户自定义属性现在按预期保存。

![修复了问题](../assets/fix.svg) <!--- MC-42927-->现在，单击一下以阻止提交多个表单，“新建公司”表单上的&#x200B;**[!UICONTROL Submit]**&#x200B;按钮会被禁用。 以前，您可以多次提交此表单，方法是反复单击此按钮，这会生成错误。

![修复了问题](../assets/fix.svg) <!--- MC-42787-->当购物者登录到已禁用重新订购的商店时，Adobe Commerce不再在店面上显示重新订购链接。

![修复了问题](../assets/fix.svg) <!--- MC-43115-->在启用共享目录后，按SKU进行的快速订购搜索现在不区分大小写。

![已修复问题](../assets/fix.svg) <!--- MC-42203-->您现在可以在创建公司时更新客户属性的文件。 以前，当您尝试创建具有`File`类型的附件的公司时，Adobe Commerce未创建该公司，并在异常日志中记录此错误： `Something went wrong while saving file`。

![已修复问题](../assets/fix.svg) <!--- MC-42242-->您现在可以创建客户帐户的公司，该客户帐户具有类型为(`File`)或(`Image`)的自定义属性。 以前，如果帐户具有其中一个可自定义选项，公司编辑页面加载器无法解析，从而导致无法编辑公司详细信息。

![已修复问题](../assets/fix.svg) <!--- MC-42268-->启用共享目录后，`products`查询现在会返回准确的`total_count`字段。

![已修复问题](../assets/fix.svg) <!--- MC-42203-->您现在可以在创建公司时更新客户属性的文件。 以前，当您尝试创建具有`File`类型的附件的公司时，Adobe Commerce未创建该公司，并在异常日志中记录此错误： `Something went wrong while saving file`。

![已修复问题](../assets/fix.svg) <!--- MC-43178-->禁用联机配送方法后，_公司配置_&#x200B;和&#x200B;_创建公司_&#x200B;页面现在可按预期工作。 添加了验证，以防止尝试处理禁用的配送模块。 以前，Adobe Commerce显示此错误： `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`。

![修复了问题](../assets/fix.svg) <!--- MC-42214--> _类别_&#x200B;页面现在在部分索引期间生成权限时显示一致的产品数据。 此进程中添加了新的目录权限部分索引器。 以前，索引器运行时显示的数据不正确。

![修复了问题](../assets/fix.svg) <!--- MC-42567-->现在，当使用目录权限并将产品分配给共享目录时，`categoryList`查询返回正确数量的产品。

![修复了问题](../assets/fix.svg) <!--- MC-42528--> `categoryList`查询现在遵循类别权限并仅返回允许的类别。 以前，它会返回所有已分配和未分配的类别。

![修复了问题](../assets/fix.svg) <!--- MC-42399--> `rest/V1/company/{id}`请求现在按预期返回`is_purchase_order_enabled`属性值。

![已修复问题](../assets/fix.svg) <!--- ACP2E-128-->自定义客户属性现在按预期显示在&#x200B;_公司管理员_&#x200B;选项卡中。

![修复了问题](../assets/fix.svg) <!--- ACP2E-130-->“我的帐户”页面上的“我的愿望清单”块现在按预期显示给公司管理员和公司用户。

![已修复问题](../assets/fix.svg) <!--- ACP2E-133-->购物车中不再显示快速订购错误。 以前，在目录中找不到SKU时，Adobe Commerce在购物车中显示此错误： `The SKU was not found in the catalog`。

![已修复问题](../assets/fix.svg) <!--- ACP2E-194-->已优化共享目录保存操作以更快地执行。 以前，与多个客户组共享目录保存可能需要几分钟的时间。

![修复了问题](../assets/fix.svg) <!--- MC-42240-->当删除父类别时，Adobe Commerce现在会从`sharedcatalog_category_permissions`表中删除所有子类别权限。 以前，只删除父类别数据。

## B2B v1.3.2

*2022年8月29日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新](../assets/new.svg)添加了对Adobe Commerce 2.4.3的支持。

![已修复问题](../assets/fix.svg) <!--- MC-39862--> Adobe Commerce现在已成功发送有关过期可转让报价的更新电子邮件。 以前，当可转让报价过期时，Adobe Commerce不会发送更新电子邮件。

![修复了问题](../assets/fix.svg) <!--- MC-40682-->现在，当`cron`作业缺失时，Adobe Commerce成功发送有关即将过期和过期可转让报价的更新电子邮件。

### 公司

![修复了问题](../assets/fix.svg) <!--- MC-41542-->新建公司帐户页面国家/地区下拉字段不再列出空选项值。 以前，前两个选项值和国家/地区代码`AN`为空。

![修复了问题](../assets/fix.svg) <!--- MC-41260-->单击&#x200B;**[!UICONTROL Return]**&#x200B;按钮以查看公司用户创建的订单时，会按预期将管理用户重定向到“创建退货”页面。 以前，管理员会被重定向至“订单历史记录”页面。

![修复了问题](../assets/fix.svg) <!--- MC-40798-->在`bin/magento setup:upgrade`期间执行`app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply`方法时，Adobe Commerce不再因内存不足错误而失败。 以前，Adobe Commerce在初始化权限时不使用批次大小进行集合，而是加载所有公司角色的集合。

![已修复问题](../assets/fix.svg) <!--- MC-40551-->公司用户现在可以编辑和更新客户自定义属性值。 以前，这些属性无法与“创建和编辑”用户表单正确绑定。 公司用户可以输入其他属性值，但Adobe Commerce未正确保存这些值。

![修复了问题](../assets/fix.svg) <!--- MC-32653-->现在可以按预期翻译公司角色权限的资源树。 以前，即使存在有效的翻译文件，也不翻译权限树。

![已修复问题](../assets/fix.svg) <!--- MC-40358--> Adobe Commerce现在可按预期保存B2B用户的自定义客户属性值。 以前，创建包含自定义客户属性的公司帐户会触发模板错误，并且Adobe Commerce无法成功加载表单。 向`company_create_account`的布局添加参数解决了此问题。

![修复了问题](../assets/fix.svg) <!--- MC-41721-->公司用户筛选器（如“显示所有用户”、“显示活动用户”和“显示非活动用户”）现在按预期工作。 以前，在公司用户页面上过滤操作会导致JavaScript错误。

### 公司信用

![修复了问题](../assets/fix.svg) <!--- MC-41551-->现在，如果管理员具有仅包含网站级别特权的受限帐户，则可以创建使用网站以外其他货币的公司。

![已修复问题](../assets/fix.svg) <!--- MC-41523--> Adobe Commerce现在从正确的`from`电子邮件地址和范围发送公司电子邮件。 以前，在发送公司信用分配或更新电子邮件时，Adobe Commerce不考虑网站范围。

### 快速订购

![修复了问题](../assets/fix.svg) <!--- MC-42104-->现在，使用CSV文件中的快速订单创建订单可以按预期对不存在的SKU起作用。

![修复了问题](../assets/fix.svg) <!--- MC-40268-->使用快速订购在多个SKU上搜索现在可按预期工作。 以前，结果包含重复条目。

![修复了问题](../assets/fix.svg) <!--- MC-40261-->现在，当您在快速订购期间使用SKU选择多个产品时，“添加的产品”列表显示会将输入的SKU视为同样的小写和大写。

![已修复问题](../assets/fix.svg) <!--- MC-40225-->使用快速订购现在会添加购物者指定数量的产品。 以前，Adobe Commerce只会在购物者指定的数量超过一个时添加一个产品。

![已修复问题](../assets/fix.svg) <!--- MC-41283-->快速订购自动完成功能现在适用于部分SKU。

![已修复问题](../assets/fix.svg) <!--- MC-41299--> Adobe Commerce现在在快速订购页面的自动建议列表和搜索结果中显示已配置为&#x200B;**不可单独显示的产品**。

![已修复问题](../assets/fix.svg) <!--- MC-42402-->购物者现在可以使用快速订购单按包含大写字符的SKU添加多个产品。 以前，只添加第一个产品。

### 可协商的报价

![已修复问题](../assets/fix.svg) <!--- MC-41232-->在URL字段中粘贴可协商报价的链接并成功登录后，购物者现在被重定向到可协商报价页面。 以前，购物者会被重定向到“我的帐户”页面。

![修复了问题](../assets/fix.svg) <!--- MC-39317-->对于包含在结账期间创建的客户帐户中具有“可自定义日期选项”的产品的订单，重新排序现在可按预期工作。 以前，Adobe Commerce不处理重新排序并显示此错误： `The product has required options. Enter the options and try again`。

![已修复问题](../assets/fix.svg) <!--- MC-39063-->在禁用采购订单模块的结账过程中，可转让报价单的送货地址不再可编辑。 此行为是以前的修复导致的，该修复中的`isQuoteAddressLocked`已从可协商的报价签出渲染器中移除。

![已修复问题](../assets/fix.svg) <!--- MC-38967-->商家现在可以从管理员将产品添加到可协商的报价。

### 采购订单

![修复了问题](../assets/fix.svg) <!--- MC-39983-->现在，当您使用PayPal Express结帐下达采购订单时（**[!UICONTROL Name Prefix]**&#x200B;属性设置为`required`），Adobe Commerce会按预期显示信息性错误消息。 以前，Adobe Commerce不会下订单或显示错误消息。

![修复了问题](../assets/fix.svg) <!--- MC-39620-->启用Google标签管理器后，采购订单模块中账单地址的UI组件现在可正确使用报价地址。 以前，支付页面上发生JavaScript错误。

### 申请列表

![已修复问题](../assets/fix.svg) <!--- MC-40426-->商户现在可以使用POST`rest/all/V1/requisition_lists`端点为客户创建申请列表。 以前，当您尝试创建申请列表时，Adobe Commerce抛出此400错误： `Could not save Requisition List`。

![已修复问题](../assets/fix.svg) <!--- MC-41123-->当购物车还包含缺货产品时，购物车的缺货产品现在会显示&#x200B;**[!UICONTROL Add to Requisition List]**&#x200B;按钮。 以前，如果购物车包含两个产品，其中一个产品缺货，则这两个产品都不会显示&#x200B;_[!UICONTROL Add to Requisition List]_按钮。

![已修复问题](../assets/fix.svg) <!--- MC-40877-->您现在可以使用REST API将产品添加到申请列表。

![已修复问题](../assets/fix.svg) <!--- MC-40155-->申请列表&#x200B;**[!UICONTROL Latest Activity Date]**&#x200B;值现在遵循区域设置格式。

![修复了问题](../assets/fix.svg) <!--- MC-39580-->当您从申请列表中编辑捆绑产品时，Adobe Commerce不再引发致命错误。

![修复了问题](../assets/fix.svg) <!--- MC-40454-->现在，当您从申请列表将带有可自定义选项`(File)`的产品添加到愿望清单时，Adobe Commerce会显示正确的产品价格。 指向已上传文件的链接也会按预期显示。 以前，Adobe Commerce显示的产品价格不正确，并且不显示指向文件的链接。

![修复了问题](../assets/fix.svg) <!--- MC-36383-->现在可以将带有可自定义选项`(File)`的产品从申请列表添加到购物车。

### 共享目录

![修复了问题](../assets/fix.svg) <!--- MC-40497-->角色仅限于特定网站的管理员现在可以创建、查看和编辑共享目录。 以前，当角色有限的管理员尝试创建共享目录时，Adobe Commerce会引发致命错误。

![已修复问题](../assets/fix.svg) <!--- MC-41337-->分层导航结果现在包含具有过滤属性的产品的准确计数，购物者现在可以应用多个过滤器。 以前，只能应用一个过滤器，因此Adobe Commerce在分层导航中显示不准确的产品计数。

![已修复问题](../assets/fix.svg) <!--- MC-40779--> Adobe Commerce现在在搜索结果中的分层导航筛选器中正确显示产品计数。 以前，“搜索结果”页的插件不使用Elasticsearch，而是向数据库发出新查询。

![修复了问题](../assets/fix.svg) <!--- MC-39978-->当商家从默认共享目录中删除所有产品时，Adobe Commerce不再删除层价。

![修复了问题](../assets/fix.svg) <!--- MC-39802-->筛选器现在按当前类别进行筛选，并在启用共享目录的情况下在所有页面上正确显示。 以前，仅针对当前页面错误地计算了过滤器，并且没有按当前类别进行过滤。

![修复了问题](../assets/fix.svg) <!--- MC-39522-->启用共享目录后，GraphQL `products`查询不再返回未分配给共享目录之产品的价格范围和类别。 以前，查询返回产品的聚合，即使产品本身未在`items`数组中返回。

## B2B v1.3.1

*2021年2月9日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新](../assets/new.svg)添加了对Adobe Commerce 2.4.2的支持。

采购订单现在支持![新的](../assets/new.svg)在线付款方式。

![修复了问题](../assets/fix.svg)当在先前订单中使用可配置产品时，将产品直接从申请列表添加到购物车不再返回系统错误。

![已修复问题](../assets/fix.svg)在部署拆分数据库配置时，Adobe Commerce现在正确显示采购订单的“需要我的审批”选项卡。

![已修复问题](../assets/fix.svg)当您查看采购订单时，Adobe Commerce现在会显示有关捆绑产品和礼品卡的详细信息。

![修复了问题](../assets/fix.svg)在启用了&#x200B;**[!UICONTROL Website Restriction]**&#x200B;且&#x200B;**[!UICONTROL Restriction Mode]**&#x200B;设置为`Private Sales: Login Only`的商店中浏览时，在登录到购物者的帐户后，购物者现在会按预期进行重定向。 以前，购物者会被重定向到商店主页。<!--- MC-38934-->

![修复了问题](../assets/fix.svg)现在，在具有包含许多客户(大于13000)的B2B公司层次结构的部署中，订单历史记录会按预期加载到公司管理员的帐户仪表板页面中。 以前，订单历史记录加载缓慢或根本不加载，Adobe Commerce显示503错误。<!--- MC-38830-->

![修复了问题](../assets/fix.svg)当您从“类别”页面将带有可自定义选项的未配置产品添加到申请列表时，Adobe Commerce不再显示多条相同的警告消息。<!--- MC-38342-->

![已修复问题](../assets/fix.svg)启用B2B共享目录后，新的和重复的产品现在会按预期显示在类别页面上。<!--- MC-38307-->

![修复了问题](../assets/fix.svg)在更新公司的客户组时，Adobe Commerce现在维护了与公司管理员关联的正确`store_id`。 以前，在更新组时，`store_id`更改为默认存储。<!--- MC-38196-->

![已修复问题](../assets/fix.svg) Adobe Commerce现在将分组产品作为简单产品列表保存到申购单列表中，其方式与将分组产品添加到购物车相同。 以前，由于Adobe Commerce保存分组产品的方式，申请列表中分组产品的链接始终重定向到简单产品，而不是分组产品。<!--- MC-38049-->

![修复了问题](../assets/fix.svg)在以CSV格式导出订单信息时，您现在可以按&#x200B;**[!UICONTROL Company Name]**&#x200B;字段筛选订单。 以前，Adobe Commerce在`var/export/{file-id}`中记录错误。<!--- MC-37785-->

![已修复问题](../assets/fix.svg)当您在店面中选择“创建新申请列表”选项卡时，Adobe Commerce现在会按预期显示“创建申请列表”弹出窗口。<!--- MC-37915-->

![已修复问题](../assets/fix.svg)申请列表现在包含已添加到列表的所有分组产品和数量。 以前，当商家从产品详细信息页面将产品添加到申购单列表后导航到该列表时，Adobe Commerce显示以下错误： `1 product(s) require your attention - Options were updated. Please review available configurations`。<!--- MC-37621-->

![修复了问题](../assets/fix.svg)在多站点部署中创建公司时，正确的商店视图现在与相关网站关联。 以前，您无法创建公司，Adobe Commerce显示此错误： `The store view is not in the associated website`。<!--- MC-37488-->

![修复了问题](../assets/fix.svg)SKU使用快速订购功能订购产品不会再导致CSV文件中的产品数量重复。<!--- MC-37427-->

![修复了问题](../assets/fix.svg)当“快速订购”页面的&#x200B;_[!UICONTROL Enter Multiple SKUs]_部分包含空值时，**[!UICONTROL Add to Cart]**按钮不再被阻止。 Adobe Commerce现在改为显示一条消息，提示您输入有效的SKU。<!--- MC-37387-->

![已修复问题](../assets/fix.svg)当您从以下申请列表提交产品审核时，Adobe Commerce现在会在产品页面上显示此消息： `You submitted your review for moderation`。 该审阅也会显示在待处理审阅页面上（管理员&#x200B;**[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**）。 以前，尽管Adobe Commerce将审核添加到待处理审核列表，但在产品页面上抛出404错误。<!--- MC-37119-->

![已修复问题](../assets/fix.svg) `sharedCatalogUpdateCategoryPermissions`使用者的性能已得到改进。 创建共享目录后，目录权限索引器现在仅使用共享目录中的客户组ID，而不使用所有客户组。<!--- MC-36770-->

![修复了问题](../assets/fix.svg)与购物者的非默认地址关联的自定义客户地址属性字段现在按预期保存在店面结账工作流中。<!--- MC-36630-->

![已修复问题](../assets/fix.svg)现在，可以按预期通过管理员REST API (`rest/V1/carts/{<CART_ID>/items`)为购物者下达属于商店默认共享目录的产品订单。 Adobe Commerce现在检查在`\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave`中验证共享目录权限之前是否已将产品分配给公共目录。 以前，Adobe Commerce未将产品添加到购物车的同时引发此错误： `No such shared catalog entity`。<!--- MC-36535-->

![已修复问题](../assets/fix.svg) Adobe Commerce现在从Adobe Commerce商店的地址发送新的公司用户注册电子邮件。 以前，此电子邮件是从公司管理员的地址发送的。<!--- MC-36480-->

![修复了问题](../assets/fix.svg) Adobe Commerce现在在允许商家保存新属性之前，会检查自定义属性是否与保留的公司属性名称重复。<!--- MC-36282-->

![已修复问题](../assets/fix.svg) `credit_history`查询现在返回指定公司最初分配金额和购买金额的信用历史记录。 以前，此查询返回错误。

![已修复问题](../assets/fix.svg)“编辑帐户信息”页面上的&#x200B;**[!UICONTROL Company]**&#x200B;和&#x200B;**[!UICONTROL Job Title]**&#x200B;字段不再可编辑。

### 已知问题

- B2B购买者可以使用在线支付方法来绕过通常的采购订单流程。 如果买方可以将整个结账总额减少到0（例如，通过促销代码或礼品卡），然后移除代码或礼品卡，则可能会发生这种情况。 即使在这些条件下，Adobe Commerce仍会根据所分配目录中的商品的价格下正确数量的订单。 **_解决方法_**：为采购订单审批启用在线付款方式时，请禁用礼品卡和优惠券代码。<!--- B2B-1603-->

- 在禁用&#x200B;**[!UICONTROL In-Context Mode]**&#x200B;的情况下，当买家尝试使用PayPal Express结帐从采购订单下订单时，会被重定向到购物车。<!--- B2B-1604-->

- 当采购员创建采购订单，然后导航到结帐页面时，Adobe Commerce有时会显示404错误。 当采购员先前使用在线付款方法创建不同的采购订单而未完成之前的采购就浏览到结帐页面时，会发生此错误。 采购员仍然可以下采购订单。 **_因应措施_**：无。<!--- B2B-1605-->

- 在采购订单结账期间，即使买方在最终结账期间更改了付款方式，特定付款方式的折扣也会保留。 因此，客户可以获得他们无权获得的折扣。 出现此问题的原因是，尽管付款方式发生了更改，但仍应用了原始付款方式的购物车规则。 **_因应措施_**：无。 请参阅[Adobe Commerce 2.4.2 B2B已知问题：更改付款方式后在线采购订单的折扣仍然存在](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) _知识库_&#x200B;文章。<!-- B2B-1012 -->

- `deleteRequisitionListOutput`查询返回有关已删除的申请列表的详细信息，而不是其余的申请列表。<!--- MC-39894-->

## B2B v1.3.0

*2020年10月15日*

[!BADGE 支持]{type=Informative tooltip="支持"}

此版本包括对订单审批、配送方式、购物车和管理员操作日志记录进行了改进。

![新](../assets/new.svg)添加了对Adobe Commerce 2.4.1的支持。

![新](../assets/new.svg) B2B订单审批已得到增强，以提高可用性并允许对采购订单执行批量操作。

![新](../assets/new.svg) B2B商家现在可以控制提供给每个公司的配送方式。<!--- BUNDLE-160 161 162 -->

![新](../assets/new.svg)商家现在可以允许用户在一次操作中清除其购物车的内容，并且可以在每个网站<!--- BUNDLE-108 -->上独立配置此功能

![新](../assets/new.svg) B2B购买者现在可以将单个项目或其购物车的全部内容直接添加到申请列表。<!--- BUNDLE-145 144-->

![新](../assets/new.svg) B2B商户可以从管理员代表客户创建订单，使用帐户付款作为付款方式。<!--- BUNDLE-166 178-->

![新](../assets/new.svg)商家现在可以从客户的详细信息页面直接查看与用户关联的所有报价。<!--- BUNDLE-139 -->

![新](../assets/new.svg)商户现在可以按公司筛选当前在线网格。<!--- BUNDLE-137 -->

![新](../assets/new.svg)管理员现在可以按销售代表在管理员中筛选客户。<!--- BUNDLE-110 -->

![新](../assets/new.svg)为了减少创建欺诈或垃圾邮件帐户，商家现在可以在店面的新公司申请表中启用Google reCAPTCHA。<!--- BUNDLE-154 -->

在公司模块中执行的![新](../assets/new.svg)管理员操作现在记录在管理员操作日志中。 从所有相关公司模块记录操作： `Company`、`NegotiableQuote`、`CompanyCredit`、`SharedCatalog`。<!--- BUNDLE-180 181 182 183 -->

![修复了问题](../assets/fix.svg)当登录的管理员无权删除安装了B2B的部署中的客户时，Adobe Commerce不再在&#x200B;**客户**&#x200B;页面上显示&#x200B;**[!UICONTROL Delete customer]**&#x200B;按钮。<!--- MC-35655-->

![已修复问题](../assets/fix.svg)当您在客户网格上编辑客户时，不再自动为分配到公司的客户更改客户组。<!--- MC-35254-->

![已修复问题](../assets/fix.svg)当商家创建共享目录时，当在目录权限设置中为客户组分配了此访问权限时，类别中&#x200B;**[!UICONTROL Display Product Prices]**&#x200B;和&#x200B;**[!UICONTROL Add to Cart]**&#x200B;功能的权限现在自动设置为`Allow`。 以前，即使将目录权限设置为`Allow`.<!--- MC-34792-->，这些设置也会自动设置为`Deny`

![修复了问题](../assets/fix.svg)从产品编辑页面编辑产品时，不再覆盖共享目录类别权限。<!--- MC-34777-->

![已修复问题](../assets/fix.svg) Adobe Commerce现在发送电子邮件通知，确认当商家启用&#x200B;**[!UICONTROL Allow To Exceed Credit Limit]**&#x200B;设置时，客户有权超过指定的信用额度。 以前，Adobe Commerce发送的通知电子邮件指示客户无权超过限制。<!--- MC-34584-->

![修复了问题](../assets/fix.svg)对于捆绑产品的子项，围绕申请列表上的产品价格的HTML容器现在已正确呈现。<!--- MC-36331-->

![已修复问题](../assets/fix.svg)商家现在可以指定在多语言部署中创建公司时发送公司用户电子邮件的语言。 以前，商家可以通过的下拉菜单选择相应的商店视图和语言，但此菜单不会显示。 <!--- MC-35777-->

![已修复问题](../assets/fix.svg)自定义客户地址属性字段现在按预期显示在店面结账工作流中。<!--- MC-35607-->

![已修复问题](../assets/fix.svg) B2B功能配置选项卡现在可正确打开。 <!--- MC-35458-->来宾现在可以使用QuickOrder将产品添加到购物车，然后成功删除项目。 以前，当购物者使用QuickOrder将多个产品添加到购物车，然后移除产品时，产品未被移除。<!--- MC-35327-->

![已修复问题](../assets/fix.svg)现在可以使用REST APIPUT`/V1/company/:companyId`请求更新公司，而无需在状态配置为&#x200B;**不需要**&#x200B;时指定`region_id`。 以前，即使不需要`region_id`，如果未指定，Adobe Commerce也会引发错误。<!--- MC-35304-->

![修复了问题](../assets/fix.svg)当您使用REST API （`http://magento.local/rest/V1/company/2`，其中`2`表示公司ID）创建或更新B2B公司时，响应现在按预期包含`applicable_payment_method`或`available_payment_methods`的设置。<!--- MC-35248-->

![已修复问题](../assets/fix.svg)当商家在店面中创建申购单列表时使用&#x200B;**Enter**&#x200B;按钮而不是单击&#x200B;**[!UICONTROL Save]**&#x200B;按钮时，Adobe Commerce不再显示404页面。<!--- MC-35094-->

![修复了问题](../assets/fix.svg)将新产品分配给公共共享目录后，类别权限不再更改。 以前，类别权限是重复的。<!--- MC-34386-->

![修复了问题](../assets/fix.svg)用于更新公司电子邮件的REST API终结点PUT`rest/default/V1/company/{id}`不再区分大小写。<!--- MC-34308-->

![已修复问题](../assets/fix.svg)禁用奖励模块不再影响客户帐户上的B2B功能。 以前，在禁用奖励模块时，不会显示以下与B2B相关的选项卡：公司配置文件、公司用户以及角色和权限。<!--- MC-34191-->

![修复了问题](../assets/fix.svg)在对公司帐户进行更改时，Adobe Commerce现在在电子邮件通知中使用正确的发件人名称。 以前，Adobe Commerce使用所有电子邮件的默认范围中定义的一般联系人发件人姓名。<!--- MC-33917-->

![已修复问题](../assets/fix.svg)您现在可以成功地为包含物理和虚拟产品的订单实施多发货。<!--- MC-33818-->

![已修复问题](../assets/fix.svg)在启用了&#x200B;**[!UICONTROL Access Restriction]**&#x200B;且&#x200B;**[!UICONTROL Restriction Mode]**&#x200B;设置为`Sales: Login Only`的情况下，商家现在可以从“我的帐户”和“公司结构”页面中的&#x200B;_[!UICONTROL Company Users]_部分创建公司用户。 以前，当商家尝试创建用户时，Adobe Commerce引发此错误： `Can not register new customer due to restrictions are enabled`。<!--- MC-33608-->

![已修复问题](../assets/fix.svg)当客户保存其帐户信息时，Adobe Commerce不再将客户的客户组重置为默认值。<!--- MC-33554-->

![修复了问题](../assets/fix.svg)管理员将具有活动购物车的客户分配给客户组时，Adobe Commerce不再引发致命错误。<!--- MC-33313-->

![已修复问题](../assets/fix.svg) Adobe Commerce现在为快速订购和申请列表页面提供`addToCart`个DataLayer事件。 <!--- MC-33295-->

![已修复问题](../assets/fix.svg)发送给分配给公司的销售代表的通知电子邮件现在包含分配的公司徽标。 以前，通知电子邮件包含默认的LUMA徽标，而不是上传的公司徽标。<!--- MC-33232-->

![已修复问题](../assets/fix.svg)申请列表现在包含已添加到该列表的所有分组产品和数量。 以前，当商家从产品详细信息页面将产品添加到申购单列表后导航到该列表时，Adobe Commerce显示以下错误： `1 product(s) require your attention - Options were updated. Please review available configurations`。<!--- MC-32877-->

![已修复问题](../assets/fix.svg)启用共享目录后，`products`查询现在会返回准确的`total_count`字段。<!--- MC-42268-->

![已修复问题](../assets/fix.svg)禁用联机配送方式后，“公司配置”和“创建公司”页面现在可按预期工作。 添加了验证，以防止尝试处理禁用的配送模块。 以前，Adobe Commerce显示此错误： `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`。<!--- MC-43178-->

![已修复问题](../assets/fix.svg)集成测试内存消耗已减少，这改进了测试性能并减少了完成测试所需的时间。<!--- AC-266-->

## B2B v1.2.0

*2020年7月28日*

[!BADGE 支持]{type=Informative tooltip="支持"}

![新](../assets/new.svg)添加了对Adobe Commerce 2.4.0的支持。

![新](../assets/new.svg)店面订单搜索，并附上对[Divante](https://www.divante.com/)和社区成员的Marek Mularczyk贡献的感谢。

![新](../assets/new.svg)采购订单已增强并重写。 现在，默认情况下包含在Adobe Commerce中。

已实施![个新的](../assets/new.svg)采购订单审批规则。 这些规则允许用户通过为订单创建采购规则来控制采购订单工作流。

默认情况下，Adobe Commerce现在包括![New](../assets/new.svg)客户登录信息。 此功能允许站点员工通过以客户身份登录来协助客户查看他们看到的内容。

![修复了问题](../assets/fix.svg)对于具有Elasticsearch的分层导航，属性聚合现在可以正常工作

![修复了问题](../assets/fix.svg)按特殊字符搜索订单现在可正常工作。

![修复了问题](../assets/fix.svg)单击&#x200B;**[!UICONTROL Clear All]**&#x200B;按钮后，现在将展开而不是折叠所有筛选器。

![已修复问题](../assets/fix.svg)产品SKU/名称现已包含在订单历史记录搜索筛选器摘要中。

![已修复问题](../assets/fix.svg)排序指示器现在在“我的采购订单”网格中正确显示。

![已修复问题](../assets/fix.svg)现在，您只能单击“批准”、“取消”、“拒绝”和“采购订单”按钮一次。 以前，您可以多次单击按钮。

![修复了问题](../assets/fix.svg)采购订单批准、拒绝、取消和验证按钮现在可在移动设备上正确呈现。

![修复了问题](../assets/fix.svg)以前，在批准带有已过期折扣的采购订单时，会将订单全额下单，并且不会更新采购订单总计。 现在，采购订单总计将更新以显示正确总计。

![修复了问题](../assets/fix.svg) 2.3.4中引入了一个问题，该问题导致自定义扩展属性不能从客户地址复制到报价地址。 此问题已修复。

![修复了问题](../assets/fix.svg)如果安装了B2B，则在将类别分配给共享目录时将会显示SQL错误。 此问题已修复。

![修复了问题](../assets/fix.svg)由于变量类型值不正确，管理员无法将可配置产品添加到订单。 不会填充选项下拉列表。 此功能现在可以正常工作。

![修复了问题](../assets/fix.svg)以前，在编辑“未登录”组的类别权限时，保存更改将会出错。 此问题已修复。

![修复了问题](../assets/fix.svg)添加了修复程序，以允许商店管理员将产品添加到不在共享目录中的订单。 以前，添加不在目录中的项目时会显示错误消息。

![修复了问题](../assets/fix.svg)以前，在运行命令`php bin/magento indexer:set-dimensions-mode catalog_product_price website`并尝试创建共享目录后，会发生错误。 此问题已修复。

![修复了问题](../assets/fix.svg)在添加公司并将公司管理员分配给非默认网站时，发送了错误的网站ID，从而导致出现错误。 此问题已修复。

![已修复问题](../assets/fix.svg)以前，在将客户移至另一个客户组后，使用&#x200B;_快速订单_&#x200B;将产品添加到订单会失败，并出现错误。 此问题已修复。

![修复了问题](../assets/fix.svg)以前，当尝试使用带有B2B引号的WebAPI签出时，向API发送了错误的值，从而导致发生错误。 此问题已修复。

![已修复问题](../assets/fix.svg)以前，通过API将公司设置为“活动”时，会发生错误。 此问题现已修复。

![已修复问题](../assets/fix.svg)由于不需要的`form`标记，在更改建议的运费后按Enter键时，订单页面会自动刷新。 此问题已修复。

![修复了问题](../assets/fix.svg)以前，在目录页面上设置产品显示限制并且该限制小于产品总数时，出现错误。 此功能现在可按预期工作。

![已修复问题](../assets/fix.svg)以前，在更改公司的管理员时，原始管理员地址将会复制到新管理员，并为他们提供两个地址。 现在，仅添加正确的地址。

![修复了问题](../assets/fix.svg)以前，在git设置为“允许并通知客户”时，使用API保存报价项会失败。 此API调用现在可按预期运行。

![已修复问题](../assets/fix.svg)已修复的产品税现在显示在“报价详细信息”页面上。

![修复了问题](../assets/fix.svg)以前，单击“我的报价”页面的“评论”选项卡中的附件将无法下载该文件。 此行为现在可按预期运行。

### 已知问题

- 在多网站部署中，Adobe Commerce在升级到B2B 1.2.0期间引发异常。 当`setup:upgrade`运行时，`PurchaseOrder`模块上出现此错误： `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`。 **解决方法**：将`B2B-716 Add NonTransactionableInterface`接口安装到`InitPurchaseOrderSalesSequence`数据修补程序修补程序，该修补程序现在可从`magento.com`的&#x200B;**我的帐户** > **下载**&#x200B;部分获得。
- 如果折扣代码在采购订单(PO)获得批准之前过期，则PO将继续显示折扣金额，但是一旦PO获得批准，订单就会按非折扣总额订购。 **解决方法**：安装此问题的`B2B-709 Purchase Order Discount patch`修补程序，该修补程序现在可从`magento.com`的&#x200B;**我的帐户** > **下载**&#x200B;部分获得。
- 如果采购订单中的物料缺货，或者在采购订单转换为实际订单时数量不足，则会发生错误。 如果启用了延交订单，则会正常处理订单。
