---
title: Sniðmát hleðslu
description: Í þessu efnisatriði er lýst hvernig eigi að setja upp farmsniðmát og hvernig á að tengja farmsniðmát við í nýjan farm.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1ea7f5244b483a1b9d6c55227c676a3878a71d83
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646400"
---
# <a name="load-templates"></a><span data-ttu-id="13d66-103">Sniðmát hleðslu</span><span class="sxs-lookup"><span data-stu-id="13d66-103">Load templates</span></span>

<span data-ttu-id="13d66-104">Þegar ný hleðsla er búin til er hægt að úthluta hleðslusniðmáti.</span><span class="sxs-lookup"><span data-stu-id="13d66-104">When you create a new load, you can assign a load template.</span></span> <span data-ttu-id="13d66-105">Hleðslusniðmátið inniheldur upplýsingar um búnað, og um mælingar á borð við hæð, breidd, dýpt og rúmmál hleðslunnar.</span><span class="sxs-lookup"><span data-stu-id="13d66-105">The load template contains information about equipment, and about measures such as the height, width, depth, and volume of the load.</span></span>

<span data-ttu-id="13d66-106">Í þessu efnisatriði er lýst hvernig eigi að setja upp farmsniðmát og hvernig á að tengja farmsniðmát við í nýjan farm.</span><span class="sxs-lookup"><span data-stu-id="13d66-106">This topic describes how to set up load templates, and how to associate a load template with a new load.</span></span>

## <a name="set-up-a-load-template"></a><span data-ttu-id="13d66-107">Setja upp hleðslusniðmát</span><span class="sxs-lookup"><span data-stu-id="13d66-107">Set up a load template</span></span>

1. <span data-ttu-id="13d66-108">Farið í **-flutningsstjórnun \> Uppsetning \> Hleðsluáætlun \> Hleðslusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="13d66-108">Go to **Transportation management \> Setup \> Load Building \> Load template**.</span></span>
1. <span data-ttu-id="13d66-109">Á aðgerðasvæðinu skal velja **Ný** til að bæta við nýju sniðmáti eða **Breyta** til að breyta fyrirliggjandi sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="13d66-109">On the Action Pane, select **New** to add a new template or **Edit** to edit an existing template.</span></span>
1. <span data-ttu-id="13d66-110">Í línunni fyrir nýtt eða fyrirliggjandi sniðmát skal stilla eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="13d66-110">In the row for the new or existing template, set the following fields:</span></span>

    - <span data-ttu-id="13d66-111">Í reitnum **Auðkenni hleðslusniðmáts** færirðu inn einkvæmt kenni fyrir hleðslusniðmátið.</span><span class="sxs-lookup"><span data-stu-id="13d66-111">**Load template ID** – Enter a unique identifier (ID) for the load template.</span></span>
    - <span data-ttu-id="13d66-112">**Búnaður** - Veljið búnað sem á að nota til að senda farminn.</span><span class="sxs-lookup"><span data-stu-id="13d66-112">**Equipment** – Select the equipment that should be used to ship the load.</span></span>
    - <span data-ttu-id="13d66-113">**Hæð farms**, **Breidd farms** og **Dýpt farms** – Sláðu inn mál farmsins.</span><span class="sxs-lookup"><span data-stu-id="13d66-113">**Load height**, **Load width**, and **Load depth** – Enter the dimensions of the load.</span></span>
    - <span data-ttu-id="13d66-114">**Leyfilegt ummál farms að hámarki** og **Þyngd farms að hámarki** – Sláðu inn leyfilegt ummál og leyfilega þyngd farms að hámarki.</span><span class="sxs-lookup"><span data-stu-id="13d66-114">**Max. allowed load volume** and **Max. allowed load weight** – Enter the maximum allowed volume and weight of the load.</span></span>
    - <span data-ttu-id="13d66-115">**Hámarks leyfileg brúttóþyngd** – Sláið inn hámarks leyfilega brúttóþyngd hleðslunnar.</span><span class="sxs-lookup"><span data-stu-id="13d66-115">**Maximum allowed gross weight** – Enter the maximum allowed gross weight of the load.</span></span> <span data-ttu-id="13d66-116">Brúttóþyngd farms inniheldur bæði umbúðaþyngd hans og hleðsluþyngd.</span><span class="sxs-lookup"><span data-stu-id="13d66-116">A load's gross weight includes both its tare weight and its loading weight.</span></span>
    - <span data-ttu-id="13d66-117">**Hámarksfjöldi leyfilegra farmhluta** – Færið inn hámarksfjölda farmhluta sem farmurinn getur innihaldið.</span><span class="sxs-lookup"><span data-stu-id="13d66-117">**Maximum number of freight pieces allowed** – Enter the maximum number of freight pieces that the load can contain.</span></span>
    - <span data-ttu-id="13d66-118">**Staflahleðsla á gólfi** – Veljið þennan gátreit til að nota gólfhleðslu.</span><span class="sxs-lookup"><span data-stu-id="13d66-118">**Stack load on floor** – Select this check box to use floor loading.</span></span> <span data-ttu-id="13d66-119">Við aðstæður þegar hlaðið er á gólf, er kössum staflað frá gólfi upp í loft, vegg til veggjar innan í gámnum til að hámarksnýta rýmið.</span><span class="sxs-lookup"><span data-stu-id="13d66-119">In a floor loading scenario, boxes are stacked floor to ceiling and wall to wall inside the container, to maximize capacity.</span></span>

1. <span data-ttu-id="13d66-120">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="13d66-120">On the Action Pane, select **Save**.</span></span>

## <a name="associate-a-load-template-with-a-new-load"></a><span data-ttu-id="13d66-121">Tengja álagssniðmát við nýja álag</span><span class="sxs-lookup"><span data-stu-id="13d66-121">Associate a load template with a new load</span></span>

1. <span data-ttu-id="13d66-122">Farið í **Flutningsstjórnun \> Áætlanagerð \> Vinnusvæði hleðsluáætlunar**.</span><span class="sxs-lookup"><span data-stu-id="13d66-122">Go to **Transportation management \> Planning \> Load planning workbench**.</span></span>
1. <span data-ttu-id="13d66-123">Í efri hluta síðunnar skal velja einn af eftirfarandi flipum, allt eftir gerð upprunaskjalsins sem verið er að búa til farm fyrir: **Sendingar**, **Sölulínur**, **Flutningslínur** eða **Innkaupapöntunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="13d66-123">In the upper part of the page, select one of the following tabs, depending on the type of source document that you're creating a load for: **Shipments**, **Sales lines**, **Transfer lines**, or **Purchase order lines**.</span></span> 
1. <span data-ttu-id="13d66-124">Veljið tiltekið skjal til að áætla hleðsluna fyrir.</span><span class="sxs-lookup"><span data-stu-id="13d66-124">Select the specific document to plan the load for.</span></span>
1. <span data-ttu-id="13d66-125">Á aðgerðasvæðinu, í flipanum **Framboð og eftirspurn**, í flokknum **Bæta við**, skal velja **Við nýjan farm**.</span><span class="sxs-lookup"><span data-stu-id="13d66-125">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span>
1. <span data-ttu-id="13d66-126">Í svarglugganum **Úthlutun hleðslusniðmáts**, í reitnum **Kenni hleðslusniðmáts**, skal velja sniðmátið sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="13d66-126">In the **Load template** dialog box, in the **Load template ID** field, select the template to apply.</span></span>
1. <span data-ttu-id="13d66-127">Veljið **Í lagi** til að nota sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="13d66-127">Select **OK** to apply the template.</span></span>
