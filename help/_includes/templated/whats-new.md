---
source-git-commit: 78d6e7fa263246e8fa52aa0386b35e4bb39553ad
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 2%

---
# 新增功能模板

## 新增功能

本部分包含过去60天中所做的更改。 我们将从此列表中排除所有次要更新，例如副本编辑。

### 2026年2月10日

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>描述</th>
      <th>类型</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>更新了Adobe Commerce as a Cloud Service 2月版的管理文档：<br /> — 在REST API中创建发票时添加了<a href="https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/stores-sales/order-management/invoices#custom-capture-amounts">自定义捕获金额</a>的文档，该文档允许商家在为部分捕获和特殊付款方案创建发票时捕获自定义金额。<br /> — 指示<a href="https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/start/reporting/reports-menu">报告菜单</a>中的哪些报告现在只是PaaS。</p>
</td>
      <td>
        重大更新
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/0c602db5a7291b95d725bce59df53923490d6b96">提交</a></td>
    </tr>
  </tbody>
</table>

### 2026年2月2

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>描述</th>
      <th>类型</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>更新了<a href="https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/start/compliance/privacy/compliance-cookie-law">Cookie法律合规性</a>以添加缺少的<code class="language-plaintext highlighter-rouge">mage-cache-timeout</code>个localStorage密钥并将免除Cookie列表转换为表格式。</p>
</td>
      <td>
        技术，反馈
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/ebb6348c6b5a30f5de4025f39bae0061b397a4b9">提交</a></td>
    </tr>
    <tr>
      <td><p>[!BADGE PaaS only]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce。"}更新了为Adobe Commerce配置IMS集成的先决条件，以提供关于请求Adobe Admin Console访问权限的信息。</p>
</td>
      <td>
        技术，反馈
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/8ea546c5e1cc9296c8b056ea7e25984a66d43851">提交</a></td>
    </tr>
  </tbody>
</table>

### 2026年1月31日

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>描述</th>
      <th>类型</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>更新了“客户管理指南”中的<a href="https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/customers/customer-groups">客户组</a>，以阐明在将客户分配给公司之后，管理员用户无法编辑客户的客户组。</p>
</td>
      <td>
        技术
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.zh-Hans/pull/81">拉取请求</a></td>
    </tr>
  </tbody>
</table>

### 2026年1月20日

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>描述</th>
      <th>类型</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>已将产品引用从“Adobe Sensei”更改为“Adobe AI”，以反映Adobe品牌更新。</p>
</td>
      <td>
        反馈
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/4077b922dae0ed9a9050a5f6160143a636646daa">提交</a></td>
    </tr>
  </tbody>
</table>

### 2026年1月16日

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>描述</th>
      <th>类型</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>添加了<a href="https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/config/sales/sales-emails#order-ready-for-pickup-in-store">订单准备就绪以在商店中提货</a>电子邮件可用时的说明。</p>
</td>
      <td>
        反馈
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/65fd67dcd3c14daddfc0f36493dc6da3630898a1">提交</a></td>
    </tr>
  </tbody>
</table>

### 2026年1月15日

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>描述</th>
      <th>类型</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>向Adobe Commerce as a Cloud Service添加了以下功能：<br /> — 添加了对<a href="https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/systems/security/captcha/security-google-recaptcha-enterprise">Google reCAPTCHA Enterprise</a>的支持，该产品通过自适应风险分析和机器学习功能提供高级机器人保护。<br /> — 通过<a href="https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/stores-sales/delivery/shipping-settings#shipment-tracking-urls">启用自定义跟踪URL</a>，将购物者电子邮件中包含的装运跟踪编号从纯文本转换为可点击链接。 USPS、UPS、FedEx和DHL支持此功能。<br /> — 您现在可以使用<a href="https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/catalog/products/pricing/product-price-tier#enable-tier-pricing-for-catalog-price-rules">目录价格规则</a>将分层定价折扣与目录规则折扣相结合。 此增强功能允许您创建更具活力和竞争力的定价策略。</p>
</td>
      <td>
        重大更新，新主题
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/70e73b47c4b0342ade3deab64dbe39f29b82191f">提交</a></td>
    </tr>
  </tbody>
</table>

### 2025年12月17日

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>描述</th>
      <th>类型</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>更新了<a href="https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty">奖励和忠诚度主题</a>，以阐明当客户在结账期间使用奖励积分或商店积分时如何计算税额。</p>
</td>
      <td>
        反馈
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/1154cd5ced746ac6dfd609946528f281774bbaaa">提交</a></td>
    </tr>
  </tbody>
</table>
