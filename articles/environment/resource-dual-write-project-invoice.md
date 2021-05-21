---
title: Project invoice integration
description: This topic provides information about Project Operations dual-write integration for customer invoicing.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod:
ms.reviewer: kfend 
ms.author: sigitac
---

# Project invoice integration

This topic provides information about Project Operations dual-write integration for customer invoicing.

In Project Operations, the Project manager manages the project billing backlog and creates a proforma invoice for the customer in Microsoft Dataverse. Based on this proforma invoice, the Accounts receivable clerk or Project accountant creates a customer-facing invoice. Dual-write integration ensures that the proforma invoice details are synchronized to Finance and Operations apps. After the customer-facing invoice is posted, the system updates the relevant project actuals in Dataverse with the accounting detail. The following graphic provides a high-level conceptual overview of this integration.

   ![Project invoice integration](./media/DW5Invoicing.png)

After the Project manager confirms the proforma invoice in Dataverse, the proforma invoice header information synchronizes to Finance and Operations apps using the dual-write table map, **Project invoice proposal V2 (invoices)**. This is a one-way integration from Dataverse to Finance and Operations apps. Creating or deleting Project invoice proposals directly in Finance and Operations apps isn't supported.

Invoice confirmation in Dataverse also triggers the business logic to create billing-related records in the **Actuals** entity. These records are synchronized to Finance and Operations using the dual-write table map, **Project Operations integration actuals (msdyn\_actuals).** For more information, see [Project estimates and actuals](resource-dual-write-estimates-actuals.md). 

Project invoice proposal lines are created by the periodic process, **Import form staging**. This process is based on the billed sales actuals details in the **Actuals staging** table. For more information, see [Manage project invoice proposals](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 