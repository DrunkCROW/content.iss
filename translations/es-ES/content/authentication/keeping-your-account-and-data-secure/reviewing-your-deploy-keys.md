---
title: Revisar tus llaves de implementación
intro: Debes revisar tus llaves de implementación para garantizar que no haya ninguna llave sin autorización (o posiblemente comprometida). También puedes aprobar llaves de implementación existentes que sean válidas.
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
shortTitle: Llaves de implementación
---

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
{% ifversion fpt or ghec or ghes > 3.4 or ghae-issue-5658 %}
3. In the "Security" section of the sidebar, click **{% octicon "key" aria-label="The key icon" %} Deploy keys**.
{% else %}
3. En la barra lateral izquierda, haz clic en **Deploy keys** (Llaves de implementación). ![Parámetro de llaves de implementación](/assets/images/help/settings/settings-sidebar-deploy-keys.png)
{% endif %}
4. En la página de Llaves de implementación, anota las llaves de implementación asociadas a tu cuenta. Para las que no reconozcas o que estén desactualizadas, haz clic en **Delete** (Eliminar). Si hay llaves de implementación válidas que quieres conservar, haz clic en **Approve** (Aprobar). ![Lista de llaves de implementación](/assets/images/help/settings/settings-deploy-key-review.png)

Para obtener más información, consulta la sección "[Administrar las llaves de despliegue](/guides/managing-deploy-keys)".

## Leer más
- [Configurar notificaciones](/account-and-profile/managing-subscriptions-and-notifications-on-github/setting-up-notifications/configuring-notifications#organization-alerts-notification-options)
