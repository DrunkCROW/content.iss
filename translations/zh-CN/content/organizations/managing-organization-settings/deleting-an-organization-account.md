---
title: 删除组织帐户
intro: '删除组织时，所有仓库、私有仓库复刻、wiki、议题、拉取请求和项目或组织页面也被删除。 {% ifversion fpt or ghec %}您的结算将结束，90 天后，组织名称将可用于新的用户或组织帐户。{% endif %}'
redirect_from:
  - /articles/deleting-an-organization-account
  - /github/setting-up-and-managing-organizations-and-teams/deleting-an-organization-account
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: 删除组织帐户
---

{% ifversion fpt or ghec %}
{% tip %}

**提示**：如果要取消已付费的订阅，可以[将组织下载到 {% data variables.product.prodname_free_team %}](/articles/downgrading-your-github-subscription) 而非删除组织及其内容。

{% endtip %}

{% endif %}

## 1. 备份组织内容

删除组织后，GitHub **无法恢复内容**。 因此，在删除组织之前，请确保您拥有该帐户中所有仓库、wiki、议题和项目板的副本。

## 2. 删除组织

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
4. 在组织设置页面底部附近，单击 **Delete this Organization（删除此组织）**。 ![删除此组织按钮](/assets/images/help/settings/settings-organization-delete.png)
