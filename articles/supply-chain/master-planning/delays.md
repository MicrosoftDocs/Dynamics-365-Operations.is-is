---
title: Seinkanir
description: Þetta efnisatriði veitir upplýsingar um seinkanir á dagsetningum í aðaláætlanagerð. Frestuð dagsetning er raunhæfur gjalddagi sem færsla fær ef fyrsta uppfyllingardagsetning sem aðaláætlanagerð reiknar út er síðar en umbeðin dagsetning.
author: roxanadiaconu
manager: AnnBe
ms.date: 03/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1a8c738fffda76f2a8492c20e2c67a154c68559
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1522290"
---
# <a name="delays"></a><span data-ttu-id="8f48c-104">Seinkanir</span><span class="sxs-lookup"><span data-stu-id="8f48c-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f48c-105">Þetta efnisatriði veitir upplýsingar um seinkanir á dagsetningum í aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="8f48c-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="8f48c-106">Frestuð dagsetning er raunhæfur gjalddagi sem færsla fær ef fyrsta uppfyllingardagsetning sem aðaláætlanagerð reiknar út er síðar en umbeðin dagsetning.</span><span class="sxs-lookup"><span data-stu-id="8f48c-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="8f48c-107">Aðaláætlanagerð°getur reiknað út fyrstu mögulegu dagsetningu uppfyllingar fyrir færslu, byggða á afhendingartíma, efnisframboði, getu til ráðstöfunar og ýmsum færibreytum áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="8f48c-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="8f48c-108">Ef aðaláætlanagerð°reiknar pöntunardagsetningu sem kemur á undan núverandi dagsetningu er ekki hægt að uppfylla pöntunina á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="8f48c-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="8f48c-109">Þess vegna seinkar pöntuninni.</span><span class="sxs-lookup"><span data-stu-id="8f48c-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="8f48c-110">Í þessu tilfelli áætlar aðaláætlanagerðin pöntunina fram í tímann frá núverandi dagsetningu og hefur afhendingartíma innifaldan.</span><span class="sxs-lookup"><span data-stu-id="8f48c-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="8f48c-111">Þessir afhendingartímar hefjast með allar vörur á neðri-stigs hluta.</span><span class="sxs-lookup"><span data-stu-id="8f48c-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="8f48c-112">Pöntunin fær svo seinkaða dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="8f48c-112">The order then receives a delayed date.</span></span> <span data-ttu-id="8f48c-113">Frestuð dagsetning er°raunhæfur gjalddagi, samkvæmt gildandi gögnum.</span><span class="sxs-lookup"><span data-stu-id="8f48c-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="8f48c-114">Aðaláætlanagerð reiknar°einnig dagafjölda seinkunar.</span><span class="sxs-lookup"><span data-stu-id="8f48c-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="8f48c-115">Í sumum tilvikum, gætir þú valið að reikna ekki seinkun, eins og þegar notendur vita að þeir°geta hraðað afhendingartíma með því að velja annan afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="8f48c-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="8f48c-116">Hægt er að skilgreina hvernig seinkanir°eru reiknaðar fyrir þekjuflokk.</span><span class="sxs-lookup"><span data-stu-id="8f48c-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="8f48c-117">Hægt er að tengja þekjuflokk°við vöru seinna.</span><span class="sxs-lookup"><span data-stu-id="8f48c-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="8f48c-118">Á síðunni**Færibreytur aðaláætlanagerðar** er hægt að stilla upphafstíma fyrir útreikning°seinkana.</span><span class="sxs-lookup"><span data-stu-id="8f48c-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="8f48c-119">Ef pöntun er uppfyllt að loknum tímafrestinum er einum degi°bætt við seinkunardagsetningu pöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="8f48c-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> [!NOTE]
> <span data-ttu-id="8f48c-120">Í eldri útgáfum voru útreiknaðar seinkanir kallaðar *Framvirk boð*, seinkunardagsetning var kölluð *Framvirk dagsetning* og frestuð færsla kallaðist *Færsla sem var sett í framtíðinni*.</span><span class="sxs-lookup"><span data-stu-id="8f48c-120">In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="desired-date"></a><span data-ttu-id="8f48c-121">Æskileg dagsetning</span><span class="sxs-lookup"><span data-stu-id="8f48c-121">Desired date</span></span>

<span data-ttu-id="8f48c-122">Á síðunni **Áætluð pöntun**, undir flipanum **Seinkanir**, er **Æskileg dagsetning** fyrir áætlaða pöntun.</span><span class="sxs-lookup"><span data-stu-id="8f48c-122">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="8f48c-123">Æskileg dagsetning fyrir áætlaða pöntun er grunndagsetning fyrir seinkanir sem er reiknuð dagsetning sem jafngildir **Umbeðinni dagsetningu** sem er reiknuð út frá **Nettóþörf**.</span><span class="sxs-lookup"><span data-stu-id="8f48c-123">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="8f48c-124">Ef áætluð pöntun er uppskriftarlína, framleiðslulína eða kanban-lína, er æskileg dagsetning byggð á **Dagsetning þarfa** og æskileg dagsetning birtist ekki á síðunni **Áætluð pöntun**.</span><span class="sxs-lookup"><span data-stu-id="8f48c-124">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="8f48c-125">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8f48c-125">Additional resources</span></span>
--------

[<span data-ttu-id="8f48c-126">Þekjustillingar</span><span class="sxs-lookup"><span data-stu-id="8f48c-126">Coverage settings</span></span>](coverage-settings.md)
