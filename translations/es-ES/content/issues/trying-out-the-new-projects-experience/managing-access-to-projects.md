---
title: Managing access to projects (beta)
intro: 'You can control who can view, edit, or manage your projects.'
allowTitleToDifferFromFilename: true
miniTocMaxHeadingLevel: 2
versions:
  fpt: '*'
  ghec: '*'
topics:
  - Projects
  - Organizations
---

{% data reusables.projects.projects-beta %}

## About project access

Admins of organization-level projects can manage access for the entire organization, for teams, for individual organization members, and for outside collaborators.

Admins of user-level projects can invite individual collaborators and manage their access.

Project admins can also control the visibility of their project for everyone on the internet. For more information, see "[Managing the visibility of your projects](/issues/trying-out-the-new-projects-experience/managing-the-visibility-of-your-projects)."

## Managing access for organization-level projects

### Managing access for everyone in your organization

The default base role is `write`, meaning that everyone in the organization can see and edit your project. To change project access for everyone in the organization, you can change the base role. Changes to the base role only affect organization members who are not organization owners and who are not granted individual access.

{% data reusables.projects.project-settings %}
1. Haz Clic en **Administrar el acceso**.
2. Under **Base role**, select the default role.
   - **No access**: Only organization owners and users granted individual access can see the project. Los propietarios de las organizaciones que también son administradores del proyecto.
   - **Read**: Everyone in the organization can see the project. Los propietarios de las organizaciones que también son administradores del proyecto.
   - **Write**: Everyone in the organization can see and edit the project. Los propietarios de las organizaciones que también son administradores del proyecto.
   - **Admin**: Everyone in the organization is an admin for the project.

### Managing access for teams and individual members of your organization

You can also add teams, external collaborators, and individual organization members as collaborators for an organization-level project. Para obtener más información, consulta la sección "[Acerca de los equipos](/organizations/organizing-members-into-teams/about-teams)".

You can only invite an individual user to collaborate on your organization-level project if they are already a member of the organization or an outside collaborator on at least one repository in the organization.

{% data reusables.projects.project-settings %}
1. Haz Clic en **Administrar el acceso**.
2. Under **Invite collaborators**, search for the team or individual user that you want to invite.
3. Selecciona el rola para el colaborador.
   - **Read**: The team or individual can view the project.
   - **Write**: The team or individual can view and edit the project.
   - **Admin**: The team or individual can view, edit, and add new collaborators to the project.
4. Haz clic en **Invitar**.

### Managing access of an existing collaborator on your project

{% data reusables.projects.project-settings %}
1. Haz Clic en **Administrar el acceso**.
1. Debajo de **Administrar acceso**, encuentra al(los) colaborador(es) cuyos permisos quieras modificar.

   You can use the **Type** and **Role** drop-down menus to filter the access list.

1. Edita el rol para el(los) colaborador(es) o haz clic en{% octicon "trash" aria-label="the trash icon" %} para eliminarlo(s).

## Managing access for user-level projects

### Granting a collaborator access to your project

{% note %}

This only affects collaborators for your project, not for repositories in your project. To view an item on the project, someone must have the required permissions for the repository that the item belongs to. Si tu proyecto incluye elementos de un repositorio privado, las personas que no sean colaboradores en el repositorio no podrán ver elementos de este. Para obtener más información, consulta las secciones "[Configurar la visibilidad de un repositorio](/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/setting-repository-visibility)" y "[Administrar los equipos y personas con acceso a tu repositorio](/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/managing-teams-and-people-with-access-to-your-repository)".

{% endnote %}

{% data reusables.projects.project-settings %}
1. Haz Clic en **Administrar el acceso**.
2. Under **Invite collaborators**, search for the user that you want to invite.
3. Selecciona el rola para el colaborador.
   - **Read**: The individual can view the project.
   - **Write**: The individual can view and edit the project.
   - **Admin**: The individual can view, edit, and add new collaborators to the project.
4. Haz clic en **Invitar**.

### Managing access of an existing collaborator on your project

{% data reusables.projects.project-settings %}
1. Haz Clic en **Administrar el acceso**.
1. Debajo de **Administrar acceso**, encuentra al(los) colaborador(es) cuyos permisos quieras modificar.

   You can use the **Role** drop-down menu to filter the access list.

1. Edita el rol para el(los) colaborador(es) o haz clic en{% octicon "trash" aria-label="the trash icon" %} para eliminarlo(s).
