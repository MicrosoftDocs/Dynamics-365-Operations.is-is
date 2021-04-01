---
title: Uppsetningarkröfur framleiðslu
description: Þessi grein veitir upplýsingar um uppsetningarskilyrðu áður en hægt er að vinna með framleiðslustýringu.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05a4c97697f13a41b65fba0df8c76bf884fc51a9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209372"
---
# <a name="production-setup-requirements"></a><span data-ttu-id="3c1aa-103">Uppsetningarkröfur framleiðslu</span><span class="sxs-lookup"><span data-stu-id="3c1aa-103">Production setup requirements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c1aa-104">Þessi grein veitir upplýsingar um uppsetningarskilyrðu áður en hægt er að vinna með framleiðslustýringu.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-104">This article provides information about setup requirements before you can work with Production control.</span></span> 

<span data-ttu-id="3c1aa-105">Framleiðslustýring er samþætt við aðgerðir í öðrum kerfiseiningum.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-105">Production control is integrated with features in other modules.</span></span> <span data-ttu-id="3c1aa-106">Vegna þessara tengsla er hægt að breyta framleiðslupöntunum og tryggja að þær uppfærist sjálfkrafa í öllum öðrum ferlum og útreikningum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-106">This interconnectivity lets you change production orders and make sure that they are automatically updated in all other related processes and calculations in the system.</span></span> <span data-ttu-id="3c1aa-107">Framkvæma ætti uppsetningaraðgerðirnar í þeirri röð sem þær birtast hér fyrir neðan.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-107">The following setup processes are listed in the order that you should complete them in.</span></span>

## <a name="required-baseline-setup-in-other-modules"></a><span data-ttu-id="3c1aa-108">Skyldug grunnuppsetning í öðrum kerfiseiningum</span><span class="sxs-lookup"><span data-stu-id="3c1aa-108">Required baseline setup in other modules</span></span>
<span data-ttu-id="3c1aa-109">Setja verður upp upplýsingar í öðrum einingum áður en hægt er að vinna með framleiðslustýringu.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-109">Information in other modules must be set up before you can work with Production control.</span></span> <span data-ttu-id="3c1aa-110">Uppsetning felur í sér eftirfarandi verkefni:</span><span class="sxs-lookup"><span data-stu-id="3c1aa-110">This setup includes the following tasks:</span></span>

-   <span data-ttu-id="3c1aa-111">Setja upp almennar upplýsingar um fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-111">Set up general company information.</span></span>
-   <span data-ttu-id="3c1aa-112">Setja upp fjárhag.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-112">Set up the general ledger.</span></span>
-   <span data-ttu-id="3c1aa-113">Skilgreina vöruflokka.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-113">Define item groups.</span></span>
-   <span data-ttu-id="3c1aa-114">Setja upp fjárhagslykla fyrir vöruflokka.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-114">Set up ledger accounts for item groups.</span></span>
-   <span data-ttu-id="3c1aa-115">Setja upp töflu fyrir birgðavörur í Birgðastjórnun.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-115">Set up the inventory item table in Inventory management.</span></span>
-   <span data-ttu-id="3c1aa-116">Stofna uppskriftir (BOMs) og uppskriftaútgáfur í birgðastjórnun.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-116">Create bills of materials (BOMs) and BOM versions in Inventory management.</span></span>

## <a name="required-calendar-and-resource-setup"></a><span data-ttu-id="3c1aa-117">Skyldug uppsetning dagatals og tilfanga</span><span class="sxs-lookup"><span data-stu-id="3c1aa-117">Required calendar and resource setup</span></span>
<span data-ttu-id="3c1aa-118">Áður en þú notar framleiðslustýring, opnaðu Fyrirtækisstjórnun og stofna og skilgreina dagatal og rekstrartilföng í eftirfarandi röð:</span><span class="sxs-lookup"><span data-stu-id="3c1aa-118">Before you use Production control, open Organization administration, and create and define the calendar and operations resources in the following order:</span></span>

