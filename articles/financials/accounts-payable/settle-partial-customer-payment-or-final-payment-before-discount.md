---
title: "Jafna hlutagreiðsla lánardrottins og endanlega greiðslu að fullu fyrir afsláttardagsetninguna"
description: "Þessi grein gefur dæmi um aðstæður sem sýna hvernig á að skrá hlutagreiðslur fyrir viðskiptavin og taka staðgreiðsluafslátt innan staðgreiðsluafsláttartímabils."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14491
ms.assetid: 0f07d3ce-a439-43ed-a22e-957ccd36a37b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 08b5fc87fdee476cd978bcc242cea324ac4bcee2
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017

---

# <a name="settle-a-partial-customer-payment-and-the-final-payment-in-full-before-the-discount-date"></a>Jafna hlutagreiðsla lánardrottins og endanlega greiðslu að fullu fyrir afsláttardagsetninguna

[!include[banner](../includes/banner.md)]


Þessi grein gefur dæmi um aðstæður sem sýna hvernig á að skrá hlutagreiðslur fyrir viðskiptavin og taka staðgreiðsluafslátt innan staðgreiðsluafsláttartímabils.

Fabrikam selur vörur til viðskiptavinar 4028. Fabrikam býður 1 prósent afslátt ef reikningurinn er greiddur innan 14 daga. Greiða þarf reikninga eftir 30 daga. Fabrikam býður einnig upp á staðgreiðsluafslætti fyrir hlutagreiðslur. Uppgjörsfæribreytur eru staðsettar á síðunni **Færibreytur viðskiptakrafna**.

## <a name="customer-invoice"></a>Reikningur viðskiptavinar
25. júní færir Apríl inn reikning uppá 1.000,00 fyrir viðskiptavin 4028. April getur skoðað þessa færslu á síðunni **viðskiptavinarfærslur**.

| Fylgiskjal   | Færslugerð | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða  | Gjaldmiðill |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10010 | Reikningur          | 6/25/2015 | 10010   | 1.000,00                             |                                       | 1.000,00 | USD      |

Úr á **Viðskiptavinar** eða **viðskiptavinafærslur** síðu, getur Arnie opna í **Jafna færslur** síðu til að skoða dagsetningar og staðgreiðsluafsláttur sem eru tiltækar fyrir reikninginn. Gjalddagi er 25 Júlí og staðgreiðsluafsláttur uppá 10,00 er tiltæk ef reikningurinn er greiddur fyrir 9 Júlí.

| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valið | Venjulegt            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1.000,00                       | USD      | 990,00           |

Afsláttarupplýsingarnar birtist neðst á **Jafna færslur** síðu fyrir merktar reikningsins.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/09/2015 |
| Upphæð staðgreiðsluafsláttar         | 10,00     |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 0,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | 10,00     |

Arnie smellir á **staðgreiðsluafsláttur** flipa til að skoða afsláttarupphæð.

| Dagsetning staðgreiðsluafsláttar | Upphæð staðgreiðsluafsláttar | Upphæð í gjaldmiðli færslu |
|--------------------|----------------------|--------------------------------|
| 7/9/2015           | 10,00                | 990,00                         |
| 7/25/2015          | 0,00                 | 1.000,00                       |

## <a name="partial-payment-by-using-the-enter-customer-payments-page"></a>Hlutagreiðsla með því að nota síðuna færa inn greiðslur viðskiptavinar
Viðskiptavinur 4028 sendir greiðslu fyrir 500,00 1. Júlí. Til að færa þessa greiðslu er smellir Apríl ekki á **Línur**. Í staðinn hann skráir greiðslu með því að stofna nýja greiðslubók og síðan opna á **færa Inn greiðslur viðskiptavina** síðu. Hann færir inn upplýsingar um greiðslu og merkir reikninginn sem hann færði inn. Þegar Arnie færir **500,00** sem upphæð færir hann einnig **500,00** í á **Upphæð til greiðslu** í hnitanetinu. Þar sem Fabrikam leyfir staðgreiðsluafslátt á hlutagreiðslur sér að hlutfallslegur staðgreiðsluafsláttur uppá 5.05 var einnig tekinn. Útreikningur fyrir þetta afsláttur er 500.00 ÷ 0.99 × 0.01 = 5.05. (Í þessum útreikningi 500,00 er deilt með 0.99, vegna þess að afsláttur 1 prósent. Þess vegna er greiðir viðskiptavinur 99 prósent af reikningi. Niðurstaðan er síðan margfaldað með afsláttarprósenta 1 prósent eða 0,01. Ef viðskiptavinurinn tekur fullt afsláttur 10,00, þarf að jafna upphæð sem er 990.00.) Afsláttarupplýsingarnar birtist í hnitaneti neðst á síðunni **Færa inn greiðslur viðskiptavina**.

