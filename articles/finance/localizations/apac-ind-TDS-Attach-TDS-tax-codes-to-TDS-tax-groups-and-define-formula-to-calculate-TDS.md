---
title: Hengja TDS-skattkóða við TDS-skattflokka og skilgreina formúluna fyrir útreikning TDS
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp TDS-skattflokka og hengja TDS-skattkóða við TDS-skattflokka. Til að reikna út TDS fyrir TDS-skattflokk þarf að skilgreina formúluna fyrir TDS-skattkóða sem eru hengdir við hana.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023337"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a><span data-ttu-id="e3a36-104">Hengja TDS-skattkóða við TDS-skattflokka og skilgreina formúluna fyrir útreikning TDS</span><span class="sxs-lookup"><span data-stu-id="e3a36-104">Attach TDS tax codes to TDS tax groups and define the formula for calculating TDS</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3a36-105">Í þessu efnisatriði er útskýrt hvernig á að setja upp TDS-skattflokka og hengja TDS-skattkóða við TDS-skattflokka.</span><span class="sxs-lookup"><span data-stu-id="e3a36-105">This topic explains how to set up Tax Deducted at Source (TDS) tax groups and attach TDS tax codes to TDS tax groups.</span></span> <span data-ttu-id="e3a36-106">Til að reikna út TDS fyrir TDS-skattflokk þarf að skilgreina formúluna fyrir TDS-skattkóða sem eru hengdir við hana.</span><span class="sxs-lookup"><span data-stu-id="e3a36-106">To calculate TDS for a TDS tax group, you must define the formula for TDS tax codes that are attached to it.</span></span>

<span data-ttu-id="e3a36-107">Fylgið þessum skrefum til að setja upp TDS-skattflokk, hengja TDS-skattkóða við hann, og skilgreina formúluna fyrir útreikning TDS.</span><span class="sxs-lookup"><span data-stu-id="e3a36-107">Follow these steps to set up a TDS tax group, attach TDS tax codes to it, and define the formula for calculating TDS.</span></span>

