---
title: Nota eina greiðslu til að jafna reikninga sem ná yfir margar afsláttartímabil
description: Þetta efnisatriði sýnir hvernig margir reikningar eru greiddir þegar hver reikningur getur veitt staðgreiðsluafslátt. Dæmin sem gefin eru í þessari grein varpa ljósi á hvernig staðgreiðsluafsláttur getur verið mismunandi, með hliðsjón af því hvenær greiðslan er gerð.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14511
ms.assetid: 3e42ccb5-b9d7-4a70-8db9-4206d10fd433
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e45004c9f93963fb886039165f16ccc6a3f98f5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991292"
---
# <a name="use-one-payment-to-settle-invoices-that-span-multiple-discount-periods"></a>Nota eina greiðslu til að jafna reikninga sem ná yfir margar afsláttartímabil

[!include [banner](../includes/banner.md)]

Þetta efnisatriði sýnir hvernig margir reikningar eru greiddir þegar hver reikningur getur veitt staðgreiðsluafslátt. Dæmin sem gefin eru í þessari grein varpa ljósi á hvernig staðgreiðsluafsláttur getur verið mismunandi, með hliðsjón af því hvenær greiðslan er gerð.

Fabrikam selur vörurn til 4032 viðskiptavina. Fabrikam býður 1 prósent afslátt ef reikningurinn er greiddur innan 14 daga. Fabrikam býður einnig upp á staðgreiðsluafslætti fyrir hlutagreiðslur. Uppgjörsfæribreytur eru staðsettar á síðunni **Færibreytur viðskiptakrafna**.

## <a name="invoices"></a>Reikningar
viðskiptavinur 4032 er með þrjá reikninga uppá samtals 3.000,00:

-   Reikningur með frjálsum texta reikningur FTI-10040, fyrir 1.000,00, var fært inn þann 15. maí. Þessi reikningur er hæf til um staðgreiðsluafslátt uppá 1 prósent ef hún er greidd innan 14 daga.
-   Reikningur með frjálsum texta reikningur FTI-10041, fyrir 1.000,00, var fært inn þann 25. júní. Þessi reikningur er hæf til um staðgreiðsluafslátt uppá 1 prósent ef hún er greidd innan 14 daga.
-   Reikningur með frjálsum texta reikningur FTI-10042, fyrir 1.000,00, var fært inn þann 25. júní. Þessi reikningur er hæf til um staðgreiðsluafslátt uppá 2 prósent ef borgað innan fimm daga og afslátt uppá 1 prósent ef hún er greidd innan 14 daga.

## <a name="settle-all-invoices-on-june-29"></a>Jafna alla reikninga 29. júní
Ef Arnie stofnar greiðslubók til að jafna að fullu þessar reikninga á 29. júní, er greiðslan 2.970,00. Samtala allra afsláttarupphæða er 30,00. Arnie stofnar greiðslu fyrir viðskiptavin 4032 og opnar svo **Jafna færslur** síðuna. Á **Jafna færslur** síðunni merkir Arnie allar þrjár reikningslínur fyrir jöfnun:

-   Greiðsla fyrir reikning FTI-10040 er 1.000,00. Enginn staðgreiðsluafsláttur er tekinn.
-   Greiðsla fyrir reikning FTI-10041 er 990.00. Staðgreiðsluafsláttur uppá 1 prósent, eða 10.00 er tekinn.
-   Greiðsla fyrir reikning FTI-10042 er 980.00. Staðgreiðsluafsláttur uppá 2 prósent, eða 20.00 er tekinn.

| Merkja                     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Gjaldmiðill | Upphæð til jöfnunar |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valið                 | Venjulegt            | FTI-10040 | 4032    | 5/15/2015 | 6/15/2015 | 10040   | 1.000,00                             |                                       | USD      | 1.000,00         |
| Valið                 | Venjulegt            | FTI-10041 | 4032    | 6/25/2015 | 7/25/2015 | 10041   | 1.000,00                             |                                       | USD      | 990,00           |
| Valdar og auðkenndar. | Venjulegt            | FTI-10042 | 4032    | 6/25/2015 | 7/25/2015 | 10042   | 1.000,00                             |                                       | USD      | 980,00           |

Eftir að greiðslan er bókuð er staða viðskiptavinar 0,00.

## <a name="settle-all-invoices-on-july-1"></a>Jafna allir reikningar á 1. Júní
Ef Arnie stofnar greiðslubók til að jafna að fullu þessar reikninga á 1. júlí, er greiðslan 2.980,00. Arnie stofnar greiðslu fyrir viðskiptavin 4032 og opnar svo **Jafna færslur** síðuna. Á **Jafna færslur** síðunni merkir Arnie allar þrjár reikningslínur fyrir jöfnun:

-   Greiðsla fyrir reikning FTI-10040 er 1.000,00. Enginn staðgreiðsluafsláttur er tekinn.
-   Greiðsla fyrir reikning FTI-10041 er 990.00. Staðgreiðsluafsláttur uppá 1 prósent, eða 10.00 er tekinn.
-   Greiðsla fyrir reikning FTI-10042 er 990.00. Staðgreiðsluafsláttur uppá 1 prósent, eða 10.00 er tekinn. Þótt 1. Júlí sé eftir tímabili sem uppfyllir skilyrði fyrir afsláttinn 2 prósent, er það enn í tímabilinu sem uppfyllir skilyrði fyrir afsláttinn 1 prósent.

