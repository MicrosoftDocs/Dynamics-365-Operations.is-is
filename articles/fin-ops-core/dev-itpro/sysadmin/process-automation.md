---
title: Sjálfvirkni ferlis
description: Í þessu efnisatriði er að finna upplýsingar um hvernig sjálfvirkni ferlis býður upp á einfalda áætlanagerð fyrir ferla sem runuþjónninn keyrir.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 06/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 2ab4e7510ff98b9fbf0223096b905e9de47f52e1
ms.sourcegitcommit: 1833c1e07a32c8ad41e4a1516e78100ae04a2156
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/26/2020
ms.locfileid: "3508186"
---
# <a name="process-automation"></a><span data-ttu-id="95189-103">Sjálfvirkni ferlis</span><span class="sxs-lookup"><span data-stu-id="95189-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="95189-104">Sjálfvirkni ferlis býður upp á einfalda áætlanagerð fyrir ferla sem runuþjónninn keyrir.</span><span class="sxs-lookup"><span data-stu-id="95189-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="95189-105">Uppfært dagatalsyfirlit áætlaðrar vinnu gerir notendum kleift að skoða og grípa til aðgerða á áætluðum og loknum vinnum.</span><span class="sxs-lookup"><span data-stu-id="95189-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="95189-106">Stjórnun</span><span class="sxs-lookup"><span data-stu-id="95189-106">Administration</span></span>

<span data-ttu-id="95189-107">Síða stjórnunarmiðstöðvar fyrir alla sjálfvirkni ferla finnst kerfisstjórnunareiningunni undir valmyndinni **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="95189-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="95189-108">Þessi síða sýnir alla sjálfvirka ferla (raðir) sem settar eru upp í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="95189-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="95189-109">Hún gerir þér einnig kleift að bæta við nýrri sjálfvirkni fyrir ferla beint af síðunni.</span><span class="sxs-lookup"><span data-stu-id="95189-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="95189-110">Þegar búið er að setja upp röð er hægt að stjórna hverri röð úr þessum lista.</span><span class="sxs-lookup"><span data-stu-id="95189-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="95189-111">Hægt er að breyta allri röðinni, eyða henni, skoða öll tilvik í listayfirliti eða slökkva á röðinni ef gera á hlé á áætlaðri vinnu í einhvern tíma.</span><span class="sxs-lookup"><span data-stu-id="95189-111">You can chose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a period of time.</span></span> 

## <a name="calendar-view"></a><span data-ttu-id="95189-112">Dagbókaryfirlit</span><span class="sxs-lookup"><span data-stu-id="95189-112">Calendar view</span></span> 
<span data-ttu-id="95189-113">Einn af helstu kostum þess að gera feril sjálfvirkan er möguleikinn á því að sjá áætlaða vinnu í einföldu dagatalsyfirliti.</span><span class="sxs-lookup"><span data-stu-id="95189-113">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="95189-114">Þetta yfirlit gerir þér kleift að sjá vinnu eina viku í senn.</span><span class="sxs-lookup"><span data-stu-id="95189-114">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="95189-115">Þú munt sjá þetta yfirlit hægra megin á síðunni **Sjálfvirkni ferlis**.</span><span class="sxs-lookup"><span data-stu-id="95189-115">You will see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="95189-116">Fyllt verður út í hana með áætlaðri vinnu fyrir valdar raðir.</span><span class="sxs-lookup"><span data-stu-id="95189-116">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="95189-117">[![Dagatal sjálfvirkni ferlis](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="95189-117">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="95189-118">Breytingar á tilviki</span><span class="sxs-lookup"><span data-stu-id="95189-118">Occurrence changes</span></span>
<span data-ttu-id="95189-119">Hægt er að breyta hverju tilviki fyrir sig án þess að hafa áhrif á önnur tilvik sem skilgreind er af röðinni þar sem tilvikin áttu uppruna sinn.</span><span class="sxs-lookup"><span data-stu-id="95189-119">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="95189-120">Tilvik áætlaðrar vinnu er hægt að breyta í dagatalsyfirlitinu með því að velja hnappinn **Skoða/breyta** og velja **Tilvik**.</span><span class="sxs-lookup"><span data-stu-id="95189-120">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="95189-121">Þetta veitir þér aðgang að öllum stillingum sem birtast upphaflega í leiðsagnarforriti fyrir uppsetningu raðar og býður upp á möguleikann á að gera einkvæma breytingu á völdu tilviki.</span><span class="sxs-lookup"><span data-stu-id="95189-121">This allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="95189-122">Einnig er hægt að slökkva á tilviki áætlaðrar vinnu með því að velja hnappinn **Gera óvirkt** í dagatalsyfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="95189-122">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span> 

## <a name="developer-documentation"></a><span data-ttu-id="95189-123">Fylgiskjöl forritunar</span><span class="sxs-lookup"><span data-stu-id="95189-123">Developer documentation</span></span> 
<span data-ttu-id="95189-124">Verið er að skrifa fylgiskjöl þróunaraðila til að gera þróunaraðilum kleift að stækka rammann utan um sjálfvirkni ferlis.</span><span class="sxs-lookup"><span data-stu-id="95189-124">Developer documentation is currently being written to allow developers to extend the process automation framework.</span></span> <span data-ttu-id="95189-125">Í þessum fylgiskjölum verður að finna upplýsingar um hvernig hægt er að búa til sérsniðin ferli sem þarf að keyra með runuþjóninum sem áætlaður er með leiðsagnarforriti fyrir sjálfvirkni ferlis og birtist sjálfkrafa í dagatalsyfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="95189-125">This documentation will provide information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>