1. <span data-ttu-id="e3a36-108">Farið í **Skattur \> Óbeinir skattar \> Staðgreiðsluskattur \> Staðgreiðsluskattsflokkar**.</span><span class="sxs-lookup"><span data-stu-id="e3a36-108">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax groups**.</span></span>

    <span data-ttu-id="e3a36-109">[![Síða staðgreiðsluskattsflokka](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span><span class="sxs-lookup"><span data-stu-id="e3a36-109">[![Withholding tax groups page](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span></span>

2. <span data-ttu-id="e3a36-110">Á aðgerðasvæðinu skal velja **Nýtt** til að stofna staðgreiðsluskattsflokk fyrir TDS og færa inn nauðsynlegar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="e3a36-110">On the Action Pane, select **New** to create a withholding tax group for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="e3a36-111">Í reitnum **Skattgerð** skal velja **TDS**.</span><span class="sxs-lookup"><span data-stu-id="e3a36-111">In the **Tax type** field, select **TDS**.</span></span>
4. <span data-ttu-id="e3a36-112">Í flýtiflipanum **Uppsetning** skal velja **Bæta við** til að stofna línu.</span><span class="sxs-lookup"><span data-stu-id="e3a36-112">On the **Setup** FastTab, select **Add** to create a line.</span></span>
5. <span data-ttu-id="e3a36-113">Í reitnum **Staðgreiðsluskattskóði** skal velja TDS-skattkóða fyrir TDS-skattflokkinn.</span><span class="sxs-lookup"><span data-stu-id="e3a36-113">In the **Withholding tax code** field, select the TDS tax code for the TDS tax group.</span></span> <span data-ttu-id="e3a36-114">Reiturinn **Heiti staðgreiðsluskatts** sýnir heiti TDS-skattkóðans og reiturinn **Gildi** sýnir gildið.</span><span class="sxs-lookup"><span data-stu-id="e3a36-114">The **Withholding tax name** field shows the name of the TDS tax code, and the **Value** field shows the value.</span></span>
6. <span data-ttu-id="e3a36-115">Til að hunsa mörkin og undantekningarmörkin sem eru skilgreind fyrir TDS-skattþáttinn sem er hengdur við TDS-skattkóðann í TDS-færslum skal velja gátreitinn **Horfa fram hjá mörkum**.</span><span class="sxs-lookup"><span data-stu-id="e3a36-115">To ignore the threshold limit and exception threshold limit that are defined for the TDS tax component that is attached to the TDS tax code in TDS transactions, select the **Overlook threshold** check box.</span></span>
7. <span data-ttu-id="e3a36-116">Til að koma í veg fyrir að skattflokkurinn verði reiknaður út í færslum skal velja gátreitinn **Undanþága**.</span><span class="sxs-lookup"><span data-stu-id="e3a36-116">To prevent the tax group from being calculated in transactions, select the **Exempt** check box.</span></span>
8. <span data-ttu-id="e3a36-117">Á aðgerðasvæðinu skal velja **Hönnuður** til að opna formúluhönnuðinn svo þú getir skilgreint formúluna fyrir útreikning á TDS fyrir TDS-skattflokkinn.</span><span class="sxs-lookup"><span data-stu-id="e3a36-117">On the Action Pane, select **Designer** to open the formula designer, so that you can define the formula for calculating TDS for the TDS tax group.</span></span> <span data-ttu-id="e3a36-118">Á síðunni **Hönnuður** sýnir flipinn **Skattar** TDS-skattkóðana sem hafa verið valdir fyrir TDS-skattflokkinn.</span><span class="sxs-lookup"><span data-stu-id="e3a36-118">On the **Designer** page, the **Taxes** tab shows the TDS tax codes that have been selected for the TDS tax group.</span></span>

    <span data-ttu-id="e3a36-119">[![Hönnuðarsíða](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span><span class="sxs-lookup"><span data-stu-id="e3a36-119">[![Designer page](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span></span>

9. <span data-ttu-id="e3a36-120">Í flipanum **Útreikningur** skal velja **Alt+N** til að stofna línu.</span><span class="sxs-lookup"><span data-stu-id="e3a36-120">On the **Calculation** tab, select **Alt+N** to create a line.</span></span> <span data-ttu-id="e3a36-121">Reiturinn **Kenni** sýnir sjálfkrafa myndað forgangskenni fyrir TDS-útreikning.</span><span class="sxs-lookup"><span data-stu-id="e3a36-121">The **ID** field shows the automatically generated priority ID for TDS calculation.</span></span>
10. <span data-ttu-id="e3a36-122">Í reitnum **Skattkóði** skal velja TDS-skattkóðann til að skilgreina formúluna fyrir hann.</span><span class="sxs-lookup"><span data-stu-id="e3a36-122">In the **Tax code** field, select the TDS tax code to define the formula for.</span></span> <span data-ttu-id="e3a36-123">Allir TDS-skattkóðarnir sem hafa verið valdir fyrir TDS-skattflokkinn er hægt að velja í þessum reit.</span><span class="sxs-lookup"><span data-stu-id="e3a36-123">All the TDS tax codes that have been selected for the TDS tax group are available for selection in this field.</span></span>
11. <span data-ttu-id="e3a36-124">Í reitnum **Skattskyldur stofn** skal velja stofninn fyrir útreikning á TDS:</span><span class="sxs-lookup"><span data-stu-id="e3a36-124">In the **Taxable basis** field, select the basis for calculating TDS:</span></span>

    - <span data-ttu-id="e3a36-125">**Brúttóupphæð** – Reiknið út TDS út frá brúttóupphæð færslunnar (þ.e. reikningsupphæðinni) með því að nota útreikningssegðina sem er skilgreind fyrir skattkóðann.</span><span class="sxs-lookup"><span data-stu-id="e3a36-125">**Gross amount** – Calculate TDS based on the gross transaction amount (that is, the invoice amount) by using the calculation expression that is defined for the tax code.</span></span>
    - <span data-ttu-id="e3a36-126">**Án brúttóupphæðar** – Reiknið út TDS út frá útreikningssegðinni sem skilgreind er fyrir skattkóðann.</span><span class="sxs-lookup"><span data-stu-id="e3a36-126">**Excl Gross amount** – Calculate TDS based on the calculation expression that is defined for the tax code.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e3a36-127">Ekki er hægt að stilla reitinn **Skattskyldur stofn** á **Án brúttóupphæðar** fyrir TDS-skattkóðann sem er með forgangskenni upp á **1**.</span><span class="sxs-lookup"><span data-stu-id="e3a36-127">The **Taxable basis** field can't be set to **Excl Gross amount** for the TDS tax code that has a priority ID of **1**.</span></span>

12. <span data-ttu-id="e3a36-128">TDS-útreikningurinn byggir á formúlunni sem er skilgreind í reitnum **Segð útreiknings** fyrir hvern skattkóða sem er hengdur við TDS-skattflokkinn.</span><span class="sxs-lookup"><span data-stu-id="e3a36-128">The TDS calculation is based on the formula that is defined in the **Calculation expression** field for each tax code that is attached to the TDS tax group.</span></span> <span data-ttu-id="e3a36-129">Veljið hnappinn fyrir plúsmerkið (**+**), mínusmerkið (**-**), margföldunarmerkið (**\**_) eða deilingarmerkið (_*/**) til að færa inn útreikningssegðina fyrir valinn TDS-skattkóða í reitnum **Segð útreiknings**.</span><span class="sxs-lookup"><span data-stu-id="e3a36-129">Select the plus sign (**+**), minus sign (**-**), multiplication sign (**\**_), or division sign (_*/**) button to enter the calculation expression for the selected TDS tax code in the **Calculation expression** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e3a36-130">Ekki er hægt að skilgreina neina útreikningssegð fyrir TDS-skattkóða sem er með forgangskennið **1**.</span><span class="sxs-lookup"><span data-stu-id="e3a36-130">No calculation expression can be defined for the TDS tax code that has a priority ID of **1**.</span></span>

13. <span data-ttu-id="e3a36-131">Til að skilgreina segð útreiknings fyrir TDS-skattkóðann í reitnum **Segð útreiknings** skal bæta við TDS-skattkóðum sem eru í boði í flipanum **Skattar**. Til að bæta við TDS-skattkóðum í reitinn **Segð útreiknings** er hægt að nota einhverja af eftirfarandi aðferðum:</span><span class="sxs-lookup"><span data-stu-id="e3a36-131">To define the calculation expression for the TDS tax code in the **Calculation expression** field, add TDS tax codes that are available on the **Taxes** tab. To add TDS tax codes in the **Calculation expression** field, you can use any of the following methods:</span></span>

    - <span data-ttu-id="e3a36-132">Dragið nauðsynlegan skattkóða úr flipanum **Skattar** og yfir í reitinn **Segð útreiknings**.</span><span class="sxs-lookup"><span data-stu-id="e3a36-132">Drag the required tax code from the **Taxes** tab to the **Calculation expression** field.</span></span>
    - <span data-ttu-id="e3a36-133">Pikkið tvisvar (eða tvísmellið) á nauðsynlegan skattkóða í flipanum **Skattar**.</span><span class="sxs-lookup"><span data-stu-id="e3a36-133">Double-tap (or double-click) the required tax code on the **Taxes** tab.</span></span>
    - <span data-ttu-id="e3a36-134">Veljið og haldið (eða hægrismellið á) nauðsynlegum skattkóða í flipanum **Skattar** og veljið síðan **Bæta við skattkóða**.</span><span class="sxs-lookup"><span data-stu-id="e3a36-134">Select and hold (or right-click) the required tax code on the **Taxes** tab, and then select **Add tax code**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e3a36-135">Setjið inn segð útreiknings á undan hverjum TDS-skattkóða.</span><span class="sxs-lookup"><span data-stu-id="e3a36-135">Insert a calculation expression before each TDS tax code.</span></span> <span data-ttu-id="e3a36-136">TDS-skattkóðarnir sem hefur verið bætt við segð útreiknings birtast innan sviga (\[...\]).</span><span class="sxs-lookup"><span data-stu-id="e3a36-136">The TDS tax codes that have been added to the calculation expression appear in brackets (\[...\]).</span></span>

14. <span data-ttu-id="e3a36-137">Til að hreinsa segð útreiknings sem er skilgreind fyrir skattkóða í reitnum **Segð útreiknings** skal velja hnappinn **C**.</span><span class="sxs-lookup"><span data-stu-id="e3a36-137">To clear the calculation expression that is defined for a tax code in the **Calculation expression** field, select the **C** button.</span></span>
15. <span data-ttu-id="e3a36-138">Til að eyða færslu í flipanum **Útreikningur** skal velja **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="e3a36-138">To delete a record on the **Calculation** tab, select **Delete**.</span></span>
16. <span data-ttu-id="e3a36-139">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e3a36-139">Close the page.</span></span>
