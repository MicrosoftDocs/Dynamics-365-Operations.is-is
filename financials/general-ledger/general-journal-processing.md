---
title: "Vinnsla almennrar færslubókar"
description: "Þessi greinum lýsir getu í Microsoft Dynamics 365 fyrir Aðgerðir sem geta hjálpað til við gera almennrar færslubókar vinnslu auðvelda og sem einnig auðvelda tryggja samræmda réttu gögnin eru sótt og innra eftirlitið er ekki öryggi í hættu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 50cd203025be8857de943e458fc32315e494fb7a
ms.lasthandoff: 03/31/2017


---

# <a name="general-journal-processing"></a>Vinnsla almennrar færslubókar

Þessar greinar lýsir getu í Microsoft Dynamics AX sem geta hjálpað að gera vinnslu almennrar færslubókar auðveldara, og það getur einnig hjálpað að tryggja að rétt gögn er tekin og innra eftirlit er ekki í hættu.  

Færslubókanöfn

Ein mikilvægasta svæðum til að setja upp er færslubókarheiti. Er góð hugmynd að skilgreina tiltekin færslubókarnöfn fyrir hvert málefni innan samstæðu, leiðrétting á uppsöfnuðum og leiðrétta. Ekki er hægt að sníða hvert færslubókarheiti til að gera gagnainnfærslu fyrir hvert málefni auðveld og öryggi. 

Á **færslubókarheiti** síðu er hægt að setja upp eftirfarandi einingar:

-   **Verkflæðissamþykkt** – til Að auka innri stýringu skal skilgreina færslubókarverkflæði sem koma á umfangsmiklum mörkum fyrir yfirferð og samþykktarskref, byggt á skilyrðum eins og heildar debetupphæð. Setja upp verkflæði fyrir almennar færslubækur á í ** fjárhags verkflæði ** síðu.
-   **Sjálfgildi** – Velja sjálfgildi fyrir mótlykill, gjaldmiðill, og fjárhagsvíddir.
-   **Færslubókareftirlit** – hægt er að setja upp takmarkanir á fyrirtæki og gerð lykils og einnig í hlutagildi. 

**Dæmi**

færslubókarheiti er hægt að nota fyrir leiðréttingar eingöngu. Í þessu tilfelli er hægt að tilgreina að aðeins **Fjárhags** lykilgerðin er gild fyrir öll fyrirtæki. [![Færslubók stýringargerðir](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Hægt er að nota heiti færslubókar eingöngu fyrir tiltekinn hluta eða fyrir svið aðallykla. [![Færslubókar eftirlit hluta](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

**Sjálfvirka bakfærslu** valkosturinn er tiltækur í almennar færslubækur. Til dæmis, er leiðrétting á uppsöfnun þar sem raunverulegur skjal hefur ekki enn verið unnin, eins og sýnt er í eftirfarandi skýringarmynd.
[![Bakfæra almennrar færslubókar](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Veitir viðbætarstigi sjálfvirkni og gerir auðveldar fyrir innslátt gagna í Microsoft Excel innbót fyrir færslu í færslubók. **Opnar línur í Excel **aðgerð er tiltæk á í **Almennrar færslubókar** og **fylgiskjal** síður. 

Á **Tímabilsbækur** síða, geturðu sett upp endurteknar færslubækur í til að gera sjálfvirkt færslubókarferli. 

Hægt er að nota fylgiskjalssniðmát hvenær. Á á **Almennar færslubækur** síðu á **Vista** og **Veljið fylgiskjalssniðmát** aðgerðir er að finna á í **fylgiskjal** síðuna undir **Aðgerðir** fyrir fylgiskjalslínurnar.

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

Nánari upplýsingar, sjá [Áætlanagerðar: Bókhaldslykil](plan-chart-of-accounts.md). 


