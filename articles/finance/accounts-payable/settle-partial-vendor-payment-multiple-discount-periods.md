---
title: Jafna hlutagreiðslu lánardrottins sem er með mörg afsláttartímabil
description: Þessi grein fer í gegnum aðstæður þar sem margar hlutagreiðslur eru greiddar til lánardrottins sem gefur marga staðgreiðsluafslætti.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14262
ms.assetid: af95c48a-afd1-476c-978d-e34995100be4
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da69d61c657ddc168a27a97fe16909d5f60eb4fd
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778038"
---
# <a name="settle-a-partial-vendor-payment-that-has-multiple-discount-periods"></a>Jafna hlutagreiðslu lánardrottins sem er með mörg afsláttartímabil

[!include [banner](../includes/banner.md)]

Þessi grein fer í gegnum aðstæður þar sem margar hlutagreiðslur eru greiddar til lánardrottins sem gefur marga staðgreiðsluafslætti. 

Lánardrottinn 3054 býður Fabrikam 2 prósent staðgreiðsluafslátt ef reikningur er greiddur innan fimm daga og um 1 prósent staðgreiðsluafslátt ef reikningurinn er greiddur innan 14 daga.

## <a name="invoice"></a>Reikningur
28. júní býr Apríl til reikning uppá 1.000,00 fyrir lánardrottinn 3054. Arnie getur skoðað þessa færslu á síðunni **lánardrottnafærslur**.

| Fylgiskjal   | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða   | Gjaldmiðill |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10060 | 6/28/2020 | 10060   |                                      | 1,000.00                              | -1.000,00 | USD      |

Eftirfarandi dagsetningar og upphæðir staðgreiðsluafsláttar eru tiltækar fyrir þennan reikning.

| Dagsetning staðgreiðsluafsláttar | Upphæð staðgreiðsluafsláttar | Upphæð í gjaldmiðli færslu |
|--------------------|----------------------|--------------------------------|
| 7/3/2020           | 20.00                | 980.00                         |
| 7/12/2020          | 10,00                | 990.00                         |
| 7/25/2020          | 0,00                 | 1,000.00                       |

## <a name="payment-on-july-2"></a>Greiðsla 2. júlí
2. júlí vill Apríl greiða 300,00 inn á þennan reikning. Hún stofnar eingreiðslu með því að nota síðuna **Greiðslubók** í Viðskiptaskuldum. Hún bætir við línu fyrir lánardrottin 3054 og færir inn upphæð greiðslu **300.00**. Síðan opnar Apríl síðuna **Jafna færslur**, þannig að hún getur merkt reikninginn sem verður jafnaður. Hún uppfærir gildið í reitnum **Upphæð til jöfnunar** í **300,00** og tekur eftir því að gildið í reitnum **Upphæð staðgreiðsluafsláttar sem á að taka** hefur breyst í **6,12**. Þar sem þessi greiðsla er í fyrsta afsláttartímabilinu er fenginn afsláttur 2 prósent.

| Merkja | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Venjulegt            | Inv-10060 | 3054    | 6/28/2020 | 7/28/2020 | 10060   | 1,000.00                       | USD      | 300.00           |

Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni.

| Svæði                        | Gildi     |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/02/2020 |
| Upphæð staðgreiðsluafsláttar         | -20.00    |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 0,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | -6.12     |

Þar sem staðgreiðsluafsláttur er tiltækut vill Apríl breyta greiðsluupphæðinni þannig heildarupphæð sem er jöfnuð er 300.00 fyrir bæði greiðsluna og staðgreiðsluafsláttinn. Hún breytir gildinu í reitnum **Upphæð til jöfnunar** í **294,00** og tekur eftir því að gildið í reitnum **Upphæð staðgreiðsluafsláttar sem á að taka** hefur breyst í **6,00**.

| Merkja | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Venjulegt            | Inv-10060 | 3054    | 6/28/2020 | 7/28/2020 | 10060   | 1,000.00                       | USD      | 294.00           |

Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni.

