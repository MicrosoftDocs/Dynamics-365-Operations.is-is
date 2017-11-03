---
title: "Jafna hlutagreiðsla lánardrottins og endanleg greiðslu að fullu fyrir afsláttardagsetninguna"
description: "Þessi grein fer í gegnum aðstæður þar sem hlutagreiðslur eru greiddar fyrir reikning lánardrottins og staðgreiðsluafsláttur er tekinn."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14431
ms.assetid: 6b8e3420-b4c9-4e02-9588-598fe6d3df0d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8436f7456f7a19320afa83ceb970d9cd0c64ac68
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="settle-a-partial-vendor-payment-and-the-final-payment-in-full-before-the-discount-date"></a>Jafna hlutagreiðsla lánardrottins og endanleg greiðslu að fullu fyrir afsláttardagsetninguna

[!include[banner](../includes/banner.md)]


Þessi grein fer í gegnum aðstæður þar sem hlutagreiðslur eru greiddar fyrir reikning lánardrottins og staðgreiðsluafsláttur er tekinn.

Fabrikam kaupir vörur frá lánardrottni 3064. Lánardrottinn veitir Fabrikam 1 prósent staðgreiðsluafslátt ef reikningurinn er greiddur innan 14 daga. Greiða þarf reikninga eftir 30 daga. Lánardrottinn veitir Fabrikam einnig staðgreiðsluafslátt á hlutagreiðslum. Uppgjörsfæribreytur eru staðsettar á síðunni **Færibreytur viðskiptaskulda**. 25. júní færir Apríl inn reikning uppá 1.000,00 fyrir lánardrottinn 3064.

## <a name="vendor-invoice-on-june-25"></a>Reikningur 25. júní
25. júní færir Apríl inn og bókar reikning uppá 1.000,00 fyrir lánardrottinn 3064. Arnie getur skoðað þessa færslu á síðunni **lánardrottnafærslur**.

| Fylgiskjal   | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða   | Gjaldmiðill |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10010 | 6/25/2015 | 10010   |                                      | 1.000,00                              | -1.000,00 | USD      |

Úr **lánardrottins** síðuna opnar April **Jafna færslur** síðu. Hún getur notað **Jafna færslur** síðu til að skoða dagsetningar og upphæðir á staðgreiðsluafslætti. Gjalddagi er 25 Júlí og staðgreiðsluafsláttur uppá -10,00 er tiltæk ef reikningurinn er greiddur fyrir 9 Júlí.

| Merkja | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Venjulegt            | Inv-10010 | 3064    | 6/25/2015 | 7/25/2015 | 10010   | 1.000,00                       | USD      | 990,00           |

Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/09/2015 |
| Upphæð staðgreiðsluafsláttar         | -10,00    |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 0,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | -10,00    |

April smellir á **staðgreiðsluafsláttur** flipa til að skoða afsláttarupphæð.

| Dagsetning staðgreiðsluafsláttar | Upphæð staðgreiðsluafsláttar | Upphæð í gjaldmiðli færslu |
|--------------------|----------------------|--------------------------------|
| 7/9/2015           | 10,00                | 990,00                         |
| 7/25/2015          | 0,00                 | 1.000,00                       |

## <a name="partial-payment-on-july-1-by-using-the-settle-transactions-page"></a>Hlutagreiðsla 1. Júlí með því að nota síðuna Jafna færslur
Apríl getur stofna greiðslubók fyrir þessa greiðslu með því að opna í **greiðslubók** síðu í viðskiptaskuldir. Hún stofnar nýja færslubók og færir inn línu fyrir lánardrottin 3064. Hún opnar síðuna **Jafna færslur** svo að hún geti merkt reikninginn fyrir jöfnun. April merkir reikninginn og breytir gildi í **Upphæðin til jöfnunar** reit í  **-500,00**. Hún sér að gildið í á **upphæð staðgreiðsluafsláttar** er **-10,00** fyrir fullan reikning og gildið í á **upphæð staðgreiðsluafsláttar sem á að taka** er **-5.05**. Þess vegna er apríl að jafna -505.05 fyrir þennan reikning.

| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valið | Venjulegt            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1.000,00                       | USD      | -500,00          |

Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/09/2015 |
| Upphæð staðgreiðsluafsláttar         | -10,00    |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 0,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | -5,05     |

Apríl vill jafna nákvæmlega helming reiknings Þessvegna breytir hún gildi í **Upphæðin til jöfnunar** reit í  **-495,00**. heildarupphæðin sem er jöfnuð er nú 500,00. Þessi upphæð inniheldur -5,00 staðgreiðsluafslátt.

| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valið | Venjulegt            | FTI-10010 | 4028    | 6/25/2015 | 7/25/2015 | 10010   | 1.000,00                       | USD      | -495,00          |

Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/09/2015 |
| Upphæð staðgreiðsluafsláttar         | -10,00    |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 0,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | -5,00     |

Apríl Lokar **Jafna færslur** síðu. Greiðslulína fyrir 495.00 er stofnuð í færslubók og þá bókar Apríl færslubókina. Apríl getur skoðað lánardrottnafærslur á síðunni **Lánardrottnafærslur**. Hún sér að reikningurinn hefur stöðuna 500,00. Hún sér einnig greiðslu uppá 495.00 og staðgreiðsluafsláttur 5,00.

| Fylgiskjal    | Færslugerð | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða | Gjaldmiðill |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10010  | Reikningur          | 6/25/2015 | 10010   |                                      | 1.000,00                              | -500,00 | USD      |
| APP-10010  | Greiðsla          | 7/1/2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10010 | Staðgreiðsluafsláttur    | 7/1/2015  |         | 5,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-amount-paid-on-july-8"></a>Eftirstandandi upphæð greiddar Júlí 8
Apríl greiðir afgang reiknings fyrir lánadrottinn 3064 á Júlí 8, sem er innan tímabils staðgreiðsluafsláttar. Apríl stofnar greiðslubók á 8 Júlí og merkir færsluna til jöfnunar. Hún sér að Upphæðin sem þarf að jafna er 495.00 . Gildið í á **Áætlaður staðgreiðsluafsláttur** er **-5,00** því 5,00 afslátturinn var áður tekinn af.

|                         |        |
|-------------------------|--------|
| Heildarmerking            | 495,00 |
| Áætlaður staðgreiðsluafsláttur | -5,00  |

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

Apríl bókar greiðslubók og fer yfir lánardrottnafærslur á við **lánardrottnafærslur** síðu. Staða reiknings er nú 0,00 og apríl sér tvo staðgreiðsluafslátta og tvær greiðslur.

| Fylgiskjal    | Færslugerð | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða | Gjaldmiðill |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10010  | Reikningur          | 6/25/2015 | 10010   |                                      | 1.000,00                              | 0,00    | USD      |
| APP-10010  |  Greiðsla         | 7/1/2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10010 | Staðgreiðsluafsláttur    | 7/1/2015  |         | 5,00                                 |                                       | 0,00    | USD      |
| APP-10011  | Greiðsla          | 7/8/2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10011 | Staðgreiðsluafsláttur    | 7/8/2015  |         | 5,00                                 |                                       | 0,00    | USD      |






