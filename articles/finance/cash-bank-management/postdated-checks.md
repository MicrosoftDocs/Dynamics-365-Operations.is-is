---
title: Fyrirframdagsettar ávísanir
description: Þessi grein veitir upplýsingar um stuðning fyrir fyrirframdagsettar ávísanir í Microsoft Dynamics 365 Finance. Fyrirframdagsettar ávísanir eru ávísanir sem eru gefnar út til að greiða og taka á móti greiðslum í framtíðinni. Þess vegna er ekki hægt að leysa út ávísun fram að tilgreindri dagsetningu.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38ee6c5b3d258c313a2066b388a83330bf696d39
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444534"
---
# <a name="postdated-checks"></a><span data-ttu-id="4e61d-105">Fyrirframdagsettar ávísanir</span><span class="sxs-lookup"><span data-stu-id="4e61d-105">Postdated checks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e61d-106">Þessi grein veitir upplýsingar um stuðning fyrir fyrirframdagsettar ávísanir.</span><span class="sxs-lookup"><span data-stu-id="4e61d-106">This article provides information about support for postdated checks.</span></span> <span data-ttu-id="4e61d-107">Fyrirframdagsettar ávísanir eru ávísanir sem eru gefnar út til að greiða og taka á móti greiðslum í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="4e61d-107">Postdated checks are checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="4e61d-108">Þess vegna er ekki hægt að leysa út ávísun fram að tilgreindri dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="4e61d-108">Therefore, the check can't be cashed until the specified date.</span></span>

