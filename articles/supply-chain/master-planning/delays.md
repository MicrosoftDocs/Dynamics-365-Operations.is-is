---
title: Seinkanir
description: Þetta efnisatriði veitir upplýsingar um seinkanir á dagsetningum í aðaláætlanagerð. Frestuð dagsetning er raunhæfur gjalddagi sem færsla fær ef fyrsta uppfyllingardagsetning sem aðaláætlanagerð reiknar út er síðar en umbeðin dagsetning.
author: roxanadiaconu
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dcb11b3665c5d2f296f1ba2ce4708c4eff241b0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977989"
---
# <a name="delays"></a><span data-ttu-id="1ab17-104">Seinkanir</span><span class="sxs-lookup"><span data-stu-id="1ab17-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ab17-105">Þetta efnisatriði veitir upplýsingar um seinkanir á dagsetningum í aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="1ab17-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="1ab17-106">Frestuð dagsetning er raunhæfur gjalddagi sem færsla fær ef fyrsta uppfyllingardagsetning sem aðaláætlanagerð reiknar út er síðar en umbeðin dagsetning.</span><span class="sxs-lookup"><span data-stu-id="1ab17-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="1ab17-107">Aðaláætlanagerð°getur reiknað út fyrstu mögulegu dagsetningu uppfyllingar fyrir færslu, byggða á afhendingartíma, efnisframboði, getu til ráðstöfunar og ýmsum færibreytum áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="1ab17-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="1ab17-108">Ef aðaláætlanagerð°reiknar pöntunardagsetningu sem kemur á undan núverandi dagsetningu er ekki hægt að uppfylla pöntunina á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="1ab17-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="1ab17-109">Þess vegna seinkar pöntuninni.</span><span class="sxs-lookup"><span data-stu-id="1ab17-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="1ab17-110">Í þessu tilfelli áætlar aðaláætlanagerðin pöntunina fram í tímann frá núverandi dagsetningu og hefur afhendingartíma innifaldan.</span><span class="sxs-lookup"><span data-stu-id="1ab17-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="1ab17-111">Þessir afhendingartímar hefjast með allar vörur á neðri-stigs hluta.</span><span class="sxs-lookup"><span data-stu-id="1ab17-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="1ab17-112">Pöntunin fær svo seinkaða dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="1ab17-112">The order then receives a delayed date.</span></span> <span data-ttu-id="1ab17-113">Frestuð dagsetning er°raunhæfur gjalddagi, samkvæmt gildandi gögnum.</span><span class="sxs-lookup"><span data-stu-id="1ab17-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="1ab17-114">Aðaláætlanagerð reiknar°einnig dagafjölda seinkunar.</span><span class="sxs-lookup"><span data-stu-id="1ab17-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="1ab17-115">Í sumum tilvikum, gætir þú valið að reikna ekki seinkun, eins og þegar notendur vita að þeir°geta hraðað afhendingartíma með því að velja annan afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="1ab17-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="1ab17-116">Hægt er að skilgreina hvernig seinkanir°eru reiknaðar fyrir þekjuflokk.</span><span class="sxs-lookup"><span data-stu-id="1ab17-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="1ab17-117">Hægt er að tengja þekjuflokk°við vöru seinna.</span><span class="sxs-lookup"><span data-stu-id="1ab17-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="1ab17-118">Á síðunni **Færibreytur aðaláætlanagerðar** er hægt að stilla upphafstíma fyrir útreikning á seinkunum.</span><span class="sxs-lookup"><span data-stu-id="1ab17-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="1ab17-119">Ef pöntun er uppfyllt að loknum tímafrestinum er einum degi°bætt við seinkunardagsetningu pöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="1ab17-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> [!NOTE]
> <span data-ttu-id="1ab17-120">Í eldri útgáfum voru útreiknaðar seinkanir kallaðar *Framvirk boð*, seinkunardagsetning var kölluð *Framvirk dagsetning* og frestuð færsla kallaðist *Færsla sem var sett í framtíðinni*.</span><span class="sxs-lookup"><span data-stu-id="1ab17-120">In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a><span data-ttu-id="1ab17-121">Takmarkaðar tafir á framleiðsluuppsetningunni með mörgum BOM-stigum</span><span class="sxs-lookup"><span data-stu-id="1ab17-121">Limited delays in production setup with multiple BOM levels</span></span>
<span data-ttu-id="1ab17-122">Þegar þú vinnur með tafir í framleiðsluuppsetningunni sem hefur mörg BOM stig, er mikilvægt að hafa í huga að aðeins vörurnar beint fyrir ofan vöruna (í BOM-skipulagingunni) sem valda seinkuninni, verða uppfærðar með töf sem hluti af keyrslu aðaláætlunar.</span><span class="sxs-lookup"><span data-stu-id="1ab17-122">When you work with delays in a production setup that has multiple BOM levels, it is important to note that only the items directly above the item (in the BOM structure) causing the delay, will be updated with a delay as part of the master planning run.</span></span> <span data-ttu-id="1ab17-123">Töfum verður ekki beitt á aðrar vörur í BOM-skipulaginu fyrr en í fyrstu keyrslu aðaláætlunar, þegar fyrirhuguð pöntun fyrir efsta stigið er samþykkt eða styrkt.</span><span class="sxs-lookup"><span data-stu-id="1ab17-123">Other items in the BOM structure will not get the delay applied until the first master planning run, when the planned order for the top level is approved or firmed.</span></span> 

