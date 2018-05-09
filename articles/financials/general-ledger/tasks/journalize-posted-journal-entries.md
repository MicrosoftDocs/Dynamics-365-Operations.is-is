--- 
title: "Skrá bókaðar bókarfærslur"
description: "Þetta ferli sýnir hvernig á að skrá bókaðar færslubókarfærslur."
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7211e56f80b085f6a245010e780512e92a52bc57
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="88d42-103">Skrá bókaðar bókarfærslur</span><span class="sxs-lookup"><span data-stu-id="88d42-103">Journalize posted journal entries</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="88d42-104">Þetta ferli sýnir hvernig á að skrá bókaðar færslubókarfærslur.</span><span class="sxs-lookup"><span data-stu-id="88d42-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="88d42-105">Þessi aðferð notar sýnifyrirtækið USMF.</span><span class="sxs-lookup"><span data-stu-id="88d42-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="88d42-106">Villuleita stillingar fyrir færslubókarskráningu undir fjárhag > fjárhagsuppsetning > færibreytur fyrir fjárhag.</span><span class="sxs-lookup"><span data-stu-id="88d42-106">Validate the settings for journalizing under General ledger > Ledger setup > General ledger parameters.</span></span>
2. <span data-ttu-id="88d42-107">Reiturinn Framlengja færslubók fjárhags er hægt að stilla á Já eða Nei.</span><span class="sxs-lookup"><span data-stu-id="88d42-107">The Extended ledger journal field can be set to Yes or No.</span></span> <span data-ttu-id="88d42-108">Ef Já verður úttak skýrslu mismunandi.</span><span class="sxs-lookup"><span data-stu-id="88d42-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="88d42-109">Velja hvort tímabliði geti verið lokað hafi ferli færslubókarskráningar ekki verið keyrt.</span><span class="sxs-lookup"><span data-stu-id="88d42-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span>
    * <span data-ttu-id="88d42-110">Ef þessi valkostur er stilltur á Já, er ekki hægt að loka tímabilið fyrr en færslubókarskráningarferlinu er lokið fyrir það tímabil.</span><span class="sxs-lookup"><span data-stu-id="88d42-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="88d42-111">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="88d42-111">Close the page.</span></span>
5. <span data-ttu-id="88d42-112">Fara í Fjárhagur > Reglubundin verkefni > Skráning í færslubók.</span><span class="sxs-lookup"><span data-stu-id="88d42-112">Go to General ledger > Periodic tasks > Journalizing.</span></span>
6. <span data-ttu-id="88d42-113">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="88d42-113">Click Filter.</span></span>
7. <span data-ttu-id="88d42-114">Auðkenna línuna með síuskilyrði sem á að skilgreina.</span><span class="sxs-lookup"><span data-stu-id="88d42-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="88d42-115">Í reitinn Skilyrði skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="88d42-115">In the Criteria field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="88d42-116">Smellið á Í lagi til að síusíðunni.</span><span class="sxs-lookup"><span data-stu-id="88d42-116">Click OK to close the filter page.</span></span>
10. <span data-ttu-id="88d42-117">Smellið á Í lagi til að hefja ferli færslubókarskráningar.</span><span class="sxs-lookup"><span data-stu-id="88d42-117">Click OK to start the journalizing process.</span></span>
    * <span data-ttu-id="88d42-118">Skýrrsla verður mynduð eftir að ferlinu er lokið.</span><span class="sxs-lookup"><span data-stu-id="88d42-118">A report will be generated after the process is complete.</span></span>  


