---
title: Ytri gögn í sjóðstreymisspám
description: Þetta efnisatriði lýsir uppsetningarskrefunum sem þarf að ljúka svo hægt sé að færa inn ytri gögn eða flytja inn í sjóðstreymisspár.
author: rcarlson
ms.date: 12/21/2021
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
ms.openlocfilehash: 66b097b2936e61c619d45ad103440eddbb983feb
ms.sourcegitcommit: c8dc60bb760553f166409c2e06dd2377f601c006
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/23/2021
ms.locfileid: "7945792"
---
# <a name="external-data-in-cash-flow-forecasts"></a>Ytri gögn í sjóðstreymisspám

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Ytri gögn er hægt að færa inn eða flytja inn í sjóðsstreymisspá. Þetta efnisatriði lýsir uppsetningarskrefunum sem eru sértæk fyrir notkun ytri gagna og sem gera kleift að taka ytri gögn með í sjóðsstreymisspá.

## <a name="external-data-setup"></a>Ytri gagnauppsetning

Nota **Ytri heimild** flipann á **Uppsetning sjóðstreymisspár** síða (**Handbært fé og bankastjórnun \> Sjóðstreymisspá \> Uppsetning sjóðstreymisspár**) til að slá inn stillingar sem styðja notkun ytri gagna í sjóðstreymisspám.

Ytri gögn er hægt að færa inn eða flytja inn í sjóðsstreymisspá. Áður en ytri gögn eru færð inn eða flutt inn verður að setja upp ytri heimildir. Á **Ytri heimild** flipa, setja upp ytri sjóðstreymisflokka. Flokkur getur verið annað hvort **Sendandi** eða **Komandi**. **Lausafjárstaða** ætti að vera valin sem færslugerð. Í **Stillingar lögaðila** grid, velja lögaðila og samsvarandi aðalreikninga sem ytra sjóðstreymisflokkar eiga við.

Fyrir frekari upplýsingar um hvernig á að setja upp sjóðstreymisspár, sjá [Sjóðstreymisspá](../cash-bank-management/cash-flow-forecasting.md).

## <a name="enter-external-data"></a>Sláðu inn ytri gögn

Til að slá inn og breyta ytri gögnum fyrir sjóðstreymisspár geturðu notað **Opnaðu í Excel** reynsla. Veldu **Ytri gögn** hnappinn á **Uppsetning sjóðstreymisspár** síðu og veldu síðan annað hvort **Bæta við ytri gögnum** eða **Breyttu fyrirliggjandi ytri gögnum**. Þegar Microsoft Excel-skráin er opnuð er hægt að færa inn upplýsingar í eftirfarandi reiti:

- **Inngangsauðkenni** (einstakt)
- **Lýsing** (valfrjálst)
- **Nafn ytri uppruna** – Veldu eitt af gildunum á listanum sem þú skilgreindir þegar þú settir upp Finance Insights.
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
