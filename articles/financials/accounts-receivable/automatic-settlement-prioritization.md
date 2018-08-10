---
title: "Sjálfvirkt uppgjör og forgangsröðun"
description: "Þetta efnisatriði lýsir því hvernig færslur eru jafnaðar ef valið er Sjálfvirkt uppgjör á síðunni Færibreytur viðskiptakrafna. Hún útskýrir einnig hvernig hægt er að nota sjálfvirkt uppgjör í samsetningu með greiðsluforgangi."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14531
ms.assetid: e7837cf6-ec69-44b4-8d47-eba38d5c7b1f
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: fc091e401f84ce2ac425897ad6cbd92fd7399736
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="automatic-settlement-and-prioritization"></a>Sjálfvirkt uppgjör og forgangsröðun

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig færslur eru jafnaðar ef valið er Sjálfvirkt uppgjör á síðunni Færibreytur viðskiptakrafna. Hún útskýrir einnig hvernig hægt er að nota sjálfvirkt uppgjör í samsetningu með greiðsluforgangi.

Tveir valkostir hafa þegar greiðslur með reikninga og aðrar færslur jafnaður. Hægt er að velja færslur til jöfnunar handvirkt eða Microsoft Dynamics 365 for Finance and Operations getur valið færslurnar sjálfkrafa með því að nota sjálfvirku jöfnunaraðgerðina. Einnig er hægt að sérsníða hvernig sjálfvirkar jafnanir eru unnar með því að nota í **Forgangsraða jöfnun** valkost. Allir þessir valkostir eru hluti af á jöfnunarfæribreytur sem eru skilgreindar á **Færibreytur viðskiptakrafna** síðu. Færslur jafnaðar sjálfkrafa hvernig geta verið mismunandi, eftir þeirri aðferð sem notuð er fyrir sjálfvirka jöfnun. Eftirtaldar aðferðir eru tiltækar:

-   Notandaskilgreind jöfnunarforgangur
-   Sjálfgefin sjálfvirka jöfnun

Í eftirfarandi köflum er lýst hvernig færslur eru jafnaðar fyrir hvern greiðslumáta.

## <a name="example-transactions"></a>Dæmi um færslur
Dæmi um jafnanir síðar í þessum kafla eru byggð á eftirfarandi færslur. Allar færslur eru fyrir viðskiptavin 2050.

| Færsla   | Dagsetning        | Upphæð | Skilmálar staðgreiðsluafsláttar | Dagsetning staðgreiðsluafsláttar | Athugasemdir                                                                                                                                                                                      |
|---------------|-------------|--------|---------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reikningur 1     | Ágúst 15   | 100,00 | 2%14, Net 30        | Ágúst 29          |                                                                                                                                                                                               |
| Reikningur 2     | 1. september | 250,00 | 2%14, Net 30        | 15. september       |                                                                                                                                                                                               |
| Reikningur 3     | 15. október  | 500,00 | 2% 14/Net 30        | 29. október         |                                                                                                                                                                                               |
| Vaxtanóta | 15. október  | 7,00   |                     |                    | Þessi vaxtanóta er fyrir reikning 1 og 2. Upphæðin er reiknuð sem vextir 2 prósent á upphæðir sem eru 30 eða fleiri daga fram yfir gjalddaga. Til dæmis, 0.02 × (100.00 + 250.00) = 7.00. |

## <a name="user-defined-settlement-priority"></a>Notandaskilgreind jöfnunarforgangur
Ef þú stillir **Nota forgang fyrir sjálfvirkar jafnanir** á **Já** í **Færibreytur viðskiptakrafna** síðuna, jöfnunarforgangur sem skilgreina á síðunni **jöfnunarforgangur** er notaður þegar færslur eru valdar fyrir sjálfvirka jöfnun. Eftirfarandi forgangsröðun jöfnunar er skilgreind í þessu dæmi:

1.  Færslugerð
    -   Greiðsluþóknanir
    -   Innheimtubréf
    -   Vaxtanótur
    -   Reikningar

2.  færsludagsetning- hækkandi
3.  Fylgiskjal

Ef að bókuð er greiðslu fyrir 700.00 á 25. Október, greiðslur jafnaðar á færslur í eftirfarandi röð.

| Fylgiskjal       | Dagsetning       | Reikningur | Upphæð í gjaldmiðli færslu | Upphæð til jöfnunar | Staða | Gjaldmiðill |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Vaxtanóta | 10/15/2015 |         | 7,00                           | 7,00             | 0,00    | USD      |
| Reikningur 1     | 8/15/2015  | 10001   | 100,00                         | 100,00           | 0,00    | USD      |
| Reikningur 2     | 9/1/2015   | 10002   | 250,00                         | 250,00           | 0,00    | USD      |
| Reikningur 3     | 10/15/2015 |         | 500,00                         | 343,00           | 157.00  | USD      |

## <a name="default-automatic-settlement"></a>Sjálfgefin sjálfvirka jöfnun
Ef það er engin notandaskilgreindur jöfnunarforgangur, eru færslur sjálfkrafa valdar til jöfnunar byggð á gjalddaga. Færslur sem eru jafnaðar verða að hafa sama gjaldmiðil og færsluna sem þær eru jafnaðar með. Ef að bóka greiðslu fyrir 700.00 á 25. Október, eru eftirfarandi færslur valdar til jöfnunar.

| Fylgiskjal       | Dagsetning       | Reikningur | Upphæð í gjaldmiðli færslu | Upphæð til jöfnunar | Staða | Gjaldmiðill |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Reikningur 1     | 8/15/2015  | 10001   | 100,00                         | 100,00           | 0,00    | USD      |
| Reikningur 2     | 9/1/2015   | 10002   | 250,00                         | 250,00           | 0,00    | USD      |
| Reikningur 3     | 10/15/2015 |         | 500,00                         | 350.00           | 150,00  | USD      |
| Vaxtanóta | 10/15/2015 |         | 7,00                           | 0,00             | 0,00    | USD      |






