---
title: Administrar los límites de gastos para los Codespaces
intro: 'Puedes configurar un límite de gastos para el uso de {% data variables.product.prodname_codespaces %}.'
versions:
  fpt: '*'
  ghec: '*'
type: how_to
product: '{% data reusables.gated-features.codespaces %}'
topics:
  - Codespaces
  - Enterprise
  - Organizations
  - Spending limits
  - User account
  - Billing
shortTitle: Límites de gastos
---

## Acerca de los límites de gastos para {% data variables.product.prodname_codespaces %}

{% data reusables.codespaces.codespaces-spending-limit-requirement %}

Una vez que hayas llegado a tu límite de gastos, tu organización o repositorio ya no podrán crear codespces nuevos y no podrán iniciar los existentes. Cualquier codespace existente que aún se esté ejecutando no se cerrará. Si no cambias el límite de gastos, no se tecobrará por la cantidad que exceda el límite.

Para obtener más información sobre los costos de uso de {% data variables.product.prodname_codespaces %}, consulta la sección "[Acerca de la facturación para {% data variables.product.prodname_codespaces %}](/billing/managing-billing-for-github-codespaces/about-billing-for-codespaces)".

{% ifversion ghec %}
## Utilizar tu suscripción de Azure
Si compraste {% data variables.product.prodname_enterprise %} mediante un Acuerdo de Microsoft Enterprise, puedes conectar tu ID de Suscripción de Azure a tu cuenta empresarial para habilitar y pagar por el uso de {% data variables.product.prodname_codespaces %}. Para obtener más información, consulta la sección "[Conectar una suscripción de Azure a tu empresa](/billing/managing-billing-for-your-github-account/connecting-an-azure-subscription-to-your-enterprise)".
{% endif %}

## Administrar el límite de gastos de {% data variables.product.prodname_codespaces %} para tu organización

Los propietarios de las organizaciones pueden administrar el límite de gastos de {% data variables.product.prodname_codespaces %} para una organización.

{% data reusables.organizations.billing-settings %}
{% data reusables.dotcom_billing.manage-spending-limit %}
{% data reusables.dotcom_billing.monthly-spending-limit-codespaces %}
{% data reusables.dotcom_billing.update-spending-limit %}

## Administrar el límite de gastos de {% data variables.product.prodname_codespaces %} para tu cuenta empresarial

Los propietarios de la empresa y gerentes de facturación pueden administrar el límite de gastos para {% data variables.product.prodname_codespaces %} para una cuenta empresarial.

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.settings-tab %}
{% data reusables.enterprise-accounts.billing-tab %}
1. Sobre "Uso mensual de {% data variables.product.prodname_codespaces %}", haz clic en **Límite de gastos**. ![Pestaña de límite de gastos](/assets/images/help/settings/spending-limit-tab-enterprise.png)
{% data reusables.dotcom_billing.monthly-spending-limit %}
{% data reusables.dotcom_billing.update-spending-limit %}

## Exportar cambios cuando llegaste a tu límite de gastos

{% data reusables.codespaces.exporting-changes %}
## Administrar las notificaciones de uso y límite de gastos

Email notifications are sent to account owners and billing managers when spending reaches 50%, 75%, 90%, and 100% of your account's spending limit.

Puedes inhabilitar estas notificaciones en cualquier momento si navegas al final de la página del **Límite de Gastos**.

![Screenshot of the billing email notification settings](/assets/images/help/billing/codespaces-spending-limit-notifications.png)

## Leer más

- "[Restringir el acceso a los tipos de máquina](/codespaces/managing-codespaces-for-your-organization/restricting-access-to-machine-types)"
- "[Administrar la facturación para los codespaces en tu organización](/codespaces/managing-codespaces-for-your-organization/managing-billing-for-codespaces-in-your-organization)"
