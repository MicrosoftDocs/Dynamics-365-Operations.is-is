---
title: Rafræn skýrsla ítarlegur ritill fyrir formúlu
description: Þetta efni lýsir því hvernig hægt er að nota háþróaða formúluritilinn til að stilla segðir í líkanavörpun rafrænnar skýrslugerðar (ER) og sniðhlutum.
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: df402bc20753d2ba14295592f4b40e20f9fdc7bf
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138899"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="09efe-103">Rafræn skýrsla ítarlegur ritill fyrir formúlu</span><span class="sxs-lookup"><span data-stu-id="09efe-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09efe-104">Í viðbót við [Rafræn skýrslugerð](general-electronic-reporting.md) [formúluritill](general-electronic-reporting-formula-designer.md) geturðu notað ítarlegan formúluritil rafrænnar skýrslugerðar til að bæta upplifunina af því að stilla segðir rafrænnar skýrslugerðar (ER).</span><span class="sxs-lookup"><span data-stu-id="09efe-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="09efe-105">Ítarlegur ritillinn er byggður á vafra og knúinn af [Mónakó-ritli](https://microsoft.github.io/monaco-editor).</span><span class="sxs-lookup"><span data-stu-id="09efe-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="09efe-106">Mest notuðu ítarlegu aðgerðum ritilsins er lýst í þessu efni:</span><span class="sxs-lookup"><span data-stu-id="09efe-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="09efe-107">Sjálfvirk snið á kóðum</span><span class="sxs-lookup"><span data-stu-id="09efe-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="09efe-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="09efe-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="09efe-109">Kóðalok</span><span class="sxs-lookup"><span data-stu-id="09efe-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="09efe-110">Kóðayfirlit</span><span class="sxs-lookup"><span data-stu-id="09efe-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="09efe-111">Uppbygging kóða</span><span class="sxs-lookup"><span data-stu-id="09efe-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="09efe-112">Finna og skrifa yfir</span><span class="sxs-lookup"><span data-stu-id="09efe-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="09efe-113">Gagnalíming</span><span class="sxs-lookup"><span data-stu-id="09efe-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="09efe-114">Málskipunarlýsing</span><span class="sxs-lookup"><span data-stu-id="09efe-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="09efe-115"><a name="ActivateAdvEditor">Kveikja á ítarlega formúluritlinum</a></span><span class="sxs-lookup"><span data-stu-id="09efe-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="09efe-116">Ljúktu eftirfarandi skrefum til að byrja að nota ítarlega formúluritara í þínu tilviki Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="09efe-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="09efe-117">Opnið **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="09efe-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="09efe-118">Á síðunni **Skilgreiningar** , í aðgerðarúðunni, í flipanum **Skilgreiningar** , í flokknum **Ítarlegar stillingar** , skal velja **Færibreytur notanda**.</span><span class="sxs-lookup"><span data-stu-id="09efe-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="09efe-119">Í glugganum **Breytur notanda** í hlutanum **Rakning keyrslu** stillirðu færibreytuna **Virkja ítarlegan formúluritil** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="09efe-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="09efe-120">[![Skilgreiningarsíða í ER](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="09efe-120">[![ER configurations page](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="09efe-121">Hafðu í huga að þessi færibreyta er notandasértæk og fyrirtækjasértæk.</span><span class="sxs-lookup"><span data-stu-id="09efe-121">Be aware that this parameter is user specific and company specific.</span></span>

## <a name=""></a><span data-ttu-id="09efe-122"><a name="Autoformatting">Sjálfvirk snið á kóðum</a></span><span class="sxs-lookup"><span data-stu-id="09efe-122"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="09efe-123">Þegar þú skrifar flókna segð sem samanstendur af mörgum línum af kóða verður inndráttur á nýrri innfellda línu sjálfkrafa byggður á inndrætti fyrri raðar.</span><span class="sxs-lookup"><span data-stu-id="09efe-123">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="09efe-124">Þú getur valið línur og breytt ídrætti þeirra með því að slá inn **Flipi** eða **Shift+Tab**.</span><span class="sxs-lookup"><span data-stu-id="09efe-124">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="09efe-125">[![ER-formúluritill](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="09efe-125">[![ER formula editor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="09efe-126">Sjálfvirk snið gerir þér kleift að halda allri segðinni vel sniðinni til að gera frekara viðhald auðveldara og til að einfalda skilning á stilltu rökfræði.</span><span class="sxs-lookup"><span data-stu-id="09efe-126">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="09efe-127"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="09efe-127"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="09efe-128">Ritillinn veitir lok orða til að hjálpa þér að skrifa segð hraðar og forðast innsláttarvillur.</span><span class="sxs-lookup"><span data-stu-id="09efe-128">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="09efe-129">Þegar þú byrjar að bæta við nýjum texta býður ritillinn sjálfkrafa upp lista yfir aðgerðir studdar í ER aðgerðum sem innihalda stafi sem þú hefur slegið inn.</span><span class="sxs-lookup"><span data-stu-id="09efe-129">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="09efe-130">Þú getur einnig kveikt á IntelliSense á hverjum stað sem er stillt með því að slá inn **Ctrl+Bil**.</span><span class="sxs-lookup"><span data-stu-id="09efe-130">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="09efe-131">[![ER-formúluritill](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="09efe-131">[![ER formula editor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="09efe-132"><a name="CodeCompletion">Kóðalok</a></span><span class="sxs-lookup"><span data-stu-id="09efe-132"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="09efe-133">Ritillinn gefur sjálfkrafa út kóðalok með:</span><span class="sxs-lookup"><span data-stu-id="09efe-133">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="09efe-134">Setja lokun sviga í þegar opnun sviga er slegin inn, svo að bendillinn helst innan svigans.</span><span class="sxs-lookup"><span data-stu-id="09efe-134">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="09efe-135">Að setja annað tilvitnunartáknið inn þegar það fyrsta er slegið inn og halda bendilnum inni í tilvitnunum.</span><span class="sxs-lookup"><span data-stu-id="09efe-135">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="09efe-136">Að setja annað tvöfalda tilvitnunartáknið inn þegar það fyrsta er slegið inn og halda bendilnum inni í tilvitnunum.</span><span class="sxs-lookup"><span data-stu-id="09efe-136">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="09efe-137">[![ER-formúluritill](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="09efe-137">[![ER formula editor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="09efe-138">Þegar þú bendir á innsleginn sviga er seinni sviginn í parinu sjálfkrafa auðkenndur til að sýna uppbygginguna sem þeir styðja.</span><span class="sxs-lookup"><span data-stu-id="09efe-138">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="09efe-139"><a name="CodeNavigation">Kóðayfirlit</a></span><span class="sxs-lookup"><span data-stu-id="09efe-139"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="09efe-140">Þú getur fundið nauðsynleg tákn eða línur í segðinni með því að slá inn skipunina **Fara í** með skipanatöflu eða samhengisvalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="09efe-140">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="09efe-141">Til dæmis, til að hoppa til línu **8** gerirðu eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="09efe-141">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="09efe-142">Ýttu á **Ctrl+G**, sláðu inn gildið **8** og ýttu síðan á **Færa inn**.</span><span class="sxs-lookup"><span data-stu-id="09efe-142">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="09efe-143">-eða-</span><span class="sxs-lookup"><span data-stu-id="09efe-143">-or-</span></span>

- <span data-ttu-id="09efe-144">Ýttu á **F1**, sláðu inn **G**, veldu **Fara í línu**, sláðu inn gildið **8** og ýttu síðan á **Færa inn**.</span><span class="sxs-lookup"><span data-stu-id="09efe-144">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="09efe-145">[![ER-formúluritill](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="09efe-145">[![ER formula editor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="09efe-146"><a name="CodeStructuring">Uppbygging kóða</a></span><span class="sxs-lookup"><span data-stu-id="09efe-146"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="09efe-147">Kóðinn fyrir sumar aðgerðir, svo sem [IF](er-functions-logical-if.md) eða [CASE](er-functions-logical-case.md), er sjálfkrafa skipulagður.</span><span class="sxs-lookup"><span data-stu-id="09efe-147">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="09efe-148">Þú getur stækkað og hrunið einhverju eða öllu samanbrotnu svæði þessa kóða til að draga úr breytanlegum hluta segðarinnar til að einbeita sér aðeins að því stykki af kóða sem þarfnast athygli þinnar.</span><span class="sxs-lookup"><span data-stu-id="09efe-148">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="09efe-149">Hægt er að nota skipanirnar brjóta saman/brjóta sundur fyrir það.</span><span class="sxs-lookup"><span data-stu-id="09efe-149">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="09efe-150">Til dæmis, til að brjóta saman öll svæði, gerirðu eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="09efe-150">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="09efe-151">Ýttu á **Ctrl+K**</span><span class="sxs-lookup"><span data-stu-id="09efe-151">Press **Ctrl+K**</span></span>

  <span data-ttu-id="09efe-152">-eða-</span><span class="sxs-lookup"><span data-stu-id="09efe-152">-or-</span></span>

- <span data-ttu-id="09efe-153">Ýttu á **F1**, ýttu á **FO**, veldu **Brjóta allt saman** og ýttu síðan á **Færa inn**</span><span class="sxs-lookup"><span data-stu-id="09efe-153">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="09efe-154">Til að brjóta öll svæði sundur gerirðu eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="09efe-154">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="09efe-155">Ýttu á **Ctrl+J**</span><span class="sxs-lookup"><span data-stu-id="09efe-155">Press **Ctrl+J**</span></span>

  <span data-ttu-id="09efe-156">-eða-</span><span class="sxs-lookup"><span data-stu-id="09efe-156">-or-</span></span>
  
- <span data-ttu-id="09efe-157">Ýttu á **F1**, sláðu inn **UN**, veldu **Brjóta allt sundur** og ýttu síðan á **Færa inn**</span><span class="sxs-lookup"><span data-stu-id="09efe-157">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="09efe-158">[![ER-formúluritill](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="09efe-158">[![ER formula editor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="09efe-159"><a name="FindAndReplace">Finna og skrifa yfir</a></span><span class="sxs-lookup"><span data-stu-id="09efe-159"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="09efe-160">Til að finna tilvik ákveðins texta skaltu velja textann í segðinni og gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="09efe-160">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="09efe-161">Ýttu á **Ctrl+F** og ýttu síðan á **F3** til að finna næsta tilvik valins texta eða ýttu á **Shift+F3** til að finna fyrra tilvikið.</span><span class="sxs-lookup"><span data-stu-id="09efe-161">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="09efe-162">-eða-</span><span class="sxs-lookup"><span data-stu-id="09efe-162">-or-</span></span>
  
- <span data-ttu-id="09efe-163">Ýttu á **F1**, sláðu inn **F**, og veldu síðan nauðsynlegan valkost til að finna valinn texta.</span><span class="sxs-lookup"><span data-stu-id="09efe-163">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="09efe-164">Til að skipta út tilvikum ákveðins texta skaltu velja textann í segðinni og gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="09efe-164">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="09efe-165">Ýttu á **Ctrl+H**.</span><span class="sxs-lookup"><span data-stu-id="09efe-165">Press **Ctrl+H**.</span></span> <span data-ttu-id="09efe-166">Sláðu inn hinn textann og veldu valkostinn sem kemur í staðinn fyrir annaðhvort valinn texta eða öll tilvik textans í núverandi segð.</span><span class="sxs-lookup"><span data-stu-id="09efe-166">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="09efe-167">-eða-</span><span class="sxs-lookup"><span data-stu-id="09efe-167">-or-</span></span>
  
- <span data-ttu-id="09efe-168">Ýttu á **F1**, sláðu inn **R**, og veldu síðan nauðsynlegan valkost til að skipta út völdum texta.</span><span class="sxs-lookup"><span data-stu-id="09efe-168">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="09efe-169">Sláðu inn hinn textann og veldu valkostinn sem kemur í staðinn fyrir annaðhvort valinn texta eða öll tilvik textans í núverandi segð.</span><span class="sxs-lookup"><span data-stu-id="09efe-169">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="09efe-170">Til að breyta öllum tilvikum ákveðins texta skaltu velja textann í segðinni og gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="09efe-170">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="09efe-171">Ýttu á **Ctrl+F2** og sláðu síðan inn annan textann.</span><span class="sxs-lookup"><span data-stu-id="09efe-171">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="09efe-172">-eða-</span><span class="sxs-lookup"><span data-stu-id="09efe-172">-or-</span></span>
  
- <span data-ttu-id="09efe-173">Ýttu á **F1**, sláðu inn **C**, og veldu síðan nauðsynlegan valkost til að breyta völdum texta.</span><span class="sxs-lookup"><span data-stu-id="09efe-173">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="09efe-174">Sláðu inn annan texta.</span><span class="sxs-lookup"><span data-stu-id="09efe-174">Enter the alternative text.</span></span>

<span data-ttu-id="09efe-175">[![ER-formúluritill](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="09efe-175">[![ER formula editor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="09efe-176"><a name="DataPasting">Gagnaheimildir og aðgerðir líma</a></span><span class="sxs-lookup"><span data-stu-id="09efe-176"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="09efe-177">Þú getur valið **Bæta við gagnagjafa**, sem límir við núverandi segð gagnagjafa sem er nú valinn á vinstra spjaldinu **Gagnagjafi**.</span><span class="sxs-lookup"><span data-stu-id="09efe-177">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="09efe-178">Eins geturðu valið **Bæta við aðgerð**, sem límir við núverandi segð aðgerð sem er nú valinn á hægra spjaldinu **Aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="09efe-178">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="09efe-179">Ef þú notar ER formúluritilinn, verður valin aðgerð eða valinn gagnagjafi alltaf límd í lok stilltrar segðarinnar.</span><span class="sxs-lookup"><span data-stu-id="09efe-179">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="09efe-180">Þegar þú notar ítarlegan ER-formúluritilinn er hægt að líma valda aðgerð eða valinn gagnagjafa við einhvern hluta stilltrar segðarinnar.</span><span class="sxs-lookup"><span data-stu-id="09efe-180">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="09efe-181">Þú verður að nota bendilinn til að tilgreina hvar þú vilt líma gögnin.</span><span class="sxs-lookup"><span data-stu-id="09efe-181">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="09efe-182">[![ER-formúluritill](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="09efe-182">[![ER formula editor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="09efe-183"><a name="SyntaxColorization">Málskipunarlýsing</a></span><span class="sxs-lookup"><span data-stu-id="09efe-183"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="09efe-184">Eins og er eru mismunandi litir notaðir til að varpa ljósi á eftirfarandi hluta segða:</span><span class="sxs-lookup"><span data-stu-id="09efe-184">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="09efe-185">Textinn í tvöföldum sviga sem getur táknað merkimiða kennis textafasta.</span><span class="sxs-lookup"><span data-stu-id="09efe-185">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="09efe-186">[![ER-formúluritill](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="09efe-186">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="09efe-187">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="09efe-187">Additional resources</span></span>

- [<span data-ttu-id="09efe-188">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="09efe-188">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="09efe-189">Formúluhönnuður í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="09efe-189">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="09efe-190">Mónakó-ritill</span><span class="sxs-lookup"><span data-stu-id="09efe-190">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)
