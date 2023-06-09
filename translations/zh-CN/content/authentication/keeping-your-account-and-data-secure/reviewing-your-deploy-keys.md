---
title: 审查您的部署密钥
intro: 您应审查部署密钥，以确保没有任何未经授权（或可能已受损）的密钥。 您还可以批准有效的现有部署密钥。
redirect_from:
  - /articles/reviewing-your-deploy-keys
  - /github/authenticating-to-github/reviewing-your-deploy-keys
  - /github/authenticating-to-github/keeping-your-account-and-data-secure/reviewing-your-deploy-keys
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Identity
  - Access management
shortTitle: 部署密钥
---

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
{% ifversion fpt or ghec or ghes > 3.4 or ghae-issue-5658 %}
3. In the "Security" section of the sidebar, click **{% octicon "key" aria-label="The key icon" %} Deploy keys**.
{% else %}
3. 在左侧边栏中，单击 **Deploy keys（部署密钥）**。 ![部署密钥设置](/assets/images/help/settings/settings-sidebar-deploy-keys.png)
{% endif %}
4. 在 Deploy keys（部署密钥）页面中，记下与您的帐户关联的部署密钥。 对于您无法识别或已过期的密钥，请单击 **Delete（删除）**。 如果有您要保留的有效部署密钥，请单击 **Approve（批准）**。 ![部署密钥列表](/assets/images/help/settings/settings-deploy-key-review.png)

更多信息请参阅“[管理部署密钥](/guides/managing-deploy-keys)”。

## 延伸阅读
- [配置通知](/account-and-profile/managing-subscriptions-and-notifications-on-github/setting-up-notifications/configuring-notifications#organization-alerts-notification-options)
