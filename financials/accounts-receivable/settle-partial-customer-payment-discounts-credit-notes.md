---
title: "Jafna hlutgreiðslu viðskiptavinar sem er með afslætti á kreditnótum"
description: "Þessi grein fer með þig í gegnum aðstæður þar sem staðgreiðsluafsláttur er tekinn á kreditnótu þegar upphaflegi reikningurinn var einnig með staðgreiðsluafslátt."
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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: Shiva.Pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4fbbd4d4b4ff9ecfcb30cd0ded2bc366d07dc1c4
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017

---

# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>Jafna hlutgreiðslu viðskiptavinar sem er með afslætti á kreditnótum

[!include[banner](../includes/banner.md)]


Þessi grein fer með þig í gegnum aðstæður þar sem staðgreiðsluafsláttur er tekinn á kreditnótu þegar upphaflegi reikningurinn var einnig með staðgreiðsluafslátt. 

Fabrikam gerir viðskiptavinum kleift að taka staðgreiðsluafslátt á hlutagreiðslur og einnig á kreditnótum (kreditreikningar). Hægt er að taka staðgreiðsluafslátt á kreditnótu þegar kreditnótan er gefið út fyrir reikning sem viðskiptavinur tók staðgreiðsluafsláttur út á. Í stað þess að veita lánsfé fyrir allri upphæðinni, geturðu skuldfærð stöðu viðskiptavinar fyrir upphæð sem tekur ekki með staðgreiðsluafsláttarprósentu sem viðskiptavinurinn tók. Uppgjörsfæribreytur eru staðsettar á síðunni **Færibreytur viðskiptakrafna**.

## <a name="invoice-and-credit-note"></a>Reikningur og Kreditnóta
Viðskiptavinur 4035 er með reikning fyrir 1.000,00 og kreditnótu fyrir 100,00. Hvert skjal er með 1 prósent afsláttur ef hún er greidd innan 14 daga. Arnie getur skoðað þessar upplýsingar á síðunni **viðskiptavinarfærslur**.

| Fylgiskjal    | Færslugerð | Dagsetning      | Reikningur  | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða  | Gjaldmiðill |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10050  | Reikningur          | 6/28/2015 | 10050    | 1.000,00                             |                                       | 1.000,00 | USD      |
| CCRN-10050 | Kreditnóta      | 6/28/2015 | CR-10050 |                                      | 100,00                                | -100,00  | USD      |

## <a name="settle-a-credit-note-with-an-invoice"></a>Jafna kreditnótuna við reikning
Úr **viðskiptavinafærslur** síðuna opnar Arnie **Jafna færslur** síðu. Hann getur nota í **Jafna færslur** síðu til að jafna reikninginn og kreditnótu. Hluti af jöfnunarferlið er að hann skoðar dagsetningar staðgreiðsluafslátts og upphæðir. Merkir tvær skjöl og síðan smellir **Bóka** til að jafna færslur. Það Er afsláttur -1.00 á kreditnótu, þar sem Fabrikam leyfir afslátt á kreditnótum.

| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal    | Reikningur | Dagsetning      | Gjalddagi  | Reikningur  | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Valið | Venjulegt            | FTI-10050  | 4035    | 6/28/2015 | 7/28/2015 | 10050    | 1.000,00                       | USD      | 990,00           |
| Valið | Venjulegt            | CCRN-10050 | 4035    | 6/28/2015 | 7/28/2015 | CR-10050 | -100,00                        | USD      | 99,00           |

Afsláttarupplýsingarnar birtist neðst á **Jafna færslur** síðunni.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/12/2015 |
| Upphæð staðgreiðsluafsláttar         | 1.00     |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 0,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | 1.00     |

Jöfnun verða 100,00 og mun innihalda greiðslu 99.00 og afslætti á 1,00.




