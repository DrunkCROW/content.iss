---
title: 关于 CI 系统中的 CodeQL 代码扫描
shortTitle: CI 中的代码扫描
intro: '您可以在第三方持续集成 系统中用 {% data variables.product.prodname_codeql %} 分析您的代码，并将结果上传到 {% data variables.product.product_location %}。 由此产生的 {% data variables.product.prodname_code_scanning %} 警报与 {% data variables.product.product_name %} 内生成的任何警报一起显示。'
product: '{% data reusables.gated-features.code-scanning %}'
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Advanced Security
  - Code scanning
  - CodeQL
  - Repositories
  - Pull requests
  - Integration
  - CI
  - SARIF
redirect_from:
  - /code-security/secure-coding/about-codeql-code-scanning-in-your-ci-system
  - /code-security/secure-coding/using-codeql-code-scanning-with-your-existing-ci-system/about-codeql-code-scanning-in-your-ci-system
---

<!--UI-LINK: When GitHub Enterprise Server 3.1+ doesn't have GitHub Actions set up, the Security > Code scanning alerts view links to this article.-->

{% data reusables.code-scanning.beta %}
{% data reusables.code-scanning.enterprise-enable-code-scanning %}

## 关于 CI 系统中的 {% data variables.product.prodname_codeql %} {% data variables.product.prodname_code_scanning %}

{% data reusables.code-scanning.about-code-scanning %} For information, see "[About {% data variables.product.prodname_code_scanning %} with {% data variables.product.prodname_codeql %}](/code-security/secure-coding/automatically-scanning-your-code-for-vulnerabilities-and-errors/about-code-scanning-with-codeql)."

{% data reusables.code-scanning.codeql-context-for-actions-and-third-party-tools %}

{% ifversion fpt or ghes > 3.1 or ghae or ghec %}
<!--Content for GitHub.com, GHAE next, and GHES 3.2 and onward. CodeQL CLI is the preferred method, and CodeQL runner is deprecated. -->

{% data reusables.code-scanning.codeql-cli-context-for-third-party-tools %}

{% data reusables.code-scanning.upload-sarif-ghas %}

## 关于 {% data variables.product.prodname_codeql_cli %}

{% data reusables.code-scanning.what-is-codeql-cli %}

使用 {% data variables.product.prodname_codeql_cli %} 分析：

- 动态语言，例如 JavaScript 和 Python。
- 编译的语言，例如 C/C++、C# 和 Java。
- 以多种语言编写的代码库。

更多信息请参阅“[在 CI 系统中安装 {% data variables.product.prodname_codeql_cli %}](/code-security/secure-coding/using-codeql-code-scanning-with-your-existing-ci-system/installing-codeql-cli-in-your-ci-system)”。

{% data reusables.code-scanning.licensing-note %}

{% ifversion ghes = 3.2 %}
<!-- Content for GHES 3.2 only. CodeQL CLI 2.6.2, which introduces full feature parity between CodeQL CLI and CodeQL runner, is officially recommended for GHES 3.0+ -->

Since version 2.6.3, the {% data variables.product.prodname_codeql_cli %} has had full feature parity with the {% data variables.product.prodname_codeql_runner %}.

{% data reusables.code-scanning.deprecation-codeql-runner %}

{% endif %}

{% endif %}

<!--Content for GHES 3.1 only. Both CodeQL CLI and CodeQL runner are available -->
{% ifversion ghes < 3.2 %}
将 {% data variables.product.prodname_codeql_cli %} 或 {% data variables.product.prodname_codeql_runner %} 添加到第三方系统，然后调用工具分析代码并将 SARIF 结果上传到 {% data variables.product.product_name %}。 由此产生的 {% data variables.product.prodname_code_scanning %} 警报与 {% data variables.product.product_name %} 内生成的任何警报一起显示。

[{% data variables.product.prodname_codeql_cli %}](https://github.com/github/codeql-cli-binaries/releases) version 2.6.3 is available now for {% data variables.product.prodname_ghe_server %} 3.0 and later versions. For more information on migrating to the {% data variables.product.prodname_codeql_cli %}, see "[Migrating from the CodeQL runner to CodeQL CLI](/code-security/code-scanning/using-codeql-code-scanning-with-your-existing-ci-system/migrating-from-the-codeql-runner-to-codeql-cli)."

{% data reusables.code-scanning.upload-sarif-ghas %}

## 比较 {% data variables.product.prodname_codeql_cli %}与 {% data variables.product.prodname_codeql_runner %}

{% data reusables.code-scanning.what-is-codeql-cli %}

The {% data variables.product.prodname_codeql_runner %} is a deprecated command-line tool that uses the {% data variables.product.prodname_codeql_cli %} to analyze code and upload the results to {% data variables.product.product_name %}. 该工具使用操作在 {% data variables.product.product_name %} 内本地模拟分析运行。

{% data variables.product.prodname_codeql_cli %} 2.6.3 is a complete replacement for the runner with full feature parity. Generally, it is better to use the {% data variables.product.prodname_codeql_cli %} directly.

更多信息请参阅“[在 CI 系统中安装 {% data variables.product.prodname_codeql_cli %}](/code-security/secure-coding/using-codeql-code-scanning-with-your-existing-ci-system/installing-codeql-cli-in-your-ci-system)”。

{% data reusables.code-scanning.deprecation-codeql-runner %}

有关 {% data variables.product.prodname_codeql_runner %} 的更多信息，请参阅“[在 CI 系统中运行 {% data variables.product.prodname_codeql_runner %}](/code-security/secure-coding/running-codeql-runner-in-your-ci-system)”。

{% endif %}
