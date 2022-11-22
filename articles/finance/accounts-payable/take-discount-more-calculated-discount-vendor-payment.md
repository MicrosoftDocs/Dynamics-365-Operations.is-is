---
title: Taka meiri afslátt en reiknaður afsláttur fyrir greiðslu lánardrottins
description: Þessi grein fer í gegnum aðstæður þar sem staðgreiðsluafsláttur er tekinn fyrir upphæð sem er hærri en afslátturinn sem var upphaflega tiltækur á reikningnum. Þessar aðstæður gætu komið upp ef fyrirtæki kemst að samkomulagi við lánardrottin að borga minni upphæð inn á reikninginn.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd74c6677f80a9075449908411350f1c81b95b02
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778358"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a>Taka meiri afslátt en reiknaður afsláttur fyrir greiðslu lánardrottins

[!include [banner](../includes/banner.md)]

Þessi grein fer í gegnum aðstæður þar sem staðgreiðsluafsláttur er tekinn fyrir upphæð sem er hærri en afslátturinn sem var upphaflega tiltækur á reikningnum. Þessar aðstæður gætu komið upp ef fyrirtæki kemst að samkomulagi við lánardrottin að borga minni upphæð inn á reikninginn. 

Lánardrottni 3051 gefur Fabrikam 4 prósent staðgreiðsluafslátt ef reikningurinn er greiddur innan sjö daga. Þann 29. júní færir Apríl inn reikning uppá 1.000,00. Lánardrottinninn heimilar Apríl að taka afslátt upp á 60,00 í staðinn fyrir sjálfgefinn afslátt upp á 40,00 sem er tiltækur fyrir reikninginn. Apríl skráir eingreiðslu með því að nota greiðslubók viðskiptaskulda. Hún færir inn lánardrottinn fyrir greiðsluna og opnar svo síðuna **Jafna færslur**. Hún merkir reikninginn og breytir gildinu í reitnum **Upphæð staðgreiðsluafsláttar** í **60,00**.

| Merkja     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valið | Venjulegt            | Reikn-10040 | 3051    | 6/29/2020 | 7/29/2020 | 10040   | 1,000.00                       | USD      | 940,00           |

Afsláttarupplýsingarnar birtist neðst á **Jafna færslur** síðunni.

| Svæði                        | Gildi     |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/12/2020 |
| Upphæð staðgreiðsluafsláttar         | 60.00     |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 0,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | 60,00     |

Apríl bókar greiðslubókina. Reikningurinn er fulljafnaður með greiðslu upp á 940,00 og afslátt upp á 60,00.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
