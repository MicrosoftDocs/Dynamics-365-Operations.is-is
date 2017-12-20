---
title: Endurstilla gagnaskemma Financial reporting
description: "Þetta efnisatriði lýsir hvernig á að endurstilla gagnaskemma Financial reporting"
author: aolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 0786d3377b914791106ef30455d676e5ab2ae03d
ms.openlocfilehash: c708fa18b8676d8ff57c26b3176a36d86df29387
ms.contentlocale: is-is
ms.lasthandoff: 12/07/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="e6610-103">Endurstilla gagnaskemma Financial reporting</span><span class="sxs-lookup"><span data-stu-id="e6610-103">Reset the Financial reporting data mart</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e6610-104">Þetta efnisatriði útskýrir hvernig á að endurstilla gagnaskemma Financial reporting fyrir eftirfarandi útgáfur:</span><span class="sxs-lookup"><span data-stu-id="e6610-104">This topic explains how to reset the Financial reporting data mart for the following versions:</span></span>

- <span data-ttu-id="e6610-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting útgáfa 7.2.6.0 og síðar</span><span class="sxs-lookup"><span data-stu-id="e6610-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>
- <span data-ttu-id="e6610-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting útgáfa 7.0.10000.4 og síðar</span><span class="sxs-lookup"><span data-stu-id="e6610-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>
- <span data-ttu-id="e6610-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (staðbundin útgáfa)</span><span class="sxs-lookup"><span data-stu-id="e6610-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)</span></span>

<span data-ttu-id="e6610-108">Til að fá Finance and Operations Financial reporting útgáfu 7.2.6.0, geturðu halað niður KB 4052514 frá <https://support.microsoft.com/en-us/help/4052514>.</span><span class="sxs-lookup"><span data-stu-id="e6610-108">To get Finance and Operations Financial reporting release 7.2.6.0, you can download KB 4052514 from <https://support.microsoft.com/en-us/help/4052514>.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a><span data-ttu-id="e6610-109">Endurstilla Financial reporting gagnaskemma fyrir Finance and Operations Financial reporting útgáfa 7.2.6.0 og síðar</span><span class="sxs-lookup"><span data-stu-id="e6610-109">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="e6610-110">Endurstilla gagnaskemma Financial reporting frá Report hönnuði</span><span class="sxs-lookup"><span data-stu-id="e6610-110">Reset the Financial reporting data mart from Report designer</span></span>

> [!NOTE]
> <span data-ttu-id="e6610-111">Skrefin í þessu ferli eru studd fyrir Finance and Operations Financial reporting útgáfa 7.2.6.0. og síðar.</span><span class="sxs-lookup"><span data-stu-id="e6610-111">The steps in this process are supported for Finance and Operations Financial reporting release 7.2.6.0 and later.</span></span> <span data-ttu-id="e6610-112">Ef þú er með eldri útgáfu skaltu hafa samband við þjónustuver okkar til að fá aðstoð.</span><span class="sxs-lookup"><span data-stu-id="e6610-112">If you have an earlier release, contact the Support team for assistance.</span></span>

<span data-ttu-id="e6610-113">Í ákveðnum aðstæðum gætirðu þurft að endurstilla gagnaskemmuna fyrir Financial reporting.</span><span class="sxs-lookup"><span data-stu-id="e6610-113">In specific scenarios, you might have to reset the data mart for Financial reporting.</span></span> <span data-ttu-id="e6610-114">Þú getur lokið þessu verki í Report hönnuður biðlara.</span><span class="sxs-lookup"><span data-stu-id="e6610-114">You can complete this task in the Report designer client.</span></span> <span data-ttu-id="e6610-115">Hér eru nokkur dæmi þar sem þú gætir þurft að endurstilla gagnaskemmuna:</span><span class="sxs-lookup"><span data-stu-id="e6610-115">Here are some scenarios where you might have to reset the data mart:</span></span>

