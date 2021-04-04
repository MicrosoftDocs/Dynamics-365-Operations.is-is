---
title: Skjöl og fylgiskjöl númeruð eftir tímaröð
description: Þetta efnisatriði útskýrir hvernig á að setja upp og nota númer í tímaröð fyrir viðeigandi skjöl og tengd fylgiskjöl.
author: ikond
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 4a27b6fdd1e244fb0cb8c5fcefc484494aeb88bd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254523"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="bc22c-103">Skjöl og fylgiskjöl númeruð eftir tímaröð</span><span class="sxs-lookup"><span data-stu-id="bc22c-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="bc22c-104">Í sumum löndum er lagaleg krafa um að númera skjöl og tengd fylgiskjöl í tímaröð.</span><span class="sxs-lookup"><span data-stu-id="bc22c-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="bc22c-105">Tímaröðin verður að vera studd af tímabilum.</span><span class="sxs-lookup"><span data-stu-id="bc22c-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="bc22c-106">Öll númer sem tilheyra fyrri tímabilum verða að vera minna en númerin sem tilheyra seinni tímabilum.</span><span class="sxs-lookup"><span data-stu-id="bc22c-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="bc22c-107">Til að uppfylla þessa kröfu hefur númeravirkni í tímaröð verið innleidd.</span><span class="sxs-lookup"><span data-stu-id="bc22c-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="bc22c-108">Þetta efnisatriði útskýrir hvernig á að skilgreina og nota númer í tímaröð fyrir viðeigandi skjöl og tengd fylgiskjöl.</span><span class="sxs-lookup"><span data-stu-id="bc22c-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bc22c-109">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="bc22c-109">Prerequisites</span></span>

<span data-ttu-id="bc22c-110">Á vinnusvæði eiginleikastjórnunar skal kveikja á eiginleikanum **Tölusetning í tímaröð**.</span><span class="sxs-lookup"><span data-stu-id="bc22c-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="bc22c-111">Frekari upplýsingar er að finna í [Eiginleikastjórnunaryfirlit](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bc22c-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="bc22c-112">Skilgreina tölusetningu í tímaröð</span><span class="sxs-lookup"><span data-stu-id="bc22c-112">Configure chronological numbering</span></span>

<span data-ttu-id="bc22c-113">Tölusetning í tímaröð hefur áhrif á eftirfarandi skjöl.</span><span class="sxs-lookup"><span data-stu-id="bc22c-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="bc22c-114">**Viðskiptakröfur**</span><span class="sxs-lookup"><span data-stu-id="bc22c-114">**Accounts receivable**</span></span>
- <span data-ttu-id="bc22c-115">Reikningur viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="bc22c-115">Customer invoice</span></span>
- <span data-ttu-id="bc22c-116">Fylgiskjal með reikningi viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="bc22c-116">Customer invoice voucher</span></span>
- <span data-ttu-id="bc22c-117">Sölukreditnóta</span><span class="sxs-lookup"><span data-stu-id="bc22c-117">Sales credit note</span></span>
- <span data-ttu-id="bc22c-118">Fylgiskjal sölukreditnótu</span><span class="sxs-lookup"><span data-stu-id="bc22c-118">Sales credit note voucher</span></span>
- <span data-ttu-id="bc22c-119">Textareikningur</span><span class="sxs-lookup"><span data-stu-id="bc22c-119">Free text invoice</span></span>
- <span data-ttu-id="bc22c-120">Fylgiskjal textareiknings</span><span class="sxs-lookup"><span data-stu-id="bc22c-120">Free text invoice voucher</span></span>
- <span data-ttu-id="bc22c-121">Textakreditnóta</span><span class="sxs-lookup"><span data-stu-id="bc22c-121">Free text credit note</span></span>
- <span data-ttu-id="bc22c-122">Fylgiskjal textakreditnótu</span><span class="sxs-lookup"><span data-stu-id="bc22c-122">Free text credit note voucher</span></span>
- <span data-ttu-id="bc22c-123">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="bc22c-123">Packing slip</span></span>
- <span data-ttu-id="bc22c-124">Fylgiskjal fylgiseðils</span><span class="sxs-lookup"><span data-stu-id="bc22c-124">Packing slip voucher</span></span>
- <span data-ttu-id="bc22c-125">Leiðréttingarskjal fyrir fylgiseðil</span><span class="sxs-lookup"><span data-stu-id="bc22c-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="bc22c-126">Fylgiskjal vaxtanótu</span><span class="sxs-lookup"><span data-stu-id="bc22c-126">Interest note voucher</span></span>
- <span data-ttu-id="bc22c-127">Fylgiskjal innheimtubréfs</span><span class="sxs-lookup"><span data-stu-id="bc22c-127">Collection letter voucher</span></span>