| Svæði                        | Gildi     |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/02/2020 |
| Upphæð staðgreiðsluafsláttar         | -20.00    |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 0,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | -6.00     |

Apríl bókar greiðsluna. Á síðunni **Lánardrottnafærslur** getur hún skoðað færslurnar. Hún sér að 300,00 hefur verið jafnað við reikninginn. Þessi upphæð inniheldur afslátt 6,00. Þess vegna eru eftirstöðvar 700.00.

| Fylgiskjal    | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða | Gjaldmiðill |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 6/28/2020 | 10060   |                                      | 1,000.00                              | -700,00 | USD      |
| APP-10060  | 7/2/2020  |         | 294.00                               |                                       | 0,00    | USD      |
| DISC-10060 | 7/2/2020  |         | 6,00                                 |                                       | 0,00    | USD      |

## <a name="payment-on-july-8"></a>Greiðsla 8. júlí
Apríl gerir viðbótargreiðslu á reikning þann 8. júlí. Til að færa inn upphæðina opnar hún síðuna **Jafna færslur** og smellir síðan á flipann **Staðgreiðsluafsláttur**. Hún sér dagsetningar og upphæðir fyrir tvennan staðgreiðsluafslátt sem er tiltækur. Þar sem þessi greiðsla er í öðru afsláttartímabilinu er tiltækur afsláttur 1 prósent, eða 5,00. Þessi upphæð er reiknuð sem helmingurinn af 1 prósent afslætti af 1.000,00 eða helmingurinn af 10,00.

| Dagsetning staðgreiðsluafsláttar | Upphæð staðgreiðsluafsláttar | Upphæð í gjaldmiðli færslu |
|--------------------|----------------------|--------------------------------|
| 7/3/2020           | 20.00                | 680.00                         |
| 7/12/2020          | 10,00                | 690.00                         |
| 7/25/2020          | 0,00                 | 700.00                         |

Apríl ákveður að greiða 495,00 og taka 5,00 staðgreiðsluafslátt. Þess vegna er heildarupphæðin sem er jöfnuð nú 500,00.

| Merkja | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Venjulegt            | Inv-10060 | 3054    | 6/28/2020 | 7/28/2020 | 10060   | 1,000.00                       | USD      | 495,00           |

Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni.

| Svæði                        | Gildi     |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/12/2020 |
| Upphæð staðgreiðsluafsláttar         | -10,00    |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | -6.00     |
| Upphæð staðgreiðsluafsláttar sem á að veita | -5,00     |

Á síðunni **Lánardrottnafærslur** sér Apríl að ný staða er 200,00.

| Fylgiskjal    | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða | Gjaldmiðill |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 6/28/2020 | 10060   |                                      | 1,000.00                              | 200.00 | USD      |
| APP-10060  | 7/2/2020  |         | 294.00                               |                                       | 0,00    | USD      |
| DISC-10060 | 7/2/2020  |         | 6,00                                 |                                       | 0,00    | USD      |
| APP-10061  | 7/12/2020 |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10061 | 7/12/2020 |         | 5.00                                 |                                       | 0,00    | USD      |

## <a name="payment-on-july-20"></a>Greiðsla 20. júlí
Þann 20. júlí stofnar Apríl lokagreiðlu upp á 200,00. Enginn afsláttur er tekinn, þar sem greitt er eftir bæði afsláttartímabilin. Staða reikningsins er 0,00.

| Fylgiskjal    | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða | Gjaldmiðill |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 6/28/2020 | 10060   |                                      | 1,000.00                              | 200.00 | USD      |
| APP-10060  | 7/2/2020  |         | 294.00                               |                                       | 0,00    | USD      |
| DISC-10060 | 7/2/2020  |         | 6,00                                 |                                       | 0,00    | USD      |
| APP-10061  | 7/12/2020 |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10061 | 7/12/2020 |         | 5.00                                 |                                       | 0,00    | USD      |
| APP-10062  | 7/20/2020 |         | 200.00                               |                                       | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
