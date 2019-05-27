---
title: Jafna hlutagreiðslu lánardrottins fyrir afsláttardagsetninguna með lokagreiðslu eftir afsláttardagsetninguna
description: Þessi grein fer í gegnum aðstæður þar sem margar hlutagreiðslur eru greiddar, sumar innan staðgreiðsluafsláttartímabils og önnur utan staðgreiðsluafsláttartímabilsins.
author: abruer
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14411
ms.assetid: 302ad6ae-28ee-4899-9f6b-f74424a5f50c
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b44d3d561b5d7fdccf34d2220d5ade0d3974ea8b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1512269"
---
# <a name="settle-a-partial-vendor-payment-before-the-discount-date-with-a-final-payment-after-the-discount-date"></a>Jafna hlutagreiðslu lánardrottins fyrir afsláttardagsetninguna með lokagreiðslu eftir afsláttardagsetninguna

[!include [banner](../includes/banner.md)]

Þessi grein fer í gegnum aðstæður þar sem margar hlutagreiðslur eru greiddar, sumar innan staðgreiðsluafsláttartímabils og önnur utan staðgreiðsluafsláttartímabilsins.

Fabrikam kaupir vörur frá lánardrottni 3057. Fabrikam fær 1 prósent afslátt ef reikningurinn er greiddur innan 14 daga. Greiða þarf reikninga eftir 30 daga. Lánardrottinn veitir Fabrikam einnig staðgreiðsluafslátt á hlutagreiðslum. Uppgjörsfæribreytur eru staðsettar á síðunni **Færibreytur viðskiptaskulda**.

## <a name="invoice-on-june-25"></a>Reikningur 25. júní
25. júní færir Apríl inn og bókar reikning uppá 1.000,00 fyrir lánardrottinn 3057. Arnie getur skoðað þessa færslu á síðunni **lánardrottnafærslur**.

| Fylgiskjal   | Færslugerð | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða   | Gjaldmiðill |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10020 | Reikningur          | 6/25/2015 | 10020   |                                      | 1.000,00                              | -1.000,00 | USD      |

## <a name="partial-payment-on-july-2"></a>Hlutagreiðsla 2. júlí
Arnie vill greiða 300,00 af þessum reikningi þann 2. júlí. Greiðslan gefur rétt á afslætti, þar sem Fabrikam gefur afslætti á hlutagreiðslur. Þess vegna greiðir Arnie 297,00 og fær 3,00 afslátt. Hún stofnar nýja færslubók og færir inn línu fyrir lánardrottin 3057. Hún opnar síðuna **Jafna færslur** svo að hún geti merkt reikninginn fyrir jöfnun.

| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valið | Venjulegt            | Inv-10020 | 3057    | 6/25/2015 | 7/25/2015 | 10020   | -1.000,00                      | USD      | -297,00          |

Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/09/2015 |
| Upphæð staðgreiðsluafsláttar         | -10,00    |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 0,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | -3,00     |

Arnie bókar síðan greiðsluna. Reikningurinn hefur núna stöðuna 700,00. Arnie getur skoðað þessa færslu á síðunni **lánardrottnafærslur**.

| Fylgiskjal    | Færslugerð | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða | Gjaldmiðill |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Reikningur          | 6/25/2015 | 10020   |                                      | 1.000,00                              | -700,00 | USD      |
| APP-10020  | Greiðsla          | 7/1/2015  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Staðgreiðsluafsláttur    | 7/1/2015  |         | 3,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--normal"></a>Eftirstöðvar 15. Júlí, Nota staðgreiðsluafslátt = Venjuleg
Arnie greiðir eftirstöðvar reikningsins 15.júlí, sem er eftir afsláttartímabilið. Á síðunni **Jafna opnar færslur** , engin afsláttarupphæð birtist á **Áætlaður staðgreiðsluafsláttur**svæði og gildið á svæðinu **upphæð staðgreiðsluafsláttar** er **0,00**. Þegar Arnie greiðir eftirstandandi 700,00 verður ekki veittur frekari afsláttur.

| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valið | Venjulegt            | Inv-10020 | 3057    | 6/25/2015 | 7/25/2015 | 10020   | -700,00                        | USD      | -700,00          |

Afsláttarupplýsingarnar birtist neðst á **Jafna færslur** síðunni. Arnie getur séð að hún hefur þegar fengið afslátt upp á 3,00.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/09/2015 |
| Upphæð staðgreiðsluafsláttar         | 0,00      |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | -3,00     |
| Upphæð staðgreiðsluafsláttar sem á að veita | 0,00      |

Arnie bókar síðan greiðsluna. Þegar hún opnar síðuna **lánardrottnafærslur** sér hún að reikningurinn hefur stöðuna 0,00. Hún sér einnig að það eru tvær greiðslur. Eina greiðslu fyrir 297,00 og 3,00 afslátt, og aðra greiðslu fyrir 700,00.

| Fylgiskjal    | Færslugerð | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða | Gjaldmiðill |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Reikningur          | 6/25/2015 | 10020   |                                      | 1.000,00                              | 0,00    | USD      |
| APP-10020  | Greiðsla          | 7/1/2015  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Staðgreiðsluafsláttur    | 7/1/2015  |         | 3,00                                 |                                       | 0,00    | USD      |
| APP-10021  | Greiðsla          | 7/15/2015 |         | 700.00                               |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--always"></a>Eftirstöðvar 15. Júlí, Nota staðgreiðsluafslátt = Alltaf
Ef lánardrottinn leyfir Arnie að fá afslátt jafnvel þó að hún sé að greiða eftir afsláttardagsetningu getur hún breytt gildinu á svæðinu **Nota staðgreiðsluafslátt** í **Alltaf**. **Reikna staðgreiðsluafslætti fyrir hlutagreiðslur** er hnekkt og afsláttur er veittur. Greiðsluupphæðin er 693,00 og afslátturinn er eftirstandandi 7,00.

| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valið | Alltaf            | Inv-10020 | 3057    | 6/25/2015 | 7/25/2015 | 10020   | 700.00                               |                                       | USD      | -693,00          |

Afsláttarupplýsingarnar birtist neðst á **Jafna færslur** síðunni.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/09/2015 |
| Upphæð staðgreiðsluafsláttar         | 7,00      |
| Nota staðgreiðsluafslátt            | Alltaf    |
| Notaður staðgreiðsluafsláttur          | -3,00     |
| Upphæð staðgreiðsluafsláttar sem á að veita | -7,00     |

Arnie bókar síðan greiðsluna. Þegar hún opnar síðuna **lánardrottnafærslur** sér hún að reikningurinn hefur stöðuna 0,00. Hún sér einnig að það eru tvær greiðslur. Ein greiðsla er fyrir 297,00 og er með afslátt upp á 3,00. Hin greiðslan er fyrir 693,00 og er með afslátt upp á 7,00.

| Fylgiskjal    | Færslugerð | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða | Gjaldmiðill |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Reikningur          | 6/25/2015 | 10020   |                                      | 1.000,00                              | 0,00    | USD      |
| APP-10020  | Greiðsla          | 7/1/2015  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Staðgreiðsluafsláttur    | 7/1/2015  |         | 3,00                                 |                                       | 0,00    | USD      |
| APP-10021  | Greiðsla          | 7/15/2015 |         | 693,00                               |                                       | 0,00    | USD      |
| DISC-10021 | Staðgreiðsluafsláttur    | 7/15/2015 |         | 7,00                                 |                                       | 0,00    | USD      |





