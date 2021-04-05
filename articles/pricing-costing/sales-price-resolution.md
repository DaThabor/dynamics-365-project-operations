---
title: Resolve sales prices for estimates and actuals
description: This topic provides information about how to resolve sales rates for estimates and actuals.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend 
ms.author: rumant
---

# Resolve sales prices for estimates and actuals

_**Applies To:** Project Operations for resource/non-stocked based scenarios_

When sales prices on estimates and actuals are resolved in Dynamics 365 Project Operations, the system first uses the date and currency of the related project quote or contract to resolve the sales price list. After the sales price list is resolved, the system resolves the sales or bill rate.

## Resolve sales rates on actual and estimate lines for time

In Project Operations, estimate lines for time are used to denote the quote line and contract line details for time and the resource assignments on the project.

After a price list for sales is resolved, the system completes the following steps to default the bill rate.

1. The system uses the **Role**, **Resourcing Company**, and **Resourcing Unit** fields on the estimate line for time, to match against the role price lines in the resolved price list. This matching assumes that out-of-box pricing dimensions for bill rates are being used. If you have configured pricing based on any other fields instead of, or in addition to **Role**, **Resourcing Company**, and **Resourcing Unit**, then that is the combination that will be used to retrieve a matching role price line.
2. If the system finds a role price line that has a bill rate for the **Role**, **Resourcing Company**, and **Resourcing Unit** field combination, then that bill rate is defaulted.
3. If the system is unable to match the **Role**, **Resourcing Company**, and **Resourcing Unit** field values, then it retrieves role price lines with a matching role but null values of **Resource Unit**. After the system finds a matching role price record, it will default the bill rate from that record. This matching assumes an out-of-the-box configuration for the relative priority of **Role** vs **Resourcing Unit** as a sales pricing dimension.

> [!NOTE]
> If you configured a different prioritization of **Role**, **Resourcing Company**, and **Resourcing Unit**, or if you have other dimensions that have higher priority, this behavior will change accordingly. The system retrieves the role price records with matching values of each of the pricing dimension values in the order of priority with rows that have null values for those dimensions coming last.

## Resolve sales rates on actual and estimate lines for expense

In Project Operations, estimate lines for expense are used to denote the quote line and contract line details for expenses and the expense estimate lines on the project.

After a price list for sales is resolved, the system completes the following steps to default the unit sales price.

1. The system uses the **Category** and **Unit** field combination on the estimate line for expense to match against the category price lines in the price list that was resolved.
2. If the system finds a category price line that has a sales rate for the **Category** and **Unit** field combination, then that sales rate is defaulted.
3. If the system finds a matching category price line, the pricing method may be used to default the sales price. The following table below shows the expense price defaulting behavior in Project Operations.

    | Context | Pricing method | Price defaulted |
    | --- | --- | --- |
    | Estimate | Price per unit | Based on the category price line |
    | &nbsp; | At cost | 0.00 |
    | &nbsp; | Markup over cost | 0.00 |
    | Actual | Price per unit | Based on the category price line |
    | &nbsp; | At cost | Based on the related cost actual |
    | &nbsp; | Markup over cost | By applying a markup as defined by the category price line on the unit cost rate of the related cost actual |

4. If the system is unable to match the **Category** and **Unit** field values, the sales rate defaults to zero(0).

## Resolve sales rates on actual and estimate lines for material

In Project Operations, estimate lines for material are used to denote the quote line and contract line details for materials and the material estimate lines on the project.

After a price list for sales is resolved, the system completes the following steps to default the unit sales price.

1. The system uses the **Product** and **Unit** field combination on the estimate line for material to match against the price list item lines in the price list that was resolved.
2. If the system finds a price list item line that has a sales rate for the **Product** and **Unit** field combination, the sales rate is used as the default. If the system finds a matching price list item line when pricing method is not currency amount, the pricing method may be used to default the sales price. 
3. If the **Product** and **Unit** field values aren't a match, the sales rate defaults to zero.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
