---
title: Stofna vinnuklasa
description: Þessi verklýsing sýnir hvernig á að setja upp vinnuklasa.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0e06cd5fc6dc27f79eb39bbd78932a166e9d442
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977214"
---
# <a name="create-a-work-class"></a><span data-ttu-id="cb51e-103">Stofna vinnuklasa</span><span class="sxs-lookup"><span data-stu-id="cb51e-103">Create a work class</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cb51e-104">Þessi verklýsing sýnir hvernig á að setja upp vinnuklasa.</span><span class="sxs-lookup"><span data-stu-id="cb51e-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="cb51e-105">Vinnuklasar eru notaðir til að beina og/eða takmarka gerð vinnupöntunarlínur sem starfsmaður í vöruhúsi er hægt að vinna í farsíma.</span><span class="sxs-lookup"><span data-stu-id="cb51e-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="cb51e-106">Línur sem starfskraftur getur unnið ákvarðast af vinnuklösum á valmyndaratriði fartækis sem starfskraftur í vöruhúsi hefur aðgang að og vinnuklasa sem er tilgreindur á vinnulínum.</span><span class="sxs-lookup"><span data-stu-id="cb51e-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that's specified on the work lines.</span></span> <span data-ttu-id="cb51e-107">Einnig er hægt að nota vinnuklösum til að villuleita frágangsstaðsetningu fyrir pöntunarlínu vinnu.</span><span class="sxs-lookup"><span data-stu-id="cb51e-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="cb51e-108">Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.</span><span class="sxs-lookup"><span data-stu-id="cb51e-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="cb51e-109">Þetta ferli er ætluð fyrir stjórnanda í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="cb51e-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="cb51e-110">Fara í vöruhúsakerfi > Uppsetning > Vinna > Vinnuklasar.</span><span class="sxs-lookup"><span data-stu-id="cb51e-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="cb51e-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="cb51e-111">Click New.</span></span>
3. <span data-ttu-id="cb51e-112">Færa inn gildi í reitnum Kenni Vinnuklasa .</span><span class="sxs-lookup"><span data-stu-id="cb51e-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="cb51e-113">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="cb51e-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cb51e-114">Í svæðinu gerð vinnupöntunar, skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="cb51e-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="cb51e-115">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="cb51e-115">Click New.</span></span>
7. <span data-ttu-id="cb51e-116">Í reitinn Gerð staðsetningar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="cb51e-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="cb51e-117">Ef gerð staðsetningar er valin, setur þetta takmarkanir á hvar hægt er að setja vörur eftir að þær hafa verið teknar til.</span><span class="sxs-lookup"><span data-stu-id="cb51e-117">If you select a location type, this sets a restriction on where items can be put after they've been picked.</span></span> <span data-ttu-id="cb51e-118">Þessi stilling er notuð þegar staðsetningarleiðbeiningar reynir að leysa úr staðsetningu, eða ef starfsmaður vöruhússins veitir staðsetningu handvirkt fyrir valmyndaratriði fartækis.</span><span class="sxs-lookup"><span data-stu-id="cb51e-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="cb51e-119">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="cb51e-119">Close the page.</span></span>

