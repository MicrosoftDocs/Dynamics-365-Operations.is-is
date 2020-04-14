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
# <a name="electronic-reporting-advanced-formula-editor"></a>Rafræn skýrsla ítarlegur ritill fyrir formúlu

[!include [banner](../includes/banner.md)]

Í viðbót við [Rafræn skýrslugerð](general-electronic-reporting.md) [formúluritill](general-electronic-reporting-formula-designer.md) geturðu notað ítarlegan formúluritil rafrænnar skýrslugerðar til að bæta upplifunina af því að stilla segðir rafrænnar skýrslugerðar (ER). Ítarlegur ritillinn er byggður á vafra og knúinn af [Mónakó-ritli](https://microsoft.github.io/monaco-editor). Mest notuðu ítarlegu aðgerðum ritilsins er lýst í þessu efni:

- [Sjálfvirk snið á kóðum](#Autoformatting)
- [IntelliSense](#IntelliSense)
- [Kóðalok](#CodeCompletion)
- [Kóðayfirlit](#CodeNavigation)
- [Uppbygging kóða](#CodeStructuring)
- [Finna og skrifa yfir](#FindAndReplace)
- [Gagnalíming](#DataPasting)
- [Málskipunarlýsing](#SyntaxColorization)

## <a name=""></a><a name="ActivateAdvEditor">Kveikja á ítarlega formúluritlinum</a>

Ljúktu eftirfarandi skrefum til að byrja að nota ítarlega formúluritara í þínu tilviki Microsoft Dynamics 365 Finance.

1.  Opnið **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2.  Á síðunni **Skilgreiningar** , í aðgerðarúðunni, í flipanum **Skilgreiningar** , í flokknum **Ítarlegar stillingar** , skal velja **Færibreytur notanda**.
3.  Í glugganum **Breytur notanda** í hlutanum **Rakning keyrslu** stillirðu færibreytuna **Virkja ítarlegan formúluritil** á **Já**.

[![Skilgreiningarsíða í ER](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)

> [!NOTE]
> Hafðu í huga að þessi færibreyta er notandasértæk og fyrirtækjasértæk.

## <a name=""></a><a name="Autoformatting">Sjálfvirk snið á kóðum</a>

Þegar þú skrifar flókna segð sem samanstendur af mörgum línum af kóða verður inndráttur á nýrri innfellda línu sjálfkrafa byggður á inndrætti fyrri raðar. Þú getur valið línur og breytt ídrætti þeirra með því að slá inn **Flipi** eða **Shift+Tab**.

[![ER-formúluritill](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)

Sjálfvirk snið gerir þér kleift að halda allri segðinni vel sniðinni til að gera frekara viðhald auðveldara og til að einfalda skilning á stilltu rökfræði.

## <a name=""></a><a name="IntelliSense">IntelliSense</a>

Ritillinn veitir lok orða til að hjálpa þér að skrifa segð hraðar og forðast innsláttarvillur. Þegar þú byrjar að bæta við nýjum texta býður ritillinn sjálfkrafa upp lista yfir aðgerðir studdar í ER aðgerðum sem innihalda stafi sem þú hefur slegið inn. Þú getur einnig kveikt á IntelliSense á hverjum stað sem er stillt með því að slá inn **Ctrl+Bil**.

[![ER-formúluritill](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)

## <a name=""></a><a name="CodeCompletion">Kóðalok</a>

Ritillinn gefur sjálfkrafa út kóðalok með:

- Setja lokun sviga í þegar opnun sviga er slegin inn, svo að bendillinn helst innan svigans.
- Að setja annað tilvitnunartáknið inn þegar það fyrsta er slegið inn og halda bendilnum inni í tilvitnunum.
- Að setja annað tvöfalda tilvitnunartáknið inn þegar það fyrsta er slegið inn og halda bendilnum inni í tilvitnunum.

[![ER-formúluritill](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)

Þegar þú bendir á innsleginn sviga er seinni sviginn í parinu sjálfkrafa auðkenndur til að sýna uppbygginguna sem þeir styðja.

## <a name=""></a><a name="CodeNavigation">Kóðayfirlit</a>

Þú getur fundið nauðsynleg tákn eða línur í segðinni með því að slá inn skipunina **Fara í** með skipanatöflu eða samhengisvalmyndinni.

Til dæmis, til að hoppa til línu **8** gerirðu eftirfarandi:

- Ýttu á **Ctrl+G**, sláðu inn gildið **8** og ýttu síðan á **Færa inn**.

  -eða-

- Ýttu á **F1**, sláðu inn **G**, veldu **Fara í línu**, sláðu inn gildið **8** og ýttu síðan á **Færa inn**.

[![ER-formúluritill](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)

## <a name=""></a><a name="CodeStructuring">Uppbygging kóða</a>

Kóðinn fyrir sumar aðgerðir, svo sem [IF](er-functions-logical-if.md) eða [CASE](er-functions-logical-case.md), er sjálfkrafa skipulagður. Þú getur stækkað og hrunið einhverju eða öllu samanbrotnu svæði þessa kóða til að draga úr breytanlegum hluta segðarinnar til að einbeita sér aðeins að því stykki af kóða sem þarfnast athygli þinnar. Hægt er að nota skipanirnar brjóta saman/brjóta sundur fyrir það.

Til dæmis, til að brjóta saman öll svæði, gerirðu eftirfarandi:

- Ýttu á **Ctrl+K**

  -eða-

- Ýttu á **F1**, ýttu á **FO**, veldu **Brjóta allt saman** og ýttu síðan á **Færa inn**

Til að brjóta öll svæði sundur gerirðu eftirfarandi:

- Ýttu á **Ctrl+J**

  -eða-
  
- Ýttu á **F1**, sláðu inn **UN**, veldu **Brjóta allt sundur** og ýttu síðan á **Færa inn**

[![ER-formúluritill](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)

## <a name=""></a><a name="FindAndReplace">Finna og skrifa yfir</a>

Til að finna tilvik ákveðins texta skaltu velja textann í segðinni og gera eftirfarandi:

- Ýttu á **Ctrl+F** og ýttu síðan á **F3** til að finna næsta tilvik valins texta eða ýttu á **Shift+F3** til að finna fyrra tilvikið.

  -eða-
  
- Ýttu á **F1**, sláðu inn **F**, og veldu síðan nauðsynlegan valkost til að finna valinn texta.

Til að skipta út tilvikum ákveðins texta skaltu velja textann í segðinni og gera eftirfarandi:

- Ýttu á **Ctrl+H**. Sláðu inn hinn textann og veldu valkostinn sem kemur í staðinn fyrir annaðhvort valinn texta eða öll tilvik textans í núverandi segð.

  -eða-
  
- Ýttu á **F1**, sláðu inn **R**, og veldu síðan nauðsynlegan valkost til að skipta út völdum texta. Sláðu inn hinn textann og veldu valkostinn sem kemur í staðinn fyrir annaðhvort valinn texta eða öll tilvik textans í núverandi segð.

Til að breyta öllum tilvikum ákveðins texta skaltu velja textann í segðinni og gera eftirfarandi:

- Ýttu á **Ctrl+F2** og sláðu síðan inn annan textann.

  -eða-
  
- Ýttu á **F1**, sláðu inn **C**, og veldu síðan nauðsynlegan valkost til að breyta völdum texta. Sláðu inn annan texta.

[![ER-formúluritill](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)

## <a name=""></a><a name="DataPasting">Gagnaheimildir og aðgerðir líma</a>

Þú getur valið **Bæta við gagnagjafa**, sem límir við núverandi segð gagnagjafa sem er nú valinn á vinstra spjaldinu **Gagnagjafi**. Eins geturðu valið **Bæta við aðgerð**, sem límir við núverandi segð aðgerð sem er nú valinn á hægra spjaldinu **Aðgerðir**. Ef þú notar ER formúluritilinn, verður valin aðgerð eða valinn gagnagjafi alltaf límd í lok stilltrar segðarinnar. Þegar þú notar ítarlegan ER-formúluritilinn er hægt að líma valda aðgerð eða valinn gagnagjafa við einhvern hluta stilltrar segðarinnar. Þú verður að nota bendilinn til að tilgreina hvar þú vilt líma gögnin.

[![ER-formúluritill](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)

## <a name=""></a><a name="SyntaxColorization">Málskipunarlýsing</a>

Eins og er eru mismunandi litir notaðir til að varpa ljósi á eftirfarandi hluta segða:

- Textinn í tvöföldum sviga sem getur táknað merkimiða kennis textafasta.

[![ER-formúluritill](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md)
- [Mónakó-ritill](https://microsoft.github.io/monaco-editor)
