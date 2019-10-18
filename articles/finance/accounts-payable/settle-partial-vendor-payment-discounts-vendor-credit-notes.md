---
title: Jafna hlutgreiðslu lánardrottins sem er með afslætti á kreditnótum lánardrottins
description: Þessi grein fer með þig í gegnum aðstæður þar sem kreditreikningur er jafnaður gagnvart reikningi.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14222
ms.assetid: 2b19f7fd-9ff9-4ee4-bddf-f582946d008e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 923ab0305ac75c1156984c7a6d051f036479a16d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178350"
---
# <a name="settle-a-partial-vendor-payment-that-has-discounts-on-vendor-credit-notes"></a>Jafna hlutgreiðslu lánardrottins sem er með afslætti á kreditnótum lánardrottins

[!include [banner](../includes/banner.md)]

Þessi grein fer með þig í gegnum aðstæður þar sem kreditreikningur er jafnaður gagnvart reikningi.

lánardrottnar Fabrikam veita staðgreiðsluafslátt á kreditnótum. lánardrottni 3050 leyfir   Fabrikam að taka 1 prósent staðgreiðsluafslátt ef reikningurinn er greiddur innan 14 daga.

## <a name="invoice-and-credit-memo"></a>Reikningur og kreditreikningur
29. júní býr Apríl til reikning uppá 1.000,00 fyrir lánardrottinn 3050. 2. júlí stofnar hún kreditnótu fyrir 200,00. Úr **lánardrottins** síðuna opnar April **Jafna færslur** síðu. Hún getur nota **Jafna færslur** síðu til að merkja bæði kreditnótu og reikninginn til jöfnunar. Afsláttur upp á 2.00 er reiknaður á kreditnótunni. Þess vegna heildarvirði kreditnótu minnkað í 198.00.

| Merkja                     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valið                 | Venjulegt            | Inv-10070 | 3050    | 6/29/2015 | 7/29/2015 | 10070   | -1.000,00                      | USD      | -990,00          |
| Valdar og auðkenndar. | Venjulegt            | CR-10070  | 3050    | 7/2/2015  | 7/29/2015 |         | 200,00                         | USD      | 198.00           |

Afsláttarupplýsingarnar fyrir kreditnótuna birtist neðst á síðunni **Jafna opnar færslur** síðunni.

|                              |           |
|------------------------------|-----------|
| Dagsetning staðgreiðsluafsláttar           | 7/13/2015 |
| Upphæð staðgreiðsluafsláttar         | 2,00      |
| Nota staðgreiðsluafslátt            | Venjulegt    |
| Notaður staðgreiðsluafsláttur          | 0,00      |
| Upphæð staðgreiðsluafsláttar sem á að veita | 2,00      |

Apríl smellir **Bóka**. Hún endurskoðar síðan lokna jöfnun. Apríl sér að 198.00 af kreditnótu var notuð og afslátt uppá 2,00 var tekinn. Þess vegna er samtalan 200.00.

| Merkja                     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur  | Upphæð í gjaldmiðli færslu | Gjaldmiðill | Upphæð til jöfnunar |
|--------------------------|-------------------|-----------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Valdar og auðkenndar. | Venjulegt            | Inv-10070 | 3050    | 6/29/2015 | 7/29/2015 | 10070    | -1.000,00                      | USD      | 200.00          |
| Valið                 | Venjulegt            | CR-10070  | 3050    | 7/2/2015  | 7/29/2015 | CR-10070 | 200,00                         | USD      | 198.00           |

Apríl getur fara yfir lánardrottnafærslur á **lánardrottnafærslur** síðu með því að velja lánardrottin á **Allir lánardrottnar** síðuna og síðan á Aðgerðasvæðinu skal á smellla **Færslur**. Á þessari síðu sér April að reikningurinn hefur stöðuna -800,00. Hún sér einnig kreditnótu fyrir 198.00 og afslátt 2,00.

| Fylgiskjal    | Færslugerð | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða | Gjaldmiðill |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10070  | Reikningur          | 6/29/2015 | 10070   |                                      | 1.000,00                              | -800.00 | USD      |
| Inv-10071  |                  | 7/2/2015  | CR10071 | 200,00                               |                                       | 0,00    | USD      |
| DISC-10071 |  Staðgreiðsluafsláttur   | 7/2/2015  |         | 2,00                                 |                                       | 0,00    | USD      |
| DISC-10071 |  Staðgreiðsluafsláttur   | 7/2/2015  |         |                                      | 2,00                                  | 0,00    | USD      |





