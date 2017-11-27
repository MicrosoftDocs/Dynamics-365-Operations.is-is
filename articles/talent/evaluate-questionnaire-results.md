---
title: "Skoða og meta niðurstöður spurningalista"
description: "Þetta efni er útskýrt hvernig á að skoða og meta niðurstöður spurningalista sem svarendur að svara."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: kherr75
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9b6357288f340e4248cd5a87c2c3f773e0c32aec
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="view-and-evaluate-the-results-of-a-questionnaire"></a><span data-ttu-id="7e767-103">Skoða og meta niðurstöður spurningalista</span><span class="sxs-lookup"><span data-stu-id="7e767-103">View and evaluate the results of a questionnaire</span></span>

<span data-ttu-id="7e767-104">Þetta efni er útskýrt hvernig á að skoða og meta niðurstöður spurningalista sem svarendur að svara.</span><span class="sxs-lookup"><span data-stu-id="7e767-104">This topic explains how you can view and evaluate the results of questionnaires that respondents complete.</span></span> 

<span data-ttu-id="7e767-105">Eftir að svarendur hafa lokið við spurningarlista eru margar leiðir til að meta niðurstöðurnar, meðal annars eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="7e767-105">After respondents complete a questionnaire, you can view and evaluate the questionnaire results in the following ways:</span></span>

-   <span data-ttu-id="7e767-106">**Loknar svarsetur** – Skoða upplýsingar um spurningalista sem svarendur hafa lokið og mynda skýrslur til að taka saman svör og öll stig sem voru áunnin.</span><span class="sxs-lookup"><span data-stu-id="7e767-106">**Completed answer sessions** – View details about the questionnaires that respondents have completed, and generate reports to summarize answers and any points that were earned.</span></span>
-   <span data-ttu-id="7e767-107">**Niðurstöðuflokkar** - Skoða upplýsingar niðurstöðuflokka og tölfræði fyrir spurningalista.</span><span class="sxs-lookup"><span data-stu-id="7e767-107">**Result groups** – View result group details and statistics for questionnaires.</span></span> <span data-ttu-id="7e767-108">Hægt er að mynda niðurstöðuflokk talnagagna fyrir allar svarsetur eða eina svarsetu fyrir spurningalista eða allar svarsetur.</span><span class="sxs-lookup"><span data-stu-id="7e767-108">Result group statistics can be generated for either a single answer session  of a questionnaire or all answer sessions.</span></span>
-   <span data-ttu-id="7e767-109">**Talnagögn spurningalista** – Tilgreina skilyrði til að reikna talnagögn fyrir tiltekinn flokk svarenda.</span><span class="sxs-lookup"><span data-stu-id="7e767-109">**Questionnaire statistics** – Specify criteria to calculate statistics for a specific group of respondents.</span></span>

<span data-ttu-id="7e767-110">Einnig er hægt að mynda ýmsar skýrslur til að skoða niðurstöðurnar sem eru flokkaðar eftir einstaklingi, svarsetu eða niðurstöðuflokk.</span><span class="sxs-lookup"><span data-stu-id="7e767-110">You can also generate various reports to view results that are sorted by person, answer session, or result group.</span></span> <span data-ttu-id="7e767-111">Eftirfarandi skýrslur sem tengjast svaraða spurningalista eru tiltækar:</span><span class="sxs-lookup"><span data-stu-id="7e767-111">The following reports that are related to completed questionnaires are available:</span></span>

-   <span data-ttu-id="7e767-112">Svör</span><span class="sxs-lookup"><span data-stu-id="7e767-112">Answers</span></span>
-   <span data-ttu-id="7e767-113">Svör eftir spurningalistum</span><span class="sxs-lookup"><span data-stu-id="7e767-113">Answers per questionnaire</span></span>
-   <span data-ttu-id="7e767-114">Svör eftir mönnum</span><span class="sxs-lookup"><span data-stu-id="7e767-114">Answers per person</span></span>
-   <span data-ttu-id="7e767-115">Svörunargreining</span><span class="sxs-lookup"><span data-stu-id="7e767-115">Feedback analysis</span></span>

