---
title: Nota ytri gögn við sjóðsstreymisspár (forskoðun)
description: Þetta efnisatriði lýsir uppsetningarskrefunum sem þarf að ljúka til að hægt sé að færa ytri gögn inn eða flytja það inn í sjóðstreymisspár.
author: rcarlson
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: b728314f4c4e18543e4f3b75fe1e7dcddc448ea0
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638537"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a>Nota ytri gögn við sjóðsstreymisspár (forskoðun)

[!include [banner](../includes/banner.md)]

Ytri gögn er hægt að færa inn eða flytja inn í sjóðsstreymisspá. Þetta efnisatriði lýsir uppsetningarskrefunum sem eru sértæk fyrir notkun ytri gagna og sem gera kleift að taka ytri gögn með í sjóðsstreymisspá.

## <a name="external-data-setup"></a>Ytri gagnauppsetning

Notaðu flipann **Ytri uppruni** á **uppsetning sjóðstreymisspár** síðu (**reiðufjár-og bankastjórnun \> sjóðsstreymisspá**) til að færa inn stillingar sem styðja notkun ytri gagna í sjóðsstreymisspá.

Frekari upplýsingar um uppsetninguna er að finna í [Sjóðstreymisspár´](../cash-bank-management/cash-flow-forecasting.md).

Til að færa inn ytri gögn fyrir sjóðsstreymisspár er hægt að nota Opna í Excel til að færa inn og breyta ytri gögnum. Velja skal hnappinn **Ytri gögn** og velja síðan annað hvort **bæta við ytri gögnum** eða **breyta fyrirliggjandi ytri gögnum**. Þegar Microsoft Excel-skráin er opnuð er hægt að færa inn upplýsingar í eftirfarandi reiti:

- **Færslukenni**
- **Lýsing** (valfrjálst)
- **Heiti ytri uppruna** – Velja skal eitt af gildunum á listanum sem voru skilgreindir þegar fjármálainnsýn var sett upp.
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
