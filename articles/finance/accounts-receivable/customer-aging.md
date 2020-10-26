---
title: Aldursskýrsla viðskiptavinar
description: Aldursgreiningarskýrsla viðskiptavinar sýnir stöðu sem er á gjalddaga hjá viðskiptavinum, raðað eftir dagsetningabili eða aldursgreiningartímabili.
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 062e8972c879d770cc4106c2811cd4c16fff0446
ms.sourcegitcommit: 25909c6ad3616e4f75a2fe006057dda18d7cc856
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974862"
---
# <a name="customer-aging-report"></a><span data-ttu-id="b0b54-103">Aldursskýrsla viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="b0b54-103">Customer aging report</span></span> 

<span data-ttu-id="b0b54-104">Skýrslan **Aldursgreining viðskiptavinar** sýnir stöðu sem er á gjalddaga hjá viðskiptavinum, raðað eftir dagsetningabili eða aldursgreiningartímabili.</span><span class="sxs-lookup"><span data-stu-id="b0b54-104">The **Customer aging** report displays the balances that are due from customers, sorted by date interval, or aging period.</span></span>

<span data-ttu-id="b0b54-105">Þegar þessi skýrsla er búin til eru eftirfarandi sjálfgefnar færibreytur sýndar.</span><span class="sxs-lookup"><span data-stu-id="b0b54-105">When you generate this report, the following default parameters are displayed.</span></span> <span data-ttu-id="b0b54-106">Hægt er að nota þessar færibreytur til að sía gögnin sem verða sýnd í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="b0b54-106">You can use these parameters to filter the data that will be displayed on the report.</span></span> <span data-ttu-id="b0b54-107">Frekari upplýsingar er að finna í [Setja upp innheimtu](set-up-collections.md).</span><span class="sxs-lookup"><span data-stu-id="b0b54-107">For more information, see [Set up collections](set-up-collections.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0b54-108">Svæði</span><span class="sxs-lookup"><span data-stu-id="b0b54-108">Field</span></span></p></th>
<th><p><span data-ttu-id="b0b54-109">lýsing</span><span class="sxs-lookup"><span data-stu-id="b0b54-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0b54-110"><strong>Reikningsflokkun</strong></span><span class="sxs-lookup"><span data-stu-id="b0b54-110"><strong>Billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b54-111">Veljið eina eða fleiri reikningsflokkanir til að hafa með í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="b0b54-111">Select one or more billing classifications to include on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="b0b54-112">**Athugið:** Þessi stýring er einungis í boði ef skilgreiningarlykillinn <STRONG>Hið opinbera</STRONG> er valinn.</span><span class="sxs-lookup"><span data-stu-id="b0b54-112">**Note:** This control is available only if the <STRONG>Public Sector</STRONG> configuration key is selected.</span></span></P>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b54-113"><strong>Hafa með færslur án reikningsflokkunar</strong></span><span class="sxs-lookup"><span data-stu-id="b0b54-113"><strong>Include transactions without a billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b54-114">Ef þessi gátreitur er valinn verða allar færslur sem eru ekki með úthlutaða reikningsflokkun birtar í þessari skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b0b54-114">If this check box is selected, all transactions that do not have a billing classification assigned to them will be displayed on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="b0b54-115">**Athugið:** Þessi stýring er einungis í boði ef skilgreiningarlykillinn <STRONG>Hið opinbera</STRONG> er valinn.</span><span class="sxs-lookup"><span data-stu-id="b0b54-115">**Note:** This control is available only if the <STRONG>Public sector</STRONG> configuration key is selected.</span></span></P>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b54-116"><strong>Aldursgreining frá og með</strong></span><span class="sxs-lookup"><span data-stu-id="b0b54-116"><strong>Aging as of</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b54-117">Sláið inn dagsetninguna sem er notuð í núgildandi aldursgreiningarramma.</span><span class="sxs-lookup"><span data-stu-id="b0b54-117">Enter the date used on the current aging bucket.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b54-118"><strong>Staða þann</strong></span><span class="sxs-lookup"><span data-stu-id="b0b54-118"><strong>Balance as of</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b54-119">Færið inn dagsetningu til að skoða stöðu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="b0b54-119">Enter the date to view the customer balances for.</span></span> <span data-ttu-id="b0b54-120">Þetta er einnig þekkt sem lokadagsetning fyrir færslur.</span><span class="sxs-lookup"><span data-stu-id="b0b54-120">This is also known as a cutoff date for transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b54-121"><strong>Upphafsdagsetning</strong></span><span class="sxs-lookup"><span data-stu-id="b0b54-121"><strong>Start date</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b54-122">Færið inn dagsetningu sem er á fyrsta tímabilinu eða aldursgreiningartímabilinu sem á að hafa með í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="b0b54-122">Enter a date that is in the first period interval or aging period to include on the report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b54-123"><strong>Skilyrði</strong></span><span class="sxs-lookup"><span data-stu-id="b0b54-123"><strong>Criteria</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b54-124">Velja dagsetningartegundina sem skýrslan á að byggjast á.</span><span class="sxs-lookup"><span data-stu-id="b0b54-124">Select the type of date to base the report on.</span></span></p>
<ul>
<li><p><span data-ttu-id="b0b54-125"><strong>Færsludagsetning</strong> – Bókunardagsetning færslunnar.</span><span class="sxs-lookup"><span data-stu-id="b0b54-125"><strong>Transaction date</strong> – The posting date of the transactions.</span></span> <span data-ttu-id="b0b54-126">Til dæmis gæti þetta verið reikningsdagsetning sem er grunnurinn að útreikningi á gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="b0b54-126">For example, this might be an invoice date that is the basis for the calculation of the due date.</span></span></p></li>
<li><p><span data-ttu-id="b0b54-127"><strong>Gjalddagi</strong> – Gjalddagi færslunnar samkvæmt greiðsluskilmála.</span><span class="sxs-lookup"><span data-stu-id="b0b54-127"><strong>Due date</strong> – The due date of the transactions, based on the terms of payment.</span></span></p></li>
<li><p><span data-ttu-id="b0b54-128"><strong>Dagsetning skjals</strong> – Notandaskilgreind dagsetning skjals sem er grundvöllur fyrir útreikning gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="b0b54-128"><strong>Document date</strong> – A user-defined document date that is the basis for the calculation of the due date.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b54-129"><strong>Skilgreining aldurstímabils</strong></span><span class="sxs-lookup"><span data-stu-id="b0b54-129"><strong>Aging period definition</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b54-130">Velja skal skilgreiningu aldurstímabils</span><span class="sxs-lookup"><span data-stu-id="b0b54-130">Select an aging period definition.</span></span> <span data-ttu-id="b0b54-131">Reiturinn <strong>Tímabil</strong> er ekki notað ef valin er skilgreining aldurstímabils.</span><span class="sxs-lookup"><span data-stu-id="b0b54-131">The <strong>Interval</strong> field is not used if you select an aging period definition.</span></span></p>
<p><span data-ttu-id="b0b54-132">Skilgreiningar aldurstímabils sem eru með fleiri en sex aldurstímabil er ekki hægt að nota í prentuðu skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="b0b54-132">Aging period definitions that have more than six aging periods cannot be used on the printed report.</span></span></p>
<div class="alert">

<span data-ttu-id="b0b54-133">**Athugið:** Hægt er að setja upp aldursgreiningartímabil á síðunni <STRONG>Skilgreiningar aldurstímabila</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="b0b54-133">**Note:** You can set up aging periods on the <STRONG>Aging period definitions</STRONG> page.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b54-134"><strong>Prenta lýsingu á aldurstímabili</strong></span><span class="sxs-lookup"><span data-stu-id="b0b54-134"><strong>Print aging period description</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b54-135">Veljið <strong>Já</strong> til að taka með lýsingar á aldurstímabilum efst í hverjum dálki aldurstímabils í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="b0b54-135">Select <strong>Yes</strong> to include aging period descriptions at the top of each aging period column on the report.</span></span> <span data-ttu-id="b0b54-136">Veljið <strong>Nei</strong> til að prenta skýrsluna án dálkhausa.</span><span class="sxs-lookup"><span data-stu-id="b0b54-136">Select <strong>No</strong> to print the report without column headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b54-137"><strong>Bil</strong></span><span class="sxs-lookup"><span data-stu-id="b0b54-137"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b54-138">Skilgreinið tímabilið sem á að nota með því að færa inn númer dags- eða mánaðareininganna á hverju tímabili.</span><span class="sxs-lookup"><span data-stu-id="b0b54-138">Define the period to use by entering the number of the day or month units in each period.</span></span> <span data-ttu-id="b0b54-139">Til dæmis til að skoða aldursupplýsingar eftir viku skal færa inn 7 í þennan reit og velja <strong>Dagur</strong> í reitnum <strong>Dagur/Mán</strong>.</span><span class="sxs-lookup"><span data-stu-id="b0b54-139">For example, to view aging information by week, enter 7 in this field and select <strong>Day</strong> in the <strong>Day/Mth</strong> field.</span></span></p>
<div class="alert">

<span data-ttu-id="b0b54-140">**Athugaðu:** Upplýsingarnar sem eru færðar inn í þetta svæði eru eingöngu notaðar ef aldursgreiningarrammi hefur ekki verið valinn.</span><span class="sxs-lookup"><span data-stu-id="b0b54-140">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span> <span data-ttu-id="b0b54-141">Annars er prentstefnan skilgreind í skilgreiningu aldurstímabils.</span><span class="sxs-lookup"><span data-stu-id="b0b54-141">Otherwise, the printing direction is defined on the aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b54-142"><strong>Dagur/Mán.</strong></span><span class="sxs-lookup"><span data-stu-id="b0b54-142"><strong>Day/Mth</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b54-143">Veljið eininguna, annaðhvort <strong>Dagur</strong> eða <strong>Mánuður</strong>, sem er notuð til að skilgreina tímabilið í reitnum <strong>Tímabil</strong>.</span><span class="sxs-lookup"><span data-stu-id="b0b54-143">Select the unit, either <strong>Day</strong> or <strong>Month</strong>, that is used to define the period in the <strong>Interval</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b54-144"><strong>Stefna prentunar</strong></span><span class="sxs-lookup"><span data-stu-id="b0b54-144"><strong>Printing direction</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b54-145">Veljið hvort eigi að reikna út stöðu og prenta aldursgreiningarskýrslur fyrir gömul tímabil eða komandi tímabil.</span><span class="sxs-lookup"><span data-stu-id="b0b54-145">Select whether to calculate balances and print the aging report for past or future periods.</span></span> <span data-ttu-id="b0b54-146">Dagsetningarnar eru metnar miðað við dagsetninguna sem valin er í reitnum <strong>Staða þann</strong>.</span><span class="sxs-lookup"><span data-stu-id="b0b54-146">The dates are evaluated relative to the date that is selected in the <strong>Balance as on</strong> field.</span></span> <span data-ttu-id="b0b54-147">Veljið <strong>Afturábak</strong> til að sýna upplýsingar um liðin tímabil.</span><span class="sxs-lookup"><span data-stu-id="b0b54-147">Select <strong>Backward</strong> to show information for past periods.</span></span> <span data-ttu-id="b0b54-148">Veljið <strong>Áfram</strong> til að sýna upplýsingar um tímabil í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="b0b54-148">Select <strong>Forward</strong> to show information for future periods.</span></span></p>

<span data-ttu-id="b0b54-149">**Athugaðu:** Upplýsingarnar sem eru færðar inn í þetta svæði eru eingöngu notaðar ef aldursgreiningarrammi hefur ekki verið valinn.</span><span class="sxs-lookup"><span data-stu-id="b0b54-149">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b54-150"><strong>Upplýsingar</strong></span><span class="sxs-lookup"><span data-stu-id="b0b54-150"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b54-151">Veljið til að skrá færslurnar sem teknar eru með í stöðunum sem eru sýndar í þessari skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b0b54-151">Select to list the transactions that are included in the balances that are shown on the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b54-152"><strong>Taka með upphæðir í færslugjaldmiðli</strong></span><span class="sxs-lookup"><span data-stu-id="b0b54-152"><strong>Include amounts in transaction currency</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b54-153">Veljið til að taka með upphæð í færslugjaldmiðlinum til viðbótar við upphæð í bókhaldsgjaldmiðlinum.</span><span class="sxs-lookup"><span data-stu-id="b0b54-153">Select to include amounts in the transaction currency in addition to amounts in the accounting currency.</span></span> <span data-ttu-id="b0b54-154">Ef þessi gátreitur er ekki valinn eru upphæðir í þessari skýrslu aðeins birtar í bókhaldsgjaldmiðlinum.</span><span class="sxs-lookup"><span data-stu-id="b0b54-154">If this check box is not selected, the amounts on the report are displayed only in the accounting currency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b54-155"><strong>Neikvæð staða</strong></span><span class="sxs-lookup"><span data-stu-id="b0b54-155"><strong>Negative balance</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b54-156">Veljið til að hafa með viðskiptavinalykla sem eru með neikvæðar stöður.</span><span class="sxs-lookup"><span data-stu-id="b0b54-156">Select to include customer accounts that have negative balances.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b54-157"><strong>Undanskilja efnahagslykla sem standa á núlli</strong></span><span class="sxs-lookup"><span data-stu-id="b0b54-157"><strong>Exclude zero balance accounts</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b54-158">Veljið til að útiloka viðskiptavinalykla sem eru með núllstöðu.</span><span class="sxs-lookup"><span data-stu-id="b0b54-158">Select to exclude customer accounts that have a zero balance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b54-159"><strong>Greiðslustaða</strong></span><span class="sxs-lookup"><span data-stu-id="b0b54-159"><strong>Payment positioning</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b54-160">Velja til að birta greiðslur sem hafa ekki verið jafnaðar.</span><span class="sxs-lookup"><span data-stu-id="b0b54-160">Select to display payments that have not been settled.</span></span> <span data-ttu-id="b0b54-161">Þær eru birtar í fyrsta dálki skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="b0b54-161">These are displayed in the first column of the report.</span></span></p></td>
</tr>
</tbody>
</table>
