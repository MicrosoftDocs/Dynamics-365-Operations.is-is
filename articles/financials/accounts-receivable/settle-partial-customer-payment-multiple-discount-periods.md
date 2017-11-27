---
title: "Jafna hlutagreiðslu viðskiptavinar sem er með mörg afsláttartímabil"
description: "Þessi grein sýnir hvernig skal jafna hlutagreiðslu viðskiptavinar þegar um er að ræða mörg afsláttartímabil."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14471
ms.assetid: b633a7c4-c18d-42e7-91cc-adcdc8a3ba98
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ac64ece82abe75f3cba437b1ec1af499fbbce8e4
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="settle-a-partial-customer-payment-that-has-multiple-discount-periods"></a>Jafna hlutagreiðslu viðskiptavinar sem er með mörg afsláttartímabil

[!include[banner](../includes/banner.md)]


Þessi grein sýnir hvernig skal jafna hlutagreiðslu viðskiptavinar þegar um er að ræða mörg afsláttartímabil.

Fabrikam býður viðskiptavin 4031 tvær staðgreiðsluafsláttartímabil. Viðskiptavinurinn fær 2 prósent staðgreiðsluafslátt ef reikningur er greiddur innan fimm daga og um 1 prósent staðgreiðsluafslátt ef reikningurinn er greiddur innan 14 daga. Fabrikam býður einnig upp á staðgreiðsluafslætti fyrir hlutagreiðslur. Uppgjörsfæribreytur eru staðsettar á síðunni **Færibreytur viðskiptakrafna**.

## <a name="invoice"></a>Reikningur
25. júní færir Apríl inn reikning uppá 1.000,00 fyrir lánardrottinn 4031. Þegar hún fer yfir staðgreiðsluafslætti fyrir þennan reikning sér Apríl að viðskiptavinur 4031 fær 20,00 afslátt ef reikningurinn er greiddur fyrir 30. Júní. Ef reikningurinn er greiddur fyrir 9 Júlí, fær viðskiptavinurinn 10,00 afslátt.

| Dagsetning staðgreiðsluafsláttar | Upphæð staðgreiðsluafsláttar | Upphæð í gjaldmiðli færslu |
|--------------------|----------------------|--------------------------------|
| 6/30/2015          | 20,00                | 980,00                         |
| 7/9/2015           | 10,00                | 990,00                         |
| 7/25/2015          | 0,00                 | 1.000,00                       |

April getur skoðað þessa færslu á síðunni **viðskiptavinarfærslur**.

| Fylgiskjal   | Færslugerð | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða  | Gjaldmiðill |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10030 | Reikningur          | 6/25/2015 | 10030   | 1.000,00                             |                                       | 1.000,00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>hlutagreiðsla fyrir dagsetningu staðgreiðsluafsláttar
Á 28. Júní gerir Viðskiptavinur 4031 hlutagreiðslu uppá 294.00. Þar sem 28. Júní er innan fyrsta tímabilsins staðgreiðsluafsláttar, tekur viðskiptavinar 6.00 afslátt. Á **Jafna færslur** síðu í**upphæð staðgreiðsluafsláttar** gildi er 20,00, og **upphæð staðgreiðsluafsláttar sem á að taka** gildi er 6.00 .

| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valið | Venjulegt            | FTI-10030 | 4031    | 6/25/2015 | 7/25/2015 | 10030   | 1.000,00                       | USD      | 294.00           |

Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni. Ef gildinu í **Upphæðin til jöfnunar** er ekki breytt í **294,00** verða gildin fyrir **Upphæð staðgreiðsluafsláttar** sem birtast mismunandi. Hins vegar verður 6,00 tekið sem staðgreiðsluafsláttur þegar greiðslan er bókuð, þar sem jöfnun leiðréttir sjálfkrafa gildið **Upphæð til jöfnunar**fyrir þig.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 6/30/2015 |
| Upphæð staðgreiðsluafsláttar         | 20,00     |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 0,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | 6,00      |

Eftir að Arnie bókar greiðslu, er staða reiknings 700.00.

## <a name="partial-payment-before-the-second-cash-discount-date"></a>Hlutagreiðsla fyrir aðra dagsetningu staðgreiðsluafsláttar
Viðskiptavinur greiðir afgangurinn af reikningsupphæðinni á 8. Júlí. Þar sem þessi greiðsla er í öðru afsláttartímabilinu , er tekinn afslátt uppá 7,00 (1 prósentum).

| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valið | Venjulegt            | FTI-10030 | 4031    | 6/25/2015 | 7/25/2015 | 10030   | 700.00                               |                                       | USD      | 693,00           |

Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/09/2015 |
| Upphæð staðgreiðsluafsláttar         | 30,00     |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 6,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | 7,00      |

Staða reiknings er nú 0.00. April getur skoðað upplýsingar á síðunni **viðskiptavinarfærslur**.

| Fylgiskjal    | Færslugerð | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða | Gjaldmiðill |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10030  | Reikningur          | 6/25/2015 | 10030   | 1.000,00                             |                                       | 0,00    | USD      |
| ARP-10030  |  Greiðsla         | 6/28/2015 |         |                                      | 294.00                                | 0,00    | USD      |
| DISC-10030 |  Staðgreiðsluafsláttur   | 6/28/2015 |         |                                      | 6,00                                  | 0,00    | USD      |
| ARP-10031  |  Greiðsla         | 7/8/2015  |         |                                      | 693,00                                | 0,00    | USD      |
| DISC-1031  |  Staðgreiðsluafsláttur   | 7/8/2015  |         |                                      | 7,00                                  | 0,00    | USD      |






