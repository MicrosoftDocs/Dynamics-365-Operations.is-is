---
title: Losa fasta eign sem rýrnun
description: Umræðuefnið lýsir ferli úthlutunar á losunarfærslum fyrir fasta eign sem var losuð sem rýrnun.
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: de105e061712540fc8e3d720a65c029f865b8948
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187292"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a><span data-ttu-id="93f31-103">Losa fasta eign sem rýrnun</span><span class="sxs-lookup"><span data-stu-id="93f31-103">Dispose of a fixed asset as scrap</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="93f31-104">Umræðuefnið lýsir ferli úthlutunar á losunarfærslum fyrir fasta eign sem var losuð sem rýrnun.</span><span class="sxs-lookup"><span data-stu-id="93f31-104">The topic describes the process of eliminating transactions for a fixed asset that was disposed of as scrap.</span></span> <span data-ttu-id="93f31-105">Færslutegundir sem hægt er að losa eru m.a. yfirtaka eignar og uppsafnaðar afskriftarfærslur og aðrar færslur fastra eigna.</span><span class="sxs-lookup"><span data-stu-id="93f31-105">The transaction types that can be eliminated include an asset's acquisition and accumulated depreciation transactions and other fixed asset transactions.</span></span> <span data-ttu-id="93f31-106">Losun þessara færslna hefur áhrif á efnahagsreikninga, svo sem aðlögun yfirtöku, afskriftarleiðréttingu, endurmat, niðurfærslu og niðurfærslu reikninga.</span><span class="sxs-lookup"><span data-stu-id="93f31-106">Elimination of these transactions affects balance sheet accounts, such as acquisition adjustment, depreciation adjustment, revaluation, write-up, and write-down accounts.</span></span>

| <span data-ttu-id="93f31-107">Færsla</span><span class="sxs-lookup"><span data-stu-id="93f31-107">Transaction</span></span>                                         | <span data-ttu-id="93f31-108">Debet (Dr.)</span><span class="sxs-lookup"><span data-stu-id="93f31-108">Debit (Dr.)</span></span> | <span data-ttu-id="93f31-109">Kredit (Cr.)</span><span class="sxs-lookup"><span data-stu-id="93f31-109">Credit (Cr.)</span></span> |
|-----------------------------------------------------|-------------|--------------|
| <span data-ttu-id="93f31-110">Uppsöfnuð afskrift Dr.</span><span class="sxs-lookup"><span data-stu-id="93f31-110">Dr. Accumulated depreciation</span></span>                        | <span data-ttu-id="93f31-111">X</span><span class="sxs-lookup"><span data-stu-id="93f31-111">X</span></span>           |              |
| <span data-ttu-id="93f31-112">Hagnaður/tap Cr. fastra eigna</span><span class="sxs-lookup"><span data-stu-id="93f31-112">Cr. Fixed assets gain/loss</span></span>                          |             | <span data-ttu-id="93f31-113">X</span><span class="sxs-lookup"><span data-stu-id="93f31-113">X</span></span>            |
| <span data-ttu-id="93f31-114">Hagnaður/tap Dr. fastra eigna</span><span class="sxs-lookup"><span data-stu-id="93f31-114">Dr. Fixed assets gain/loss</span></span>                          | <span data-ttu-id="93f31-115">X</span><span class="sxs-lookup"><span data-stu-id="93f31-115">X</span></span>           |              |
| <span data-ttu-id="93f31-116">Bókunarlykill Cr. eignakaupa</span><span class="sxs-lookup"><span data-stu-id="93f31-116">Cr. Fixed asset acquisition account</span></span>                 |             | <span data-ttu-id="93f31-117">X</span><span class="sxs-lookup"><span data-stu-id="93f31-117">X</span></span>            |
| <span data-ttu-id="93f31-118">Hagnaður/tap Dr. fastra eigna (bókfært virði \[BNV\])</span><span class="sxs-lookup"><span data-stu-id="93f31-118">Dr. Fixed assets gain/loss (net book value \[NBV\])</span></span> | <span data-ttu-id="93f31-119">X</span><span class="sxs-lookup"><span data-stu-id="93f31-119">X</span></span>           |              |
| <span data-ttu-id="93f31-120">Hagnaður/tap Cr. fastra eigna (BNV)</span><span class="sxs-lookup"><span data-stu-id="93f31-120">Cr. Fixed assets gain/loss (NBV)</span></span>                    |             | <span data-ttu-id="93f31-121">X</span><span class="sxs-lookup"><span data-stu-id="93f31-121">X</span></span>            |

