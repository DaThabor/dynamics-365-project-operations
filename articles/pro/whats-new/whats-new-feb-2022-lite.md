---
title: What's new February 2022 - Project Operations lite deployment
description: This topic provides information about the quality updates that are available in the February 2022 release of Project Operations lite deployment.
author: sigitac
ms.date: 01/24/2021
ms.topic: article
ms.prod:
ms.reviewer: kfend 
ms.author: sigitac
---

# What's new February 2022 - Project Operations lite deployment

_Applies To: Lite deployment - deal to proforma invoicing_

This topic applies to the following components and versions of Microsoft Dynamics 365 Project Operations:

- Project Operations in a Dataverse environment version 4.28.0.120

## Features included in this release

With this release, you can add up to 300 team members to a single project. Previously, the maximum team member limit was 150. For more information, see [Project limits](../project-management/create-wbs.md#project-limitations).


## Quality updates

| **Feature area** | **Reference number** | **Quality update** |
| --- | --- | --- |
| Billing and pricing | 2497369 | Material correction must follow the date value on the **Correction** parameters. |
| Billing and pricing | 2498697 | Improved the security configuration for **Time entry recall**. |
| Billing and pricing | 2517455 | The **Refreshed invoice line transactions** action must not be allowed to trigger multiple times for the same invoice simultaneously. |
| Billing and pricing | 2517465 | The **Deactivate invoice line details** action is blocked because it's not supported. |
| Billing and pricing | 2556660 | Fixed data effectivity checks on the pricelist that's attached to a project parameters record. |
| Opportunity management | 2369202 | Corrected the business logic that verifes pricelists with overlapping effectivity dates can be attached to the same project contract. |
| Opportunity management | 2385965 | Corrected the behavior on the **Project contract** page, on the **Customers** tab, when you select **Save and close**. |
