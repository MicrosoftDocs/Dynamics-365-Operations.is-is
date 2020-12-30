---
title: Eignir og verkbeiðnir
description: Þetta efni lýsir eignum og verkbeiðnum í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c2500a695fcffe0d60ac13b1b74cda4322b0e14
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430375"
---
# <a name="assets-and-work-orders"></a><span data-ttu-id="25e75-103">Eignir og verkbeiðnir</span><span class="sxs-lookup"><span data-stu-id="25e75-103">Assets and work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="25e75-104">Þetta efni lýsir eignum og verkbeiðnum í eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="25e75-104">This topic describes assets and work orders in Asset Management.</span></span> <span data-ttu-id="25e75-105">Eignir og verkbeiðnir eru meginhlutir eignastýringar.</span><span class="sxs-lookup"><span data-stu-id="25e75-105">Assets and work orders are the central parts of Asset Management.</span></span> <span data-ttu-id="25e75-106">*Eign* er vél eða vélarhluti sem krefst stöðugs viðhalds og þjónustu.</span><span class="sxs-lookup"><span data-stu-id="25e75-106">An *asset* is a machine or machine part that requires continuous maintenance and service.</span></span> <span data-ttu-id="25e75-107">Hægt er að búa til eignir í stigveldisskipulagi og þær geta tengst virkum stöðum.</span><span class="sxs-lookup"><span data-stu-id="25e75-107">Assets can be created in a hierarchical structure, and they can be related to functional locations.</span></span> <span data-ttu-id="25e75-108">Viðhaldsstörf geta verið áætluð á öllum stigum eignaskipulagsins.</span><span class="sxs-lookup"><span data-stu-id="25e75-108">Maintenance jobs can be planned at all levels in the asset structure.</span></span>

<span data-ttu-id="25e75-109">Ýmis gögn, svo sem vöruupplýsingar og eignaskilgreining, og nauðsynlegar viðhaldsáætlanir eru settar upp um hverja eign.</span><span class="sxs-lookup"><span data-stu-id="25e75-109">Various data, such as product information and asset specification, and required maintenance plans are set up on each asset.</span></span> <span data-ttu-id="25e75-110">Eftirfarandi mynd sýnir yfirlit yfir eignargögn og tengingu eigna við starfstegundir.</span><span class="sxs-lookup"><span data-stu-id="25e75-110">The following illustration shows an overview of asset data and the affiliation of assets to job types.</span></span> <span data-ttu-id="25e75-111">Rauður texti er notaður fyrir dæmi sem sýna arf og háð.</span><span class="sxs-lookup"><span data-stu-id="25e75-111">Red text is used for examples that show inheritance and dependencies.</span></span>

![Skýringarmynd sem sýnir eignargögn sem tengjast vinnslugerðum](media/05-overview-image.png)

<span data-ttu-id="25e75-113">Sérhver verkbeiðni er með gerð af verkbeiðni, svo fyrirbyggjandi viðhald, úrbótaviðhald eða skoðun.</span><span class="sxs-lookup"><span data-stu-id="25e75-113">Every work order has a work order type, such preventive maintenance, corrective maintenance, or inspection.</span></span> <span data-ttu-id="25e75-114">Verkbeiðnin inniheldur eitt eða fleiri störf í verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="25e75-114">The work order contains one or more work order jobs.</span></span> <span data-ttu-id="25e75-115">Sérhver starf í verkbeiðni skilgreinir starf sem þarf að framkvæma á eign og tengda starfstegund.</span><span class="sxs-lookup"><span data-stu-id="25e75-115">Every work order job defines a job that must be performed on an asset and a related job type.</span></span> <span data-ttu-id="25e75-116">Dæmi um skyldar starfstegundir eru 10.000 km, 50.000 km, 1 árs yfirferð og öryggisskoðun.</span><span class="sxs-lookup"><span data-stu-id="25e75-116">Examples of related job types include 10,000 km, 50,000 km, 1-year overhaul, and safety inspection.</span></span> <span data-ttu-id="25e75-117">Ein verkpöntun getur tengst mörgum eignum.</span><span class="sxs-lookup"><span data-stu-id="25e75-117">One work order can be related to multiple assets.</span></span>

<span data-ttu-id="25e75-118">Eftirfarandi mynd sýnir yfirlit yfir lykilgögnin í verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="25e75-118">The following illustration shows an overview of the key data in a work order.</span></span>

![Skýringarmynd sem sýnir lykilgögn í verkbeiðni](media/06-overview-image.png)

<span data-ttu-id="25e75-120">Verkbeiðnin getur verið tengt annarri verkbeiðni og starfstegundir geta innihaldið störf sem hafa náð árangri sem skapa verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="25e75-120">A work order can be related to another work order, and job types can contain succeeding jobs that create a work order.</span></span> <span data-ttu-id="25e75-121">Almennt eru engin háð á milli verkbeiðna.</span><span class="sxs-lookup"><span data-stu-id="25e75-121">In general, there are no dependencies between work orders.</span></span> <span data-ttu-id="25e75-122">Þess vegna geta þeir breytt líftímastöðum verkbeiðni og hægt er að skipuleggja þær óháð hvor annarri.</span><span class="sxs-lookup"><span data-stu-id="25e75-122">Therefore, they can change their work order lifecycle state and can be scheduled independently of each other.</span></span>

<span data-ttu-id="25e75-123">Verkbeiðnir geta verið búnar til á ýmsa vegu sem tengjast lagfærandi, fyrirbyggjandi eða viðbrögðum viðhaldi.</span><span class="sxs-lookup"><span data-stu-id="25e75-123">Work orders can be created in various ways that are related to corrective, preventive, or reactive maintenance.</span></span> <span data-ttu-id="25e75-124">Einnig er hægt að stofna verkbeiðnir handvirkt.</span><span class="sxs-lookup"><span data-stu-id="25e75-124">You can also create work orders manually.</span></span> <span data-ttu-id="25e75-125">Eftirfarandi mynd sýnir yfirlit yfir ferlið við sjálfvirka eða handvirka stofnun verkbeiðna.</span><span class="sxs-lookup"><span data-stu-id="25e75-125">The following illustration shows an overview of the process for automatic or manual creation of work orders.</span></span>

![Skýringarmynd sem sýnir sjálfvirka eða handvirka stofnun verkbeiðna](media/07-overview-image.png)

<span data-ttu-id="25e75-127">Nokkrum skrefum verður að vera lokið þegar þú vilt skipuleggja og keyra viðhaldsstörf í verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="25e75-127">Several steps must be completed when you want to schedule and run a maintenance job on a work order.</span></span> <span data-ttu-id="25e75-128">Eftirfarandi mynd sýnir yfirlit yfir vinnslu fyrir verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="25e75-128">The following illustration shows an overview of the processing for a work order.</span></span>

![Skýringarmynd sem sýnir yfirlit yfir vinnslu á verkbeiðni](media/08-overview-image.png)

> [!NOTE]
> <span data-ttu-id="25e75-130">Almennt þegar þú vinnur í Dynamics 365 Supply Chain Management og einingunni **Eignastýring** velurðu **Nýtt** til að búa til nýja skrá, velur **Breyta** til að uppfæra fyrirliggjandi skrá og þú velur **Vista** til að vista ný eða breytt gögn.</span><span class="sxs-lookup"><span data-stu-id="25e75-130">In general, when you work in Dynamics 365 Supply Chain Management and the **Asset Management** module, you select **New** to create a new record, you select **Edit** to update an existing record, and you select **Save** to save new or edited data.</span></span>
