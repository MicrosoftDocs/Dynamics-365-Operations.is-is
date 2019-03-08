---
title: Skrá bókaðar bókarfærslur
description: Þetta ferli sýnir hvernig á að skrá bókaðar færslubókarfærslur.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b50809cf9eb59475856f91d9f1ddfe28ecfd8de6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "318535"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="a531c-103">Skrá bókaðar bókarfærslur</span><span class="sxs-lookup"><span data-stu-id="a531c-103">Journalize posted journal entries</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a531c-104">Þetta ferli sýnir hvernig á að skrá bókaðar færslubókarfærslur.</span><span class="sxs-lookup"><span data-stu-id="a531c-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="a531c-105">Þessi aðferð notar sýnifyrirtækið USMF.</span><span class="sxs-lookup"><span data-stu-id="a531c-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="a531c-106">Villuleita stillingar fyrir færslubókarskráningu undir fjárhag > fjárhagsuppsetning > færibreytur fyrir fjárhag.</span><span class="sxs-lookup"><span data-stu-id="a531c-106">Validate the settings for journalizing under General ledger > Ledger setup > General ledger parameters.</span></span>
2. <span data-ttu-id="a531c-107">Reiturinn Framlengja færslubók fjárhags er hægt að stilla á Já eða Nei.</span><span class="sxs-lookup"><span data-stu-id="a531c-107">The Extended ledger journal field can be set to Yes or No.</span></span> <span data-ttu-id="a531c-108">Ef Já verður úttak skýrslu mismunandi.</span><span class="sxs-lookup"><span data-stu-id="a531c-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="a531c-109">Velja hvort tímabliði geti verið lokað hafi ferli færslubókarskráningar ekki verið keyrt.</span><span class="sxs-lookup"><span data-stu-id="a531c-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span>
    * <span data-ttu-id="a531c-110">Ef þessi valkostur er stilltur á Já, er ekki hægt að loka tímabilið fyrr en færslubókarskráningarferlinu er lokið fyrir það tímabil.</span><span class="sxs-lookup"><span data-stu-id="a531c-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="a531c-111">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a531c-111">Close the page.</span></span>
5. <span data-ttu-id="a531c-112">Fara í Fjárhagur > Reglubundin verkefni > Skráning í færslubók.</span><span class="sxs-lookup"><span data-stu-id="a531c-112">Go to General ledger > Periodic tasks > Journalizing.</span></span>
6. <span data-ttu-id="a531c-113">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="a531c-113">Click Filter.</span></span>
7. <span data-ttu-id="a531c-114">Auðkenna línuna með síuskilyrði sem á að skilgreina.</span><span class="sxs-lookup"><span data-stu-id="a531c-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="a531c-115">Í reitinn Skilyrði skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="a531c-115">In the Criteria field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="a531c-116">Smellið á Í lagi til að síusíðunni.</span><span class="sxs-lookup"><span data-stu-id="a531c-116">Click OK to close the filter page.</span></span>
10. <span data-ttu-id="a531c-117">Smellið á Í lagi til að hefja ferli færslubókarskráningar.</span><span class="sxs-lookup"><span data-stu-id="a531c-117">Click OK to start the journalizing process.</span></span>
    * <span data-ttu-id="a531c-118">Skýrrsla verður mynduð eftir að ferlinu er lokið.</span><span class="sxs-lookup"><span data-stu-id="a531c-118">A report will be generated after the process is complete.</span></span>  

