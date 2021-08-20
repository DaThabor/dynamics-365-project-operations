---
title: Sign up for Project Operations trials
description: This topic provides information about how to deploy a trial of Dynamics 365 Project Operations.
author: ruhercul
ms.date: 08/19/2021
ms.topic: article
ms.reviewer: kfend 
ms.author: ruhercul
---

# Sign up for Project Operations trials 

_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing, Project Operations for stocked/production-based scenarios_ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

This topic explains how to subscribe to the preview partner offer and deploy a Dynamics 365 Project Operations environment.

With the new Project Operations trial, you can automatically deploy any of the three supported deployment scenarios by completing a questionnaire that recommends the best deployment approach. This topic provides information about how to:

- Redeem your trial offer.
- Initiate provisioning.
- Configure dual-write.
- Learn more about Project Operations. 

The following table outlines the details of the new trial offer.

| **Offer item**               | **Details**                                  |
|------------------------------|----------------------------------------------|
| Offer type                   | This offer type is Admin lead so a tenant admin is required in order to redeem. |
| Offer use                    | One time per tenant                          |
| Offer duration               | 30 calendar days                             |
| Redemptions per tenant       | 1                                            |
| Number of users              | 25                                           |
| Extension                    | 1 extension, 30 calendars days               |
| Number of trial environments | 3                                            |


## Admin trial details
The following table lists the trial details and how they apply to each deployment type.

| **Item**                      | **Lite**                                     | **Non-stocked materials** | **Stocked materials** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Setup data provided           | Yes                                          | Yes                       | Yes (USSI)            |
| Transactional data            | No                                           | No                        | No                    |
| Provisioning time in minutes  | 15                                           | 90                        | 30                    |
 
## Prerequisites
The following prerequisites are required to deploy a trial of Dynamics 365 Project Operations.

- Sign-up for the [Dynamics 365 Project Operations - Preview Trial](https://www.aka.ms/try-po).
- The user who deploys the preview must have Azure tenant global administrator rights.

> [!IMPORTANT]
> Only one person in an organization, the tenant administrator, needs to perform this task. If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.

### Dynamics 365 Project Operations - Preview trial 

Before you begin, sign in to a browser with the user work account in the tenant where you want the Project Operations preview.

1. Redeem the first offer code, **Dynamics 365 Project Operations - Preview Trial** by pasting it into the browser URL.

    ![Redeem Offer](./media/16RedeemFirstOfferNew.png)

2. Confirm your order.

    ![Confirm the order](./media/17ConfirmOrderNew.png)

  You will see that the confirmation offer was successfully redeemed.

   ![Confirmation](./media/18OrderConfirmationNew.png)

  You will be redirected to the [Power Platform admin center](https://admin.powerplatform.com/projectoperationstrial).

## Questionnaire and provisioning

1.	Go to the [Power Platform admin center](https://admin.powerplatform.com/projectoperationstrial) and complete the questionnaire.  
2.	Review the recommended deployment type, and select **Begin Setup** to initiate provisioning.
3.	Review the terms and conditions and then select **Start**.

   After provisioning starts, you are redirected to the environment list in the Power Platform admin center. While provisioning is in progress, the state of your environment is **PreparingInstance**.
 
  After the provisioning is complete, the state of your environment is **Ready**.
 
4.	When the provisioning is complete, select the respective Microsoft Dataverse URL, and the Finance and Operations apps URLs to validate the deployment.

## Demo data installation

Use the following links to access demo data packages for both non-stocked materials and lite deployment scenarios. 
- [Non-stocked materials demo data](resource-apply-pro-setup-config-data.md)
- [Lite demo data](lite-apply-demo-setup-config-data.md)

## Configuring dual-write
For non-stocked materials deployments only, configure your dual-write mappings. For more information, see [Project Operations dual-write map versions](resource-dual-write-maps.md).

## Assign licenses

You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.

1. Go to the [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.

   ![Admin center home page](./media/14AdminPortal.png)

2. On the **Active users** page, select the users that you want to assign a license to.

   ![Assign Licenses](./media/15AssignLicenses.png)

3. Verify that the **Dynamics 365 Project Operations Preview**  license has been selected, and then select **Save changes**.

## Additional resources

The following resources provide helpful guidance as you begin your journey with Project Operations:

- [Video Series -Project Operations Overview, feature deep dives and roadmap](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Determine your deployment type](determine-deployment-type.md)

## Frequently asked questions

### What if I require ALM or ELM for my Finance and Operations apps environment?

- For partners who require full environment lifecycle management capabilities, see the [Partner Sandbox License Request](https://experience.dynamics.com/requestlicense) to review the new partner offer. 
- For partners seeking more information about Internal Use Rights, see [Internal Use Rights cloud and software benefit (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### Can I extend my trial beyond 30 days?
To extend your trial, complete the following steps.

1. In the **Microsoft 365 Admin Center**, go to **Billing** > **Your products**.
2. Select **Dynamics 365 Project Operations (CE) - Preview Trial**.
3. Under **Expiration Date**, select **Extend Date**.

### Can I upgrade from the lite deployment to the resource/non-stocked based scenario deployment?
Currently, there is no support to upgrade an environment from a lite to a non-stocked based deployment.

### Can I access Lifecycle Services (LCS) for my Finance environments?  
No. For these trials, deployment is handled through the Power Platform Admin Center. Access to the Finance environment is restricted.

### Can I install my trial on an existing environment?
If you have an existing environment, you will be allowed to install the lite deployment on an existing sales Dataverse environment from the Power Platform Admin center.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
