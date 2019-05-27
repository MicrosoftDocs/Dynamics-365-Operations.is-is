---
title: Verksamningar
description: Þetta efnisatriði gefur dæmi um verksamninga sem hægt er að búa til fyrir ýmsar gerðir verka og uppruna fjármögnunar og hvernig hægt er að vinna með samninga og senda viðskiptavinum reikninga vegna verka í Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0f0fcec64ce03c6e1d877fb1c8d004bb416bd95
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561434"
---
# <a name="project-contracts"></a><span data-ttu-id="f669a-103">Verksamningar</span><span class="sxs-lookup"><span data-stu-id="f669a-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f669a-104">Þessi grein gefur dæmi um verksamninga sem hægt er að búa til fyrir ýmsar gerðir verka og uppruna fjármögnunar og hvernig hægt er að vinna með samninga og senda viðskiptavinum reikninga vegna verka í Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f669a-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="f669a-105">Gerð verks sem er stofnuð fyrir verksamningur ákvarðar aðferðina sem er notuð til að reikningsfæra viðskiptavini verksins.</span><span class="sxs-lookup"><span data-stu-id="f669a-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="f669a-106">Hægt er að breyta verksamningi og tengdum verkum, en ekki er hægt að breyta gerð verks.</span><span class="sxs-lookup"><span data-stu-id="f669a-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="f669a-107">Með því að nota verksamning er hægt að reikningsfæra eitt eða fleiri verk samtímis.</span><span class="sxs-lookup"><span data-stu-id="f669a-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="f669a-108">Verksamningurinn stuðlar einnig að því að tryggja að samræmt reikningsfærsluferli sé notað fyrir hvert undirverk verkskipulags.</span><span class="sxs-lookup"><span data-stu-id="f669a-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="f669a-109">Hvert verk sem verður reikningsfært verður að tengja við verksamning.</span><span class="sxs-lookup"><span data-stu-id="f669a-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="f669a-110">Stillingar fyrir verksamning eiga við öll verk og undirverk sem tengjast verksamningnum.</span><span class="sxs-lookup"><span data-stu-id="f669a-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="f669a-111">Verksamningur getur tilgreint fleiri en einn uppruna fjármögnunar.</span><span class="sxs-lookup"><span data-stu-id="f669a-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="f669a-112">Þannig er hægt að skipta reikningagerð á marga fjármögnunaraðila, setja upp fjármögnunartakmörk þannig að uppruni fjármögnunar eru ekki rukkaðir um meira en tilgreinda upphæð, og stilla fjármögnunarreglur til að gjaldfæra útgjöld.</span><span class="sxs-lookup"><span data-stu-id="f669a-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="f669a-113">Fjármögnun fyrir verksamninga</span><span class="sxs-lookup"><span data-stu-id="f669a-113">Funding for project contracts</span></span>
<span data-ttu-id="f669a-114">Sumar verksamninga tilgreina að margir aðila deila ábyrgð fyrir fjármögnunar verkkostnaðar.</span><span class="sxs-lookup"><span data-stu-id="f669a-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="f669a-115">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="f669a-115">Here are some examples:</span></span>