## <a name="answer-session-results"></a><span data-ttu-id="7e767-116">Niðurstöður svarsetu</span><span class="sxs-lookup"><span data-stu-id="7e767-116">Answer session results</span></span>
<span data-ttu-id="7e767-117">Þegar svarendur ljúka við spurningalista geturðu skoðað niðurstöður loknu svarsetanna.</span><span class="sxs-lookup"><span data-stu-id="7e767-117">After respondents complete a questionnaire, you can view the results of the completed answer sessions.</span></span> <span data-ttu-id="7e767-118">Svarseta er svar eins notanda við spurningalista.</span><span class="sxs-lookup"><span data-stu-id="7e767-118">An answer session is one user’s response to a questionnaire.</span></span> <span data-ttu-id="7e767-119">Hægt er að skoða upplýsingar um loknar svarsetur í **Svör** síðu.</span><span class="sxs-lookup"><span data-stu-id="7e767-119">You can view details about completed answer sessions on the **Answers** page.</span></span> <span data-ttu-id="7e767-120">Svarsetur sem eru höfð með í á **Svör** síðu eru síuð með mismunandi hætti eftir því hvernig þú opnar síðuna:</span><span class="sxs-lookup"><span data-stu-id="7e767-120">The answer sessions that are included on the **Answers** page are filtered in various ways, depending on how you open the page:</span></span>

-   <span data-ttu-id="7e767-121">Allir spurningalistar</span><span class="sxs-lookup"><span data-stu-id="7e767-121">All questionnaires</span></span>
-   <span data-ttu-id="7e767-122">Tiltekinn spurningalisti</span><span class="sxs-lookup"><span data-stu-id="7e767-122">A specific questionnaire</span></span>
-   <span data-ttu-id="7e767-123">Tiltekinn einstaklingur</span><span class="sxs-lookup"><span data-stu-id="7e767-123">A specific person</span></span>

<span data-ttu-id="7e767-124">Úr **Svör** síðu er hægt að skoða upplýsingar um svör, stig sem voru áunnin, svörum sem svarandi veitti í hverjum niðurstöðuflokki og spurningastigveldi sem var notað á valda spurningalistanum , ef notast var við spurningastigveldi.</span><span class="sxs-lookup"><span data-stu-id="7e767-124">From the **Answers** page, you can view details about answers, points that were earned, a respondent’s responses in each result group, and the question hierarchy that was used on the selected questionnaire, if a question hierarchy was used.</span></span> <span data-ttu-id="7e767-125">Einnig er hægt að mynda og prenta eftirfarandi skýrslur:</span><span class="sxs-lookup"><span data-stu-id="7e767-125">You can also generate and print the following reports:</span></span>

-   <span data-ttu-id="7e767-126">**Niðurstöðuskýrsla** – Þessi skýrsla sýnir myndræna framsetningu stiga sem voru áunnin eftir niðurstöðuflokki fyrir valda svarsetu.</span><span class="sxs-lookup"><span data-stu-id="7e767-126">**Results report** – This report shows a graphical representation of the points that were earned per result group for the selected answer session.</span></span>
-   <span data-ttu-id="7e767-127">**Svarskýrsla** – Þessi skýrsla sýnir svörin sem svarandi valdi fyrir hverja spurningu í spurningalistanum.</span><span class="sxs-lookup"><span data-stu-id="7e767-127">**Answer report** – This report shows the answers that the respondent selected for each question on the questionnaire.</span></span>
-   <span data-ttu-id="7e767-128">**Röng svör** – Þessi skýrsla sýnir upplýsingar sem tengjast röngum svörum sem svarandi valdi.</span><span class="sxs-lookup"><span data-stu-id="7e767-128">**Incorrect answers** – This report shows information that is related to the incorrect answers that the respondent selected.</span></span>

<span data-ttu-id="7e767-129">**Ábending:** **Niðurstöður** skýrsla býðst aðeins ef þú notar niðurstöðuflokka í spurningalista og ef valið er **niðurstöðusíðu** á **Spurningalista** síðu.</span><span class="sxs-lookup"><span data-stu-id="7e767-129">**Note:** The **Results** report is available only if you use results groups on the questionnaire, and if you selected **Results page** on the **Questionnaires** page.</span></span> <span data-ttu-id="7e767-130">Í **Svar** skýrslu og **Röng svör** skýrsla er aðeins tiltæk ef þú velur **Svar skýrsla** á í **Spurningalista** síðu.</span><span class="sxs-lookup"><span data-stu-id="7e767-130">The **Answer** report and the **Incorrect answers** report are available only if you selected **Answer report** on the **Questionnaires** page.</span></span>

