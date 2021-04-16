---
title: Loka fjárhag í lok tímabils
description: Þetta efnisatriði lýsir þeim verkefnum sem er yfirleitt lokið þegar tímabilslokun er gerð fyrir fjárhag.
author: aprilolson
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9781a439469b54e5449382fbdd04447a7f4a079
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821914"
---
# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="e977d-103">Loka fjárhag í lok tímabils</span><span class="sxs-lookup"><span data-stu-id="e977d-103">Close the general ledger at period end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e977d-104">Þetta efnisatriði lýsir þeim verkefnum sem er yfirleitt lokið þegar tímabilslokun er gerð fyrir fjárhag.</span><span class="sxs-lookup"><span data-stu-id="e977d-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="e977d-105">Hægt er að ljúka við lokunarferlin í fjárhagnum við lok tímabils og ársins.</span><span class="sxs-lookup"><span data-stu-id="e977d-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="e977d-106">Lokunarferli°undirbúa kerfið fyrir nýtt tímabil.</span><span class="sxs-lookup"><span data-stu-id="e977d-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="e977d-107">Til að undirbúa kerfið fyrir nýtt ár verður að keyra ferlið Árslokavinnsla.</span><span class="sxs-lookup"><span data-stu-id="e977d-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="e977d-108">Hvert fyrirtæki hefur mismunandi ferli og skref sem það framkvæmir fyrir lok tímabils.</span><span class="sxs-lookup"><span data-stu-id="e977d-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="e977d-109">Hér eru sum valfrjálsu skrefin fyrir lok tímabila:</span><span class="sxs-lookup"><span data-stu-id="e977d-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="e977d-110">Ljúka verkefni fyrir allar aðrar kerfiseiningar, svo sem Viðskiptakröfur, Viðskiptaskuldir, og Birgðir.</span><span class="sxs-lookup"><span data-stu-id="e977d-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="e977d-111">Staðfestu að allar færslubækur séu bókaðar.</span><span class="sxs-lookup"><span data-stu-id="e977d-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="e977d-112">Keyra endurmat á erlendum gjaldmiðli til að mynda allan óinnleystan hagnað eða tapupphæðir.</span><span class="sxs-lookup"><span data-stu-id="e977d-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="e977d-113">Jafna færslur á milli fjárhagslykla.</span><span class="sxs-lookup"><span data-stu-id="e977d-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="e977d-114">Vinna allar áskildar úthlutanir.</span><span class="sxs-lookup"><span data-stu-id="e977d-114">Process any required allocations.</span></span>
-   <span data-ttu-id="e977d-115">Bóka leiðréttingar í lok tímabils handvirkt.</span><span class="sxs-lookup"><span data-stu-id="e977d-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="e977d-116">Skráð færslur og fara yfir **fjárhagsbók** skýrslu.</span><span class="sxs-lookup"><span data-stu-id="e977d-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="e977d-117">Framkvæma samlegð með því að nota samstæðufyrirtæki eða fjárhagsskýrslur.</span><span class="sxs-lookup"><span data-stu-id="e977d-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="e977d-118">Mynda ársreikninga í lok tímabils með því að nota fjárhagsskýrslur.</span><span class="sxs-lookup"><span data-stu-id="e977d-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="e977d-119">Stilla fjárhagstímabil á **Í bið**, þannig að engin önnur bókun á sér stað.</span><span class="sxs-lookup"><span data-stu-id="e977d-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="e977d-120">Einnig er hægt að takmarka tímabil við ákveðinn notendaflokk á meðan á aðgerðum við lok tímabils stendur, til að fá betri stýringu.</span><span class="sxs-lookup"><span data-stu-id="e977d-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="e977d-121">Ekki er gott að stilla tímabil á **Lokað fyrir fullt og allt**, þar sem ekki er hægt að enduropna tímabil sem hefur verið lokað.</span><span class="sxs-lookup"><span data-stu-id="e977d-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="e977d-122">Vinnusvæði lokunar fjárhagstímabils má nota til að til að skipuleggja og rekja verkefni sem eru áskilin fyrir mismunandi lokunarferli tímabila.</span><span class="sxs-lookup"><span data-stu-id="e977d-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="e977d-123">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="e977d-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="e977d-124">Vinnusvæði lokunar fjárhagstímabils</span><span class="sxs-lookup"><span data-stu-id="e977d-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="e977d-125">Árslokalokun</span><span class="sxs-lookup"><span data-stu-id="e977d-125">Year-end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="e977d-126">Fjöldalokun fjárhagstímabils</span><span class="sxs-lookup"><span data-stu-id="e977d-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]