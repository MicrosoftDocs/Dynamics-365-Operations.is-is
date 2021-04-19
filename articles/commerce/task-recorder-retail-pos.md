---
title: Verkskráning og hjálp fyrir Retail Modern POS (MPOS) og sölukerfi í skýinu
description: Þetta efnisatriði lýsir hvernig á að nota verkskráningu í Retail Modern POS og Cloud POS.
author: mugunthanm
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d4bb8ce1abc07bc57e90e893e7e327761131d52a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795214"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="5d60a-103">Verkskráning og hjálp fyrir Retail Modern POS (MPOS) og sölukerfi í skýinu</span><span class="sxs-lookup"><span data-stu-id="5d60a-103">Task recorder and Help for Retail Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5d60a-104">Þetta efnisatriði lýsir hvernig á að nota verkskráningu í Retail Modern POS og Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="5d60a-104">This topic describes how to use Task recorder in Retail Modern POS and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="5d60a-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="5d60a-105">Overview</span></span>

<span data-ttu-id="5d60a-106">Verkskráning í Retail Modern POS eða Cloud POS er ný lausn sem var þróuð með áherslu á mikla viðbragðsflýti.</span><span class="sxs-lookup"><span data-stu-id="5d60a-106">Task recorder in Retail Modern POS or Cloud POS is a new solution that was built with a focus on high responsiveness.</span></span> <span data-ttu-id="5d60a-107">Hún býður upp á sveigjanleg forritaskil (API) sem eykur þenslugetu og auðveldar snurðulausa samþættingu við neytendur skráninga verkferla.</span><span class="sxs-lookup"><span data-stu-id="5d60a-107">It provides a flexible application programming interface (API) for extensibility and seamless integration with consumers of business process recordings.</span></span> <span data-ttu-id="5d60a-108">Að auki hefur samþætting verkskráningar við viðskiptaferlavinnslutólið (BPM) í Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) verið þróað áfram.</span><span class="sxs-lookup"><span data-stu-id="5d60a-108">Additionally, Task recorder integration with the Business process modeler (BPM) tool on Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) has been brought forward.</span></span> <span data-ttu-id="5d60a-109">Notendur geta því haldið áfram að búa til efnismiklar skýringarmyndir verkferla úr skráningum til að greina og þróa forrit sín.</span><span class="sxs-lookup"><span data-stu-id="5d60a-109">Therefore, users can continue to produce rich business process diagrams from recordings to analyze and design their applications.</span></span>

## <a name="architecture"></a><span data-ttu-id="5d60a-110">Högun</span><span class="sxs-lookup"><span data-stu-id="5d60a-110">Architecture</span></span>