- <span data-ttu-id="e6610-116">Finance and Operations gagnagrunnurinn var endurheimtur, en gagnaskemma gagnasafnið var ekki endurreist.</span><span class="sxs-lookup"><span data-stu-id="e6610-116">The Finance and Operations database was restored, but the data mart database wasn't restored.</span></span>
- <span data-ttu-id="e6610-117">Þú sérð röng gögn fyrir tímabil.</span><span class="sxs-lookup"><span data-stu-id="e6610-117">You see incorrect data for a period.</span></span>
- <span data-ttu-id="e6610-118">Notendaþjónusta leiðbeinir þér við að endurstilla gagnaskemmuna sem hluti af skrefi úrræðaleitar.</span><span class="sxs-lookup"><span data-stu-id="e6610-118">Support instructs you to reset the data mart as part of a troubleshooting step.</span></span>

<span data-ttu-id="e6610-119">Endurstilling gagnaskemmu ætti aðeins að vera framkvæmd á tímum þegar vinnslumagn í gagnagrunninum er lítið.</span><span class="sxs-lookup"><span data-stu-id="e6610-119">The data mart reset should be done only during times when the amount of processing on the database is small.</span></span> <span data-ttu-id="e6610-120">Financial reporting verður ótiltækt á meðan endurstillingarferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="e6610-120">Financial reporting will be unavailable during the reset process.</span></span>

#### <a name="reset-the-data-mart"></a><span data-ttu-id="e6610-121">Endurstillið gagnaskemmuna:</span><span class="sxs-lookup"><span data-stu-id="e6610-121">Reset the data mart</span></span>

<span data-ttu-id="e6610-122">Til að endurstilla gagnaskemmuna skal á valmyndinni **verkfæri** velja **Endurstilla gagnaskemmu**.</span><span class="sxs-lookup"><span data-stu-id="e6610-122">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart**.</span></span> <span data-ttu-id="e6610-123">Svarglugginn sem birtist inniheldur tvo hluta: **Talnagögn** og **Endurstilla**.</span><span class="sxs-lookup"><span data-stu-id="e6610-123">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="e6610-124">[![Endurstilla gagnaskemma svargluggi](./media/Statistics.png)](./media/Statistics.png)</span><span class="sxs-lookup"><span data-stu-id="e6610-124">[![Reset Data Mart dialog box](./media/Statistics.png)](./media/Statistics.png)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="e6610-125">Samþættingartilraunir</span><span class="sxs-lookup"><span data-stu-id="e6610-125">Integration attempts</span></span>

<span data-ttu-id="e6610-126">**Samþættingartilraunir** hnitanetið sýnir hversu oft kerfið hefur reynt að samþætta færslur.</span><span class="sxs-lookup"><span data-stu-id="e6610-126">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="e6610-127">Kerfið heldur áfram að reyna að samþætta gögn yfir nokkurra daga tímabil ef fyrstu tilraunirnar mistekst.</span><span class="sxs-lookup"><span data-stu-id="e6610-127">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="e6610-128">Þú munt vita að gagnaskemmu verður að endurstilla ef fjöldi tilrauna er 8 eða meira, og ef það eru margar víddarsamsetningar eða færsluskrár.</span><span class="sxs-lookup"><span data-stu-id="e6610-128">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="e6610-129">Við þessar aðstæður verður ekki tilkynnt um gögnin.</span><span class="sxs-lookup"><span data-stu-id="e6610-129">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="e6610-130">Gagnastaða</span><span class="sxs-lookup"><span data-stu-id="e6610-130">Data status</span></span>

<span data-ttu-id="e6610-131">**Gagnastaða** hnitanet veitir skyndimynd af færslum, gengi og víddargildum í gagnaskemmunni.</span><span class="sxs-lookup"><span data-stu-id="e6610-131">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="e6610-132">Mikill fjöldi útrunninna skráa gefur til kynna að fjölmargir uppfærslur á skrám hafi átt sér stað.</span><span class="sxs-lookup"><span data-stu-id="e6610-132">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="e6610-133">Þetta ástand gæti valdið hægari myndunartíma skráa.</span><span class="sxs-lookup"><span data-stu-id="e6610-133">This situation might cause slower report generation times.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="e6610-134">Vitlaus röðun aðallyklaflokka</span><span class="sxs-lookup"><span data-stu-id="e6610-134">Misaligned main account categories</span></span>

