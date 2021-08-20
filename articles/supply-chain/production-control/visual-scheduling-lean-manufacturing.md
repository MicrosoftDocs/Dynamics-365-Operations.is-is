---
title: Sjónræn röðun fyrir lean-framleiðslu
description: Þetta efnisatriði veitir upplýsingar um Kanban-áætlunarborð, sem framleiðsluskipuleggjari getur nota' til að stýra og hámarka framleiðsluáætlunina kanban vinnslur.
author: johanhoffmann
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoard, KanbanJobSchedulingListPage, LeanProductionFlowVisualization, KanbanBoardUnplannedJobs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: af5803793a4874ee73f943d0f059047458c37dc48b7d3276dadc8d8803599fb9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764813"
---
# <a name="visual-scheduling-for-lean-manufacturing"></a>Sjónræn röðun fyrir lean-framleiðslu

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um Kanban-áætlunarborð, sem framleiðsluskipuleggjari getur nota' til að stýra og hámarka framleiðsluáætlunina kanban vinnslur.

Þetta efnisatriði veitir upplýsingar um Kanban-áætlunarborð, sem framleiðsluskipuleggjari getur nota' til að stýra og hámarka framleiðsluáætlunina kanban vinnslur.

Áætlunarborð Kanban gerir framleiðsluskipuleggjanda stýra og hámarka framleiðsluáætlunina fyrir kanbanvinnslur. Það gerir flæði kanban-vinnsla gegnsætt og gefur skipuleggjanda framleiðslu verkfæri sem hámarkar og leiðréttir framleiðsluáætlunina fyrir vinnureitinn lean manufacturing.

## <a name="visual-scheduling-of-kanban-jobs"></a>Sýnileg röðun fyrir kanban-vinnslur
Kanban-vinnsla getur samanstaðið af einni eða mörgum kanban-vinnslum. Til eru tvær gerðir kanban-vinnsla:

-   Vinnsla
-   Flutningur

Aðeins er hægt að raða vinnslum af gerðinni **Keyra**. Kanban-vinnslan og eiginleikar hennar, eins og tími verkþáttar, er skilgreind í kanban framleiðsluflæðinu. Í kanban framleiðsluflæðinu er kanban vinnslan líka tengd við vinnureits. Daglega afkastageta vinnureits er reiknuð á grundvelli afkastagetu vinnureitar sem er stillt í tilfangahópnum. Hún er leiðrétt með daglegum vinnutíma í tengdu dagatali. Þegar kanban vinnslu er raðað hleður vinnslan afkastagetu vinnureitsins. Kanban-áætlunarborðið veitir eftirfarandi aðaleiginleika:

-   Myndrænt yfirlit yfir framleiðsluáætlunina í lean vinnurei. Þetta yfirlit sýnir áætlaðar kanban-ferlisvinnslur í skilgreindum tímabilum.
-   Verkfæri sem gerir kleift að raða óáætluðum kanban-vinnslum og endurraða áður áætluðum vinnslum.

## <a name="kanban-schedule-board"></a>Kanban-áætlunartafla
Síðan **Kanban-áætlunarborð** inniheldur sjö aðalatriði, eins og sýnt er í eftirfarandi dæmi. 

![Kanban-áætlunartafla.](./media/kanban-schedule-board-1024x554.png)
1.  Aðgerðasvæði
2.  Sía svæði
3.  Hnappur fyrir óvæntar vinnslur
4.  Tímabilshnútur
5.  Kanban-vinnsla
6.  Afkastagetustika
7.  Tímakvarði

### <a name="view-the-time-scale"></a>Skoða tímamælikvarðann

Borðinu er skipt upp í tímabil sem hvort um sig er sýnt sem hnútur (4). Tímabilshnútarnir eru skráðir á lóðrétta ásinn og lárétti ásinn táknar tímakvarða (7) sem sýnir lengd tímabilsins. Tímabil er með lengd einn dagur eða ein vika. Lengdin er ákvörðuð út frá skilgreiningu vinnureitsins sem valið er til fyrir Kanban tímabilið raða frítt um borð (2). Fyrir hvern hnút tímabils gefur Kanban-áætlunarborð til kynna hversu mikið kanban raðaðar vinnslur eru hleðslu tímabilsins. Einnig er vísbending um hámarks gegnumstreymi fyrir tímabilið. Ef áætlað gegnumstreymi fer fram úr hámarks gegnumstreymi, telst tímabilið vera ofhlaðið og rautt viðvörunarmerki birtist. Vinnsla áætlaða kanban birtist á tímabili sem er með áætlaða upphafs- og lokatíma (5). Lengd vinnslu jafngildir tíma verkþáttar. Kanban-vinnslur skarast á tímabili ef aðgerðartími þeirra fer yfir verktíma vinnuflokksins.

### <a name="view-job-status"></a>Skoða vinnslustöðuna

