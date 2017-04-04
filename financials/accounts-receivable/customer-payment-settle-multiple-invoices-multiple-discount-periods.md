---
title: "Greiðsla viðskiptavinar er notuð til að jafna marga reikninga sem ná yfir margar afsláttartímabil"
description: "Þessi grein sýnir hvernig margir reikningar eru greiddir þegar hver reikningur getur veitt staðgreiðsluafslátt. Dæmin sem gefin eru í greininni varpa ljósi á hvernig staðgreiðsluafsláttur getur verið mismunandi, með hliðsjón af því hvenær greiðslan er gerð."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14511
ms.assetid: 3e42ccb5-b9d7-4a70-8db9-4206d10fd433
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 6fd78a587d70ec371861084ac9f76b439c821a8f
ms.lasthandoff: 03/31/2017


---

# <a name="use-a-customer-payment-to-settle-multiple-invoices-that-span-multiple-discount-periods"></a>Greiðsla viðskiptavinar er notuð til að jafna marga reikninga sem ná yfir margar afsláttartímabil

Þessi grein sýnir hvernig margir reikningar eru greiddir þegar hver reikningur getur veitt staðgreiðsluafslátt. Dæmin sem gefin eru í greininni varpa ljósi á hvernig staðgreiðsluafsláttur getur verið mismunandi, með hliðsjón af því hvenær greiðslan er gerð.

Fabrikam selur vörurnar 4032 viðskiptavinar. Fabrikam býður upp á 1 prósent staðgreiðsluafslátt ef reikningurinn er greiddur á 14 daga. Fabrikam býður einnig upp á staðgreiðsluafslætti fyrir hlutagreiðslur. Færibreytur settement eru staðsett á **Færibreytur viðskiptakrafna** síðu.

## <a name="invoices"></a>Reikningar
viðskiptavinur 4032 er með þrjá reikninga uppá samtals 3.000,00:

-   Reikningur MEÐ-10040, fyrir 1000,00, var fært inn þann 15 Maí. Þessi reikningur er hæf til um 1 prósent staðgreiðsluafslátt ef hún er greidd í 14 daga.
-   Reikningur MEÐ-10041, fyrir 1000,00, var fært inn á 25. Júní. Þessi reikningur er hæf til um 1 prósent staðgreiðsluafslátt ef hún er greidd í 14 daga.
-   Reikningur MEÐ-10042, fyrir 1000,00, var fært inn á 25. Júní. Þessi reikningur er hæf til 2 prósent staðgreiðsluafslátt ef hún er greidd í fimm daga- og afsláttarupplýsingar um 1 prósent ef hún er greidd í 14 daga.

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

Arnie hægt að færa handvirkt greiðsluupphæðin 1,485.00 áður en hann opnar fyrir **Jafna færslur** síðu. Ef Arnie færir greiðsluupphæðin handvirkt og þá merkir allar færslur á þremur en hann ekki að leiðrétta gildið í á **Upphæðin til jöfnunar** svæði fyrir hverja færslu hann fær eftirfarandi skilaboð þegar hann lokar síðan:

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




