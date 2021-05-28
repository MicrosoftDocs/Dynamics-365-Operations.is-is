---
title: Gera upp TDS-greiðslur hjá TDS-lánardrottnayfirvaldi og mynda TDS-greiðslukvittun
description: Í þessu efnisatriði er útskýrt hvernig á að gera upp skatta sem dregnir eru frá upprunalegri greiðslu (TDS) til lánardrottnayfirvalds TDS.
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 5b77985a75d2930267cf94d6f218d53b47e6e705
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023335"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a><span data-ttu-id="a03e4-103">Gera upp TDS-greiðslur hjá TDS-lánardrottnayfirvaldi og mynda TDS-greiðslukvittun</span><span class="sxs-lookup"><span data-stu-id="a03e4-103">Settle TDS payments to TDS authority vendors and generate TDS challan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a03e4-104">Í þessu efnisatriði er útskýrt hvernig á að gera upp skatta sem dregnir eru frá upprunalegri greiðslu (TDS) til lánardrottnayfirvalds TDS.</span><span class="sxs-lookup"><span data-stu-id="a03e4-104">This topic explains how to settle Tax Deducted at Source (TDS) payments to TDS authority vendors.</span></span>

1. <span data-ttu-id="a03e4-105">Farið í **Viðskiptaskuldir \> Greiðslur \> Greiðslubók lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="a03e4-105">Go to **Accounts payable \> Payments \> Vendor payment journal**.</span></span>

    <span data-ttu-id="a03e4-106">[![Greiðslubókarsíða lánardrottins](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span><span class="sxs-lookup"><span data-stu-id="a03e4-106">[![Vendor payment journal page](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span></span>

2. <span data-ttu-id="a03e4-107">Á síðunni **Greiðslubók lánardrottins** skal velja **Ný** til að búa til nýja færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="a03e4-107">On the **Vendor payment journal** page, select **New** to create a journal line.</span></span>
3. <span data-ttu-id="a03e4-108">Í reitnum **Lykill** skal velja lánardrottnayfirvald TDS til að gera upp TDS-greiðslur við.</span><span class="sxs-lookup"><span data-stu-id="a03e4-108">In the **Account** field, select the TDS authority vendor to settle TDS payments to.</span></span>
4. <span data-ttu-id="a03e4-109">Veljið **Jöfnunarfærslur** til að opna síðuna **Jöfnunarfærslur** þar sem hægt er að skoða jafnaðar TDS-færslur fyrir lánardrottnayfirvald TDS.</span><span class="sxs-lookup"><span data-stu-id="a03e4-109">Select **Settlement transactions** to open the **Settlement transactions** page, where you can view the settled TDS transactions for the TDS authority vendor.</span></span>

    <span data-ttu-id="a03e4-110">Jafnaðar TDS-færslur fyrir jöfnunartímabil eru sýndar á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="a03e4-110">The settled TDS transactions for a settlement period are shown in the following way:</span></span>

    - <span data-ttu-id="a03e4-111">TDS-færslur þar sem eðli matsflokksins er **Fyrirtæki** eru sýndar sem ein færslulína.</span><span class="sxs-lookup"><span data-stu-id="a03e4-111">TDS transactions where the nature of assessee category is **Company** are shown as one transaction line.</span></span>
    - <span data-ttu-id="a03e4-112">TDS-færslur þar sem eðli matsflokksins er **HUF**, **Firma**, **Einstaklingur**, **AOP**, **BOI**, **Staðaryfirvald** eða **Annað** eru sýndar sem ein færslulína.</span><span class="sxs-lookup"><span data-stu-id="a03e4-112">TDS transactions where the nature of assessee category is **HUF**, **Firm**, **Individual**, **AOP**, **BOI**, **Local authority**, or **Others** are shown as one transaction line.</span></span>
    - <span data-ttu-id="a03e4-113">Reiturinn **Upphæð** sýnir heildarupphæð TDS sem á að greiða lánardrottnayfirvaldi TDS.</span><span class="sxs-lookup"><span data-stu-id="a03e4-113">The **Amount** field shows the total TDS amount that is due to be paid to the TDS authority vendor.</span></span>

5. <span data-ttu-id="a03e4-114">Veljið **Staðgreiðsluskattsfærslur** til að skoða ólíkar TDS-færslur sem eru hafðar með fyrir jöfnunarfærslurnar.</span><span class="sxs-lookup"><span data-stu-id="a03e4-114">Select **Withholding tax transactions** to view the different TDS transactions that are included for the settlement record.</span></span> <span data-ttu-id="a03e4-115">Hægt er að skoða skiptingu hverrar TDS-færslu sem hefur verið tekin með í jöfnunarferlið fyrir jöfnunartímabilið á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="a03e4-115">You can view the split of each TDS transaction that has been included in the settlement process for the settlement period on this page.</span></span>
6. <span data-ttu-id="a03e4-116">Í flipanum **Yfirlit** skal velja gátreitinn **Merkja** fyrir TDS-færslurnar sem á að gera upp við lánardrottnayfirvald TDS.</span><span class="sxs-lookup"><span data-stu-id="a03e4-116">On the **Overview** tab, select the **Mark** check box for the TDS transactions to settle to the TDS authority vendor.</span></span>

    <span data-ttu-id="a03e4-117">Flipinn **Yfirlit** sýnir eftirfarandi upplýsingar fyrir hverja opna TDS-færslu:</span><span class="sxs-lookup"><span data-stu-id="a03e4-117">The **Overview** tab shows the following information for each open TDS transaction:</span></span>

    - <span data-ttu-id="a03e4-118">**Dagsetning** – Færsludagsetning TDS.</span><span class="sxs-lookup"><span data-stu-id="a03e4-118">**Date** – The TDS transaction date.</span></span>
    - <span data-ttu-id="a03e4-119">**Fylgiskjal** – Fylgiskjalsnúmerið.</span><span class="sxs-lookup"><span data-stu-id="a03e4-119">**Voucher** – The voucher number.</span></span>
    - <span data-ttu-id="a03e4-120">**Uppruni** – Einingin sem TDS-færslan er bókuð í.</span><span class="sxs-lookup"><span data-stu-id="a03e4-120">**Source** – The module that the TDS transaction is posted in.</span></span>
    - <span data-ttu-id="a03e4-121">**Söluaðili/viðskiptavinur** – Númer lánardrottins eða viðskiptavinalykils sem TDS er dregið frá.</span><span class="sxs-lookup"><span data-stu-id="a03e4-121">**Vendor/Customer** – The vendor or customer account number that the TDS is deducted from.</span></span>
    - <span data-ttu-id="a03e4-122">**Heiti aðila sem dregið er frá** – Heiti lánardrottins eða viðskiptavinar sem TDS er dregið frá.</span><span class="sxs-lookup"><span data-stu-id="a03e4-122">**Name of deductee/party** – The name of the vendor or customer that the TDS is deducted from.</span></span>
    - <span data-ttu-id="a03e4-123">**Eðli mats** – Eðli matsflokks sem aðilinn sem dregið er frá tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="a03e4-123">**Nature of assessee** – The nature of assessee category that the deductee belongs to.</span></span>
    - <span data-ttu-id="a03e4-124">**Upphæð** – Upphæð reiknings sem TDS var reiknað fyrir.</span><span class="sxs-lookup"><span data-stu-id="a03e4-124">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="a03e4-125">**Skattupphæð** – TDS-upphæð sem reiknuð var fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="a03e4-125">**Tax amount** – The TDS amount that was calculated for the transaction.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a03e4-126">Hreinsið gátreitinn **Merkja** fyrir allar TDS-færslur sem á ekki að jafna gagnvart lánardrottnayfirvaldi TDS.</span><span class="sxs-lookup"><span data-stu-id="a03e4-126">Clear the **Mark** check box for any TDS transactions that should not be settled to the TDS authority vendor.</span></span>

    <span data-ttu-id="a03e4-127">Í flipanum **Almennt** sýnir reiturinn **PAN** varanlegt lykilnúmer (PAN) frádráttaraðilans.</span><span class="sxs-lookup"><span data-stu-id="a03e4-127">On the **General** tab, the **PAN** field shows the permanent account number (PAN) of the deductee.</span></span> <span data-ttu-id="a03e4-128">Reiturinn **Dagsetning** sýnir dagsetningu TDS-útreiknings og reiturinn **Gildi** sýnir heildarprósentuna sem var notuð í TDS-útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="a03e4-128">The **Date** field shows the date of the TDS calculation, and the **Value** field shows the total percentage that was used for the TDS calculation.</span></span>

7. <span data-ttu-id="a03e4-129">Veldu **skjámynd** til að skoða fylgiskjalsfærslur fyrir TDS-færsluna.</span><span class="sxs-lookup"><span data-stu-id="a03e4-129">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
8. <span data-ttu-id="a03e4-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a03e4-130">Close the page.</span></span>
10. <span data-ttu-id="a03e4-131">Veljið **Þættir staðgreiðsluskatts** til að opna síðuna **Þættir staðgreiðsluskatts** þar sem hægt er að skoða TDS sem var reiknað fyrir hvern TDS-skattþátt fyrir tiltekinn TDS-skattkóða.</span><span class="sxs-lookup"><span data-stu-id="a03e4-131">Select **Withholding tax components** to open the **Withholding tax components** page, where you can view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>

    <span data-ttu-id="a03e4-132">Í flipanum **Yfirlit** sýnir reiturinn **Skattþáttur** TDS-skattþáttinn sem var notaður fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="a03e4-132">On the **Overview** tab, the **Tax component** field shows the TDS tax component that was used for the transaction.</span></span> <span data-ttu-id="a03e4-133">Reiturinn **Upphæð** sýnir TDS-upphæðina sem var reiknuð út fyrir TDS-skattþáttinn í grunngjaldmiðlinum.</span><span class="sxs-lookup"><span data-stu-id="a03e4-133">The **Amount** field shows the TDS amount that was calculated for the TDS tax component, in the base currency.</span></span> <span data-ttu-id="a03e4-134">Reiturinn **Uppsöfnuð upphæð** sýnir heildarupphæð TDS sem var reiknuð út fyrir TDS-skattþáttinn fyrir allar jafnaðar færslur.</span><span class="sxs-lookup"><span data-stu-id="a03e4-134">The **Accumulated amount** field shows the total TDS amount that was calculated for the TDS tax component for all settled transactions.</span></span>

    <span data-ttu-id="a03e4-135">Í flipanum **Upphæð** sýnir hlutinn **Sjálfgefinn gjaldmiðill** TDS-upphæðina sem var reiknuð fyrir TDS-skattþáttinn í sjálfgefna gjaldmiðlinum.</span><span class="sxs-lookup"><span data-stu-id="a03e4-135">On the **Amount** tab, the **Default currency** section shows the TDS amount that was calculated for the TDS tax component, in the default currency.</span></span> <span data-ttu-id="a03e4-136">Hlutinn **Aukagjaldmiðill** sýnir upphæðina í aukagjaldmiðlinum.</span><span class="sxs-lookup"><span data-stu-id="a03e4-136">The **Secondary currency** section shows the amount in the secondary currency.</span></span>

11. <span data-ttu-id="a03e4-137">Lokið síðunni **Þættir staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="a03e4-137">Close the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="a03e4-138">Takið eftir að á síðunni **Breytingar á opnum færslum**, í reitnum **Upphæð**, er heildarupphæð sem á að jafna gagnvart lánardrottnayfirvaldi TDS fyrir jöfnunartímabilið uppfærð.</span><span class="sxs-lookup"><span data-stu-id="a03e4-138">On the **Open transaction editing** page, in the **Amount** field, notice that the total amount to settle to the TDS authority vendor for the settlement period is updated.</span></span>
13. <span data-ttu-id="a03e4-139">Til að jafna TDS-færslur mismunandi TDS-jöfnunartímabila gagnvart lánardrottnayfirvaldi TDS skal velja gátreitinn **Merkja** fyrir færslurnar.</span><span class="sxs-lookup"><span data-stu-id="a03e4-139">To settle the TDS transactions of different TDS settlement periods to the TDS authority vendor, select the **Mark** check box for the transactions.</span></span>
14. <span data-ttu-id="a03e4-140">Lokið síðunni **Breytingar á opnum færslum**.</span><span class="sxs-lookup"><span data-stu-id="a03e4-140">Close the **Open transaction editing** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a03e4-141">Ef aðeins fáeinar færslur eru valdar fyrir jöfnunina á síðunni **Staðgreiðsluskattsfærslur** verður heildarupphæð TDS á völdum færslum uppfærð í reitnum **Leiðrétting** á síðunni **Breytingar á opnum færslum**.</span><span class="sxs-lookup"><span data-stu-id="a03e4-141">If only a few transactions are selected for settlement on the **Withholding tax transactions** page, the total TDS amount of the selected transactions is updated in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="a03e4-142">Leiðréttingarupphæðin er uppfærð í færslubókarlínunni á síðunni **Færslubókarfylgiskjal** og síðunni **Breytingar á opnum færslum** er lokað.</span><span class="sxs-lookup"><span data-stu-id="a03e4-142">The correction amount is updated on the journal line on the **Journal voucher** page, and the **Open transaction editing** page is closed.</span></span>

    <span data-ttu-id="a03e4-143">Á síðunni **Færslubókarfylgiskjal** sýnir reiturinn **Debetfærsla** heildarupphæðina sem greiða á lánardrottnayfirvaldi TDS.</span><span class="sxs-lookup"><span data-stu-id="a03e4-143">On the **Journal voucher** page, the **Debit** field shows the total amount to pay to the TDS authority vendor.</span></span>

15. <span data-ttu-id="a03e4-144">Færið inn upplýsingar um mótlykilinn.</span><span class="sxs-lookup"><span data-stu-id="a03e4-144">Enter the offset account details.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a03e4-145">Ef TDS-færslur eru með mismunandi skattlykilnúmer (TAN) verða færslubókarlínur stofnaðar fyrir hvert TAN á síðunni **Færslubókarfylgiskjal**.</span><span class="sxs-lookup"><span data-stu-id="a03e4-145">If TDS transactions have different Tax Account Numbers (TANs), journal lines are created per TAN on the **Journal voucher** page.</span></span>

16. <span data-ttu-id="a03e4-146">Í flipanum **Greiðsluþóknun**, í reitnum **Kenni þóknunar**, skal velja kenni þóknunar sem er með gerð þóknunar sem **Vextir** eða **Annað** til að rukka greiðsluþóknun fyrir seinkaðar greiðslur sem eru greiddar lánardrottnayfirvaldi TDS.</span><span class="sxs-lookup"><span data-stu-id="a03e4-146">On the **Payment fee** tab, in the **Fee ID** field, select a fee ID that has a fee type of **Interest** or **Others** to charge the payment fee for delayed payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="a03e4-147">Í flipanum **Skattaupplýsingar**, í hlutanum **Fyrirtækjaupplýsingar**, sýnir reiturinn **Heiti** nafn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="a03e4-147">On the **Tax information** tab, in the **Company information** section, the **Name** field shows the company name.</span></span> <span data-ttu-id="a03e4-148">Í hlutanum **Staðgreiðsluskattur** sýnir reiturinn **Skattlykilnúmer (TAN)** TAN sem er hengt við færslulínuna.</span><span class="sxs-lookup"><span data-stu-id="a03e4-148">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the TAN that is attached to the transaction line.</span></span>

17. <span data-ttu-id="a03e4-149">Villuleita og bóka færslubók.</span><span class="sxs-lookup"><span data-stu-id="a03e4-149">Validate and post the journal.</span></span>
18. <span data-ttu-id="a03e4-150">Veljið **Staðgreiðsluskattur \> Upplýsingar um greiðslukvittun** til að færa inn upplýsingar um greiðslukvittun vegna færslunnar.</span><span class="sxs-lookup"><span data-stu-id="a03e4-150">Select **Withholding tax \> Challan information** to enter the challan details for the transaction.</span></span>

    <span data-ttu-id="a03e4-151">Reiturinn **Fylgiskjal** sýnir fylgiskjalsnúmer færslunnar.</span><span class="sxs-lookup"><span data-stu-id="a03e4-151">The **Voucher** field shows the voucher number of the transaction.</span></span>
    
19. <span data-ttu-id="a03e4-152">Veljið gátreitinn **TDS lagt inn með bókarfærslu** ef TDS-upphæðin er lögð inn með því að nota bókarfærslu.</span><span class="sxs-lookup"><span data-stu-id="a03e4-152">Select the **TDS deposited by book entry** check box if the TDS amount is deposited by using book entry.</span></span>
20. <span data-ttu-id="a03e4-153">Í reitnum **Númer greiðslukvittunar** skal færa inn númer greiðslukvittunar sem er notuð til að greiða lánardrottnayfirvaldi TDS.</span><span class="sxs-lookup"><span data-stu-id="a03e4-153">In the **Challan number** field, enter the challan number that is used to make the payment to the TDS authority vendor.</span></span>
21. <span data-ttu-id="a03e4-154">Í reitinn **Dagsetning** skal færa inn dagsetningu greiðslukvittunar.</span><span class="sxs-lookup"><span data-stu-id="a03e4-154">In the **Date** field, enter the challan date.</span></span>
22. <span data-ttu-id="a03e4-155">Í reitnum **Heiti banka** skal velja heiti bankans sem greiða á TDS-upphæðina til vegna lánardrottnayfirvalds TDS sem leggja á inn á.</span><span class="sxs-lookup"><span data-stu-id="a03e4-155">In the **Bank name** field, select the name of the bank that the TDS amount that is payable to the TDS authority vendor should be deposited to.</span></span> <span data-ttu-id="a03e4-156">Þessi reitur sýnir alla bankareikninga sem settir voru upp fyrir lánardrottnayfirvald TDS á **Viðskiptaskuldir \> Allir lánardrottnar \> Uppsetning \> Bankareikningar**.</span><span class="sxs-lookup"><span data-stu-id="a03e4-156">This field lists all the bank accounts that were set up for the TDS authority vendor at **Accounts payable \> All vendors \> Set up \> Bank accounts**.</span></span>
23. <span data-ttu-id="a03e4-157">Í reitinn **BSR-kóði** skal færa inn BSR-kóða (Basic Statistical Return) bankans.</span><span class="sxs-lookup"><span data-stu-id="a03e4-157">In the **BSR code** field, enter the Basic Statistical Return (BSR) code of the bank.</span></span>
24. <span data-ttu-id="a03e4-158">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a03e4-158">Close the page.</span></span>

### <a name="example"></a><span data-ttu-id="a03e4-159">Dæmi</span><span class="sxs-lookup"><span data-stu-id="a03e4-159">Example</span></span>

<span data-ttu-id="a03e4-160">Tímabilið 01/04/2009 er gert upp fyrir TDS-hlutaflokkinn **Leiga** með því að nota reglubundið TDS-uppgjörsferli.</span><span class="sxs-lookup"><span data-stu-id="a03e4-160">The period 04/01/2009 is settled for the **Rent** TDS component group by using the periodic TDS settlement process.</span></span> <span data-ttu-id="a03e4-161">Heildarupphæð TDS sem nemur 141.625,00 er bókuð á lykil lánardrottnayfirvalds TDS fyrir TDS-uppgjörstímabil.</span><span class="sxs-lookup"><span data-stu-id="a03e4-161">The total TDS amount of 141,625.00 is posted to the TDS vendor authority account for the TDS settlement period.</span></span> <span data-ttu-id="a03e4-162">Hægt er að skoða þessa upphæð í reitnum **Upphæð** á síðunni **Breytingar á opnum færslum** fyrir lánardrottnayfirvald TDS.</span><span class="sxs-lookup"><span data-stu-id="a03e4-162">You can view this amount in the **Amount** field on the **Open transaction editing** page for the TDS authority vendor.</span></span>

<span data-ttu-id="a03e4-163">Ef valið er **Staðgreiðsluskattsfærslur** til að skoða mismunandi TDS-færslur sem voru gerðar upp fyrir tímabilið, birtast eftirfarandi upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="a03e4-163">If you select **Withholding tax transactions** to view the different TDS transactions that were settled for the period, the following information is shown.</span></span>

| <span data-ttu-id="a03e4-164">TDS upphæð</span><span class="sxs-lookup"><span data-stu-id="a03e4-164">TDS amount</span></span> |
|------------|
| <span data-ttu-id="a03e4-165">16,995.00</span><span class="sxs-lookup"><span data-stu-id="a03e4-165">16,995.00</span></span>  |
| <span data-ttu-id="a03e4-166">22,660.00</span><span class="sxs-lookup"><span data-stu-id="a03e4-166">22,660.00</span></span>  |
| <span data-ttu-id="a03e4-167">28,325.00</span><span class="sxs-lookup"><span data-stu-id="a03e4-167">28,325.00</span></span>  |
| <span data-ttu-id="a03e4-168">16,995.00</span><span class="sxs-lookup"><span data-stu-id="a03e4-168">16,995.00</span></span>  |
| <span data-ttu-id="a03e4-169">28,325.00</span><span class="sxs-lookup"><span data-stu-id="a03e4-169">28,325.00</span></span>  |
| <span data-ttu-id="a03e4-170">16,995.00</span><span class="sxs-lookup"><span data-stu-id="a03e4-170">16,995.00</span></span>  |
| <span data-ttu-id="a03e4-171">11,330.00</span><span class="sxs-lookup"><span data-stu-id="a03e4-171">11,330.00</span></span>  |

<span data-ttu-id="a03e4-172">Fyrir ákveðna TDS-upphæð er hægt að velja **Þættir staðgreiðsluskatts** til að skoða TDS sem var reiknað fyrir hvern TDS-skattaþátt fyrir ákveðinn TDS-skattkóða.</span><span class="sxs-lookup"><span data-stu-id="a03e4-172">For a specific TDS amount, you can select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span> <span data-ttu-id="a03e4-173">Í þessu dæmi er valið **Þættir staðgreiðsluskatts** fyrir TDS-upphæðina 16.995,00.</span><span class="sxs-lookup"><span data-stu-id="a03e4-173">For this example, you select **Withholding tax components** for the TDS amount 16,995.00.</span></span> <span data-ttu-id="a03e4-174">Skattupphæðin sem reiknuð var í hvern þátt í færslunni kemur fram.</span><span class="sxs-lookup"><span data-stu-id="a03e4-174">The tax amount that was calculated per component for the transaction is shown.</span></span>

| <span data-ttu-id="a03e4-175">Skatthluti</span><span class="sxs-lookup"><span data-stu-id="a03e4-175">Tax component</span></span> | <span data-ttu-id="a03e4-176">Upphæð</span><span class="sxs-lookup"><span data-stu-id="a03e4-176">Amount</span></span>    | <span data-ttu-id="a03e4-177">Uppsöfnuð upphæð</span><span class="sxs-lookup"><span data-stu-id="a03e4-177">Accumulated amount</span></span> |
|---------------|-----------|--------------------|
| <span data-ttu-id="a03e4-178">SNERTIMÖRK:</span><span class="sxs-lookup"><span data-stu-id="a03e4-178">TDS</span></span>           | <span data-ttu-id="a03e4-179">1,5000.00</span><span class="sxs-lookup"><span data-stu-id="a03e4-179">1,5000.00</span></span> | <span data-ttu-id="a03e4-180">125,000.00</span><span class="sxs-lookup"><span data-stu-id="a03e4-180">125,000.00</span></span>         |
| <span data-ttu-id="a03e4-181">Álag </span><span class="sxs-lookup"><span data-stu-id="a03e4-181">Surcharge</span></span>     | <span data-ttu-id="a03e4-182">1,500.00</span><span class="sxs-lookup"><span data-stu-id="a03e4-182">1,500.00</span></span>  | <span data-ttu-id="a03e4-183">12,500.00</span><span class="sxs-lookup"><span data-stu-id="a03e4-183">12,500.00</span></span>          |
| <span data-ttu-id="a03e4-184">PE-Cess</span><span class="sxs-lookup"><span data-stu-id="a03e4-184">PE-Cess</span></span>       | <span data-ttu-id="a03e4-185">330.00</span><span class="sxs-lookup"><span data-stu-id="a03e4-185">330.00</span></span>    | <span data-ttu-id="a03e4-186">2,750.00</span><span class="sxs-lookup"><span data-stu-id="a03e4-186">2,750.00</span></span>           |
| <span data-ttu-id="a03e4-187">SHE Cess</span><span class="sxs-lookup"><span data-stu-id="a03e4-187">SHE Cess</span></span>      | <span data-ttu-id="a03e4-188">165.00</span><span class="sxs-lookup"><span data-stu-id="a03e4-188">165.00</span></span>    | <span data-ttu-id="a03e4-189">1,375.00</span><span class="sxs-lookup"><span data-stu-id="a03e4-189">1,375.00</span></span>           |

<span data-ttu-id="a03e4-190">Ef aðeins voru valdar TDS-upphæðirnar 16.995,00, 22.660,00 og 28.325,00 fyrir uppgjörið á síðunni **Staðgreiðsluskattar**, er heildarupphæð jöfnunar sýnd sem **67.980,00** í reitnum **Leiðrétting** á síðunni **Breytingar á opnum færslum**.</span><span class="sxs-lookup"><span data-stu-id="a03e4-190">If you selected only the TDS amounts 16,995.00, 22,660.00, and 2,8325.00 for settlement on the **Withholding tax transactions** page, the total amount for settlement is shown as **67,980.00** in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="a03e4-191">Ef þessi færsla er merkt fyrir jöfnun og síðuan **Breytingar á opnum færslum** er lokuð, er upphæðin **67.980,00** sýnd í reitnum **Debetfærsla** á síðunni **Fylgiskjal færslubókar**.</span><span class="sxs-lookup"><span data-stu-id="a03e4-191">If this transaction is marked for settlement, and the **Open transaction editing** page is closed, the amount **67,980.00** is shown in the **Debit** field on the **Journal voucher** page.</span></span>

<span data-ttu-id="a03e4-192">Nú er hægt að bóka dagbókina og búa til TDS challan.</span><span class="sxs-lookup"><span data-stu-id="a03e4-192">You can now post the journal and generate the TDS challan.</span></span>

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a><span data-ttu-id="a03e4-193">Leiðrétting á fyrirframgreiðslum sem greiddar eru lánardrottnayfirvöldum TDS</span><span class="sxs-lookup"><span data-stu-id="a03e4-193">Adjustment of advance payments that are made to TDS authority vendors</span></span>

<span data-ttu-id="a03e4-194">Til að breyta fyrirframgreiðslu sem var greidd lánardrottnayfirvaldi TDS yfir í raunverulega greiðslu skal fara í **Viðskiptaskuldir \> Lánardrottnar \> Allir lánardrottnar \> Breytingar á færslum**.</span><span class="sxs-lookup"><span data-stu-id="a03e4-194">To adjust an advance payment that was made to the TDS authority vendor to an actual payment, go to **Accounts payable \> Vendors \> All vendors \> Transactions editing**.</span></span> <span data-ttu-id="a03e4-195">Ef raunveruleg greiðsla sem er innt af hendi fer umfram fyrirframgreiðsluna verða tvö númer greiðslukvittunar búin til fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="a03e4-195">If the actual payment that is made exceeds the advance payment, two challan numbers are generated for the transaction.</span></span> <span data-ttu-id="a03e4-196">Hins vegar er aðeins fyrsta númer greiðslukvittunarinnar sýnt í fyrirspurn TDS.</span><span class="sxs-lookup"><span data-stu-id="a03e4-196">However, only the first challan number is shown in the TDS inquiry.</span></span>