> [!NOTE]
> <span data-ttu-id="93f31-122">Við mælum með að þú vinnur náið með fjármálastjóra fyrirtækisins (fjármálastjóra) eða stjórnanda til að bera kennsl á réttu reikningana sem nota ætti fyrir hverja tegund viðskipta og einnig til að sannreyna að förgunarferlið og viðskiptin sem það býr uppfæra reikninga rétt.</span><span class="sxs-lookup"><span data-stu-id="93f31-122">We recommend that you work closely with your company's chief financial officer (CFO) or controller to identify the correct accounts that should be used for each transaction type, and also to verify that the disposal process and the transactions that it generates update those accounts correctly.</span></span>

<span data-ttu-id="93f31-123">Áður en þú losar fasta eign sem rýrnun verðurðu að stofna bókhald sem er tengt við yfirtökuverðmæti eignarinnar, afskriftir yfirstandandi árs, afskriftir fyrri ára og BNV eignarinnar.</span><span class="sxs-lookup"><span data-stu-id="93f31-123">Before you dispose of a fixed asset as scrap, you must create ledger accounts that are associated with the asset's acquisition value, depreciation for the current year, depreciation for previous years, and the asset's NBV.</span></span> <span data-ttu-id="93f31-124">Færslugerðir fastra eigna eru skráðar á síðunni **Bókunarforstillingar fastra eigna**.</span><span class="sxs-lookup"><span data-stu-id="93f31-124">The fixed asset transaction types are listed on the **Fixed assets posting profile** page.</span></span> <span data-ttu-id="93f31-125">Farðu í **Fastar eignir \> Uppsetning \> Bókunarforstillingar fastra eigna**, og síðan á flýtiflipann **Losun**, veldu **Rýrnun** í reitnum fyrir ofan hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="93f31-125">Go to **Fixed assets \> Setup \> Fixed asset posting profiles**, and then, on the **Disposal** FastTab, select **Scrap** in the field above the grid.</span></span> <span data-ttu-id="93f31-126">Eftirfarandi mynd sýnir lista yfir færslugerðir fastra eigna á síðunni **Bókunarforstillingar fastra eigna**.</span><span class="sxs-lookup"><span data-stu-id="93f31-126">The following illustration shows the list of fixed asset transaction types on the **Fixed asset posting profiles** page.</span></span>


