---
title: Staðgreiðsluskattur í innkaupafærslum
description: Fyrir lánardrottna sem þurfa að greiða staðgreiðsluskatt er hægt að úthluta sjálfgefna **Staðgreiðsluskattsflokknum** á síðunni **Allir lánardrottnar**.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 06c18e6b0779539a6da7ae7afbe000c4cfc78d9e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256668"
---
# <a name="withholding-tax-in-purchase-transactions"></a><span data-ttu-id="897e9-103">Staðgreiðsluskattur í innkaupafærslum</span><span class="sxs-lookup"><span data-stu-id="897e9-103">Withholding tax in purchase transactions</span></span>

<span data-ttu-id="897e9-104">Fyrir lánardrottna sem þurfa að greiða staðgreiðsluskatt er hægt að úthluta sjálfgefna **Staðgreiðsluskattsflokknum** á síðunni **Allir lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="897e9-104">For vendors who are liable to withholding tax, you can assign the default **Withholding tax group** on the **All vendors** page.</span></span>

1. <span data-ttu-id="897e9-105">Farið í **Yfirlitssvæði > Einingar > Viðskiptaskuldir > Lánardrottnar > Allir lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="897e9-105">Go to **Navigation pane > Modules > Accounts payable > Vendors > All vendors**.</span></span>

2. <span data-ttu-id="897e9-106">Smellið á tilheyrandi lánardrottnalykil og smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="897e9-106">Click the respective Vendor account, click **Edit**.</span></span>

3. <span data-ttu-id="897e9-107">Í flipanum **Reikningsfæra og afhenda** skal stilla reitinn **Reikna staðgreiðsluskatt** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="897e9-107">In **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="897e9-108">Staðgreiðsluskattur verður ekki reiknaður ef ekki er kveikt á **Reikna staðgreiðsluskatt** fyrir þennan lánardrottin í gögnunum.</span><span class="sxs-lookup"><span data-stu-id="897e9-108">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this vendor in the data.</span></span>

4. <span data-ttu-id="897e9-109">Veljið flokk staðgreiðsluskatts í **Staðgreiðsluskattsflokkur**.</span><span class="sxs-lookup"><span data-stu-id="897e9-109">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="897e9-110">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="897e9-110">Click **Save**.</span></span>

<span data-ttu-id="897e9-111">Fyrir vörur/þjónustu þar sem þarf að greiða staðgreiðsluskatt er hægt að úthluta sjálfgefnum **Staðgreiðsluskattsflokki vöru** í **Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="897e9-111">For items/services which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="897e9-112">Farðu í **Skoðunarrúða > Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="897e9-112">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="897e9-113">Smellið á viðkomandi vörunúmer og smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="897e9-113">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="897e9-114">Í flipanum **Innkaup** skal smella á **Reikna staðgreiðsluskatt**.</span><span class="sxs-lookup"><span data-stu-id="897e9-114">In **Purchase** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="897e9-115">Staðgreiðsluskattur verður ekki reiknaður ef **Reikna staðgreiðsluskatt** er ekki stillt á **Já** fyrir þessa vöru í flipanum **Innkaup** á síðunni **Útgefin afurð**.</span><span class="sxs-lookup"><span data-stu-id="897e9-115">Withholding tax will not be calculated if **Calculate withholding tax** isn't set to **Yes** for this Item in the **Purchase** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="897e9-116">Veljið staðgreiðsluskattflokk vöru úr listanum **Staðgreiðsluskattsflokkur**.</span><span class="sxs-lookup"><span data-stu-id="897e9-116">Select an item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="897e9-117">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="897e9-117">Click **Save**.</span></span>

<span data-ttu-id="897e9-118">Hægt er að úthluta staðgreiðsluskattsflokkum og staðgreiðsluskattflokkum vöru á síður:</span><span class="sxs-lookup"><span data-stu-id="897e9-118">Withholding tax groups and Item withholding tax groups can be assigned in pages:</span></span> 

- <span data-ttu-id="897e9-119">**Innkaupapöntun**</span><span class="sxs-lookup"><span data-stu-id="897e9-119">**Purchase order**</span></span>
- <span data-ttu-id="897e9-120">**Reikningur frá lánardrottni**</span><span class="sxs-lookup"><span data-stu-id="897e9-120">**Vendor invoice**</span></span>
- <span data-ttu-id="897e9-121">**Reikningabók**</span><span class="sxs-lookup"><span data-stu-id="897e9-121">**Invoice journal**</span></span>

<span data-ttu-id="897e9-122">Sjálfgefinn staðgreiðsluskattsflokkur og staðgreiðsluskattflokkur vöru verða færðir inn í línurnar þegar **Innkaupapantanir** og/eða **Reikningar frá lánardrottni í bið** eru stofnaðir.</span><span class="sxs-lookup"><span data-stu-id="897e9-122">The default Withholding tax group and Item withholding tax group will be carried into the lines when creating **Purchase orders** and/or **Pending Vendor invoices**.</span></span> <span data-ttu-id="897e9-123">Fyrir **Reikningabók lánardrottins** er hægt að kveikja á **Reikna staðgreiðsluskatt** og velja **Staðgreiðsluskattflokk vöru** í flipanum **Almennt** í færslubókinni.</span><span class="sxs-lookup"><span data-stu-id="897e9-123">For **Vendor invoice journal**, you can switch on **Calculate withholding tax** and select **Item withholding tax group** in the **General** tab in the journal.</span></span>

<span data-ttu-id="897e9-124">Tímabundin upphæð staðgreiðsluskatts er í boði í reitnum **Leiðréttur staðgreiðsluskattur** í flipanum **Samtölur** á síðunni **Innkaupapöntun**.</span><span class="sxs-lookup"><span data-stu-id="897e9-124">The temporary amount of withholding tax is available in the field **Adjusted withholding tax** of the **Totals** tab on the **Purchase order** page.</span></span>

![Staðgreiðsluskattur er hafður með í innkaupapöntuninni](media/withholding-tax-adjusted.png)

<span data-ttu-id="897e9-126">Staðgreiðsluskattur er reiknaður í **Greiðslubók lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="897e9-126">Withholding tax is calculated on **Vendor payment journal**.</span></span> <span data-ttu-id="897e9-127">Hægt er að leiðrétta viðeigandi staðgreiðsluskattskóða handvirkt rétt eins og raunverulegum upphæðum staðgreiðsluskatts í flipanum **Staðgreiðsluskattur** á síðunni **Jafna færslur**.</span><span class="sxs-lookup"><span data-stu-id="897e9-127">You can manually adjust the applicable withholding tax codes as well as the actual withholding tax amounts in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

![Staðgreiðslu er hægt að leiðrétta handvirkt á síðu færslujöfnunar](media/withholding-tax-vendor-payment-tab.png)

<span data-ttu-id="897e9-129">Afleidd upphæð staðgreiðsluskatts verður dregin frá lánardrottnagreiðslunni og bókuð í **Staðgreiðsluskattslykli** í tengdu fylgiskjali.</span><span class="sxs-lookup"><span data-stu-id="897e9-129">The derived withholding tax amount will be deducted from the vendor payment and posted to the **Withholding tax account** in a related voucher.</span></span>

![Staðgreiðsluskattslykill sem sýnir tengt fylgiskjal](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]