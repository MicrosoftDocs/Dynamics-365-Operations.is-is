---
title: "Áætla bókhaldslykla"
description: "Þessi skrá upplýsingar sem hjálpa þér áætla bókhaldslykla fyrir fyrirtæki þitt."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 34425ecd4b78a134c92a2282576d0d7967d870b3
ms.lasthandoff: 03/31/2017


---

# <a name="plan-your-chart-of-accounts"></a>Áætla bókhaldslykla

Þessi skrá upplýsingar sem hjálpa þér áætla bókhaldslykla fyrir fyrirtæki þitt.

Til að rekja og vinna með fjárhagslegar upplýsingar í fyrirtæki er hægt að setja upp bókhaldslykil bókhaldslykil er safn af lyklum sem skilgreina fjárhagsramma. Til að rekja frekar færslurnar í þessara lykla er hlutum, sem kallast fjárhagsvíddir, bætt við aðallyklana. Til dæmis gæti kostnaðarlykil hafa fjárhagsvíddir með heitinu Deild, kostnaðarstað og tilgang. Notandaskilgreind reglur, sem kallast ítarlegar reglur, ákvarða hvernig þessar fjárhagsvíddir eru tengdar við aðallykla og aðrar fjárhagsvíddir og hvernig hægt að færa inn færslur saman. 

Bókhaldslykillinn er skipulagður listi yfir fjárhagslykla lögaðila. Listinn er notaður til að útbúa fjárhagsskýrslur fyrir yfirvöld og eigendur. Lyklarnir eru flokkaðir eftir gerðum og síðan lagðir saman í stærri tegundir. Á almennasta stiginu eru lyklar flokkaðir sem tekjur og kostnaður (rekstrarlykill) og eignir og skuldbindingar (stöðulykill). 

Bókhaldslykla getur verið samnýtt og notuð af hvaða lögaðila sem er í fyrirtæki. Skilgreint er í bókhaldslyklum sem notað er hjá lögaðila á **Fjárhag** síðu. 

Nokkra þætti þarf að hafa í huga þegar skipulag bókhaldslykla er ákveðið fyrir fyrirtækið, þar á meðal:

-   skýrslukrafa lands/svæðis þar sem fyrirtæki þitt er staðsett.
-   Tilkynningarskyldur við lögaðila
-   Sérhæfingarstig sem þörf er á, bæði fyrir ytri fyrirtæki og þitt fyrirtæki.

Stofnaðu bókhaldslykil í **Bókhaldslykill ** síðu. Hægt er að stofna aðallykla úr  **Bókhaldslykil** síðu eða **aðallykla** síðu. aðallyklar þínir ættu ekki að nota sérstaka stafi sem eru notaðar sem skiltákn bókhaldslykils. Ef sérstaf er hjá þér sem er sú sama og við skiltákn bókhaldslykils, gæti orðið óstöðugleiki, eða þörf á til að nota alltaf uppflettingar eða hliðarglugga þegar verið er að færa inn reikning eða samsetningar víddar. 

Það er góð hugmynd að tengja við aðallykla tegundir aðallykils þannig er hægt nýta sjálfgefna fjárhagsskýrslur án þess að þurfa að gera neinar breytingar. Þess vegna er hægt að hanna og viðhalda skýrslur á fljótari og auðveldari hátt. 

Notið síðunni **Skilgreina lykilskipulag ** til að skilgreina lykilskipulag. Lykilskipulag tilgreina gildar samsetningar. Samsetningar með aðallykla, skjámyndinni bókhaldslykla. 

**Legal entity overrides** 

Ekki allar aðallykla gilda fyrir alla lögaðila og sumar má aðeins vera máli fyrir ákveðið tímabil. Í þessum aðstæðum Lögaðili hnekkir getur verið notað til að auðkenna hvaða fyrirtæki ætti ekki að nota aðallykil fyrir, hver er eigandi og tímabilið sem víddin er virk. Hnekkingar á samnýttu stigi má ekki vera meira takmarkandi en hnekking á stigi lögaðila.

Nánari upplýsingar, sjá [fjárhagsvíddir](financial-dimensions.md).


