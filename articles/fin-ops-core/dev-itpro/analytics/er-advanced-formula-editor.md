---
title: Rafræn skýrsla ítarlegur ritill fyrir formúlu
description: Þessi grein lýsir því hvernig hægt er að nota háþróaða formúluritilinn til að stilla segðir í líkanavörpun rafrænnar skýrslugerðar (ER) og sniðhlutum.
author: kfend
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
ms.openlocfilehash: 269102028962cf1ebae599b9885f97871785a551
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286218"
---
# <a name="electronic-reporting-advanced-formula-editor"></a>Rafræn skýrsla ítarlegur ritill fyrir formúlu

[!include [banner](../includes/banner.md)]

Í viðbót við [Rafræn skýrslugerð](general-electronic-reporting.md) [formúluritill](general-electronic-reporting-formula-designer.md) geturðu notað ítarlegan formúluritil rafrænnar skýrslugerðar til að bæta upplifunina af því að stilla segðir rafrænnar skýrslugerðar (ER). Ítarlegur ritillinn er byggður á vafra og knúinn af [Mónakó-ritli](https://microsoft.github.io/monaco-editor). Mest notuðu ítarlegu aðgerðum ritilsins er lýst í þessari grein:

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

1.  Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2.  Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
3.  Í svarglugganum **Færibreytur notanda**, í hlutanum **Rakning keyrslu**, skal stilla færibreytuna **Kveikja á ítarlegum formúluritli** á **Já**.

[![Svarglugginn Notandafæribreytur, Virkja færibreytu ítarlegs formúluritils auðkennt.](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)

> [!NOTE]
> Hafðu í huga að þessi færibreyta er notandasértæk og fyrirtækjasértæk.

Frá og með Microsoft Dynamics 365 Finance útgáfu 10.0.19 er hægt að stjórna því hvaða formúluritill rafrænnar skýrslugerðar er sjálfgefið boðið upp á. Ljúkið eftirfarandi skrefum til að virkja ítarlegan formúluritil fyrir alla notendur og fyrirtæki núverandi fjármálatilviks.

1.  Opnaðu vinnusvæðið **Eiginleikastjórnun**.
2.  Finnið og veljið eiginleikann **Stilla ítarlegan formúluritil rafrænnar skýrslugerðar sem sjálfgefinn fyrir alla notendur** úr listanum og veljið síðan **Virkja núna**.
3.  Farið í **Fyrirtækisstjórnun** > **Rafræn skýrslugerð** > **Skilgreiningar**.
4.  Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
5.  Í svarglugganum **Færibreytur notanda** skal finna færibreytuna **Slökkva á ítarlegum formúluritli** og staðfesta að hún sé stillt á **Nei**.

[![Svarglugginn Notandafæribreytur, Slökkva á færibreytu ítarlegs formúluritils auðkennt.](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)

> [!NOTE]
> Gildi færibreytanna **Kveikja á ítarlegum formúluritli** og **Slökkva á ítarlegum formúluritli** er haldið aðskildum fyrir hvern notanda og boðið upp á í svarglugganum **Færibreytur notanda** eftir því hver staðan er á eiginleikanum **Stilla ítarlegan formúluritil rafrænnar skýrslugerðar sem sjálfgefinn fyrir alla notendur**.

## <a name=""></a><a name="Autoformatting">Sjálfvirk snið á kóðum</a>

Þegar þú skrifar flókna segð sem samanstendur af mörgum línum af kóða verður inndráttur á nýrri innfellda línu sjálfkrafa byggður á inndrætti fyrri raðar. Þú getur valið línur og breytt ídrætti þeirra með því að slá inn **Flipi** eða **Shift+Tab**.

[![Gif-mynd af formúluritli rafrænnar skýrslugerðar þar sem línur eru valdar og inndrætti breytt.](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)

Sjálfvirk snið gerir þér kleift að halda allri segðinni vel sniðinni til að gera frekara viðhald auðveldara og til að einfalda skilning á stilltu rökfræði.

## <a name=""></a><a name="IntelliSense">IntelliSense</a>

Ritillinn veitir lok orða til að hjálpa þér að skrifa segð hraðar og forðast innsláttarvillur. Þegar þú byrjar að bæta við nýjum texta býður ritillinn sjálfkrafa upp lista yfir aðgerðir studdar í ER aðgerðum sem innihalda stafi sem þú hefur slegið inn. Þú getur einnig kveikt á IntelliSense á hverjum stað sem er stillt með því að slá inn **Ctrl+Bil**.

[![Gif-mynd af formúluritli rafrænnar skýrslugerðar þar sem IntelliSense er ræst.](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)

## <a name=""></a><a name="CodeCompletion">Kóðalok</a>

Ritillinn gefur sjálfkrafa út kóðalok með:

- Setja lokun sviga í þegar opnun sviga er slegin inn, svo að bendillinn helst innan svigans.
- Að setja annað tilvitnunartáknið inn þegar það fyrsta er slegið inn og halda bendilnum inni í tilvitnunum.
- Að setja annað tvöfalda tilvitnunartáknið inn þegar það fyrsta er slegið inn og halda bendilnum inni í tilvitnunum.

[![Gif-mynd af formúluritli rafrænnar skýrslugerðar þar sem ritill setur inn kóða sjálfkrafa.](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)

Þegar þú bendir á innsleginn sviga er seinni sviginn í parinu sjálfkrafa auðkenndur til að sýna uppbygginguna sem þeir styðja.

## <a name=""></a><a name="CodeNavigation">Kóðayfirlit</a>

Þú getur fundið nauðsynleg tákn eða línur í segðinni með því að slá inn skipunina **Fara í** með skipanatöflu eða samhengisvalmyndinni.

Til dæmis, til að hoppa til línu **8** gerirðu eftirfarandi:

- Ýttu á **Ctrl+G**, sláðu inn gildið **8** og ýttu síðan á **Færa inn**.

  -eða-

- Ýttu á **F1**, sláðu inn **G**, veldu **Fara í línu**, sláðu inn gildið **8** og ýttu síðan á **Færa inn**.

[![Gif-mynd af formúluritli rafrænnar skýrslugerðar þar sem sýnt er hvernig á að hafa upp á hlutum segðar með skipanatöflu.](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)

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

[![Gif-mynd af formúluritli rafrænnar skýrslugerðar þar sem kóði er sýndur.](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)

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

[![Gif-mynd af formúluritli rafrænnar skýrslugerðar þar sem finna og skipta út er sýnt.](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)

## <a name=""></a><a name="DataPasting">Gagnaheimildir og aðgerðir líma</a>

Þú getur valið **Bæta við gagnagjafa**, sem límir við núverandi segð gagnagjafa sem er nú valinn á vinstra spjaldinu **Gagnagjafi**. Eins geturðu valið **Bæta við aðgerð**, sem límir við núverandi segð aðgerð sem er nú valinn á hægra spjaldinu **Aðgerðir**. Ef þú notar ER formúluritilinn, verður valin aðgerð eða valinn gagnagjafi alltaf límd í lok stilltrar segðarinnar. Þegar þú notar ítarlegan ER-formúluritilinn er hægt að líma valda aðgerð eða valinn gagnagjafa við einhvern hluta stilltrar segðarinnar. Þú verður að nota bendilinn til að tilgreina hvar þú vilt líma gögnin.

[![Gif-mynd af formúluritli rafrænnar skýrslugerðar þar sem gagnagjafa er bætt við og aðgerð límd.](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)

## <a name=""></a><a name="SyntaxColorization">Málskipunarlýsing</a>

Eins og er eru mismunandi litir notaðir til að varpa ljósi á eftirfarandi hluta segða:

- Textinn í tvöföldum sviga sem getur táknað merkimiða kennis textafasta.

[![ER-formúluritill.](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)

## <a name="limitations"></a>Takmarkanir

Ritillinn er nú studdur í eftirfarandi vöfrum:

- Chrome
- Edge
- Firefox
- Opera
- Safari

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md)
- [Mónakó-ritill](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
