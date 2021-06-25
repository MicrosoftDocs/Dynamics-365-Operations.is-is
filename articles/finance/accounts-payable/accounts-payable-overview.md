---
title: Yfirlit yfir skilgreiningu viðskiptaskulda
description: Þessi grein lýsir þeim síðum sem þú notar til að setja upp grundvallaraðgerðir og valfrjálsar aðgerðir fyrir viðskiptaskuldir. Hún lýsir einnig uppsetningarskrefum sem þú verður að ljúka áður en þú byrjar að setja upp viðskiptaskuldir.
author: abruer
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: roschlom
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0edc2fcbde536e98fa3ce3567c2c8fdf3fc864ad
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188783"
---
# <a name="configure-accounts-payable-overview"></a><span data-ttu-id="15cef-104">Yfirlit yfir skilgreiningu viðskiptaskulda</span><span class="sxs-lookup"><span data-stu-id="15cef-104">Configure Accounts payable overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15cef-105">Þessi grein lýsir þeim síðum sem þú notar til að setja upp grundvallaraðgerðir og valfrjálsar aðgerðir fyrir viðskiptaskuldir.</span><span class="sxs-lookup"><span data-stu-id="15cef-105">This article describes the pages that you use to set up basic and optional functionality for Accounts payable.</span></span> <span data-ttu-id="15cef-106">Hún lýsir einnig uppsetningarskrefum sem þú verður að ljúka áður en þú byrjar að setja upp viðskiptaskuldir.</span><span class="sxs-lookup"><span data-stu-id="15cef-106">It also describes setup steps that you must complete before you start to set up Accounts payable.</span></span>

## <a name="prerequisites-for-accounts-payable-setup"></a><span data-ttu-id="15cef-107">Skilyrði fyrir uppsetningu viðskiptaskulda</span><span class="sxs-lookup"><span data-stu-id="15cef-107">Prerequisites for Accounts payable setup</span></span>

<span data-ttu-id="15cef-108">Áður en hægt er að setja upp viðskiptaskuldir, verður að ljúka eftirfarandi uppsetningu:</span><span class="sxs-lookup"><span data-stu-id="15cef-108">Before you can set up Accounts payable, you must complete the following setup:</span></span>

-   <span data-ttu-id="15cef-109">Í Fjárhag</span><span class="sxs-lookup"><span data-stu-id="15cef-109">In General ledger:</span></span>
    -   <span data-ttu-id="15cef-110">Ef ætlunin er að nota greiðslubók þarf að setja upp greiðslubækur.</span><span class="sxs-lookup"><span data-stu-id="15cef-110">If you plan to use payment journals, set up payment journals.</span></span>
    -   <span data-ttu-id="15cef-111">Ef ætlunin er að keyra gengisleiðréttingar þarf að setja upp gjaldmiðilskóða í síðuna Gjaldmiðlum, setja upp gerðir gengis á síðu gerðir gengis og setja upp gengi gjaldmiðla á síðu gengi Gjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="15cef-111">If you plan to run exchange rate adjustments, set up currency codes on the Currencies page, set up exchange rate types on the Exchange rate types page, and set up currency exchange rates on the Currency exchange rates page.</span></span>
-   <span data-ttu-id="15cef-112">Í reiðufjár- og bankastjórnun, eru settir upp bankareikningar til þess að nota með greiðsluháttum.</span><span class="sxs-lookup"><span data-stu-id="15cef-112">In Cash and bank management, set up bank accounts to use with methods of payment.</span></span>

## <a name="setup-pages-for-accounts-payable"></a><span data-ttu-id="15cef-113">Uppsetningarsíður fyrir viðskiptaskuldir</span><span class="sxs-lookup"><span data-stu-id="15cef-113">Setup pages for Accounts payable</span></span>

