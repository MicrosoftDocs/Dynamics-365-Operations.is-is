---
title: "Safna upp áskriftum"
description: "Með þjónustuáskriftum er tekjum safnað upp handvirkt á tímabilum sem koma á eftir þeim degi þegar þóknunarfærsla var reikningsfærð."
author: YuyuScheller
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: acbf7432c9487cbefaf24a2a98772c8f0ec7ffe6
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="accruing-subscriptions"></a><span data-ttu-id="1cedb-103">Safna upp áskriftum</span><span class="sxs-lookup"><span data-stu-id="1cedb-103">Accruing subscriptions</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1cedb-104">Með þjónustuáskriftum er tekjum safnað upp handvirkt á tímabilum sem koma á eftir þeim degi þegar þóknunarfærsla var reikningsfærð.</span><span class="sxs-lookup"><span data-stu-id="1cedb-104">With service subscriptions, you manually accrue revenue in the periods following the date when you invoiced a fee transaction.</span></span>

<span data-ttu-id="1cedb-105">Uppsöfnunartímabil eru stofnuð fyrir reikningstímabilið sem sett eru fyrir áskriftarþóknunina, og uppsöfnunartímabilin eru byggð á tímabilskóða áskriftarinnar.</span><span class="sxs-lookup"><span data-stu-id="1cedb-105">Accrual periods are created for the invoice period that you set up for the subscription fee, and the accrual periods are based on the period code of the subscription.</span></span>

<span data-ttu-id="1cedb-106">Hægt er að safna upp og bakfæra uppsöfnuðum tekjum.</span><span class="sxs-lookup"><span data-stu-id="1cedb-106">You can accrue and reverse accrued revenue.</span></span>

## <a name="reverse-accruals-of-credit-amounts"></a><span data-ttu-id="1cedb-107">Bakfæra uppsafnaðar upphæð inneignar</span><span class="sxs-lookup"><span data-stu-id="1cedb-107">Reverse accruals of credit amounts</span></span>

<span data-ttu-id="1cedb-108">Ef þú gjaldfærir upphæðir áskriftarreikninga er hægt að nota tvær aðferðir til að bakfæra uppsafnaðri upphæð:</span><span class="sxs-lookup"><span data-stu-id="1cedb-108">If you credit invoiced subscription amounts, you can use two methods to reverse the accrual amounts:</span></span>

  - <span data-ttu-id="1cedb-109">Þú getur bakfært hverja uppsöfnuð tekjufærslu fyrir sig, áður en þú býrð til kreditnótutillögu fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="1cedb-109">You can reverse each accrued revenue transaction individually before you create the credit note proposal for the transaction.</span></span> <span data-ttu-id="1cedb-110">Þetta er handvirka aðferðin.</span><span class="sxs-lookup"><span data-stu-id="1cedb-110">This is the manual method.</span></span> <span data-ttu-id="1cedb-111">(handvirkt)</span><span class="sxs-lookup"><span data-stu-id="1cedb-111">(manual)</span></span>

  - <span data-ttu-id="1cedb-112">Þú getur bakfært uppsafnaðar upphæðir á þeim degi sem kreditnótutillagan er bókuð eða á upphaflegu bókunardagsetningu uppsöfnunar.</span><span class="sxs-lookup"><span data-stu-id="1cedb-112">You can have the accrued amounts reversed on the date where the credit note is posted or on the original posting date of the accrual.</span></span>

