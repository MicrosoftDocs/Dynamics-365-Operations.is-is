---
title: Ytri gögn í sjóðsstreymisspám
description: Þessi grein lýsir uppsetningarskrefunum sem þarf að ljúka til að hægt sé að færa ytri gögn inn eða flytja það inn í sjóðstreymisspár.
author: RyanCCarlson2
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f0cb05770dc2fbd4e13af261b5f0a0e117a2f6d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846974"
---
# <a name="external-data-in-cash-flow-forecasts"></a>Ytri gögn í sjóðsstreymisspám

[!include [banner](../includes/banner.md)]

Ytri gögn er hægt að færa inn eða flytja inn í sjóðsstreymisspá. Þessi grein lýsir uppsetningarskrefunum sem eru sértæk fyrir notkun ytri gagna og sem gera kleift að taka ytri gögn með í sjóðsstreymisspá.

## <a name="external-data-setup"></a>Ytri gagnauppsetning

Notaðu flipann **Ytri uppruni** á **uppsetning sjóðstreymisspár** síðu (**reiðufjár-og bankastjórnun \> sjóðsstreymisspá\>Uppsetning sjóðsstreymisspár**) til að færa inn stillingar sem styðja notkun ytri gagna í sjóðsstreymisspá.

Ytri gögn er hægt að færa inn eða flytja inn í sjóðsstreymisspá. Áður en ytri gögn eru slegin inn eða flutt inn verður að setja upp ytri uppsprettur. Á flipanum **Ytri uppruni**, setjið upp utanaðkomandi sjóðstreymisflokka. Flokkur getur annað hvort verið **Á útleið** eða **Á innleið**. **Greiðslugeta** ætti að vera valin sem bókunargerð. Í töfluna **Stillingar lögaðila** skal velja lögaðila og samsvarandi aðallykla sem utanaðkomandi sjóðstreymisflokkar eiga við.

Nánari upplýsingar um hvernig setja skuli upp sjóðstreymisspá eru að finna í [Sjóðstreymisspá](../cash-bank-management/cash-flow-forecasting.md).

## <a name="enter-external-data"></a>Bæta við ytri gögnum

Til að færa inn og breyta ytri gögnum fyrir sjóðsstreymisspár er hægt að nota **Opna í Excel**. Velja skal hnappinn **Ytri gögn** á **Sjóðstreymisspá** síðu vinnusvæðis og svo annað hvort **Bæta við ytri gögnum** eða **Breyta fyrirliggjandi ytri gögnum**. Þegar Microsoft Excel-skráin er opnuð er hægt að færa inn upplýsingar í eftirfarandi reiti:

- **Kenni færslu** (einkvæmt)
- **Lýsing** (valfrjálst)
- **Heiti ytri uppruna** – Velja skal eitt af gildunum á listanum sem voru skilgreindir þegar Finance Insights var sett upp.
- **Lögaðili**
- **Dagsetning**
- **Upphæð í gjaldmiðli færslu**
- **Gjaldmiðilskóði**
- **Sjálfgefin vídd** (valfrjálst)
- **Skjalanúmer** (valfrjálst)
- **Reikningsnúmer** (valfrjálst)
- **Reikningsheiti** (valfrjálst)

## <a name="importing-external-data-by-using-the-data-management-framework"></a>Flytur inn ytri gögn með því að nota rammann Stjórnun gagna

Hægt er að flytja inn ytri gögn fyrir sjóðsstreymisspá með því að nota vinnusvæðið **Gagnastjórnun** og eininguna sem er nefnd **Færsla ytri uppruna sjóðstreymisspár**.

Til viðbótar, ef nauðsynlegt er að setja uppsetningargögn úr einu umhverfi í annað, verða eftirfarandi einingar til staðar fyrir uppsetningartöflurnar sem krafist er:

- Uppsetning ytri uppruna sjóðstreymisspár
- Lögaðilauppsetning ytri uppruna sjóðstreymisspár

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
