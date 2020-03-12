---
title: "Privileged Identity Management - Azure AD"
description: "APIs for Azure AD Privileged Identity Management to manage Azure AD."
localization_priority: Priority
author: "davidmu1"
ms.prod: "microsoft-identity-platform"
doc_type: conceptualPageType
---

# Privileged Identity Management - Azure AD

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

You can use [Azure Active Directory (Azure AD) Privileged Identity Management (PIM)](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-configure) for Azure AD roles to set up just-in-time access workflow for your built-in and custom Azure AD roles (also known as Office365 roles). You can also use it to update role settings, manage role assignments, get information regarding role definitions.

## Common use cases for PIM and Azure resources using a REST API

| Use case | Resource | See also |
| --- | --- | --- |
| List all the built-in and custom roles in your directory. | [governanceRoleDefinition](governanceroledefinition.md) |  |
| Retrieve all role settings for a role or make an update to a role setting. | [governanceRoleSetting](governancerolesetting.md) | [Configure role setting](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-resource-roles-configure-role-settings) |
| List and export all role assignments for a directory role. | [governanceRoleAssignment](governanceroleassignment.md) | [Export role assignments](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/azure-pim-resource-rbac#export-role-assignments-with-children) |
| Create or remove an eligible or active role assignment, activate/deactivate an eligible assignment, view a list of pending requests, approve or deny a pending request or cancel your own pending request. | [governanceRoleAssignmentRequest](governanceroleassignmentrequest.md) | [Role Assignment](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-resource-roles-assign-roles)<br/>[Role activation](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-resource-roles-activate-your-roles)<br/>[Approve requests](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/azure-ad-pim-approval-workflow) |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Service root",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
