---
title: Stofnun farmbréf fyrir afurðarsniðmát byggt á víddum
description: Fyrir þetta ferli áttu að hafa lokið fyrri 4 leiðbeiningum í þessari röð af átta skráningum.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13053dd87242963586678b46c64493feb3383c4c
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920706"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="0b252-103">Stofnun farmbréf fyrir afurðarsniðmát byggt á víddum</span><span class="sxs-lookup"><span data-stu-id="0b252-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b252-104">Fyrir þetta ferli áttu að hafa lokið fyrri 4 leiðbeiningum í þessari röð af átta skráningum.</span><span class="sxs-lookup"><span data-stu-id="0b252-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="0b252-105">Fyrstu 4 skráningar settu upp gögn sem þarf til að ljúka þessu ferli.</span><span class="sxs-lookup"><span data-stu-id="0b252-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="0b252-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="0b252-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0b252-107">Þetta verk er yfirleitt í höndum hönnuðar afurðar.</span><span class="sxs-lookup"><span data-stu-id="0b252-107">This task is typically handled by the product designer.</span></span>

## <a name="select-the-product"></a><span data-ttu-id="0b252-108">Velja afurð</span><span class="sxs-lookup"><span data-stu-id="0b252-108">Select the product</span></span>

1. <span data-ttu-id="0b252-109">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="0b252-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="0b252-110">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="0b252-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0b252-111">Finna útgefin afurðarsniðmát með tækni fyrir víddaskilgreiningu sem var stofnaður í fyrsta leiðarvísi í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="0b252-111">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
1. <span data-ttu-id="0b252-112">Á aðgerðasvæðinu skal velja **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="0b252-112">On the Action Pane, select **Engineer**.</span></span>
1. <span data-ttu-id="0b252-113">Veljið **Uppskriftarútgáfur**.</span><span class="sxs-lookup"><span data-stu-id="0b252-113">Select **BOM versions**.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="0b252-114">Stofna nýja uppskrift og uppskriftarútgáfu.</span><span class="sxs-lookup"><span data-stu-id="0b252-114">Create new BOM and BOM version</span></span>

1. <span data-ttu-id="0b252-115">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="0b252-115">Select **New**.</span></span>
1. <span data-ttu-id="0b252-116">Veljið **Uppskrift og uppskriftarútgáfa**.</span><span class="sxs-lookup"><span data-stu-id="0b252-116">Select **BOM and BOM version**.</span></span>
1. <span data-ttu-id="0b252-117">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="0b252-117">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="0b252-118">Stillingar svæðis</span><span class="sxs-lookup"><span data-stu-id="0b252-118">Setting a site</span></span>  
    * <span data-ttu-id="0b252-119">Í þessu ferli stillum við ekki inn tiltekið svæði fyrir Uppskriftina.</span><span class="sxs-lookup"><span data-stu-id="0b252-119">In this procedure we don't set a specific site for the BOM.</span></span>  
1. <span data-ttu-id="0b252-120">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0b252-120">Select **OK**.</span></span>
1. <span data-ttu-id="0b252-121">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="0b252-121">Select **New**.</span></span>
    * <span data-ttu-id="0b252-122">Í þessu ferli er bætt við fjórar línur við Uppskrift.</span><span class="sxs-lookup"><span data-stu-id="0b252-122">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="0b252-123">Tvær línur sýna valkosti fyrir kapal og tvær línur sýna valkosti fyrir geymslu.</span><span class="sxs-lookup"><span data-stu-id="0b252-123">Two lines represent cable options and two lines represent cabinet options.</span></span>  
