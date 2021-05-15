---
title: Skattur er bókaður í rangan fjárhagslykil í fylgiskjalinu
description: Í þessu efnisatriði veitir upplýsingar um úrræðaleit sem getur hjálpað til þegar skattur er bókaður á rangan fjárhagslykil í fylgiskjalinu.
author: qire
manager: beya
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0404d71f0492e188ed5da62387bb90a336e69c5a
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947657"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a><span data-ttu-id="dea23-103">Skattur er bókaður í rangan fjárhagslykil í fylgiskjalinu</span><span class="sxs-lookup"><span data-stu-id="dea23-103">Tax is posted to the wrong ledger account in the voucher</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dea23-104">Meðan á bókun stendur gæti skattur verið bókaður á rangan fjárhagslykil í fylgiskjalinu.</span><span class="sxs-lookup"><span data-stu-id="dea23-104">During posting, tax might be posted to the wrong ledger account in the voucher.</span></span> <span data-ttu-id="dea23-105">Til að leysa úr vandamálinu skal fylgja skrefunum í eftirfarandi hlutum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="dea23-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span> <span data-ttu-id="dea23-106">Dæmin í þessu efnisatriði nota sölupöntun sem viðskiptaskjal.</span><span class="sxs-lookup"><span data-stu-id="dea23-106">The examples in this topic use a sales order as the business document.</span></span>

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a><span data-ttu-id="dea23-107">Finndu skattkóðann fyrir ranglega bókaða skattfærslu</span><span class="sxs-lookup"><span data-stu-id="dea23-107">Find the tax code of the incorrectly posted tax transaction</span></span>

