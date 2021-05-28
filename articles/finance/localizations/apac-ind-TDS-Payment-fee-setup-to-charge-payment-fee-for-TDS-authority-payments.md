---
title: Setja upp greiðsluþóknanir fyrir TDS-greiðslur til yfirvalda
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp greiðsluþóknanir sem eru innheimtar fyrir TDS-greiðslur til yfirvalda.
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
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023343"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a><span data-ttu-id="b6212-103">Setja upp greiðsluþóknanir fyrir TDS-greiðslur til yfirvalda</span><span class="sxs-lookup"><span data-stu-id="b6212-103">Set up payment fees for TDS authority payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6212-104">Í þessu efnisatriði er útskýrt hvernig á að setja upp greiðsluþóknanir sem eru innheimtar fyrir TDS-greiðslur til yfirvalda.</span><span class="sxs-lookup"><span data-stu-id="b6212-104">This topic explains how to set up payment fees that are charged for Tax Deducted at Source (TDS) authority payments.</span></span>

1. <span data-ttu-id="b6212-105">Farið í **Viðskiptaskuldir \> Greiðsluuppsetning \> Greiðsluþóknun**.</span><span class="sxs-lookup"><span data-stu-id="b6212-105">Go to **Accounts payable \> Payment setup \> Payment fee**.</span></span>

    <span data-ttu-id="b6212-106">[![Síða greiðsluþóknunar](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span><span class="sxs-lookup"><span data-stu-id="b6212-106">[![Payment fee page](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span></span>

2. <span data-ttu-id="b6212-107">Veljið **Ný** til að stofna nýja greiðsluþóknun og færið inn nauðsynlegar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="b6212-107">Select **New** to create a payment fee, and enter the required details.</span></span>
3. <span data-ttu-id="b6212-108">Í reitnum **Gerð þóknunar** skal velja gerð greiðsluþóknunar:</span><span class="sxs-lookup"><span data-stu-id="b6212-108">In the **Fee type** field, select the type of payment fee:</span></span>

    - <span data-ttu-id="b6212-109">**Engum**</span><span class="sxs-lookup"><span data-stu-id="b6212-109">**None**</span></span>
    - <span data-ttu-id="b6212-110">**Vextir** – Vextir eru innheimtir á síðbúnum greiðslum sem eru greiddar lánardrottnayfirvaldi TDS.</span><span class="sxs-lookup"><span data-stu-id="b6212-110">**Interest** – Interest is charged on late payments that are made to the TDS authority vendor.</span></span>
    - <span data-ttu-id="b6212-111">**Önnur** – Önnur gjöld eru innheimt á síðbúnum greiðslum sem eru greiddar lánardrottnayfirvaldi TDS.</span><span class="sxs-lookup"><span data-stu-id="b6212-111">**Others** – Other charges are charged on late payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="b6212-112">Ef **Vextir** eða **Önnur** er valið verður reiturinn **Gjöld** sjálfkrafa stilltur á **Fjárhagur**.</span><span class="sxs-lookup"><span data-stu-id="b6212-112">If you select **Interest** or **Others**, the **Charge** field is automatically set to **Ledger**.</span></span>

4. <span data-ttu-id="b6212-113">Ef valið var **Vextir** eða **Önnur** í reitnum **Reitargerð**, í reitnum **Aðallykill**, skal velja fjárhagslykilinn til að bóka vextina eða önnur gjöld á.</span><span class="sxs-lookup"><span data-stu-id="b6212-113">If you selected **Interest** or **Others** in the **Field type** field, in the **Main account** field, select the ledger account to post the interest or other charges to.</span></span>
5. <span data-ttu-id="b6212-114">Færið inn aðrar áskildar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="b6212-114">Enter the other required details.</span></span>
6. <span data-ttu-id="b6212-115">Á aðgerðasvæðinu skal velja **Uppsetning greiðsluþóknunar** til að opna síðuna **Uppsetning greiðsluþóknunar** þar sem hægt er að setja upp greiðsluþóknanir fyrir ýmsar samsetningar banka, greiðslumáta, greiðsluupplýsinga, gjaldmiðla og dagsetningarbila.</span><span class="sxs-lookup"><span data-stu-id="b6212-115">On the Action Pane, select **Payment fee setup** to open the **Payment fee setup** page, where you can set up payment fees for various combinations of banks, methods of payment, payment specifications, currencies, and date intervals.</span></span>

    <span data-ttu-id="b6212-116">[![Uppsetningarsíða greiðsluþóknunar](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span><span class="sxs-lookup"><span data-stu-id="b6212-116">[![Payment fee setup page](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span></span>

7. <span data-ttu-id="b6212-117">Í flipanum **Yfirlit**, í reitnum **Flokkanir**, skal tilgreina hvaða banka er verið að setja upp greiðsluþóknun fyrir:</span><span class="sxs-lookup"><span data-stu-id="b6212-117">On the **Overview** tab, in the **Groupings** field, specify which banks you're setting up the payment fee for:</span></span>

    - <span data-ttu-id="b6212-118">**Tafla** – Þóknunin er gild fyrir tiltekinn bankareikning.</span><span class="sxs-lookup"><span data-stu-id="b6212-118">**Table** – The fee is valid for a specific bank account.</span></span>
    - <span data-ttu-id="b6212-119">**Flokkur** – Þóknunin er gild fyrir tiltekinn bankaflokk.</span><span class="sxs-lookup"><span data-stu-id="b6212-119">**Group** – The fee is valid for a specific bank group.</span></span>
    - <span data-ttu-id="b6212-120">**Allir** – Þóknunin er gild fyrir alla bankareikninga.</span><span class="sxs-lookup"><span data-stu-id="b6212-120">**All** – The fee is valid for all the bank accounts.</span></span>

8. <span data-ttu-id="b6212-121">Ef **Tafla** eða **Flokkur** var valið í reitnum **Flokkanir**, í reitnum **Bankavensl**, skal velja tiltekinn bankareikning eða bankaflokk sem verið er að setja upp greiðsluþóknun fyrir.</span><span class="sxs-lookup"><span data-stu-id="b6212-121">If you selected **Table** or **Group** in the **Groupings** field, in the **Bank relation** field, select the specific bank account or bank group that you're setting up the payment fee for.</span></span>
9. <span data-ttu-id="b6212-122">Í reitnum **Greiðslumáti** skal velja greiðsluaðferðina fyrir greiðsluþóknanir.</span><span class="sxs-lookup"><span data-stu-id="b6212-122">In the **Method of payment** field, select the method of payment for the payment of fees.</span></span>
10. <span data-ttu-id="b6212-123">Í reitnum **Greiðsluupplýsingar** skal velja eða færa inn kóða greiðsluupplýsinga sem var búinn til á síðunni **Greiðsluupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="b6212-123">In the **Payment specification** field, select or enter the payment specification code that was generated on the **Payment specification** page.</span></span>
    - <span data-ttu-id="b6212-124">Greiðsluupplýsingar er notaður við rafræna sjóður greiðsluhættir flutning.</span><span class="sxs-lookup"><span data-stu-id="b6212-124">The Payment specification is used with electronic fund transfer methods of payment.</span></span>
12. <span data-ttu-id="b6212-125">Í reitnum **Greiðslugjaldmiðill** skal velja gjaldmiðilinn sem virkjar þóknunina.</span><span class="sxs-lookup"><span data-stu-id="b6212-125">In the **Payment currency** field, select the currency that activates the fee.</span></span> <span data-ttu-id="b6212-126">Einungis færslur sem nota valinn gjaldmiðil geta virkjað þóknunina.</span><span class="sxs-lookup"><span data-stu-id="b6212-126">Only transactions that use the selected currency can activate the fee.</span></span> <span data-ttu-id="b6212-127">Ef þessi reitur er skilinn eftir auður virkja allir gjaldmiðlar þóknunina.</span><span class="sxs-lookup"><span data-stu-id="b6212-127">If you leave this field blank, all currencies activate the fee.</span></span>
13. <span data-ttu-id="b6212-128">Í reitnum **Prósenta/upphæð** skal velja útreikningsaðferðina.</span><span class="sxs-lookup"><span data-stu-id="b6212-128">In the **Percentage/Amount** field, select the calculation method.</span></span> <span data-ttu-id="b6212-129">Valkostirnir eru **Upphæð**, **Prósenta** og **Tímabil**.</span><span class="sxs-lookup"><span data-stu-id="b6212-129">The options are **Amount**, **Percent**, and **Interval**.</span></span>
14. <span data-ttu-id="b6212-130">Í reitnum **Upphæð þóknunar** skal tilgreina upphæð þóknunar sem annaðhvort prósentu af greiðslu eða upphæð fyrir eina greiðslu.</span><span class="sxs-lookup"><span data-stu-id="b6212-130">In the **Fee amount** field, specify the fee amount as either a percentage of the payment or the amount for one payment.</span></span>
15. <span data-ttu-id="b6212-131">Í reitnum **Gjaldmiðill þóknunar** skal tilgreina gjaldmiðilskóðann fyrir þóknunina.</span><span class="sxs-lookup"><span data-stu-id="b6212-131">In the **Fee currency** field, specify the currency code for the fee.</span></span>
16. <span data-ttu-id="b6212-132">Veljið flipann **Almennt** til að skoða eða breyta upplýsingunum fyrir valinn bankareikning.</span><span class="sxs-lookup"><span data-stu-id="b6212-132">Select the **General** tab to view or modify the details for the selected bank account.</span></span>

    <span data-ttu-id="b6212-133">[![Almennt](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span><span class="sxs-lookup"><span data-stu-id="b6212-133">[![General tab](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span></span>

16. <span data-ttu-id="b6212-134">Í reitnum **Lágmark** skal færa inn lágmarksupphæð færslu sem virkjar þóknunina.</span><span class="sxs-lookup"><span data-stu-id="b6212-134">In the **Minimum** field, enter the minimum transaction amount that activates the fee.</span></span>
17. <span data-ttu-id="b6212-135">Í reitnum **Hámark** skal færa inn hámarksupphæð færslu sem virkjar þóknunina.</span><span class="sxs-lookup"><span data-stu-id="b6212-135">In the **Maximum** field, enter the maximum transaction amount that activates the fee.</span></span>
18. <span data-ttu-id="b6212-136">Í reitunum **Frá dagsetningu** og **Til dagsetningar** skal skilgreina dagsetningabil fyrir útreikning á þóknunum.</span><span class="sxs-lookup"><span data-stu-id="b6212-136">In the **From date** and **To date** fields, define a date range for calculating fees.</span></span>
19. <span data-ttu-id="b6212-137">Í reitnum **Lágmarksþóknun** skal tilgreina upphæð þóknunar sem annaðhvort prósentu af greiðslu eða upphæð fyrir eina greiðslu.</span><span class="sxs-lookup"><span data-stu-id="b6212-137">In the **Minimum fee** field, specify the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
20. <span data-ttu-id="b6212-138">Í reitnum **VSK-flokkur** skal velja VSK-flokkinn sem nota á við útreikning á virðisaukaskatti fyrir upphæð þóknunar.</span><span class="sxs-lookup"><span data-stu-id="b6212-138">In the **Sales tax group** field, select the sales tax group to use to calculate the sales tax for the fee amount.</span></span>
21. <span data-ttu-id="b6212-139">Í reitnum **VSK-flokkur vöru** skal velja VSK-flokk vöru sem nota á við útreikning á virðisaukaskatti vöru fyrir upphæð þóknunar.</span><span class="sxs-lookup"><span data-stu-id="b6212-139">In the **Item sales tax group** field, select the item sales tax group to use to calculate the item sales tax for the fee amount.</span></span>
22. <span data-ttu-id="b6212-140">Veljið flipann **Tímabil**.</span><span class="sxs-lookup"><span data-stu-id="b6212-140">Select the **Interval** tab.</span></span> 

    <span data-ttu-id="b6212-141">[![Tímabilsflipi](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span><span class="sxs-lookup"><span data-stu-id="b6212-141">[![Interval tab](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span></span>

23. <span data-ttu-id="b6212-142">Í reitnum **Dagar** skal færa inn fjölda daga á milli bókunardagsetningu (afsláttardagsetningu) greiðslunnar og gjalddaga eigin víxla.</span><span class="sxs-lookup"><span data-stu-id="b6212-142">In the **Days** field, enter the number of days between the posting date (discounting date) of the payment and the due date of the promissory note.</span></span>
24. <span data-ttu-id="b6212-143">Í reitnum **Prósenta/upphæð** skal velja hvort hafi verið tilgreint prósenta eða ákveðin upphæð.</span><span class="sxs-lookup"><span data-stu-id="b6212-143">In the **Percentage/Amount** field, select whether the specification is a percentage or a set amount.</span></span>
25. <span data-ttu-id="b6212-144">Í reitnum **Upphæð þóknunar** skal færa inn upphæð þóknunar sem annaðhvort prósentu af greiðslu eða upphæð fyrir eina greiðslu.</span><span class="sxs-lookup"><span data-stu-id="b6212-144">In the **Fee amount** field, enter the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
26. <span data-ttu-id="b6212-145">Lokið síðunni **Uppsetning greiðsluþóknunar**.</span><span class="sxs-lookup"><span data-stu-id="b6212-145">Close the **Payment fee setup** page.</span></span>
27. <span data-ttu-id="b6212-146">Lokið síðunni **Greiðsluþóknun**.</span><span class="sxs-lookup"><span data-stu-id="b6212-146">Close the **Payment fee** page.</span></span>