<span data-ttu-id="bc22c-128">**Viðskiptaskuldir**</span><span class="sxs-lookup"><span data-stu-id="bc22c-128">**Accounts payable**</span></span>
- <span data-ttu-id="bc22c-129">Fylgiskjal reiknings</span><span class="sxs-lookup"><span data-stu-id="bc22c-129">Invoice voucher</span></span>
- <span data-ttu-id="bc22c-130">Fylgiskjal á kreditnótum</span><span class="sxs-lookup"><span data-stu-id="bc22c-130">Credit note voucher</span></span>
- <span data-ttu-id="bc22c-131">Innhreyfingarskjal afurða</span><span class="sxs-lookup"><span data-stu-id="bc22c-131">Product receipt voucher</span></span>

<span data-ttu-id="bc22c-132">**Verkefnastjórnun**</span><span class="sxs-lookup"><span data-stu-id="bc22c-132">**Project management**</span></span>
- <span data-ttu-id="bc22c-133">Reikningur</span><span class="sxs-lookup"><span data-stu-id="bc22c-133">Invoice</span></span>
- <span data-ttu-id="bc22c-134">Fylgiskjal reiknings</span><span class="sxs-lookup"><span data-stu-id="bc22c-134">Invoice voucher</span></span>
- <span data-ttu-id="bc22c-135">Kreditnóta</span><span class="sxs-lookup"><span data-stu-id="bc22c-135">Credit note</span></span>
- <span data-ttu-id="bc22c-136">Fylgiskjal á kreditnótum</span><span class="sxs-lookup"><span data-stu-id="bc22c-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="bc22c-137">Skilgreina númeraraðir</span><span class="sxs-lookup"><span data-stu-id="bc22c-137">Define number sequences</span></span>

<span data-ttu-id="bc22c-138">Til að skilgreina númeraraðir skal fara í **Fyrirtækisstjórnun** > **Númeraraðir** > **Númeraraðir**.</span><span class="sxs-lookup"><span data-stu-id="bc22c-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="bc22c-139">Hægt er að skilgreina eins margar númeraraðir og þörf er á til að ná yfir tilheyrandi tímabil fyrir nauðsynleg skjöl.</span><span class="sxs-lookup"><span data-stu-id="bc22c-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="bc22c-140">Tilgreinið fyrirtæki fyrir hverja númeraröð.</span><span class="sxs-lookup"><span data-stu-id="bc22c-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="bc22c-141">Hlutar númeraraðanna verða að vera skilgreindir þannig að þeir bjóði upp á rétta tímaröð fyrir tímabil.</span><span class="sxs-lookup"><span data-stu-id="bc22c-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="bc22c-142">Til dæmis geta heiti hlutanna innihaldið sérstakt forskeyti sem vísar í tiltekið tímabil.</span><span class="sxs-lookup"><span data-stu-id="bc22c-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![Uppsetning númeraraðar](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="bc22c-144">Skilgreina númeraraðaflokka</span><span class="sxs-lookup"><span data-stu-id="bc22c-144">Configure number sequence groups</span></span>

<span data-ttu-id="bc22c-145">Til að skilgreina númeraraðaflokka skal fara í **Viðskiptakröfur** > **Uppsetning** > **Færibreytur viðskiptakröfu**.</span><span class="sxs-lookup"><span data-stu-id="bc22c-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="bc22c-146">Í flipanum **Númeraraðir** skal skilgreina eins marga númeraraðaflokka og þörf er á til að ná yfir tilheyrandi tímabil.</span><span class="sxs-lookup"><span data-stu-id="bc22c-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="bc22c-147">Fyrir hvern flokk, í hlutanum **Tilvísun**, skal velja eina af studdu skjalatilvísununum og í reitnum **Númeraraðarkóði** skal vísa í númeraröð sem var áður búin til fyrir tilheyrandi tímabil.</span><span class="sxs-lookup"><span data-stu-id="bc22c-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![Uppsetning númeraraðaflokks](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="bc22c-149">Á svipaðan hátt skal skilgreina númeraraðaflokka í einingunum **Viðskiptaskuldir** og **Verkefnastjórnun og bókhald**.</span><span class="sxs-lookup"><span data-stu-id="bc22c-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="bc22c-150">Skilgreina tímaröð númeraraðaflokka</span><span class="sxs-lookup"><span data-stu-id="bc22c-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="bc22c-151">Til að skilgreina tímaröð númeraraðaflokka skal fara í **Fyrirtækisstjórnun** > **Númeraraðir** > **Númeraraðaflokkar í tímaröð**.</span><span class="sxs-lookup"><span data-stu-id="bc22c-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="bc22c-152">Skilgreinið skilyrði númeraraðaflokks þegar hann tekur gildi.</span><span class="sxs-lookup"><span data-stu-id="bc22c-152">Define the applicability conditions for number sequence groups.</span></span>

