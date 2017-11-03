---
title: "Áætlun bókhaldslykila"
description: "Þessi skrá upplýsingar sem hjálpa þér áætla bókhaldslykla fyrir fyrirtæki þitt."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 848da7ec8f4a7915f3b78945b808b564f4510434
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="plan-your-chart-of-accounts"></a>Áætlun bókhaldslykila

[!include[banner](../includes/banner.md)]


Þessi skrá upplýsingar sem hjálpa þér áætla bókhaldslykla fyrir fyrirtæki þitt.

Til að rekja og vinna með fjárhagslegar upplýsingar í fyrirtæki er hægt að setja upp bókhaldslykil bókhaldslykil er safn af lyklum sem skilgreina fjárhagsramma. Til að rekja frekar færslurnar í þessara lykla er hlutum, sem kallast fjárhagsvíddir, bætt við aðallyklana. Til dæmis gæti kostnaðarlykil hafa fjárhagsvíddir með heitinu Deild, kostnaðarstað og tilgang. Notandaskilgreind reglur, sem kallast ítarlegar reglur, ákvarða hvernig þessar fjárhagsvíddir eru tengdar við aðallykla og aðrar fjárhagsvíddir og hvernig hægt að færa inn færslur saman. 

Bókhaldslykillinn er skipulagður listi yfir fjárhagslykla lögaðila. Listinn er notaður til að útbúa fjárhagsskýrslur fyrir yfirvöld og eigendur. Lyklarnir eru flokkaðir eftir gerðum og síðan lagðir saman í stærri tegundir. Á almennasta stiginu eru lyklar flokkaðir sem tekjur og kostnaður (rekstrarlykill) og eignir og skuldbindingar (stöðulykill). 

Bókhaldslykla getur verið samnýtt og notuð af hvaða lögaðila sem er í fyrirtæki. Bókhaldslyklar sem eru notaðir hjá lögaðila eru skilgreindir á síðunni **Fjárhagur**. 

Nokkra þætti þarf að hafa í huga þegar skipulag bókhaldslykla er ákveðið fyrir fyrirtækið, þar á meðal:

-   skýrslukrafa lands/svæðis þar sem fyrirtæki þitt er staðsett.
-   Tilkynningarskyldur við lögaðila
-   Sérhæfingarstig sem þörf er á, bæði fyrir ytri fyrirtæki og þitt fyrirtæki.

Stofnaðu bókhaldslykil í **Bókhaldslykill** síðu. Hægt er að stofna aðallykla úr  **Bókhaldslykil** síðu eða **aðallykla** síðu. aðallyklar þínir ættu ekki að nota sérstaka stafi sem eru notaðar sem skiltákn bókhaldslykils. Ef sérstaf er hjá þér sem er sú sama og við skiltákn bókhaldslykils, gæti orðið óstöðugleiki, eða þörf á til að nota alltaf uppflettingar eða hliðarglugga þegar verið er að færa inn reikning eða samsetningar víddar. Nánari upplýsingar sjá [Stofna aðallykil](tasks/create-account-structures.md).


Það er góð hugmynd að tengja við aðallykla tegundir aðallykils þannig er hægt nýta sjálfgefna fjárhagsskýrslur án þess að þurfa að gera neinar breytingar. Þess vegna er hægt að hanna og viðhalda skýrslur á fljótari og auðveldari hátt. 

Notið síðunni **Skilgreina lykilskipulag** til að skilgreina lykilskipulag. Lykilskipulag tilgreina gildar samsetningar. Samsetningar með aðallykla, skjámyndinni bókhaldslykla.  Nánari upplýsingar sjá [Stofna lykilsskipulag](tasks/create-main-account.md).

**Lögaðili hnekkir** 

Ekki eru allir aðallyklar gildir fyrir alla lögaðila og sumir kunna aðeins að eiga við um ákveðið tímabil. Í þessum aðstæðum Lögaðili hnekkir getur verið notað til að auðkenna hvaða fyrirtæki ætti ekki að nota aðallykil fyrir, hver er eigandi og tímabilið sem víddin er virk. Hnekkingar á samnýttu stigi má ekki vera meira takmarkandi en hnekking á stigi lögaðila.

Nánari upplýsingar eru í eftirfarandi efnisatriðum: [Fjárhagsvíddir](financial-dimensions.md)
[Stofna og úthluta skipulagi um ítarlegar reglur](tasks/create-assign-advanced-rule-structures.md)