1.  <span data-ttu-id="3c1aa-119">**Sniðmát vinnutíma** – Setja upp sniðmát vinnutíma til að skilgreina tímana sem eru í boði fyrir framleiðsluröðun.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-119">**Working time templates** – Set up working time templates to define the times that are available for production scheduling.</span></span>
2.  <span data-ttu-id="3c1aa-120">**Dagatöl** – Setja upp vinnutímadagatal til að skilgreina daga ársins sem eru í boði fyrir framleiðsluröðun.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-120">**Calendars** – Set up working time calendars to define the days of the year that are available for production scheduling.</span></span>
3.  <span data-ttu-id="3c1aa-121">**Tilfangaflokkar** – Setja upp tilfangaflokka til að flokka rekstrartilföngum, þannig að hægt er að fá yfirlit yfir allar lausa afkastagetu þegar röðun er keyrð.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-121">**Resource groups** – Set up resource groups to group the operations resources, so that you can get an overview of any free capacity when you run scheduling.</span></span> <span data-ttu-id="3c1aa-122">Ekki þarf að setja upp tilfangaflokka áður en þú setur upp rekstrartilföng.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-122">You don't have to set up resource groups before you set up operations resources.</span></span> <span data-ttu-id="3c1aa-123">Þó er mælt með að skilja hvernig skuli flokka tilföng þegar sett er upp framleiðslustýringu.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-123">However, we recommend that you understand how to group resources when you set up Production control.</span></span>
4.  <span data-ttu-id="3c1aa-124">**Tilföng** - Setja upp rekstrartilföng til að skilgreina tilföng sem notuð eru til að ljúka framleiðsluferli og til að áætla afkastagetu.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-124">**Resources** – Set up operations resources to define the resources that are used to complete the production process and plan for capacity.</span></span>

## <a name="required-production-parameters-setup"></a><span data-ttu-id="3c1aa-125">Skyldug uppsetning framleiðslufæribreyta</span><span class="sxs-lookup"><span data-stu-id="3c1aa-125">Required production parameters setup</span></span>
<span data-ttu-id="3c1aa-126">**Færibreytur framleiðslustýringar** – Setja upp grunnfæribreytur framleiðslu til að skilgreina hvernig kerfið meðhöndlar og vinnur úr framleiðslupöntunum.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-126">**Production control parameters** – Set up basic production parameters to define how the system handles and processes production orders.</span></span> <span data-ttu-id="3c1aa-127">Skilgreinið hvernig á að stofna, meta, raða og nota framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-127">Define how production orders are created, estimated, scheduled, and consumed.</span></span> <span data-ttu-id="3c1aa-128">Einnig er hægt að velja um svörun og hvernig kostnaðarbókhald fer fram.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-128">You can also select what kind of feedback you want and how cost accounting is done.</span></span>

## <a name="required-journal-name-identification"></a><span data-ttu-id="3c1aa-129">Skyldug auðkenning færslubókarheita</span><span class="sxs-lookup"><span data-stu-id="3c1aa-129">Required journal name identification</span></span>
<span data-ttu-id="3c1aa-130">**Heiti framleiðslubóka** – Tilgreina heiti framleiðslubóka sem eru notaðar til að skrá og bóka færslur.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-130">**Production journal names** – Specify the production journal names that are used to record and post transactions.</span></span>

## <a name="setup-if-you-use-operations"></a><span data-ttu-id="3c1aa-131">Uppsetning ef aðgerðir eru notaðar</span><span class="sxs-lookup"><span data-stu-id="3c1aa-131">Setup if you use operations</span></span>
<span data-ttu-id="3c1aa-132">Aðgerðir tákna tiltekna verkþætti sem er lokið til að framleiða endanlega afurð.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-132">Operations represent the specific activities that are completed to produce the finished product.</span></span> <span data-ttu-id="3c1aa-133">**Ábending:** Þú verður að þekkja gerðir verkþátta sem eru nauðsynleg til að framleiða vöruna, og röð og forgang þeirra verkþætti.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-133">**Note:** You must know the types of activities that are required in order to produce your item, and the order and priorities of those activities.</span></span> <span data-ttu-id="3c1aa-134">Þú Verður einnig vitað er hvaða tilföng eru innifalin, og hversu margar.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-134">You must also know which resources are involved, and how many.</span></span>

1.  <span data-ttu-id="3c1aa-135">**Aðgerðir** - Setja upp aðgerðir sem standa fyrir þau verk sem þarf að ljúka til að framleiða lokna afurð.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-135">**Operations** – Set up operations to represent the tasks that must be completed to produce the finished item.</span></span>
2.  <span data-ttu-id="3c1aa-136">**Tengsl** - Setja upp vensl aðgerða til að gefa ítarlegri eiginleika.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-136">**Relations** – Set up operation relations to establish detailed properties.</span></span> <span data-ttu-id="3c1aa-137">Vensl aðgerða eru skilgreind með því að smella á **Tengsl** á í **Aðgerðir** síðu.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-137">To define operation relations, click **Relations** on the **Operations** page.</span></span>

