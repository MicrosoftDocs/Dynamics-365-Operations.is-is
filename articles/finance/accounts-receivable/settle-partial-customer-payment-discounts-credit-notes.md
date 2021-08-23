---
title: Jafna hlutgreiðslu viðskiptavinar sem er með afslætti á kreditnótum
description: Þessi grein fer með þig í gegnum aðstæður þar sem staðgreiðsluafsláttur er tekinn á kreditnótu þegar upphaflegi reikningurinn var einnig með staðgreiðsluafslátt.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6476fed0ac10888c51266128f950fc0e1418b13c743894ab0992d051e733c4e1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740147"
---
# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>Jafna hlutgreiðslu viðskiptavinar sem er með afslætti á kreditnótum

[!include [banner](../includes/banner.md)]

Þessi grein fer með þig í gegnum aðstæður þar sem staðgreiðsluafsláttur er tekinn á kreditnótu þegar upphaflegi reikningurinn var einnig með staðgreiðsluafslátt. 

Fabrikam gerir viðskiptavinum kleift að taka staðgreiðsluafslátt á hlutagreiðslur og einnig á kreditnótum (kreditreikningar). Hægt er að taka staðgreiðsluafslátt á kreditnótu þegar kreditnótan er gefið út fyrir reikning sem viðskiptavinur tók staðgreiðsluafsláttur út á. Í stað þess að veita lánsfé fyrir allri upphæðinni, geturðu skuldfærð stöðu viðskiptavinar fyrir upphæð sem tekur ekki með staðgreiðsluafsláttarprósentu sem viðskiptavinurinn tók. Uppgjörsfæribreytur eru staðsettar á síðunni **Færibreytur viðskiptakrafna**.

## <a name="invoice-and-credit-note"></a>Reikningur og Kreditnóta
Viðskiptavinur 4035 er með reikning fyrir 1.000,00 og kreditnótu fyrir 100,00. Hvert skjal er með 1 prósent afsláttur ef hún er greidd innan 14 daga. Arnie getur skoðað þessar upplýsingar á síðunni **viðskiptavinarfærslur**.

| Fylgiskjal    | Færslugerð | Dagsetning      | Reikningur  | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða  | Gjaldmiðill |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10050  | Reikningur          | 6/28/2015 | 10050    | 1.000,00                             |                                       | 1.000,00 | USD      |
| CCRN-10050 | Kreditnóta      | 6/28/2015 | CR-10050 |                                      | 100,00                                | -100,00  | USD      |

## <a name="settle-a-credit-note-with-an-invoice"></a>Jafna kreditnótuna við reikning
Úr **viðskiptavinafærslur** síðuna opnar Arnie **Jafna færslur** síðu. Arnie getur nota í **Jafna færslur** síðu til að jafna reikninginn og kreditnótu. Hluti af jöfnunarferlinu er að Arni skoðar dagsetningar staðgreiðsluafslátts og upphæðir. Arnie merkir tvö skjöl og smellir svo á **Bóka** til að jafna færslur. Það Er afsláttur -1.00 á kreditnótu, þar sem Fabrikam leyfir afslátt á kreditnótum.

| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal    | Reikningur | Dagsetning      | Gjalddagi  | Reikningur  | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Valið | Venjulegt            | FTI-10050  | 4035    | 6/28/2015 | 7/28/2015 | 10050    | 1.000,00                       | USD      | 990,00           |
| Valið | Venjulegt            | CCRN-10050 | 4035    | 6/28/2015 | 7/28/2015 | CR-10050 | -100,00                        | USD      | 99,00           |

Afsláttarupplýsingarnar birtist neðst á **Jafna færslur** síðunni.

- **Dagsetning staðgreiðsluafsláttar**: 12/07/2015 
- **Upphæð staðgreiðsluafsláttar**: -1.00     
- **Nota staðgreiðsluafslátt**: Venjulegt    
- **Notaður staðgreiðsluafsláttur**: 0.00      
- **Upphæð staðgreiðsluafsláttar sem á að veita**: -1.00     

Jöfnun verða 100,00 og mun innihalda greiðslu 99.00 og afslætti á 1,00.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]