<span data-ttu-id="15cef-114">Notið eftirfarandi síður til þess að setja upp grundvallaraðgerðir viðskiptaskulda fyrir hvert lögaðila.</span><span class="sxs-lookup"><span data-stu-id="15cef-114">Use the following pages to set up the basic functionality of Accounts payable for each legal entity.</span></span> <span data-ttu-id="15cef-115">Síðum er raðað í ráðlagðri röð fyrir uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="15cef-115">The pages are listed in the recommended order of setup.</span></span> <span data-ttu-id="15cef-116">Hægt er stofna sniðmát úr fyrstu færslunum sem eru stofnaðar, til þess að einfalda uppsetningarferlið.</span><span class="sxs-lookup"><span data-stu-id="15cef-116">To make the setup process easier, you can create templates from the first records that you create.</span></span> <span data-ttu-id="15cef-117">Í sniðmáti eru yfirleitt færslur færðar inn í mörgum svæðum til að endurspegla aðgerðirnar sem fyrirtækið vill innleiða fyrir tiltekna gerð lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="15cef-117">In a template, values are typically entered in many fields to reflect the features that the organization wants to implement for a particular type of vendor.</span></span>
1.  <span data-ttu-id="15cef-118">Á síðunni greiðsluskilmálar, Skilgreinið greiðsluskilmála sem er úthlutað á sölupantanir, innkaupapantanir og viðskiptavinur, og lánardrottna, og ákvarða gjalddaga reikninga.</span><span class="sxs-lookup"><span data-stu-id="15cef-118">On the Terms of payment page, define the terms of payment that you assign to sales orders, purchase orders, customers, and vendors, and that determine invoice due dates.</span></span> <span data-ttu-id="15cef-119">Nánari upplýsingar er að finna í [Skilgreina greiðsluþóknanir lánardrottna](tasks/define-vendor-payment-fees.md).</span><span class="sxs-lookup"><span data-stu-id="15cef-119">For more information, see [Define vendor payment fees](tasks/define-vendor-payment-fees.md).</span></span>
2.  <span data-ttu-id="15cef-120">Á greiðsluaðferðir - lánardrottnar síðu, Stofna og viðhalda upplýsingar um hvernig fyrirtækið greiðir lánardrottnum.</span><span class="sxs-lookup"><span data-stu-id="15cef-120">On the Methods of payment - vendors page, create and maintain information about how the organization pays its vendors.</span></span>
3.  <span data-ttu-id="15cef-121">Á síðunni lánardrottnaflokkur, stofnið og viðhaldið lánardrottnaflokkum sem deila mikilvægum færibreytum fyrir bókun, greiðslu og jöfnun, skýrslugerð og spár.</span><span class="sxs-lookup"><span data-stu-id="15cef-121">On the Vendor groups page, create and maintain groups of vendors that share important parameters for posting, settlement and payment, reporting, and forecasting.</span></span>
4.  <span data-ttu-id="15cef-122">Á bókunarreglu lánardrottins síðu, skal skilgreina hvernig lánardrottnafærslur eru bókaðar í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="15cef-122">On the Vendor posting profiles page, define how vendor transactions are posted to the general ledger.</span></span>
5.  <span data-ttu-id="15cef-123">Á færibreytusíðum viðskiptaskulda skal setja upp sjálfgefnar stillingar sem eru notaðar ef nánari stillingar eru ekki tilgreindar, færibreytur fyrir ýmsar aðgerðir og ýmsar númeraraðir fyrir viðskiptaskuldir.</span><span class="sxs-lookup"><span data-stu-id="15cef-123">On the Accounts payable parameters page, set up default settings that are applied if a more specific setting isn't specified, parameters for various kinds of functionality, and the various number sequences for Accounts payable.</span></span>
6.  <span data-ttu-id="15cef-124">Á Síðunni uppsetning sniðs, skal Skilgreina snið ýmissa skjala sem tengjast lánardrottnum og eru notuð innan fyrirtækisins til þess að rekja móttöku frá lánardrottnum og færa inn ástæður fyrir greiðsluflæði til lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="15cef-124">On the Form setup page, define the format of various documents that are related to vendors, and that the organization uses to keep track of receipts from vendors and enter reasons for the flow of payments to vendors.</span></span>
7.  <span data-ttu-id="15cef-125">Á síðunni lánardrottinn, Stofna og viðhalda lánardrottnalyklum, og einnig skattyfirvöldum sem fyrirtækið sendir VSK-skýrslur til.</span><span class="sxs-lookup"><span data-stu-id="15cef-125">On the Vendors page, create and maintain vendor accounts, and also the tax authorities that your organization reports sales taxes to.</span></span>

