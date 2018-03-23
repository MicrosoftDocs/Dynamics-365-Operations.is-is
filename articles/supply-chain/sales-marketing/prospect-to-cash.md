---
title: Prospect to cash
description: "Þetta efnisatriði veitir yfirlit yfir Prospect to cash lausnarinnar á milli Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 02/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: e342c67f53828c77f77d99a2c3f909a23ced8989
ms.openlocfilehash: 5d9bc41c92258f9856088b04ec5af123c8e915e5
ms.contentlocale: is-is
ms.lasthandoff: 03/13/2018

---

# <a name="prospect-to-cash"></a><span data-ttu-id="ac54e-103">Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="ac54e-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ac54e-104">Prospect to cash lausnin veitir beina samstillingu milli Dynamics 365 for Finance and Operations, Enterprise Edition og Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="ac54e-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, Enterprise edition, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="ac54e-105">Prospect to cash sniðmát sem eru í boði með eiginleika gagnasamþættingar leyfir flæði gagna fyrir reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantanir og sölureikninga milli Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="ac54e-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="ac54e-106">Á meðan gögnin flæði á milli Finance and Operations og Sales er hægt að framkvæma sölu- og markaðsstarf í Sales og meðhöndla pöntunaruppfyllingu með því að nota birgðastjórnun í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac54e-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="ac54e-107">Fyrir frekari upplýsingar um samþættingu Prospect to cash, skoðaðu stutt YouTube myndband:</span><span class="sxs-lookup"><span data-stu-id="ac54e-107">For more information about the Prospect to cash integration, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/AVV9x5x-XCg]

<span data-ttu-id="ac54e-108">Í núverandi útgáfu býður Prospect to cash lausnin upp á eftirfarandi gerðir af beinni samstillingu:</span><span class="sxs-lookup"><span data-stu-id="ac54e-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="ac54e-109">Viðhalda reikningum í Sales og samstilla þá beint úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac54e-109">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="ac54e-110">Vinna með afurðir í Finance and Operations og samstilla þær beint við Sales</span><span class="sxs-lookup"><span data-stu-id="ac54e-110">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="ac54e-111">Vinna með tengiliði í Sales og samstilla þá beint við tengiliði eða viðskiptavini í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac54e-111">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="ac54e-112">Samstilla sölutilboð beint úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac54e-112">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="ac54e-113">Samstilla sölupantanir beint milli Sales og Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac54e-113">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="ac54e-114">Samstilla sölureikninga beint úr Finance and Operations við Sales</span><span class="sxs-lookup"><span data-stu-id="ac54e-114">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="ac54e-115">Kerfisskilyrði fyrir Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac54e-115">System requirements for Finance and Operations</span></span>

<span data-ttu-id="ac54e-116">Prospect to cash samþætting er studd í eftirfarandi útgáfum:</span><span class="sxs-lookup"><span data-stu-id="ac54e-116">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="ac54e-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (desember 2017)</span><span class="sxs-lookup"><span data-stu-id="ac54e-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="ac54e-118">Dynamics 365 for Finance and Operations, Enterprise Edition (desember 2017) - Smíðun forrits 7.3.11971.56116 með verkvangsuppfærslu 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="ac54e-118">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="ac54e-119">Dynamics 365 for Finance and Operations, Enterprise Edition (júlí 2017)</span><span class="sxs-lookup"><span data-stu-id="ac54e-119">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="ac54e-120">Dynamics 365 for Finance and Operations, Enterprise Edition (júlí 2017) með verkvangsuppfærslu 8 (Smíðun forrits 7.2.11792.56024 með verkvangssmíði 7.0.4565.16212).</span><span class="sxs-lookup"><span data-stu-id="ac54e-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="ac54e-121">Eftirtaldir bráðabætur eru nauðsynlegar:</span><span class="sxs-lookup"><span data-stu-id="ac54e-121">The following hotfixes are required:</span></span>

    - <span data-ttu-id="ac54e-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** - Þessi bráðabót gerir mögulega samstillingu sölupantana frá Sales til Finance and Operations gegnum gagnasamþættingareiginleikann.</span><span class="sxs-lookup"><span data-stu-id="ac54e-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="ac54e-123">Það veitir einnig nokkrar aðrar endurbætur.</span><span class="sxs-lookup"><span data-stu-id="ac54e-123">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="ac54e-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** - Þessi bráðabót gerir mögulega samstillingu sölupöntunarlína frá Finance and Operations til Sales gegnum gagnasamþættingareiginleikann.</span><span class="sxs-lookup"><span data-stu-id="ac54e-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="ac54e-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** - Þessi bráðabót gerir mögulega samstillingu sölupantana frá Finance and Operations til Sales gegnum gagnasamþættingareiginleikann.</span><span class="sxs-lookup"><span data-stu-id="ac54e-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ac54e-126">Þú þarft aðeins að setja upp KB4045570 vegna þess að uppsetningin inniheldur breytingar frá öðrum bráðabótum.</span><span class="sxs-lookup"><span data-stu-id="ac54e-126">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="ac54e-127">Dynamics 365 for Finance and Operations útgáfa 1611 (nóvember 2016)</span><span class="sxs-lookup"><span data-stu-id="ac54e-127">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="ac54e-128">Microsoft Dynamics 365 for Finance and Operations útgáfa 1611 (nóvember 2016) með verkvangsuppfærslu 8 eða hærra</span><span class="sxs-lookup"><span data-stu-id="ac54e-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="ac54e-129">Eftirtaldir bráðabætur eru nauðsynlegar:</span><span class="sxs-lookup"><span data-stu-id="ac54e-129">The following hotfixes are required:</span></span>

    - <span data-ttu-id="ac54e-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Gera samstillingu sölupantana við gagnasamþættingu mögulega frá Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="ac54e-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
    - <span data-ttu-id="ac54e-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Gera samstillingu sölupantanahausa og lína við gagnasamþættingu mögulega frá Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="ac54e-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
    - <span data-ttu-id="ac54e-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Stuðningi við prospect to cash samþættingu gegnum gagnaeiningar er krafist.</span><span class="sxs-lookup"><span data-stu-id="ac54e-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="ac54e-133">Eftir að hafa sett upp bráðabætur þarftu að kveikja á eftirfarandi runuvinnslu frá skjámyndinni **SalesPopulateProspectToCash**.</span><span class="sxs-lookup"><span data-stu-id="ac54e-133">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="ac54e-134">Þetta form er falið þar sem þú þarft það aðeins einu sinni.</span><span class="sxs-lookup"><span data-stu-id="ac54e-134">This form is hidden because you only need it once.</span></span> <span data-ttu-id="ac54e-135">Til að fá aðgang að forminu skaltu skrá þig inn í umhverfið og bæta eftirfarandi við vefslóðina í vafrafanginu þínu: &mi=action:SalesPopulateProspectToCash, til dæmis, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="ac54e-135">To access the form, log in to the environment and add the following to the URL in your browser address: &mi=action:SalesPopulateProspectToCash, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="ac54e-136">Þegar formið opnast skaltu smella á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="ac54e-136">When the form opens, click OK.</span></span> <span data-ttu-id="ac54e-137">Þetta mun fylla upp í nýjan **LineCreationSequnceNumber** reit í **SalesLine**, **SalesQuotationLine** og **CustInvoiceTrans** töflunum með einkvæmum gildum og endurhlaða afurðalistann.</span><span class="sxs-lookup"><span data-stu-id="ac54e-137">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="ac54e-138">Þetta er áskilið svo að Prospect to cash samþættingin virki.</span><span class="sxs-lookup"><span data-stu-id="ac54e-138">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="ac54e-139">Kerfisskilyrði fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="ac54e-139">System requirements for Sales</span></span>

