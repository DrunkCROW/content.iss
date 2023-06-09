---
title: 团队
intro: '通过团队 API，您可以在您的 {% data variables.product.product_name %} 组织中创建和管理团队。'
redirect_from:
  - /v3/teams
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - API
miniTocMaxHeadingLevel: 3
---

此 API 仅适用于团队[组织](/rest/reference/orgs)中经过身份验证的成员。 OAuth 访问令牌需要 `read:org` [scope](/apps/building-oauth-apps/understanding-scopes-for-oauth-apps/)。 {% data variables.product.prodname_dotcom %}  从团队 `name` 生成团队的 `slug`。

{% for operation in currentRestOperations %}
  {% unless operation.subcategory %}{% include rest_operation %}{% endunless %}
{% endfor %}

## 讨论

团队讨论 API 允许您获取、创建、编辑和删除团队页面上的讨论帖子。 您可以使用团队讨论进行不特定于存储库或项目的对话。 团队[组织](/rest/reference/orgs)的任何成员都可以创建和阅读公共讨论帖子。 更多信息请参阅“[关于团队讨论](//organizations/collaborating-with-your-team/about-team-discussions/)”。 要详细了解对讨论帖子的评论，请参阅[团队讨论评论 API](/rest/reference/teams#discussion-comments)。 此 API 仅适用于团队组织中经过身份验证的成员。

{% for operation in currentRestOperations %}
  {% if operation.subcategory == 'discussions' %}{% include rest_operation %}{% endif %}
{% endfor %}

## 讨论评论

团队讨论评论 API 允许您在[团队讨论](/rest/reference/teams#discussions)帖子上获取、 创建、编辑和删除讨论评论。 团队[组织](/rest/reference/orgs)的任何成员都可以创建和阅读公共讨论上的评论。 更多信息请参阅“[关于团队讨论](/organizations/collaborating-with-your-team/about-team-discussions/)”。 此 API 仅适用于团队组织中经过身份验证的成员。

{% for operation in currentRestOperations %}
  {% if operation.subcategory == 'discussion-comments' %}{% include rest_operation %}{% endif %}
{% endfor %}

## 成员

此 API 仅适用于团队组织中经过身份验证的成员。 OAuth 访问令牌需要 `read:org` [scope](/apps/building-oauth-apps/understanding-scopes-for-oauth-apps/)。

{% ifversion fpt or ghes or ghec %}
{% note %}

**注：**当您为具有组织身份提供程序 (IdP) 的团队设置了团队同步时，如果尝试使用 API 更改团队的成员身份，则会看到错误。 如果您有权访问 IdP 中的组成员身份，可以通过身份提供程序管理 GitHub 团队成员身份，该提供程序会自动添加和删除组织的成员。 更多信息请参阅“<a href="/organizations/managing-saml-single-sign-on-for-your-organization/managing-team-synchronization-for-your-organization" class="dotcom-only">在身份提供程序与 GitHub 之间同步团队</a>”。

{% endnote %}

{% endif %}

{% for operation in currentRestOperations %}
  {% if operation.subcategory == 'members' %}{% include rest_operation %}{% endif %}
{% endfor %}

{% ifversion ghec or ghae %}
## 外部组

外部组 API 允许您查看可用于组织的外部身份提供程序组，并管理组织中外部组和团队之间的连接。

要使用此 API，经过身份验证的用户必须是团队维护员或与团队关联的组织的所有者。

{% ifversion ghec %}
{% note %}

**注意：**

- 外部组 API 仅适用于属于使用 {% data variables.product.prodname_emus %} 的企业中的组织。 更多信息请参阅“[关于企业管理用户](/admin/authentication/managing-your-enterprise-users-with-your-identity-provider/about-enterprise-managed-users)”。
- 如果您的组织使用团队同步，则可以使用团队同步 API。 更多信息请参阅“[团队同步 API](#team-synchronization)”。

{% endnote %}
{% endif %}

{% for operation in currentRestOperations %}
  {% if operation.subcategory == 'external-groups' %}{% include rest_operation %}{% endif %}
{% endfor %}

{% endif %}

{% ifversion fpt or ghes or ghec %}
## 团队同步

团队同步 API 允许您管理 {% data variables.product.product_name %} 团队与外部身份提供程序 (IdP) 组之间的连接。 要使用此 API，经过身份验证的用户必须是团队维护员或与团队关联的组织的所有者。 用于身份验证的令牌还需要获得授权才能与 IdP (SSO) 提供程序一起使用。 更多信息请参阅“<a href="/github/authenticating-to-github/authorizing-a-personal-access-token-for-use-with-saml-single-sign-on" class="dotcom-only">授权个人访问令牌用于 SAML 单点登录组织</a>”。

您可以通过 IdP 通过团队同步管理 GitHub 团队成员。 必须启用团队同步才能使用团队同步 API。 更多信息请参阅“<a href="/organizations/managing-saml-single-sign-on-for-your-organization/managing-team-synchronization-for-your-organization" class="dotcom-only">在身份提供程序与 GitHub 之间同步团队</a>”。

{% note %}

**注意：** 团队同步 API 不能与 {% data variables.product.prodname_emus %} 一起使用。 要了解有关管理 {% data variables.product.prodname_emu_org %} 的更多信息，请参阅“[外部组 API](/enterprise-cloud@latest/rest/reference/teams#external-groups)”。

{% endnote %}

{% for operation in currentRestOperations %}
  {% if operation.subcategory == 'team-sync' %}{% include rest_operation %}{% endif %}
{% endfor %}

{% endif %}