## <a name="optional-setup-pages-for-accounts-payable"></a><span data-ttu-id="15cef-126">Valfrjálsar uppsetningarsíður fyrir viðskiptaskuldir</span><span class="sxs-lookup"><span data-stu-id="15cef-126">Optional setup pages for Accounts payable</span></span>
<span data-ttu-id="15cef-127">Auk grunnaðgerðum, hafa viðskiptaskuldir aðrar aðgerðir sem hægt er að setja upp.</span><span class="sxs-lookup"><span data-stu-id="15cef-127">In addition to the basic functionality, Accounts payable has other functionality that you can set up.</span></span>

<span data-ttu-id="15cef-128">Viðbótar uppsetningarsíður eru skipulagðar eftir aðgerðum.</span><span class="sxs-lookup"><span data-stu-id="15cef-128">The additional setup pages are organized by functionality.</span></span>

<span data-ttu-id="15cef-129">**Reglur**</span><span class="sxs-lookup"><span data-stu-id="15cef-129">**Policies**</span></span>
-   <span data-ttu-id="15cef-130">Síðunni stefna fyrir reikning lánardrottins er að setja upp stefna fyrir reikning lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="15cef-130">On the Vendor invoice policy page, set up vendor invoice policies.</span></span>

<span data-ttu-id="15cef-131">**Reikningsjöfnun**</span><span class="sxs-lookup"><span data-stu-id="15cef-131">**Invoice matching**</span></span>

-   <span data-ttu-id="15cef-132">Á síðunni vikmörk fyrir heildarupphæð reiknings skal setja upp vikmörk fyrir heildarupphæð reiknings.</span><span class="sxs-lookup"><span data-stu-id="15cef-132">On the Invoice totals tolerances page, set up tolerances for invoice totals.</span></span>
-   <span data-ttu-id="15cef-133">Á síðunni jöfnunarregla skal Setja upp tvíhliða og þríhliða Jöfnunarreglur.</span><span class="sxs-lookup"><span data-stu-id="15cef-133">On the Matching policy page, set up two-way and three-way matching policies.</span></span>
-   <span data-ttu-id="15cef-134">Á síðunni vikmörk verðs skal setja upp vikmörk fyrir einingarverð.</span><span class="sxs-lookup"><span data-stu-id="15cef-134">On the Price tolerances page, set up tolerances for unit prices.</span></span>
-   <span data-ttu-id="15cef-135">Á síðunni vikmarkaflokkur vöruverðs skal setja upp vikmarkaflokkur fyrir vöruverð.</span><span class="sxs-lookup"><span data-stu-id="15cef-135">On the Item price tolerance groups page, set up tolerance groups for item prices.</span></span>
-   <span data-ttu-id="15cef-136">Á síðunni vikmarkaflokkur lánardrottnaverðs skal setja upp vikmarkaflokkur fyrir lánardrottnaverð.</span><span class="sxs-lookup"><span data-stu-id="15cef-136">On the Vendor price tolerance groups page, set up  tolerance groups for vendor prices.</span></span>
-   <span data-ttu-id="15cef-137">Á síðunni vikmörk fyrir gjald skal setja upp vikmörk fyrir gjöld.</span><span class="sxs-lookup"><span data-stu-id="15cef-137">On the Charges tolerances page, set up tolerances for charges.</span></span>

<span data-ttu-id="15cef-138">**Verkflæði**</span><span class="sxs-lookup"><span data-stu-id="15cef-138">**Workflow**</span></span>

-   <span data-ttu-id="15cef-139">Á síðunni Verkflæði viðskiptaskulda skal setja upp verkflæðisskilgreiningar fyrir færslubókarsamþykktir og innkaupabeiðnir.</span><span class="sxs-lookup"><span data-stu-id="15cef-139">On the Accounts payable workflows page, set up workflow configurations for journal approvals and purchase requisitions.</span></span>

<span data-ttu-id="15cef-140">**Ástæður**</span><span class="sxs-lookup"><span data-stu-id="15cef-140">**Reasons**</span></span>

