---
title: "Áætlun bókhaldslykila"
description: "Þessi skrá upplýsingar sem hjálpa þér áætla bókhaldslykla fyrir fyrirtæki þitt."
author: aprilolson
manager: AnnBe
ms.date: 01/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ad55dd57483de4351c8501c5e226180fc73606aa
ms.openlocfilehash: 3d2cdeaf2fdeb2f587f82c97249886fb8db49154
ms.contentlocale: is-is
ms.lasthandoff: 01/11/2018

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

Stofnaðu bókhaldslykil í **Bókhaldslykill** síðu. Hægt er að stofna aðallykla úr  **Bókhaldslykil** síðu eða **aðallykla** síðu. aðallyklar þínir ættu ekki að nota sérstaka stafi sem eru notaðar sem skiltákn bókhaldslykils. Ef sérstaf er hjá þér sem er sú sama og við skiltákn bókhaldslykils, gæti orðið óstöðugleiki, eða þörf á til að nota alltaf uppflettingar eða hliðarglugga þegar verið er að færa inn reikning eða samsetningar víddar. Nánari upplýsingar sjá [Stofna aðallykil](tasks/create-main-account.md).


Það er góð hugmynd að tengja við aðallykla tegundir aðallykils þannig er hægt nýta sjálfgefna fjárhagsskýrslur án þess að þurfa að gera neinar breytingar. Þess vegna er hægt að hanna og viðhalda skýrslur á fljótari og auðveldari hátt. 

Notið síðunni **Skilgreina lykilskipulag** til að skilgreina lykilskipulag. Lykilskipulag tilgreina gildar samsetningar. Samsetningar með aðallykla, skjámyndinni bókhaldslykla.  Nánari upplýsingar sjá [Stofna lykilsskipulag](tasks/create-account-structures.md).

**Lögaðili hnekkir** 

Ekki eru allir aðallyklar gildir fyrir alla lögaðila og sumir kunna aðeins að eiga við um ákveðið tímabil. Í þessum aðstæðum Lögaðili hnekkir getur verið notað til að auðkenna hvaða fyrirtæki ætti ekki að nota aðallykil fyrir, hver er eigandi og tímabilið sem víddin er virk. Hnekkingar á samnýttu stigi má ekki vera meira takmarkandi en hnekking á stigi lögaðila.

Nánari upplýsingar eru í eftirfarandi efnisatriðum: [Fjárhagsvíddir](financial-dimensions.md)
[Stofna og úthluta skipulagi um ítarlegar reglur](tasks/create-assign-advanced-rule-structures.md)