<span data-ttu-id="1ab17-124">Til að vinna í kringum þessa þekktu takmörkun er hægt að samþykkja (eða stýra) framleiðslupöntunum efst í BOM-skipulaginu með seinkunum áður en næsta aðaláætlunargerð er keyrð.</span><span class="sxs-lookup"><span data-stu-id="1ab17-124">To work around this known limitation, the production orders on the top of the BOM structure with delays can be approved (or firmed) prior to the next master planning run.</span></span> <span data-ttu-id="1ab17-125">Þannig verður seinkun frá seinkaðri fyrirhugaðri framleiðslupöntun haldið og allir undirliggjandi íhlutir uppfærðir til samræmis.</span><span class="sxs-lookup"><span data-stu-id="1ab17-125">This way the delay from the delayed approved planned production order will be kept and all underlying components will be updated accordingly.</span></span>
<span data-ttu-id="1ab17-126">Aðgerðaskilaboð er einnig hægt að nota til að bera kennsl á fyrirhugaðar pantanir sem hægt er að færa á síðari dagsetningu, vegna annarra tafa á BOM-skipulagi.</span><span class="sxs-lookup"><span data-stu-id="1ab17-126">Action messages can also be used to identify planned orders that can be moved to a later date, due to other delays in the BOM structure.</span></span>

## <a name="desired-date"></a><span data-ttu-id="1ab17-127">Æskileg dagsetning</span><span class="sxs-lookup"><span data-stu-id="1ab17-127">Desired date</span></span>

<span data-ttu-id="1ab17-128">Á síðunni **Áætluð pöntun**, undir flipanum **Seinkanir**, er **Æskileg dagsetning** fyrir áætlaða pöntun.</span><span class="sxs-lookup"><span data-stu-id="1ab17-128">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="1ab17-129">Æskileg dagsetning fyrir áætlaða pöntun er grunndagsetning fyrir seinkanir sem er reiknuð dagsetning sem jafngildir **Umbeðinni dagsetningu** sem er reiknuð út frá **Nettóþörf**.</span><span class="sxs-lookup"><span data-stu-id="1ab17-129">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="1ab17-130">Ef áætluð pöntun er uppskriftarlína, framleiðslulína eða kanban-lína, er æskileg dagsetning byggð á **Dagsetning þarfa** og æskileg dagsetning birtist ekki á síðunni **Áætluð pöntun**.</span><span class="sxs-lookup"><span data-stu-id="1ab17-130">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="1ab17-131">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1ab17-131">Additional resources</span></span>
--------

[<span data-ttu-id="1ab17-132">Þekjustillingar</span><span class="sxs-lookup"><span data-stu-id="1ab17-132">Coverage settings</span></span>](coverage-settings.md)
