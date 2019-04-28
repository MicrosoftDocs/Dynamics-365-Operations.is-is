---
title: Taka staðgreiðsluafslátt utan tímabilsins staðgreiðsluafsláttar
description: Þessi grein sýnir tvenns konar aðstæður þar sem hægt er að taka staðgreiðsluafslátt jafnvel þó greiðslan eigi sér stað utan tímabils staðgreiðsluafsláttar.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 07d7c2740b23f6ad291bd295c878817e466da3bb
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/25/2019
ms.locfileid: "896788"
---
# <a name="take-a-cash-discount-outside-the-cash-discount-period"></a>Taka staðgreiðsluafslátt utan tímabilsins staðgreiðsluafsláttar

[!include [banner](../includes/banner.md)]

Þessi grein sýnir tvenns konar aðstæður þar sem hægt er að taka staðgreiðsluafslátt jafnvel þó greiðslan eigi sér stað utan tímabils staðgreiðsluafsláttar.

28. júní býr Apríl til reikning uppá 2.000,00 fyrir lánardrottinn 3052. Reikningurinn er með 1 prósent afslætti ef reikningurinn er greiddur innan 14 daga.

## <a name="use-cash-discount-option--always"></a>Nota valkostinn staðgreiðsluafsláttur = Alltaf
Apríl stofnar til greiðslu á 1. Júlí, sem er eftir dagsetningu afsláttar. Apríl opnar síðuna **Jafna færslur** til að skoða færslur sem hægt er að jafna. 

Apríl merkir reikninginn til greiðslu. Enginn staðgreiðsluafsláttur er tekinn, þar sem greitt er eftir afsláttartímabil. Hins vegar hefur lánardrottinn gefið Apríl samþykki fyrir því að taka staðgreiðsluafslátt samt. Þess vegna breytir Apríl gildi á svæðinu **Nota staðgreiðsluafslátt** í **Alltaf**.

| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning staðgreiðsluafsláttar | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Valið | Alltaf            | Inv-10030 | 3052    | 6/28/2015          | 7/12/2015 | 10030   | -2.000,00                      | USD      | -1.980.00        |

Afsláttarupplýsingarnar birtist neðst á **Jafna færslur** síðunni.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/12/2015 |
| Upphæð staðgreiðsluafsláttar         | -20.00    |
| Nota staðgreiðsluafslátt            | Alltaf    |
| Notaður staðgreiðsluafsláttur          | 0,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | -20.00    |

## <a name="date-to-use-for-calculating-discounts--selected-date"></a>Dagsetning fyrir útreikning afslátta = Valin dagsetning.
Ef bæði reikningur og greiðsla hefur verið bókuð, er enn hægt að fá staðgreiðsluafslátt þegar færslurnar eru jafnaðar á°síðunni **Jafna færslur**. Apríl breytir gildi á svæðinu **Dagsetning sem á að nota fyrir útreikning afslátta** í **Valin dagsetning**. Hún færir svo dagsetninguna 28. Júní sem er staðgreiðsluafsláttartímabili‘ fyrir reikninginn. Sú dagsetning er notuð til að reikna staðgreiðsluafslátt fyrir færsluna. Á síðunni **Jafna opnar færslur** sér Apríl að,sem sjálfgefið, birtist fullur afsláttur upp á 20,00. Reikningslínan sýnir að upphæð til jöfnunar er 1.980.00.

| Merkja                     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning staðgreiðsluafsláttar | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|--------------------------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Valdar og auðkenndar. | Venjulegt            | Inv-10030 | 3052    | 6/28/2015          | 7/12/2015 | 10030   | -2.000,00                      | USD      | -1.980.00        |
| Valið                 | Venjulegt            | APP-10030 | 3052    | 7/15/2015          | 7/15/2015 |         | 500,00                         | USD      | 500,00           |

Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni. Upphæð afsláttar sem er tekinn er 20,00, þar sem upphæðin til jöfnunar fyrir reikning er sjálfgefna upphæðin, 1,980.00.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/12/2015 |
| Upphæð staðgreiðsluafsláttar         | -20.00    |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 0,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | -20.00    |

Apríl uppfærir gildið á svæðinu **Upphæð til jöfnunar** í **500,00**. Gildið í svæðinu **Upphæð staðgreiðsluafsláttar sem á að taka** er reiknað sem **5,05**.

| Merkja                     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valdar og auðkenndar. | Venjulegt            | Inv-10030 | 3052    | 6/28/2015 | 7/12/2015 | 10030   | 2.000,00                       | USD      | -500,00          |
| Valið                 | Venjulegt            | APP-10030 | 3052    | 7/15/2015 | 7/15/2015 |         | 500,00                         | USD      | 500,00           |

Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni. Gildið í svæðinu **Upphæð staðgreiðsluafsláttar sem á að taka** er **5,05**, þar sem upphæðin til jöfnunar fyrir reikninginn var breytt í greiðsluupphæðina 500,00.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/12/2015 |
| Upphæð staðgreiðsluafsláttar         | -20.00    |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 0,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | -5,05     |





