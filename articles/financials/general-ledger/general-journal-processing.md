---
title: "Vinnsla almennrar færslubókar"
description: "Þessi grein lýsir eiginleikum í Microsoft Dynamics 365 Finance and Operations, Enterprise útgáfu sem geta hjálpað við að gera vinnslu almennrar færslubókar auðveldari, sem og að tryggja að rétt gögn séu tekin og að innri stýring sé ekki í hættu."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 68da281cb4793ed83f70c68d061d327aa8a8c772
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="general-journal-processing"></a>Vinnsla almennrar færslubókar

[!include[banner](../includes/banner.md)]


Þessi grein lýsir eiginleikum í Microsoft Dynamics 365 Finance and Operations, Enterprise útgáfu sem geta hjálpað við að gera vinnslu almennrar færslubókar auðveldari, sem og að tryggja að rétt gögn séu tekin og að innri stýring sé ekki í hættu.  

Færslubókanöfn

Eitt af mikilvægustu sviðum til að setja upp eru heiti færslubókar. Góð hugmynd er að skilgreina ákveðin heiti færslubókar fyrir hvert málefni, eins og innan samstæðu, leiðrétting á uppsöfnun og villuleiðrétting. Hægt er að sníða hvert heiti færslubókar til að hjálpa við að gera gagnainnfærslu fyrir hvert málefni auðvelda og örugga. 

Á **færslubókarheiti** síðu er hægt að setja upp eftirfarandi einingar:

-   **Verkflæðissamþykkt** – til Að auka innri stýringu skal skilgreina færslubókarverkflæði sem koma á umfangsmiklum mörkum fyrir yfirferð og samþykktarskref, byggt á skilyrðum eins og heildar debetupphæð. Verkflæði fyrir almennar færslubækur eru sett upp á síunni **Verkflæði fyrir fjárhag**.
-   **Sjálfgildi** – Velja sjálfgildi fyrir mótlykill, gjaldmiðill, og fjárhagsvíddir.
-   **Færslubókareftirlit** – hægt er að setja upp takmarkanir á fyrirtæki og gerð lykils og einnig í hlutagildi. 

**Dæmi**

færslubókarheiti er hægt að nota fyrir leiðréttingar eingöngu. Í þessu tilfelli er hægt að tilgreina að aðeins **Fjárhags** lykilgerðin er gild fyrir öll fyrirtæki. [![Gerðir lykla fyrir færslubókareftirlit](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Hægt er að nota heiti færslubókar eingöngu fyrir tiltekinn hluta eða fyrir svið aðallykla. [![Hluti færslubókareftirlits](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

**Sjálfvirka bakfærslu** valkosturinn er tiltækur í almennar færslubækur. Til dæmis, er leiðrétting á uppsöfnun þar sem raunverulegur skjal hefur ekki enn verið unnin, eins og sýnt er í eftirfarandi skýringarmynd.
[![Almenn færslubók sem er bakfærð](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Microsoft Excel-innbót fyrir færslu í færslubók veitir meiri sjálfvirkni og auðveldar innfærslu gagna. **Opnar línur í Excel** aðgerð er tiltæk á í **Almennrar færslubókar** og **fylgiskjal** síður. 

Á **Tímabilsbækur** síða, geturðu sett upp endurteknar færslubækur í til að gera sjálfvirkt færslubókarferli. 

Hægt er að nota sniðmát fyrir fylgiskjöl hvenær sem er. Á síðunni **Almennar færslubækur** má finna aðgerðirnar **Vista** og **Velja sniðmát fylgiskjals** á síðunni **Færslubókarfylgiskjal** undir **Aðgerðir** fyrir línur fylgiskjals.

## <a name="related-setup"></a>Tengd uppsetning
Eftirfarandi uppsetningar er ekki bundinn við almennar færslubækur en hjálpar að tryggja samræmda gagnainnslætti sem er rétt og auðveld.

### <a name="main-account"></a>Aðallykill

Uppsetning aðallykils býður upp á marga valkosti fyrir úrvinnslu almennrar færslubókar:

-   **DC/KR krafa** – Notið þennan valkost ef aðallykil er takmarkaður við debet-eða kreditfærslur. Uppsetning er sannprófað þegar færslubók er villuleitað eða bókað.
-   **Sjálfgefinn mótlykill**
-   **Frestað** – Fresta aðallykil fyrir innslátt gagna í öllum fyrirtækjum eða fyrir tiltekin fyrirtæki/lögaðilaa.
-   **Ekki leyfa handvirkan innslátt** – koma í veg Fyrir að notendur fært inn gildi handvirkt fyrir lykilinn í færslubók.
-   **Sjálfgildur/villuleita gjaldmiðil**
-   **Hnekkja lögaðila** – Þessi uppsetning á sérstaklega við fyrirtæki/lögaðila:
    -   **sjálfgefnir/sannprófa VSK-flokka**
    -   **Sjálfgefin vídd** – **Ekki föst** eða **Föst gildi**. **Föst gildi** hjálpar að tryggja allar bókanir fyrir þennan aðallykil séu ávallt að nota víddargildið sem er sett upp sem **Fast**.
-   **Bókunarvilluleit**
    -   **Villuleit notanda** – valkosturinn stýrir því hvaða notendur hafa heimild til að bóka aðallykil.
    -   **Villuleit bókunargerðar** – valkosturinn stýrir því hvaða bókunargerð eru leyfðar fyrir aðallykil.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Bókhaldslykilskipulag og skipulag ítarlegra reglna

Bókhaldsskipulag og skipulag ítarlegra reglna er mjög mikilvægt fyrir að tryggja gögn sem þarf fyrir fjárhagslega skýrslugerð og afkastarakningu er sótt við úrvinnslu almennrar færslubókar og allra fylgiskjala. Bókhaldslykilskipulag og skipulag ítarlegra reglna leyfa þér að klæðskerasníða upplifun af gagnainnslætti. Hægt er að leyfa innslátt gagna aðeins fyrir fjárhagsvíddir sem eiga við hverja aðstæðu, og getur framfylgt þeirri kröfu að áskilin og rétt gögn séu ávallt sótt.

Frekari upplýsingar er hægt að finna í eftirfarandi efni:
- [Áætlanagerð: bókhaldslykilsins](plan-chart-of-accounts.md). 
- [Stofna ítarlegar reglur fyrir færslubækur](tasks/create-advanced-rules-journals.md)
- [Stofna færslu í færslubók með því að nota sniðmát](tasks/create-journal-entry-template.md)
- [Stofna og sannprófa færslubækur](tasks/create-validate-journals.md)
- [Bóka tímabilsbækur](tasks/post-periodic-journals.md)
- [Vinna úr færslubók kostnaðarúthlutunar](tasks/process-ledger-allocation-journal.md)



