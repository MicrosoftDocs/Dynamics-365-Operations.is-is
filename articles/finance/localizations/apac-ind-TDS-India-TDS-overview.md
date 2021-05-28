---
title: Yfirlit yfir frádreginn skatt á upprunastað (TDS) fyrir Indland
description: Þetta efnisatriði veitir ítarlegar upplýsingar um frádreginn skatt á upprunastað (TDS) fyrir Indland. TDS-fylgiskjölin ná yfir virknina í þessum möguleika.
author: kailiang
ms.date: 03/19/2021
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
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 28ee843036e11bd37b97a065ce53d2eb860c79d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023341"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a><span data-ttu-id="d9326-104">Yfirlit yfir frádreginn skatt á upprunastað (TDS) fyrir Indland</span><span class="sxs-lookup"><span data-stu-id="d9326-104">Indian Tax Deducted at Source (TDS) overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9326-105">Þetta efnisatriði veitir ítarlegar upplýsingar um frádreginn skatt á upprunastað (TDS) fyrir Indland.</span><span class="sxs-lookup"><span data-stu-id="d9326-105">This topic provides detailed information about Indian Tax Deducted at Source (TDS).</span></span>

<span data-ttu-id="d9326-106">TDS-fylgiskjölin ná yfir virknina í þessum möguleika.</span><span class="sxs-lookup"><span data-stu-id="d9326-106">The TDS documentation covers the functionality of this capability.</span></span> <span data-ttu-id="d9326-107">Það útskýrir einnig hvernig á að gera grunnuppsetningu fyrir TDS, reikna út TDS í færslum, ljúka uppgjörsferli TDS, skrá vottorðanúmer TDS og mynda TDS-fyrirspurnir, TDS-uppgjör og TDS-vottorð.</span><span class="sxs-lookup"><span data-stu-id="d9326-107">It also explains how to do the basic setup for TDS, calculate TDS on transactions, complete the TDS settlement process, record TDS certificate numbers, and generate TDS inquiries, TDS statements, and TDS certificates.</span></span> <span data-ttu-id="d9326-108">Fylgiskjölin innihalda eftirfarandi efnisatriði:</span><span class="sxs-lookup"><span data-stu-id="d9326-108">The documentation includes the following topics:</span></span>

