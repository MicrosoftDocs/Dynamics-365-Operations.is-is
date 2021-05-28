---
title: Setja upp skatthluta fyrir TDS-skattgerðina
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp hluta staðgreiðsluskatts fyrir skattgerðina þar sem skattur er dreginn frá upprunalegri greiðslu (TDS). Það útskýrir einnig hvernig skilgreina á mörkin sem eru notuð til að reikna út TDS fyrir hvern TDS-hluta.
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
ms.openlocfilehash: 6e0a6a05fcb4afb8c8965e25c3089bc1b3d98431
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023323"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a><span data-ttu-id="0fcc0-104">Setja upp skatthluta fyrir TDS-skattgerðina</span><span class="sxs-lookup"><span data-stu-id="0fcc0-104">Set up tax components for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0fcc0-105">Í þessu efnisatriði er útskýrt hvernig á að setja upp hluta staðgreiðsluskatts fyrir skattgerðina þar sem skattur er dreginn frá upprunalegri greiðslu (TDS).</span><span class="sxs-lookup"><span data-stu-id="0fcc0-105">This topic explains how to set up withholding tax components for the Tax Deducted at Source (TDS) tax type.</span></span> <span data-ttu-id="0fcc0-106">TDS-hlutarnir eru TDS, aukagjald, PE-Cess og SHE Cess.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-106">The TDS components are TDS, surcharge, PE-Cess, and SHE Cess.</span></span> <span data-ttu-id="0fcc0-107">Í þessu efnisatriði er einnig útskýrt hvernig skilgreina á mörkin sem eru notuð til að reikna út TDS fyrir hvern TDS-hluta.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-107">This topic also explains how to define the threshold that is used to calculate TDS for each TDS component.</span></span> <span data-ttu-id="0fcc0-108">Auk þess er hægt að skilgreina undantekningamörk sem eru notuð til að reikna út TDS fyrir hvern TDS-hluta.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-108">Additionally, you can define an exception threshold that is used to calculate TDS for each TDS component.</span></span>

<span data-ttu-id="0fcc0-109">Fylgið þessum skrefum til að setja upp TDS-hluta.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-109">Follow these steps to set up TDS components.</span></span>

