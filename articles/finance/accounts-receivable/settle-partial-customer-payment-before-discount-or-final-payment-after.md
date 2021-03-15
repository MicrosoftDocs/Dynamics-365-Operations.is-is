---
title: Jafna hlutagreiðslu fyrir afsláttardagsetninguna við lokagreiðslu eftir afsláttardagsetninguna
description: Þessi grein fer yfir áhrif þess að jafna greiðslur á reikninga fyrir viðskiptavini. Aðstæðurnar einblína á áhrifin í undirbókinni, ekki í Fjárhagnum.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14584
ms.assetid: e54936f5-053b-4ed3-b778-42c7e9aeb7cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad922bc6c9378078012b7a838909e4074b48f263
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979065"
---
# <a name="settle-partial-payment-before-discount-date-with-final-payment-after-discount-date"></a>Jafna hlutagreiðslu fyrir afsláttardagsetninguna við lokagreiðslu eftir afsláttardagsetninguna

[!include [banner](../includes/banner.md)]

Þessi grein fer yfir áhrif þess að jafna greiðslur á reikninga fyrir viðskiptavini. Aðstæðurnar einblína á áhrifin í undirbókinni, ekki í Fjárhagnum.

Fabrikam selur vörurn til 4027 viðskiptavina. Fabrikam býður 1 prósent afslátt ef reikningurinn er greiddur innan 14 daga. Greiða þarf reikninga eftir 30 daga. Fabrikam býður einnig upp á staðgreiðsluafslætti fyrir hlutagreiðslur. Uppgjörsfæribreytur eru staðsettar á síðunni **Færibreytur viðskiptakrafna**.

## <a name="invoice"></a>Reikningur
25. júní færir Apríl inn og bókar reikning uppá 1.000,00 fyrir viðskiptamann 4027. Arnie getur skoðað þennan reikning með því að nota hnappinn **Færslur** á síðunni **Viðskiptavinir**.

| Fylgiskjal   | Færslugerð | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða  | Gjaldmiðill |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10020 | Reikningur          | 6/25/2015 | 10020   | 1.000,00                             |                                       | 1.000,00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>hlutagreiðsla fyrir dagsetningu staðgreiðsluafsláttar
2. júlí gerir viðskiptavinar 4027 hlutagreiðslu upp á 297.00 fyrir reikninginn. Greiðslan gefur rétt á afslætti, þar sem Fabrikam býður afslátt á hlutagreiðslur og hlutagreiðslan er gerð á undan dagsetningu staðgreiðsluafsláttar. Þess vegna fær viðskiptavinar 4027 3,00 í staðgreiðsluafslátt. Arnie skráir greiðslu fyrir viðskiptavin 4027 með því að nota greiðslubók. Síðan opnar Arnie síðuna **Jafna færslur** svo að hann geti merkt reikninginn fyrir jöfnun.

| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í færslugjaldmiðli - debet | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Valið | Venjulegt            | FTI-10020 | 4027    | 6/25/2015 | 7/25/2015 | 10020   | 1.000,00                             | USD      | 297,00           |

Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni. Ef gildinu í **Upphæðin til jöfnunar** er ekki breytt í 297.00 verða gildin fyrir **Upphæð staðgreiðsluafsláttar** sem birtast vera mismunandi. Hins vegar verður 3,00 notað sem staðgreiðsluafsláttur þegar greiðslan er bókuð, þar sem jöfnun leiðréttir sjálfkrafa gildið **Upphæð til jöfnunar** fyrir þig.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/09/2015 |
| Upphæð staðgreiðsluafsláttar         | 10,00     |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 0,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | 3,00      |

Arnie bókar þessa greiðslu. Reikningurinn hefur núna stöðuna 700,00. Hægt er að sjá eftirfarandi færslur fyrir viðskiptavininn.

| Fylgiskjal    | Færslugerð | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða | Gjaldmiðill |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10020  | Reikningur          | 6/25/2015 | 10020   | 1.000,00                             |                                       | 700.00  | USD      |
| ARP-10020  |  Greiðsla         | 7/1/2015  |         |                                      | 297,00                                | 0,00    | USD      |
| DISC-10020 |  Staðgreiðsluafsláttur   | 7/1/2015  |         |                                      | 3,00                                  | 0,00    | USD      |

## <a name="remaining-payment-after-the-cash-discount-date"></a>Eftirstandandi greiðsla eftir dagsetningu staðgreiðsluafsláttar
Þann 11. júlí, sem er eftir afsláttartímabilið, greiðir viðskiptavinur 4027 afganginn af reikningnum. Á síðunni **Jafna opnar færslur** birtist afsláttarupphæð ekki í reitnum **Áætlaður staðgreiðsluafsláttur** og gildið í reitnum **Upphæð staðgreiðsluafsláttar** er **0,00**. Þegar viðskiptavinur 4027 greiðir eftirstandandi 700,00 verður ekki veittur frekari afsláttur.

| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í færslugjaldmiðli - debet | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Valið | Venjulegt            | FTI-10020 | 4027    | 6/25/2015 | 7/25/2015 | 10020   | 700.00                               | USD      | 700.00           |

Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/09/2015 |
| Upphæð staðgreiðsluafsláttar         | 0,00      |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 3,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | 0,00      |

Ef Arnie breytir gildi í reitnum **Nota staðgreiðsluafslátt** í **Alltaf** er stillingunni **Reikna staðgreiðsluafslátt fyrir hlutagreiðslur** er hnekkt og staðgreiðsluafsláttur er veittur. Greiðsluupphæðin breytist í 693,00 og staðgreiðsluafslátturinn er 7,00.

| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valið | Alltaf            | FTI-10020 | 4027    | 6/25/2015 | 7/25/2015 | 10020   | 700.00                               |                                       | USD      | 693,00           |

Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/09/2015 |
| Upphæð staðgreiðsluafsláttar         | 7,00      |
| Nota staðgreiðsluafslátt            | Alltaf    |
| Notaður staðgreiðsluafsláttur          | 3,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | 7,00      |

Arnie breytir gildinu í reitnum **Nota staðgreiðsluafslátt** aftur í **Venjulegt**, þar sem hann lætur þennan viðskiptavin ekki fá eftirstandandi staðgreiðsluafslátt upp á 7,00. Síðan bókar Arnie reikninginn. Þegar Arnie opnar síðuna **Færslur viðskiptavina** sér hann að reikningurinn hefur stöðuna 0,00. Hann sér einnig að það eru tvær greiðslur. Ein greiðsla er upp á 297,00 með 3,00 staðgreiðsluafslætti og önnur greiðsla er upp á 700,00.

| Fylgiskjal    | Færslugerð | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða | Gjaldmiðill |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10020  | Reikningur          | 6/25/2015 | 10020   | 1.000,00                             |                                       | 0,00    | USD      |
| ARP-10020  |                  | 7/1/2015  |         |                                      | 297,00                                | 0,00    | USD      |
| DISC-10020 |                  | 7/1/2015  |         |                                      | 3,00                                  | 0,00    | USD      |
| ARP 10021  |                  | 7/11/2015 |         |                                      | 700.00                                | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]