<span data-ttu-id="e6610-135">Ef þú ert að nota eldri útgáfu en Microsoft Dynamics 365 for Finance and Operations Financial reporting útgáfa 7.2.1, gætir þú þurft að endurstilla gagnaskemmuna ef þú endurnefnir reikninga og færir reikninga á milli reikningsflokka.</span><span class="sxs-lookup"><span data-stu-id="e6610-135">If you're using a release that is earlier than Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="e6610-136">Þessar aðgerðir geta valdið því að flokkar aðalreikningsins verða ósamstilltir.</span><span class="sxs-lookup"><span data-stu-id="e6610-136">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="e6610-137">**Ósamstilltir flokkar aðalreiknings** reiturinn sýnir hvort þú átt við þetta vandamál að stríða.</span><span class="sxs-lookup"><span data-stu-id="e6610-137">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a><span data-ttu-id="e6610-138">Endurstilla gagnaskemmuna í Finance and Operations Financial reporting útgáfa 7.2.6.0</span><span class="sxs-lookup"><span data-stu-id="e6610-138">Reset the data mart in Finance and Operations Financial reporting release 7.2.6.0</span></span>

<span data-ttu-id="e6610-139">Til að endurstilla gagnaskemmuna í Finance and Operations Financial reporting útgáfa 7.2.6.0 og eldri, í svarglugganum **Endurstilla gagnaskemmu**, veldu gátreitinn **Endurstilla gagnaskemmu** og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e6610-139">To reset the data mart in Finance and Operations Financial reporting release 7.2.6.0 and earlier, in the **Reset Data Mart** dialog box, select the **Reset data mart** check box, and then select **OK**.</span></span> <span data-ttu-id="e6610-140">Þú ættir að endurstilla gagnaskemmu aðeins á áætluðum niðurtíma.</span><span class="sxs-lookup"><span data-stu-id="e6610-140">You should reset the data mart only during scheduled downtime.</span></span>

