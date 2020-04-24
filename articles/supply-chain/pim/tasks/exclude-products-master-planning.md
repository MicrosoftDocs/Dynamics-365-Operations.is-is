---
title: Búa til lífferlisstöðu afurðar til að útiloka afurðir frá aðaláætlanagerð
description: Þessi ferli sýnir hvernig á að stofna nýja lífferlisstöðu afurðar sem útilokar vörur úr aðaláætlanagerð og úrreikningi á uppskriftarstigi.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 999702b9a14965271b1ed350cda752e715a22a25
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203596"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="9612e-103">Búa til lífferlisstöðu afurðar til að útiloka afurðir frá aðaláætlanagerð</span><span class="sxs-lookup"><span data-stu-id="9612e-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9612e-104">Þessi ferli sýnir hvernig á að stofna nýja lífferlisstöðu afurðar sem útilokar vörur úr aðaláætlanagerð og úrreikningi á uppskriftarstigi.</span><span class="sxs-lookup"><span data-stu-id="9612e-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="9612e-105">Stofna úrelda stöðu</span><span class="sxs-lookup"><span data-stu-id="9612e-105">Create an obsolete state</span></span>
1. <span data-ttu-id="9612e-106">Fara í Upplýsingastjórnun afurðar > Uppsetning > Lífferilsstaða afurðar.</span><span class="sxs-lookup"><span data-stu-id="9612e-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="9612e-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="9612e-107">Click New.</span></span>
3. <span data-ttu-id="9612e-108">Í reitinn Staða skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9612e-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="9612e-109">Velja skal Nei í reitinum Er virk fyrir áætlunargerð.</span><span class="sxs-lookup"><span data-stu-id="9612e-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="9612e-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="9612e-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="9612e-111">Tengja úrelta stöðu á útgefina afurð</span><span class="sxs-lookup"><span data-stu-id="9612e-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="9612e-112">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9612e-112">Close the page.</span></span>
2. <span data-ttu-id="9612e-113">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="9612e-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="9612e-114">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="9612e-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9612e-115">Til dæmis skal sía svæðið Leitarheiti með gildinu „M00“.</span><span class="sxs-lookup"><span data-stu-id="9612e-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="9612e-116">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="9612e-116">Click Edit.</span></span>
5. <span data-ttu-id="9612e-117">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="9612e-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="9612e-118">Sláið inn eða veljið gildi í reitnum Lífferilsstaða afurðar.</span><span class="sxs-lookup"><span data-stu-id="9612e-118">In the Product lifecycle state field, enter or select a value.</span></span>

