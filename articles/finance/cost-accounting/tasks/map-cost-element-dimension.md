---
title: Varpa kostnaðareiningarvídd
description: Eftirlitsmaður kostnaðar getur notað þetta ferli til að varpa kostnaðareiningarvídd til kostnaðareiningarvíddar í MXMF-lögaðila.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 346c64ffb19e320d0babf886c15f1b46959b4f32
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178281"
---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="fa25b-103">Varpa kostnaðareiningarvídd</span><span class="sxs-lookup"><span data-stu-id="fa25b-103">Map a cost element dimension</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fa25b-104">Eftirlitsmaður kostnaðar getur notað þetta ferli til að varpa kostnaðareiningarvídd til kostnaðareiningarvíddar í MXMF-lögaðila.</span><span class="sxs-lookup"><span data-stu-id="fa25b-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="fa25b-105">Þessi skráning notar USP2-sýnigagnafyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="fa25b-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="fa25b-106">Fara í kostnaðarbókhald > Víddir > Víddir kostnaðareininga.</span><span class="sxs-lookup"><span data-stu-id="fa25b-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="fa25b-107">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="fa25b-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fa25b-108">Í þessu dæmi skal velja kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="fa25b-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="fa25b-109">Smellt er á Víddarvarpanir.</span><span class="sxs-lookup"><span data-stu-id="fa25b-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="fa25b-110">Smellt er á Skilgreina varpanir frá þessari vídd.</span><span class="sxs-lookup"><span data-stu-id="fa25b-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="fa25b-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="fa25b-111">Click New.</span></span>
6. <span data-ttu-id="fa25b-112">Sláið inn eða veldu gildi í reitnum í Til víddar.</span><span class="sxs-lookup"><span data-stu-id="fa25b-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="fa25b-113">Í þessu dæmi, velja MXMF kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="fa25b-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="fa25b-114">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="fa25b-114">Click New.</span></span>
8. <span data-ttu-id="fa25b-115">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="fa25b-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="fa25b-116">Sláið inn eða veldu gildi í reitnum Frá víddarstak.</span><span class="sxs-lookup"><span data-stu-id="fa25b-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="fa25b-117">Í þessu dæmi, velja víddarstak 606400 Síma & Fax útgjöld.</span><span class="sxs-lookup"><span data-stu-id="fa25b-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="fa25b-118">Sláið inn eða veldu gildi í reitnum í Til víddarstak.</span><span class="sxs-lookup"><span data-stu-id="fa25b-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="fa25b-119">Í þessu dæmi, velja víddarstak 6001004 Símanr.</span><span class="sxs-lookup"><span data-stu-id="fa25b-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="fa25b-120">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="fa25b-120">Click Save.</span></span>
