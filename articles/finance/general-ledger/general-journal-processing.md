---
title: Vinnsla almennrar færslubókar
description: Þetta efnisatriði lýsir eiginleikum í Microsoft Dynamics 365 Finance sem geta hjálpað við að gera vinnslu almennrar færslubókar auðveldari, sem og að tryggja að rétt gögn séu tekin og að innri stýring sé ekki í hættu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2becf8213cfa46e2c0cf0c553f0b5e503dfc3704
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570241"
---
# <a name="general-journal-processing"></a>Vinnsla almennrar færslubókar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir eiginleikum sem geta hjálpað við að gera vinnslu almennrar færslubókar auðveldari, sem og að tryggja að rétt gögn séu tekin og að innri stýring sé ekki í hættu.  

## <a name="journal-names"></a>Færslubókanöfn

Eitt af mikilvægustu sviðum til að setja upp eru heiti færslubókar. Góð hugmynd er að skilgreina ákveðin heiti færslubókar fyrir hvert málefni, eins og innan samstæðu, leiðrétting á uppsöfnun og villuleiðrétting. Hægt er að sníða hvert heiti færslubókar til að hjálpa við að gera gagnainnfærslu fyrir hvert málefni auðvelda og örugga. 

Á **færslubókarheiti** síðu er hægt að setja upp eftirfarandi einingar:

-   **Verkflæðissamþykkt** – til Að auka innri stýringu skal skilgreina færslubókarverkflæði sem koma á umfangsmiklum mörkum fyrir yfirferð og samþykktarskref, byggt á skilyrðum eins og heildar debetupphæð. Setja upp verkflæði fyrir almennar færslubækur á í **verkflæði fyrir fjárhag** síðu.
-   **Sjálfgildi** – Velja sjálfgildi fyrir mótlykill, gjaldmiðill, og fjárhagsvíddir.
-   **Færslubókareftirlit** – hægt er að setja upp takmarkanir á fyrirtæki og gerð lykils og einnig í hlutagildi. 

**Dæmi**

færslubókarheiti er hægt að nota fyrir leiðréttingar eingöngu. Í þessu tilfelli er hægt að tilgreina að aðeins **Fjárhags** lykilgerðin er gild fyrir öll fyrirtæki. 