1. <span data-ttu-id="0b252-124">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="0b252-124">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0b252-125">Í reitinn **Vörunúmer** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="0b252-125">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="0b252-126">Velja vörunúmer A0001, HDMI 6' Cables.</span><span class="sxs-lookup"><span data-stu-id="0b252-126">Select item number A0001, HDMI 6' Cables.</span></span>  
1. <span data-ttu-id="0b252-127">Sláið inn eða veldu gildi í reitnum **Afbrigðisflokkur**.</span><span class="sxs-lookup"><span data-stu-id="0b252-127">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="0b252-128">Veljið Afbirgðisflokkur kapals sem stofnuð var í leiðbeiningum 4 í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="0b252-128">Select the cable configuration group created in guide 4 in this sequence.</span></span>  
1. <span data-ttu-id="0b252-129">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="0b252-129">Select **New**.</span></span>
    * <span data-ttu-id="0b252-130">Velja vörunúmer A0002, HDMI 12' Cables.</span><span class="sxs-lookup"><span data-stu-id="0b252-130">Select item number A0002, HDMI 12' Cables.</span></span>  
1. <span data-ttu-id="0b252-131">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="0b252-131">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0b252-132">Í reitinn **Vörunúmer** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="0b252-132">In the **Item number** field, enter or select a value.</span></span>
1. <span data-ttu-id="0b252-133">Sláið inn eða veldu gildi í reitnum **Afbrigðisflokkur**.</span><span class="sxs-lookup"><span data-stu-id="0b252-133">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="0b252-134">Veljið aftur Afbirgðisflokkur kapals.</span><span class="sxs-lookup"><span data-stu-id="0b252-134">Select the cable configuration group again.</span></span>  
1. <span data-ttu-id="0b252-135">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="0b252-135">Select **New**.</span></span>
1. <span data-ttu-id="0b252-136">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="0b252-136">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0b252-137">Í reitinn **Vörunúmer** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="0b252-137">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="0b252-138">Velja vörunúmer D0002 Cabinet.</span><span class="sxs-lookup"><span data-stu-id="0b252-138">Select item number D0002 Cabinet.</span></span>  
1. <span data-ttu-id="0b252-139">Sláið inn eða veldu gildi í reitnum **Afbrigðisflokkur**.</span><span class="sxs-lookup"><span data-stu-id="0b252-139">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="0b252-140">Veljið afbrigðaflokki xabinet fyrir þessa uppskriftarlínu.</span><span class="sxs-lookup"><span data-stu-id="0b252-140">Select the cabinet configuration group for this BOM line.</span></span>  
1. <span data-ttu-id="0b252-141">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="0b252-141">Select **New**.</span></span>
1. <span data-ttu-id="0b252-142">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="0b252-142">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0b252-143">Í reitinn **Vörunúmer** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="0b252-143">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="0b252-144">Veljið vörunúmer M0007 StandardCabinet sem síðustu uppskriftarlínu.</span><span class="sxs-lookup"><span data-stu-id="0b252-144">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
1. <span data-ttu-id="0b252-145">Sláið inn eða veldu gildi í reitnum **Afbrigðisflokkur**.</span><span class="sxs-lookup"><span data-stu-id="0b252-145">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="0b252-146">Veljið afbrigðaflokk Cabinet fyrir síðustu uppskriftarlínu.</span><span class="sxs-lookup"><span data-stu-id="0b252-146">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="0b252-147">Samþykkja og virkja</span><span class="sxs-lookup"><span data-stu-id="0b252-147">Approve and activate</span></span>

1. <span data-ttu-id="0b252-148">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0b252-148">Close the page.</span></span>
1. <span data-ttu-id="0b252-149">Veljið **Samþykkja**.</span><span class="sxs-lookup"><span data-stu-id="0b252-149">Select **Approve**.</span></span>
1. <span data-ttu-id="0b252-150">Sláið inn eða veldu gildi í reitnum **Samþykki eftir**.</span><span class="sxs-lookup"><span data-stu-id="0b252-150">In the **Approved by** field, enter or select a value.</span></span>
1. <span data-ttu-id="0b252-151">Veldu *Já* í reitnum **Viltu einnig að samþykkja uppskriftina?**.</span><span class="sxs-lookup"><span data-stu-id="0b252-151">Select *Yes* in the **Do you also want to approve the bill of materials?** field.</span></span>
1. <span data-ttu-id="0b252-152">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0b252-152">Select **OK**.</span></span>
1. <span data-ttu-id="0b252-153">Veldu **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="0b252-153">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]