<span data-ttu-id="5d60a-111">Verkskráning getur skráð aðgerðir notanda í biðlara af mikilli nákvæmni.</span><span class="sxs-lookup"><span data-stu-id="5d60a-111">Task recorder can record user actions in the client with exact fidelity.</span></span> <span data-ttu-id="5d60a-112">Hver stjórntakki er stilltur til að tilkynna verkskráningu um allar framkvæmdar aðgerðir notanda.</span><span class="sxs-lookup"><span data-stu-id="5d60a-112">Each control is instrumented to notify Task recorder about the execution of a user action.</span></span> <span data-ttu-id="5d60a-113">Stjórntakkinn tillkynnir verkskráningu að tilvik hafi átt sér stað og kemur til skila öllum veigamiklum upplýsingum um samsvarandi rauntímaaðgerð notanda.</span><span class="sxs-lookup"><span data-stu-id="5d60a-113">The control notifies Task recorder that an event occurred and passes along all pertinent information about the corresponding user action in real time.</span></span> <span data-ttu-id="5d60a-114">Þessar upplýsingar úr verkskráning geta safnað gerðum notandaaðgerða (svo sem smellum á hnappa, færslu gilda eða flettingum) og öllum gögnum sem tengjast notandaaðgerða (svo sem gildum og gerð innsláttargagna, samhengi skjámynda eða samhengi færslna).</span><span class="sxs-lookup"><span data-stu-id="5d60a-114">From this information, Task recorder can capture the type of user action (such as a button click, value entry, or navigation) and any data that is related to the user action (such as the input data value and type, form context, or record context).</span></span> <span data-ttu-id="5d60a-115">Verkskráning viðheldur upplýsingum af nægilegri nákvæmni til að tryggja að afspilun upptökunnar geti framkvæmt skráðar aðgerðir nákvæmlega eins og notandinn framkvæmdi þær.</span><span class="sxs-lookup"><span data-stu-id="5d60a-115">Task recorder persists the information with enough detail to help guarantee that a playback of the recording can perform the recorded actions exactly as the user performed them.</span></span> <span data-ttu-id="5d60a-116">(Afspilunareiginleikinn hefur ekki enn verið innleitt í Retail modern POS eða Cloud POS.)</span><span class="sxs-lookup"><span data-stu-id="5d60a-116">(The playback feature isn't yet implemented at Retail modern POS or Cloud POS.)</span></span>

## <a name="basic-configuration"></a><span data-ttu-id="5d60a-117">Einföld grunnstilling</span><span class="sxs-lookup"><span data-stu-id="5d60a-117">Basic configuration</span></span>

<span data-ttu-id="5d60a-118">Fylgið eftirfarandi skrefum til að virkja verkskráningu á sölustað:</span><span class="sxs-lookup"><span data-stu-id="5d60a-118">To enable task recording in POS, follow these steps.</span></span>

1. <span data-ttu-id="5d60a-119">Smella á **Retail og Commerce** &gt; **Uppsetning rásar** &gt; **Uppsetning smásölustaðar** &gt; **Afgreiðslukassar**.</span><span class="sxs-lookup"><span data-stu-id="5d60a-119">Click **Retail and Commerce** &gt; **Channel Setup** &gt; **POS Setup** &gt; **Registers**.</span></span>
2. <span data-ttu-id="5d60a-120">Smellið á afgreiðslukassa til að kveikja á verkskráningu.</span><span class="sxs-lookup"><span data-stu-id="5d60a-120">Click the register to enable task recording on.</span></span>
3. <span data-ttu-id="5d60a-121">Á flipanum **Afgreiðslukassi** á flýtiflipanum **Almennt** skal stilla valkostinn **Kveikja á verkskráningu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="5d60a-121">On the **Register** tab, on the **General** FastTab, set the **Enable task recording** option to **Yes**.</span></span>
4. <span data-ttu-id="5d60a-122">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5d60a-122">Click **Save**.</span></span>
5. <span data-ttu-id="5d60a-123">Farðu í **Retail og Commerce** &gt; **Upplýsingatækni í Retail og Commerce** &gt; **Dreifingaráætlun**.</span><span class="sxs-lookup"><span data-stu-id="5d60a-123">Go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedule**.</span></span>
6. <span data-ttu-id="5d60a-124">Veljið verkið **Afgreiðslukassar (1090)** og smellið svo á **keyra núna**.</span><span class="sxs-lookup"><span data-stu-id="5d60a-124">Select the **Registers (1090)** job, and then click **Run now**.</span></span>

## <a name="create-a-recording"></a><span data-ttu-id="5d60a-125">Stofna skráningu</span><span class="sxs-lookup"><span data-stu-id="5d60a-125">Create a recording</span></span>

<span data-ttu-id="5d60a-126">Fylgið þessum skrefum til að stofna nýja skráningu með því að nota Verkskráningu.</span><span class="sxs-lookup"><span data-stu-id="5d60a-126">Follow these steps to create a new recording using Task recorder.</span></span>

1. <span data-ttu-id="5d60a-127">Ræsa Retail Modern POS eða Cloud POS, og skrá inn.</span><span class="sxs-lookup"><span data-stu-id="5d60a-127">Start Retail Modern POS or Cloud POS, and sign in.</span></span>
2. <span data-ttu-id="5d60a-128">Á síðunni **Stillingar** í hlutanum **Verkskráning** er smellt á **Opna verkskráningu**.</span><span class="sxs-lookup"><span data-stu-id="5d60a-128">On the **Settings** page, in the **Task Recorder** section, click **Open task recorder**.</span></span> <span data-ttu-id="5d60a-129">Rúðan **Verkskráning** birtist.</span><span class="sxs-lookup"><span data-stu-id="5d60a-129">The **Task recorder** pane appears.</span></span> <span data-ttu-id="5d60a-130">Hægt er að smella á hnappinn **Loka** (**X**) í efra hægra horni til að loka rúðunni **Verkskráning** áður en byrjað er á nýrri skráningu.</span><span class="sxs-lookup"><span data-stu-id="5d60a-130">You can click the **Close** button (**X**) in the upper-right corner to close the **Task recorder** pane before you begin a new recording.</span></span> <span data-ttu-id="5d60a-131">Endurtakið skref 2 til að opna rúðuna aftur.</span><span class="sxs-lookup"><span data-stu-id="5d60a-131">To reopen the pane, repeat step 2.</span></span>

    <span data-ttu-id="5d60a-132">[![Rúðan Verkskráning birtist](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span><span class="sxs-lookup"><span data-stu-id="5d60a-132">[![Task recorder pane](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span></span>

3. <span data-ttu-id="5d60a-133">Sláið inn nafn og lýsingu fyrir skráninguna, og smellið á **Ræsa**.</span><span class="sxs-lookup"><span data-stu-id="5d60a-133">Enter a name and description for the recording, and then click **Start**.</span></span> <span data-ttu-id="5d60a-134">Skráningarlotan hefst um leið og smellt er á **Ræsa**.</span><span class="sxs-lookup"><span data-stu-id="5d60a-134">The recording session begins as soon as you click **Start**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5d60a-135">Ef smellt er á hnappinn **Loka** (**X**) í efra hægra horni á meðan skráning er í gangi er rúðunni fyrir **Verkskráningu** lokað en skráningarlotunni er ekki hætt.</span><span class="sxs-lookup"><span data-stu-id="5d60a-135">If you click the **Close** button (**X**) in the upper-right corner while recording is in progress, the **Task recorder** pane is closed, but the recording session isn't ended.</span></span> <span data-ttu-id="5d60a-136">Til að enduropna rúðuna fyrir verkskráningu skal smella á hnappinn **Hjálp** (spurningamerki) efst á skjánum.</span><span class="sxs-lookup"><span data-stu-id="5d60a-136">To reopen the Task recorder pane, click the **Help** button (question mark) at the top of the screen.</span></span>
    >
    > <span data-ttu-id="5d60a-137">[![Spurningarmerki](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="5d60a-137">[![Question mark](./media/help.jpg)](./media/help.jpg)</span></span>

4. <span data-ttu-id="5d60a-138">Eftir að smellt er á **Ræsa** fer Verkskráning í skráningarstillingu.</span><span class="sxs-lookup"><span data-stu-id="5d60a-138">After you click **Start**, Task recorder enters recording mode.</span></span> <span data-ttu-id="5d60a-139">Rúðan **Verkskráning** sýnir upplýsingar og stjórntakka sem tengjast skráningarferlinu.</span><span class="sxs-lookup"><span data-stu-id="5d60a-139">The **Task recorder** pane shows information and controls that are related to the recording process.</span></span>
5. <span data-ttu-id="5d60a-140">Framkvæmið aðgerðirnar sem á að framkvæma í notandaviðmóti (UI) Retail Modern POS eða Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="5d60a-140">Perform the actions that you want to perform in the Retail Modern POS or Cloud POS user interface (UI).</span></span>
6. <span data-ttu-id="5d60a-141">Smellið á **Stöðva** til að stöðva skráninguna.</span><span class="sxs-lookup"><span data-stu-id="5d60a-141">To end the recording session, click **Stop**.</span></span>

## <a name="download-options"></a><span data-ttu-id="5d60a-142">Niðurhalsvalkostir</span><span class="sxs-lookup"><span data-stu-id="5d60a-142">Download options</span></span>

<span data-ttu-id="5d60a-143">Þegar búið er að ljúka lotunni birtast nokkrir valkostir birtast til að hægt sé að hala niður skráningunni.</span><span class="sxs-lookup"><span data-stu-id="5d60a-143">After you end the recording session, several options are shown, so that you can download your recording.</span></span>

<span data-ttu-id="5d60a-144">[![Valkostir við niðurhal](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span><span class="sxs-lookup"><span data-stu-id="5d60a-144">[![Download options](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span></span>

### <a name="save-to-this-pc"></a><span data-ttu-id="5d60a-145">Vista í þessari tölvu</span><span class="sxs-lookup"><span data-stu-id="5d60a-145">Save to this PC</span></span>

<span data-ttu-id="5d60a-146">Verkskráningarpakkann er hægt að nota til að spila verkefnaleiðbeiningar, vinna með upptökuna eða breyta færslum upptökunnar.</span><span class="sxs-lookup"><span data-stu-id="5d60a-146">You can use the recording package to play a Task guide, maintain the recording, or edit the annotations in the recording.</span></span> <span data-ttu-id="5d60a-147">(Þessi eiginleiki er ekki enn innleiddur í Retail Modern POS og Cloud POS.)</span><span class="sxs-lookup"><span data-stu-id="5d60a-147">(This feature isn't yet implemented in Retail Modern POS and Cloud POS.)</span></span>

### <a name="export-as-word-document"></a><span data-ttu-id="5d60a-148">Flytja út sem Word-skjal</span><span class="sxs-lookup"><span data-stu-id="5d60a-148">Export as Word document</span></span>

<span data-ttu-id="5d60a-149">Hægt er að vista skráningu sem Microsoft Microsoft Word-skjal.</span><span class="sxs-lookup"><span data-stu-id="5d60a-149">You can save the recording as a Microsoft Word document.</span></span> <span data-ttu-id="5d60a-150">Skjalið inniheldur skráð skref og skjámyndirnar sem voru vistaðar.</span><span class="sxs-lookup"><span data-stu-id="5d60a-150">The document will contain the recorded steps and the screenshots that were captured.</span></span>

### <a name="save-as-developer-recording"></a><span data-ttu-id="5d60a-151">Vista sem skráningu þróunaraðila</span><span class="sxs-lookup"><span data-stu-id="5d60a-151">Save as developer recording</span></span>

<span data-ttu-id="5d60a-152">Óunnin upptökuskráin nýtist vel í þróunarsviðsmyndum, t.d. við myndun prófunarkóða.</span><span class="sxs-lookup"><span data-stu-id="5d60a-152">The raw recording file will be useful for developer scenarios such as test code generation.</span></span> <span data-ttu-id="5d60a-153">(Þessi eiginleiki er ekki enn innleiddur.)</span><span class="sxs-lookup"><span data-stu-id="5d60a-153">(This feature isn't yet implemented.)</span></span>

## <a name="recording-controls"></a><span data-ttu-id="5d60a-154">Stýringar verkskráningar</span><span class="sxs-lookup"><span data-stu-id="5d60a-154">Recording controls</span></span>

<span data-ttu-id="5d60a-155">[![Stýringar verkskráningar](./media/controls.jpg)](./media/controls.jpg)</span><span class="sxs-lookup"><span data-stu-id="5d60a-155">[![Recording controls](./media/controls.jpg)](./media/controls.jpg)</span></span>

### <a name="stop"></a><span data-ttu-id="5d60a-156">Stöðva</span><span class="sxs-lookup"><span data-stu-id="5d60a-156">Stop</span></span>

<span data-ttu-id="5d60a-157">Smellið á **Stöðva** til að stöðva skráninguna.</span><span class="sxs-lookup"><span data-stu-id="5d60a-157">Click **Stop** to end the recording session.</span></span> <span data-ttu-id="5d60a-158">Athugið að hægt er að byrja aftur á lotu eftir að hún hefur verið stöðvuð.</span><span class="sxs-lookup"><span data-stu-id="5d60a-158">Note that you can't restart a session after you end it.</span></span> <span data-ttu-id="5d60a-159">Því skal ganga úr skugga um að skráningunni sé lokið áður en henni er hætt.</span><span class="sxs-lookup"><span data-stu-id="5d60a-159">Therefore, make sure that the recording is completed before you end it.</span></span>

### <a name="pause"></a><span data-ttu-id="5d60a-160">Hlé</span><span class="sxs-lookup"><span data-stu-id="5d60a-160">Pause</span></span>

<span data-ttu-id="5d60a-161">Smellt er á **Hlé** til að stöðva skráninguna tímabundið (gera hlé) og halda áfram við aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="5d60a-161">Click **Pause** to temporarily stop (pause) the recording session and continue with the operation.</span></span> <span data-ttu-id="5d60a-162">Skrefin sem framkvæmd eru eftir að smellt er á **Hlé** eru ekki skráð..</span><span class="sxs-lookup"><span data-stu-id="5d60a-162">Steps that you perform after you click **Pause** aren't recorded.</span></span>

### <a name="continue"></a><span data-ttu-id="5d60a-163">Halda áfram</span><span class="sxs-lookup"><span data-stu-id="5d60a-163">Continue</span></span>

<span data-ttu-id="5d60a-164">Smellið á **Halda áfram** til að halda áfram með skráningarlotuna eftir að hlé var gert á henni.</span><span class="sxs-lookup"><span data-stu-id="5d60a-164">To resume the recording session after you've paused it, click **Continue**.</span></span>

### <a name="capture-screenshots"></a><span data-ttu-id="5d60a-165">Taka skjámyndir</span><span class="sxs-lookup"><span data-stu-id="5d60a-165">Capture screenshots</span></span>

<span data-ttu-id="5d60a-166">Verkskráning getur tekið skjámyndir af notendaviðmóti Retail Modern POS á meðan þú skráir viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="5d60a-166">Task recorder can capture screenshots of the Retail Modern POS UI as you record a business process.</span></span> <span data-ttu-id="5d60a-167">Til að kveikja á eiginleikanum til að taka skjámyndir skal stilla valkostinn **Taka skjámynd** á **Já** og svo framkvæma upptökuna.</span><span class="sxs-lookup"><span data-stu-id="5d60a-167">To turn on the screenshot capture feature, set the **Capture screenshot** option to **Yes** and then make the recording.</span></span> <span data-ttu-id="5d60a-168">Þegar upptökunni er lokið skal smella á **Stopp** og hlaða niður Word-skjalinu.</span><span class="sxs-lookup"><span data-stu-id="5d60a-168">Once the recording is completed, click **Stop** and download the Word document.</span></span> <span data-ttu-id="5d60a-169">Skjalið mun innihalda skrefin með viðeigandi skjámyndum.</span><span class="sxs-lookup"><span data-stu-id="5d60a-169">The document will contain the steps with relevant screenshots.</span></span>

> [!NOTE]
> <span data-ttu-id="5d60a-170">Virknin Taka skjámynd er ekki studd í Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="5d60a-170">Capture screenshot functionality is not supported in Cloud POS.</span></span>

### <a name="start-task-and-end-task"></a><span data-ttu-id="5d60a-171">Hefja verk og Ljúka verki</span><span class="sxs-lookup"><span data-stu-id="5d60a-171">Start task and End task</span></span>

<span data-ttu-id="5d60a-172">Hægt er að tilgreina upphaf og endi mengis skrefa sem flokkuð eru saman í hópa með því að nota hnappana **Hefja verk** og **Ljúka** **verki**.</span><span class="sxs-lookup"><span data-stu-id="5d60a-172">You can specify the beginning and end of a set of grouped steps by using the **Start task** and **End** **task** buttons.</span></span> <span data-ttu-id="5d60a-173">Smellið á **Hefja verk** til að bæta við „Hefja verk“-skrefi og framkvæmið svo skrefið sem á að taka með í hópnum.</span><span class="sxs-lookup"><span data-stu-id="5d60a-173">Click **Start task** to add a "Start Task" step, and then perform the steps that should be included in the group.</span></span> <span data-ttu-id="5d60a-174">Þegar búið er að framkvæma skrefin fyrir þennan hóp er smellt á **Ljúka verki**.</span><span class="sxs-lookup"><span data-stu-id="5d60a-174">After you've finished performing the steps for the group, click **End task**.</span></span> <span data-ttu-id="5d60a-175">Verk hjálpa þér að skipuleggja verkferlin þín.</span><span class="sxs-lookup"><span data-stu-id="5d60a-175">Tasks help you organize your procedures.</span></span> <span data-ttu-id="5d60a-176">Verk er hægt að falda innan annarra verka.</span><span class="sxs-lookup"><span data-stu-id="5d60a-176">Tasks can be nested within other tasks.</span></span> <span data-ttu-id="5d60a-177">Þannig verður auðveldara að skipuleggja mjög löng og flókin viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="5d60a-177">In this way, you can better organize very long and complex business processes.</span></span>

## <a name="adding-annotations"></a><span data-ttu-id="5d60a-178">Athugasemdum bætt við</span><span class="sxs-lookup"><span data-stu-id="5d60a-178">Adding annotations</span></span>

<span data-ttu-id="5d60a-179">Athugasemd er viðbótartexti sem bætt er við skref í skráningu.</span><span class="sxs-lookup"><span data-stu-id="5d60a-179">An annotation is additional text that you add to a step in a recording.</span></span> <span data-ttu-id="5d60a-180">Til dæmis er hægt að nota athugasemdir til að gefa notandanum skýrara samhengi eða leiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="5d60a-180">For example, you can use annotations to give the user more context or instructions.</span></span> <span data-ttu-id="5d60a-181">Hægt er að bæta við athugasemdir á undan or á eftir a skref.athugasemdum á undan eða á eftir þrepi.</span><span class="sxs-lookup"><span data-stu-id="5d60a-181">You can add annotations before or after a step.</span></span> <span data-ttu-id="5d60a-182">Hægt er að bæta við athugasemd í hvaða skrefi sem er með því að smella á hnappinn **Breyta** (blýantstákn) hægra megin við skrefið.</span><span class="sxs-lookup"><span data-stu-id="5d60a-182">You can add an annotation to any step by clicking the **Edit** button (pencil symbol) to the right of the step.</span></span>

<span data-ttu-id="5d60a-183">[![Breyta hnappi fyrir þrep](./media/annotate.jpg)](./media/annotate.jpg)</span><span class="sxs-lookup"><span data-stu-id="5d60a-183">[![Edit button for a step](./media/annotate.jpg)](./media/annotate.jpg)</span></span>

### <a name="texts-and-notes"></a><span data-ttu-id="5d60a-184">Textar og athugasemdir</span><span class="sxs-lookup"><span data-stu-id="5d60a-184">Texts and notes</span></span>

<span data-ttu-id="5d60a-185">Hægt er að nota reitina **Textar** og **Athugasemdir** til að bæta við texta sem ætti að tengja við skref í Verkefnaleiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="5d60a-185">You can use the **Texts** and **Notes** fields to add text that should be associated with a step in a Task guide.</span></span>

<span data-ttu-id="5d60a-186">[![Reitirnir Texti og Athugasemdir](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span><span class="sxs-lookup"><span data-stu-id="5d60a-186">[![Text and Notes fields](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span></span>

#### <a name="text"></a><span data-ttu-id="5d60a-187">Texti</span><span class="sxs-lookup"><span data-stu-id="5d60a-187">Text</span></span>

<span data-ttu-id="5d60a-188">Texti sem færður er inn í reitinn **Texti** birtist *fyrir ofan* texta fyrir skref í Verkefnaleiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="5d60a-188">Text that you enter in the **Text** field appears *above* the step text in the Task guide.</span></span> <span data-ttu-id="5d60a-189">Þessi staðsetning er fyrir textann sem notandinn að lesa áður en hann eða hún lýkur við skrefið.</span><span class="sxs-lookup"><span data-stu-id="5d60a-189">This location is appropriate for text that you want the user to read before he or she completes the step.</span></span>

#### <a name="notes"></a><span data-ttu-id="5d60a-190">Athugasemdir</span><span class="sxs-lookup"><span data-stu-id="5d60a-190">Notes</span></span>

<span data-ttu-id="5d60a-191">Texti sem færður er inn reitinn **Texti** birtist *undir* texta um skref í Verkefnaleiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="5d60a-191">Text that you enter in the **Notes** field appears *below* the step text in the Task guide.</span></span> <span data-ttu-id="5d60a-192">Til að lesa textann fyrir athugasemdina þarf notandinn að víkka texta um skref í sprettiglugga.</span><span class="sxs-lookup"><span data-stu-id="5d60a-192">To read the note text, the user must expand the step text in the pop-up window.</span></span> <span data-ttu-id="5d60a-193">Þessi staðsetning er fyrir valfrjálst lesefni eða aðrar upplýsingar sem gætu verið gagnlegar fyrir notandann en sem notandinn þarf ekki nauðsynlega að lesa áður en hann eða hún lýkur við aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="5d60a-193">This location is appropriate for optional reading material or other information that might be useful to the user, but that the user doesn't require in order to complete the action.</span></span>

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a><span data-ttu-id="5d60a-194">Hjálp í Retail Modern POS og sölukerfi í skýinu</span><span class="sxs-lookup"><span data-stu-id="5d60a-194">Help in Retail Modern POS and Cloud POS</span></span>

<span data-ttu-id="5d60a-195">Til að sýna þínar eigin sérsniðnu verkskráningar í hjálparsvæðinu á Retail Modern POS og Cloud POS þannig að hægt er að skoða þær sem texta eða skoða texta þarf að vista verkskráninguna í eigin BPM-safni og síðan uppfæra færibreytur Hjálparkerfis til að vísa í BPM-safnið þitt.</span><span class="sxs-lookup"><span data-stu-id="5d60a-195">To show your own custom task recordings in the Help pane of Retail Modern POS and Cloud POS so that they can be viewed as text, you must save your task recordings to your own BPM library, and then update your Help system parameters to point to your BPM library.</span></span> <span data-ttu-id="5d60a-196">Nánari upplýsingar, sjá [Tengt við hjálparkerfið](../fin-and-ops/get-started/help-connect.md).</span><span class="sxs-lookup"><span data-stu-id="5d60a-196">For more information, see [Connecting the Help system](../fin-and-ops/get-started/help-connect.md).</span></span> <span data-ttu-id="5d60a-197">Retail Modern POS og Cloud POS Help leita í LCS í rauntíma.</span><span class="sxs-lookup"><span data-stu-id="5d60a-197">Retail Modern POS and Cloud POS Help searches LCS in real time.</span></span> <span data-ttu-id="5d60a-198">Leitin er gerð í öllum BPM-söfnum sem valin eru í færibreytum fyrir Hjálparkerfi Commerce og leitin birtir viðeigandi niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="5d60a-198">It searches across all the BPM libraries that are selected in the Commerce Help system parameters and shows the relevant results.</span></span> <span data-ttu-id="5d60a-199">Til að komast í valmyndina **Hjálp** er smellt á hnappinn **Hjálp** (spurningamerki) efst á skjánum og síðan er heiti verkferlisins slegið inn í leitargluggann og smellt á hnappinn Leita.</span><span class="sxs-lookup"><span data-stu-id="5d60a-199">To access the **Help** menu, click the **Help** button (question mark) at the top of the screen and then in the search box type your process name and hit the search button.</span></span>

<span data-ttu-id="5d60a-200">[![Hnappurinn Hjálp](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="5d60a-200">[![Help button](./media/help.jpg)](./media/help.jpg)</span></span>

<span data-ttu-id="5d60a-201">Þegar smellt er á Verkefnaleiðberiningar í leitarniðurstöðum er hægt að skoða þrepin sem hjálparefni eða flytja út þrepin í Word-skjal.</span><span class="sxs-lookup"><span data-stu-id="5d60a-201">When you click a Task guide in the search results, you can either view the steps as a Help topic or export the steps to a Word document.</span></span>

> [!NOTE]
> <span data-ttu-id="5d60a-202">Hjálp í Retail Modern POS og sölukerfi í skýinu mun ekki sýna verkefnaleiðbeiningar í samræmi við skjámyndina sem þú ert í eða aðgerðina sem þú ert að framkvæma.</span><span class="sxs-lookup"><span data-stu-id="5d60a-202">Help in Retail Modern POS and Cloud POS will not bring up task guides according to what form you're on or operation you're doing.</span></span> <span data-ttu-id="5d60a-203">Hafa við vinnslu nafn í reitnum leit og smellið síðan á **Leit**.</span><span class="sxs-lookup"><span data-stu-id="5d60a-203">You have to type the process name in the search box and then click **Search**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]