-   <span data-ttu-id="15cef-141">Á síðunni ástæður lánardrottins, Setja upp ástæðukóða</span><span class="sxs-lookup"><span data-stu-id="15cef-141">On the Vendor reasons page, set up reason codes.</span></span>

<span data-ttu-id="15cef-142">**Gjöld**</span><span class="sxs-lookup"><span data-stu-id="15cef-142">**Charges**</span></span>

-   <span data-ttu-id="15cef-143">Á síðunni gjaldakóðar, skal Setja upp kóða fyrir gjöld sem eru notaðir í innkaupapöntunum.</span><span class="sxs-lookup"><span data-stu-id="15cef-143">On the Charges code page, set up codes for the charges that are used in purchase orders.</span></span>
-   <span data-ttu-id="15cef-144">Á síðunni Gjaldaflokkur lánardrottins stofna og vinna með gjaldaflokka fyrir lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="15cef-144">On the Vendor charges group page, create and maintain charges groups for vendors.</span></span>
-   <span data-ttu-id="15cef-145">Á síðunni Kostnaðaraukaflokki skal stofna og vinna með gjaldaflokka fyrir afurðir.</span><span class="sxs-lookup"><span data-stu-id="15cef-145">On the Item charge groups page, create and maintain charges groups for items.</span></span>
-   <span data-ttu-id="15cef-146">Á sjálfvirk gjöldsíðunni skal Skilgreina gjöld sem eru sjálfvirkt úthlutað á pantanir.</span><span class="sxs-lookup"><span data-stu-id="15cef-146">On the Auto charges page, define the charges that are automatically assigned to orders.</span></span>

<span data-ttu-id="15cef-147">**Fylgivörur**</span><span class="sxs-lookup"><span data-stu-id="15cef-147">**Supplementary items**</span></span>

-   <span data-ttu-id="15cef-148">Á við fylgivöruflokkar- Lánardrottins síðu, skal stofna og viðhalda fylgivöruflokkum fyrir lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="15cef-148">On the Supplementary item groups - Vendor page, create and maintain supplementary item groups for vendors.</span></span>
-   <span data-ttu-id="15cef-149">Á við fylgivöruflokkar- birgðirsíðu, skal stofna og viðhalda fylgivöruflokkum fyrir afurðir.</span><span class="sxs-lookup"><span data-stu-id="15cef-149">On the Supplementary item groups - Inventory page, create and maintain supplementary item groups for items.</span></span>

<span data-ttu-id="15cef-150">**Arðgreiðsla**</span><span class="sxs-lookup"><span data-stu-id="15cef-150">**Distribution**</span></span>

-   <span data-ttu-id="15cef-151">Á síðunni Afhendingarskilmálar skal stofna og viðhalda skilmálum fyrir flutning vöru frá seljanda til kaupanda.</span><span class="sxs-lookup"><span data-stu-id="15cef-151">On the Terms of delivery page, create and maintain the conditions for an item's transfer from seller to buyer.</span></span>
-   <span data-ttu-id="15cef-152">Á Afhendingarmátum síðu, stofna og vinna með aðferðir við flutning sem er notaður þegar pöntun er afhent frá seljanda til kaupanda.</span><span class="sxs-lookup"><span data-stu-id="15cef-152">On the Modes of delivery page, create and maintain the methods of transport that are used when an order is delivered from the seller to the buyer.</span></span>
-   <span data-ttu-id="15cef-153">Á áfangastaðakóðasíðu Stofna og viðhalda kennimerki og lýsingum fyrir afhendingaráfangastaði</span><span class="sxs-lookup"><span data-stu-id="15cef-153">On the Destination codes page, create and maintain identifiers and descriptions for delivery destinations.</span></span>

<span data-ttu-id="15cef-154">**Skjámyndir**</span><span class="sxs-lookup"><span data-stu-id="15cef-154">**Forms**</span></span>

