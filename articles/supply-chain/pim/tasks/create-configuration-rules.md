---
title: Stofna skilgreiningareglur
description: Þetta ferli stofnar skilgreiningarreglur sem hægt er að nota fyrir víddaskilgreining til að tryggja eða koma í veg fyrir tilteknar samsetningar uppskriftarlína.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9ef9f4d464fb2a61dd03914efcf7a584fe955ae9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213379"
---
# <a name="create-configuration-rules"></a><span data-ttu-id="a2c25-103">Stofna skilgreiningareglur</span><span class="sxs-lookup"><span data-stu-id="a2c25-103">Create configuration rules</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a2c25-104">Þetta ferli stofnar skilgreiningarreglur sem hægt er að nota fyrir víddaskilgreining til að tryggja eða koma í veg fyrir tilteknar samsetningar uppskriftarlína.</span><span class="sxs-lookup"><span data-stu-id="a2c25-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="a2c25-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="a2c25-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a2c25-106">Þetta er sjöunda ferli af átta sem útskýrir hvernig á að byggja upp samsetningar fyrir víddaskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="a2c25-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="a2c25-107">Fara í Upplýsingar um afurðarstjórnun > Uppskriftir efni og formúlur > Uppskriftir.</span><span class="sxs-lookup"><span data-stu-id="a2c25-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="a2c25-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a2c25-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a2c25-109">Finna og velja Uppskrift fyrir á víddaskilgreining.</span><span class="sxs-lookup"><span data-stu-id="a2c25-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="a2c25-110">Í aðgerðasvæðinu er smellt á valkostir.</span><span class="sxs-lookup"><span data-stu-id="a2c25-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="a2c25-111">Smellið á skoða Breytingu.</span><span class="sxs-lookup"><span data-stu-id="a2c25-111">Click Change view.</span></span>
5. <span data-ttu-id="a2c25-112">Smellið á skoða Haus.</span><span class="sxs-lookup"><span data-stu-id="a2c25-112">Click Header view.</span></span>
    * <span data-ttu-id="a2c25-113">Opna hausyfirlit til að fara í flýtiflipann Afbrigðaleið.</span><span class="sxs-lookup"><span data-stu-id="a2c25-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="a2c25-114">Stækka eða fella saman hlutann Afbrigðaleið.</span><span class="sxs-lookup"><span data-stu-id="a2c25-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="a2c25-115">Flýtiflipinn Skilgreiningarleið verður að vera í útvíkkuðum ham.</span><span class="sxs-lookup"><span data-stu-id="a2c25-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="a2c25-116">Smellt er á Skilgreiningarreglur.</span><span class="sxs-lookup"><span data-stu-id="a2c25-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="a2c25-117">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a2c25-117">Click New.</span></span>
9. <span data-ttu-id="a2c25-118">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="a2c25-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="a2c25-119">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="a2c25-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a2c25-120">Vörur í núgildandi skilgreiningarflokk eru birtar.</span><span class="sxs-lookup"><span data-stu-id="a2c25-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="a2c25-121">Veljið einn sem stendur fyrir skilyrði í reglunni.</span><span class="sxs-lookup"><span data-stu-id="a2c25-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="a2c25-122">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a2c25-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="a2c25-123">Veljið valkost í svæðinu aðferð.</span><span class="sxs-lookup"><span data-stu-id="a2c25-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="a2c25-124">Mögulegt er að koma á öryggisstefnu fyrir val eða afval vöru úr öðrum skilgreiningarflokki.</span><span class="sxs-lookup"><span data-stu-id="a2c25-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="a2c25-125">Í reitnum Afleiddur flokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="a2c25-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="a2c25-126">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a2c25-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="a2c25-127">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a2c25-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a2c25-128">Veljið viðeigandi afbrigðisflokkur.</span><span class="sxs-lookup"><span data-stu-id="a2c25-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="a2c25-129">Í reitnum Afleitt vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="a2c25-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="a2c25-130">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a2c25-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a2c25-131">Velja vörunúmerið sem verður annað hvort valin eða hafnað eftir þeirri aðferð sem var valið.</span><span class="sxs-lookup"><span data-stu-id="a2c25-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="a2c25-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a2c25-132">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]