<span data-ttu-id="e6610-141">[![Endurstilla gagnaskemma gátreitur](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="e6610-141">[![Reset data mart check box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a><span data-ttu-id="e6610-142">Endurstilla gagnaskemmuna og velja ástæðu í Microsoft Dynamics 365 for Finance and Operations Financial reporting útgáfa 7.3.0</span><span class="sxs-lookup"><span data-stu-id="e6610-142">Reset the data mart and select a reason in Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.3.0</span></span>

<span data-ttu-id="e6610-143">Ef þú ákveður að þörf sé á að endurstilla gagnaskemmuna skaltu velja gátreitinn **Endurstilla gagnaskemmu** og veldu síðan ástæðu í **Ástæða** reitnum.</span><span class="sxs-lookup"><span data-stu-id="e6610-143">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="e6610-144">Eftirtaldir valkostir eru í boði:</span><span class="sxs-lookup"><span data-stu-id="e6610-144">The following options are available:</span></span>

- <span data-ttu-id="e6610-145">**Týnd eða röng gögn** - Á grundvelli tölfræðinnar hefur þú ákveðið að gögn gæti vantað.</span><span class="sxs-lookup"><span data-stu-id="e6610-145">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="e6610-146">Áður en þú heldur áfram mælum við með því að þú vinnur með notendaþjónustu til að ákvarða hver grunnorsökin er.</span><span class="sxs-lookup"><span data-stu-id="e6610-146">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="e6610-147">**Endurheimta gagnagrunn** - Finance and Operations gagnagrunnurinn var endurheimtur, en gagnagrunnurinn fyrir Financial reporting gagnaskemmuna var ekki endurreist.</span><span class="sxs-lookup"><span data-stu-id="e6610-147">**Restore database** – The Finance and Operations database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="e6610-148">**Annað** - Þú ert að endurstilla gagnaskemmuna af öðrum ástæðum.</span><span class="sxs-lookup"><span data-stu-id="e6610-148">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="e6610-149">Ef þú hefur áhyggjur af því að upp sé komið vandamál skaltu hafa samband við notendaþjónustu til að bera kennsl á það.</span><span class="sxs-lookup"><span data-stu-id="e6610-149">If you're concerned that there is an issue, contact Support to identify it.</span></span>

> [!NOTE]
> <span data-ttu-id="e6610-150">Staðfestu að samþætting allra fyrirliggjandi verka sé lokið áður en þú lýkur við skrefin.</span><span class="sxs-lookup"><span data-stu-id="e6610-150">Verify that all existing tasks have finished integrating before you complete the steps.</span></span> <span data-ttu-id="e6610-151">Hægt er að skoða stöðu samþættingar með því að velja **Verkfæri** &gt; **Staða samþættingar**.</span><span class="sxs-lookup"><span data-stu-id="e6610-151">You can view the status of the integration by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="e6610-152">Hreinsa notendur og fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="e6610-152">Clear users and companies</span></span>

<span data-ttu-id="e6610-153">Veldu **hreinsa notendur og fyrirtæki** í gátreitnum ef þú hefur endurheimt gagnagrunninn þinn, en gerðir síðan breytingar á notendum eða fyrirtækjum.</span><span class="sxs-lookup"><span data-stu-id="e6610-153">Select the **Clear users and companies** check box if you restored your database, but you then made changes to users or companies.</span></span> <span data-ttu-id="e6610-154">Þú ættir sjaldan að þurfa að velja þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="e6610-154">You should rarely have to select this check box.</span></span>

<span data-ttu-id="e6610-155">Þegar þú ert tilbúinn til að hefja endurstillingarferlið skaltu velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e6610-155">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="e6610-156">Þú ert beðinn um að staðfesta að þú sért tilbúinn til að hefja ferlið.</span><span class="sxs-lookup"><span data-stu-id="e6610-156">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="e6610-157">Athugaðu að Financial reporting verður ekki tiltækt á meðan endurstilling fer fram og fyrsta gagnasamþætting, sem á sér stað eftir endurstillinguna.</span><span class="sxs-lookup"><span data-stu-id="e6610-157">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="e6610-158">Ef þú vilt skoða stöðu samþættingarinnar skaltu velja **Verkfæri** &gt; **Staða samþættingar** til að sjá síðustu skipti sem samþættingin var keyrð og stöðuna.</span><span class="sxs-lookup"><span data-stu-id="e6610-158">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="e6610-159">[![Skoða stöðu samþættingar](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="e6610-159">[![View the status of the integration](./media/Integration.png)](./media/Integration.png)</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a><span data-ttu-id="e6610-160">Endrustilla Financial reporting gagnaskemmu fyrir Finance and Operations Financial reporting útgáfa 7.0.10000.4 og síðar</span><span class="sxs-lookup"><span data-stu-id="e6610-160">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>

<span data-ttu-id="e6610-161">Ef þú einhvern tímann endurheimtir Finance and Operations gagnagrunninn úr öryggisafritum eða afritar gagnagrunninn úr öðru umhverfi, er nauðsynlegt að fylgja skrefunum í þessu efnisatriði til að tryggja að gagnaskemma Financial reporting sé að nota endurheimtan gagnagrunn Finance and Operations á réttan hátt.</span><span class="sxs-lookup"><span data-stu-id="e6610-161">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored Finance and Operations database.</span></span>

> [!NOTE]
> <span data-ttu-id="e6610-162">Skrefin í þessu ferli eru studd fyrir Microsoft Dynamics AX forrit útgáfa 7.0.1 (maí 2016) (forrit smíð 7.0.1265.23014 og Financial reporting smíð 7.0.10000.4) og síðar.</span><span class="sxs-lookup"><span data-stu-id="e6610-162">The steps in this process are supported for Microsoft Dynamics AX application version 7.0.1 (May 2016) (application build 7.0.1265.23014 and Financial reporting build 7.0.10000.4) and later.</span></span> <span data-ttu-id="e6610-163">Ef þú er með eldri útgáfu af Finance and Operations skaltu hafa samband við þjónustuver okkar til að fá aðstoð.</span><span class="sxs-lookup"><span data-stu-id="e6610-163">If you have an earlier version of Finance and Operations, contact Support for assistance.</span></span>

### <a name="export-report-definitions"></a><span data-ttu-id="e6610-164">Flytja út skilgreiningu á skýrslum</span><span class="sxs-lookup"><span data-stu-id="e6610-164">Export report definitions</span></span>

<span data-ttu-id="e6610-165">Fyrst skaltu fylgja þessum skrefum til að flytja út skýrsluhönnunina frá Report hönnuði.</span><span class="sxs-lookup"><span data-stu-id="e6610-165">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="e6610-166">Í Report hönnuður velurðu **Fyrirtæki** &gt; **Einingahópar**.</span><span class="sxs-lookup"><span data-stu-id="e6610-166">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="e6610-167">Veldu einingahópinn sem á að flytja út og síðan er smellt á **Flytja út**.</span><span class="sxs-lookup"><span data-stu-id="e6610-167">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e6610-168">Í Finance and Operations er aðeins einn einingahópur studdur, **Sjálfgefið**.</span><span class="sxs-lookup"><span data-stu-id="e6610-168">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="e6610-169">Veldu skýrsluskilgreiningar til að flytja út:</span><span class="sxs-lookup"><span data-stu-id="e6610-169">Select the report definitions to export:</span></span>

    - <span data-ttu-id="e6610-170">Til að flytja út allar skýrsluskilgreiningar og tengdar einingar er smellt á **Velja allt**.</span><span class="sxs-lookup"><span data-stu-id="e6610-170">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="e6610-171">Til að flytja út tilteknar skýrslur, línur, dálka, skipurit eða víddasamstæður er smellt á viðeigandi flipa og svo valin atriði til að flytja út.</span><span class="sxs-lookup"><span data-stu-id="e6610-171">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="e6610-172">Ýttu á og haltu niðri Ctrl lyklinum til að mörg atriði á flipa. Þegar valdar eru skýrslur til að flytja út eru valdar tengdar línur, dálkar, skipurit og víddasamstæður.</span><span class="sxs-lookup"><span data-stu-id="e6610-172">Press and hold the Ctrl key to select multiple items on a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4. <span data-ttu-id="e6610-173">Velja **Flytja út**.</span><span class="sxs-lookup"><span data-stu-id="e6610-173">Select **Export**.</span></span>
5. <span data-ttu-id="e6610-174">Færið inn skráarnafn og veljið örugga staðsetningu þar sem á að vista útfluttar skýrsluskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="e6610-174">Enter a file name, and select a secure location where you want to save the exported report definitions.</span></span>
6. <span data-ttu-id="e6610-175">Veldu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e6610-175">Select **Save**.</span></span>

<span data-ttu-id="e6610-176">Þú getur afritað eða hlaðið inn skrána á öruggan stað.</span><span class="sxs-lookup"><span data-stu-id="e6610-176">You can copy or upload the file to a secure location.</span></span> <span data-ttu-id="e6610-177">Þannig má flytja skrána inn í annað umhverfi seinna.</span><span class="sxs-lookup"><span data-stu-id="e6610-177">In this way, the file can be imported into a different environment later.</span></span> <span data-ttu-id="e6610-178">Upplýsingar um notkun í geymslulykils Microsoft Azure, sjá [Flytja gögn með AzCopy Skipun-Lína hjálparforriti](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="e6610-178">For information about how to use a Microsoft Azure storage account, see [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="e6610-179">Microsoft veitir ekki geymslulykil sem hluta af samningi þínum um Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e6610-179">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="e6610-180">Annaðhvort verður að kaupa geymslulykil eða nota geymslulykil úr aðskilinni Azure-áskrift.</span><span class="sxs-lookup"><span data-stu-id="e6610-180">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!WARNING]
> <span data-ttu-id="e6610-181">Huga skal að hegðun D-drifs á sýndarvélum (VM) Azure.</span><span class="sxs-lookup"><span data-stu-id="e6610-181">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="e6610-182">Ekki vista útflutta einingahópa þína til langframa á D-drifi. Sjá frekari upplýsingar um tímabundin drif á [Skilningur á tímabundnum drifum í sýndarvélum Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="e6610-182">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="stop-services"></a><span data-ttu-id="e6610-183">Stöðvunarþjónusta</span><span class="sxs-lookup"><span data-stu-id="e6610-183">Stop services</span></span>

<span data-ttu-id="e6610-184">Eftirfarandi Microsoft Windows þjónustur munu hafa opnar tengingar við gagnagrunn Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e6610-184">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="e6610-185">Þar af leiðandi þarftu að nota Microsoft Remote Desktop til að tengjast öllum tölvum í umhverfinu og síðan að stöðva þessa þjónustu með því að nota services.msc.</span><span class="sxs-lookup"><span data-stu-id="e6610-185">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="e6610-186">Birtingarþjónusta á vefnum (á öllum AOS tölvum)</span><span class="sxs-lookup"><span data-stu-id="e6610-186">World wide web publishing service (on all Application Object Servers [AOS] computers)</span></span>
- <span data-ttu-id="e6610-187">Runustjórnunarþjónusta Finance and Operations (aðeins í AOS-tölvum sem ekki eru einkatölvur)</span><span class="sxs-lookup"><span data-stu-id="e6610-187">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="e6610-188">Ferlaþjónusta Management Reporter 2012 (aðeins á BI tölvum)</span><span class="sxs-lookup"><span data-stu-id="e6610-188">Management Reporter 2012 Process Service (on Business intelligence [BI] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="e6610-189">Endurstilla</span><span class="sxs-lookup"><span data-stu-id="e6610-189">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="e6610-190">Hlaða niður nýjasta MinorVersionDataUpgrade.zip pakkanum</span><span class="sxs-lookup"><span data-stu-id="e6610-190">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="e6610-191">Hlaða niður nýjasta MinorVersionDataUpgrade.zip pakkanum.</span><span class="sxs-lookup"><span data-stu-id="e6610-191">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="e6610-192">Fyrir leiðbeiningar um hvernig skal finna og hlaða niður réttu útgáfunni af gagnauppfærslupakkanum, sjá[Hlaða niður nýjustu útgáfu af virkjanlegum gagnauppfærslupakka](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span><span class="sxs-lookup"><span data-stu-id="e6610-192">For instructions about how to find and download the correct version of the data upgrade package, see the[Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="e6610-193">Uppfærslu er ekki krafist til að hægt sé að hlaða niður MinorVersionDataUpgrade.zip pakkanum.</span><span class="sxs-lookup"><span data-stu-id="e6610-193">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="e6610-194">Þess vegna þarftu bara að fylgja skrefunum í „Afrita nýjustu útgáfu af virkjanlegum gagnauppfærslupakka“ hlutanum í því efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="e6610-194">Therefore, you just have follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="e6610-195">Þú getur sleppt öllum öðrum skrefum í efnisatriðinu.</span><span class="sxs-lookup"><span data-stu-id="e6610-195">You can skip all the other steps in the topic.</span></span>

#### <a name="run-scripts-against-the-finance-and-operations-database"></a><span data-ttu-id="e6610-196">Keyra forskriftir gagnvart gagnagrunni Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e6610-196">Run scripts against the Finance and Operations database</span></span>

<span data-ttu-id="e6610-197">Keyra eftirfarandi forskriftir gagnvart gagnagrunni Finance and Operations (ekki gagnvart gagnagrunni Financial reporting):</span><span class="sxs-lookup"><span data-stu-id="e6610-197">Run the following scripts against the Finance and Operations database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="e6610-198">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="e6610-198">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="e6610-199">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="e6610-199">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="e6610-200">Þessar forskriftir tryggja að notendur, hlutverk og stillingar á breytingarakningu séu réttar.</span><span class="sxs-lookup"><span data-stu-id="e6610-200">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a><span data-ttu-id="e6610-201">Keyra Windows PowerShell-skipun til að endurstilla gagnagrunninn</span><span class="sxs-lookup"><span data-stu-id="e6610-201">Run a Windows PowerShell command to reset the database</span></span>

<span data-ttu-id="e6610-202">Á AOS-tölvunni skal opna Microsoft Windows PowerShell sem stjórnanda, og keyra eftirfarandi skipanir til að endurstilla samþættingu milli Finance and Operations og Financial reporting.</span><span class="sxs-lookup"><span data-stu-id="e6610-202">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between Finance and Operations and Financial reporting.</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

<span data-ttu-id="e6610-203">Hér er skýring á færibreytunum í **Endurstilla-DatamartIntegration** skipuninni:</span><span class="sxs-lookup"><span data-stu-id="e6610-203">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="e6610-204">Gildu gildin fyrir **-Reason** eru **SERVICING**, **BADDATA**, og **OTHER**.</span><span class="sxs-lookup"><span data-stu-id="e6610-204">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="e6610-205">**-ReasonDetail** færibreytan er fyrir valkvæman texta.</span><span class="sxs-lookup"><span data-stu-id="e6610-205">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="e6610-206">Reason og reason detail verða skráð í eftirlit fjarmælingu/umhverfis.</span><span class="sxs-lookup"><span data-stu-id="e6610-206">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="e6610-207">Eftir keyrslu skipananna verður beðið um að fært sé inn **Y** til að staðfesta að þú viljir endurstilla gagnagrunninn.</span><span class="sxs-lookup"><span data-stu-id="e6610-207">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="e6610-208">Endurræsi þjónustu</span><span class="sxs-lookup"><span data-stu-id="e6610-208">Restart services</span></span>

<span data-ttu-id="e6610-209">Nota services.msc að endurræsa þjónustuna sem þú hættir áður:</span><span class="sxs-lookup"><span data-stu-id="e6610-209">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="e6610-210">Birtingarþjónusta á vefnum (á allar AOS tölvur)</span><span class="sxs-lookup"><span data-stu-id="e6610-210">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="e6610-211">Runustjórnunarþjónusta Finance and Operations (aðeins í AOS-tölvum sem ekki eru einkatölvur)</span><span class="sxs-lookup"><span data-stu-id="e6610-211">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="e6610-212">Ferlaþjónusta Management Reporter 2012 (aðeins á BI tölvum)</span><span class="sxs-lookup"><span data-stu-id="e6610-212">Management Reporter 2012 Process Service (on BI computers only)</span></span>

#### <a name="import-report-definitions"></a><span data-ttu-id="e6610-213">Flytja inn skýrsluskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="e6610-213">Import report definitions</span></span>

<span data-ttu-id="e6610-214">Flytja inn skýrsluhönnun notanda úr Report hönnuðinum með skránni sem var búin til við útflutninginn.</span><span class="sxs-lookup"><span data-stu-id="e6610-214">Import your report designs from Report designer by using the file that was created during the export.</span></span>

1. <span data-ttu-id="e6610-215">Í Report hönnuður velurðu **Fyrirtæki** &gt; **Einingahópar**.</span><span class="sxs-lookup"><span data-stu-id="e6610-215">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="e6610-216">Veldu einingahópinn sem á að flytja út og síðan er smellt á **Flytja út**.</span><span class="sxs-lookup"><span data-stu-id="e6610-216">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e6610-217">Í Finance and Operations er aðeins einn einingahópur studdur, **Sjálfgefið**.</span><span class="sxs-lookup"><span data-stu-id="e6610-217">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="e6610-218">Veldu eininguna **Sjálfgefið** og smelltu á **Innflutning**.</span><span class="sxs-lookup"><span data-stu-id="e6610-218">Select the **Default** building block, and then select **Import**.</span></span>
4. <span data-ttu-id="e6610-219">Veldu skrána með útfluttum skýrsluskilgreiningum og smelltu á **Opna**.</span><span class="sxs-lookup"><span data-stu-id="e6610-219">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
5. <span data-ttu-id="e6610-220">Smellið á skýrsluskilgreiningarnar í svarglugganum **Flytja inn** til að flytja inn:</span><span class="sxs-lookup"><span data-stu-id="e6610-220">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="e6610-221">Til að flytja inn allar skýrsluskilgreiningar og tengdar einingar er smellt á **Velja allt**.</span><span class="sxs-lookup"><span data-stu-id="e6610-221">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="e6610-222">Til að flytja inn tilteknar skýrslur, línur, dálka, skipurit eða víddasamstæður skal velja skýrslur, línur, dálka, skipurit eða víddasamstæður sem á að flytja inn.</span><span class="sxs-lookup"><span data-stu-id="e6610-222">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6. <span data-ttu-id="e6610-223">Velja **Innflutningur**.</span><span class="sxs-lookup"><span data-stu-id="e6610-223">Select **Import**.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a><span data-ttu-id="e6610-224">Endurstilla Financial reporting gagnaskemmu fyrir Finance and Operations Financial (staðbundin útgáfa)</span><span class="sxs-lookup"><span data-stu-id="e6610-224">Reset the Financial reporting data mart for Finance and Operations (on-premises)</span></span>

1. <span data-ttu-id="e6610-225">Fyrirskipa öllum notendum að fara út úr Report hönnuður og Financial reporting svæði Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e6610-225">Instruct all users to exit Report designer and the Financial reporting area of Finance and Operations.</span></span>
2. <span data-ttu-id="e6610-226">Keyra eftirfarandi forskriftir gagnvart gagnagrunni Finance and Operations (MRDB).</span><span class="sxs-lookup"><span data-stu-id="e6610-226">Run the following script against the Financial reporting database (MRDB).</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. <span data-ttu-id="e6610-227">Stýfa eða eyða öllum skrám úr FINANCIALREPORTS töflunni í Finance and Operations gagnagrunninum (AXDB).</span><span class="sxs-lookup"><span data-stu-id="e6610-227">Truncate or delete all records from the FINANCIALREPORTS table in the Finance and Operations database (AXDB).</span></span>
4. <span data-ttu-id="e6610-228">Stýfa eða eyða öllum skrám úr FINANCIALREPORTVERSION töflunni, ef þessi tafla er til staðar í gagnagrunni Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e6610-228">Truncate or delete all records from the FINANCIALREPORTVERSION table, if this table exists in the Finance and Operations database.</span></span> <span data-ttu-id="e6610-229">Ef taflan er ekki til í gagnagrunni Finance and Operations, skal sleppa þessu skrefi.</span><span class="sxs-lookup"><span data-stu-id="e6610-229">If the table doesn't exist in the Finance and Operations database, skip this step.</span></span>
5. <span data-ttu-id="e6610-230">Keyra forskriftina **ResetDatamart.sql** gagnvart gagnagrunni Financial reporting.</span><span class="sxs-lookup"><span data-stu-id="e6610-230">Run the **ResetDatamart.sql** script against the Financial reporting database.</span></span> <span data-ttu-id="e6610-231">Þessi forskrift gerir óvirka samþættingu gagnaskemmu, eyðir öllum gögnum gagnaskemmu, og endurvirkjar svo samþættingu gagnaskemmu.</span><span class="sxs-lookup"><span data-stu-id="e6610-231">This script disables the data mart integration, deletes all the data mart data, and then reenables the data mart integration.</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. <span data-ttu-id="e6610-232">Eftir endurstillinguna geturðu staðfest gagnaendurhleðsluna handvirkt með því að keyra eftirfarandi fyrirspurn gagnvart gagnagrunni Financial reporting.</span><span class="sxs-lookup"><span data-stu-id="e6610-232">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    <span data-ttu-id="e6610-233">Staðfestu að allar raðirnar hafi **LastRunTime** gildi, og að **StateType** sé stillt á **5**.</span><span class="sxs-lookup"><span data-stu-id="e6610-233">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="e6610-234">**StateType** gildi upp á **5** gefur til kynna að endurhleðsla gagna hafið heppnast.</span><span class="sxs-lookup"><span data-stu-id="e6610-234">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="e6610-235">Gildið **7** tilgreinir villu í stöðu.</span><span class="sxs-lookup"><span data-stu-id="e6610-235">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="e6610-236">Stundum hefur Stigveldi fyrirtækis kortið þessa stöðu í fyrsta skipti sem það keyrir.</span><span class="sxs-lookup"><span data-stu-id="e6610-236">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="e6610-237">Hins vegar á villustaða að leysast sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="e6610-237">However, the faulted state but should be automatically resolved.</span></span>

