---
title: Stofna staðsetningarforstillingu
description: Í þessu efnisatriði er útskýrt hvernig á að stofna staðsetningarforstillingu í Dynamics 365 Supply Chain Management.
author: ShylaThompson
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 101d80216f786eb8edb687031e4deac8cc3033ff
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831027"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="314fc-103">Stofna staðsetningarforstillingu</span><span class="sxs-lookup"><span data-stu-id="314fc-103">Create a location profile</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="314fc-104">Í þessu efnisatriði er útskýrt hvernig á að stofna staðsetningarforstillingu í Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="314fc-104">This topic explains how to create a location profile in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="314fc-105">Hver staðsetning í vöruhúsi verður að hafa staðsetningarforstillingu tengda sem lýsir eiginleikum staðsetningar, t.d. hvort staðsetning heimilar blandaðar vörur.</span><span class="sxs-lookup"><span data-stu-id="314fc-105">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="314fc-106">Í þessu ferli munum við stofna forstillingu fyrir staðsetningu sem ekki þarf stýringu númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="314fc-106">In this procedure we'll create a profile for a location that doesn't require license plate control.</span></span> <span data-ttu-id="314fc-107">Við munum virkja blandaðar vörur og blandaða birgðastöðu, og leyfa reglulega talningu.</span><span class="sxs-lookup"><span data-stu-id="314fc-107">We'll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="314fc-108">Hægt er að nota þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="314fc-108">You can use this procedure in the USMF demo data company.</span></span>


1. <span data-ttu-id="314fc-109">Í skoðunarrúðunni ferðu í **Kerfi > Vöruhúsakerfi > Uppsetning > Vöruhús > Staðsetningarforstillingar**.</span><span class="sxs-lookup"><span data-stu-id="314fc-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span>
2. <span data-ttu-id="314fc-110">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="314fc-110">Select **New**.</span></span>
3. <span data-ttu-id="314fc-111">Í reitnum **Kenni staðsetningarforstillingar**.</span><span class="sxs-lookup"><span data-stu-id="314fc-111">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="314fc-112">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="314fc-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="314fc-113">Í reitinn **Staðsetningarsnið** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="314fc-113">In the **Location format** field, enter or select a value.</span></span>
6. <span data-ttu-id="314fc-114">Í reitinn **Gerð staðsetningar** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="314fc-114">In the **Location type** field, enter or select a value.</span></span>
7. <span data-ttu-id="314fc-115">Í reitinn **Auðkenni fyrir forstillingu dreifingarstjórnunar** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="314fc-115">In the **Dock management profile ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="314fc-116">Velja skal **Já** í reitnum **Leyfa blandaðar vörur**.</span><span class="sxs-lookup"><span data-stu-id="314fc-116">Select **Yes** in the **Allow mixed items** field.</span></span>
9. <span data-ttu-id="314fc-117">Velja skal **Já** í reitnum **Heimila blandaðar birgðastöður**.</span><span class="sxs-lookup"><span data-stu-id="314fc-117">Select **Yes** in the **Allow mixed inventory statuses** field.</span></span>
10. <span data-ttu-id="314fc-118">Velja skal **Já** í reitnum **Leyfa reglulega talningu**.</span><span class="sxs-lookup"><span data-stu-id="314fc-118">Select **Yes** in the **Allow cycle counting** field.</span></span>
11. <span data-ttu-id="314fc-119">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="314fc-119">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]