<span data-ttu-id="4e61d-109">Dynamics 365 Finance styður ferli fullrar stjórnunar fyrir fyrirframdagsettar ávísanir bæði í Viðskiptakröfum og Viðskiptaskuldum, eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="4e61d-109">Dynamics 365 Finance supports the full management cycle for postdated checks in both Accounts receivable and Accounts payable, as shown in the following table.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4e61d-110">Aðstæður</span><span class="sxs-lookup"><span data-stu-id="4e61d-110">Scenario</span></span></th>
<th><span data-ttu-id="4e61d-111">Upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4e61d-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4e61d-112">Uppsetning fyrirframdagsettra ávísana</span><span class="sxs-lookup"><span data-stu-id="4e61d-112">Set up postdated checks</span></span></td>
<td><span data-ttu-id="4e61d-113">Þarf að setja upp nýju greiðsluaðferðina og tilgreina greiðsluaðferðina fyrir millireikninga fyrir útgefnar ávísanir, mótteknar ávísanir og staðgreiðsluskatt.</span><span class="sxs-lookup"><span data-stu-id="4e61d-113">You must set up a new payment method, and specify the payment routine for clearing accounts for issued checks, received checks, and withholding tax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e61d-114">Skráning og bókun fyrirframdagsettrar ávísunar fyrir lánardrottin</span><span class="sxs-lookup"><span data-stu-id="4e61d-114">Register and post a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="4e61d-115">Skrá upplýsingar um fyrirframdagsettar ávísanir sem er gefin út til lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="4e61d-115">Register the details of a postdated check that you issue to a vendor.</span></span> <span data-ttu-id="4e61d-116">Þegar greiðslan er bókuð er skuld lánardrottins viðurkennd , en bankareikningurinn er ekki enn kreditfærður.</span><span class="sxs-lookup"><span data-stu-id="4e61d-116">When the payment is posted, the vendor liability is recognized, but the bank account isn’t yet credit.</span></span> <span data-ttu-id="4e61d-117">Í stað þess er millireikningur notað fyrir þennan tilgang.</span><span class="sxs-lookup"><span data-stu-id="4e61d-117">Instead, a clearing account is used for this purpose.</span></span> </td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e61d-118">Skrá og bóka fyrirframdagsetta ávísun fyrir lánardrottin</span><span class="sxs-lookup"><span data-stu-id="4e61d-118">Register and post a postdated check for a customer</span></span></td>
<td><span data-ttu-id="4e61d-119">Skrá upplýsingar um fyrirframdagsettar ávísanir sem er tekið er við frá viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="4e61d-119">Register the details of a postdated check that you receive from a customer.</span></span> <span data-ttu-id="4e61d-120">Þegar greiðslan er bókuð er viðskiptakrafa viðskiptavinar kreditfærð, en bankareikningurinn er ekki enn debetfærður.</span><span class="sxs-lookup"><span data-stu-id="4e61d-120">When the payment is posted, the customer receivable is credit, but the bank account isn’t yet debit.</span></span> <span data-ttu-id="4e61d-121">Í stað þess er millireikningur notað fyrir þennan tilgang.</span><span class="sxs-lookup"><span data-stu-id="4e61d-121">Instead, a clearing account is used for this purpose.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e61d-122">Skráning og bókun fyrirframdagsettrar ávísunar skiptivöru fyrir viðskiptavin eða lánardrottin</span><span class="sxs-lookup"><span data-stu-id="4e61d-122">Register and post a replacement postdated check for a customer or a vendor</span></span></td>
<td>
<span data-ttu-id="4e61d-123">Ef upprunaleg ávísun til lánardrottins eða frá viðskiptavini tapast eða skemmist er hægt að gefa út endurnýjaða fyrirframdagsetta ávísun.</span><span class="sxs-lookup"><span data-stu-id="4e61d-123">If your original check to a vendor or from a customer is lost or damaged, you can issue a replacement postdated check.</span></span> <span data-ttu-id="4e61d-124">Þegar upplýsingar um ávísunina eru skráðar skal tilvísun í upprunalegu ávísunina fylgja með og gefa til kynna að nýja ávísunin komi í stað þeirra upprunalegu.</span><span class="sxs-lookup"><span data-stu-id="4e61d-124">When you register the check details, provide a reference to the original check, and indicate that the new check is a replacement for the original.</span></span> <span data-ttu-id="4e61d-125">Einnig er hægt að bóka endurnýjaða ávísun.</span><span class="sxs-lookup"><span data-stu-id="4e61d-125">You can also post the replacement check.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e61d-126">Flytja fyrirframdagsettar ávísanir viðskiptavinar til lánardrottins</span><span class="sxs-lookup"><span data-stu-id="4e61d-126">Transfer a customer postdated check to a vendor</span></span></td>
<td><span data-ttu-id="4e61d-127">Þegar tekið er á móti fyrirframdagsettri ávísun frá viðskiptavini er hægt að flytja þá ávísun til lánardrottins sem greiðsla.</span><span class="sxs-lookup"><span data-stu-id="4e61d-127">When you receive a postdated check from a customer, you can transfer that check to a vendor as a payment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4e61d-128">Jöfnun fyrirframdagsettar ávísunar viðskiptamanns eða lánardrottins</span><span class="sxs-lookup"><span data-stu-id="4e61d-128">Settle a postdated check for a customer or a vendor</span></span></td>
<td><span data-ttu-id="4e61d-129">Gera upp fyrirframdagsetta ávísun sem er bókuð á millilykil fyrir viðskiptamann eða lánardrottin þegar ávísunin gjaldfellur loks.</span><span class="sxs-lookup"><span data-stu-id="4e61d-129">Settle a postdated check that is posted to a bridging account for a customer or a vendor when the check finally matures.</span></span> <span data-ttu-id="4e61d-130">Þegar ávísun er jafnaður, er bankans að lokum debet- eða kreditfærður gagnvart millireikning sem notuð var áður.</span><span class="sxs-lookup"><span data-stu-id="4e61d-130">When the check is settled, the bank is finally debit or credit against the clearing account that was used earlier.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4e61d-131">Afturkalla fyrirframdagsetta ávísun fyrir lánardrottin</span><span class="sxs-lookup"><span data-stu-id="4e61d-131">Cancel a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="4e61d-132">Hægt er að hætta við bókaða fyrirframdagsetta ávísun í eftirfarandi aðstæðum: - Ávísuninni var skilað af bankanum.</span><span class="sxs-lookup"><span data-stu-id="4e61d-132">You can cancel a posted postdated check in these situations: - The check is returned by the bank.</span></span>
<span data-ttu-id="4e61d-133">- Ávísunin er notuð fyrir rangan reikning.</span><span class="sxs-lookup"><span data-stu-id="4e61d-133">- The check is applied to an incorrect invoice.</span></span>
<span data-ttu-id="4e61d-134">- Staðgreiðsla er framkvæmd í stað ávísunarinnar.</span><span class="sxs-lookup"><span data-stu-id="4e61d-134">- A cash payment is made against the check.</span></span>
  </td>
  </tr>
  <tr class="even">
  <td><span data-ttu-id="4e61d-135">Stöðva greiðslu fyrir fyrirframdagsettri ávísun</span><span class="sxs-lookup"><span data-stu-id="4e61d-135">Stop payment for a postdated check</span></span></td>
  <td><span data-ttu-id="4e61d-136">Hægt er að stöðva greiðslu á fyrirframdagsettu ávísuninni sem gefin var út á lánardrottinn vegna ástæðna svo sem ónógrar innistæðu á bankareikningnum, breytingum á skilmálum lánardrottins, sendingu á gölluðum vörum frá lánardrottni eða vöruskilum til lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="4e61d-136">You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor.</span></span> <span data-ttu-id="4e61d-137">Aðeins er hægt er að stöðva greiðslu vegna ávísana sem ekki er búið að innleysa.</span><span class="sxs-lookup"><span data-stu-id="4e61d-137">You can stop payment only on checks that haven’t cleared.</span></span></td>
  </tr>
  </tbody>
  </table>



<span data-ttu-id="4e61d-138">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="4e61d-138">For more information, see the following topics:</span></span>

[<span data-ttu-id="4e61d-139">Setja upp fyrirframdagsettar ávísanir</span><span class="sxs-lookup"><span data-stu-id="4e61d-139">Set up postdated checks</span></span>](tasks/set-up-postdated-checks.md)

[<span data-ttu-id="4e61d-140">Skrá og bóka fyrirframdagsetta ávísun fyrir viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="4e61d-140">Register and post a postdated check for a customer</span></span>](tasks/register-post-postdated-check-customer.md)

[<span data-ttu-id="4e61d-141">Gera upp fyrirframdagsetta ávísun frá viðskiptavini</span><span class="sxs-lookup"><span data-stu-id="4e61d-141">Settle a postdated check from a customer</span></span>](tasks/settle-postdated-check-customer.md)

[<span data-ttu-id="4e61d-142">Skrá og bóka fyrirframdagsetta ávísun fyrir lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="4e61d-142">Register and post a postdated check for a vendor</span></span>](tasks/register-post-postdated-check-vendor.md) 

[<span data-ttu-id="4e61d-143">Gera upp fyrirframdagsetta ávísun fyrir lánardrottin</span><span class="sxs-lookup"><span data-stu-id="4e61d-143">Settle a postdated check for a vendor</span></span>](tasks/settle-postdated-check-vendor.md)



