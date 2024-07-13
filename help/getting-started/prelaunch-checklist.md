---
title: 启动前检查清单
description: 使用此列表检查所需的配置设置，以确保在商店投入生产之前所有内容都正确。
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# 启动前检查清单

完成商店的设计、开发和测试后，请检查以下配置设置，确保在商店&#x200B;_上线_&#x200B;之前一切正常。 有关每个配置设置的完整说明，请参阅&#x200B;[_配置引用_](../configuration-reference/guide-overview.md)。

## 常规设置

- [商店URL](../stores-purchase/store-urls.md) — 验证商店和管理员的商店URL对于实时生产环境是否正确。
- 安全证书 — 在启动存储之前，请为基本URL中指定的域安装100%签名和受信任的安全证书。
- [存储电子邮件地址](../getting-started/store-details.md#store-email-addresses) — 完成用于发送和接收电子邮件通知的所有电子邮件地址，例如新订单、发票、装运、贷项通知单、产品价格提醒和新闻稿。 确保每个字段都包含有效的企业电子邮件地址。

## 营销设置

- [电子邮件模板](../systems/email-templates.md) — 更新默认电子邮件模板以反映您的品牌。 如果您创建模板，请确保更新配置。
- [销售通信](../stores-purchase/introduction.md#order-management-and-operations) — 确保您的发票和包装单包含正确的业务信息并反映您的品牌。
- [Google Tools](../merchandising-promotions/google-tools.md) - [!DNL Commerce]提供了与Google API的集成，以允许您的企业使用Google Analytics和Google AdWords。

## 销售设置

- [购物车选项](../stores-purchase/cart-configuration.md) — 查看购物车配置设置，查看是否存在要更改的内容，例如设置购物车中价格的最小订单量和存留期。
- [签出选项](../stores-purchase/checkout-process.md#checkout-options) — 查看签出选项，查看是否有要更改的内容，如设置条款和条件以及配置来宾签出。
- [税费](../stores-purchase/taxes.md) — 确保根据您的营业税规则和当地要求正确配置税费。
- [交货方式](../stores-purchase/delivery.md) — 允许公司使用所有承运人和交货方式。
- [PayPal](../stores-purchase/paypal.md) — 如果您计划为客户提供使用PayPal付款的便利，请打开PayPal商家帐户并设置付款方式。 在存储上线之前，以沙盒模式运行一些测试事务。
- [付款方法](../stores-purchase/payments.md) — 启用您计划使用的付款方法，并确保正确配置这些方法。 检查订单状态设置、接受的货币、允许的国家/地区等。

## 系统设置

[Cron（计划任务）](../systems/cron.md) - Cron作业用于处理电子邮件、目录价格规则、新闻稿、客户提醒、Google Sitemap、更新汇率等。 确保将Cron作业设置为以适当的时间间隔（以分钟为单位）运行。