Nánari upplýsingar um vinnslu kanban eru tiltæk í ábendingum sem birtast þegar þú heldur bendlinum yfir vinnslu. Tákn gefur upplýsingar um stöðu vinnslunnar. Til dæmis bendir klukkutákn til þess að kanban-vinnslan sé komin á gjalddaga.

### <a name="use-colors-to-view-the-kanban-schedule-board"></a>Nota liti til að skoða Kanban-áætlunarborð

Til að auka yfirlitið sem Kanban-áætlunarborðið veitir er hægt að nota liti til að aðgreina kanban-vinnslur. Litur á kanban-vinnslum er skilgreindur í flokki í markvissri áætlanagerð, þar sem er hægt að steypa saman vörum sem á að framleiða í sömu röð. Hnappurinn **Nota þemaliti** á flipanum í **Borð** í Aðgerðarúðu gerir mögulegt að skipta á milli þemalita í forritinu og litanna sem eru skilgreindir í flokki í markvissri áætlanagerð. Fyrir hvert tímabil burðargetu strikamerkis (6) gefur til kynna hversu mörg eintök af tiltækar klukkustundir fyrir tímabilið hafa verið hlaðið kanban störf. Ef tímabilið er ofhlaðið birtist verður afkastastikan þykkari og rauð. Allar þessar aðgerðir eru mögulegar á á **frítt um Borð** flipa í Aðgerðarúðu (1) efst í **Kanban tilrauna fjöl** síðu.

## <a name="plan-unplanned-jobs"></a>Áætla óáætluð störf
Raða gert ráð fyrir óvæntum kanban störf í **Áætlun gert ráð fyrir óvæntum vinnslur** svarglugga. Til að opna svargluggann, smellið á **gert ráð fyrir Óvæntum vinnslur** hnapp sem sýnir núverandi vinnslufjölda gert ráð fyrir óvæntum. Einnig er hægt að smella á **Áætla óvæntar vinnslur** á flipanum **Borð** í Aðgerðarúðu. Svarglugginn sýnir lista af óvæntum kanban-vinnsum fyrir vinnureitinn. Hægt er að nota svæðið **Síu** til að sía öll svæði í töflunni. Til dæmis er hægt að sía eftir kanban-vinnslum fyrir ákveðna vöru. Eftir að síaða lista yfir vinnslur sem á að raða getur verið valið í listanum og smellið síðan á **í lagi**. Til að nota sjálfvirka áætlun til að raða vinnslum er stillt á **Sjálfgefna áætlunargerð** valkostinn að **Já**. Í þessu tilfelli er vinnslum raðað í tímabili eftir gjalddaga þeirra. Einnig er hægt að raða vinnslum eftir tímabilum. Veldu bara tímabilslykil á svæðinu **Tímabil**. Eftirfarandi skýringarmynd sýnir dæmi um svargluggann **Áætla óvæntar vinnslur**. 

![Svarglugginn Áætla óáætluð störf.](./media/plan-unplanned-jobs-1024x564.png)

## <a name="sequence-kanban-jobs-within-the-same-period"></a>Raða kanban-verk innan sama tímabils
Hægt er að breyta röðinni á einum eða fleiri valdar vinnslur innan tímabils. Þessi afkastageta getur verið gagnleg ef vilji er til þess að forgangsraða nokkur störf á tímabili. Einnig er hægt að raða vinnslum sem hafa sömu vörueigindir, til að hámarka vinnsluframkvæmd. Hægt er að breyta röð með því að draga og sleppa aðgerð eða með því að nota í **Aftur** og **Áfram** valmyndaratriðunum á flipanum **Borð** í Aðgerðarúðu.

## <a name="reassign-kanban-jobs-across-periods"></a>Endurúthluta kanban-vinnslum yfir tímabil
Hægt er að endurúthluta vinnslum frá einu tímabili til annars. Þessi afkastageta getur verið gagnleg ef tímabil er ofhlaðið og stig álagið á tímabilum sem hafa afkastagetu til skiptanna. Hægt er að endurúthluta vinnslum með því að draga og sleppa aðgerð eða með því að nota valmyndaratriðin **Næsta tímabil** og **Fyrra tímabil** á flipanum **Borð** í Aðgerðarúðu.

## <a name="open-the-kanban-schedule-board"></a>Opna kanban-áætlunartöfluna
Hægt er að opna Kanban-áætlunarborð með valmyndaratriði á eftirfarandi síðum:

-   Síðan **Framleiðslusvæði**
-   Síðan **Áætlun kanban-vinnslu**
-   Síðan **Gera framleiðsluflæði sýnilegt**


## <a name="additional-resources"></a>Frekari upplýsingar

[Röðun kanban-vinnslu fyrir lean-framleiðslu](lean-manufacturing-kanban-job-scheduling.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]