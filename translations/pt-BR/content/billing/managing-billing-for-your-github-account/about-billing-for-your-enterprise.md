---
title: Sobre a cobrança para a sua empresa
intro: 'You can view billing information for your enterprise{% ifversion ghec or ghes %} account on {% data variables.product.prodname_dotcom_the_website %}{% endif %}.'
redirect_from:
  - /admin/overview/managing-billing-for-your-enterprise
  - /enterprise/admin/installation/managing-billing-for-github-enterprise
  - /enterprise/admin/overview/managing-billing-for-github-enterprise
  - /admin/overview/managing-billing-for-github-enterprise
versions:
  ghec: '*'
  ghes: '*'
  ghae: '*'
type: overview
topics:
  - Enterprise
shortTitle: Cobrança para sua empresa
---

## Sobre a cobrança para a sua empresa

{% ifversion ghae %}

{% data reusables.github-ae.about-billing %} Uma vez por dia, {% data variables.product.prodname_dotcom %} contará o número de usuários com uma licença para sua empresa. {% data variables.product.company_short %} efetua a cobrança para cada usuário licenciado independentemente de o usuário estar conectado a {% data variables.product.prodname_ghe_managed %} nesse dia.

Para regiões comerciais, o preço por usuário por dia é de $ 1,2580645161. Por meses de 31 dias, o custo mensal para cada usuário é de $ 39. Nos meses com menos dias, o custo mensal é menor. Cada mês de cobrança começa em um horário fixo no primeiro dia do mês do calendário.

Se você adicionar um usuário licenciado no meio do mês, esse usuário será incluído apenas na contagem dos dias em que tem uma licença. Ao remover um usuário licenciado, esse usuário permanecerá na contagem até o final desse mês. Portanto, se você adicionar um usuário durante o mês ou depois remover o usuário no mesmo mês, o usuário será incluído na contagem a partir do dia em que o usuário foi adicionado até o final do mês. Não há custos adicionais se você adicionar novamente um usuário no mesmo mês em que o usuário foi removido.

Por exemplo, aqui estão os custos para os usuários com licenças em datas diferentes.

| Usuário   | Datas de licença                                                   | Dias contados | Custo   |
| --------- | ------------------------------------------------------------------ | ------------- | ------- |
| @octocat  | 1 de Janeiro - 31 de Janeiro                                       | 31            | $ 39    |
| @robocat  | 1 de fevereiro - 28 de fevereiro                                   | 28            | $ 35,23 |
| @devtocat | 15 de Janeiro - 31 de Janeiro                                      | 17            | $ 21,39 |
| @doctocat | 1 de Janeiro - 15 de Janeiro                                       | 31            | $ 39    |
| @prodocat | 7 de Janeiro - 15 de Janeiro                                       | 25            | $ 31,45 |
| @monalisa | 1 de janeiro - 7 de janeiro<br>15 de janeiro - 31 de janeiro | 31            | $ 39    |

{% data variables.product.prodname_ghe_managed %} tem uma instância mínima de 500 usuários. {% data variables.product.company_short %} cobra de você um mínimo de 500 usuários por instância, mesmo que haja menos de 500 usuários com uma licença nesse dia.

