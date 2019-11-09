---
title: Loka fjárhag í lok tímabils
description: Þetta efnisatriði lýsir þeim verkefnum sem er yfirleitt lokið þegar tímabilslokun er gerð fyrir fjárhag.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eca533ed1621ec3507d8510f75842c0f0165275
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186740"
---
# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="5ee44-103">Loka fjárhag í lok tímabils</span><span class="sxs-lookup"><span data-stu-id="5ee44-103">Close the general ledger at period end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ee44-104">Þetta efnisatriði lýsir þeim verkefnum sem er yfirleitt lokið þegar tímabilslokun er gerð fyrir fjárhag.</span><span class="sxs-lookup"><span data-stu-id="5ee44-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="5ee44-105">Hægt er að ljúka við lokunarferlin í fjárhagnum við lok tímabils og ársins.</span><span class="sxs-lookup"><span data-stu-id="5ee44-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="5ee44-106">Lokunarferli°undirbúa kerfið fyrir nýtt tímabil.</span><span class="sxs-lookup"><span data-stu-id="5ee44-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="5ee44-107">Til að undirbúa kerfið fyrir nýtt ár verður að keyra ferlið Árslokavinnsla.</span><span class="sxs-lookup"><span data-stu-id="5ee44-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="5ee44-108">Hvert fyrirtæki hefur mismunandi ferli og skref sem það framkvæmir fyrir lok tímabils.</span><span class="sxs-lookup"><span data-stu-id="5ee44-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="5ee44-109">Hér eru sum valfrjálsu skrefin fyrir lok tímabila:</span><span class="sxs-lookup"><span data-stu-id="5ee44-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="5ee44-110">Ljúka verkefni fyrir allar aðrar kerfiseiningar, svo sem Viðskiptakröfur, Viðskiptaskuldir, og Birgðir.</span><span class="sxs-lookup"><span data-stu-id="5ee44-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="5ee44-111">Staðfestu að allar færslubækur séu bókaðar.</span><span class="sxs-lookup"><span data-stu-id="5ee44-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="5ee44-112">Keyra endurmat á erlendum gjaldmiðli til að mynda allan óinnleystan hagnað eða tapupphæðir.</span><span class="sxs-lookup"><span data-stu-id="5ee44-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="5ee44-113">Jafna færslur á milli fjárhagslykla.</span><span class="sxs-lookup"><span data-stu-id="5ee44-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="5ee44-114">Vinna allar áskildar úthlutanir.</span><span class="sxs-lookup"><span data-stu-id="5ee44-114">Process any required allocations.</span></span>
-   <span data-ttu-id="5ee44-115">Bóka leiðréttingar í lok tímabils handvirkt.</span><span class="sxs-lookup"><span data-stu-id="5ee44-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="5ee44-116">Skráð færslur og fara yfir **fjárhagsbók** skýrslu.</span><span class="sxs-lookup"><span data-stu-id="5ee44-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="5ee44-117">Framkvæma samlegð með því að nota samstæðufyrirtæki eða fjárhagsskýrslur.</span><span class="sxs-lookup"><span data-stu-id="5ee44-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="5ee44-118">Mynda ársreikninga í lok tímabils með því að nota fjárhagsskýrslur.</span><span class="sxs-lookup"><span data-stu-id="5ee44-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="5ee44-119">Stilla fjárhagstímabil á **Í bið**, þannig að engin önnur bókun á sér stað.</span><span class="sxs-lookup"><span data-stu-id="5ee44-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="5ee44-120">Einnig er hægt að takmarka tímabil við ákveðinn notendaflokk á meðan á aðgerðum við lok tímabils stendur, til að fá betri stýringu.</span><span class="sxs-lookup"><span data-stu-id="5ee44-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="5ee44-121">Ekki er gott að stilla tímabil á **Lokað fyrir fullt og allt**, þar sem ekki er hægt að enduropna tímabil sem hefur verið lokað.</span><span class="sxs-lookup"><span data-stu-id="5ee44-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="5ee44-122">Vinnusvæði lokunar fjárhagstímabils má nota til að til að skipuleggja og rekja verkefni sem eru áskilin fyrir mismunandi lokunarferli tímabila.</span><span class="sxs-lookup"><span data-stu-id="5ee44-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="5ee44-123">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="5ee44-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="5ee44-124">Vinnusvæði lokunar fjárhagstímabils</span><span class="sxs-lookup"><span data-stu-id="5ee44-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="5ee44-125">Árslok</span><span class="sxs-lookup"><span data-stu-id="5ee44-125">Year end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="5ee44-126">Fjöldalokun fjárhagstímabils</span><span class="sxs-lookup"><span data-stu-id="5ee44-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)



