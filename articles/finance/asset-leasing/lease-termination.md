---
title: Tillaga að riftun leigusamnings
description: Í þessu efnisatriði er útskýrt hvernig á að leggja til riftun leigusamnings.
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ff3795f26ab10ac19cc3a0dd00dca65095118f45
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207304"
---
# <a name="propose-a-lease-for-termination"></a>Leggja til riftun á leigusamningi

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Ef leigusamningi er rift snemma getur eignarleiga skráð riftunarfærslu í færslubók til að afskrifa leiguskuldbindinguna, afnotarétt af eign og uppsafnaðar afskriftir og bóka hagnað og tap. Snemmbúna riftunarferlið riftir leigusamningi og tengum leigubókum. Það riftir ekki einstökum leigubókum. Í þessu efnisatriði er lýst virkni sem gerir þér kleift að leggja til riftun á leigusamningi og vinna úr riftunarfærslu leigusamnings í færslubókinni.

Ef leigusamningur er ekki flokkaður sem frestaðar leigugreiðslur leigusamnings og tengist ekki eign mun eignarleiga búa til eftirfarandi riftunarfærslu í færslubók.

| Færsla                           | Debet (Dr.) | Kredit (Cr.) |
|---------------------------------------|-------------|--------------|
| Leiguskuldbinding debet                   | X           |              |
| Uppsöfnuð afskrift Dr.          | X           |              |
| Hagnaður (tap) á breytingu leigusamnings - debet | X           |              |
| Leigueign - kredit                       |             | X            |
| Hagnaður (tap) á breytingu leigusamnings - kredit |             | X            |

Ef leigubókin er flokkuð sem frestuð leigubók, afskrifar færslan stöðu frestaðar leigu á undan riftuninni á hagnaðar- eða taplykli eins og sýnt er hér.

| Færsla                           | Debet (Dr.) | Kredit (Cr.) | 
|---------------------------------------|-------------|--------------|
| Frestaðar leigugreiðslur - debet                     | X           |              |
| Hagnaður (tap) á breytingu leigusamnings - kredit |             | X            |
| Frestaðar leigugreiðslur - kredit                     |             | X            |
| Hagnaður (tap) á breytingu leigusamnings - debet | X           |              |

Ef leigubókin er tengd við eign er gerð grein fyrir afnotarétti af eign í Eignum. Þetta bókhald inniheldur bókun snemmbærra riftana. Eignarleiga býr til eftirfarandi færslu í færslubók til að afskrifa leiguskuldbindinguna.

| Færsla                           | Debet (Dr.) | Kredit (Cr.) |
|---------------------------------------|-------------|--------------|
| Leiguskuldbinding debet                   | X           |              |
| Hagnaður (tap) á breytingu leigusamnings - kredit |             | X            |

Til að fá upplýsingar um rétta leið til að losa sig við afnotarétt af eign skal skoða [Losa eign sem rýrnun](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md).

## <a name="propose-a-lease-for-termination"></a>Leggja til riftun á leigusamningi

1. Farið í leigusamninginn sem á að rifta og síðan á aðgerðasvæðinu skal velja **Tillaga um riftun**.

    > [!NOTE]
    > Hnappurinn **Tillaga um riftun** er ekki í boði ef einhverjar óbókaðar færslur eru til staðar gagnvart einhverri bók. Áður en hægt er að rifta leigusamningnum þarf að bóka eða eyða þeim færslum í færslubók sem hafa verið búnar til á móti leigusamningnum.

2. Í svarglugganum sem birtist skal stilla reitina **Gildisdagsetning** og **Bókunardagsetning** fyrir riftunarfærslu færslubókarinnar.
3. Velja skal **Tillaga um riftun** til að leggja til riftun á leigusamningi.
4. Velja skal **Bóka riftun leigusamnings** til að bóka sjálfkrafa riftunarfærslu leigusamnings í færslubók.
5. Á síðunni **Riftun leigusamninga** skal velja kenni leigusamnings sem lagt er til að verði rift til að skoða riftunarlínurnar. Riftunarlínunar sýna bókfært virði afnotaréttar af eigninni, leiguskuldbindingu, uppsafnaðra afskrifta, frestaðra leigugreiðslna (ef á við) og tap og hagnað sem þarf að skrá við riftun leigusamningsins.

Leigusamningurinn er nú tilbúinn til riftunar. Gildið í reitnum **Staða riftunar** fyrir leigubókina er breytt í **Tilbúinn til riftunar**. Á þessu stigi er ekki lengur hægt að bóka færslur í færslubók vegna leigusamningsins eða laga eða draga úr honum. 

## <a name="process-leases-that-are-ready-for-termination"></a>Vinna úr leigusamningum sem eru tilbúnir til riftunar

Til að vinna úr leigusamningum sem eru tilbúnir til riftunar og bóka riftunarfærsluna í færslubók skal fylgja þessum skrefum.

1. Á síðunni **Riftun leigusamninga** skal velja leigusamninginn sem á að vinna úr og síðan velja **Rifta**.
2. Í svarglugganum sem birtist skal smella á **Í lagi**.

Kerfið bókar riftunarfærslu í færslubókina. Reiturinn **Staða leigusamnings** fyrir leigubókina er stilltur á **Riftur** og reiturinn **Staða riftunartillögu** er stilltur á **Lokið**.

## <a name="reverse-a-lease-termination"></a>Bakfæra riftun leigusamnings

Til að bakfæra riftunarfærslu leigusamnings í færslubók og opna riftan leigusamning skal fylgja þessu skrefi.

- Á síðunni **Riftun leigusamninga** skal velja riftan leigusamning til að bakfæra og síðan velja **Bakfæra riftun**.

