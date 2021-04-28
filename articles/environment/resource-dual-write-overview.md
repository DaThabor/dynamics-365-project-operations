---
title: Project Operations dual-write integration 
description: This topic provides an overview of Project Operations dual-write integration.
author: sigitac
ms.date: 04/23/2021
ms.topic: article
ms.prod:
ms.service: project-operations
ms.reviewer: kfend 
ms.author: sigitac
---

# Project Operations dual-write integration overview

_**Applies To:** Project Operations for resource/non-stocked based scenarios_

Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.

The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.

![Project Operations data flows overview](./media/ProjectOperationsFlows.jpg)

Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities. Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.

Project Operations in Finance provides project accounting and revenue recognition support. Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more. The Project accountant experiences are mostly based in Finance.

Project Operations integration consists of the following component integration:

- [Setup and configuration data](resource-dual-write-setup-integration.md) 
- Project estimates and actuals
- [Project invoices](resource-dual-write-project-invoice.md)
- [Expense management](resource-dual-write-expense.md)
- Vendor invoices
