---
title: Seinkanir
description: "Þessi grein gefur upplýsingar um frestaðar dagsetningar á aðaláætlanagerð. Frestuð dagsetning er raunhæfur gjalddagi sem færsla fær ef fyrsta uppfyllingardagsetning sem aðaláætlanagerð reiknar út er síðar en umbeðin dagsetning."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8db5c507fbc68e637dbbc4ef3311d1fbd298f24f
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="delays"></a><span data-ttu-id="e8505-104">Seinkanir</span><span class="sxs-lookup"><span data-stu-id="e8505-104">Delays</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e8505-105">Þessi grein gefur upplýsingar um frestaðar dagsetningar á aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="e8505-105">This article provides information about delayed dates in master planning.</span></span> <span data-ttu-id="e8505-106">Frestuð dagsetning er raunhæfur gjalddagi sem færsla fær ef fyrsta uppfyllingardagsetning sem aðaláætlanagerð reiknar út er síðar en umbeðin dagsetning.</span><span class="sxs-lookup"><span data-stu-id="e8505-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="e8505-107">Aðaláætlanagerð°getur reiknað út fyrstu mögulegu dagsetningu uppfyllingar fyrir færslu, byggða á afhendingartíma, efnisframboði, getu til ráðstöfunar og ýmsum færibreytum áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="e8505-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="e8505-108">Ef aðaláætlanagerð°reiknar pöntunardagsetningu sem kemur á undan núverandi dagsetningu er ekki hægt að uppfylla pöntunina á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="e8505-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="e8505-109">Þess vegna seinkar pöntuninni.</span><span class="sxs-lookup"><span data-stu-id="e8505-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="e8505-110">Í þessu tilfelli áætlar aðaláætlanagerðin pöntunina fram í tímann frá núverandi dagsetningu og hefur afhendingartíma innifaldan.</span><span class="sxs-lookup"><span data-stu-id="e8505-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="e8505-111">Þessir afhendingartímar hefjast með allar vörur á neðri-stigs hluta.</span><span class="sxs-lookup"><span data-stu-id="e8505-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="e8505-112">Pöntunin fær svo seinkaða dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="e8505-112">The order then receives a delayed date.</span></span> <span data-ttu-id="e8505-113">Frestuð dagsetning er°raunhæfur gjalddagi, samkvæmt gildandi gögnum.</span><span class="sxs-lookup"><span data-stu-id="e8505-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="e8505-114">Aðaláætlanagerð reiknar°einnig dagafjölda seinkunar.</span><span class="sxs-lookup"><span data-stu-id="e8505-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="e8505-115">Í sumum tilvikum, gætir þú valið að reikna ekki seinkun, eins og þegar notendur vita að þeir°geta hraðað afhendingartíma með því að velja annan afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="e8505-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="e8505-116">Hægt er að skilgreina hvernig seinkanir°eru reiknaðar fyrir þekjuflokk.</span><span class="sxs-lookup"><span data-stu-id="e8505-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="e8505-117">Hægt er að tengja þekjuflokk°við vöru seinna.</span><span class="sxs-lookup"><span data-stu-id="e8505-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="e8505-118">Á síðunni**Færibreytur aðaláætlanagerðar** er hægt að stilla upphafstíma fyrir útreikning°seinkana.</span><span class="sxs-lookup"><span data-stu-id="e8505-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="e8505-119">Ef pöntun er uppfyllt að loknum tímafrestinum er einum degi°bætt við seinkunardagsetningu pöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="e8505-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

<span data-ttu-id="e8505-120">**Ábending:** Í eldri útgáfum voru reiknaðar seinkanir kallaðar *Framvirk boð*,°seinkunardagsetning var kölluð *Framvirk dagsetning*,°og°frestuð færsla kallaðist *Færsla sem var sett í framtíðinni*.</span><span class="sxs-lookup"><span data-stu-id="e8505-120">**Note:** In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

<a name="see-also"></a><span data-ttu-id="e8505-121">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e8505-121">See also</span></span>
--------

[<span data-ttu-id="e8505-122">Þekjustillingar</span><span class="sxs-lookup"><span data-stu-id="e8505-122">Coverage settings</span></span>](coverage-settings.md)