## <a name="questionnaire-statistics"></a><span data-ttu-id="7e767-131">Talnagögn spurningalista</span><span class="sxs-lookup"><span data-stu-id="7e767-131">Questionnaire statistics</span></span>
<span data-ttu-id="7e767-132">Hægt er að nota talnagögn spurningalista til að greina niðurstöður svaraðra spurningalista, byggðan á útreikningi sem þú skilgreinir.</span><span class="sxs-lookup"><span data-stu-id="7e767-132">You can use questionnaire statistics to analyze the results of a completed questionnaire, based on calculations that you define.</span></span> <span data-ttu-id="7e767-133">Til að skilgreina útreikninga, verður að ljúka eftirfarandi verkum:</span><span class="sxs-lookup"><span data-stu-id="7e767-133">To define calculations, you must complete the following tasks:</span></span>

-   <span data-ttu-id="7e767-134">Velja skilyrði til að reikna og birta talnagögn.</span><span class="sxs-lookup"><span data-stu-id="7e767-134">Select criteria to calculate and display the statistics.</span></span>
    -   <span data-ttu-id="7e767-135">Hægt er að birta talnagögn spurningalista, spurningar, spurningaraðir eða flokka niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="7e767-135">You can show statistics by questionnaire, questions, question rows, or results groups.</span></span>
    -   <span data-ttu-id="7e767-136">Velja gerð línurits sem verður notað þegar niðurstöður eru skoðaðar.</span><span class="sxs-lookup"><span data-stu-id="7e767-136">Select the type of chart that will be used when you view results.</span></span>
    -   <span data-ttu-id="7e767-137">Velja gerðir einstaklinga af netinu eins og starfsmaður, tengiliður eða umsækjandi, til að hafa svör innifalin fyrir.</span><span class="sxs-lookup"><span data-stu-id="7e767-137">Select the types of people from the network, such as employees, contact persons, or applicants, to include answers for.</span></span> <span data-ttu-id="7e767-138">Einnig er hægt að taka með svör spurningalista sem nafnlaust var lokið.</span><span class="sxs-lookup"><span data-stu-id="7e767-138">You can also include answers from questionnaires that were completed anonymously.</span></span>
    -   <span data-ttu-id="7e767-139">Setja upp bil sem eru byggðar á aldur eða starfsaldur til að greina niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="7e767-139">Set up intervals that are based on age or seniority to analyze results.</span></span>
-   <span data-ttu-id="7e767-140">Velja eða skoða stillingar sem fínstilla efni talnagagnanna.</span><span class="sxs-lookup"><span data-stu-id="7e767-140">Select or verify settings that refine the subject of the statistics.</span></span> <span data-ttu-id="7e767-141">Ef t.d. er valið póstnúmer er hægt að greina niðurstöður allra svarenda innan þess svæðis.</span><span class="sxs-lookup"><span data-stu-id="7e767-141">For example, by selecting a ZIP Code or postal code, you can analyze results for all respondents within a specific geographic area.</span></span>
-   <span data-ttu-id="7e767-142">Velja eða staðfesta skilyrði til að greina niðurstöður eftir svaranda eða einkennum spurningalista.</span><span class="sxs-lookup"><span data-stu-id="7e767-142">Select or verify criteria to analyze results by respondent or questionnaire characteristics.</span></span> <span data-ttu-id="7e767-143">Til dæmis með því að velja **póstnúmer**, er hægt að greina samræmi milli staðsetningar svaranda og rétt svör.</span><span class="sxs-lookup"><span data-stu-id="7e767-143">For example, by selecting **ZIP/postal code**, you can analyze the correlation between a respondent’s location and correct answers.</span></span>

<span data-ttu-id="7e767-144">Stillingarnar sem eru skilgreindar eru vistaðar og er hægt að nota þær til þess að endurreikna niðurstöður reglulega.</span><span class="sxs-lookup"><span data-stu-id="7e767-144">The settings that you define are saved and can be used to periodically recalculate results.</span></span>

<a name="see-also"></a><span data-ttu-id="7e767-145">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="7e767-145">See also</span></span>
--------

[<span data-ttu-id="7e767-146">Hönnun spurningalista</span><span class="sxs-lookup"><span data-stu-id="7e767-146">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="7e767-147">Nota spurningalista.</span><span class="sxs-lookup"><span data-stu-id="7e767-147">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="7e767-148">Dreifa og ljúka°spurningalista</span><span class="sxs-lookup"><span data-stu-id="7e767-148">Distributing and completing questionnaires</span></span>](distribute-questionnaires.md)