Kerfið bakfærir riftunarfærslu færslubókar. Reiturinn **Staða leigusamnings** fyrir leigubókina er stilltur á **Opinn**. Leigusamningurinn sést ekki lengur á síðunni **Riftun leigusamninga** og hægt er að leggja til riftun á honum á nýjan leik.

## <a name="example-of-a-lease-termination"></a>Dæmi um riftun leigusamnings

Í þessu dæmi tengist leigusamningurinn ósérhæfðri eign og flytur ekki eignarhald eignar eða gefur leigjanda möguleika á að kaupa eignina.

### <a name="setup"></a>Setja upp

Eftirfarandi töflur sýna gildin sem eru stillt á flipunum **Almennt** og **Greiðsluáætlunarlínur** fyrir leigusamninginn sem er notaður í þessu dæmi.

**Almennt**

| Svæði                      | Virði            |
|----------------------------|------------------|
| Gangvirði eignarinnar    | 600,000          |
| Gjaldmiðill                   | USD              |
| Stofnkostnaður       | 1.000            |
| Vextir á nýju lánsfé | 7%               |
| Samsett tímabil       | Árlega         |
| Nýtingartími eignar (mánuðir) | 600              |
| Tegund afborgunar               | Venjulegar afborganir |
| Upphafsdagsetning          | 1/1/2019         |

**Flipi greiðsluáætlunarlína**

| Svæði             | Virði      |
|-------------------|------------|
| Upphafsdagsetning        | 1/1/2019   |
| Tímabil   | Mánaðarlega    |
| Tímabil           | 120        |
| Lokadagsetning          | 31/12/2028 |
| Greiðslutíðni | Árlega   |
| Upphæð greiðslu    | 10,000     |

### <a name="steps-for-terminating-the-lease"></a>Leiðbeiningar um riftun leigusamnings

1. Þegar lokið er við að stofna leigusamninginn eins og lýst er fyrr í þessu efnisatriði er leigubókin opnuð og greiðsluáætlunin staðfest. Bókið síðan upphaflegu skráninguna í færslubókina. Upphaflegur afnotaréttur af eign er $71.235,81 og leiguskuldbinding á að vera $70.235,81. Í þessu dæmi var leigusamningurinn flokkaður sem rekstrarleigusamningur samkvæmt efnisatriði um skráningarkerfi reikningsskilastaðla 842 (ASC 842).
2. Keyrið runubókarferlið þrisvar sinnum til að herma eftir framrás þriggja ára vegna leigugreiðslna, vaxtakostnaðar og afskriftarkostnaðar.
3. Þegar keyrslu allra þriggja runuvinnslanna er lokið skal fara aftur í leigubókina og opna töflur skulda og eignarfærslna til að skoða núverandi bókfært virði afnotaréttar af eign og leiguskuldbindingar. Eftir þrjú ár ætti virði skuldarinnar að vera um -53.893,00 USD og virði eignarinnar að vera u.þ.b. 54.593,00 USD.

    Að þremur árum liðnum samþykkir fyrirtækið og leigusalinn að rifta leigusamningnum. Þess vegna verður nú að rifta leigusamningnum.

4. Farið í leigusamninginn sem á að rifta og síðan á aðgerðasvæðinu skal velja **Tillaga um riftun**. 
5. Í svarglugganum sem birtist skal í reitina **Gildisdagsetning** og **Bókunardagsetning** færa inn **1/1/2021**.
6. Velja skal **Tillaga um riftun** til að leggja til riftun á leigusamningi.

    Síðan **Riftun leigusamninga** birtist og sýnir leigusamninginn sem verður riftur.

7. Til að skoða riftunarlínurnar skal velja kenni leigusamningsins sem lagt var til að yrði rift. Riftunarlínurnar sýna bókfært virði leigusamningsins. Eftirfarandi tafla sýnir hvað þessi gildi ættu að vera fyrir þetta dæmi. 

    | Svæði                                                 | Virði      |
    |-------------------------------------------------------|------------|
    | Bókfærð staða skuldar í færslugjaldmiðli | $53.892,89 |
    | Afnotaréttur af eign í færslugjaldmiðli            | $71.235,81 |
    | Uppsafnaðar afskriftir í færslugjaldmiðli      | $16.642,92 |
    | Hagnaður (tap) í færslugjaldmiðli                   | $-700,00   |

8. Til að bóka riftunarfærslu í færslubók skal velja leigusamninginn á síðunni **Riftun leigusamninga** og síðan velja **Rifta**.
9. Í svarglugganum sem birtist skal smella á **Í lagi**.
10. Til að skoða riftunarfærslu í færslubók sem hefur verið búin til og bókuð skal fara í leigubók eignar í leigubókinni. Eftirfarandi tafla sýnir hvernig þessi færsla ætti að líta út fyrir þetta dæmi.

    | Færsla                           | Debet (Dr.) | Kredit (Cr.) |
    |---------------------------------------|-------------|--------------|
    | Leiguskuldbinding debet                   | 53,892.89   |              |
    | Uppsöfnuð afskrift Dr.          | 16,642.92   |              |
    | Hagnaður (tap) á breytingu leigusamnings - debet | 700.00      |              |
    | Leigueign - kredit                       |             | 71,235.81    |

11. Til að skoða nettóáhrif riftunar þar sem afnotaréttur af eign og leiguskuldbinding verða 0 (núll) skal opna töflur yfir færslur leiguskuldbindingar og eignar.

Nú ætti staða leigusamningsins að vera **Riftur**. Engar frekari færslur í færslubók verða bókaðar gagnvart þessum leigusamningi nema riftunin verði bakfærð.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]