| Upphæð staðgreiðsluafsláttar sem á að veita | Notaður staðgreiðsluafsláttur | Upphæð til greiðslu |
|------------------------------|---------------------|---------------|
| 5,05                         | 0,00                | 500,00        |

## <a name="partial-payment-by-using-the-journal-lines"></a>Hlutagreiðsla með því að nota færslubókarlínur
Í stað þess að opna **færa Inn greiðslur viðskiptavina** síðu í greiðslubók getur Arnie  smellt á **Línur** til að færa inn greiðslu. Greiðslubók birtist, þar sem Arnie getur færa inn línu fyrir viðskiptavin 4028. Síðan opnar Arnie síðuna **Jafna færslur** svo að hann geti merkt reikninginn fyrir jöfnun. Arnie merkir reikninginn og breytir gildi í **Upphæðin til jöfnunar** reit í  **500,00**. Aftur, sér hann að gildið í á **upphæð staðgreiðsluafsláttar** er **10,00** fyrir fullan reikning og gildið í á **upphæð staðgreiðsluafsláttar sem á að taka** er **5.05**. Þess vegna er Arnie að jafna 505.05 fyrir þennan reikning.

| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valið | Venjulegt            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1.000,00                       | USD      | 500,00           |

Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/09/2015 |
| Upphæð staðgreiðsluafsláttar         | 10,00     |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 0,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | 5,05      |

Ef viðskiptavinurinn vill jafna nákvæmlega helming reiknings, viðskiptavinar sendir greiðslu uppá 495.00. Í þessu tilfelli færir Arnie inn **495.00** í á **Upphæðin til jöfnunar** svæði. Staðgreiðsluafsláttur fyrir 5,00 verður einnig tekið, svo að heildarupphæð sem er jöfnuð er 500,00.

| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valið | Venjulegt            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1.000,00                       | USD      | 495,00           |

Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/09/2015 |
| Upphæð staðgreiðsluafsláttar         | 10,00     |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 0,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | 5,00      |

Arnie Lokar **Jafna færslur** síðu. Greiðslulína fyrir 495.00 er stofnuð í færslubók og þá bókar Arnie færslubókina. Hann getur endurskoða viðskiptavinafærslur á í **viðskiptavinafærslur** síðu. Á þessari síðu sér Arnie að reikningurinn hefur stöðuna 500,00. Hann sér einnig greiðslu uppá 495.00 og afsláttur 5,00.

| Fylgiskjal    | Færslugerð | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða | Gjaldmiðill |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Reikningur          | 6/25/2015 | 10010   | 1.000,00                             |                                       | 500,00  | USD      |
| ARP-10010  |  Greiðsla         | 7/1/2015  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10010 |  Staðgreiðsluafsláttur   | 7/1/2015  |         |                                      | 5,00                                  | 0,00    | USD      |

## <a name="payment-for-the-remaining-amount"></a>Greiðsla eftirstandandi upphæðar
viðskiptavinur 4028 greiðir eftirstandandi upphæð 495.00 á Júlí 8, sem er innan tímabils staðgreiðsluafsláttar. Arnie stofnar greiðslubók á 8 Júlí og merkir færsluna til jöfnunar. hann sér að Upphæðin sem þarf að jafna er 495.00 . Gildið í á **Áætlaður staðgreiðsluafsláttur** er **5,00** því 5,00 afslátturinn var áður tekinn af.

|                         |        |
|-------------------------|--------|
| Heildarmerking            | 495,00 |
| Áætlaður staðgreiðsluafsláttur | 5,00   |

Upplýsingar um merkta færslan birtist í hnitaneti í á **Jafna opnar færslur** síðu.

| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valið | Venjulegt            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1.000,00                       | USD      | 495,00           |

Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/09/2015 |
| Upphæð staðgreiðsluafsláttar         | 10,00     |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 5,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | 5,00      |

Arnie bókar þessa færslubók og fer yfir viðskiptavinafærslur á **viðskiptavinafærslur** síðu. Staða reiknings er nú 0,00 og Arnie sér tvo staðgreiðsluafslátta og tvær greiðslur.

| Fylgiskjal    | Færslugerð | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða | Gjaldmiðill |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Reikningur          | 6/25/2015 | 10010   | 1.000,00                             |                                       | 0,00    | USD      |
| ARP-10010  | Greiðsla          | 7/1/2015  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10010 | Staðgreiðsluafsláttur    | 7/1/2015  |         |                                      | 5,00                                  | 0,00    | USD      |
| ARP-10011  | Greiðsla          | 7/8/2015  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10011 | Staðgreiðsluafsláttur    | 7/8/2015  |         |                                      | 5,00                                  | 0,00    | USD      |





