---
title: Samþætting við yfirlit Microsoft Dynamics 365 Field Service
description: Þetta efnisatriði veitir yfirlit yfir samþættingu við Microsoft Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
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
ms.openlocfilehash: 2a5c3e49f09bf4f1f90449db10d439f563ecc2c0
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249841"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a><span data-ttu-id="3dcc9-103">Samþætting við yfirlit Microsoft Dynamics 365 Field Service</span><span class="sxs-lookup"><span data-stu-id="3dcc9-103">Integration with Microsoft Dynamics 365 Field Service overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3dcc9-104">Supply Chain Management virkjar samstillingu viðskiptaferla á milli Dynamics 365 Supply Chain Management og Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="3dcc9-104">Supply Chain Management enables synchronization of business processes between Dynamics 365 Supply Chain Management and Dynamics 365 Field Service.</span></span> <span data-ttu-id="3dcc9-105">Samþættingarsviðin eru grunnstillt með því að nota sniðmát teygjanlegrar gagnasamþættingar og Common Data Service til að gera samþættingu viðskiptaferla virka.</span><span class="sxs-lookup"><span data-stu-id="3dcc9-105">The integration scenarios are configured by using extensible Data integrator templates and Common Data Service to enable the synchronization of business processes.</span></span>
<span data-ttu-id="3dcc9-106">Hægt er að nota stöðluð sniðmát til að búa til sérsniðin samþættingarverk þar sem hægt er að varpa stöðluðum og sérsniðnum viðbótarreitum og einingum, til að aðlaga samþættinguna og uppfylla sérstakar viðskiptaþarfir.</span><span class="sxs-lookup"><span data-stu-id="3dcc9-106">Standard templates can be used to create custom integration projects, where additional standard and custom fields and entities can be mapped to adjust the integration and meet specific business needs.</span></span> 

<span data-ttu-id="3dcc9-107">Samþætting field service byggir ofan á fyrirliggjandi prospect-to-cash virknina.</span><span class="sxs-lookup"><span data-stu-id="3dcc9-107">The field service integration builds on top of the existing prospect-to-cash functionality.</span></span>

![Samstilling viðskiptaferla milli Supply Chain Management og Field Service](./media/field-service-integration.png)

<span data-ttu-id="3dcc9-109">Fyrsti áfangi samþættingar milli Field Service og Supply Chain Management einblínir á að gera kleift að reikningsfæra vinnupantanir og samninga frá Field Service til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3dcc9-109">The first phase  of the integration between Field Service and Supply Chain Management is focused on enabling work orders and agreements in Field Service to be invoiced in Supply Chain Management.</span></span> <span data-ttu-id="3dcc9-110">Studda flæðið byrjar í Field Service, þar sem upplýsingar frá vinnupöntunum eru samstilltar við Supply Chain Management sem sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="3dcc9-110">The supported flow starts in Field Service, where information from work orders is synchronized to Supply Chain Management as sales orders.</span></span> <span data-ttu-id="3dcc9-111">Í Supply Chain Management eru sölupantanir innheimtir til að búa til reikningsgögn.</span><span class="sxs-lookup"><span data-stu-id="3dcc9-111">In Supply Chain Management, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="3dcc9-112">Að auki eru upplýsingarnar frá samþykktum reikningum Field Service samstilltar við Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3dcc9-112">In addition, the information from Field Service agreement invoices is synchronized to Supply Chain Management.</span></span> <span data-ttu-id="3dcc9-113">Gagnasamþætting Microsoft Dynamics 365 samstillir gögn með sérsniðnum verkum.</span><span class="sxs-lookup"><span data-stu-id="3dcc9-113">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="3dcc9-114">Hægt er að nota stöðluð sniðmát til að búa til sérsniðin samþættingarverk þar sem hægt er að varpa stöðluðum og sérsniðnum viðbótarreitum, ásamt einingum, til að aðlaga samþættinguna og uppfylla sérstakar kröfur.</span><span class="sxs-lookup"><span data-stu-id="3dcc9-114">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="3dcc9-115">Fyrsti áfangi samþættingar milli Field Service og Supply Chain Management virkjar samstillingu á eftirfarandi atriðum:</span><span class="sxs-lookup"><span data-stu-id="3dcc9-115">The first phase of the integration between Field Service and Supply Chain Management enables synchronization of the following items:</span></span>

