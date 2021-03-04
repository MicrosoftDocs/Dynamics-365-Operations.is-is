---
title: Yfirlit yfir bókhaldslykil
description: Þessi efnisatriði veita upplýsingar sem hjálpa til við að áætla bókhaldslykla fyrir fyrirtækið.
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 007b634c18ce897160aea38e05c9a73a64dd3917
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444461"
---
# <a name="plan-your-chart-of-accounts"></a>Yfirlit yfir bókhaldslykil

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar sem hjálpa til við að áætla bókhaldslykla fyrir fyrirtækið.

Til að rekja og vinna með fjárhagslegar upplýsingar í fyrirtæki er hægt að setja upp bókhaldslykil bókhaldslykil er safn af lyklum sem skilgreina fjárhagsramma. Til að rekja enn frekar færslurnar í þessum lyklum er hægt að bæta við hluta. Þessir hlutar eru þekktir sem fjárhagsvíddir. Til dæmis gæti kostnaðarlykil hafa fjárhagsvíddir með heitinu Deild, kostnaðarstað og tilgang. Notandaskilgreindar reglur ákvarða hvernig þessar fjárhagsvíddir eru tengdar við aðallykla og aðrar fjárhagsvíddir og hvernig hægt að færa inn færslur. Þessar notandaskilgreindu reglur eru þekktar sem lykilskipulag og ítarlegar reglur.

Bókhaldslykillinn er skipulagður listi yfir fjárhagslykla lögaðila. Listinn er notaður til að útbúa fjárhagsskýrslur fyrir yfirvöld og eigendur. Lyklarnir eru fyrst flokkaðir eftir gerðum þeirra og síðan lagðir saman í stærri tegundir. Á almennasta stiginu eru lyklar flokkaðir sem tekjur og kostnaður (rekstrarlykill) og eignir og skuldbindingar (stöðulykill).

Bókhaldslykla getur verið samnýtt og notuð af hvaða lögaðila sem er í fyrirtæki. Bókhaldslyklar sem eru notaðir hjá lögaðila eru skilgreindir á síðunni **Fjárhagur**.

Nokkra þætti þarf að hafa í huga þegar skipulag bókhaldslykla er ákveðið fyrir fyrirtækið, þar á meðal:

- Skýrslukrafa lands eða svæðis þar sem fyrirtæki þitt er staðsett
- Tilkynningarskyldur við lögaðila
- Sérhæfingarstig sem þörf er á, bæði fyrir ytri fyrirtæki og þitt fyrirtæki.

Þú stofnar bókhaldslykil á síðunni **Bókhaldslykill**. Þú getur búið til aðallykla á síðunni **Bókhaldslykill** eða á síðunni **Aðallyklar**. Aðallyklar þínir ættu ekki að nota sérstafi sem eru notaðar sem skiltákn bókhaldslykils. Annars gætir þú fundið fyrir óstöðugleika, eða þú gætir þurft að nota uppflettingar eða svarglugga þegar þú slærð inn samsetningar lykla og vídda. Nánari upplýsingar sjá [Stofna aðallykil](tasks/create-main-account.md).

> [!NOTE]
> Í Dynamics 365 for Finance and Operations útgáfu 8.0 (apríl 2018) er hægt að breyta skiltákni bókhaldslykils á síðunni **Færibreytur fjárhags**.

Það er góð hugmynd að tengja við aðallykla tegundir aðallykils þannig er hægt nýta sjálfgefna fjárhagsskýrslur án þess að þurfa að gera neinar breytingar. Þess vegna er hægt að hanna og viðhalda skýrslur á fljótari og auðveldari hátt.

Þú stofnar lykilskipulag á síðunni **Skilgreina lykilskipulag**. Lykilskipulag tilgreina gildar samsetningar. Þessar samsetningar, ásamt aðallyklum, mynda bókhaldslykla. Nánari upplýsingar sjá [Stofna lykilsskipulag](tasks/create-account-structures.md).

**Lögaðili hnekkir**

Ekki eru allir aðallyklar gildir fyrir alla lögaðila og sumir aðallyklar kunna aðeins að eiga við um ákveðið tímabil. Í þessari atburðarás getur þú notað kaflann **Hnekkingar lögaðila** til að bera kennsl á fyrirtækin sem aðallykillinn ætti að vera lokaður fyrir, eigandinn og tímabilið þegar víddin er virk. Hnekkingar á samnýttu stigi mega ekki vera meira takmarkandi en hnekkingar á stigi lögaðila.

Frekari upplýsingar er hægt að finna í eftirfarandi efni:

- [Fjárhagsvíddir](financial-dimensions.md)
- [Stofna og úthluta ítarlegu regluskipulagi](tasks/create-assign-advanced-rule-structures.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]