## <a name="setup-if-you-use-routes"></a><span data-ttu-id="3c1aa-138">Uppsetning ef leiðir eru notaðar</span><span class="sxs-lookup"><span data-stu-id="3c1aa-138">Setup if you use routes</span></span>
<span data-ttu-id="3c1aa-139">Ef unnið er með leiðir þarf að skilgreina aðgerðir fyrir hverja framleiðsluleið sem sett er upp.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-139">If you're working with routes, operations must be defined for every production route that you set up.</span></span> <span data-ttu-id="3c1aa-140">Leiðin sýnir hvernig varan fer á milli aðgerða, og frá upphafi framleiðsluferlis til enda.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-140">The route represents the path that the item takes from operation to operation, from the start of the production process to the end.</span></span>

1.  <span data-ttu-id="3c1aa-141">**Kostnaðartegundir** - Setja upp kostnaðartegundir til að skilgreina kostnað á hverja klukkustund í tilgreindum ferlum og uppsetningartímum.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-141">**Cost categories** – Set up cost categories to define the cost per hour of specified processes and setup times.</span></span>
2.  <span data-ttu-id="3c1aa-142">**Kostnaðarflokkar** - Setja upp kostnaðarflokka til að stofna og hafa umsjón með mörgum gerðum kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-142">**Cost groups** – Set up cost groups to create and maintain different types of costing.</span></span>
3.  <span data-ttu-id="3c1aa-143">**Leiðarflokkar** - Setja upp leiðaflokka til að skilgreina færibreytur sem eiga við um hópa af leiðum.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-143">**Route groups** – Set up route groups to define parameters that are related to groups of routes.</span></span> <span data-ttu-id="3c1aa-144">Það verður að setja upp leiðaflokka áður en farið er að stofna framleiðsluleiðir.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-144">You must set up route groups before you can create production routes.</span></span>
4.  <span data-ttu-id="3c1aa-145">**Leiðir** Setja upp framleiðsluleiðir og skilgreinið sjálfgefnar stillingar til að stjórna röðun, kostnaðarútreikning og verðlagningu leiðaaðgerða og framvinduskýrslur.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-145">**Routes** – Set up production routes, and define default settings to control scheduling, costing, and pricing of route operations, and to control progress reporting.</span></span>
5.  <span data-ttu-id="3c1aa-146">**Leiðarútgáfa** - Setja upp leiðarútgáfur til að virkja vöruafbrigði í framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-146">**Route version** – Set up route versions to enable item variations in production.</span></span>

## <a name="optional-advanced-settings"></a><span data-ttu-id="3c1aa-147">Valfrjálsar, ítarlegar stillingar</span><span class="sxs-lookup"><span data-stu-id="3c1aa-147">Optional advanced settings</span></span>
1.  <span data-ttu-id="3c1aa-148">**Framleiðsluflokkar** - Setja upp framleiðsluflokka til koma á tengslum milli framleiðslupöntunar og fjárhagslykla.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-148">**Production groups** – Set up production groups to establish relationships between the production order and ledger accounts.</span></span> <span data-ttu-id="3c1aa-149">Pantanir verða bókaðar í fjárhagslyklana eða flokkaðar í þá við skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-149">The ledger accounts are used to post or group orders for reporting.</span></span>
2.  <span data-ttu-id="3c1aa-150">**Framleiðsluhópar** - Stofna framleiðsluhópa til að flokka framleiðslupantanir fyrir vinnslu mikilvægra pantana eða til að eyða og bóka flokka pantana.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-150">**Production pools** – Create production pools to group production orders so that you can process urgent production orders, or delete and post groups of orders.</span></span>
3.  <span data-ttu-id="3c1aa-151">**Eiginleikar** -Skilgreina eiginleika til að stofna sérstakar eigindir sem hægt er að tengja við tilföng til að stýra röð framleiðslna.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-151">**Properties** – Define properties to create special attributes that you can assign to your resources to control the order of productions.</span></span> <span data-ttu-id="3c1aa-152">Eigindirnar eru tengdar vinnutímasniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="3c1aa-152">These attributes are connected to the working time template.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]