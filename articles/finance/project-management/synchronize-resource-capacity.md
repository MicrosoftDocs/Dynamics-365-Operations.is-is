---
title: Samstilla tilfangagetu
description: Í þessu efnisatriði er að finna upplýsingar um hvernig á að samstilla afkastagetu tilfanga í dagatölum og verkum.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760572"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="2e601-103">Samstilla tilfangagetu</span><span class="sxs-lookup"><span data-stu-id="2e601-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e601-104">Vinnslur fyrir samstillingu tilfanga hjálpar til við að tryggja að upplýsingar fyrir dagatal og grunndagatal seytli niður í röðun tilfanga verks.</span><span class="sxs-lookup"><span data-stu-id="2e601-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="2e601-105">Ef dagatali er breytt gera ferlin nauðsynlegar uppfærslur á áætlun tilfanga verks.</span><span class="sxs-lookup"><span data-stu-id="2e601-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="2e601-106">Ferlin hjálpa einnig til með að bæta afköst, þar sem tilfangaupplýsingar á dagatalinu eru samstilltar fyrirfram.</span><span class="sxs-lookup"><span data-stu-id="2e601-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="2e601-107">Því gerast uppfærslur á upplýsingum tilfanga hraðar.</span><span class="sxs-lookup"><span data-stu-id="2e601-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="2e601-108">Mælt er með er skipuleggja ferlin sem runuvinnslu í stað þess að skipuleggja einn í einu.</span><span class="sxs-lookup"><span data-stu-id="2e601-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="2e601-109">Annars er hætta á að einhver gleymi sameiginlegum dagsetningum þegar upplýsingarnar voru síðast samstilltar.</span><span class="sxs-lookup"><span data-stu-id="2e601-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="2e601-110">Ef ekki eru notaðar sameiginlegar dagsetningar geta eyður komið fram við samstillingu á dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="2e601-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Samstilling dagatals](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="2e601-112">Samstilla tilfangagetu samantekta</span><span class="sxs-lookup"><span data-stu-id="2e601-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="2e601-113">Samstillingarferlið er hannað til að samstilla upplýsingar um öll dagatöl tilfanga.</span><span class="sxs-lookup"><span data-stu-id="2e601-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="2e601-114">Þessar upplýsingar innihalda grunnupplýsingar dagatals um allar breytingar á Töflu yfir afkastagetu tilfangadagatals.verksins.</span><span class="sxs-lookup"><span data-stu-id="2e601-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="2e601-115">Ef nýjum tilföngum er bætt við verkið, hjálpar samstilling við að tryggja að uppfærðu dagatalsupplýsingarnar séu tiltækar.</span><span class="sxs-lookup"><span data-stu-id="2e601-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="2e601-116">Þessa samstillingu er hægt að gera hvenær sem er.</span><span class="sxs-lookup"><span data-stu-id="2e601-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="2e601-117">Mælt er með því að nota runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="2e601-117">We recommend that you use a batch.</span></span> <span data-ttu-id="2e601-118">Valkostirnir er tiltækir í samstillingu frátekinnar afkastagetu.</span><span class="sxs-lookup"><span data-stu-id="2e601-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="2e601-119">Valið er **Verkefnastjórnun og bókhald** &gt; **Reglubundið** &gt; **Samstilling afkastagetu** &gt; **Samstilla afkastagetu samantekta**.</span><span class="sxs-lookup"><span data-stu-id="2e601-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="2e601-120">Stillið valkostina í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="2e601-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="2e601-121">Valkostur</span><span class="sxs-lookup"><span data-stu-id="2e601-121">Option</span></span>      | <span data-ttu-id="2e601-122">lýsing</span><span class="sxs-lookup"><span data-stu-id="2e601-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="2e601-123">Tímabilskóði</span><span class="sxs-lookup"><span data-stu-id="2e601-123">Period code</span></span> | <span data-ttu-id="2e601-124">Einnig er hægt að velja kóða dagsetningabils í fjárhagi til að stilla upphafs og lokadag fyrir samstillingarferli fyrir tilfangagetu samantekta.</span><span class="sxs-lookup"><span data-stu-id="2e601-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="2e601-125">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="2e601-125">Start date</span></span>  | <span data-ttu-id="2e601-126">Færa skal inn upphafsdag fyrir samstillingarferli fyrir tilfangagetu samantekta.</span><span class="sxs-lookup"><span data-stu-id="2e601-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="2e601-127">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="2e601-127">End date</span></span>    | <span data-ttu-id="2e601-128">Færa skal inn lokadag fyrir samstillingarferli fyrir tilfangagetu samantekta.</span><span class="sxs-lookup"><span data-stu-id="2e601-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="2e601-129">[![Samstillingarferli](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="2e601-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
