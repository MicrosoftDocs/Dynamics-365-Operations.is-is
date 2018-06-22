---
title: "Samþætting við Microsoft Dynamics 365 for Field Service"
description: "Þetta efnisatriði veitir yfirlit yfir samþættingu við Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
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
ms.sourcegitcommit: a57e23691a6b4d48c6b8dd6d1f61fc9730365b39
ms.openlocfilehash: 0c1268d2fddcf7b28ecfc3197f21e9d30a5a5855
ms.contentlocale: is-is
ms.lasthandoff: 05/31/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="1798e-103">Samþætting við Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="1798e-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1798e-104">Microsoft Dynamics 365 for Finance and Operations virkjar samstillingu viðskiptaferla milli Finance and Operations og Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="1798e-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="1798e-105">Samþættingarsviðin eru grunnstillt með því að nota sniðmát teygjanlegrar gagnasamþættingar og Common Data Service (CDS) til að gera samþættingu viðskiptaferla virka.</span><span class="sxs-lookup"><span data-stu-id="1798e-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="1798e-106">[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="1798e-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="1798e-107">Fyrsti áfangi samþættingar milli Field Service og Finance and Operations einblínir á að gera kleift að reikningsfæra vinnupantanir og samninga frá Field Service til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1798e-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="1798e-108">Studda flæðið byrjar í Field Service, þar sem upplýsingar frá vinnupöntunum eru samstilltar við Finance and Operations sem sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="1798e-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="1798e-109">Í Finance and Operations eru sölupantanir reikningsfærðar til að búa til reikningsskjöl.</span><span class="sxs-lookup"><span data-stu-id="1798e-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="1798e-110">Að auki eru upplýsingarnar frá samþykktum reikningum Field Service samstilltar við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1798e-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="1798e-111">Gagnasamþætting Microsoft Dynamics 365 samstillir gögn með sérsniðnum verkum.</span><span class="sxs-lookup"><span data-stu-id="1798e-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="1798e-112">Hægt er að nota stöðluð sniðmát til að búa til sérsniðin samþættingarverk þar sem hægt er að varpa stöðluðum og sérsniðnum viðbótarreitum, ásamt einingum, til að aðlaga samþættinguna og uppfylla sérstakar kröfur.</span><span class="sxs-lookup"><span data-stu-id="1798e-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="1798e-113">Fyrsti áfangi samþættingar milli Field Service og Finance og Operations virkjar samstillingu á eftirfarandi atriðum:</span><span class="sxs-lookup"><span data-stu-id="1798e-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="1798e-114">Afurðir í Finance and Operations við afurðir í Field Service sem innihalda upplýsingar um gerð afurðar</span><span class="sxs-lookup"><span data-stu-id="1798e-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="1798e-115">Vinnupantanir í Field Service við sölupantanir í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1798e-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="1798e-116">Reikningar í Field Service við reikninga með frjálsum texta í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1798e-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="1798e-117">Til að sjá dæmi um hvernig þú getur samstillt vinnupöntun milli Field Service og Finance and Operations skaltu horfa á stutta YouTube vídeóið [Samstilling vinnupöntunar á milli Dynamics 365 for Field Service og Finance and Operations](https://www.youtube.com/watch?v=hAB4TDVMjxU).</span><span class="sxs-lookup"><span data-stu-id="1798e-117">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video [Synchronize a work order between Dynamics 365 for Field Service and Finance and Operations](https://www.youtube.com/watch?v=hAB4TDVMjxU).</span></span>

[![](https://img.youtube.com/vi/hAB4TDVMjxU/0.jpg)](https://www.youtube.com/watch?v=hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="1798e-118">Kerfisskilyrði fyrir Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1798e-118">System requirements for Finance and Operations</span></span>
<span data-ttu-id="1798e-119">Samþætting Field Service styður eftirfarandi útgáfur:</span><span class="sxs-lookup"><span data-stu-id="1798e-119">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="1798e-120">Dynamics 365 for Finance and Operations útgáfa 8.0 (apríl 2018) eða nýrri</span><span class="sxs-lookup"><span data-stu-id="1798e-120">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="1798e-121">Dynamics 365 for Finance and Operations útgáfa 8.0 (apríl 2018) var gefin út í apríl 2018 og hefur útgáfunúmer forrits 8.0.30.8020 með verkvangsuppfærslu 15 (7.0.4841.35234).</span><span class="sxs-lookup"><span data-stu-id="1798e-121">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="1798e-122">Kerfisskilyrði fyrir Field Service</span><span class="sxs-lookup"><span data-stu-id="1798e-122">System requirements for Field Service</span></span>
<span data-ttu-id="1798e-123">Til að nota samþættingarlausn Field Service verður að setja upp eftirfarandi hluti:</span><span class="sxs-lookup"><span data-stu-id="1798e-123">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="1798e-124">Microsoft Dynamics 365 for Field Service 9.0 eða nýrri</span><span class="sxs-lookup"><span data-stu-id="1798e-124">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="1798e-125">Dynamics 365 for Field Service útgáfa 1612 (9.0.1.733) (DB 9.0.1.733) á netinu eða nýrri útgáfa.</span><span class="sxs-lookup"><span data-stu-id="1798e-125">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="1798e-126">Prospect to Cash (P2C) lausn fyrir Dynamics 365, útgáfa 1.15.0.1 eða nýrri útgáfa.</span><span class="sxs-lookup"><span data-stu-id="1798e-126">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="1798e-127">Lausnina er hægt að sækja hjá [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="1798e-127">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="1798e-128">Samþættingarlausn Field Service fyrir Dynamics 365, útgáfa 1.0.0.0 eða nýrri útgáfa.</span><span class="sxs-lookup"><span data-stu-id="1798e-128">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="1798e-129">Lausnina er hægt að sækja hjá [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span><span class="sxs-lookup"><span data-stu-id="1798e-129">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span></span>

