---
title: Sjálfvirkt uppgjör og forgangsröðun
description: Þessi grein lýsir því hvernig færslur eru jafnaðar ef valið er Sjálfvirkt uppgjör á síðunni Færibreytur viðskiptakrafna. Það útskýrir einnig hvernig hægt er að nota sjálfvirkt uppgjör í samsetningu með greiðsluforgangi.
author: ShivamPandey-msft
ms.date: 01/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: kfend
ms.custom: 14531
ms.assetid: e7837cf6-ec69-44b4-8d47-eba38d5c7b1f
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd5b894c82beb1b5d69ad6bf485161ab9c91a806
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855521"
---
# <a name="automatic-settlement-and-prioritization"></a>Sjálfvirkt uppgjör og forgangsröðun

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig færslur eru jafnaðar ef valið er Sjálfvirkt uppgjör á síðunni Færibreytur viðskiptakrafna. Það útskýrir einnig hvernig hægt er að nota sjálfvirkt uppgjör í samsetningu með greiðsluforgangi.

Þú hefur tvo valkosti við jöfnun á greiðslum með reikninga og öðrum færslum. Hægt er að velja færslur til jöfnunar handvirkt, eða kerfið getur valið færslurnar sjálfkrafa með því að nota sjálfvirku jöfnunaraðgerðina. Einnig er hægt að sérsníða hvernig sjálfvirkar jafnanir eru unnar með því að nota valkostinn **Forgangsraða jöfnun**. Allir þessir valkostir eru hluti af jöfnunarfæribreytum sem eru skilgreindar á síðunni **Færibreytur viðskiptakrafna**. Misjafnt er hvernig færslur eru jafnaðar sjálfkrafa, eftir þeirri aðferð sem notuð er fyrir sjálfvirka jöfnun. Eftirtaldar aðferðir eru tiltækar:

-   Notandaskilgreindur jöfnunarforgangur
-   Sjálfgefin sjálfvirk jöfnun

Í eftirfarandi köflum er lýst hvernig færslur eru jafnaðar fyrir hvern greiðslumáta.

## <a name="example-transactions"></a>Dæmi um færslur
Dæmi um jafnanir síðar í þessum kafla eru byggð á eftirfarandi færslum. Allar færslur eru fyrir viðskiptavin 2050.

| Færsla   | Dagsetning        | Upphæð | Skilmálar staðgreiðsluafsláttar | Dagsetning staðgreiðsluafsláttar | Athugasemdir                                                                                                                                                                                      |
|---------------|-------------|--------|---------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reikningur 1     | 15. ágúst   | 100,00 | 2%14, Net 30        | 29. ágúst          |                                                                                                                                                                                               |
| Reikningur 2     | 1. september | 250,00 | 2%14, Net 30        | 15. september       |                                                                                                                                                                                               |
| Reikningur 3     | 15. október  | 500,00 | 2% 14/Net 30        | 29. október         |                                                                                                                                                                                               |
| Vaxtanóta | 15. október  | 7,00   |                     |                    | Þessi vaxtanóta er fyrir reikning 1 og 2. Upphæðin er reiknuð sem 2 prósent vextir á upphæðir sem eru 30 eða fleiri daga fram yfir gjalddaga. Til dæmis, 0,02 × (100,00 + 250,00) = 7,00. |

## <a name="user-defined-settlement-priority"></a>Notandaskilgreindur jöfnunarforgangur
Ef þú stillir **Nota forgang fyrir sjálfvirkar jafnanir** á **Já** í **Færibreytur viðskiptakrafna** síðuna, jöfnunarforgangur sem skilgreina á síðunni **jöfnunarforgangur** er notaður þegar færslur eru valdar fyrir sjálfvirka jöfnun. Eftirfarandi forgangsröðun jöfnunar er skilgreind í þessu dæmi:

1.  Færslugerð
    -   Greiðsluþóknanir
    -   Innheimtubréf
    -   Vaxtanótur
    -   Reikningar

2.  færsludagsetning- hækkandi
3.  Fylgiskjal

Ef þú bókar greiðslu fyrir 700,00 þann 25. október, er greiðslan jöfnuð á færslurnar í eftirfarandi röð.

| Fylgiskjal       | Dagsetning       | Reikningur | Upphæð í gjaldmiðli færslu | Upphæð til jöfnunar | Staða | Gjaldmiðill |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Vaxtanóta | 15/10/2015 |         | 7,00                           | 7,00             | 0,00    | USD      |
| Reikningur 1     | 15/8/2015  | 10001   | 100,00                         | 100,00           | 0,00    | USD      |
| Reikningur 2     | 1/9/2015   | 10002   | 250,00                         | 250,00           | 0,00    | USD      |
| Reikningur 3     | 15/10/2015 |         | 500,00                         | 343,00           | 157.00  | USD      |

## <a name="default-automatic-settlement"></a>Sjálfgefin sjálfvirka jöfnun
Ef enginn notandaskilgreindur jöfnunarforgangur er til staðar, eru færslur sjálfkrafa valdar til jöfnunar byggt á gjalddaga. Færslur sem eru jafnaðar verða að hafa sama gjaldmiðil og færslan sem þær eru jafnaðar við. Ef þú bókar greiðslu fyrir 700,00 þann 25. október, eru eftirfarandi færslur valdar til jöfnunar.

| Fylgiskjal       | Dagsetning       | Reikningur | Upphæð í gjaldmiðli færslu | Upphæð til jöfnunar | Staða | Gjaldmiðill |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Reikningur 1     | 15/8/2015  | 10001   | 100,00                         | 100,00           | 0,00    | USD      |
| Reikningur 2     | 1/9/2015   | 10002   | 250,00                         | 250,00           | 0,00    | USD      |
| Reikningur 3     | 15/10/2015 |         | 500.00                         | 350.00           | 150.00  | USD      |
| Vaxtanóta | 15/10/2015 |         | 7.00                           | 0,00             | 7.00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