Você pode ver seu uso atual no seu [Portal da conta do Azure](https://portal.azure.com).

{% elsif ghec or ghes %}

{% ifversion ghec %}

{% data variables.product.company_short %} faz a cobrança mensal para o número total de membros da sua conta corporativa, bem como quaisquer serviços adicionais que você usar com {% data variables.product.prodname_ghe_cloud %}.

{% elsif ghes %}

Cada usuário em {% data variables.product.product_location %} consome uma estação na sua licença. {% data variables.product.company_short %} faz a cobrança mensal no número total de estações consumidas na sua licença.

{% endif %}

{% data reusables.billing.about-invoices-for-enterprises %} For more information about {% ifversion ghes %}licensing, usage, and invoices{% elsif ghec %}usage and invoices{% endif %}, see the following{% ifversion ghes %} in the {% data variables.product.prodname_ghe_cloud %} documentation.{% else %}.{% endif %}

{%- ifversion ghes %}
- "[Sobre preços por usuário](/enterprise-cloud@latest/billing/managing-billing-for-your-github-account/about-per-user-pricing)"
{%- endif %}
- "[Viewing the subscription and usage for your enterprise account]({% ifversion ghes %}/enterprise-cloud@latest{% endif %}/billing/managing-billing-for-your-github-account/viewing-the-subscription-and-usage-for-your-enterprise-account)"
- "[Managing invoices for your enterprise]({% ifversion ghes %}/enterprise-cloud@latest{% endif %}/billing/managing-billing-for-your-github-account/managing-invoices-for-your-enterprise)"

Os administradores da conta corporativa em {% data variables.product.prodname_dotcom_the_website %} podem acessar e gerenciar a cobrança da empresa. For more information, see "[Roles in an enterprise]({% ifversion ghes %}/enterprise-cloud@latest{% endif %}/admin/user-management/managing-users-in-your-enterprise/roles-in-an-enterprise){% ifversion ghec %}."{% elsif ghes %}" in the {% data variables.product.prodname_ghe_cloud %} documentation.{% endif %}

{% ifversion ghec %}

{% data reusables.enterprise-accounts.billing-microsoft-ea-overview %} Para obter mais informações, consulte "[Conectando uma assinatura do Azure à sua empresa](/billing/managing-billing-for-your-github-account/connecting-an-azure-subscription-to-your-enterprise)".

{% endif %}

{% ifversion ghes %}

{% data reusables.billing.ghes-with-no-enterprise-account %}

{% endif %}

{% ifversion ghec %}

## Per-user pricing

{% data variables.product.company_short %} bills for services consumed on {% data variables.product.prodname_dotcom_the_website %}, each user for deployments of {% data variables.product.prodname_ghe_server %}, and each member of organizations on {% data variables.product.prodname_ghe_cloud %}. For more information about per-user pricing, see "[About per-user pricing](/billing/managing-billing-for-your-github-account/about-per-user-pricing)."

{% data reusables.billing.per-user-pricing-reference %}

For more information about roles, see "[Roles in an enterprise](/admin/user-management/managing-users-in-your-enterprise/roles-in-an-enterprise)" or "[Roles in an organization](/organizations/managing-peoples-access-to-your-organization-with-roles/roles-in-an-organization)."

For more information about outside collaborators, see "[Adding outside collaborators to repositories in your organization](/organizations/managing-access-to-your-organizations-repositories/adding-outside-collaborators-to-repositories-in-your-organization)."

{% endif %}

## Sobre a sincronização do uso da licença

{% data reusables.enterprise.about-deployment-methods %}

{% data reusables.enterprise-licensing.about-license-sync %} Para mais informações, consulte {% ifversion ghec %}"[Sincronizando o uso da licença entre {% data variables.product.prodname_ghe_server %} e {% data variables.product.prodname_ghe_cloud %}](/enterprise-server/billing/managing-your-license-for-github-enterprise/syncing-license-usage-between-github-enterprise-server-and-github-enterprise-cloud)" na documentação de {% data variables.product.prodname_ghe_server %}.{% elsif ghes %}"[Sincronizando o uso da licença entre {% data variables.product.prodname_ghe_server %} e {% data variables.product.prodname_ghe_cloud %}](/billing/managing-your-license-for-github-enterprise/syncing-license-usage-between-github-enterprise-server-and-github-enterprise-cloud)."{% endif %}

{% endif %}

## Leia mais

- "[Sobre as contas corporativas](/admin/overview/about-enterprise-accounts)"{% ifversion ghec or ghes %}
- "[Sobre licenças para o GitHub Enterprise](/billing/managing-your-license-for-github-enterprise/about-licenses-for-github-enterprise)"{% endif %}
