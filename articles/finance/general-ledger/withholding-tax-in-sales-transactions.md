---
title: Staðgreiðsluskattur í sölufærslum
description: Þetta efnisatriði sýnir skrefin til að komast hjá útreikningi staðgreiðsluskatts fyrir valda viðskiptavini. Fyrir viðskiptavini sem tilgreina staðgreiðsluskatt í greiðslum til þín, er hægt að úthluta sjálfgefnum staðgreiðsluskattsflokki.
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
ms.openlocfilehash: c50f6df1c63c91107da65f463934565f786d6ccd
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060751"
---
# <a name="withholding-tax-in-sales-transactions"></a><span data-ttu-id="ce007-104">Staðgreiðsluskattur í sölufærslum</span><span class="sxs-lookup"><span data-stu-id="ce007-104">Withholding tax in sales transactions</span></span>

<span data-ttu-id="ce007-105">Þetta efnisatriði sýnir skrefin til að komast hjá útreikningi staðgreiðsluskatts fyrir valda viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="ce007-105">This topic lists the steps for avoiding the calculation of withholding tax for selected customers.</span></span> <span data-ttu-id="ce007-106">Fyrir viðskiptavini sem tilgreina staðgreiðsluskatt í greiðslum til þín, er hægt að úthluta sjálfgefnum **Staðgreiðsluskattsflokki** á síðunni **Viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="ce007-106">For customers who specify withholding tax in their payments to you, you can assign the default **Withholding tax group** on the **Customers** page.</span></span> 

1. <span data-ttu-id="ce007-107">Farið í **Yfirlitssvæði > Einingar > Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="ce007-107">Go to **Navigation pane > Modules > Accounts receivable > Customers > All customers**.</span></span>

2. <span data-ttu-id="ce007-108">Smellið á tilheyrandi viðskiptavinalykil og smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="ce007-108">Click the respective customer account, click **Edit**.</span></span>

3. <span data-ttu-id="ce007-109">Í flipanum **Reikningsfæra og afhenda** skal stilla reitinn **Reikna staðgreiðsluskatt** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="ce007-109">In the **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="ce007-110">Staðgreiðsluskattur verður ekki reiknaður ef ekki er kveikt á **Reikna staðgreiðsluskatt** fyrir þennan viðskiptavin í aðalgögnunum.</span><span class="sxs-lookup"><span data-stu-id="ce007-110">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this customer in the master data.</span></span>

4. <span data-ttu-id="ce007-111">Veljið flokk staðgreiðsluskatts í **Staðgreiðsluskattsflokkur**.</span><span class="sxs-lookup"><span data-stu-id="ce007-111">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="ce007-112">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="ce007-112">Click **Save**.</span></span>

<span data-ttu-id="ce007-113">Fyrir vörur/þjónustu þar sem þarf að greiða staðgreiðsluskatt er hægt að úthluta sjálfgefnum **Staðgreiðsluskattsflokki vöru** í **Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="ce007-113">For items/services, which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="ce007-114">Farðu í **Skoðunarrúða > Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="ce007-114">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="ce007-115">Smellið á viðkomandi vörunúmer og smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="ce007-115">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="ce007-116">Í flipanum **Selja** skal smella á **Reikna staðgreiðsluskatt**.</span><span class="sxs-lookup"><span data-stu-id="ce007-116">In the **Sell** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="ce007-117">Staðgreiðsluskattur verður ekki reiknaður ef **Reikna staðgreiðsluskatt** er ekki stillt á **Já** fyrir þessa vöru í flipanum **Selja** á síðunni **Útgefin afurð**.</span><span class="sxs-lookup"><span data-stu-id="ce007-117">Withholding tax will not be calculated if **Calculate withholding tax** is not set to **Yes** for this Item in the **Sell** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="ce007-118">Veljið staðgreiðsluskattflokk vöru úr listanum **Staðgreiðsluskattsflokkur**.</span><span class="sxs-lookup"><span data-stu-id="ce007-118">Select an Item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="ce007-119">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="ce007-119">Click **Save**.</span></span>

<span data-ttu-id="ce007-120">Hægt er að úthluta staðgreiðsluskattsflokkum og staðgreiðsluskattflokkum vöru með því að nota síðuna **Sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="ce007-120">Withholding tax groups and Item withholding tax groups can be assigned using the **Sales order** page.</span></span> 

<span data-ttu-id="ce007-121">Sjálfgefinn staðgreiðsluskattsflokkur og staðgreiðsluskattflokkur vöru verða notaðir sem sjálfgefnar færslur í sölupöntunarlínum þegar ný sölupöntun er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="ce007-121">The default Withholding tax group and Item withholding tax group will be used as default entries on sales order lines when you create a new sales order.</span></span>

<span data-ttu-id="ce007-122">Staðgreiðsluskattur er reiknaður og bókaður með **Greiðslubók viðskiptavinar**.</span><span class="sxs-lookup"><span data-stu-id="ce007-122">Withholding tax is calculated and posted with **Customer payment journal**.</span></span> <span data-ttu-id="ce007-123">Hægt er að leiðrétta viðeigandi staðgreiðsluskattskóða handvirkt rétt eins og raunverulega upphæð staðgreiðsluskatts í flipanum **Staðgreiðsluskattur** á síðunni **Jafna færslur**.</span><span class="sxs-lookup"><span data-stu-id="ce007-123">You can manually adjust the applicable withholding tax code, as well as the actual withholding tax amount in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

<span data-ttu-id="ce007-124">Reiknuð upphæð staðgreiðsluskatts verður dregin frá lánardrottnagreiðslunni og bókuð í **Mótlykli staðgreiðsluskatts** í tengdu fylgiskjali.</span><span class="sxs-lookup"><span data-stu-id="ce007-124">The calculated withholding tax amount will be deducted from the customer payment and posted to the **Withholding tax offset** account in a related voucher.</span></span>
