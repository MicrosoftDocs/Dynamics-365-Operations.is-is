---
title: Prospect to cash
description: Þetta efnisatriði veitir yfirlit yfir Prospect to cash lausnarinnar á milli Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: b46ece384a28f8e78989253fcf467fbf3feaf1b7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "309496"
---
# <a name="prospect-to-cash"></a><span data-ttu-id="8e9b2-103">Prospect to cash</span><span class="sxs-lookup"><span data-stu-id="8e9b2-103">Prospect to cash</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e9b2-104">Prospect to cash lausnin veitir beina samstillingu milli Dynamics 365 for Finance and Operations og Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="8e9b2-105">Prospect to cash sniðmát sem eru í boði með eiginleika gagnasamþættingar leyfir flæði gagna fyrir reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantanir og sölureikninga milli Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="8e9b2-106">Á meðan gögnin flæði á milli Finance and Operations og Sales er hægt að framkvæma sölu- og markaðsstarf í Sales og meðhöndla pöntunaruppfyllingu með því að nota birgðastjórnun í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="8e9b2-107">Frekari upplýsingar um samþættingu Prospect to cash er hægt að skoða í stuttu YouTube myndbandi: [Prospect to cash samþætting](https://www.youtube.com/watch?v=AVV9x5x-XCg).</span><span class="sxs-lookup"><span data-stu-id="8e9b2-107">For more information about the Prospect to cash integration, watch the short YouTube video [Prospect to cash integration](https://www.youtube.com/watch?v=AVV9x5x-XCg).</span></span>

