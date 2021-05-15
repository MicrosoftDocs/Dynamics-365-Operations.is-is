---
title: Stofna sölupöntun fyrir skilgreinanlega afurð
description: Þetta verkefni sýnir hvernig á að nota grunnstillingarsniðmát fyrir afurð á sölupöntun.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921290"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="c0bef-103">Stofna sölupöntun fyrir skilgreinanlega afurð</span><span class="sxs-lookup"><span data-stu-id="c0bef-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c0bef-104">Þetta verkefni sýnir hvernig á að nota grunnstillingarsniðmát fyrir afurð á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="c0bef-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="c0bef-105">Þetta dæmi notar D0006 líkanið í USMF sýnigögnum fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="c0bef-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="c0bef-106">Venjulega notar sölupantanavinnsla þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="c0bef-106">Typically, a sales order processor uses this procedure.</span></span>

## <a name="create-a-sales-order"></a><span data-ttu-id="c0bef-107">Stofna sölupöntun</span><span class="sxs-lookup"><span data-stu-id="c0bef-107">Create a sales order</span></span>

1. <span data-ttu-id="c0bef-108">Farið í **Sala og markaðssetning \> Vinnusvæði \> Vinnsla og fyrirspurnir sölupantana**.</span><span class="sxs-lookup"><span data-stu-id="c0bef-108">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="c0bef-109">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="c0bef-109">Select **New**.</span></span>
1. <span data-ttu-id="c0bef-110">Veldu **Velja sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="c0bef-110">Select **Sales order**.</span></span>
1. <span data-ttu-id="c0bef-111">Í reitnum **Viðskiptavinalykill** skal velja *US-001*.</span><span class="sxs-lookup"><span data-stu-id="c0bef-111">In the **Customer account** field, select *US-001*.</span></span> 
1. <span data-ttu-id="c0bef-112">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c0bef-112">Select **OK**.</span></span>
1. <span data-ttu-id="c0bef-113">Í svæðið **Vörunúmer** veldu *D0006*.</span><span class="sxs-lookup"><span data-stu-id="c0bef-113">In the **Item number** field, select *D0006*.</span></span>
    * <span data-ttu-id="c0bef-114">Fyrir þetta verk þarf að velja samskipanlega afurð.</span><span class="sxs-lookup"><span data-stu-id="c0bef-114">For this task, you must select a configurable product.</span></span>  
1. <span data-ttu-id="c0bef-115">Veljið **Afurð og framboð**.</span><span class="sxs-lookup"><span data-stu-id="c0bef-115">Select **Product and supply**.</span></span>
1. <span data-ttu-id="c0bef-116">Veljið **Skilgreina línu**.</span><span class="sxs-lookup"><span data-stu-id="c0bef-116">Select **Configure line**.</span></span>
    * <span data-ttu-id="c0bef-117">Athugið að verði hefur verið breytt, byggt á stillingunni sem var valin, og að **Taka með kapla** svæðið er núna stillt á *Satt*.</span><span class="sxs-lookup"><span data-stu-id="c0bef-117">Note that the price has changed, based on the configuration that was selected, and that the **Include cable** field is now set to *True*.</span></span>  
    * <span data-ttu-id="c0bef-118">Athugið sjálfgefna verð- og stillingar sem eru valdar fyrir á köplum.</span><span class="sxs-lookup"><span data-stu-id="c0bef-118">Note the default price and the settings that are selected for the cable.</span></span>  
1. <span data-ttu-id="c0bef-119">Veljið **Hleðslusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="c0bef-119">Select **Load template**.</span></span>
    * <span data-ttu-id="c0bef-120">Þetta dæmi sýnir hvernig hægt er að nota sniðmát til að velja forskilgreind afbrigði.</span><span class="sxs-lookup"><span data-stu-id="c0bef-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="c0bef-121">Ef þetta ferli er notað sem verkleiðbeining og þú vilt sjá hin eigindargildin sem eru tiltæk verður þú velja hnappinn **Opna**.</span><span class="sxs-lookup"><span data-stu-id="c0bef-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must select the **Unlock** button.</span></span>  
1. <span data-ttu-id="c0bef-122">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c0bef-122">Select **OK**.</span></span>
1. <span data-ttu-id="c0bef-123">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c0bef-123">Select **OK**.</span></span>
1. <span data-ttu-id="c0bef-124">Útvíkkaðu hlutann **upplýsingar Línu**.</span><span class="sxs-lookup"><span data-stu-id="c0bef-124">Expand the **Line details** section.</span></span>
1. <span data-ttu-id="c0bef-125">Veljið flipann **Afurð**.</span><span class="sxs-lookup"><span data-stu-id="c0bef-125">Select the **Product** tab.</span></span>
    * <span data-ttu-id="c0bef-126">Afbrigði vörunnar er nú skráður undir afurðarvíddum.</span><span class="sxs-lookup"><span data-stu-id="c0bef-126">The configuration of the item is now listed under the product dimensions.</span></span>  
1. <span data-ttu-id="c0bef-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c0bef-127">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]