| Merkja                     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Gjaldmiðill | Upphæð til jöfnunar |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valið                 | Venjulegt            | FTI-10040 | 4032    | 5/15/2015 | 6/15/2015 | 10040   | 1.000,00                             |                                       | USD      | 1.000,00         |
| Valið                 | Venjulegt            | FTI-10041 | 4032    | 6/25/2015 | 7/25/2015 | 10041   | 1.000,00                             |                                       | USD      | 990,00           |
| Valdar og auðkenndar. | Venjulegt            | FTI-10042 | 4032    | 6/25/2015 | 7/25/2015 | 10042   | 1.000,00                             |                                       | USD      | 990,00           |

## <a name="partial-settlement-on-june-29"></a>Hlutauppgjör á 29. júní
viðskiptavinurinn 4032 getur greitt hluta af upphæð eins og helming hvers reiknings. Arnie stofnar greiðslu fyrir viðskiptavin 4032 og opnar svo **Jafna færslur** síðuna. Á **Jafna færslur** síðu Arnie merkir allar þrjár reikningslínur fyrir jöfnun: Í hverri línu, færir hann inn upphæðin til jöfnunar, byggt á leiðbeiningunum sem viðskiptavinar veitti. Þegar Arnie velur línu, hann sér afsláttarupphæð fyrir þess línu og upphæð staðgreiðsluafsláttar sem er tekin. Þar sem viðskiptavinurinn greiðir hálft reiknings, sér Arnie að gildi í svæðinu **upphæð staðgreiðsluafsláttar** fyrir er FTI-10042 er **20,00**, en gildið í á **staðgreiðsluafsláttur tekinn** er **10,00**. Greiðsluupphæðin er 1.485,00

| Merkja                     | Nota staðgreiðsluafslátt | Fylgiskjal   | Reikningur | Dagsetning      | Gjalddagi  | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Gjaldmiðill | Upphæð til jöfnunar |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Valið                 | Venjulegt            | FTI-10040 | 4032    | 5/15/2015 | 6/15/2015 | 10040   | 1.000,00                             |                                       | USD      | 500,00           |
| Valið                 | Venjulegt            | FTI-10041 | 4032    | 6/25/2015 | 7/25/2015 | 10041   | 1.000,00                             |                                       | USD      | 495,00           |
| Valdar og auðkenndar. | Venjulegt            | FTI-10042 | 4032    | 6/25/2015 | 7/25/2015 | 10042   | 1.000,00                             |                                       | USD      | 490,00           |

Arnie getur einnig færa handvirkt greiðsluupphæð 1,485.00 áður en hann opnar fyrir **Jafna færslur** síðu. Ef Arnie færir greiðsluupphæðina handvirkt og merkir síðan allar færslur þrjár en hann leiðrétta ekki að gildið í **Upphæðin til jöfnunar** svæði fyrir hverja færslu hann fær eftirfarandi skilaboð þegar hann lokar síðu:

> Heildarupphæð merktra færslna er ekki sú sama og færslubókarupphæð. Á að breyta færslubók upphæð?

Ef Arnie vill að greiðsluupphæðin sé aðeins 1,485.00 hann smellir **Nei** og bókar síðan færslubók. Færslurnar eru jafnaðar á eftirfarandi hátt:

1.  Reikningur FTI-10040 er jafnaður að fullu fyrir 1.000,00, þar sem hann var færður inn þann 15. Maí og er elsti reikningur. Enginn staðgreiðsluafsláttur er tekinn. Eftirstandandi upphæð á greiðslufærslu er 485,00.
2.  Reikningur FTI-10041 er alls ekki jafnaður. Reikningar FTI-10041 og FTI-10042 voru færðir inn á sömu dagsetningu. Hins vegar er 1 prósent afsláttur tiltækur fyrir reikning FTI-10041 og býðst 2 prósent staðgreiðsluafsláttur fyrir reikning FTI-10042 Því betri afsláttur er fyrir reikning FTI-10042 eru eftirstandandi 485,00 jöfnuð með reikningi FTI-10042
3.  FTI-10042 er jafnaður við eftirstandandi 485,00. Fabrikam býður upp á hlutaafslátt. Í þessu tilfelli er afsláttur 9,90 (= 485.00 ÷ 0.98 × 0.02). Upphæð (485,00) er deilt með 0.98, þar sem það eru 2 prósent afsláttur (því greiðir viðskiptavinur 98 prósent reikningsins). Niðurstaðan er síðan margfölduð með afsláttarprósentu, eða 2 prósent. Greiðslan 485.00 plús afslátturinn 9,90 jafngildir 494.90. Upphæð upphaflegs reiknings var 1,000.00 Þess vegna hefur færslan stöðu 505,10 (= 1.000,00 – 494,90).

April getur skoðað upplýsingar á síðunni **viðskiptavinarfærslur**.

| Fylgiskjal    | Færslugerð | Dagsetning      | Reikningur | Upphæð í færslugjaldmiðli - debet | Upphæð í færslugjaldmiðli - kredit | Staða  | Gjaldmiðill |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10040  | Reikningur          | 5/15/2015 | 10040   | 1.000,00                             |                                       | 0,00     | USD      |
| FTI-10041  | Reikningur          | 6/25/2015 | 10041   | 1.000,00                             |                                       | 1.000,00 | USD      |
| FTI-10042  | Reikningur          | 6/25/2015 | 10042   | 1.000,00                             |                                       | 505,10   | USD      |
| ARP 10040  | Greiðsla          | 6/29/2015 |         |                                      | 1.485,00                              | 0,00     | USD      |
| DISC-10040 | Staðgreiðsluafsláttur    | 6/29/2015 |         |                                      | 9,90                                  | 0,00     | USD      |





