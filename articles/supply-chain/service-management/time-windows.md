---
title: Tímaskjámyndir
description: Hægt er að nota tímaglugga til að bæta röðun á þjónustupöntunarlínum.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d79e3d3756b8dc402d6f293437209b2e108be38e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430493"
---
# <a name="time-windows"></a><span data-ttu-id="dd969-103">Tímaskjámyndir</span><span class="sxs-lookup"><span data-stu-id="dd969-103">Time windows</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd969-104">Hægt er að nota tímaglugga til að bæta röðun á þjónustupöntunarlínum.</span><span class="sxs-lookup"><span data-stu-id="dd969-104">You can use time windows to optimize the scheduling of service order lines.</span></span> <span data-ttu-id="dd969-105">Hægt er að setja upp kerfið þannig að það stofni þjónustupantanir sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="dd969-105">You can set up the system so that it automatically creates service orders.</span></span> <span data-ttu-id="dd969-106">Byggt á skilyrðinu sem er tilgreint með tímaglugga er hægt að tengja eins margar þjónustupöntunarlínur og mögulegt er og niður í eins fáar þjónustupantanir og mögulegt er.</span><span class="sxs-lookup"><span data-stu-id="dd969-106">Based on the criteria specified by a time window, you can connect as many service order lines as possible to as few service orders as possible.</span></span>

<span data-ttu-id="dd969-107">Tímagluggar tilgreina hversu langt þjónustupöntunarlína getur færst til frá útreiknaðri dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="dd969-107">Time windows specify how far a service order line can move from its calculated date.</span></span> <span data-ttu-id="dd969-108">Útreiknaða dagsetningin er sú dagsetning þegar þjónustupöntunarlínan var látin eiga sér stað.</span><span class="sxs-lookup"><span data-stu-id="dd969-108">The calculated date is the date when the service order line was scheduled to occur.</span></span> <span data-ttu-id="dd969-109">Dagsetningin byggist á bilstillingunni og þjónustutímabilinu sem var skilgreint á síðunni **Þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="dd969-109">The date is based on its interval setting and the service period that you defined in the **Create service orders** page.</span></span> <span data-ttu-id="dd969-110">Tímagluggi er skilgreindur með því að nota gildin í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="dd969-110">You define a time window by using the values in the following table.</span></span>

| <span data-ttu-id="dd969-111">Aðferð</span><span class="sxs-lookup"><span data-stu-id="dd969-111">Method</span></span> | <span data-ttu-id="dd969-112">lýsing</span><span class="sxs-lookup"><span data-stu-id="dd969-112">Description</span></span>                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd969-113">Vika</span><span class="sxs-lookup"><span data-stu-id="dd969-113">Week</span></span>   | <span data-ttu-id="dd969-114">Hægt er að færa þjónustupöntunarlínuna yfir á hvaða opinn dag í sömu vikunni og upprunalega útreiknaða dagsetningin.</span><span class="sxs-lookup"><span data-stu-id="dd969-114">The date that the service order line can be moved to any open day in the same week as the initial calculated date.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="dd969-115">Mánuður</span><span class="sxs-lookup"><span data-stu-id="dd969-115">Month</span></span>  | <span data-ttu-id="dd969-116">Hægt er að færa þjónustupöntunarlínuna yfir á hvaða opinn dag í sama mánuðinum og upprunalega útreiknaða dagsetningin.</span><span class="sxs-lookup"><span data-stu-id="dd969-116">The date that the service order line can be moved to any open day in the same month as the initial calculated date.</span></span> <span data-ttu-id="dd969-117">Útreiknuð dagsetning þjónustupöntunarlínu er til dæmis 15. febrúar, 2017.</span><span class="sxs-lookup"><span data-stu-id="dd969-117">For example, the calculated date for a service order line is February 15, 2017.</span></span> <span data-ttu-id="dd969-118">Hægt er að raða þjónustupöntunarlínu á hvaða vikudag milli 1. febrúar og 28. febrúar, 2017.</span><span class="sxs-lookup"><span data-stu-id="dd969-118">The service order line can be scheduled for any weekday between February 1 and February 28, 2017.</span></span> |
| <span data-ttu-id="dd969-119">Beinskiptur</span><span class="sxs-lookup"><span data-stu-id="dd969-119">Manual</span></span> | <span data-ttu-id="dd969-120">Hámarksfjöldi daga fyrir og eftir upprunalegu útreiknuðu dagsetninguna þar sem hægt er að færa þjónustupöntunarlínuna er skilgreint.</span><span class="sxs-lookup"><span data-stu-id="dd969-120">You define the maximum number of days before or after the initial calculated date that the service order line can be moved.</span></span>                                                                                                                                                                           |

<span data-ttu-id="dd969-121">Ef tímagluggi er ekki tilgreindur fyrir þjónustupöntunarlínu þarf þjónustupöntunarlínan sem er afleidd af þjónustusamningnum að vera á nákvæmlega sömu dagsetningu og hún var upprunalega áætluð á.</span><span class="sxs-lookup"><span data-stu-id="dd969-121">If you do not specify a time window for a service agreement line, the service order line that is derived from the service agreement must be on the exact date for which it was originally scheduled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd969-122">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="dd969-122">Related topics</span></span>

[<span data-ttu-id="dd969-123">Stofna tímaskjámyndir</span><span class="sxs-lookup"><span data-stu-id="dd969-123">Create time windows</span></span>](create-time-windows.md)

