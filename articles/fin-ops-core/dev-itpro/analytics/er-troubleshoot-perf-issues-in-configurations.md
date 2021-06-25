---
title: Úrræðaleita vandamál sem tengjast afköstum í skilgreiningum rafrænnar skýrslugerðar
description: Þetta efnisatriði útskýrir hvernig á að finna og laga vandamál sem tengjast afköstum í skilgreiningum rafrænnar skýrslugerðar.
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d77c2aad904ba911ac19009d6a981ea4153aaa48
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216866"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a><span data-ttu-id="c57c0-103">Úrræðaleita vandamál sem tengjast afköstum í skilgreiningum rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="c57c0-103">Troubleshooting performance issues in ER configurations</span></span>

<span data-ttu-id="c57c0-104">Þetta efnisatriði útskýrir hvernig á að finna og leysa vandamál sem tengjast afköstum í [skilgreiningum](general-electronic-reporting.md#Configuration) [rafrænnar skýrslugerðar](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="c57c0-104">This topic explains how to find and solve performance issues in [Electronic reporting](general-electronic-reporting.md) (ER) [configurations](general-electronic-reporting.md#Configuration).</span></span>

<span data-ttu-id="c57c0-105">Yfirleitt felur rannsókn á afköstum í sér nokkur skref.</span><span class="sxs-lookup"><span data-stu-id="c57c0-105">Typically, performance investigation consists of several steps.</span></span>

1. <span data-ttu-id="c57c0-106">[Safna](#collecting-data) gögnum.</span><span class="sxs-lookup"><span data-stu-id="c57c0-106">[Collect](#collecting-data) data.</span></span>
2. <span data-ttu-id="c57c0-107">Greinið söfnuð gögn.</span><span class="sxs-lookup"><span data-stu-id="c57c0-107">Analyze the collected data.</span></span>
3. <span data-ttu-id="c57c0-108">Byggt á niðurstöðum greiningarinnar skal nota skilgreiningar rafrænnar skýrslugerðar til að [gera breytingar](#making-changes) eða taka ákvörðun um að safna meiri gögnum.</span><span class="sxs-lookup"><span data-stu-id="c57c0-108">Based on the results of the analysis, use ER configurations to [make changes](#making-changes), or decide to collect more data.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="c57c0-109">Úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="c57c0-109">Troubleshooting</span></span>

### <a name="analyze-execution-time"></a><span data-ttu-id="c57c0-110">Greina keyrslutíma</span><span class="sxs-lookup"><span data-stu-id="c57c0-110">Analyze execution time</span></span>

<span data-ttu-id="c57c0-111">Keyrslutími getur verið háður óvæntum þáttum á borð við önnur verk sem keyra í sama umhverfinu og skyndiminni sem notar gögn þegar kallað er á það í fyrsta skipti.</span><span class="sxs-lookup"><span data-stu-id="c57c0-111">Execution time can depend on unpredictable factors, such as other tasks that are running in the same environment and caching that uses data when it's called for the first time.</span></span> <span data-ttu-id="c57c0-112">Þess vegna ætti að endurtaka framkvæmdina og mælinguna nokkrum sinnum.</span><span class="sxs-lookup"><span data-stu-id="c57c0-112">Therefore, you should repeat the execution and measurement several times.</span></span>

<span data-ttu-id="c57c0-113">Stundum koma upp afkastavandamál sem tengjast ekki skilgreiningu rafræns skýrslugerðarsniðs sem er notað í skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="c57c0-113">Sometimes, performance issues aren't caused by an ER format configuration that is used for reporting.</span></span> <span data-ttu-id="c57c0-114">Þess í stað stafa þau af X++ kóðanum sem er notaður til að opna skilgreiningu rafræns skýrslugerðarsniðs.</span><span class="sxs-lookup"><span data-stu-id="c57c0-114">Instead, they are caused by the X++ code that is used to open that ER format configuration.</span></span>

1. <span data-ttu-id="c57c0-115">Í annaðhvort [Aðgerðamiðstöðinni](#infolog-time) eða [tilvikakladdanum](#event-log-time) skal skoða keyrslutíma skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="c57c0-115">In either the [Action center](#infolog-time) or the [event log](#event-log-time), look at the execution time of the report.</span></span>
2. <span data-ttu-id="c57c0-116">Berið saman keyrslutíma skýrslunnar við heildartíma keyrslunnar í aðstæðunum.</span><span class="sxs-lookup"><span data-stu-id="c57c0-116">Compare the execution time of the report with the total execution time in the scenario.</span></span>
3. <span data-ttu-id="c57c0-117">Ef keyrslutími skýrslunnar er mun styttri en heildartími keyrslunnar skal skoða gagnamagnið sem skýrslan vinnur úr:</span><span class="sxs-lookup"><span data-stu-id="c57c0-117">If the execution time of the report is much less than the total execution time, consider the amount of data that the report processes:</span></span>

    - <span data-ttu-id="c57c0-118">Ef skýrslan vinnur úr litlu gagnamagni gæti vandamálið tengst hleðslutíma skilgreiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="c57c0-118">If the report processes a small amount of data, the issue might involve the loading time of the configuration.</span></span>
    - <span data-ttu-id="c57c0-119">Ef skýrslan vinnur úr miklu gagnamagni gæti vandamálið tengst forvinnslu X++.</span><span class="sxs-lookup"><span data-stu-id="c57c0-119">If the report processes a large amount of data, the issue might involve preprocessing X++.</span></span> <span data-ttu-id="c57c0-120">Notið [Rakningarþáttara](#analyze-trace-parser-trace) til að greina vandamálið.</span><span class="sxs-lookup"><span data-stu-id="c57c0-120">Use [Trace parser](#analyze-trace-parser-trace) to analyze this case.</span></span>

    <span data-ttu-id="c57c0-121">Sjáið næstu hluta fyrir annars konar vandamál.</span><span class="sxs-lookup"><span data-stu-id="c57c0-121">For other cases, see the next sections.</span></span>

4. <span data-ttu-id="c57c0-122">Keyrið mörg próf sem fela í sér mismunandi gagnamagn til að fá úr því skorið hvort keyrslutíminn fari eftir gagnamagninu.</span><span class="sxs-lookup"><span data-stu-id="c57c0-122">Run multiple tests that involve different amounts of data to determine how the execution time depends on the amount of data.</span></span>

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a><span data-ttu-id="c57c0-123">Greina rakningar rakningarþáttara</span><span class="sxs-lookup"><span data-stu-id="c57c0-123">Analyze Trace parser traces</span></span>

<span data-ttu-id="c57c0-124">Undirbúið lítið sýnishorn eða safnið saman nokkrum rakningum á handahófskenndum tímapunktum skýrslumyndunar.</span><span class="sxs-lookup"><span data-stu-id="c57c0-124">Prepare a small example, or collect several traces during random parts of the report generation.</span></span>

<span data-ttu-id="c57c0-125">Gerið síðan hefðbundna alhliða greiningu í [Rakningarþáttara](#trace-parser) og svarið eftirfarandi spurningum:</span><span class="sxs-lookup"><span data-stu-id="c57c0-125">Then, in [Trace parser](#trace-parser), do a standard bottom-to-up analysis, and answer the following questions:</span></span>

- <span data-ttu-id="c57c0-126">Hverjar eru helstu aðferðirnar hvað varðar tímanotkun?</span><span class="sxs-lookup"><span data-stu-id="c57c0-126">What are the top methods in terms of time consumption?</span></span>
- <span data-ttu-id="c57c0-127">Hvaða hluta af heildartímanum nota þessar aðferðir?</span><span class="sxs-lookup"><span data-stu-id="c57c0-127">What part of the overall time do those methods use?</span></span>

<span data-ttu-id="c57c0-128">Svarið sömu spurningunum fyrir fyrirspurnir.</span><span class="sxs-lookup"><span data-stu-id="c57c0-128">Answer the same questions for queries.</span></span>

<span data-ttu-id="c57c0-129">Ef þú sérð að aðferðir hafa forskeytið „ER“ skaltu fara í næsta hluta.</span><span class="sxs-lookup"><span data-stu-id="c57c0-129">If you see that methods are prefixed with "ER," move on to the next section.</span></span>

<span data-ttu-id="c57c0-130">Ef þú sérð að aðferðir eða fyrirspurnir eiga uppruna sinn í forritspakkanum skaltu íhuga almennar fínstillingar (til dæmis búa til atriðaskrá).</span><span class="sxs-lookup"><span data-stu-id="c57c0-130">If you see that methods or queries originated in the application suite, consider generic optimizations (for example, create indexes).</span></span>

<span data-ttu-id="c57c0-131">Greinið fjölda kalla.</span><span class="sxs-lookup"><span data-stu-id="c57c0-131">Analyze the number of calls.</span></span> <span data-ttu-id="c57c0-132">Ef talan er umtalsvert hærri en búist var við ætti að íhuga að vista samsvarandi hnúta skilgreiningarinnar í skyndiminni.</span><span class="sxs-lookup"><span data-stu-id="c57c0-132">If the number is significantly higher than expected, consider caching the corresponding nodes of the configuration.</span></span>

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a><span data-ttu-id="c57c0-133">Greina gagnagrunnsköll</span><span class="sxs-lookup"><span data-stu-id="c57c0-133">Analyze database calls</span></span>

<span data-ttu-id="c57c0-134">Undirbúið dæmi sem inniheldur lítið magn af gögnum þannig að hægt sé að safna [Rakningu rafrænnar skýrslugerðar](#electronic-reporting-traces).</span><span class="sxs-lookup"><span data-stu-id="c57c0-134">Prepare an example that has a small amount of data, so that you can collect an [ER trace](#electronic-reporting-traces).</span></span>

<span data-ttu-id="c57c0-135">Opnið síðan rakninguna í hönnuði líkanavörpunar rafrænnar skýrslugerðar og kíkið neðst á síðuna.</span><span class="sxs-lookup"><span data-stu-id="c57c0-135">Then open the trace in the ER model mapping designer, and look at the bottom of the page.</span></span> <span data-ttu-id="c57c0-136">Svarið eftirfarandi spurningum:</span><span class="sxs-lookup"><span data-stu-id="c57c0-136">Answer the following questions:</span></span>

- <span data-ttu-id="c57c0-137">Eru einhverjar tvítekningar á fyrirspurn?</span><span class="sxs-lookup"><span data-stu-id="c57c0-137">Is there any query duplication?</span></span> <span data-ttu-id="c57c0-138">Ef svo er skaltu íhuga eina af eftirfarandi leiðréttingum:</span><span class="sxs-lookup"><span data-stu-id="c57c0-138">If there is, consider one of the following fixes:</span></span>

    - <span data-ttu-id="c57c0-139">[Notaðu vistun í skyndiminni](#use-caching) ef þú telur að mörg köll séu inni í einni yfirskrá.</span><span class="sxs-lookup"><span data-stu-id="c57c0-139">[Use caching](#use-caching) if you think that there are several calls inside one parent record.</span></span>
    - <span data-ttu-id="c57c0-140">[Notaðu færibreytustilltan reiknaðan reit sem vistaður er í skyndiminni](#cached-parameterized) ef þú telur að það séu köll í sömu færsluna inni í mismunandi færslum.</span><span class="sxs-lookup"><span data-stu-id="c57c0-140">[Use a cached, parameterized calculated field](#cached-parameterized) if you think that there are calls to the same record inside different records.</span></span>
    - <span data-ttu-id="c57c0-141">[Notaðu **JOIN** gagnagjafa](#use-join-datasource) ef nauðsyn reynist að lesa umtalsverðan fjölda af færslum úr gagnagrunni.</span><span class="sxs-lookup"><span data-stu-id="c57c0-141">[Use a **JOIN** data source](#use-join-datasource) if you have to read to a substantial number of different records from a database.</span></span>

- <span data-ttu-id="c57c0-142">Samræmist fjöldi fyrirspurna og sóttra færslna heildarfjölda gagna?</span><span class="sxs-lookup"><span data-stu-id="c57c0-142">Does the number of queries and fetched records correspond to the overall amount of data?</span></span> <span data-ttu-id="c57c0-143">Ef skjal hefur t.d. 10 línur, sýnir tölfræðin að skýrslan dragi út 10 línur eða 1000 línur?</span><span class="sxs-lookup"><span data-stu-id="c57c0-143">For example, if a document has 10 lines, do the statistics show that the report extracts 10 lines or 1,000 lines?</span></span> <span data-ttu-id="c57c0-144">Ef talsverður fjöldi færslna er sóttur skal íhuga eina af eftirfarandi lagfæringum:</span><span class="sxs-lookup"><span data-stu-id="c57c0-144">If you have a substantial number of fetched records, consider one of the following fixes:</span></span>

    - <span data-ttu-id="c57c0-145">[Notið **FILTER** aðgerðina í stað **WHERE** aðgerðarinnar](#filter) til að vinna úr gögnum hjá SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c57c0-145">[Use the **FILTER** function instead of the **WHERE** function](#filter) to process data on the SQL Server side.</span></span>
    - <span data-ttu-id="c57c0-146">Notið vistun í skyndiminni til að forðast að sækja sömu gögnin.</span><span class="sxs-lookup"><span data-stu-id="c57c0-146">Use caching to avoid fetching the same data.</span></span>
    - <span data-ttu-id="c57c0-147">[Notið söfnuð gögn](#collected-data) til að forðast að sækja sömu gögnin fyrir samantekt.</span><span class="sxs-lookup"><span data-stu-id="c57c0-147">[Use collected data functions](#collected-data) to avoid fetching the same data for summarization.</span></span>

### <a name="analyze-perfview-traces"></a><span data-ttu-id="c57c0-148">Greina PerfView-rakningar</span><span class="sxs-lookup"><span data-stu-id="c57c0-148">Analyze PerfView traces</span></span>

<span data-ttu-id="c57c0-149">[PerfView](#perfview) er verkfæri fyrir reynda þróunaraðila.</span><span class="sxs-lookup"><span data-stu-id="c57c0-149">[PerfView](#perfview) is a tool for experienced developers.</span></span> <span data-ttu-id="c57c0-150">Ítarlegri upplýsingar um eftirfarandi skref er að finna í [Grunnatriði um tíma veggjaklukku](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span><span class="sxs-lookup"><span data-stu-id="c57c0-150">For more detailed information about the following steps, see [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span></span>

1. <span data-ttu-id="c57c0-151">Safnið saman rakningu með því að nota tíma þráðar.</span><span class="sxs-lookup"><span data-stu-id="c57c0-151">Collect a trace by using thread time.</span></span>
2. <span data-ttu-id="c57c0-152">Hafið aðeins með stafla sem nota **runUnattended** til að sía aðeins þráðinn sem er með skilgreiningarkeyrslu.</span><span class="sxs-lookup"><span data-stu-id="c57c0-152">Include only stacks that use **runUnattended**, to filter only the thread that has configuration execution.</span></span> <span data-ttu-id="c57c0-153">(Bætið **runUnattended** við **IncPats** innsláttarreitinn.)</span><span class="sxs-lookup"><span data-stu-id="c57c0-153">(Add **runUnattended** to the **IncPats** input box.)</span></span>
3. <span data-ttu-id="c57c0-154">Fellið saman örgjörva, netkerfi og útilokaðan tíma.</span><span class="sxs-lookup"><span data-stu-id="c57c0-154">Fold all CPU, network, and blocked time.</span></span>
4. <span data-ttu-id="c57c0-155">Hlaðið inn [forstillingum rafrænnar skýrslugerðar fyrir PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span><span class="sxs-lookup"><span data-stu-id="c57c0-155">Load [ER presets for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span></span>
5. <span data-ttu-id="c57c0-156">Veljið **ER** \> **Önnur forstilling**.</span><span class="sxs-lookup"><span data-stu-id="c57c0-156">Select **ER** \> **Other preset**.</span></span>
6. <span data-ttu-id="c57c0-157">Skoðið nöfnin:</span><span class="sxs-lookup"><span data-stu-id="c57c0-157">Look at the names:</span></span>

    - <span data-ttu-id="c57c0-158">Líklega sjáið þið verkvangskóðann sem notar mestan tímann.</span><span class="sxs-lookup"><span data-stu-id="c57c0-158">You will probably see the platform code that consumes the most time.</span></span>
    - <span data-ttu-id="c57c0-159">Hægt er að tvípikka (eða tvísmella) og fara upp í gegnum **hringjendur**.</span><span class="sxs-lookup"><span data-stu-id="c57c0-159">You can double-tap (or double-click) and go up through **callees**.</span></span>

        <span data-ttu-id="c57c0-160">Ef klasar finnast með forskeytinu „ERExpression“ og þeir eru aðgerðir sem tengjast formúlum er hægt að giska á heiti aðgerðarinnar út frá klasaheitinu og hægt er að kíkja á geymslu rafrænnar skýrslugerðar til að skoða eigindirnar.</span><span class="sxs-lookup"><span data-stu-id="c57c0-160">If you find classes that have the prefix "ERExpression," and if they are functions that are related to formulas, you can guess the function name based on the class name, and you can look at the ER repo to view the attributes.</span></span>

### <a name="fixes"></a><span data-ttu-id="c57c0-161">Lagfæringar</span><span class="sxs-lookup"><span data-stu-id="c57c0-161">Fixes</span></span>

- <span data-ttu-id="c57c0-162">Ef kemur í ljós að mestur örgjörvatíminn fer í fyrirspurnir skal reyna að draga úr fjölda fyrirspurna:</span><span class="sxs-lookup"><span data-stu-id="c57c0-162">If you see that most of the CPU time is consumed by queries, try to reduce the number of queries:</span></span>

    - <span data-ttu-id="c57c0-163">[Farið yfir rakningu rafrænnar skýrslugerðar](#analyze-database-calls) fyrir tvíteknar fyrirspurnir.</span><span class="sxs-lookup"><span data-stu-id="c57c0-163">[Review the ER trace](#analyze-database-calls) for duplicated queries.</span></span>
    - <span data-ttu-id="c57c0-164">Skoðið hversu margar færslur eru sóttar og metið hversu mikið af gögnum eigi fræðilega að sækja.</span><span class="sxs-lookup"><span data-stu-id="c57c0-164">See how many records are fetched, and evaluate how much data should theoretically be fetched.</span></span>

- <span data-ttu-id="c57c0-165">Ef kemur í ljós að meirihluti örgjörvatíma fer í aðgerðir sem eru notaðar skal reyna að finna staðinn í skilgreiningunni sem notar flest tilföngin.</span><span class="sxs-lookup"><span data-stu-id="c57c0-165">If you see that most of the CPU time is consumed by the functions that are used, try to find the place in the configuration that consumes the most resources.</span></span>
- <span data-ttu-id="c57c0-166">Ef kemur í ljós að mestur örgjörvatími fer í aðgerðir gagnasöfnunar skal íhuga að skipta þeim út fyrir *SQL-flokka eftir* á síðu líkanavörpunar.</span><span class="sxs-lookup"><span data-stu-id="c57c0-166">If you see that most of the CPU time is consumed by data collection functions, consider replacing them with *SQL group by* on the model mapping side.</span></span>

### <a name="collecting-data"></a><a name="collecting-data"></a><span data-ttu-id="c57c0-167">Safna gögnum</span><span class="sxs-lookup"><span data-stu-id="c57c0-167">Collecting data</span></span>

<span data-ttu-id="c57c0-168">Til eru nokkrar leiðir til að safna tiltækum gögnum eftir umhverfinu þínu:</span><span class="sxs-lookup"><span data-stu-id="c57c0-168">Depending on your environment, there are several ways to collect available data:</span></span>

- <span data-ttu-id="c57c0-169">Sækja heildarkeyrslutíma:</span><span class="sxs-lookup"><span data-stu-id="c57c0-169">Get the total running time:</span></span>

    - <span data-ttu-id="c57c0-170">Úr aðgerðamiðstöðinni</span><span class="sxs-lookup"><span data-stu-id="c57c0-170">From the Action center</span></span>
    - <span data-ttu-id="c57c0-171">Frá viðburðaferli</span><span class="sxs-lookup"><span data-stu-id="c57c0-171">From the event log</span></span>

- <span data-ttu-id="c57c0-172">Setjið saman keyrsluna:</span><span class="sxs-lookup"><span data-stu-id="c57c0-172">Profile the execution:</span></span>

    - <span data-ttu-id="c57c0-173">Með því að nota verkfæri rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="c57c0-173">By using ER tools</span></span>
    - <span data-ttu-id="c57c0-174">Með því að nota rakningarþáttara</span><span class="sxs-lookup"><span data-stu-id="c57c0-174">By using Trace parser</span></span>
    - <span data-ttu-id="c57c0-175">Með því að nota PerfView</span><span class="sxs-lookup"><span data-stu-id="c57c0-175">By using PerfView</span></span>

#### <a name="collecting-data-in-a-production-environment"></a><span data-ttu-id="c57c0-176">Gagnasöfnun í vinnsluumhverfi</span><span class="sxs-lookup"><span data-stu-id="c57c0-176">Collecting data in a production environment</span></span>

<span data-ttu-id="c57c0-177">Stundum er eingöngu hægt að endurskapa vandamál í vinnsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="c57c0-177">Sometimes, issues can be reproduced only in a production environment.</span></span> <span data-ttu-id="c57c0-178">Hægt er að safna gögnum á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="c57c0-178">Data can be collected in the following ways:</span></span>

- <span data-ttu-id="c57c0-179">Með því að nota rakningar [Rakningarþáttara](../perf-test/trace-trace-tutorial.md)</span><span class="sxs-lookup"><span data-stu-id="c57c0-179">By using [Trace parser](../perf-test/trace-trace-tutorial.md) traces</span></span>
- <span data-ttu-id="c57c0-180">Með því að nota rakningar [rafrænnar skýrslugerðarkeyrslu](trace-execution-er-troubleshoot-perf.md)</span><span class="sxs-lookup"><span data-stu-id="c57c0-180">By using [ER execution](trace-execution-er-troubleshoot-perf.md) traces</span></span>
- <span data-ttu-id="c57c0-181">Með því að nota heildartíma keyrslu</span><span class="sxs-lookup"><span data-stu-id="c57c0-181">By using the total execution time</span></span>

#### <a name="collecting-data-in-a-development-environment"></a><span data-ttu-id="c57c0-182">Gagnasöfnun í þróunarumhverfi</span><span class="sxs-lookup"><span data-stu-id="c57c0-182">Collecting data in a development environment</span></span>

<span data-ttu-id="c57c0-183">Auk þeirra verkfæra sem hægt er að nota í vinnsluuumhverfi eru til ýmis verkfæri sem hægt er að nota í þróunarumhverfi:</span><span class="sxs-lookup"><span data-stu-id="c57c0-183">In addition to the tools that can be used in a production environment, there are several tools that you can use in a development environment:</span></span>

- <span data-ttu-id="c57c0-184">Tilvikakladdi (Microsoft-Dynamics-ElectronicReporting).</span><span class="sxs-lookup"><span data-stu-id="c57c0-184">Event log (Microsoft-Dynamics-ElectronicReporting).</span></span> <span data-ttu-id="c57c0-185">Þessi kladdi getur gefið þér heildartíma keyrslu.</span><span class="sxs-lookup"><span data-stu-id="c57c0-185">This log can give you the total execution time.</span></span>
- <span data-ttu-id="c57c0-186">Algeng .NET-verkfæri á borð við PerfView.</span><span class="sxs-lookup"><span data-stu-id="c57c0-186">Common .NET tools, such as PerfView.</span></span>

<span data-ttu-id="c57c0-187">Þróunarumhverfi veitir þér aukinn sveigjanleika til að gera tilraunir.</span><span class="sxs-lookup"><span data-stu-id="c57c0-187">Additionally, a development environment gives you more flexibility to experiment.</span></span> <span data-ttu-id="c57c0-188">Til dæmis er hægt að slökkva á skýrsluhlutum til að sjá hvaða áhrif það hefur á keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="c57c0-188">For example, you can turn off parts of reports to see how the execution time is affected.</span></span>

### <a name="tools"></a><a name="tools"></a><span data-ttu-id="c57c0-189">Verkfæri</span><span class="sxs-lookup"><span data-stu-id="c57c0-189">Tools</span></span>

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a><span data-ttu-id="c57c0-190">Keyrslutími í aðgerðamiðstöðinni</span><span class="sxs-lookup"><span data-stu-id="c57c0-190">Execution time in the Action center</span></span>

<span data-ttu-id="c57c0-191">Rafræn skýrslugerð getur sýnt keyrslutíma skilgreiningarinnar í aðgerðamiðstöðinni.</span><span class="sxs-lookup"><span data-stu-id="c57c0-191">ER can show the execution time of the configuration in the Action center.</span></span> <span data-ttu-id="c57c0-192">Þessi valkostur virkar aðeins fyrir tiltekinn notanda og tiltekið fyrirtæki og aðeins fyrir gagnvirkar lotur.</span><span class="sxs-lookup"><span data-stu-id="c57c0-192">This option works only for a specific user and a specific company, and only for interactive sessions.</span></span> <span data-ttu-id="c57c0-193">Til að gera þennan eiginleika aðgengilegan skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="c57c0-193">To make this feature available, follow these steps.</span></span>

1. <span data-ttu-id="c57c0-194">Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="c57c0-194">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="c57c0-195">Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.</span><span class="sxs-lookup"><span data-stu-id="c57c0-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="c57c0-196">Í svarglugganum **Færibreytur notanda** skal stilla valkostinn **Sýna tíma skráarmyndunar** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="c57c0-196">In the **User parameters** dialog box, set the **Show file generation time** option to **Yes**.</span></span>

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a><span data-ttu-id="c57c0-197">Keyrslutími í tilvikakladdanum</span><span class="sxs-lookup"><span data-stu-id="c57c0-197">Execution time in the event log</span></span>

1. <span data-ttu-id="c57c0-198">Opnið Windows Event Viewer.</span><span class="sxs-lookup"><span data-stu-id="c57c0-198">Open Windows Event Viewer.</span></span>
2. <span data-ttu-id="c57c0-199">Undir **Forrits- og þjónustukladda** skal opna **Microsoft-Dynamics-ElectronicReporting/Operational**.</span><span class="sxs-lookup"><span data-stu-id="c57c0-199">Under **Applications and Services logs**, open **Microsoft-Dynamics-ElectronicReporting/Operational**.</span></span>
3. <span data-ttu-id="c57c0-200">Leitið að tilvikum **FormatMapingRun** þar sem **EventID=2** vegna þess að þessi tilvik innihalda upplýsingarnar um liðinn tíma.</span><span class="sxs-lookup"><span data-stu-id="c57c0-200">Look for **FormatMapingRun** events where **EventID=2**, because these events contain the information about elapsed time.</span></span>

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a><span data-ttu-id="c57c0-201">Rakningar rakningarþáttara</span><span class="sxs-lookup"><span data-stu-id="c57c0-201">Trace parser traces</span></span> 

<span data-ttu-id="c57c0-202">Þar sem rafræn skýrslugerð er innfelld í X++ er hægt að nota algeng X++ verkfæri til að greina afköst.</span><span class="sxs-lookup"><span data-stu-id="c57c0-202">Because ER is implemented in X++, you can use common X++ tools to analyze performance.</span></span> <span data-ttu-id="c57c0-203">Frekari upplýsingar er að finna í [Gera rakningar með því að nota rakningarþáttara](../perf-test/trace-trace-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="c57c0-203">For more information, see [Take traces by using Trace parser](../perf-test/trace-trace-tutorial.md).</span></span>

<span data-ttu-id="c57c0-204">Nokkrar takmarkanir eru á þessari nálgun.</span><span class="sxs-lookup"><span data-stu-id="c57c0-204">There are a few limitations to this approach.</span></span> <span data-ttu-id="c57c0-205">Þar sem hluti rafrænnar skýrslugerðar er felldur inn í C# verða ekki allar upplýsingar aðgengilegar.</span><span class="sxs-lookup"><span data-stu-id="c57c0-205">Because part of ER is implemented in C#, not all the details will be available.</span></span> <span data-ttu-id="c57c0-206">Hins vegar er hægt að skoða upplýsingar um gagnanotkun.</span><span class="sxs-lookup"><span data-stu-id="c57c0-206">However, you can view the data usage details.</span></span> <span data-ttu-id="c57c0-207">Auk þess geta langar skýrslukeyrslur farið fram úr geymslumörkum rakningar.</span><span class="sxs-lookup"><span data-stu-id="c57c0-207">Additionally, long report runs can exceed trace storage limitations.</span></span>

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a><span data-ttu-id="c57c0-208">ER spor</span><span class="sxs-lookup"><span data-stu-id="c57c0-208">ER traces</span></span>

<span data-ttu-id="c57c0-209">Rafræn skýrslugerð getur safnað sínum eigin rakningum og hún hefur myndrænar framsetningar og greiningarverkfæri fyrir þessar rakningar.</span><span class="sxs-lookup"><span data-stu-id="c57c0-209">ER can collect its own traces, and it has visualization and analysis tools for those traces.</span></span> <span data-ttu-id="c57c0-210">Frekari upplýsingar er að finna í [Rekja framkvæmd á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="c57c0-210">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

#### <a name="perfview"></a><a name="perfview"></a><span data-ttu-id="c57c0-211">PerfView</span><span class="sxs-lookup"><span data-stu-id="c57c0-211">PerfView</span></span>

<span data-ttu-id="c57c0-212">Þar sem bæði X++ og rafræn skýrslugerð eru felld inn ofan á .NET-verkvanginn er hægt að nota algeng .NET-verkfæri.</span><span class="sxs-lookup"><span data-stu-id="c57c0-212">Because both X++ and ER are implemented on top of the .NET platform, you can use common .NET tools.</span></span> <span data-ttu-id="c57c0-213">Til dæmis er hægt að nota ókeypis [PerfView](https://github.com/Microsoft/perfview) verkfæri.</span><span class="sxs-lookup"><span data-stu-id="c57c0-213">For example, you can use the free [PerfView](https://github.com/Microsoft/perfview) tool.</span></span>

<span data-ttu-id="c57c0-214">Einnig er hægt að safna gögnum úr skipanalínunni.</span><span class="sxs-lookup"><span data-stu-id="c57c0-214">You can also collect data from the command line.</span></span> <span data-ttu-id="c57c0-215">Til dæmis safnar eftirfarandi forskrift Windows PowerShell keyrslutímanum þar til keyrsla á einhverju sniði er stöðvuð í vélinni.</span><span class="sxs-lookup"><span data-stu-id="c57c0-215">For example, the following Windows PowerShell script collects the execution time until any format execution is stopped on the machine.</span></span>

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

<span data-ttu-id="c57c0-216">Nokkrar takmarkanir eru á þessari nálgun.</span><span class="sxs-lookup"><span data-stu-id="c57c0-216">There are a few limitations to this approach.</span></span> <span data-ttu-id="c57c0-217">Þú verður að hafa stjórnandaaðgang að vélinni.</span><span class="sxs-lookup"><span data-stu-id="c57c0-217">You must have administrative access to the machine.</span></span> <span data-ttu-id="c57c0-218">Að auki þarftu að vera reyndur þróunaraðili þar sem lærdómsferlið er krefjandi.</span><span class="sxs-lookup"><span data-stu-id="c57c0-218">Additionally, you must be an experienced developer, because there is a steep learning curve.</span></span>

### <a name="making-changes"></a><a name="making-changes"></a><span data-ttu-id="c57c0-219">Að gera breytingar</span><span class="sxs-lookup"><span data-stu-id="c57c0-219">Making changes</span></span>

#### <a name="use-caching"></a><a name="use-caching"></a><span data-ttu-id="c57c0-220">Nota vistun í skyndiminni</span><span class="sxs-lookup"><span data-stu-id="c57c0-220">Use caching</span></span>

<span data-ttu-id="c57c0-221">Þrátt fyrir að vistun í skyndiminni dregur úr tímanum sem þarf til að sækja gögn aftur, kostar það minni.</span><span class="sxs-lookup"><span data-stu-id="c57c0-221">Although caching reduces the amount of time that is required to fetch data again, it costs memory.</span></span> <span data-ttu-id="c57c0-222">Notið vistun í skyndiminni í tilvikum þar sem fjöldi sóttra gagna er ekki mjög mikill.</span><span class="sxs-lookup"><span data-stu-id="c57c0-222">Use caching in cases where the amount of fetched data isn't very large.</span></span> <span data-ttu-id="c57c0-223">Frekari upplýsingar og dæmi sem sýnir hvernig á að nota vistun í skyndiminni er að finna í [Bæta líkanavörpun á grundvelli upplýsinga úr framkvæmdarakningu](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span><span class="sxs-lookup"><span data-stu-id="c57c0-223">For more information and an example that shows how to use caching, see [Improve the model mapping based on information from the execution trace](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span></span>

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a><span data-ttu-id="c57c0-224">Nota færibreytustilltan reiknaðan reit sem vistaður er í skyndiminni</span><span class="sxs-lookup"><span data-stu-id="c57c0-224">Use a cached, parameterized calculated field</span></span>

<span data-ttu-id="c57c0-225">Stundum þarf að fletta upp gildum ítrekað.</span><span class="sxs-lookup"><span data-stu-id="c57c0-225">Sometimes, values must be looked up repeatedly.</span></span> <span data-ttu-id="c57c0-226">Sem dæmi má nefna reikningsheiti og reikningsnúmer.</span><span class="sxs-lookup"><span data-stu-id="c57c0-226">Examples include account names and account numbers.</span></span> <span data-ttu-id="c57c0-227">Til að spara tíma er hægt að búa til reiknaðan reit með færibreytum á efsta stigi og bæta svo reitnum við skyndiminnið.</span><span class="sxs-lookup"><span data-stu-id="c57c0-227">To help save time, you can create a calculated field that has parameters on the top level, and then add the field to the cache.</span></span>

<span data-ttu-id="c57c0-228">Mælt er með því að aðferðin sé aðeins notuð þegar stærð gagna í skyndiminni er lítil.</span><span class="sxs-lookup"><span data-stu-id="c57c0-228">We recommend that you use this approach only when the size of the cached data is small.</span></span> <span data-ttu-id="c57c0-229">Frekari upplýsingar eru í [Bættu frammistöðu rafrænna skýrslugerðarlausna með því að bæta við gagnagjöfum með reiknaða reiti með færibreytum](er-calculated-field-ds-performance.md).</span><span class="sxs-lookup"><span data-stu-id="c57c0-229">For more information, see [Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources](er-calculated-field-ds-performance.md).</span></span>

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a><span data-ttu-id="c57c0-230">Nota JOIN-gagnagjafi</span><span class="sxs-lookup"><span data-stu-id="c57c0-230">Use a JOIN data source</span></span>

<span data-ttu-id="c57c0-231">**JOIN** gagnagjafi gerir kleift að sækja margar tengdar færslur í einni fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="c57c0-231">A **JOIN** data source enables several connected records to be fetched by one query.</span></span> <span data-ttu-id="c57c0-232">Ekki þarf að nota sérstaka fyrirspurn til að sækja hverja tengda færslu.</span><span class="sxs-lookup"><span data-stu-id="c57c0-232">A separate query doesn't have to be used to fetch each connected record.</span></span> <span data-ttu-id="c57c0-233">Ef t.d. 1000 línur eru til staðar og gögn um hverja línu út frá tengslum verða fyrirspurnirnar samtals 1001 (= 1000 + 1).</span><span class="sxs-lookup"><span data-stu-id="c57c0-233">For example, if you have 1,000 lines, and you fetch item data for each line by relation, you will have 1,001 queries (= 1,000 + 1).</span></span> <span data-ttu-id="c57c0-234">Ef **JOIN** gagnagjafi er notaður þarf aðeins að nota eina fyrirspurn til að sækja sömu gögnin.</span><span class="sxs-lookup"><span data-stu-id="c57c0-234">If you use a **JOIN** data source, you will use only one query to fetch the same data.</span></span> <span data-ttu-id="c57c0-235">Frekari upplýsingar eru í [Notaðu JOIN gagnaheimildir í ER-líkanavörpun til að fá gögn úr mörgum töflum forrita](er-join-data-sources.md).</span><span class="sxs-lookup"><span data-stu-id="c57c0-235">For more information, see [Use JOIN data sources in ER model mappings to get data from multiple application tables](er-join-data-sources.md).</span></span>

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a><span data-ttu-id="c57c0-236">Nota FILTER-aðgerðina í staðinn fyrir WHERE-aðgerðina</span><span class="sxs-lookup"><span data-stu-id="c57c0-236">Use the FILTER function instead of the WHERE function</span></span>

<span data-ttu-id="c57c0-237">**[FILTER](er-functions-list-filter.md)** aðgerðin keyrir skilyrði á SQL-þjóni, en **WHERE** aðgerðin sækir öll gögn úr listanum, eina færslu í einu, og notar skilyrðið fyrir hverja færslu fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="c57c0-237">The **[FILTER](er-functions-list-filter.md)** function runs conditions on SQL Server, whereas the **WHERE** function fetches all data from the list, one record at a time, and applies the condition for each record.</span></span> <span data-ttu-id="c57c0-238">Til dæmis ef velja á eina færslu af 1000.</span><span class="sxs-lookup"><span data-stu-id="c57c0-238">For example, you want to select one record out of 1,000 records.</span></span> <span data-ttu-id="c57c0-239">Ef notað er **WHERE** verða allar 1000 færslurnar sóttar.</span><span class="sxs-lookup"><span data-stu-id="c57c0-239">If you use **WHERE**, all 1,000 records will be fetched.</span></span> <span data-ttu-id="c57c0-240">Ef hins vegar **FILTER** er notað verður nákvæmlega ein færsla sótt.</span><span class="sxs-lookup"><span data-stu-id="c57c0-240">However, if you use **FILTER**, exactly one record will be fetched.</span></span> <span data-ttu-id="c57c0-241">**FILTER** getur einnig notað atriðaskrá gagnagrunnsins.</span><span class="sxs-lookup"><span data-stu-id="c57c0-241">**FILTER** can also use indexes on the database side.</span></span>

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a><span data-ttu-id="c57c0-242">Aðgerðir gagnasöfnunar eða gagnagjafi uppsafnaðra gagna notað</span><span class="sxs-lookup"><span data-stu-id="c57c0-242">Using collected data functions or an accumulated data data source</span></span>

<span data-ttu-id="c57c0-243">Ef skilgreiningin er með *flokka eftir* þátt sem tekur saman gögn sem skýrsla sótti mun þátturinn sækja öll gögnin aftur.</span><span class="sxs-lookup"><span data-stu-id="c57c0-243">If your configuration has a *group by* component that summarizes previously fetched data by report, the component will fetch all the data again.</span></span> <span data-ttu-id="c57c0-244">Með því að nota aðgerðir gagnasöfnunar gerir þú rafrænni skýrslugerð kleift að safna saman gögnum þegar sótt er í fyrsta skipti.</span><span class="sxs-lookup"><span data-stu-id="c57c0-244">By using collected data functions, you enable ER to accumulate data during the first fetch.</span></span> <span data-ttu-id="c57c0-245">Frekari upplýsingar er að finna í [Skilgreina snið rafrænnar skýrslugerðar til að gera talningu og samlagningu](tasks/er-format-counting-summing-2.md).</span><span class="sxs-lookup"><span data-stu-id="c57c0-245">For more information, see [ER Configure format to do counting and summing](tasks/er-format-counting-summing-2.md).</span></span>

#### <a name="rewrite-parts-of-the-configuration-in-x"></a><span data-ttu-id="c57c0-246">Endurskrifa hluta skilgreiningarinnar í X++</span><span class="sxs-lookup"><span data-stu-id="c57c0-246">Rewrite parts of the configuration in X++</span></span>

<span data-ttu-id="c57c0-247">Rafræn skýrslugerð styður aðferðir til að kalla á töflur og klasa, þ.m.t. viðbætur.</span><span class="sxs-lookup"><span data-stu-id="c57c0-247">ER supports calling methods of tables and classes, including extensions.</span></span> <span data-ttu-id="c57c0-248">Íhugið að endurskrifa hluta líkanavörpunarinnar í X++ til að auka afköstin.</span><span class="sxs-lookup"><span data-stu-id="c57c0-248">Consider rewriting parts of the model mapping in X++ to help improve performance.</span></span>

<span data-ttu-id="c57c0-249">Rafræn skýrslugerð getur notað gögn frá eftirfarandi upprunum:</span><span class="sxs-lookup"><span data-stu-id="c57c0-249">ER can consume data from the following sources:</span></span>

- <span data-ttu-id="c57c0-250">Klösum (**hlutar** og **klasa** gagnagjöfum)</span><span class="sxs-lookup"><span data-stu-id="c57c0-250">Classes (**object** and **class** data sources)</span></span>
- <span data-ttu-id="c57c0-251">Töflum (**töflu** og **töflufærslna** gagnagjöfum)</span><span class="sxs-lookup"><span data-stu-id="c57c0-251">Tables (**table** and **table records** data sources)</span></span>

<span data-ttu-id="c57c0-252">[API rafrænnar skýrslugerðar](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) býður einnig upp á leið til að senda fyrirframreiknuð gögn úr köllunarkóðanum.</span><span class="sxs-lookup"><span data-stu-id="c57c0-252">The [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) also provides a way to send precalculated data from the calling code.</span></span> <span data-ttu-id="c57c0-253">Forritapakkinn inniheldur fjölmörg dæmi um þessa nálgun.</span><span class="sxs-lookup"><span data-stu-id="c57c0-253">The application suite contains numerous examples of this approach.</span></span>