- [<span data-ttu-id="d9326-109">Grunnuppsetning TDS</span><span class="sxs-lookup"><span data-stu-id="d9326-109">Basic setup for TDS</span></span>](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [<span data-ttu-id="d9326-110">Virkni formúluhönnuðar og vikmarka fyrir TDS-útreikning</span><span class="sxs-lookup"><span data-stu-id="d9326-110">Formula designer and threshold limit functionality used for TDS calculation</span></span>](apac-ind-TDS-Formula-designer.md)
- [<span data-ttu-id="d9326-111">Útreikningur TDS á reikningum, greiðslum, eigin víxlum og færslum milli fyrirtækja</span><span class="sxs-lookup"><span data-stu-id="d9326-111">Calculation of TDS on invoices, payments, promissory notes, and intercompany transactions</span></span>](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [<span data-ttu-id="d9326-112">Reglubundið TDS-uppgjörsferli og uppgjör TDS-upphæða til TDS-lánardrottnayfirvalda</span><span class="sxs-lookup"><span data-stu-id="d9326-112">Periodic TDS settlement process and settlement of TDS amounts to TDS authority vendors</span></span>](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [<span data-ttu-id="d9326-113">Skráning og uppfærsla á númerum og dagsetningum TDS-vottorða</span><span class="sxs-lookup"><span data-stu-id="d9326-113">Recording and updating TDS certificate numbers and dates</span></span>](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a><span data-ttu-id="d9326-114">Kynning á TDS</span><span class="sxs-lookup"><span data-stu-id="d9326-114">Introduction to TDS</span></span>

<span data-ttu-id="d9326-115">Samkvæmt lögum um tekjuskatt, 1961, er tekjuskattur dreginn frá uppruna af viðtakanda þjónustunnar þegar fyrirframgreiðsla er innt af hendi eða við bókhaldsvinnu kreditfærslu, hvort sem kemur á undan.</span><span class="sxs-lookup"><span data-stu-id="d9326-115">Per the Income tax Act, 1961, income tax is deducted at the source by the receiver of the service at the time of advance payment or accounting of credit, whichever occurs first.</span></span> <span data-ttu-id="d9326-116">Sá sem greiðir þarf að draga skattupphæðina frá og greiða þjónustuaðilanum aðeins nettóstöðu vegna þjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="d9326-116">The person who makes the payment must deduct the tax amount and pay only the net balance to the provider of the service.</span></span> <span data-ttu-id="d9326-117">TDS er notað í þjónustum sem yfirvöld tilgreina og skatturinn er dreginn frá með því að nota taxtana sem yfirvöld gefa upp fyrir tímabil.</span><span class="sxs-lookup"><span data-stu-id="d9326-117">TDS is applied on services that the government specifies, and the tax is deducted by using the rates that the government specifies for a period.</span></span> <span data-ttu-id="d9326-118">Frádráttarhlutfallið byggir á stöðu þess sem tekur við greiðslunni eða veitir þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="d9326-118">The rate of deduction is based on the status of the entity that receives the payment or provides the service.</span></span> <span data-ttu-id="d9326-119">Stöður eru **Einstaklingur**, **Óskipt hindúafjölskylda** (**HUF**), **Fyrirtæki**, **Firma**, **Samtök einstaklinga** (**AOP**), **Hópur einstaklinga** (**BOI**) og **Staðaryfirvöld**.</span><span class="sxs-lookup"><span data-stu-id="d9326-119">Statuses include **Individual**, **Hindu Undivided Family** (**HUF**), **Company**, **Firm**, **Association of Persons** (**AOP**), **Body of Individuals** (**BOI**), and **Local authority**.</span></span>

<span data-ttu-id="d9326-120">Eftirfarandi hlutar telja upp þá þjónustu sem TDS er notað fyrir eins og tilgreint af yfirvöldum á Indlandi.</span><span class="sxs-lookup"><span data-stu-id="d9326-120">The following sections list the services that TDS is applied on, as specified by the Government of India.</span></span>

<span data-ttu-id="d9326-121">**Íbúar**</span><span class="sxs-lookup"><span data-stu-id="d9326-121">**Residents**</span></span>

- <span data-ttu-id="d9326-122">Tekjur af launum (skv. lið 192)</span><span class="sxs-lookup"><span data-stu-id="d9326-122">Income from salaries (Under section 192)</span></span>
- <span data-ttu-id="d9326-123">Tekjur af vöxtum verðbréfa (skv. lið 193)</span><span class="sxs-lookup"><span data-stu-id="d9326-123">Income from interest on securities (Under section 193)</span></span>
- <span data-ttu-id="d9326-124">Tekjur af arði (skv. lið 194)</span><span class="sxs-lookup"><span data-stu-id="d9326-124">Income from dividend (Under section 194)</span></span>
- <span data-ttu-id="d9326-125">Tekjur af vöxtum (skv. lið 194A)</span><span class="sxs-lookup"><span data-stu-id="d9326-125">Income from interest (Under section 194A)</span></span>
- <span data-ttu-id="d9326-126">Tekjur af happdrætti (skv. lið 194B)</span><span class="sxs-lookup"><span data-stu-id="d9326-126">Income from lotteries or puzzles (Under section 194B)</span></span>
- <span data-ttu-id="d9326-127">Að vinna úr kappreiðum o.fl. (undir kafla 194BB)</span><span class="sxs-lookup"><span data-stu-id="d9326-127">Winning from horse races etc. (Under section 194BB)</span></span>
- <span data-ttu-id="d9326-128">Verktakar og undirverktakar (skv. lið 194C)</span><span class="sxs-lookup"><span data-stu-id="d9326-128">Contractors and sub-contractors (Under section 194C)</span></span>
- <span data-ttu-id="d9326-129">Tryggingarþóknun (skv. lið 194D)</span><span class="sxs-lookup"><span data-stu-id="d9326-129">Insurance commission (Under section 194D)</span></span>
- <span data-ttu-id="d9326-130">Tekjur af innborgun vegna séreignasparnaðar (skv. lið 194EE)</span><span class="sxs-lookup"><span data-stu-id="d9326-130">Income from deposit under national saving scheme (Under section 194EE)</span></span>
- <span data-ttu-id="d9326-131">Tekjur af verðbréfasjóði eða UTI (skv. lið 194F)</span><span class="sxs-lookup"><span data-stu-id="d9326-131">Income from mutual fund or UTI (Under section 194F)</span></span>
- <span data-ttu-id="d9326-132">Þóknun, umbun, verðlaun o.s.frv. af sölu eða happdrætti (skv. lið 194G)</span><span class="sxs-lookup"><span data-stu-id="d9326-132">Commission, Remuneration, Prize etc., on sale or lottery (Under section 194G)</span></span>
- <span data-ttu-id="d9326-133">Greiðsla þóknunar eða miðlunar (skv. lið 194H)</span><span class="sxs-lookup"><span data-stu-id="d9326-133">Payment of Commission or brokerage (Under section 194H)</span></span>
- <span data-ttu-id="d9326-134">Leiga (skv. lið 194I)</span><span class="sxs-lookup"><span data-stu-id="d9326-134">Rent (Under section 194I)</span></span>
- <span data-ttu-id="d9326-135">Fagleg þjónusta (skv. lið 194J)</span><span class="sxs-lookup"><span data-stu-id="d9326-135">Professional service (Under section 194J)</span></span>
- <span data-ttu-id="d9326-136">Tekjur af einingum (skv. lið 194K)</span><span class="sxs-lookup"><span data-stu-id="d9326-136">Income from Units (Under section 194K)</span></span>
- <span data-ttu-id="d9326-137">Greiðsla þóknunar við kaup á tiltekinni fasteign (skv. lið 194LA)</span><span class="sxs-lookup"><span data-stu-id="d9326-137">Payment of compensation on acquisition of certain immovable property (Under section 194LA)</span></span>

<span data-ttu-id="d9326-138">**Ekki ríkisborgari**</span><span class="sxs-lookup"><span data-stu-id="d9326-138">**Non-residents**</span></span>

- <span data-ttu-id="d9326-139">Greiðslur til erlends íþróttafólks eða erlends íþróttasambands (skv. lið 194E)</span><span class="sxs-lookup"><span data-stu-id="d9326-139">Payments to Non-resident sportsmen or sports association (Under section 194E)</span></span>
- <span data-ttu-id="d9326-140">Aðrar fjárhæðir (skv. lið 195)</span><span class="sxs-lookup"><span data-stu-id="d9326-140">Other sums (Under section 195)</span></span>
- <span data-ttu-id="d9326-141">Tekjur vegna eininga erlendra aðila (skv. lið 196A)</span><span class="sxs-lookup"><span data-stu-id="d9326-141">Income in respect of units of non-residents (Under section 196A)</span></span>

    - <span data-ttu-id="d9326-142">Tekjur af skuldabréfum eða hlutabréfum í erlendum gjaldmiðli í indversku fyrirtæki (skv. lið 196C)</span><span class="sxs-lookup"><span data-stu-id="d9326-142">Income from foreign currency bonds or shares of Indian Company (Under section 196C)</span></span>
    - <span data-ttu-id="d9326-143">Tekjur erlendra fagfjárfesta af verðbréfum (skv. lið 196D)</span><span class="sxs-lookup"><span data-stu-id="d9326-143">Incomes of foreign institutional investors from securities (Under section 196D)</span></span>
    - <span data-ttu-id="d9326-144">Laun og allar aðrar jákvæðar tekjur undir hvaða tekjuhóp sem er (liður 192)</span><span class="sxs-lookup"><span data-stu-id="d9326-144">Salary and all other positive incomes under any head on income (Section 192)</span></span>
    - <span data-ttu-id="d9326-145">Vextir af verðbréfum (liður 193)</span><span class="sxs-lookup"><span data-stu-id="d9326-145">Interest on securities (Section 193)</span></span>
    - <span data-ttu-id="d9326-146">Vextir aðrir en vextir af verðbréfum (liður 194A)</span><span class="sxs-lookup"><span data-stu-id="d9326-146">Interest other than interest on securities (Section 194A)</span></span>
    - <span data-ttu-id="d9326-147">Greiðslur til verktaka og undirverktaka (liður 194C)</span><span class="sxs-lookup"><span data-stu-id="d9326-147">Payments to contractors and sub-contractors (Section 194C)</span></span>
    - <span data-ttu-id="d9326-148">Vinningar úr happdrætti eða krossgátum (liður 194B)</span><span class="sxs-lookup"><span data-stu-id="d9326-148">Winnings from Lottery or crossword puzzles (Section 194B)</span></span>
    - <span data-ttu-id="d9326-149">Vinningar úr kappreiðum (kafli 194BB)</span><span class="sxs-lookup"><span data-stu-id="d9326-149">Winnings from horse races (Section 194BB)</span></span>
    - <span data-ttu-id="d9326-150">Tryggingaþóknun sem nær yfir allar greiðslur fyrir öflun tryggingastarfsemi (liður 194D)</span><span class="sxs-lookup"><span data-stu-id="d9326-150">Insurance Commission covering all payments for procuring Insurance business (Section 194D)</span></span>
    - <span data-ttu-id="d9326-151">Allir aðrir vextir en vextir af verðbréfum sem greiðast til erlendra aðila sem ekki eru fyrirtæki eða til erlends fyrirtækis (liður 195)</span><span class="sxs-lookup"><span data-stu-id="d9326-151">Any interest other than interest on securities payable to non-residents not being a company or to a foreign company (Section 195)</span></span>
    - <span data-ttu-id="d9326-152">Greiðsla til erlends íþróttamanns, þ.m.t. íþróttasambands eða stofnunar.</span><span class="sxs-lookup"><span data-stu-id="d9326-152">Payment to non-resident sportsman including athlete or sports association or institution.</span></span> <span data-ttu-id="d9326-153">Ef um erlendan íþróttamann er að ræða, greiðslur í sambandi við auglýsingar ásamt greinum um leiki/íþróttir á Indlandi í fréttablöðum, tímaritum o.þ.h.</span><span class="sxs-lookup"><span data-stu-id="d9326-153">In case of non-resident sportsman, payments in respect of advertisements as well as articles on any game/sports in India in newspapers, magazines, and so.</span></span> <span data-ttu-id="d9326-154">er innifalið (liður 194E)</span><span class="sxs-lookup"><span data-stu-id="d9326-154">is included (Section 194E)</span></span>
    - <span data-ttu-id="d9326-155">Greiðsla vegna innstæðna samkvæmt NSS \[National Saving Scheme\] (liður 194EE)</span><span class="sxs-lookup"><span data-stu-id="d9326-155">Payment in respect of deposits under NSS \[National Savings Scheme\] (Section 194EE)</span></span>
    - <span data-ttu-id="d9326-156">Greiðsla vegna endurkaupa á einingum með verðbréfasjóði eða UTI (liður 194F)</span><span class="sxs-lookup"><span data-stu-id="d9326-156">Payment on account of repurchase of Units by Mutual Fund or UTI (Section 194F)</span></span>
    - <span data-ttu-id="d9326-157">Greiðsla fyrir þóknun eða miðlun (liður 194H)</span><span class="sxs-lookup"><span data-stu-id="d9326-157">Payment for Commission or brokerage (Section 194H)</span></span>
    - <span data-ttu-id="d9326-158">Greiðsla leigu (liður 194I)</span><span class="sxs-lookup"><span data-stu-id="d9326-158">Payment of rent (Section 194I)</span></span>
    - <span data-ttu-id="d9326-159">Greiðsla þóknana vegna faglegrar eða tæknilegrar þjónustu (liður 194J)</span><span class="sxs-lookup"><span data-stu-id="d9326-159">Payment of fees for professional or technical services (Section 194J)</span></span>
    - <span data-ttu-id="d9326-160">Þóknun til kaupmanna, dreifingaraðila, kaupenda og seljenda happdrættismiða, þ.m.t. endurgjald eða verðlaun fyrir slíka miða (liður 194G)</span><span class="sxs-lookup"><span data-stu-id="d9326-160">Commission to Stockiest, distributors, buyers and sellers of Lottery tickets including remuneration or prize on such tickets (Section 194G)</span></span>
    - <span data-ttu-id="d9326-161">Tekjur af einingum sem keyptar eru í erlendum gjaldmiðli eða langtíma verðmætisaukning sem stafar af flutningi slíkra eininga sem keyptar eru í erlendum gjaldmiðli (liður 196B)</span><span class="sxs-lookup"><span data-stu-id="d9326-161">Income from Units purchased in foreign currency or long-term capital gain arising from the transfer of such Units purchased in foreign currency (Section 196B)</span></span>
    - <span data-ttu-id="d9326-162">Greiðsla allra tekna til erlendra aðila vegna vaxta eða arðs af skuldabréfum og hlutabréfum (liður 196C)</span><span class="sxs-lookup"><span data-stu-id="d9326-162">Payment of any income to non-residents in respect of interest or dividend on bonds and shares (Section 196C)</span></span>

<span data-ttu-id="d9326-163">TDS er reiknað vegna kaupa, sölu, söluskila, kreditnóta, eignakaupa, fyrirframgreiðslna, eigin víxla, vinnuskatts og færslna milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="d9326-163">TDS is calculated on purchases, sales, sales returns, credit notes, fixed asset acquisitions, prepayments, advance payments, promissory notes, works tax, and intercompany transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="d9326-164">Í núverandi skattaumhverfi Indlands er TDS ekki reiknað fyrir sölufærslur.</span><span class="sxs-lookup"><span data-stu-id="d9326-164">In the current Indian tax scenario, TDS isn't calculated on sales transactions.</span></span> <span data-ttu-id="d9326-165">Kerfið inniheldur hins vegar ákvæði um að reikna út TDS sem er endurheimtanlegt í sölufærslum, þá sérstaklega fyrir færslur milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="d9326-165">However, the system includes a provision to calculate TDS recoverable on sales transactions, especially for intercompany transactions.</span></span>

<span data-ttu-id="d9326-166">Útreikningur á TDS tekur alltaf mið af mörkum og undantekningarmörkum sem eru skilgreind fyrir TDS-hlutann.</span><span class="sxs-lookup"><span data-stu-id="d9326-166">The calculation of TDS always considers the threshold and the exception threshold that are defined for the TDS component.</span></span>

<span data-ttu-id="d9326-167">Reglubundið uppgjörsferli TDS þarf að keyra og TDS-greiðslur þarf að gera upp hjá TDS-lánardrottnayfirvöldum.</span><span class="sxs-lookup"><span data-stu-id="d9326-167">The periodic TDS settlement process must be run, and the TDS payments must be settled to TDS authority vendors.</span></span>

<span data-ttu-id="d9326-168">Hægt er að skrá og uppfæra númer og dagsetningar vottorða fyrir TDS-vottorð sem eru móttekin frá lánardrottnum eða viðskiptavinum.</span><span class="sxs-lookup"><span data-stu-id="d9326-168">The certificate numbers and dates for TDS certificates that are received from vendors or customers can be recorded and updated.</span></span> <span data-ttu-id="d9326-169">Auk þess er hægt að mynda eyðublað 26Q og 27Q vegna ársfjórðungslegs uppgjörs og eyðublað 16A vegna vottorðs fyrir TDS í Finance.</span><span class="sxs-lookup"><span data-stu-id="d9326-169">Additionally, Form 26Q and Form 27Q quarterly statements, and the Form 16A certificate for TDS, can be generated in Finance.</span></span>

## <a name="setting-up-and-working-with-tds"></a><span data-ttu-id="d9326-170">Setja upp og vinna með TDS</span><span class="sxs-lookup"><span data-stu-id="d9326-170">Setting up and working with TDS</span></span>

<span data-ttu-id="d9326-171">Hér er yfirlit yfir ferlið við að setja upp og að vinna með TDS:</span><span class="sxs-lookup"><span data-stu-id="d9326-171">Here is an overview of the process for setting up and working with TDS:</span></span>

1. <span data-ttu-id="d9326-172">**TDS uppsetning:**</span><span class="sxs-lookup"><span data-stu-id="d9326-172">**TDS setup:**</span></span>

    - <span data-ttu-id="d9326-173">Uppsetning á færibreytum</span><span class="sxs-lookup"><span data-stu-id="d9326-173">Parameter setup:</span></span>

        - <span data-ttu-id="d9326-174">Í færibreytum fjárhags skal virkja færibreytur sem tengjast TDS.</span><span class="sxs-lookup"><span data-stu-id="d9326-174">In General ledger parameters, activate parameters that are related to TDS.</span></span>
        - <span data-ttu-id="d9326-175">Í færibreytum fjárhags skal setja upp númeraraðir fyrir greiðslur staðgreiðsluskatts.</span><span class="sxs-lookup"><span data-stu-id="d9326-175">In General ledger parameters, set up the number sequence for withholding tax payments.</span></span>
        - <span data-ttu-id="d9326-176">Setjið upp færibreytur í viðskiptaskuldum og viðskiptakröfum.</span><span class="sxs-lookup"><span data-stu-id="d9326-176">Set up parameters in Accounts payable and Accounts receivable.</span></span>

    - <span data-ttu-id="d9326-177">Grunnuppsetning:</span><span class="sxs-lookup"><span data-stu-id="d9326-177">Basic setup:</span></span>

        - <span data-ttu-id="d9326-178">Setjið upp TDS-skráningarnúmer fyrir fyrirtæki, viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="d9326-178">Set up TDS registration numbers for a company, customers, and vendors.</span></span>
        - <span data-ttu-id="d9326-179">Setjið upp flokka TDS-hluta.</span><span class="sxs-lookup"><span data-stu-id="d9326-179">Set up TDS component groups.</span></span>
        - <span data-ttu-id="d9326-180">Setjið upp TDS-hluta, hengið flokka TDS-hluta við þá og skilgreinið mörkin og undantekningarmörkin fyrir þá.</span><span class="sxs-lookup"><span data-stu-id="d9326-180">Set up TDS components, attach TDS component groups to them, and define the threshold and exception threshold for them.</span></span>
        - <span data-ttu-id="d9326-181">Setjið upp TDS-yfirvöld.</span><span class="sxs-lookup"><span data-stu-id="d9326-181">Set up TDS authorities.</span></span>
        - <span data-ttu-id="d9326-182">Setjið upp TDS-uppgjörstímabil.</span><span class="sxs-lookup"><span data-stu-id="d9326-182">Set up TDS settlement periods.</span></span>
        - <span data-ttu-id="d9326-183">Setjið upp skattkóða TDS og hengið TDS-hluta við þá.</span><span class="sxs-lookup"><span data-stu-id="d9326-183">Set up TDS tax codes, and attach TDS components to them.</span></span>
        - <span data-ttu-id="d9326-184">Setjið upp skattflokka TDS og hengið skattkóða TDS við þá.</span><span class="sxs-lookup"><span data-stu-id="d9326-184">Set up TDS tax groups, and attach TDS tax codes to them.</span></span>
        - <span data-ttu-id="d9326-185">Í formúluhönnuðinum skal skilgreina formúlu til að reikna út TDS fyrir TDS-flokk.</span><span class="sxs-lookup"><span data-stu-id="d9326-185">In the formula designer, define a formula to calculate TDS for a TDS group.</span></span>
        - <span data-ttu-id="d9326-186">Skráið vottorðanúmer TDS-skattaívilnunar.</span><span class="sxs-lookup"><span data-stu-id="d9326-186">Record TDS concession certificate numbers.</span></span>

    - <span data-ttu-id="d9326-187">Uppsetning fjárhagslykla og fyrirtækis:</span><span class="sxs-lookup"><span data-stu-id="d9326-187">Ledger accounts and company setup:</span></span>

        - <span data-ttu-id="d9326-188">Setjið upp fjárhagslykla viðskiptaskulda og viðskiptakrafa TDS.</span><span class="sxs-lookup"><span data-stu-id="d9326-188">Set up TDS payable and receivable ledger accounts.</span></span>
        - <span data-ttu-id="d9326-189">Setjið upp lykilnúmer skattafrádrátts og skattinnheimtu (TAN) og flokk frádráttargerðar fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="d9326-189">Set up a Tax Deduction and Collection Account Number (TAN) and a deductor type category for the company.</span></span>

    - <span data-ttu-id="d9326-190">Önnur uppsetning:</span><span class="sxs-lookup"><span data-stu-id="d9326-190">Other setup:</span></span>

        - <span data-ttu-id="d9326-191">Setjið upp greiðsluáætlun sem inniheldur TDS-úthlutun.</span><span class="sxs-lookup"><span data-stu-id="d9326-191">Set up a payment schedule that includes TDS allocation.</span></span>
        - <span data-ttu-id="d9326-192">Setjið upp gerð greiðsluþóknunar fyrir greiðslur til TDS-yfirvalda.</span><span class="sxs-lookup"><span data-stu-id="d9326-192">Set up a payment fee type for payments to the TDS authority.</span></span>
        - <span data-ttu-id="d9326-193">Setjið upp upplýsingar um TDS-flokka, varanleg lykilnúmer (PAN) og TAN fyrir lánardrottna og viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="d9326-193">Set up information about TDS groups, permanent account numbers (PANs), and TANs for vendors and customers.</span></span>

2. <span data-ttu-id="d9326-194">**Útreikningur TDS í færslum:**</span><span class="sxs-lookup"><span data-stu-id="d9326-194">**Calculation of TDS in transactions:**</span></span>

    - <span data-ttu-id="d9326-195">Reikningar og greiðslur</span><span class="sxs-lookup"><span data-stu-id="d9326-195">Invoices and payments</span></span>
    - <span data-ttu-id="d9326-196">Eigin víxlar</span><span class="sxs-lookup"><span data-stu-id="d9326-196">Promissory notes</span></span>
    - <span data-ttu-id="d9326-197">Fyrirframgreiðslur</span><span class="sxs-lookup"><span data-stu-id="d9326-197">Advance payments</span></span>
    - <span data-ttu-id="d9326-198">Fyrirframgreiðslur</span><span class="sxs-lookup"><span data-stu-id="d9326-198">Prepayments</span></span>

3. <span data-ttu-id="d9326-199">**TDS-uppgjör:**</span><span class="sxs-lookup"><span data-stu-id="d9326-199">**TDS settlement:**</span></span>

    - <span data-ttu-id="d9326-200">Reglubundið uppgjörsferli TDS</span><span class="sxs-lookup"><span data-stu-id="d9326-200">Periodic TDS settlement process</span></span>
    - <span data-ttu-id="d9326-201">Uppgjör á TDS-greiðslum til lánardrottnayfirvalda TDS og myndun TDS-greiðslukvittunar</span><span class="sxs-lookup"><span data-stu-id="d9326-201">Settlement of TDS payments to TDS authority vendors and generation of TDS challan</span></span>

4. <span data-ttu-id="d9326-202">**Fyrirspurnir, uppgjör og vottorð vegna TDS:**</span><span class="sxs-lookup"><span data-stu-id="d9326-202">**TDS inquiries, statements, and certificate:**</span></span>

    - <span data-ttu-id="d9326-203">Skráið og uppfærið númer og dagsetningar TDS-vottorða.</span><span class="sxs-lookup"><span data-stu-id="d9326-203">Record and update TDS certificate numbers and dates.</span></span>
    - <span data-ttu-id="d9326-204">Búið til TDS-fyrirspurn og bókið TDS-fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="d9326-204">Generate a TDS inquiry and a posted TDS inquiry.</span></span>
    - <span data-ttu-id="d9326-205">Búið til TDS-eyðublað 27A, 26Q og 27Q og rafræn ársfjórðungsleg uppgjör TDS.</span><span class="sxs-lookup"><span data-stu-id="d9326-205">Generate Form 27A, Form 26Q, and Form 27Q TDS and e-TDS quarterly statements.</span></span>
    - <span data-ttu-id="d9326-206">Búið til eyðublað 16A vegna TDS-vottorðs.</span><span class="sxs-lookup"><span data-stu-id="d9326-206">Generate a Form 16A TDS certificate.</span></span>
