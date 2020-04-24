---
title: Stofna sniðmátsuppskrift
description: Þú getur búið til sniðmátsuppskrift með því að nota ýmsar aðferðir.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 815b6b726e9a76a9294995bc5689b030cf623ec0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202584"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="0ad1c-103">Stofna sniðmátsuppskrift</span><span class="sxs-lookup"><span data-stu-id="0ad1c-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0ad1c-104">Hægt er að stofna sniðmátsuppskrift með hvaða af eftirfarandi aðferðum.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="0ad1c-105">Fyrir alla aðferðir eru **Frá dagsetning** og **Til dagsetning** reitir valfrjálst og aðeins til upplýsinga.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="0ad1c-106">Stofna sniðmátsuppskrift handvirkt</span><span class="sxs-lookup"><span data-stu-id="0ad1c-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="0ad1c-107">Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Þjónustuhlutir** \> **Sniðmátsuppskriftir**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="0ad1c-108">Ýttu á CTRL + N til að opna **Búa til sniðmátsuppskrift** skjámynd.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="0ad1c-109">Undir **Afrita uppskriftarlínur frá tilvísun**, veldu **Handvirkt** valkostinn.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="0ad1c-110">Í **Vörunúmer** reitnum, sláðu in vöru af gerðinni **Uppskrift**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="0ad1c-111">Í **Heiti** reitinn, slá inn heiti fyrir sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="0ad1c-112">Í **Frá dagsetningu** og **Til dagsetningar** reitina, slá inn dagsetningu millibili þar sem sniðmátsuppskriftin er virkt.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="0ad1c-113">Smelltu á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-113">Click **OK**.</span></span>

<span data-ttu-id="0ad1c-114">Ný, tóm sniðmátsuppskrift er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="0ad1c-115">Stofna sniðmátsuppskrift sem byggð er á annarri sniðmátsuppskrift</span><span class="sxs-lookup"><span data-stu-id="0ad1c-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="0ad1c-116">Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Þjónustuhlutir** \> **Sniðmátsuppskriftir**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="0ad1c-117">Ýttu á CTRL + N til að opna **Búa til sniðmátsuppskrift** skjámynd.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="0ad1c-118">Undir **Afrita uppskriftarlínur frá tilvísun**, veldu **Sniðmátsuppskrift** valkostinn.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="0ad1c-119">Í **Tilvísunarnúmer** reitinn, skal velja fyrirliggjandi sniðmátsuppskrift til að afrita á nýja sniðmátsuppskrift þína.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="0ad1c-120">Í **Heiti** reitinn, slá inn heiti fyrir sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="0ad1c-121">Í **Frá dagsetningu** og **Til dagsetningar** reitina, slá inn dagsetningu millibili þar sem sniðmátsuppskriftin er virkt.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="0ad1c-122">Smelltu á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-122">Click **OK**.</span></span>

<span data-ttu-id="0ad1c-123">Ný sniðmátsuppskrift er stofnuð með því að notast við línur sem samsvara línunum í upprunalegu sniðmátsuppskriftinni.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="0ad1c-124">Stofna sniðmátsuppskrift sem byggð er á uppskriftarvöru</span><span class="sxs-lookup"><span data-stu-id="0ad1c-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="0ad1c-125">Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Þjónustuhlutir** \> **Sniðmátsuppskriftir**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="0ad1c-126">Ýttu á CTRL + N til að opna **Búa til sniðmátsuppskrift** skjámynd.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="0ad1c-127">Undir **Afrita uppskriftarlínur frá tilvísun**, veldu **Uppskrift**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="0ad1c-128">Í **Tilvísunarnúmer** reitur, velja uppskriftar útgáfu.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="0ad1c-129">Vara af gerðinni Uppskrift er afrituð í **Vörunúmer**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="0ad1c-130">Í **Heiti** reitinn, slá inn heiti fyrir sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="0ad1c-131">Í **Frá dagsetningu** og **Til dagsetningar** reitina, slá inn dagsetningu millibili þar sem sniðmátsuppskriftin er virkt.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="0ad1c-132">Smelltu á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-132">Click **OK**.</span></span>

<span data-ttu-id="0ad1c-133">Nýtt sniðmátsuppskrift er búið til með því að nota línur sem samsvara línunum í uppskriftinni sem er skráð í **Uppskriftir**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="0ad1c-134">Stofna sniðmátsuppskrift sem byggð er á framleiðsluuppskrift</span><span class="sxs-lookup"><span data-stu-id="0ad1c-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="0ad1c-135">Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Þjónustuhlutir** \> **Sniðmátsuppskriftir**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="0ad1c-136">Ýttu á CTRL + N til að opna **Búa til sniðmátsuppskrift** skjámynd.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="0ad1c-137">Undir **Afrita uppskriftarlínur frá tilvísun**, veldu **Framleiðsla**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="0ad1c-138">Í **Tilvísunarnúmer** reitnum, velja framleiðsluuppskrift.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="0ad1c-139">Í **Heiti** reitinn, slá inn heiti fyrir sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="0ad1c-140">Í **Frá dagsetningu** og **Til dagsetningar** reitina, slá inn dagsetningu millibili þar sem sniðmátsuppskriftin er virkt.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="0ad1c-141">Smelltu á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-141">Click **OK**.</span></span>

<span data-ttu-id="0ad1c-142">Nýtt sniðmátsuppskrift er búið til með því að nota línur sem samsvara línunum í Uppskrift sem er skráð í **Uppskrift**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ad1c-143">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0ad1c-143">See also</span></span>

[<span data-ttu-id="0ad1c-144">Uppskriftir sniðmáts</span><span class="sxs-lookup"><span data-stu-id="0ad1c-144">Template BOMs</span></span>](template-boms.md)

  


