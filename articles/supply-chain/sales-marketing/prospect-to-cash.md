---
title: Prospect to cash
description: "Þetta efnisatriði veitir yfirlit yfir Prospect to cash milli Dynamics 365 for Finance and Operations, Enterprise Edition og Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="1311e-103">Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="1311e-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1311e-104">Prospect to cash lausnin notar [Gagnasamþættingu](/common-data-service/entity-reference/dynamics-365-integration) til að samstilla gögn milli Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og Dynamics 365 for Sales tilvik með Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="1311e-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="1311e-105">Prospect to cash sniðmát í boði með gagnasamþættingu leyfir flæði milli reikninga, tengiliða, vara, sölutilboða, sölupantana og sölureikningagagna milli Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="1311e-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="1311e-106">Þegar gögnin flæði á milli Finance and Operations og Sales er hægt að framkvæma sölu- og markaðsstarf í Sales og meðhöndla pöntunina í birgðastjórnun í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1311e-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="1311e-107">Þessi lausn veitir samþættingu á eftirfarandi sviðum:</span><span class="sxs-lookup"><span data-stu-id="1311e-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="1311e-108">Viðhalda reikningum í Sales og samstilla þá við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1311e-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="1311e-109">Viðhalda tengiliðum í Sales og samstilla þá við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1311e-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="1311e-110">Viðhalda vörum í Finance and Operations og samstilla þær við Sales</span><span class="sxs-lookup"><span data-stu-id="1311e-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="1311e-111">Búa til sölutilboð í Sales og samstilla þau við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1311e-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="1311e-112">Búa til sölupantanir í Finance and Operations og samstilla þær við Sales</span><span class="sxs-lookup"><span data-stu-id="1311e-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="1311e-113">Búa til sölureikninga í Finance and Operations og samstilla þá við Sales</span><span class="sxs-lookup"><span data-stu-id="1311e-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="1311e-114">Kerfiskröfur fyrir Dynamics 365 for Finance and Operations, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="1311e-114">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="1311e-115">Eftirfarandi verður að setja upp áður en Prospect to cash er notað:</span><span class="sxs-lookup"><span data-stu-id="1311e-115">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="1311e-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (July 2017) með verkvangsuppfærslu 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="1311e-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="1311e-117">Tvær bráðabætur fyrir Dynamics 365 for Finance and Operations, Enterprise Edition (júlí 2017).</span><span class="sxs-lookup"><span data-stu-id="1311e-117">Two hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>

    -  <span data-ttu-id="1311e-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - Þessi bráðabót gerir samstillingu sölupöntunarlína við gagnasamþættingarkost mögulegan frá Finance and Operations við Sales.</span><span class="sxs-lookup"><span data-stu-id="1311e-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="1311e-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)- Þessi bráðabót gerir samstillingu sölupantana við gagnasamþættingarkost mögulegan frá Finance and Operations við Sales.</span><span class="sxs-lookup"><span data-stu-id="1311e-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
    
<span data-ttu-id="1311e-120">**Athugaðu**: Þú þarft aðeins að setja upp KB4036524 vegna þess að uppsetningin inniheldur breytingar frá KB4036461.</span><span class="sxs-lookup"><span data-stu-id="1311e-120">**Note**: You only need to install KB4036524 because the installation includes the changes from KB4036461.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="1311e-121">Kerfiskröfur fyrir Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="1311e-121">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="1311e-122">Eftirfarandi verður að setja upp áður en Prospect to cash er notað:</span><span class="sxs-lookup"><span data-stu-id="1311e-122">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="1311e-123">Dynamics 365 for Sales útgáfa 1612 (8.2.1.207) (DB 8.2.1.207) á netinu eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="1311e-123">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or later.</span></span>
- <span data-ttu-id="1311e-124">Prospect to cash lausn fyrir Dynamics 365 for Sales, útgáfa 1.14.0.0 (v14) eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="1311e-124">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="1311e-125">Settu upp Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="1311e-125">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="1311e-126">Sæktu [Prospect to cash fyrir Dynamics 365 for Sales solution package zip-skrá](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) á CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="1311e-126">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="1311e-127">Gakktu úr skugga um að zip-skráin sé ólæst þannig að þú fáir ekki villuskilaboðin „Engir innflutningspakkar fundust“ þegar þú setur upp pakkann.</span><span class="sxs-lookup"><span data-stu-id="1311e-127">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="1311e-128">Til að opna skrána skaltu gerirðu eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="1311e-128">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="1311e-129">Hægrismelltu á zip-skrána.</span><span class="sxs-lookup"><span data-stu-id="1311e-129">Right-click the zip file.</span></span>
    -  <span data-ttu-id="1311e-130">Veldu **Eiginleikar** og Svo **Opna**.</span><span class="sxs-lookup"><span data-stu-id="1311e-130">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="1311e-131">Opnaðu hana og keyrðu PackageDeployer.exe.</span><span class="sxs-lookup"><span data-stu-id="1311e-131">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="1311e-132">Settu upp Prospect í Cash lausn í Sales tilvikið þitt.</span><span class="sxs-lookup"><span data-stu-id="1311e-132">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="1311e-133">Veldu **Office 365** Deployment.</span><span class="sxs-lookup"><span data-stu-id="1311e-133">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="1311e-134">Veldu **Sýna ítarlegt**.</span><span class="sxs-lookup"><span data-stu-id="1311e-134">Select **Show advanced**.</span></span>
    - <span data-ttu-id="1311e-135">Veldu **Svæði** fyrir skjóta uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="1311e-135">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="1311e-136">Ef þú velur **Veit ekki** leitar kerfið að öllum svæðum og uppsetning tekur lengri tíma.</span><span class="sxs-lookup"><span data-stu-id="1311e-136">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="1311e-137">Sláðu inn **Notandanafn** og **Aðgangsorð** kerfisnotanda sem hefur leyfi til að setja upp.</span><span class="sxs-lookup"><span data-stu-id="1311e-137">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