1. <span data-ttu-id="0fcc0-110">Farið í **Skattur \> Uppsetning \> Staðgreiðsluskattur \> Staðgreiðsluskattshlutar**.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-110">Go to **Tax \> Setup \> Withholding tax \> Withholding tax components**.</span></span>

    <span data-ttu-id="0fcc0-111">[![Síða staðgreiðsluskattshluta](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span><span class="sxs-lookup"><span data-stu-id="0fcc0-111">[![Withholding tax components page](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span></span>

2. <span data-ttu-id="0fcc0-112">Í reitnum **Skattgerð** skal velja **TDS** til að setja upp staðgreiðsluskattshluta fyrir skattgerð TDS.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-112">In the **Tax type** field, select **TDS** to set up withholding tax components for the TDS tax type.</span></span>
3. <span data-ttu-id="0fcc0-113">Veldu **Nýtt** á aðgerðasvæðinu til að búa til línu.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-113">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="0fcc0-114">Í reitnum **Staðgreiðsluskattshluti** skal færa inn heiti fyrir TDS-hluta.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-114">In the **Withholding tax component** field, enter a name for the TDS component.</span></span>
5. <span data-ttu-id="0fcc0-115">Í reitnum **Flokkur staðgreiðsluskattshluta** skal velja flokk staðgreiðsluskattshluta TDS til að hengja TDS-hlutann við.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-115">In the **Withholding tax component group** field, select the TDS withholding tax component group to attach the TDS component to.</span></span>
6. <span data-ttu-id="0fcc0-116">Í flipanum **Almennt**, í reitnum **Lýsing**, skal slá inn lýsingu á TDS einingunni.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-116">On the **General** FastTab, in the **Description** field, enter a description of  the TDS component.</span></span>
7. <span data-ttu-id="0fcc0-117">Á aðgerðasvæðinu skal velja **Mörk** til að opna síðuna **Mörk** þannig að sé hægt að skilgreina mörkin sem eru notuð til að reikna út TDS fyrir TDS-hlutann.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-117">On the Action Pane, select **Threshold** to open **Threshold** page, so that you can define the threshold that is used to calculate TDS for the TDS component.</span></span>
8. <span data-ttu-id="0fcc0-118">Notið reitina **Frá dagsetningu** og **Til dagsetningar** til að skilgreina tímabilið sem mörkin eiga að gilda fyrir.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-118">Use the **From date** and **To date** fields to define the period that the threshold is applicable to.</span></span>
9. <span data-ttu-id="0fcc0-119">Í flýtiflipann **Almennt**, í reitinn **Mörk**, skal færa inn upphæð marka sem eru notuð til að reikna út TDS fyrir TDS-hlutann.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-119">On the **General** FastTab, in the **Threshold** field, enter the threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="0fcc0-120">Skatturinn verður dreginn frá upprunanum aðeins þegar uppsöfnuð reikningsupphæð fer yfir mörkin.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-120">The tax will be deducted at the source only when the cumulative invoice amount crosses the threshold.</span></span>

    <span data-ttu-id="0fcc0-121">Ef upphæð marka er til dæmis 10.000, þá er TDS reiknað eftir að uppsöfnuð reikningsupphæð fer yfir 10.000 (með öðrum orðum, þegar hún er 10.001 eða hærri).</span><span class="sxs-lookup"><span data-stu-id="0fcc0-121">For example, if the threshold amount is 10,000, TDS is calculated after the cumulative invoice amount exceeds 10,000 (in other words, when it's 10,001 or more).</span></span>

10. <span data-ttu-id="0fcc0-122">Í reitinn **Undantekningarmörk** skal færa inn upphæð undantekningarmarka sem eru notuð til að reikna út TDS fyrir TDS-hlutann.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-122">In the **Exception threshold** field, enter the exception threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="0fcc0-123">Skatturinn í reikningslínu verður dreginn frá upprunanum aðeins þegar upphæðin fer yfir undantekningarmörkin.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-123">The tax on an invoice line will be deducted at the source only when the amount crosses the exception threshold.</span></span>

    <span data-ttu-id="0fcc0-124">Ef til dæmis upphæð undantekningarmarka er 5000, þá er TDS reiknaðu í tiltekinni reikningslínu ef upphæð reikningslínunnar fer yfir 5000 (með öðrum orðum, ef hún er 5001 eða hærri).</span><span class="sxs-lookup"><span data-stu-id="0fcc0-124">For example, if the exception threshold amount is 5,000, TDS is calculated on a specific invoice line if the invoice line amount exceeds 5,000 (in other words, if it's 5,001 or more).</span></span>

    <span data-ttu-id="0fcc0-125">[![Þröskuldssíða](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span><span class="sxs-lookup"><span data-stu-id="0fcc0-125">[![Threshold page](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="0fcc0-126">Upphæð undantekningarmarka verður að vera minni en eða jafnt og upphæð marka.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-126">The exception threshold amount must be less than or equal to the threshold amount.</span></span>
    >
    > <span data-ttu-id="0fcc0-127">Skatturinn er dreginn frá færslu ef færsluupphæðin fer yfir undantekningarmörkin, jafnvel þótt uppsöfnuð reikningsupphæð fer ekki yfir mörkin sem eru tilgreind í reitnum **Mörk**.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-127">The tax is deducted for a transaction if the transaction amount crosses the exception threshold, even if the cumulative invoice amount doesn't cross the threshold that is specified in the **Threshold** field.</span></span>

11. <span data-ttu-id="0fcc0-128">Lokið síðunni **Mörk** til að fara aftur á síðuna **Staðgreiðsluskattshlutar**.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-128">Close the **Threshold** page to return to the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="0fcc0-129">Á aðgerðasvæðinu skal velja **Afrita** til að opna svargluggann **Afrita staðgreiðsluskattshluta** þannig að hægt sé að afrita TDS-hlutana sem voru settir upp fyrir einn flokk TDS-hluta til annars flokks TDS-hluta.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-129">On the Action Pane, select **Copy** to open the **Copy withholding tax components** dialog box, so that you can copy the TDS components that were set up for one TDS component group to another TDS component group.</span></span>
13. <span data-ttu-id="0fcc0-130">Í reitnum **Frá** skal velja flokk TDS-hluta til að afrita TDS-hlutana úr.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-130">In the **From** field, select the TDS component group to copy the TDS components from.</span></span> <span data-ttu-id="0fcc0-131">Í reitnum **Til** skal velja flokk staðgreiðsluskattshluta til að afrita TDS-hlutana í.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-131">In the **To** field, select the withholding tax component group to copy the TDS components to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0fcc0-132">Algengir TDS-hlutar sem eru hengdir við báða flokka TDS-hluta eru ekki afritaðir.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-132">Common TDS components that are attached to both TDS component groups aren't copied.</span></span>

14. <span data-ttu-id="0fcc0-133">Veljið **Í lagi** til að afrita og stofna TDS-hluta fyrir hinn flokk TDS-hluta á síðunni **Staðgreiðsluskattshlutar**.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-133">Select **OK** to copy and create TDS components for the other TDS component group on the **Withholding tax components** page.</span></span>

    <span data-ttu-id="0fcc0-134">[![Svargluggi afritunar staðgreiðsluskattshluta](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span><span class="sxs-lookup"><span data-stu-id="0fcc0-134">[![Copy withholding tax components dialog box](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span></span>

15. <span data-ttu-id="0fcc0-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0fcc0-135">Close the page.</span></span>