<span data-ttu-id="ac54e-140">Eftirfarandi einingar verður að setja upp áður en Prospect to cash lausin er notað:</span><span class="sxs-lookup"><span data-stu-id="ac54e-140">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="ac54e-141">Dynamics 365 for Sales útgáfa 1612 (8.2.1.207) (DB 8.2.1.207) á netinu eða nýrri útgáfa</span><span class="sxs-lookup"><span data-stu-id="ac54e-141">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="ac54e-142">Prospect to cash lausn fyrir Dynamics 365 for Sales, útgáfa 1.15.0.0 (v15)</span><span class="sxs-lookup"><span data-stu-id="ac54e-142">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="ac54e-143">Settu upp Prospect to cash lausn fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="ac54e-143">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="ac54e-144">Sæktu [Prospect to cash fyrir Dynamics 365 for Sales lausn pakki zip-skrá](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) frá CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="ac54e-144">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="ac54e-145">Gakktu úr skugga um að opið sé fyrir zip-skrána.</span><span class="sxs-lookup"><span data-stu-id="ac54e-145">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="ac54e-146">Annars geta eftirfarandi villuboð birst þegar þú reynir að setja upp lausnapakkann: „Fann enga uppsetningarpakka.“</span><span class="sxs-lookup"><span data-stu-id="ac54e-146">Otherwise, when you try to install the solution package, you may receive the following error message, "No import packages were found."</span></span> <span data-ttu-id="ac54e-147">Til að opna fyrir zip-skrána, skaltu hægrismella á hana og velja **Eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="ac54e-147">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="ac54e-148">Veldu síðan **Opna fyrir**.</span><span class="sxs-lookup"><span data-stu-id="ac54e-148">Select **Unblock**.</span></span>
3. <span data-ttu-id="ac54e-149">Afþjappaðu hana og keyrðu **PackageDeployer.exe**.</span><span class="sxs-lookup"><span data-stu-id="ac54e-149">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="ac54e-150">Settu upp Prospect to Cash lausn á Sales tilvikinu þínu:</span><span class="sxs-lookup"><span data-stu-id="ac54e-150">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="ac54e-151">Veldu **Office 365** sem uppsetningartegund.</span><span class="sxs-lookup"><span data-stu-id="ac54e-151">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="ac54e-152">Veldu **Sýna ítarlegt**.</span><span class="sxs-lookup"><span data-stu-id="ac54e-152">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="ac54e-153">Veldu svæði fyrir skjóta uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="ac54e-153">For a quick installation, select a region.</span></span> <span data-ttu-id="ac54e-154">Ef þú velur **Veit ekki** leitar kerfið að öllum svæðum og uppsetning tekur lengri tíma.</span><span class="sxs-lookup"><span data-stu-id="ac54e-154">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="ac54e-155">Sláðu inn Notandanafn og Aðgangsorð kerfisnotanda sem hefur leyfi til að setja upp.</span><span class="sxs-lookup"><span data-stu-id="ac54e-155">Enter the user name and password of an admin user who has installation rights.</span></span>