[![Gerðir lykla fyrir færslubókareftirlit](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Hægt er að nota heiti færslubókar eingöngu fyrir tiltekinn hluta eða fyrir svið aðallykla. 

[![Hluti færslubókareftirlits](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

**Sjálfvirka bakfærslu** valkosturinn er tiltækur í almennar færslubækur. Til dæmis, er leiðrétting á uppsöfnun þar sem raunverulegur skjal hefur ekki enn verið unnin, eins og sýnt er í eftirfarandi skýringarmynd.
[![Almenn færslubók sem er bakfærð](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Microsoft Excel innbót fyrir færslu í færslubók veitir meiri sjálfvirkni og auðveldar innfærslu gagna. **Opnar línur í Excel** aðgerð er tiltæk á í **Almennrar færslubókar** og **fylgiskjal** síður. 

Á **Tímabilsbækur** síða, geturðu sett upp endurteknar færslubækur í til að gera sjálfvirkt færslubókarferli. 

Hægt er að nota sniðmát fyrir fylgiskjöl hvenær sem er. Á síðunni **Almennar færslubækur** má finna aðgerðirnar **Vista** og **Velja sniðmát fylgiskjals** á síðunni **Færslubókarfylgiskjal** undir **Aðgerðir** fyrir línur fylgiskjals.

## <a name="related-setup"></a>Tengd uppsetning
Eftirfarandi uppsetning er ekki bundinn við almennar færslubækur en hjálpar að tryggja gagnainnslætti sem eru réttir og auðveldir.

### <a name="main-account"></a>Aðallykill

Uppsetning aðallykils býður upp á marga valkosti fyrir úrvinnslu almennrar færslubókar:

-   **DC/KR krafa** – Notið þennan valkost ef aðallykil er takmarkaður við debet-eða kreditfærslur. Uppsetning er sannprófað þegar færslubók er villuleitað eða bókað.

-   **Sjálfgefinn mótlykill**
-   **Frestað** – Fresta aðallykil fyrir innslátt gagna í öllum fyrirtækjum eða fyrir tiltekin fyrirtæki/lögaðila.
-   **Ekki leyfa handvirkan innslátt** – koma í veg Fyrir að notendur fært inn gildi handvirkt fyrir lykilinn í færslubók.
-   **Sjálfgildur/villuleita gjaldmiðil**
-   **Hnekkja lögaðila** – Þessi uppsetning á sérstaklega við fyrirtæki/lögaðila:
    -   **sjálfgefnir/sannprófa VSK-flokka**
    -   **Sjálfgefin vídd** – **Ekki föst** eða **Föst gildi**. **Föst gildi** hjálpar að tryggja allar bókanir fyrir þennan aðallykil séu ávallt að nota víddargildið sem er sett upp sem **Fast**.
-   **Bókunarvilluleit**
    -   **Villuleit notanda** – valkosturinn stýrir því hvaða notendur hafa heimild til að bóka aðallykil.
    -   **Villuleit bókunargerðar** – valkosturinn stýrir því hvaða bókunargerð eru leyfðar fyrir aðallykil.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Bókhaldslykilskipulag og skipulag ítarlegra reglna

Bókhaldsskipulag og skipulag ítarlegra reglna er mjög mikilvægt til að tryggja gögn sem þarf fyrir fjárhagslega skýrslugerð og afkastarakningu er sótt við úrvinnslu almennrar færslubókar og allra fylgiskjala. Bókhaldslykilskipulag og skipulag ítarlegra reglna leyfa þér að klæðskerasníða upplifun af gagnainnslætti. Hægt er að leyfa gagnaskráningu aðeins fyrir fjárhagsvíddir sem eiga við í hverjum aðstæðum fyrir sig, og sem getur framfylgt þeirri kröfu að áskilin og rétt gögn séu ávallt sótt.

Frekari upplýsingar er hægt að finna í eftirfarandi efni:
- [Áætlanagerð: bókhaldslykilsins](plan-chart-of-accounts.md). 
- [Stofna ítarlegar reglur fyrir færslubækur](tasks/create-advanced-rules-journals.md)
- [Stofna færslu í færslubók með því að nota sniðmát](tasks/create-journal-entry-template.md)
- [Stofna og sannprófa færslubækur](tasks/create-validate-journals.md)
- [Bóka tímabilsbækur](tasks/post-periodic-journals.md)
- [Vinna úr færslubók kostnaðarúthlutunar](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a>Herma eftir bókun
Þú getur fundið **Herma eftir bókun** í valmyndinni **Sannprófa** fyrir flestar færslubækur. Þegar þú sannprófar færslubók með aðgerðinni **Sannprófa** prófar kerfið færslubókina í ákveðnum villuskilyrðum. Ef þú notar aðgerðina **Herma eftir bókun** keyrir kerfið öll sömu ferlin sem eru keyrð við bókun án þess að bóka færslubókina. Þú getur síðan farið yfir skilaboðin sem birtast, lagað allar villur sem þú finnur og opnað síðan á valmyndina **Bóka** til að bóka færslubókina. 

**Herma eftir bókun** er ekki í boði fyrir runuvinnslu. Hins vegar er kóði í boði til að herma eftir bókun í runu og þróunaraðilar geta aukið við kóðann til að bæta þessari virkni við.  

## <a name="journal-unlock"></a>Aflæsing færslubókar
Hnappur er til á færslubókarsíðunni til að opna færslubók sem hefur stöðuna „læst af kerfinu“ stillt á Já. Þessari aflæsingu er hægt að framkvæma af kerfisstjóra sem hefur greint hvaða framkvæmd hópastörf og staðfest að þessi færslubók er ekki lengur unnin af runuvinnslu. Þessi hnappur virkjast með aðgerðinni sem heitir **Hnappur til að aflæsa færslubók** á síðunni **Stjórnun eiginleika**. 

## <a name="workflow-recall"></a>Afturköllun verkflæðis 
Geta til að rifja upp dagbók í verkflæði sem hefur stöðuna „óendurheimtanleg“ er virk með því að nota hnappinn **Verkflæði** í dagbók og á síðunni **Verkflæðissaga**. Þetta er gert kleift með aðgerðinni sem heitir **Endurstilling á verkflæðisstöðu fyrir færslubækur** á síðunni **Stjórnun eiginleika**.

## <a name="delete-journal-lines"></a>Eyða færslubókarlínum
Getan til að eyða öllum dagbókarlínum hratt er virk í dagbók undir **Aðgerðir** > **Eyða færslubókalínum**. Til að virkja þennan eiginleika, á **Stjórnun eiginleika** skaltu velja **Eyða afkastafínstillingu færslubókar**.