- [<span data-ttu-id="3dcc9-116">Afurðir í Supply Chain Management við afurðir í Field Service sem innihalda upplýsingar um gerð afurðar</span><span class="sxs-lookup"><span data-stu-id="3dcc9-116">Products in Supply Chain Management to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="3dcc9-117">Vinnupantanir úr Field Service við sölupantanir í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3dcc9-117">Work orders in Field Service to sales orders in Supply Chain Management</span></span>](field-service-work-order.md)
- [<span data-ttu-id="3dcc9-118">Reikningar í Field Service við reikninga með frjálsum texta í Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3dcc9-118">Invoices in Field Service to free text invoices in Supply Chain Management</span></span>](field-service-invoice.md)

<span data-ttu-id="3dcc9-119">Til að sjá dæmi um hvernig þú getur samstillt vinnupöntun milli Field Service og Supply Chain Management skaltu horfa á stutta YouTube vídeóið [Hvernig á að samstilla vinnupöntun við Microsoft Dynamics 365 samþættingu](https://www.youtube.com/watch?v=46ylO7raZAo).</span><span class="sxs-lookup"><span data-stu-id="3dcc9-119">To see an example of how you can synchronize a work order between Field Service and Supply Chain Management, watch the short YouTube video [How to synchronize a work order with Microsoft Dynamics 365 Integration](https://www.youtube.com/watch?v=46ylO7raZAo).</span></span>

## <a name="integration-with-field-service-including-inventory-and-project-information"></a><span data-ttu-id="3dcc9-120">Samþætting við Field Service, þ.m.t. birgðir og verkupplýsingar</span><span class="sxs-lookup"><span data-stu-id="3dcc9-120">Integration with Field Service, including inventory and project information</span></span>

<span data-ttu-id="3dcc9-121">Viðbótarvirknin í þessum seinni áfanga lagði áherslu á að veita tæknimönnum á vettvangi innsýn í birgðaupplýsingar frá Supply Chain Management, sem gerir þeim kleift að uppfæra birgðastöður og sjá um flutning á efni.</span><span class="sxs-lookup"><span data-stu-id="3dcc9-121">The additional functionality in this second phase focused on giving field technicians insight about the inventory information from Supply Chain Management, allowing them to update inventory levels and do material transfers.</span></span> <span data-ttu-id="3dcc9-122">Að auki njóta fyrirtæki, sem setja upp eða þjónusta seldar vörur, ávinnings af betri stýringu og sýnileika á sölu- og þjónustuferlinu út í gegn með samþættingu frá verkum.</span><span class="sxs-lookup"><span data-stu-id="3dcc9-122">In addition, companies installing or servicing sold goods will benefit from better control and visibility to the full sales and service process with integration from projects.</span></span>

### <a name="functionality-includes-integration-of"></a><span data-ttu-id="3dcc9-123">Virkni felur í sér samþættingu á:</span><span class="sxs-lookup"><span data-stu-id="3dcc9-123">Functionality includes integration of:</span></span>
- <span data-ttu-id="3dcc9-124">Upplýsingum um vöruhúsa</span><span class="sxs-lookup"><span data-stu-id="3dcc9-124">Warehouse information</span></span>
- <span data-ttu-id="3dcc9-125">Upplýsingum um lagerbirgðir</span><span class="sxs-lookup"><span data-stu-id="3dcc9-125">On-hand inventory information</span></span>
- <span data-ttu-id="3dcc9-126">Birgðaflutningum</span><span class="sxs-lookup"><span data-stu-id="3dcc9-126">Inventory transfers</span></span>
- <span data-ttu-id="3dcc9-127">Leiðrétting birgða</span><span class="sxs-lookup"><span data-stu-id="3dcc9-127">Inventory adjustments</span></span>
- <span data-ttu-id="3dcc9-128">Verkefni Supply Chain Management tengd verkbeiðnir Dynamics 365 Field Service</span><span class="sxs-lookup"><span data-stu-id="3dcc9-128">Supply Chain Management projects connected with Dynamics 365 Field Service work orders</span></span>
- <span data-ttu-id="3dcc9-129">Dynamics 365 Field Service vinnupantanir með tengli við verk Supply Chain Management, nota þetta verknúmer á sölupöntun til að gera reikningsfærslu úr verkinu mögulega.</span><span class="sxs-lookup"><span data-stu-id="3dcc9-129">Dynamics 365 Field Service work orders with link to Supply Chain Management projects, apply this project number to the sales order to allow invoicing from the project.</span></span> 

![Samstilling viðskiptaferla milli Supply Chain Management og Field Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a><span data-ttu-id="3dcc9-131">Seinni áfangi samþættingar milli Field Service og Supply Chain Management virkjar samstillingu við eftirfarandi sniðmát:</span><span class="sxs-lookup"><span data-stu-id="3dcc9-131">The second phase of the integration between Field Service and Supply Chain Management enables synchronization with the following templates:</span></span>
- <span data-ttu-id="3dcc9-132">Vöruhús (Framboðsstjórnun að sviði þjónustu) - Vöruhús frá Supply Chain Management til Field Service [Ítarleg fyrirspurn]</span><span class="sxs-lookup"><span data-stu-id="3dcc9-132">Warehouses (Supply Chain Management to Field Service) - Warehouses from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="3dcc9-133">Birgðir afurðar (Supply Chain Management að Field Service) - Upplýsingar um birgðastöðu frá Supply Chain Management til Field Service [Ítarleg fyrirspurn]</span><span class="sxs-lookup"><span data-stu-id="3dcc9-133">Product Inventory (Supply Chain Management to Field Service) - Inventory level information from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="3dcc9-134">Leiðrétting birgða (Field Service til Supply Chain Management) - Leiðrétting birgða frá Field Service til Supply Chain Management [Ítarleg fyrirspurn]</span><span class="sxs-lookup"><span data-stu-id="3dcc9-134">Inventory Adjustment (Field Service to Supply Chain Management) - Inventory adjustments from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="3dcc9-135">Birgðaflutningar (Field Service til Supply Chain Management) - Birgðaflutningar frá Field Service til Supply Chain Management [Ítarleg fyrirspurn]</span><span class="sxs-lookup"><span data-stu-id="3dcc9-135">Inventory Transfers (Field Service to Supply Chain Management) - Inventory transfers from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="3dcc9-136">Verk (Supply Chain Management að Field Service) - Verklisti frá Supply Chain Management til Field Service</span><span class="sxs-lookup"><span data-stu-id="3dcc9-136">Projects (Supply Chain Management to Field Service) - Project list from Supply Chain Management to Field Service</span></span> 
- <span data-ttu-id="3dcc9-137">Vinnupantanir með Project (Field Service til Supply Chain Management) - Vinnupantanir í Field Service til sölupantana í Supply Chain Management, með stuðningi fyrir Project [Ítarleg fyrirspurn]</span><span class="sxs-lookup"><span data-stu-id="3dcc9-137">Work Orders with Project (Field Service to Supply Chain Management) - Work orders in Field Service to Sales orders  in Supply Chain Management, with support for Project [Advanced Query]</span></span> 
- <span data-ttu-id="3dcc9-138">Afurðir Field Service með birgðaeiningu (Supply Chain Management til Sales) - Supply Chain Management „Seljanlegar útgefnar afurðir“ Finance and Operations til „afurða“ Sales fyrir Field Service, þ.m.t. birgðaeiningu</span><span class="sxs-lookup"><span data-stu-id="3dcc9-138">Field Service Products with Inventory unit (Supply Chain Management to Sales) - Supply Chain Management 'Sellable released products' to Sales 'Products' for Field Service, including Inventory unit</span></span> 

## <a name="system-requirements"></a><span data-ttu-id="3dcc9-139">Kerfiskröfur</span><span class="sxs-lookup"><span data-stu-id="3dcc9-139">System requirements</span></span>

### <a name="system-requirements-for-supply-chain-management"></a><span data-ttu-id="3dcc9-140">Kerfiskröfur fyrir Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3dcc9-140">System requirements for Supply Chain Management</span></span>
<span data-ttu-id="3dcc9-141">Samþætting Field Service styður eftirfarandi útgáfur:</span><span class="sxs-lookup"><span data-stu-id="3dcc9-141">Field Service integration supports the following versions:</span></span>

- <span data-ttu-id="3dcc9-142">Dynamics 365 for Finance and Operations útgáfa 8.1.2 (desember 2018) var gefin út í desember 2018 og hefur útgáfunúmer forrits 8.1.195 með verkvangsuppfærslu 22 (7.0.5095).</span><span class="sxs-lookup"><span data-stu-id="3dcc9-142">Dynamics 365 for Finance and Operations version 8.1.2 (December 2018) was released in December 2018 and has an application build number 8.1.195 with Platform update 22 (7.0.5095).</span></span> 

### <a name="system-requirements-for-field-service"></a><span data-ttu-id="3dcc9-143">Kerfisskilyrði fyrir Field Service</span><span class="sxs-lookup"><span data-stu-id="3dcc9-143">System requirements for Field Service</span></span>
<span data-ttu-id="3dcc9-144">Til að nota samþættingarlausn Field Service verður að setja upp eftirfarandi hluti:</span><span class="sxs-lookup"><span data-stu-id="3dcc9-144">To use the Field Service integration solution, you must install the following components:</span></span>

- <span data-ttu-id="3dcc9-145">Field Service (útgáfa 8.2.0.286) eða nýrri útgáfa á Dynamics 365 9.1.x - Gefin út í nóvember 2018</span><span class="sxs-lookup"><span data-stu-id="3dcc9-145">Field Service (version 8.2.0.286) or a later version on Dynamics 365 9.1.x - Released November 2018</span></span>
- <span data-ttu-id="3dcc9-146">Prospect to Cash (P2C) lausn fyrir Dynamics 365, útgáfa 1.15.0.1 eða nýrri útgáfa.</span><span class="sxs-lookup"><span data-stu-id="3dcc9-146">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="3dcc9-147">Lausnina er hægt að sækja hjá [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="3dcc9-147">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="3dcc9-148">Samþætting Field Service, verk- og birgðalausnir fyrir Dynamics 365, útgáfa 2.0.0.0 eða nýrri útgáfa.</span><span class="sxs-lookup"><span data-stu-id="3dcc9-148">'Field Service Integration, Project and Inventory' solution for Dynamics 365, version 2.0.0.0 or a later version.</span></span> <span data-ttu-id="3dcc9-149">Lausnina er hægt að sækja hjá [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span><span class="sxs-lookup"><span data-stu-id="3dcc9-149">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span></span>