<span data-ttu-id="1cedb-113">Nánari upplýsingar er að finna í [Áskriftarbreytur (eyðublað)](https://technet.microsoft.com/en-us/library/aa619615.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1cedb-113">For more information, see [Subscription parameters (form)](https://technet.microsoft.com/en-us/library/aa619615.aspx).</span></span>

## <a name="setup-requirements"></a><span data-ttu-id="1cedb-114">Setja upp kröfur</span><span class="sxs-lookup"><span data-stu-id="1cedb-114">Setup requirements</span></span>

<span data-ttu-id="1cedb-115">Til að safna upp tekjum skaltu ganga úr skugga um að eftirfarandi kröfur um gögn séu uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="1cedb-115">To accrue revenue, make sure that the following data requirements are met:</span></span>

## <a name="account-setup"></a><span data-ttu-id="1cedb-116">Uppsetning lykils</span><span class="sxs-lookup"><span data-stu-id="1cedb-116">Account setup</span></span>

<span data-ttu-id="1cedb-117">The **WIP - áskrift** og **Uppsafnaðar tekjur - áskrift** reikningarnir verða að vera sett upp í **Verkefni** mátinu.</span><span class="sxs-lookup"><span data-stu-id="1cedb-117">The **WIP - subscription** and the **Accrued revenue - subscription** accounts must be set up in the **Project** module.</span></span>

<span data-ttu-id="1cedb-118">Þegar þú bókar uppsafnaðar tekjur er **WIP - Áskrift** reikningurinn skuldfærður með uppsöfnunarupphæð og **Uppsafnaðar tekjur - áskrift** reikningurinn gjaldfærður með uppöfnunarupphæð.</span><span class="sxs-lookup"><span data-stu-id="1cedb-118">When you post accrued revenue, the **WIP - subscription** account is debited with the accrual amount, and the **Accrued revenue - subscription** account is credited with the accrual amount.</span></span>

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a><span data-ttu-id="1cedb-119">Lyklar settir upp fyrir uppsöfnun áskriftartekna</span><span class="sxs-lookup"><span data-stu-id="1cedb-119">Set up accounts for accrual of subscription revenue</span></span>

1.  <span data-ttu-id="1cedb-120">Smelltu á **Verkefnastjórnun og bókhald** \> **Uppsetning** \> **Bókun** \> **Uppsetning fjárhagsbókunar**.</span><span class="sxs-lookup"><span data-stu-id="1cedb-120">Click **Project management and accounting** \> **Setup** \> **Posting** \> **Ledger posting setup**.</span></span>

2.  <span data-ttu-id="1cedb-121">Smelltu á **Tekjureikningar** flipann og veldu **WIP - áskrift** eða **Uppsafnaðar tekjur - áskrift** til að setja upp reikningana.</span><span class="sxs-lookup"><span data-stu-id="1cedb-121">Click the **Revenue accounts** tab, and select **WIP - subscription** or **Accrued revenue - subscription** to set up the accounts.</span></span>

## <a name="subscription-group-setup"></a><span data-ttu-id="1cedb-122">Uppsetning áskriftarhópa</span><span class="sxs-lookup"><span data-stu-id="1cedb-122">Subscription group setup</span></span>

<span data-ttu-id="1cedb-123">Til að hægt sé að safna upp tekjum fyrir áskriftir verður að velja gátreitinn **Safna upp tekjum**.</span><span class="sxs-lookup"><span data-stu-id="1cedb-123">To be able to accrue revenue for subscriptions, the **Accrue revenue** check box must be selected.</span></span> <span data-ttu-id="1cedb-124">Þetta er að finna á **Áskriftarflokkar** skjámynd fyrir hópinn sem fylgir áskriftinni.</span><span class="sxs-lookup"><span data-stu-id="1cedb-124">This is found on the **Subscription groups** form for the group that is attached to the subscription.</span></span> <span data-ttu-id="1cedb-125">Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Þjónusta áskrift** \> **Áskriftarflokkar** .</span><span class="sxs-lookup"><span data-stu-id="1cedb-125">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="enable-revenue-accrual-on-a-subscription-group"></a><span data-ttu-id="1cedb-126">Uppsöfnun tekna gerð virk á áskriftarhópi</span><span class="sxs-lookup"><span data-stu-id="1cedb-126">Enable revenue accrual on a subscription group</span></span>

1.  <span data-ttu-id="1cedb-127">Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Þjónusta áskrift** \> **Áskriftarflokkar** .</span><span class="sxs-lookup"><span data-stu-id="1cedb-127">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="periods"></a><span data-ttu-id="1cedb-128">Tímabil</span><span class="sxs-lookup"><span data-stu-id="1cedb-128">Periods</span></span>

<span data-ttu-id="1cedb-129">Setja verður upp reikningstímabilskóða.</span><span class="sxs-lookup"><span data-stu-id="1cedb-129">You must set up an invoicing period code.</span></span> <span data-ttu-id="1cedb-130">Nema þú viljir safna upp tekjum á sama tímabili og þú notar til að reikningsfæra, verður þú einnig að setja upp uppsöfnunartímabil.</span><span class="sxs-lookup"><span data-stu-id="1cedb-130">Unless you want to accrue revenue in the same time intervals as you use for invoicing, you must also set up an accrual period.</span></span>

<span data-ttu-id="1cedb-131">Eftirfarandi tafla veitir yfirlit um hvaða uppsöfnunartímabil má setja upp fyrir hvert reikningsfærslutímabil:</span><span class="sxs-lookup"><span data-stu-id="1cedb-131">The following table provides an overview of which accrual periods can be set up for each invoicing period:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1cedb-132">Tímabil reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="1cedb-132">Invoicing period</span></span></p></th>
<th><p><span data-ttu-id="1cedb-133">Uppsöfnunartímabil</span><span class="sxs-lookup"><span data-stu-id="1cedb-133">Accrual period</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1cedb-134"><strong>Ár</strong></span><span class="sxs-lookup"><span data-stu-id="1cedb-134"><strong>Years</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="1cedb-135"><strong>Ár</strong></span><span class="sxs-lookup"><span data-stu-id="1cedb-135"><strong>Years</strong></span></span></p></li>
<li><p><span data-ttu-id="1cedb-136"><strong>Ársfjórðungur</strong></span><span class="sxs-lookup"><span data-stu-id="1cedb-136"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="1cedb-137"><strong>Mánuður</strong></span><span class="sxs-lookup"><span data-stu-id="1cedb-137"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="1cedb-138"><strong>Dagur</strong></span><span class="sxs-lookup"><span data-stu-id="1cedb-138"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cedb-139"><strong>Ársfjórðungur</strong></span><span class="sxs-lookup"><span data-stu-id="1cedb-139"><strong>Quarter</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="1cedb-140"><strong>Ársfjórðungur</strong></span><span class="sxs-lookup"><span data-stu-id="1cedb-140"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="1cedb-141"><strong>Mánuður</strong></span><span class="sxs-lookup"><span data-stu-id="1cedb-141"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="1cedb-142"><strong>Dagur</strong></span><span class="sxs-lookup"><span data-stu-id="1cedb-142"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cedb-143"><strong>Mánuður</strong></span><span class="sxs-lookup"><span data-stu-id="1cedb-143"><strong>Month</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="1cedb-144"><strong>Mánuður</strong></span><span class="sxs-lookup"><span data-stu-id="1cedb-144"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="1cedb-145"><strong>Dagur</strong></span><span class="sxs-lookup"><span data-stu-id="1cedb-145"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cedb-146"><strong>Vika</strong></span><span class="sxs-lookup"><span data-stu-id="1cedb-146"><strong>Week</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="1cedb-147"><strong>Dagur</strong></span><span class="sxs-lookup"><span data-stu-id="1cedb-147"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cedb-148"><strong>Dagur</strong></span><span class="sxs-lookup"><span data-stu-id="1cedb-148"><strong>Day</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="1cedb-149"><strong>Dagur</strong></span><span class="sxs-lookup"><span data-stu-id="1cedb-149"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1cedb-150">Uppsetning reikningsfærsutímabilsins er lögboðin hluti af heildaruppsetningu áskriftarflokksins.</span><span class="sxs-lookup"><span data-stu-id="1cedb-150">Setting up the invoicing period is a mandatory part of the overall subscription group setup.</span></span> <span data-ttu-id="1cedb-151">Þú getur ákveðið hvort þú setur einnig upp uppsöfnunartímabil fyrir áskriftarflokkinn.</span><span class="sxs-lookup"><span data-stu-id="1cedb-151">You can decide whether to also set up an accrual period for the subscription group.</span></span> <span data-ttu-id="1cedb-152">Ef þú setur upp uppsöfnunartímabil fyrir áskriftarflokkinn er þetta tímabil lagt til í **Tímabilskóði** reitinn.</span><span class="sxs-lookup"><span data-stu-id="1cedb-152">If you set up an accrual period for the subscription group, this period is suggested in the **Period code** field.</span></span> <span data-ttu-id="1cedb-153">Þessi reitur er að finna í **Uppsafnaðar áskriftartekjur** skjámynd, þegar þú safnar upp áskriftartekjur.</span><span class="sxs-lookup"><span data-stu-id="1cedb-153">This field is found in the **Accrue subscription revenue** form, when you accrue subscription revenue.</span></span> <span data-ttu-id="1cedb-154">Uppsöfnunartímabilið er hins vegar valfrjálsar upplýsingar um áskriftarhópinn.</span><span class="sxs-lookup"><span data-stu-id="1cedb-154">However, the accrual period is optional information about the subscription group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1cedb-155">Notaðu eftirfarandi slóð til að opna <STRONG>Safna upp áskriftartekjum</STRONG> skjámyndina.</span><span class="sxs-lookup"><span data-stu-id="1cedb-155">Use the following path to open the <STRONG>Accrue subscription revenue</STRONG> form.</span></span> <span data-ttu-id="1cedb-156">Smelltu á <STRONG>Þjónustustjórnun</STRONG> &gt; <STRONG>Tímabil</STRONG> &gt; <STRONG>Þjónustuáskriftir</STRONG> &gt; <STRONG>Safna upp áskriftartekjum</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="1cedb-156">Click <STRONG>Service management</STRONG> &gt; <STRONG>Periodic</STRONG> &gt; <STRONG>Service subscriptions</STRONG> &gt; <STRONG>Accrue subscription revenue</STRONG>.</span></span></P>


## <a name="transactions"></a><span data-ttu-id="1cedb-157">Færslur</span><span class="sxs-lookup"><span data-stu-id="1cedb-157">Transactions</span></span>

<span data-ttu-id="1cedb-158">Þú getur stjórnað fjölda fjárhagsfærslna sem eru búnar til þegar þú bókar uppsafnaðar tekjur.</span><span class="sxs-lookup"><span data-stu-id="1cedb-158">You can control the number of ledger transactions that are created when you post accrued revenue.</span></span> <span data-ttu-id="1cedb-159">Á áskriftum skal tilgreina hvort fjárhagsfærslur skuli búin til sem samtala eða á hverja línu.</span><span class="sxs-lookup"><span data-stu-id="1cedb-159">On subscriptions, define if the ledger transactions should be created as a total or per line.</span></span>

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a><span data-ttu-id="1cedb-160">Tilgreinið stig bókunarupplýsingar sem sýna á fyrir uppsöfnunarfærslur</span><span class="sxs-lookup"><span data-stu-id="1cedb-160">Specify the level of posting details to display for accrued transactions</span></span>

1.  <span data-ttu-id="1cedb-161">Smelltu á **Verkefnastjórnun og bókhald** \> **Uppsetning** \> **Verkefnastjórnun og bókhaldsfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="1cedb-161">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="1cedb-162">Á **Fjármál** flipanum, í reitnum **Reikningur** skal velja **Samtala** eða **Lína**.</span><span class="sxs-lookup"><span data-stu-id="1cedb-162">On the **Financial** tab, in the **Invoice** field, select **Total** or **Line**.</span></span>


## <a name="see-also"></a><span data-ttu-id="1cedb-163">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1cedb-163">See also</span></span>

[<span data-ttu-id="1cedb-164">Safna upp áskriftartekjum</span><span class="sxs-lookup"><span data-stu-id="1cedb-164">Accrue subscription revenue</span></span>](accrue-subscription-revenue.md)

  