<span data-ttu-id="93f31-127">[![Eign lostuð sem rýrnun, mynd 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span><span class="sxs-lookup"><span data-stu-id="93f31-127">[![Disposing of an asset as scap, Fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span></span>

<span data-ttu-id="93f31-128">Fyrir eftirfarandi dæmi var föst eign keypt þann 1. janúar 2018 og hún verður úrelt þann 31. mars 2019.</span><span class="sxs-lookup"><span data-stu-id="93f31-128">For the following example, a fixed asset was acquired on January 1, 2018, and it will be scrapped on March 31, 2019.</span></span>

- <span data-ttu-id="93f31-129">**Kaupverð:** 24.000,00 Bandaríkjadalir (USD)</span><span class="sxs-lookup"><span data-stu-id="93f31-129">**Acquisition price:** 24,000.00 US dollars (USD)</span></span>
- <span data-ttu-id="93f31-130">**Líftími:** Tvö ár</span><span class="sxs-lookup"><span data-stu-id="93f31-130">**Service life:** Two years</span></span>
- <span data-ttu-id="93f31-131">**Afskriftaraðferð:** Línuleg á líftíma</span><span class="sxs-lookup"><span data-stu-id="93f31-131">**Depreciation method:** Straight line service life</span></span>
- <span data-ttu-id="93f31-132">**Afskriftarfjárhæð:** 1,000.00 USD á mánuði</span><span class="sxs-lookup"><span data-stu-id="93f31-132">**Depreciation amount:** 1,000.00 USD per month</span></span>

<span data-ttu-id="93f31-133">BNV af fastri eign er reiknað með því að nota eftirfarandi formúlu:</span><span class="sxs-lookup"><span data-stu-id="93f31-133">The NBV of a fixed asset is calculated by using the following formula:</span></span>

<span data-ttu-id="93f31-134">Nettó bókað virði = yfirtökuverð - afskriftir</span><span class="sxs-lookup"><span data-stu-id="93f31-134">Net book value = Acquisition price – Depreciation</span></span>

<span data-ttu-id="93f31-135">Í þessu dæmi var fasta eignin keypt og var afskrifuð í 15 mánuði, frá janúar 2018 til mars 2019.</span><span class="sxs-lookup"><span data-stu-id="93f31-135">In this example, the fixed asset was acquired and was depreciated for 15 months, from January 2018 through March 2019.</span></span> <span data-ttu-id="93f31-136">Þess vegna er BNV eignarinnar 9,000.00 USD (24.000,00 USD - 15.000,00 USD).</span><span class="sxs-lookup"><span data-stu-id="93f31-136">Therefore, the asset's NBV is 9,000.00 USD (24,000.00 USD – 15,000.00 USD).</span></span>

<span data-ttu-id="93f31-137">[![Dæmi um afskriftir eigna](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span><span class="sxs-lookup"><span data-stu-id="93f31-137">[![Fixed asset depreciation example](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span></span>


<span data-ttu-id="93f31-138">Til að búa til losunarfærslubók skaltu fara í **Fastar eignir \>Færslur í færslubók \> Eignabók** og veldu síðan **Línur** í aðgerðaglugganum.</span><span class="sxs-lookup"><span data-stu-id="93f31-138">To create a disposal journal, go to **Fixed assets \> Journal entries \> Fixed assets journal**, and then, on the Action Pane, select **Lines**.</span></span> <span data-ttu-id="93f31-139">Veldu **Losun - rýrnun** og veldu síðan kenni fastra eigna.</span><span class="sxs-lookup"><span data-stu-id="93f31-139">Select **Disposal – scrap**, and then select a fixed asset ID.</span></span> <span data-ttu-id="93f31-140">Til að losa eignina að fullu skaltu hvorki færa gildi í reitinn **Debet** né reitinn **Kredit**.</span><span class="sxs-lookup"><span data-stu-id="93f31-140">To fully dispose of the asset, don't enter a value in either the **Debit** field or the **Credit** field.</span></span>

<span data-ttu-id="93f31-141">[![Eignabók](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span><span class="sxs-lookup"><span data-stu-id="93f31-141">[![Fixed assets journal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span></span>

<span data-ttu-id="93f31-142">Rýrnunarfærsla losunar á föstum eignum breytir reitagildi eignabókar á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="93f31-142">The fixed asset disposal scrap transaction changes the field values for the fixed asset book in the following ways:</span></span>

- <span data-ttu-id="93f31-143">Í hlutanum **Staða** er reiturinn **Staða** uppfærður í **Rýrnað**.</span><span class="sxs-lookup"><span data-stu-id="93f31-143">In the **Balance** section, the **Status** field is updated to **Scrapped**.</span></span>
- <span data-ttu-id="93f31-144">Í hlutanum **Útgáfa** er reiturinn **Losunardagur** stilltur á dagsetninguna þegar eignin var rýrð.</span><span class="sxs-lookup"><span data-stu-id="93f31-144">In the **Issue** section, the **Disposal date** field is set to the date when the asset was scrapped.</span></span>

<span data-ttu-id="93f31-145">[![Ítarupplýsingar eignabókar](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span><span class="sxs-lookup"><span data-stu-id="93f31-145">[![Fixed assets journal detail](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span></span>

<span data-ttu-id="93f31-146">Eftirfarandi mynd sýnir stöðu fastra eigna.</span><span class="sxs-lookup"><span data-stu-id="93f31-146">The following illustration shows the fixed asset balance.</span></span>

<span data-ttu-id="93f31-147">[![Staða fastra eigna](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span><span class="sxs-lookup"><span data-stu-id="93f31-147">[![Fixed asset balance](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span></span>

<span data-ttu-id="93f31-148">Eftirfarandi mynd sýnir fylgiskjalið sem er sent.</span><span class="sxs-lookup"><span data-stu-id="93f31-148">The following illustration shows the voucher that is posted.</span></span>

<span data-ttu-id="93f31-149">[![Bókað nettóvirði](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span><span class="sxs-lookup"><span data-stu-id="93f31-149">[![Net book value](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span></span>
