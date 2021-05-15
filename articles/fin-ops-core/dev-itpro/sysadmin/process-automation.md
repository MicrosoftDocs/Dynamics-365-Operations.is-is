---
title: Sjálfvirkni ferlis
description: Í þessu efnisatriði er að finna upplýsingar um hvernig sjálfvirkni ferlis býður upp á einfalda áætlanagerð fyrir ferla sem runuþjónninn keyrir.
author: RyanCCarlson2
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: a8722adfe410f15bc379f9b550f0618c881f067d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920830"
---
# <a name="process-automation"></a><span data-ttu-id="fc304-103">Sjálfvirkni ferlis</span><span class="sxs-lookup"><span data-stu-id="fc304-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fc304-104">Sjálfvirkni ferlis býður upp á einfalda áætlanagerð fyrir ferla sem runuþjónninn keyrir.</span><span class="sxs-lookup"><span data-stu-id="fc304-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="fc304-105">Uppfært dagatalsyfirlit áætlaðrar vinnu gerir notendum kleift að skoða og grípa til aðgerða á áætluðum og loknum vinnum.</span><span class="sxs-lookup"><span data-stu-id="fc304-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="fc304-106">Stjórnun</span><span class="sxs-lookup"><span data-stu-id="fc304-106">Administration</span></span>

<span data-ttu-id="fc304-107">Síða stjórnunarmiðstöðvar fyrir alla sjálfvirkni ferla finnst kerfisstjórnunareiningunni undir valmyndinni **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="fc304-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="fc304-108">Þessi síða sýnir alla sjálfvirka ferla (raðir) sem settar eru upp í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="fc304-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="fc304-109">Hún gerir þér einnig kleift að bæta við nýrri sjálfvirkni fyrir ferla beint af síðunni.</span><span class="sxs-lookup"><span data-stu-id="fc304-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="fc304-110">Þegar búið er að setja upp röð er hægt að stjórna hverri röð úr þessum lista.</span><span class="sxs-lookup"><span data-stu-id="fc304-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="fc304-111">Hægt er að breyta allri röðinni, eyða henni, skoða öll tilvik í listayfirliti eða slökkva á röðinni ef gera á hlé á áætlaðri vinnu í einhvern tíma.</span><span class="sxs-lookup"><span data-stu-id="fc304-111">You can choose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a while.</span></span> 

<span data-ttu-id="fc304-112">Öll ferli sem eru óvirk í eiginleikastjórnun birtast ekki þegar eiginleikinn er óvirkur.</span><span class="sxs-lookup"><span data-stu-id="fc304-112">Any processes that are disabled in feature management won't show when the feature is disabled.</span></span> <span data-ttu-id="fc304-113">Þar að auki mun röðunarvél fyrir sjálfvirkni ferlis ekki tímasetja nein tilvik eða bakgrunnsvinnslur fyrir óvirkan eiginleika.</span><span class="sxs-lookup"><span data-stu-id="fc304-113">Additionally, the process automation scheduling engine won't schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="fc304-114">Með því að virkja eiginleikann aftur verða öll tímasett tilvik eða bakgrunnsvinnslur í fortíðinni keyrð strax.</span><span class="sxs-lookup"><span data-stu-id="fc304-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span> <span data-ttu-id="fc304-115">Sjálfvirk áætlunarvél ferlisins treystir á runuvinnslu kerfisins, **Bókunarvinnsla sjálfvirkniferlis í kerfinu**, keyri.</span><span class="sxs-lookup"><span data-stu-id="fc304-115">The process automation scheduling engine relies on the system batch job, **Process automation polling system job** to run.</span></span> <span data-ttu-id="fc304-116">Ekki má breyta eða eiga við verkið á neinum tímapunkti.</span><span class="sxs-lookup"><span data-stu-id="fc304-116">The job shouldn't be altered or tampered with at any time.</span></span> 

## <a name="calendar-view"></a><span data-ttu-id="fc304-117">Dagbókaryfirlit</span><span class="sxs-lookup"><span data-stu-id="fc304-117">Calendar view</span></span>

<span data-ttu-id="fc304-118">Einn af helstu kostum þess að gera feril sjálfvirkan er möguleikinn á því að sjá áætlaða vinnu í einföldu dagatalsyfirliti.</span><span class="sxs-lookup"><span data-stu-id="fc304-118">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="fc304-119">Þetta yfirlit gerir þér kleift að sjá vinnu eina viku í senn.</span><span class="sxs-lookup"><span data-stu-id="fc304-119">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="fc304-120">Þú munt sjá þetta yfirlit hægra megin á síðunni **Sjálfvirkni ferlis**.</span><span class="sxs-lookup"><span data-stu-id="fc304-120">You'll see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="fc304-121">Fyllt verður út í hana með áætlaðri vinnu fyrir valdar raðir.</span><span class="sxs-lookup"><span data-stu-id="fc304-121">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="fc304-122">[![Dagatal sjálfvirkni ferlis](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="fc304-122">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="fc304-123">Breytingar á tilviki</span><span class="sxs-lookup"><span data-stu-id="fc304-123">Occurrence changes</span></span>

<span data-ttu-id="fc304-124">Hægt er að breyta hverju tilviki fyrir sig án þess að hafa áhrif á önnur tilvik sem skilgreind er af röðinni þar sem tilvikin áttu uppruna sinn.</span><span class="sxs-lookup"><span data-stu-id="fc304-124">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="fc304-125">Tilvik áætlaðrar vinnu er hægt að breyta í dagatalsyfirlitinu með því að velja hnappinn **Skoða/breyta** og velja **Tilvik**.</span><span class="sxs-lookup"><span data-stu-id="fc304-125">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="fc304-126">Þessi síða veitir þér aðgang að öllum stillingum sem birtast upphaflega í leiðsagnarforriti fyrir uppsetningu raðar og býður upp á möguleikann á að gera einkvæma breytingu á völdu tilviki.</span><span class="sxs-lookup"><span data-stu-id="fc304-126">This page allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="fc304-127">Einnig er hægt að slökkva á tilviki áætlaðrar vinnu með því að velja hnappinn **Gera óvirkt** í dagatalsyfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="fc304-127">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span>

## <a name="developer-documentation"></a><span data-ttu-id="fc304-128">Fylgiskjöl forritunar</span><span class="sxs-lookup"><span data-stu-id="fc304-128">Developer documentation</span></span>

<span data-ttu-id="fc304-129">Þróunarrammi ferlisins gerir þróunaraðilum kleift að víkka sjálfvirkni ferlisins.</span><span class="sxs-lookup"><span data-stu-id="fc304-129">The process automation framework allows developers to extend the process automation framework.</span></span> <span data-ttu-id="fc304-130">Í fylgiskjölum [Meðhöndla sjálfvirkniramma](../process-automation/process-automation-framework.md) verður að finna upplýsingar um hvernig hægt er að búa til sérsniðin ferli sem þarf að keyra með runuþjóninum sem áætlaður er með leiðsagnarforriti fyrir sjálfvirkni ferlis og birtist sjálfkrafa í dagatalsyfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="fc304-130">The [Process automation framework](../process-automation/process-automation-framework.md) documentation provides information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