-   <span data-ttu-id="15cef-155">Á síðunni Athugasemdir eyðublaða skal stofna staðlaðan texta sem birtist á ýmsum síðum.</span><span class="sxs-lookup"><span data-stu-id="15cef-155">On the Form notes page, create the standard text that appears on various pages.</span></span>
-   <span data-ttu-id="15cef-156">Á síðunni Röðunarfæribreytur skjámyndar skal setja upp röðunarskipan fyrir beiðnir, innhreyfingarlista, fylgiseðla og reikninga.</span><span class="sxs-lookup"><span data-stu-id="15cef-156">On the Form sorting parameters page, set up the sorting order for requisitions, receipt lists, packing slips, and invoices.</span></span>
-   <span data-ttu-id="15cef-157">Á uppsetningu prentstýringar síðu, setja upp upplýsingar um prentstýringu fyrir frumrit og afrit af síðum.</span><span class="sxs-lookup"><span data-stu-id="15cef-157">On the Print management setup page, set up print management information for originals and copies of pages.</span></span>

<span data-ttu-id="15cef-158">**Greiðslur**</span><span class="sxs-lookup"><span data-stu-id="15cef-158">**Payments**</span></span>

-   <span data-ttu-id="15cef-159">Á Staðgreiðsluafsláttur síða, setja upp og Stýra skilmála til að fá staðgreiðsluafsláttur.</span><span class="sxs-lookup"><span data-stu-id="15cef-159">On the Cash discounts page, set up and manage the terms for obtaining cash discounts.</span></span> <span data-ttu-id="15cef-160">Staðgreiðsluafsláttarkóðar eru tengdir lánardrottnum og notaðir í innkaupapöntunum.</span><span class="sxs-lookup"><span data-stu-id="15cef-160">The cash discount codes are linked to vendors and are applied to purchase orders.</span></span>
-   <span data-ttu-id="15cef-161">Á Greiðsluáætlun síða, setja upp greiðsluáætlun sem eru notaðar til að stjórna afborgunargreiðslum til lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="15cef-161">On the Payment schedules page, set up the payment schedules that are used to manage installment payments to vendors.</span></span>
-   <span data-ttu-id="15cef-162">Á síðunni Greiðsludagar skaltu skilgreina greiðsludaga sem eru notaðir til þess að reikna gjalddaga og tilgreina greiðsludaga fyrir tiltekinn dag vikunnar eða mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="15cef-162">On the Payment days page, define the payment days that are used to calculate due dates, and specify payment days for a specific day of the week or month.</span></span>
-   <span data-ttu-id="15cef-163">Á Greiðsluþóknun síða, stofna og viðhalda greiðsluþóknun sem tengist lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="15cef-163">On the Payment fee page, create and maintain the payment fees that are associated with vendors.</span></span>
-   <span data-ttu-id="15cef-164">Á greiðslufyrirmælin síðu, stofna og viðhalda greiðslufyrirmælum.</span><span class="sxs-lookup"><span data-stu-id="15cef-164">On the Payment instruction page, create and maintain payment instructions.</span></span>

<span data-ttu-id="15cef-165">**Upplýsingar**</span><span class="sxs-lookup"><span data-stu-id="15cef-165">**Statistics**</span></span>

-   <span data-ttu-id="15cef-166">Á skilgreining aldurstímabilssíðuSetja upp notendaskilgreind bil til þess að greina gjalddagadreifingu fyrir lánardrottinslykla.</span><span class="sxs-lookup"><span data-stu-id="15cef-166">On the Aging period definitions page, set up user-defined intervals that are used to analyze the maturity distribution of vendor accounts.</span></span>
-   <span data-ttu-id="15cef-167">Á Atvinnugrein síðu, stofnið línu atvinnugreinakóða (LOB) sem eru úthlutað á lánardrottnum.</span><span class="sxs-lookup"><span data-stu-id="15cef-167">On the Line of business page, create the line of business (LOB) codes that are assigned to vendors.</span></span>

<span data-ttu-id="15cef-168">**skattur 1099**</span><span class="sxs-lookup"><span data-stu-id="15cef-168">**Tax 1099**</span></span>

-   <span data-ttu-id="15cef-169">Á síðunni **1099-svæðin** staðfesta og uppfæra lágmarksupphæðir sem verður að skrá í skattstofa (IRS), samkvæmt nýjustu kröfum skattayfirvalda Bandaríkjanna.</span><span class="sxs-lookup"><span data-stu-id="15cef-169">On the **1099 fields** page, verify and update the minimum amounts that must be reported to the Internal Revenue Service (IRS), based on the latest IRS requirements.</span></span>

