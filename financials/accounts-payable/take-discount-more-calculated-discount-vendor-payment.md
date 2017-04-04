---
title: "Taka afsláttar sem er meira en reiknaður afsláttur fyrir greiðslu lánardrottins"
description: "Þessi grein fer í gegnum aðstæður þar sem staðgreiðsluafsláttur er tekinn fyrir upphæð sem er hærri en afslátturinn sem var upphaflega tiltækur á reikningnum. Þessar aðstæður gætu komið upp ef fyrirtæki kemst að samkomulagi við lánardrottin að borga minni upphæð inn á reikninginn."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 22ba73681faa509a5144517163cc173a1267a534
ms.lasthandoff: 03/31/2017


---

# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a>Taka afsláttar sem er meira en reiknaður afsláttur fyrir greiðslu lánardrottins

Þessi grein fer í gegnum aðstæður þar sem staðgreiðsluafsláttur er tekinn fyrir upphæð sem er hærri en afslátturinn sem var upphaflega tiltækur á reikningnum. Þessar aðstæður gætu komið upp ef fyrirtæki kemst að samkomulagi við lánardrottin að borga minni upphæð inn á reikninginn. 

Lánardrottni 3051 gefur Fabrikam 4 prósent staðgreiðsluafslátt ef reikningurinn er greiddur innan sjö daga. Þann 29. júní færir Apríl inn reikning uppá 1.000,00. Lánardrottinninn heimilar Apríl að taka afslátt upp á 60,00 í staðinn fyrir sjálfgefinn afslátt upp á 40,00 sem er tiltækur fyrir reikninginn. Apríl skráir eingreiðslu með því að nota greiðslubók viðskiptaskulda. Hann færir inn lánardrottins fyrir greiðslu og svo opnar það **Jafna færslur** síðu. Hún merkir reikninginn og breytir gildi í í **upphæð staðgreiðsluafsláttar** svæðinu **60,00**.
| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valið | Venjulegt            | Reikn-10040 | 3051    | 6/29/2015 | 7/29/2015 | 10040   | 1.000,00                       | USD      | 940,00           |

Afsláttarupplýsingarnar birtist neðst á **Jafna færslur** síðunni.
|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/12/2015 |
| Upphæð staðgreiðsluafsláttar         | 60,00     |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 0,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | 60,00     |

Apríl bókar greiðslubókina. Reikningurinn er fulljafnaður með greiðslu upp á 940,00 og afslátt upp á 60,00.