<span data-ttu-id="8e9b2-108">Í núverandi útgáfu býður Prospect to cash lausnin upp á eftirfarandi gerðir af beinni samstillingu:</span><span class="sxs-lookup"><span data-stu-id="8e9b2-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="8e9b2-109">Viðhalda reikningum í Sales og samstilla þá beint úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8e9b2-109">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="8e9b2-110">Vinna með afurðir í Finance and Operations og samstilla þær beint við Sales</span><span class="sxs-lookup"><span data-stu-id="8e9b2-110">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="8e9b2-111">Vinna með tengiliði í Sales og samstilla þá beint við tengiliði eða viðskiptavini í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8e9b2-111">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="8e9b2-112">Samstilla sölutilboð beint úr Sales við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8e9b2-112">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="8e9b2-113">Samstilla sölupantanir beint milli Sales og Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8e9b2-113">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="8e9b2-114">Samstilla sölureikninga beint úr Finance and Operations við Sales</span><span class="sxs-lookup"><span data-stu-id="8e9b2-114">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="8e9b2-115">Kerfisskilyrði fyrir Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8e9b2-115">System requirements for Finance and Operations</span></span>
<span data-ttu-id="8e9b2-116">Prospect to cash samþætting er studd í eftirfarandi útgáfum:</span><span class="sxs-lookup"><span data-stu-id="8e9b2-116">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="8e9b2-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (desember 2017)</span><span class="sxs-lookup"><span data-stu-id="8e9b2-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="8e9b2-118">Dynamics 365 for Finance and Operations, Enterprise Edition (desember 2017) - Smíðun forrits 7.3.11971.56116 með verkvangsuppfærslu 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="8e9b2-118">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="8e9b2-119">Dynamics 365 for Finance and Operations, Enterprise Edition (júlí 2017)</span><span class="sxs-lookup"><span data-stu-id="8e9b2-119">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="8e9b2-120">Dynamics 365 for Finance and Operations, Enterprise Edition (July 2017) með verkvangsuppfærslu 8 (Forrit smíð 7.2.11792.56024 með verkvangur smíð 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="8e9b2-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="8e9b2-121">Eftirtaldir bráðabætur eru nauðsynlegar:</span><span class="sxs-lookup"><span data-stu-id="8e9b2-121">The following hotfixes are required:</span></span>

  - <span data-ttu-id="8e9b2-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** - Þessi bráðabót gerir mögulega samstillingu sölupantana frá Sales til Finance and Operations gegnum gagnasamþættingareiginleikann.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="8e9b2-123">Það veitir einnig nokkrar aðrar endurbætur.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-123">It also provides several other enhancements.</span></span>
  - <span data-ttu-id="8e9b2-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** - Þessi bráðabót gerir mögulega samstillingu sölupöntunarlína frá Finance and Operations til Sales gegnum gagnasamþættingareiginleikann.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
  - <span data-ttu-id="8e9b2-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** - Þessi bráðabót gerir mögulega samstillingu sölupantana frá Finance and Operations til Sales gegnum gagnasamþættingareiginleikann.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e9b2-126">Þú þarft aðeins að setja upp KB4045570 vegna þess að uppsetningin inniheldur breytingar frá öðrum bráðabótum.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-126">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="8e9b2-127">Dynamics 365 for Finance and Operations útgáfa 1611 (nóvember 2016)</span><span class="sxs-lookup"><span data-stu-id="8e9b2-127">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="8e9b2-128">Dynamics 365 for Finance and Operations útgáfa 1611 (nóvember 2016) með verkvangsuppfærslu 8 eða hærra</span><span class="sxs-lookup"><span data-stu-id="8e9b2-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="8e9b2-129">Eftirtaldir bráðabætur eru nauðsynlegar:</span><span class="sxs-lookup"><span data-stu-id="8e9b2-129">The following hotfixes are required:</span></span>

  - <span data-ttu-id="8e9b2-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Gera samstillingu sölupantana við gagnasamþættingu mögulega frá Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
  - <span data-ttu-id="8e9b2-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Gera samstillingu sölupantanahausa og lína við gagnasamþættingu mögulega frá Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
  - <span data-ttu-id="8e9b2-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Stuðningi við prospect to cash samþættingu gegnum gagnaeiningar er krafist.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="8e9b2-133">Eftir að hafa sett upp bráðabætur þarftu að kveikja á eftirfarandi runuvinnslu frá skjámyndinni **SalesPopulateProspectToCash**.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-133">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="8e9b2-134">Þetta form er falið þar sem þú þarft það aðeins einu sinni.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-134">This form is hidden because you only need it once.</span></span> <span data-ttu-id="8e9b2-135">Til að fá aðgang að forminu skaltu skrá þig inn í umhverfið og bæta eftirfarandi við veffang vafra þíns: *&mi=action:SalesPopulateProspectToCash*, til dæmis, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-135">To access the form, log in to the environment and add the following to the URL in your browser address: *&mi=action:SalesPopulateProspectToCash*, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="8e9b2-136">Þegar formið opnast skaltu smella á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-136">When the form opens, click OK.</span></span> <span data-ttu-id="8e9b2-137">Þetta mun fylla upp í nýjan **LineCreationSequnceNumber** reit í **SalesLine**, **SalesQuotationLine** og **CustInvoiceTrans** töflunum með einkvæmum gildum og endurhlaða afurðalistann.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-137">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="8e9b2-138">Þetta er áskilið svo að Prospect to cash samþættingin virki.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-138">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="8e9b2-139">Kerfisskilyrði fyrir Sales</span><span class="sxs-lookup"><span data-stu-id="8e9b2-139">System requirements for Sales</span></span>

<span data-ttu-id="8e9b2-140">Eftirfarandi einingar verður að setja upp áður en Prospect to cash lausin er notað:</span><span class="sxs-lookup"><span data-stu-id="8e9b2-140">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="8e9b2-141">Dynamics 365 for Sales útgáfa 1612 (8.2.1.207) (DB 8.2.1.207) á netinu eða nýrri útgáfa</span><span class="sxs-lookup"><span data-stu-id="8e9b2-141">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="8e9b2-142">Prospect to cash lausn fyrir Dynamics 365 for Sales, útgáfa 1.15.0.0 eða nýrri útgáfa.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-142">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 or a later version.</span></span> <span data-ttu-id="8e9b2-143">Lausnina er hægt að sækja hjá AppSource.</span><span class="sxs-lookup"><span data-stu-id="8e9b2-143">The solution is available for download from AppSource.</span></span> <span data-ttu-id="8e9b2-144">[Sækja Dynamics 365, Prospect to Cash](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="8e9b2-144">[Download Dynamics 365, Prospect to Cash](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
