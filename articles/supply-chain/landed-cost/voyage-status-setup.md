---
title: Staða ferðar
description: Þetta efnisatriði lýsir því hvernig á að koma á fót stöðugildunum sem notendur geta úthlutað á ferðir.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: b7180cc9ab2d13f2260635d717adb7aab2177ab9
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500887"
---
# <a name="voyage-status-setup"></a><span data-ttu-id="8c0ca-103">Uppsetningarstaða ferðar</span><span class="sxs-lookup"><span data-stu-id="8c0ca-103">Voyage status setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8c0ca-104">Á síðunni **Ferðastöður** eru sett upp mengi stöðugilda sem notendur geta úthlutað á ferðir.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-104">On the **Voyage statuses** page, you establish the set of status values that users can assign to voyages.</span></span> <span data-ttu-id="8c0ca-105">Notendur geta úthlutað gildi ferðastöðu á öll stig ferðar: ferð, gám, fólíó, innkaupapöntun og vöru (innkaupalínur og flutningspöntunarlínur).</span><span class="sxs-lookup"><span data-stu-id="8c0ca-105">Users can assign voyage status values to all levels of a voyage: voyage, shipping container, folio, purchase order, and item (purchase lines and transfer order lines).</span></span> <span data-ttu-id="8c0ca-106">Þetta er notað í tvennum tilgangi:</span><span class="sxs-lookup"><span data-stu-id="8c0ca-106">They are used for two purposes:</span></span>

- <span data-ttu-id="8c0ca-107">Upplýsa skal notandann um stöðu á ferð, gámi, fólíói, innkaupapöntun eða vöru (innkaupalínum og flutningspöntunarlínum).</span><span class="sxs-lookup"><span data-stu-id="8c0ca-107">Inform the user about the status of the voyage, shipping container, folio, purchase order, or item (purchase lines and transfer order lines).</span></span>
- <span data-ttu-id="8c0ca-108">Takmarka notkun kostnaðarsvæðisins við að koma í veg fyrir breytingar eða eyðingu.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-108">Limit the use of the cost area by preventing modification or deletion.</span></span>

<span data-ttu-id="8c0ca-109">Til að setja upp ferðastöður skal fara í **Heildarkostnaður \> Uppsetning \> Ferðastöður**.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-109">To set up your voyage statuses, go to **Landed cost \> Setup \> Voyage statuses**.</span></span> <span data-ttu-id="8c0ca-110">Þar er hægt að bæta við, fjarlægja og breyta stöðu með því að nota hnappana á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-110">There, you can add, remove, and edit statuses by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="8c0ca-111">Hvert kostnaðarsvæði er með eigin stillingar og stigveldi fyrir ferðastöðu.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-111">Each cost area has its own set and hierarchy of voyage statuses.</span></span> <span data-ttu-id="8c0ca-112">Þar af leiðandi, á síðunni **Ferðastöður**, í reitnum **Kostnaðarþáttur**, þarf fyrst að velja kostnaðarþáttinn sem á að skoða eða búa til stöðu ferðar fyrir.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-112">Therefore, on the **Voyage statuses** page, in the **Cost area** field, you must first select the cost area that you want to view or create voyage statuses for.</span></span> <span data-ttu-id="8c0ca-113">Fyrir hverja ferðastöðu skal því næst stilla reitina sem lýst er í eftirfarandi töflu, eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-113">Then, for each voyage status, set the fields that are described in the following table, as required.</span></span> <span data-ttu-id="8c0ca-114">Athugið að stöðu á ferð er einnig hægt að breyta sjálfkrafa eftir kerfisatvikum, eins og reglur sem hafa verið settar á með því að nota stjórnstöð rakningar.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-114">Note that the status of a voyage can also be automatically changed by system events, such as rules that have been established by using the tracking control center.</span></span>

| <span data-ttu-id="8c0ca-115">Svæði</span><span class="sxs-lookup"><span data-stu-id="8c0ca-115">Field</span></span> | <span data-ttu-id="8c0ca-116">lýsing</span><span class="sxs-lookup"><span data-stu-id="8c0ca-116">Description</span></span> |
|---|---|
| <span data-ttu-id="8c0ca-117">Staða ferðar</span><span class="sxs-lookup"><span data-stu-id="8c0ca-117">Voyage status</span></span> | <span data-ttu-id="8c0ca-118">Færið inn heiti ferðastöðunnar.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-118">Enter the name of the voyage status.</span></span> |
| <span data-ttu-id="8c0ca-119">lýsing</span><span class="sxs-lookup"><span data-stu-id="8c0ca-119">Description</span></span> | <span data-ttu-id="8c0ca-120">Færa inn lýsingu á ferðastöðunni.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-120">Enter a description of the voyage status.</span></span> |
| <span data-ttu-id="8c0ca-121">Breyta</span><span class="sxs-lookup"><span data-stu-id="8c0ca-121">Modify</span></span> | <span data-ttu-id="8c0ca-122">Veljið þennan gátreit ef notendur hafa leyfi til að breyta ferðum sem eru með þessa stöðu.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-122">Select this check box if users are allowed to modify voyages that have this status.</span></span> |
| <span data-ttu-id="8c0ca-123">Eyða</span><span class="sxs-lookup"><span data-stu-id="8c0ca-123">Delete</span></span> | <span data-ttu-id="8c0ca-124">Veljið þennan gátreit ef notendur hafa leyfi til að eyða ferðum sem eru með þessa stöðu.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-124">Select this check box if users are allowed to delete voyages that have this status.</span></span> |
| <span data-ttu-id="8c0ca-125">Skylda</span><span class="sxs-lookup"><span data-stu-id="8c0ca-125">Mandatory</span></span> | <span data-ttu-id="8c0ca-126">Veljið þennan gátreit til að gera ferðastöðuna áskilda, svo ekki sé hægt að sleppa henni.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-126">Select this check box to make the voyage status mandatory, so that it can't be skipped.</span></span> |
| <span data-ttu-id="8c0ca-127">Yfirstig</span><span class="sxs-lookup"><span data-stu-id="8c0ca-127">Parent</span></span> | <span data-ttu-id="8c0ca-128">Notið þennan reit til að koma á stigveldi á meðal stöðugildanna.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-128">Use this field to establish a hierarchy among the status values.</span></span> <span data-ttu-id="8c0ca-129">Aðeins er hægt að breyta ferðastöðum (annaðhvort handvirkt eða sjálfkrafa) niður á við í stigveldinu, frá stöðu yfireiningar til einnar af undireiningunum.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-129">Voyage statuses can be changed (either manually or automatically) only downward in the hierarchy, from a parent status to one of its child statuses.</span></span>

> [!NOTE]
> <span data-ttu-id="8c0ca-130">Aðeins þarf að setja upp tilgreinda ferðastöður sem fyrirtækið notar.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-130">You have to set up only the specific voyage statuses that your organization uses.</span></span> <span data-ttu-id="8c0ca-131">Dæmigerðar stöður ferðar eru m.a. *Staðfest*, *Vörur í flutningi*, *Móttekið*, *Tilbúið fyrir kostnaðarútreikning* og *Kostnaðarútreikningur*.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-131">Typical voyage statuses include *Confirmed*, *Goods in transit*, *Received*, *Ready for costing*, and *Costed*.</span></span> <span data-ttu-id="8c0ca-132">Hins vegar gætu aðrar stöður verið í boði.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-132">However, other statuses might be present.</span></span>