![Uppsetning númera í tímaröð](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="bc22c-154">Svæði</span><span class="sxs-lookup"><span data-stu-id="bc22c-154">Field</span></span>            | <span data-ttu-id="bc22c-155">lýsing</span><span class="sxs-lookup"><span data-stu-id="bc22c-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc22c-156">Virkt</span><span class="sxs-lookup"><span data-stu-id="bc22c-156">Effective</span></span>  | <span data-ttu-id="bc22c-157">Upphafsdagsetning þegar númeraraðaflokkur tekur gildi.</span><span class="sxs-lookup"><span data-stu-id="bc22c-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="bc22c-158">Lok gildistíma</span><span class="sxs-lookup"><span data-stu-id="bc22c-158">Expiration</span></span>      | <span data-ttu-id="bc22c-159">Lokadagsetning þegar númeraraðaflokkur gildir ekki lengur.</span><span class="sxs-lookup"><span data-stu-id="bc22c-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="bc22c-160">Ef engin lokadagsetning á við skal velja **Aldrei**.</span><span class="sxs-lookup"><span data-stu-id="bc22c-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="bc22c-161">Númeraraðaflokkur</span><span class="sxs-lookup"><span data-stu-id="bc22c-161">Number sequence group</span></span> | <span data-ttu-id="bc22c-162">Númeraraðaflokkur sem verður notaður til að mynda skjalanúmer á tímabilinu.</span><span class="sxs-lookup"><span data-stu-id="bc22c-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="bc22c-163">Upprunalegur númeraraðarflokkur</span><span class="sxs-lookup"><span data-stu-id="bc22c-163">Original number sequence group</span></span> | <span data-ttu-id="bc22c-164">Þessi kóði númeraraðaflokks er notaður fyrir frekari afmarkanir fyrir tilfelli þar sem skjöl eru þegar með tiltekinn *varanlegan* númeraraðaflokk úthlutaðan.</span><span class="sxs-lookup"><span data-stu-id="bc22c-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="bc22c-165">Autt gildi er talið sérstakt gildi.</span><span class="sxs-lookup"><span data-stu-id="bc22c-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="bc22c-166">Ef hunsa þarf fyrirfram úthlutaðan flokk skal nota valkostinn **Sjálfgefinn** fyrir þessa uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="bc22c-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="bc22c-167">Sjálfgefinn</span><span class="sxs-lookup"><span data-stu-id="bc22c-167">Default</span></span> | <span data-ttu-id="bc22c-168">Ef kveikt er á þessu hunsar kerfið fyrirfram úthlutaðan númeraraðaflokk skjals og notar aðeins upphafs- og lokadagsetningar til að greina hvað á við.</span><span class="sxs-lookup"><span data-stu-id="bc22c-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="bc22c-169">Ef slökkt er á þessu notar kerfið fullu samsetninguna **Virkt** + **Gildistími** + **Upprunalegur númeraraðaflokkur** fyrir val.</span><span class="sxs-lookup"><span data-stu-id="bc22c-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="bc22c-170">Bókun skjals</span><span class="sxs-lookup"><span data-stu-id="bc22c-170">Document posting</span></span>
<span data-ttu-id="bc22c-171">Þegar skjal er bókað er viðeigandi númeraraðaflokki úthlutað á skjalið byggt á bókunardagsetningu skjals og síðan notaður til að mynda skjalanúmer byggt á greindri númeraröð.</span><span class="sxs-lookup"><span data-stu-id="bc22c-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="bc22c-172">Kerfið býður upp á skilaboð varðandi úthlutun númeraraðarflokks.</span><span class="sxs-lookup"><span data-stu-id="bc22c-172">The system provides a message regarding the number sequence group assignment.</span></span>

![Skjalnúmer](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="bc22c-174">Í sumum löndum er þegar búið að innleiða ákveðna reglu fyrir númerasetningu skjala.</span><span class="sxs-lookup"><span data-stu-id="bc22c-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="bc22c-175">Í slíku tilfelli mun regla tiltekins lands hnekkja eiginleikanum **Tölusetning í tímaröð**.</span><span class="sxs-lookup"><span data-stu-id="bc22c-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]