## <a name="optional-setup-for-other-modules"></a><span data-ttu-id="15cef-170">**Valfrjáls uppsetning fyrir aðrar kerfiseiningar**</span><span class="sxs-lookup"><span data-stu-id="15cef-170">**Optional setup for other modules**</span></span>
<span data-ttu-id="15cef-171">**Fyrirtækisstjórnun**</span><span class="sxs-lookup"><span data-stu-id="15cef-171">**Organization administration**</span></span>

-   <span data-ttu-id="15cef-172">Á númeraraðir síðu, setja upp númeraraðaflokka fyrir reikningsnúmera.</span><span class="sxs-lookup"><span data-stu-id="15cef-172">On the Number sequences page, set up number sequence groups for invoice numbers.</span></span>
-   <span data-ttu-id="15cef-173">Á eftirfarandi síðum skal setja upp upplýsingar um aðsetur:</span><span class="sxs-lookup"><span data-stu-id="15cef-173">On the following pages, set up address information:</span></span>
    -   <span data-ttu-id="15cef-174">Uppsetning aðseturs</span><span class="sxs-lookup"><span data-stu-id="15cef-174">Address setup</span></span>
    -   <span data-ttu-id="15cef-175">NAF-kóðar</span><span class="sxs-lookup"><span data-stu-id="15cef-175">NAF codes</span></span>
    -   <span data-ttu-id="15cef-176">Flytja inn póstnúmer</span><span class="sxs-lookup"><span data-stu-id="15cef-176">Import ZIP/postal codes</span></span>

<span data-ttu-id="15cef-177">**Fjárhagur**</span><span class="sxs-lookup"><span data-stu-id="15cef-177">**General ledger**</span></span>

-   <span data-ttu-id="15cef-178">Á fjárhagsvíddirsíðu, skal setja upp fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="15cef-178">On the Financial dimensions page, set up financial dimensions.</span></span>
-   <span data-ttu-id="15cef-179">Á eftirfarandi síðum skal setja upp skattaupplýsingar:</span><span class="sxs-lookup"><span data-stu-id="15cef-179">On the following pages, set up tax information:</span></span>
    -   <span data-ttu-id="15cef-180">VSK-kóðar</span><span class="sxs-lookup"><span data-stu-id="15cef-180">Sales tax codes</span></span>
    -   <span data-ttu-id="15cef-181">VSK-flokkar</span><span class="sxs-lookup"><span data-stu-id="15cef-181">Sales tax groups</span></span>
    -   <span data-ttu-id="15cef-182">VSK-flokkar vöru</span><span class="sxs-lookup"><span data-stu-id="15cef-182">Item sales tax groups</span></span>
    -   <span data-ttu-id="15cef-183">Lykilflokkur</span><span class="sxs-lookup"><span data-stu-id="15cef-183">Account group</span></span>
    -   <span data-ttu-id="15cef-184">Undanþágukóðar VSK</span><span class="sxs-lookup"><span data-stu-id="15cef-184">Sales tax exempt codes</span></span>
    -   <span data-ttu-id="15cef-185">Skattaumdæmi</span><span class="sxs-lookup"><span data-stu-id="15cef-185">Sales tax jurisdictions</span></span>
    -   <span data-ttu-id="15cef-186">Skattayfirvöld</span><span class="sxs-lookup"><span data-stu-id="15cef-186">Sales tax authorities</span></span>
    -   <span data-ttu-id="15cef-187">Virðisaukaskatttímabil</span><span class="sxs-lookup"><span data-stu-id="15cef-187">Sales tax settlement periods</span></span>

<span data-ttu-id="15cef-188">**Reiðufjár- og bankastjórnun**</span><span class="sxs-lookup"><span data-stu-id="15cef-188">**Cash and bank management**</span></span>

-   <span data-ttu-id="15cef-189">Á greiðslumálefnakóða síðu, setja upp málefniskóða seðlabanka</span><span class="sxs-lookup"><span data-stu-id="15cef-189">On the Payment purpose codes page, set up the Central Bank purpose code.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]