-   <span data-ttu-id="f669a-116">Stór viðskiptavinar sem er með margar deildir biður um að fjármögnun verks sé skipt eftir deild.</span><span class="sxs-lookup"><span data-stu-id="f669a-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="f669a-117">Fyrirtækið þitt deilir kostnaði fyrir stórt verk með ytri fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="f669a-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="f669a-118">Vegavinnuverk er samfjármagnað af tveimur sveitarfélaga.</span><span class="sxs-lookup"><span data-stu-id="f669a-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="f669a-119">Á Brúarvinnuverk er fjármagnað af opinber styrkur og einkafyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="f669a-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="f669a-120">Í Finance and Operations er hægt að skipta reikningum fyrir einstaka færslu eða allt verkið á milli margra viðskiptavina, styrkja eða fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="f669a-120">In Finance and Operations, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="f669a-121">Í verkum sem hafa mörg fjármögnunaraðila, verða allir aðilar sem eiga þátt í fjármögnunar ítarlega fjármögnunarverks kallast fjármögnunaraðilar.</span><span class="sxs-lookup"><span data-stu-id="f669a-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="f669a-122">Eftir að viðskiptavini, fyrirtæki eða styrks er skilgreind sem fjármögnunaraðilar, má úthluta þeim á ein eða fleiri fjármögnunarreglur.</span><span class="sxs-lookup"><span data-stu-id="f669a-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="f669a-123">Fjármögnunarreglur innihalda þau skilyrði sem ákvarða hvernig gjöldum er úthlutað á ýmsar fjármögnunaraðila fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="f669a-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="f669a-124">Þar sem vörur í birgðum, eins og þær sem birtast á innkaupabeiðnir og innkaupapantanir, er ekki hægt að skipta, ekki er hægt að skipta, er ekki hægt að skipta kostnaðarupphæð milli marga fjármögnunaraðila á tíma dreifingarinnar.</span><span class="sxs-lookup"><span data-stu-id="f669a-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="f669a-125">Þess vegna helst upprunagildi fjármögnunar 0 (núll) þar til úthreyfing birgða er bókuð.</span><span class="sxs-lookup"><span data-stu-id="f669a-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="f669a-126">Þegar bókað er úthreyfing birgða, kostnaðarupphæð er dreift samkvæmt reglum um dreifingu á reikninga fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="f669a-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="f669a-127">Hér eru nokkur skref sem má grípa til svo auðveldara sé að skipta reikningum á milli marga fjármögnunaraðila:</span><span class="sxs-lookup"><span data-stu-id="f669a-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="f669a-128">Tilgreinið að allar færslur sem eru færðar inn fyrir verk nota sama sölugjaldmiðill og verksamning.</span><span class="sxs-lookup"><span data-stu-id="f669a-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="f669a-129">Setja upp fjármögnunarmörk, þannig að á fjármögnunaraðila er ekki reikningsfærður fyrir meira en tilgreind upphæð hvað varðar verk.</span><span class="sxs-lookup"><span data-stu-id="f669a-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="f669a-130">Skilgreina fjármögnunarreglur og hámarki fjármögnunar fyrir hvern starfsmann, vöru, tegund, tegundaflokk og færslugerð (eða fyrir allar færslugerðir).</span><span class="sxs-lookup"><span data-stu-id="f669a-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="f669a-131">Veljið valfrjálsar upphafs- og lokadagsetningar til að skilgreina tímabil þegar hver fjármögnunarregla er gild.</span><span class="sxs-lookup"><span data-stu-id="f669a-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="f669a-132">Tilgreinið þá prósentu sem hver fjármögnunaraðila er ábyrgur fyrir.</span><span class="sxs-lookup"><span data-stu-id="f669a-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="f669a-133">Tilgreina hvaða fjármögnunaraðila er ábyrgur fyrir sléttunarmismunur sem eru orsökuð af útreikninga á úthlutun fjármögnunar.</span><span class="sxs-lookup"><span data-stu-id="f669a-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="f669a-134">Setja upp reglur sem ákvarða hvernig verkkostnað eru reikningsfærð til utanaðkomandi viðskiptavina og gjaldfærð fyrir samstæðufyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="f669a-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="f669a-135">Skrá á færslur fyrir fjármögnunarlykil í biðstöðu þar til viðbótarfjármagn fæst eða þar til notandi ákveður að bera kostnaðinn innan fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="f669a-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="f669a-136">Til að ákvarða hvaða skattflokk til að tengja við færslu, er leitað í verkinu fyrir úthlutun í skattflokk.</span><span class="sxs-lookup"><span data-stu-id="f669a-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="f669a-137">Ef enginn úthlutunin skattflokks er gerð á verkstiginu, er leitað í verksamning.</span><span class="sxs-lookup"><span data-stu-id="f669a-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="f669a-138">Dæmi: marga uppruni fjármögnunar (einfalt)</span><span class="sxs-lookup"><span data-stu-id="f669a-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="f669a-139">Eftirfarandi tafla gefur dæmi fyrir stjórnun úthlutunar á fjármögnun milli marga uppruna fjármögnunar.</span><span class="sxs-lookup"><span data-stu-id="f669a-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="f669a-140">Þessar aðstæður eru byggð á eftirtöldum ályktunum:</span><span class="sxs-lookup"><span data-stu-id="f669a-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="f669a-141">Forgangsstillingar eru látnar vera þáttur í úthlutun fjármagns áður en önnur skilyrði fjármögnunarreglu er beitt.</span><span class="sxs-lookup"><span data-stu-id="f669a-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="f669a-142">Engin dagsetningabil hefur verið tilgreindur til að skilgreina tímabil þegar fjármögnunarreglan er í gildi.</span><span class="sxs-lookup"><span data-stu-id="f669a-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f669a-143"><strong>Aðstæður</strong></span><span class="sxs-lookup"><span data-stu-id="f669a-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="f669a-144"><strong>Uppruni fjármögnunar </strong></span><span class="sxs-lookup"><span data-stu-id="f669a-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="f669a-145"><strong>Úthlutunarhlutfall </strong></span><span class="sxs-lookup"><span data-stu-id="f669a-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="f669a-146"><strong>Úthlutanaforgangur</strong></span><span class="sxs-lookup"><span data-stu-id="f669a-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f669a-147">Þú vilt úthluta kostnaði til einn uppruni fjármögnunar þar til fjármagn eru uppurið, úthluta kostnaði til annars uppruni fjármögnunar þar til fjármagn þess er uppurið, og úthluta að lokum eftirstandandi kostnaður á þriðja uppruni fjármögnunar.</span><span class="sxs-lookup"><span data-stu-id="f669a-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="f669a-148">Uppruni fjármögnunar　1</span><span class="sxs-lookup"><span data-stu-id="f669a-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="f669a-149">Uppruni fjármögnunar　2</span><span class="sxs-lookup"><span data-stu-id="f669a-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="f669a-150">Uppruni fjármögnunar　3</span><span class="sxs-lookup"><span data-stu-id="f669a-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f669a-151">100%</span><span class="sxs-lookup"><span data-stu-id="f669a-151">100%</span></span></li>
<li><span data-ttu-id="f669a-152">100%</span><span class="sxs-lookup"><span data-stu-id="f669a-152">100%</span></span></li>
<li><span data-ttu-id="f669a-153">100%</span><span class="sxs-lookup"><span data-stu-id="f669a-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f669a-154">1</span><span class="sxs-lookup"><span data-stu-id="f669a-154">1</span></span></li>
<li><span data-ttu-id="f669a-155">2</span><span class="sxs-lookup"><span data-stu-id="f669a-155">2</span></span></li>
<li><span data-ttu-id="f669a-156">3</span><span class="sxs-lookup"><span data-stu-id="f669a-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f669a-157">Þú vilt úthluta 75 prósent af kostnaði í einn uppruna fjármögnunar og 25 prósent í annan uppruna fjármögnunar.</span><span class="sxs-lookup"><span data-stu-id="f669a-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="f669a-158">Þegar annað hvor uppruni fjármögnunar er uppurinn viltu greiða eftirstandandi kostnað frá þriðja uppruna fjármögnunar.</span><span class="sxs-lookup"><span data-stu-id="f669a-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="f669a-159">Uppruni fjármögnunar　1</span><span class="sxs-lookup"><span data-stu-id="f669a-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="f669a-160">Uppruni fjármögnunar　2</span><span class="sxs-lookup"><span data-stu-id="f669a-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="f669a-161">Uppruni fjármögnunar　3</span><span class="sxs-lookup"><span data-stu-id="f669a-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f669a-162">75%</span><span class="sxs-lookup"><span data-stu-id="f669a-162">75%</span></span></li>
<li><span data-ttu-id="f669a-163">25%</span><span class="sxs-lookup"><span data-stu-id="f669a-163">25%</span></span></li>
<li><span data-ttu-id="f669a-164">100%</span><span class="sxs-lookup"><span data-stu-id="f669a-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f669a-165">1</span><span class="sxs-lookup"><span data-stu-id="f669a-165">1</span></span></li>
<li><span data-ttu-id="f669a-166">1</span><span class="sxs-lookup"><span data-stu-id="f669a-166">1</span></span></li>
<li><span data-ttu-id="f669a-167">2</span><span class="sxs-lookup"><span data-stu-id="f669a-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f669a-168">Þú vilt úthluta 75 prósent af kostnaði í einn uppruna fjármögnunar og 25 prósent í annan uppruna fjármögnunar.</span><span class="sxs-lookup"><span data-stu-id="f669a-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="f669a-169">Þegar annað hvor uppruni fjármögnunar er uppurinn viltu skipta eftirstandandi kostnaður á milli þriðja uppruni fjármögnunar og fjórða uppruni fjármögnunar.</span><span class="sxs-lookup"><span data-stu-id="f669a-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="f669a-170">Uppruni fjármögnunar　1</span><span class="sxs-lookup"><span data-stu-id="f669a-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="f669a-171">Uppruni fjármögnunar　2</span><span class="sxs-lookup"><span data-stu-id="f669a-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="f669a-172">Uppruni fjármögnunar　3</span><span class="sxs-lookup"><span data-stu-id="f669a-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="f669a-173">Uppruni fjármögnunar　4</span><span class="sxs-lookup"><span data-stu-id="f669a-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f669a-174">75%</span><span class="sxs-lookup"><span data-stu-id="f669a-174">75%</span></span></li>
<li><span data-ttu-id="f669a-175">25%</span><span class="sxs-lookup"><span data-stu-id="f669a-175">25%</span></span></li>
<li><span data-ttu-id="f669a-176">50%</span><span class="sxs-lookup"><span data-stu-id="f669a-176">50%</span></span></li>
<li><span data-ttu-id="f669a-177">50%</span><span class="sxs-lookup"><span data-stu-id="f669a-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f669a-178">1</span><span class="sxs-lookup"><span data-stu-id="f669a-178">1</span></span></li>
<li><span data-ttu-id="f669a-179">1</span><span class="sxs-lookup"><span data-stu-id="f669a-179">1</span></span></li>
<li><span data-ttu-id="f669a-180">2</span><span class="sxs-lookup"><span data-stu-id="f669a-180">2</span></span></li>
<li><span data-ttu-id="f669a-181">2</span><span class="sxs-lookup"><span data-stu-id="f669a-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f669a-182">Þú vilt úthluta fyrstu 25 prósent af kostnaði í einn uppruni fjármögnunar og afganginum á seinni uppruni fjármögnunar.</span><span class="sxs-lookup"><span data-stu-id="f669a-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="f669a-183">Uppruni fjármögnunar　1</span><span class="sxs-lookup"><span data-stu-id="f669a-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="f669a-184">Uppruni fjármögnunar　2</span><span class="sxs-lookup"><span data-stu-id="f669a-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f669a-185">25%</span><span class="sxs-lookup"><span data-stu-id="f669a-185">25%</span></span></li>
<li><span data-ttu-id="f669a-186">100%</span><span class="sxs-lookup"><span data-stu-id="f669a-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f669a-187">1</span><span class="sxs-lookup"><span data-stu-id="f669a-187">1</span></span></li>
<li><span data-ttu-id="f669a-188">2</span><span class="sxs-lookup"><span data-stu-id="f669a-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="f669a-189">Dæmi: marga uppruni fjármögnunar (flókið)</span><span class="sxs-lookup"><span data-stu-id="f669a-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="f669a-190">Þú ert með þrjá uppruna fjármögnunar sem þú vilt nota í eftirfarandi röð:</span><span class="sxs-lookup"><span data-stu-id="f669a-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="f669a-191">Notið uppruni fjármögnunar 2 og uppruni fjármögnunar 3 jafnt þar til uppruni fjármögnunar 2 er uppurinn.</span><span class="sxs-lookup"><span data-stu-id="f669a-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="f669a-192">Halda áfram að nota uppruni fjármögnunar 3 þar til hún er uppurinn.</span><span class="sxs-lookup"><span data-stu-id="f669a-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="f669a-193">Notið uppruni fjármögnunar 1 þar til uppruni fjármögnunar 3 er uppurinn.</span><span class="sxs-lookup"><span data-stu-id="f669a-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="f669a-194">Til að ná þessu markmiði þarf að gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="f669a-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="f669a-195">Setja upp hámark fjármögnunar fyrir uppruni fjármögnunar 2 og 3, fyrir viðeigandi upphæðir.</span><span class="sxs-lookup"><span data-stu-id="f669a-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="f669a-196">Stofna eftirfarandi fjármögnunarreglur:</span><span class="sxs-lookup"><span data-stu-id="f669a-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="f669a-197">Regla 1 (Forgangur 1): Úthluta 50 prósent færsla í uppruni fjármögnunar 2 og 50 prósent í uppruni fjármögnunar 3.</span><span class="sxs-lookup"><span data-stu-id="f669a-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="f669a-198">Regla 2 (Forgangur 2): Úthluta 100 prósent færsla í uppruni fjármögnunar 3.</span><span class="sxs-lookup"><span data-stu-id="f669a-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="f669a-199">Regla 3 (Forgangur 3): Úthluta 100 prósent færsla í uppruni fjármögnunar 1.</span><span class="sxs-lookup"><span data-stu-id="f669a-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="f669a-200">Þessi uppsetning virkar þar sem færslur eru athugaðar gagnvart reglur og mörk til að ákvarða hvort einhver þeirra eigi við færsluna.</span><span class="sxs-lookup"><span data-stu-id="f669a-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="f669a-201">Ef engar sérstakar reglur eða takmarkanir eiga við um færsluna, gilda allar færslureglur.</span><span class="sxs-lookup"><span data-stu-id="f669a-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="f669a-202">Allar færslureglur samsvara allar færslur.</span><span class="sxs-lookup"><span data-stu-id="f669a-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="f669a-203">Ef regla finnst sem samsvarar færslu, er prósentu sem hefur verið úthlutað í þeirri reglu beitt fyrst, en aðeins eftir samsvaranir eru athugaðar gagnar öllum mörkum sem hafa verið settar upp.</span><span class="sxs-lookup"><span data-stu-id="f669a-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="f669a-204">Ef mörk hafi verið náð og fjármagn uppruni fjármögnunar eru uppurin, er fjármögnunarreglan sem er tengdur við hámark fjármögnunar hunsuð og forritið athugar næsta regluna sem á við.</span><span class="sxs-lookup"><span data-stu-id="f669a-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="f669a-205">Í sumum tilvikum, aðeins hluti af færslu er hægt að úthluta samkvæmt reglu.</span><span class="sxs-lookup"><span data-stu-id="f669a-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="f669a-206">Þetta gæti gerst þar sem mörk er náð þegar færsluna er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="f669a-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="f669a-207">Í þessu tilfelli eru aðeins tiltekna upphæð úthlutað samkvæmt þeirri reglu, eins og 50 prósent á hvern uppruni fjármögnunar.</span><span class="sxs-lookup"><span data-stu-id="f669a-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="f669a-208">Þetta er tilfellið í reglu 1, sem er lýst fyrr í þessum hluta.</span><span class="sxs-lookup"><span data-stu-id="f669a-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="f669a-209">Afgangurinn er úthlutað samkvæmt næstu reglu í röðinni.</span><span class="sxs-lookup"><span data-stu-id="f669a-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="f669a-210">Eftirfarandi tafla athugar þessar aðstæður í meiri smáatriðum.</span><span class="sxs-lookup"><span data-stu-id="f669a-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f669a-211"><strong>Áhersla</strong></span><span class="sxs-lookup"><span data-stu-id="f669a-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="f669a-212"><strong>Upplýsingar</strong></span><span class="sxs-lookup"><span data-stu-id="f669a-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f669a-213">Fjármögnunarreglur</span><span class="sxs-lookup"><span data-stu-id="f669a-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="f669a-214">Regla 1 (Forgangur 1): Allar færslur.</span><span class="sxs-lookup"><span data-stu-id="f669a-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="f669a-215">Úthluta uppruni fjármögnunar 2 við 50% og uppruni fjármögnunar 3 við 50%.</span><span class="sxs-lookup"><span data-stu-id="f669a-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="f669a-216">Regla 2 (Forgangur 2): Allar færslur.</span><span class="sxs-lookup"><span data-stu-id="f669a-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="f669a-217">Úthluta uppruna fjármögnunar 3 á 100%.</span><span class="sxs-lookup"><span data-stu-id="f669a-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="f669a-218">Regla 3 (Forgangur 2): Allar færslur.</span><span class="sxs-lookup"><span data-stu-id="f669a-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="f669a-219">Úthluta uppruna fjármögnunar 1 á 100%.</span><span class="sxs-lookup"><span data-stu-id="f669a-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f669a-220">Fjármögnunarmörk</span><span class="sxs-lookup"><span data-stu-id="f669a-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="f669a-221">Uppruni fjármögnunar 1 takmörk = 10.000,00</span><span class="sxs-lookup"><span data-stu-id="f669a-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="f669a-222">Uppruni fjármögnunar 2 takmörk = 500,00</span><span class="sxs-lookup"><span data-stu-id="f669a-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="f669a-223">Uppruni fjármögnunar 3 takmörk = 750,00</span><span class="sxs-lookup"><span data-stu-id="f669a-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f669a-224">Færsla 1</span><span class="sxs-lookup"><span data-stu-id="f669a-224">Transaction 1</span></span></td>
<td><span data-ttu-id="f669a-225"><strong>Færsluupphæð:</strong> 100,00<strong>fjármögnun:</strong> Færslan er greitt samkvæmt reglu 1 eingöngu, þar sem færslan er fullgreidd eftir að reglu 1 er beitt.</span><span class="sxs-lookup"><span data-stu-id="f669a-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="f669a-226">Færslan er fjármagnað jafnt milli uppruni fjármögnunar 2 og uppruni fjármögnunar 3 .</span><span class="sxs-lookup"><span data-stu-id="f669a-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="f669a-227">Uppruni fjármögnunar 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="f669a-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="f669a-228">Uppruni fjármögnunar 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="f669a-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f669a-229">Færsla 2</span><span class="sxs-lookup"><span data-stu-id="f669a-229">Transaction 2</span></span></td>
<td><span data-ttu-id="f669a-230"><strong>Færsluupphæð:</strong> 5.000,00<strong>Fjármögnun:</strong> Færslan er greidd í samræmi við allar þrjár reglunar.</span><span class="sxs-lookup"><span data-stu-id="f669a-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="f669a-231"><strong>Regla 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="f669a-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="f669a-232">Uppruni fjármögnunar 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="f669a-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="f669a-233">Uppruni fjármögnunar 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="f669a-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="f669a-234">
<strong>Regla 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="f669a-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="f669a-235">Uppruni fjármögnunar 3: 250.00 (= 750.00 – 50.00 – 450.00)</span><span class="sxs-lookup"><span data-stu-id="f669a-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="f669a-236">
<strong>Regla 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="f669a-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="f669a-237">Uppruni fjármögnunar 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="f669a-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f669a-238">Samtals fjármagn sem er dreift á hvern uppruni fjármögnunar</span><span class="sxs-lookup"><span data-stu-id="f669a-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="f669a-239">Uppruni fjármögnunar 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="f669a-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="f669a-240">Uppruni fjármögnunar 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="f669a-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="f669a-241">Uppruni fjármögnunar 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="f669a-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="f669a-242">Innheimtureglur</span><span class="sxs-lookup"><span data-stu-id="f669a-242">Billing rules</span></span>
<span data-ttu-id="f669a-243">Þegar verksamningur er saminn við viðskiptavin skilgreinirðu hvernig og hvenær hægt er að reikningsfæra á viðskiptavininn fyrir vinnu við verk.</span><span class="sxs-lookup"><span data-stu-id="f669a-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="f669a-244">Eftir að þú setur upp verksamninginn og verkið, geturðu sett upp reikningsreglur fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="f669a-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="f669a-245">Reikningsreglur byggist á skilmálum verks sem er tilgreindur í verksamningnum.</span><span class="sxs-lookup"><span data-stu-id="f669a-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="f669a-246">Reikningsreglur sem hægt er að stofna velta á skilmálum í verksamningi og tegund verks, eins og Tími og efni eða Fast verð, sem tengt er við reikningsreglu.</span><span class="sxs-lookup"><span data-stu-id="f669a-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="f669a-247">Hægt er að stofna fleiri en eina reikningsreglu fyrir verksamning.</span><span class="sxs-lookup"><span data-stu-id="f669a-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="f669a-248">Einnig er hægt að úthluta reikningsreglu á mörg verk sem tengjast sama verksamning og hafa svipaðar innheimtuskilmála.</span><span class="sxs-lookup"><span data-stu-id="f669a-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="f669a-249">Þú getur sett upp eftirfarandi gerðir innheimtureglna:</span><span class="sxs-lookup"><span data-stu-id="f669a-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="f669a-250">**Afhendingareining** - Stofna reikning viðskiptavinar þegar þú hefur lokið einingu afhendingar.</span><span class="sxs-lookup"><span data-stu-id="f669a-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="f669a-251">Skilgreina einingarnar afhendingar í samningnum.</span><span class="sxs-lookup"><span data-stu-id="f669a-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="f669a-252">**Framvinda** - Sendu viðskiptavini reikning þegar þú klárar ákveðið hlutfall af verkefninu.</span><span class="sxs-lookup"><span data-stu-id="f669a-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="f669a-253">Þú getur sett upp innheimtureglu til að sjálfkrafa reikna hlutfall lokinnar vinnu, eða þú getur handvirkt reiknað hlutfall af lokinni vinnu og fjárhæð sem á að reikningsfæra viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="f669a-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="f669a-254">**Þáttaskil**– Stofna reikning fyrir alla upphæð áfanga þegar nýjum verkáfanga er náð.</span><span class="sxs-lookup"><span data-stu-id="f669a-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="f669a-255">**Gjald** - Sendu viðskiptavini reikning fyrir þjónustu þína auk umsýsluþóknun, venjulega hlutfall af kostnaði við þjónustu.</span><span class="sxs-lookup"><span data-stu-id="f669a-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="f669a-256">**Tími og efni** - Stofna reikning viðskiptavinar fyrir verðmæti tíma og efnum sem notuð eru á verkefninu.</span><span class="sxs-lookup"><span data-stu-id="f669a-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="f669a-257">Fyrir allar gerðir reikningsreglum, er hægt að tilgreina hlutfall varðveislu að draga úr reikningi viðskiptavinar þar til verki nær á samþykkt við stig.</span><span class="sxs-lookup"><span data-stu-id="f669a-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="f669a-258">Hlutfall varðveislu á greiðslu er tilgreindur í verksamningnum.</span><span class="sxs-lookup"><span data-stu-id="f669a-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="f669a-259">Upphæðin er reiknuð út á grunni, og dreginn frá, heildarvirði lína í reikningi viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="f669a-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="f669a-260">Fyrir **Tími og efni** og **Framvindu** reikningsreglur, geturðu úthlutað gjaldfæranlegum flokkum.</span><span class="sxs-lookup"><span data-stu-id="f669a-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="f669a-261">Reikningshæfar tegundir tilgreina færslur sem eiga að birtast í reikningum viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="f669a-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="f669a-262">Þegar þú ert tilbúinn til að reikningsfæra viðskiptavininn, er fjárhæð sem á að reikningsfæra fyrir verkefnið reiknuð út á grunni innheimtureglna og reikningstillaga er mynduð.</span><span class="sxs-lookup"><span data-stu-id="f669a-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="f669a-263">Eftirfarandi kaflar gefa dæmi sem sýna hvernig á að setja upp og stjórna reikningsreglu fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="f669a-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="f669a-264">Dæmi: Stofna reikningsreglur byggt á fjölda afhentra eininga</span><span class="sxs-lookup"><span data-stu-id="f669a-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="f669a-265">Fyrirtækið þitt fellst á að nota þjónustuna í samtals fimm þjálfunarsetur fyrir starfsmann viðskiptavinar á kostnaðinum 10.000 fyrir hverja þjálfunarsetu.</span><span class="sxs-lookup"><span data-stu-id="f669a-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="f669a-266">Að reikningsfæra á viðskiptavininn eftir hverja þjálfun setu.</span><span class="sxs-lookup"><span data-stu-id="f669a-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="f669a-267">Þegar þú gerir Uppsetning reikningsreglna fyrir verksamning notarðu eftirfarandi gildum:</span><span class="sxs-lookup"><span data-stu-id="f669a-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="f669a-268">Eining afhendingartíma er eina þjálfun setu.</span><span class="sxs-lookup"><span data-stu-id="f669a-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="f669a-269">Einingarverð er 10.000 á þjálfun setu.</span><span class="sxs-lookup"><span data-stu-id="f669a-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="f669a-270">Fjöldi eininga sem er fimm þjálfun lotur.</span><span class="sxs-lookup"><span data-stu-id="f669a-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="f669a-271">Þegar þú lýkur einni þjálfunarlotu, geturðu stofnað reikning fyrir 10.000 fyrir fyrsta afhentu vörurnar og sendir reikning til viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="f669a-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="f669a-272">Dæmi: Stofna reikningsreglur byggt á fjölda tiltekinnar prósentu af loknu verki (handvirkur útreikningur)</span><span class="sxs-lookup"><span data-stu-id="f669a-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="f669a-273">Samtakanna í hugbúnað consulting staðfesta, færir inn samningur við viðskiptavin til að þróa hluti afurðar sem viðskiptavinurinn er að þróa.</span><span class="sxs-lookup"><span data-stu-id="f669a-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="f669a-274">Fyrirtækið samþykkir að afhenda hugbúnaðarkóða yfir sex mánaða tímabil.</span><span class="sxs-lookup"><span data-stu-id="f669a-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="f669a-275">Viðskiptavinurinn fellst á að greiða fyrirtækið samtals 100.000 fyrir vinnustöðina.</span><span class="sxs-lookup"><span data-stu-id="f669a-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="f669a-276">Þú stofnar reikningsreglur til að reikningsfæra viðskiptavin byggt á þeirri prósentu vinnu sem er lokið á verkið eins og tilgreint er í samningnum.</span><span class="sxs-lookup"><span data-stu-id="f669a-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="f669a-277">Í lok fyrsta mánaðar, þú hittir viðskiptavininn til að ákvarða hversu stóru hlutfalli vinnu sé lokið.</span><span class="sxs-lookup"><span data-stu-id="f669a-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="f669a-278">Eftir að þú og viðskiptavinur hafið gert skoðun á verkinu ákveður þú að verkinu sé 15 prósent lokið.</span><span class="sxs-lookup"><span data-stu-id="f669a-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="f669a-279">Þú stofnar reikning fyrir 15,000 (15 prósent af 100.000) og sendir hann til viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="f669a-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="f669a-280">Dæmi: Stofna reikningsreglur byggðar á fjölda tiltekinnar prósentu af loknu verki (sjálfvirkur útreikningur)</span><span class="sxs-lookup"><span data-stu-id="f669a-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="f669a-281">Fyrirtæki þitt, sem er í hugbúnaðarþróun, samþykkir að þróa launabókhaldspakka fyrir viðskiptavinar fyrir 30.000.</span><span class="sxs-lookup"><span data-stu-id="f669a-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="f669a-282">Viðskiptavinurinn fellst á að greiða fyrirtækið byggðar á prósentu vinnu sem lokið.</span><span class="sxs-lookup"><span data-stu-id="f669a-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="f669a-283">Verkkostnaður er 20,000 er metin.</span><span class="sxs-lookup"><span data-stu-id="f669a-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="f669a-284">Verksamningurinn tilgreinir þær tegundir vinnu sem þú getur notað í reikningagerð.</span><span class="sxs-lookup"><span data-stu-id="f669a-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="f669a-285">Setja upp er reglur sem reikningsfæra sjálfkrafa reikningsupphæðir fyrir hlutfall vinnu sem er lokið fyrir hverja tegund.</span><span class="sxs-lookup"><span data-stu-id="f669a-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="f669a-286">Hægt er að setja upp fjárhagsáætlunar fyrir hverja tegund:</span><span class="sxs-lookup"><span data-stu-id="f669a-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="f669a-287">**Þróun** – Kostnaður 15.000 og tekjur af 20.000</span><span class="sxs-lookup"><span data-stu-id="f669a-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="f669a-288">**Uppsetning** - Kostnaður 5.000 og tekjur upp á 10.000</span><span class="sxs-lookup"><span data-stu-id="f669a-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="f669a-289">Þegar reikningur viðskiptavinar er stofnaður í fyrsta sinn er reikningsupphæð sjálfkrafa reiknuð út frá eftirfarandi upplýsingum:</span><span class="sxs-lookup"><span data-stu-id="f669a-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="f669a-290">Eftir mánuð, starfsmanns í verki sendir vinnukort fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="f669a-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="f669a-291">Kostnaður við tíma starfsmanns er 5.000 fyrir þróun og 1.000 fyrir uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="f669a-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="f669a-292">Þróunarvinnu er 33 prósenta (5.000 raunveruleg kostnaðar/15.000 kostnað fjárhagsáætlunar) og uppsetningarvinnu er 20 prósent lokið (1.000 raunveruleg kostnaðar/5.000 kostnað fjárhagsáætlunar).</span><span class="sxs-lookup"><span data-stu-id="f669a-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="f669a-293">Reikningsupphæð 8,667 er sjálfkrafa reiknaður (hlutfall (33 prósent 20,000 plús 20% af 10.000).</span><span class="sxs-lookup"><span data-stu-id="f669a-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="f669a-294">Þú stofnar reikning fyrir 8,667 og sendir hann til viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="f669a-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="f669a-295">Dæmi: Stofna reikningsreglur sem eru byggðar á þáttaskilum samkvæmt samkomulagi</span><span class="sxs-lookup"><span data-stu-id="f669a-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="f669a-296">Fyrirtækið, ráðgjöf fyrir birgðastjórnun, samþykkir að framkvæma markaðsrannsókn á neytendaafurð sem viðskiptamaður hyggst selja.</span><span class="sxs-lookup"><span data-stu-id="f669a-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="f669a-297">Viðskiptavinurinn fellst á að nota við þjónustu fyrir þriggja mánaða tímabil hefst í Mars og samþykkir að borga fyrirtækið 50.000.</span><span class="sxs-lookup"><span data-stu-id="f669a-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="f669a-298">Verkið eru þrír áfangar:</span><span class="sxs-lookup"><span data-stu-id="f669a-298">The project has three milestones:</span></span>

-   <span data-ttu-id="f669a-299">1. áfangi: Safna neytendagögnum – 31. mars</span><span class="sxs-lookup"><span data-stu-id="f669a-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="f669a-300">2. áfangi: Greina neytendagögn – 30. apríl</span><span class="sxs-lookup"><span data-stu-id="f669a-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="f669a-301">3. áfangi: Leggja fram tillögu um lífvænleika afurðar – 31. maí</span><span class="sxs-lookup"><span data-stu-id="f669a-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="f669a-302">Viðskiptavinurinn fellst á að greiða fyrirtæki þínu 10.000 fyrir fyrsta þáttaskil og 20,000 fyrir annað þáttaskil, og 20.000 fyrir þriðju þáttaskil.</span><span class="sxs-lookup"><span data-stu-id="f669a-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="f669a-303">Þegar settur er upp verksamningur samþykkir þú að rukka viðskiptavininn byggt loknum áfanga.</span><span class="sxs-lookup"><span data-stu-id="f669a-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="f669a-304">Reikningsregluuppsetningin inniheldur eftirfarandi skref:</span><span class="sxs-lookup"><span data-stu-id="f669a-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="f669a-305">Skilgreina áfanga verks.</span><span class="sxs-lookup"><span data-stu-id="f669a-305">Define the project milestones.</span></span>
-   <span data-ttu-id="f669a-306">Skilgreina upphæðina sem á að reikningsfæra á viðskiptavininn þegar hverju þáttaskil er lokið.</span><span class="sxs-lookup"><span data-stu-id="f669a-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="f669a-307">Þegar fyrsta þáttaskil lýkur 31. Mars, merkirðu þáttaskilunum sé lokið og stofna síðan reikning fyrir 10.000 og senda hann til viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="f669a-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="f669a-308">Ekki er hægt að stofna reikning fyrir þáttaskil þar til búið er að merkja þáttaskilunum sé lokið.</span><span class="sxs-lookup"><span data-stu-id="f669a-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="f669a-309">Dæmi: Stofna reikningsreglur sem eru byggðar á þjónustu plús stjórnunargjald</span><span class="sxs-lookup"><span data-stu-id="f669a-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="f669a-310">Fyrirtækið þitt, ráðgjafafyrirtæki í stjórnun, fellst á að framkvæma rannsóknir á markaði til að meta sýnileika afurðar sem viðskiptavinur, smásölufyrirtæki, er að þróa.</span><span class="sxs-lookup"><span data-stu-id="f669a-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="f669a-311">Samningsatriði tilgreina að þú munir veita þjónustu þriggja háttsettra stjórnunarráðgjafa til þess að framkvæma rannsóknina á tíma- og efni.</span><span class="sxs-lookup"><span data-stu-id="f669a-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="f669a-312">Viðskiptamaðurinn fellst á að borga 100 á klukkustund auk 10 prósent viðbótar stjórnunarþóknun fyrir tíma ráðgjafans sem eru skuldfærðir á verkið.</span><span class="sxs-lookup"><span data-stu-id="f669a-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="f669a-313">Þegar settur er upp verksamningur, skal stofna reikningsreglur til að bæta 10 prósenta stjórnunargjaldi við ráðgjafartíma sem er gjaldfærð á verk.</span><span class="sxs-lookup"><span data-stu-id="f669a-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="f669a-314">Þegar þú stofnar reikning fyrir viðskiptavin, er viðskiptavinurinn krafinn um 10 prósent stjórnunarþóknun auk tímakostnaðar við ráðgjöf.</span><span class="sxs-lookup"><span data-stu-id="f669a-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="f669a-315">Til dæmis, ef þrír utanaðkomandi ráðgjöfum unnu samtals 200 klukkustundir í verki, reikningur er búinn til uppá 22.000, á eftirfarandi útreikningum.</span><span class="sxs-lookup"><span data-stu-id="f669a-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="f669a-316">200 klukkustundir með 100 á klukkustund = 20.000</span><span class="sxs-lookup"><span data-stu-id="f669a-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="f669a-317">10 prósent stjórnunarþóknun = 2000</span><span class="sxs-lookup"><span data-stu-id="f669a-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="f669a-318">Heildarupphæð reiknings = 22.000</span><span class="sxs-lookup"><span data-stu-id="f669a-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="f669a-319">Ef þóknanir eru skattskyldar til viðskiptavinar og þú velur vsk-flokk í verksamningnum,er vsk-flokki sjálfkrafa færður inn í á reikningsreglu fyrir þóknun.</span><span class="sxs-lookup"><span data-stu-id="f669a-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="f669a-320">Til dæmis: Stofna reikningsreglur gildi tíma og efnis</span><span class="sxs-lookup"><span data-stu-id="f669a-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="f669a-321">Fyrirtæki þitt, hugbúnaðarráðgjafafyrirtæki, samþykkir að veita fimm tæknilega ráðgjafa til að vinna að hugbúnaðarþróunarverkefni fyrir viðskiptavin í næstu sex mánuði.</span><span class="sxs-lookup"><span data-stu-id="f669a-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="f669a-322">Viðskiptavinurinn fellst á að greiða 150 fyrir hverja ráðgjafatíma sem og kostnað fyrir skrifstofuvörur.</span><span class="sxs-lookup"><span data-stu-id="f669a-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="f669a-323">Fyrirtækið sendir reikning til viðskiptavinar í lok hvers mánaðar.</span><span class="sxs-lookup"><span data-stu-id="f669a-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="f669a-324">Þegar settur er upp verksamningur, samþykkir þú að rukka viðskiptavininn mánaðarlega fyrir tíma og efni á verki.</span><span class="sxs-lookup"><span data-stu-id="f669a-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="f669a-325">Að stofna reikningsreglur sem inniheldur eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="f669a-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="f669a-326">Samningstímabil er sex mánuðir.</span><span class="sxs-lookup"><span data-stu-id="f669a-326">The contract period is six months.</span></span>
-   <span data-ttu-id="f669a-327">Ráðgjafartíma er reiknaður á virðinu 150 á klukkustund.</span><span class="sxs-lookup"><span data-stu-id="f669a-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="f669a-328">Skrifstofuvörur eru reikningsfærð á kostnaðarverði, og heildarkostnaður fyrir verkið má ekki fara yfir 10.000.</span><span class="sxs-lookup"><span data-stu-id="f669a-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="f669a-329">Stofna reikning viðskiptavinar í lok hvers almanaksmánaðar á meðan verki stendur.</span><span class="sxs-lookup"><span data-stu-id="f669a-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="f669a-330">Fyrsta mánuð samtals 800 klukkustundir eru skráð hjá utanaðkomandi ráðgjöfum í verkinu.</span><span class="sxs-lookup"><span data-stu-id="f669a-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="f669a-331">Kostnaður skrifstofuvörur sem gjaldfærðir eru á verkið er 2.000.</span><span class="sxs-lookup"><span data-stu-id="f669a-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="f669a-332">Þessvegna, Í lok mánaðarins stofnar þú reikning upp á 122.000, reiknað sem 800 klukkustundir með 150 á klst. plús 2.000 fyrir skrifstofuvörur.</span><span class="sxs-lookup"><span data-stu-id="f669a-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