1. <span data-ttu-id="dea23-108">Á síðunni **Fylgiskjalafærslur** skal velja færsluna sem vinna á með og velja síðan **Bókaður virðisaukaskattur**.</span><span class="sxs-lookup"><span data-stu-id="dea23-108">On the **Voucher transactions** page, select the transaction that you want to work with, and then select **Posted sales tax**.</span></span>

    <span data-ttu-id="dea23-109">[![Hnappur bókaðs virðisaukaskatts á síðunni fyrir fylgiskjalsfærslu](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="dea23-109">[![Posted sales tax button on the Voucher transactions page](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span></span>

2. <span data-ttu-id="dea23-110">Farið yfir gildið í reitnum **VSK-kóði**.</span><span class="sxs-lookup"><span data-stu-id="dea23-110">Review the value in the **Sales tax code** field.</span></span> <span data-ttu-id="dea23-111">Í þessu dæmi er það **VSK 19**.</span><span class="sxs-lookup"><span data-stu-id="dea23-111">In this example, it's **VAT 19**.</span></span>

    <span data-ttu-id="dea23-112">[![Reiturinn VSK-kóði á síðunni Bókaður virðisaukaskattur](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="dea23-112">[![Sales tax code field on the Posted sales tax page](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span></span>

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a><span data-ttu-id="dea23-113">Athugaðu fjárhagsbókunarflokk skattkóðans</span><span class="sxs-lookup"><span data-stu-id="dea23-113">Check the ledger posting group of the tax code</span></span>

1. <span data-ttu-id="dea23-114">Farið í **Skattur** \> **Óbeinir skattar** \> **Söluskattur** \> **Söluskattflokkur**.</span><span class="sxs-lookup"><span data-stu-id="dea23-114">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
2. <span data-ttu-id="dea23-115">Finndu og veldu skattkóðann og farðu síðan yfir gildið í reitnum **Fjárhagsbókunarflokkur**.</span><span class="sxs-lookup"><span data-stu-id="dea23-115">Find and select the tax code, and then review the value in the **Ledger posting group** field.</span></span> <span data-ttu-id="dea23-116">Í þessu dæmi er það **VSK**.</span><span class="sxs-lookup"><span data-stu-id="dea23-116">In this example, it's **VAT**.</span></span>

    <span data-ttu-id="dea23-117">[![Reitur fjárhagsbókunarflokks á síðu VSK-kóða](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="dea23-117">[![Ledger posting group field on the Sales tax codes page](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span></span>

3. <span data-ttu-id="dea23-118">Gildið í svæðinu **Fjárhagsbókunarflokkur** er tengill.</span><span class="sxs-lookup"><span data-stu-id="dea23-118">The value in the **Ledger posting group** field is a link.</span></span> <span data-ttu-id="dea23-119">Veldu tengilinn til að skoða upplýsingar um stillingar hópsins.</span><span class="sxs-lookup"><span data-stu-id="dea23-119">To view the details of the group's configuration, select the link.</span></span> <span data-ttu-id="dea23-120">Einnig er hægt að velja og halda niðri (eða hægrismella) í reitnum og velja síðan **Skoða upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="dea23-120">Alternatively, select and hold (or right-click) in the field, and then select **View details**.</span></span>

    <span data-ttu-id="dea23-121">[![Skoða upplýsingar um skipun](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="dea23-121">[![View details command](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span></span>

4. <span data-ttu-id="dea23-122">Í reitnum **Útskattur** skal staðfesta að reikningsnúmerið sé rétt samkvæmt færslugerðinni.</span><span class="sxs-lookup"><span data-stu-id="dea23-122">In the **Sales tax payable** field, verify that the account number is correct, according to the transaction type.</span></span> <span data-ttu-id="dea23-123">Ef svo er ekki skal velja rétta lykilinn sem á að bóka á.</span><span class="sxs-lookup"><span data-stu-id="dea23-123">If it isn't, select the correct account to post to.</span></span> <span data-ttu-id="dea23-124">Í þessu dæmi er virðisaukaskattur sölupöntunarinnar færður á virðisaukaskattslyjkil 222200.</span><span class="sxs-lookup"><span data-stu-id="dea23-124">In this example, the sales tax of the sales order should be posted to sales tax payable account 222200.</span></span>

    <span data-ttu-id="dea23-125">[![Reitur útskatts á síðu fjárhagsbókunarflokks](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="dea23-125">[![Sales tax payable field on the Ledger posting groups page](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span></span>

    <span data-ttu-id="dea23-126">Í eftirfarandi töflu má finna upplýsingar um hvert svæði á síðunni **Fjárhagsbókunarflokkar**.</span><span class="sxs-lookup"><span data-stu-id="dea23-126">The following table provides information about each field on the **Ledger posting groups** page.</span></span>

    | <span data-ttu-id="dea23-127">Svæði</span><span class="sxs-lookup"><span data-stu-id="dea23-127">Field</span></span>                  | <span data-ttu-id="dea23-128">lýsing</span><span class="sxs-lookup"><span data-stu-id="dea23-128">Description</span></span> |
    |------------------------|-------------|
    | <span data-ttu-id="dea23-129">Útskattur</span><span class="sxs-lookup"><span data-stu-id="dea23-129">Sales tax payable</span></span>      | <span data-ttu-id="dea23-130">Aðallykil fyrir útskatt sem er til greiðslu til skattyfirvalda.</span><span class="sxs-lookup"><span data-stu-id="dea23-130">The main account for outgoing sales taxes that are payable to the tax authority.</span></span> |
    | <span data-ttu-id="dea23-131">Innskattur</span><span class="sxs-lookup"><span data-stu-id="dea23-131">Sales tax receivable</span></span>   | <span data-ttu-id="dea23-132">Aðallykill fyrir innskatt sem er móttekinn frá skattyfirvöldum.</span><span class="sxs-lookup"><span data-stu-id="dea23-132">The main account for incoming taxes that are received from the tax authority.</span></span> |
    | <span data-ttu-id="dea23-133">Kostnaður neysluskatts</span><span class="sxs-lookup"><span data-stu-id="dea23-133">Use tax expense</span></span>        | <span data-ttu-id="dea23-134">Aðallykillinn sem er notaður til að bóka frádráttarbæran neysluskatt sem lánardrottnar gera ekki kröfu um eða gefa upp til skattayfirvalda sem hluti af bakfærðum gjöldum vöru- og þjónustuskatts (ÞST)/Samræmdum virðisaukaskatti Evrópusambandsins.</span><span class="sxs-lookup"><span data-stu-id="dea23-134">The main account that is used to post deductible use taxes that vendors don't claim or report to the tax authority as part of European Union (EU) reverse charge Goods and Services Tax (GST)/Harmonized Sales Tax (HST).</span></span> <span data-ttu-id="dea23-135">**Neysluskattur** verður að vera valinn fyrir VSK-kóði í VSK-flokkur sem er notaður í færslunni.</span><span class="sxs-lookup"><span data-stu-id="dea23-135">**Use tax** must be selected for the sales tax code in the sales tax group that is used in the transaction.</span></span> <span data-ttu-id="dea23-136">Þetta svæði er ekki tiltækt ef **Reglur fyrir beitingu skattlagningu söluskatts** er valinn á síðunni **Færibreytur fjárhags**.</span><span class="sxs-lookup"><span data-stu-id="dea23-136">This field isn't available if **Apply sales tax taxation rules** is selected on the **General ledger parameters** page.</span></span> |
    | <span data-ttu-id="dea23-137">Neysluskattur út</span><span class="sxs-lookup"><span data-stu-id="dea23-137">Use tax payable</span></span>        | <span data-ttu-id="dea23-138">Aðallykillinn sem er notaður til að bóka neysluskatt á innleið sem greiða á skattayfirvöldum.</span><span class="sxs-lookup"><span data-stu-id="dea23-138">The main account that is used to post incoming use taxes that are payable to tax authorities.</span></span> |
    | <span data-ttu-id="dea23-139">Jöfnunarlykill</span><span class="sxs-lookup"><span data-stu-id="dea23-139">Settlement account</span></span>     | <span data-ttu-id="dea23-140">Aðallykillinn sem er notaður til að bóka nettóstöðu fjárhagslykla sem eru tilgreindir í reitunum **Útskattur** og **Innskattur**.</span><span class="sxs-lookup"><span data-stu-id="dea23-140">The main account that is used to post the net balance of the ledger accounts that are specified in the **Use tax payable** and **Sales tax receivable** fields.</span></span> |
    | <span data-ttu-id="dea23-141">Staðgreiðsluafsláttur lánardrottins</span><span class="sxs-lookup"><span data-stu-id="dea23-141">Vendor cash discount</span></span>   | <span data-ttu-id="dea23-142">Aðallykillinn sem er notaður til að bóka staðgreiðsluafslátt fyrir VSK-kóða sem tengjast þessum fjárhagsbókunarflokki.</span><span class="sxs-lookup"><span data-stu-id="dea23-142">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |
    | <span data-ttu-id="dea23-143">Staðgreiðsluafsláttur viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="dea23-143">Customer case discount</span></span> | <span data-ttu-id="dea23-144">Aðallykillinn sem er notaður til að bóka staðgreiðsluafslátt fyrir VSK-kóða sem tengjast þessum fjárhagsbókunarflokki.</span><span class="sxs-lookup"><span data-stu-id="dea23-144">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |

    <span data-ttu-id="dea23-145">Nánari upplýsingar er að finna í [Setja upp bókunarflokka virðisaukaskatts](tasks/set-up-ledger-posting-groups-sales-tax.md)</span><span class="sxs-lookup"><span data-stu-id="dea23-145">For more information, see, [Set up Ledger posting groups for sales tax](tasks/set-up-ledger-posting-groups-sales-tax.md)</span></span>

## <a name="debug-in-code-to-check-ledger-dimensions"></a><span data-ttu-id="dea23-146">Kema í kóða til að athuga fjárhagsvíddir</span><span class="sxs-lookup"><span data-stu-id="dea23-146">Debug in code to check ledger dimensions</span></span>

<span data-ttu-id="dea23-147">Í kóðanum er bókunarreikningurinn ákvarðaður af fjárhagsvíddinni.</span><span class="sxs-lookup"><span data-stu-id="dea23-147">In the code, the posting account is determined by the ledger dimension.</span></span> <span data-ttu-id="dea23-148">Fjárhagsvíddin vistar kenni aðgangs í gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="dea23-148">The ledger dimension saves the record ID of an account in the database.</span></span>

1. <span data-ttu-id="dea23-149">Fyrir sölupöntun skal bæta rofstað við í aðferðunum **Tax::saveAndPost()** and **Tax::post()**.</span><span class="sxs-lookup"><span data-stu-id="dea23-149">For a sales order, add a breakpoint at the **Tax::saveAndPost()** and **Tax::post()** methods.</span></span> <span data-ttu-id="dea23-150">Takið eftir gildi **\_ledgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="dea23-150">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="dea23-151">[![Dæmi um kóða sölupöntunar sem er með rofstað](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="dea23-151">[![Sales order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span></span>

    <span data-ttu-id="dea23-152">Fyrir innkaupapöntun skal bæta við rofstað við **TaxPost::saveAndPost()** og **TaxPost::postToTaxTrans()** aðferðirnar.</span><span class="sxs-lookup"><span data-stu-id="dea23-152">For a purchase order, add a breakpoint at the **TaxPost::saveAndPost()** and **TaxPost::postToTaxTrans()** methods.</span></span> <span data-ttu-id="dea23-153">Takið eftir gildi **\_ledgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="dea23-153">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="dea23-154">[![Dæmi um kóða innkaupapöntunar sem er með rofstað](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span><span class="sxs-lookup"><span data-stu-id="dea23-154">[![Purchase order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span></span>

2. <span data-ttu-id="dea23-155">Keyrðu eftirfarandi SQL-fyrirspurn til að finna birtingargildi reikningsins í gagnagrunninum, byggt á færslukenninu sem er vistað í fjárhagsvíddinni.</span><span class="sxs-lookup"><span data-stu-id="dea23-155">Run the following SQL query to find the display value of the account in the database, based on the record ID that is saved by the ledger dimension.</span></span>

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    <span data-ttu-id="dea23-156">[![Birta gildi færsluauðkennisins](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span><span class="sxs-lookup"><span data-stu-id="dea23-156">[![Display value of the record ID](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span></span>

3. <span data-ttu-id="dea23-157">Skoðaðu kallastakka til að finna hvar **_ledgerDimension** gildinu er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="dea23-157">Examine the callstack to find where the **_ledgerDimension** value is assigned.</span></span> <span data-ttu-id="dea23-158">Vanalega er gildið frá **TmpTaxWorkTrans**.</span><span class="sxs-lookup"><span data-stu-id="dea23-158">Usually, the value is from **TmpTaxWorkTrans**.</span></span> <span data-ttu-id="dea23-159">Í þessu tilviki ætti að bæta rofstað við **TmpTaxWorkTrans::insert()** og **TmpTaxWorkTrans::update()** til að sjá hvar gildinu er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="dea23-159">In this case, you should add a breakpoint at **TmpTaxWorkTrans::insert()** and **TmpTaxWorkTrans::update()** to find where the value assigned.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="dea23-160">Ákvarða hvort sérstilling sé til staðar</span><span class="sxs-lookup"><span data-stu-id="dea23-160">Determine whether customization exists</span></span>

<span data-ttu-id="dea23-161">Ef þú hefur lokið við skrefin í fyrri hlutum en hefur ekki getað leyst vandamálið skaltu komast að því hvort sérstillingar séu til staðar.</span><span class="sxs-lookup"><span data-stu-id="dea23-161">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="dea23-162">Ef engin sérstilling er til skal stofna þjónustubeiðni frá Microsoft til að fá frekari aðstoð.</span><span class="sxs-lookup"><span data-stu-id="dea23-162">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
