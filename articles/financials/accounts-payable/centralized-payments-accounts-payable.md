---
title: "Miðstýrðar greiðslur fyrir viðskiptaskuldir"
description: "Fyrirtæki sem innihalda marga lögaðila geta stofnað og stjórnað greiðslum með því að nota einn lögaðila sem sér um allar greiðslur. Þess vegna þarf ekki að færa inn sömu greiðslur í marga lögaðila. Þessi skrá gefur dæmi sem sýna hvernig bókanir fyrir miðstýrðar greiðslur eru meðhöndlaðar í mismunandi aðstæðum."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14341
ms.assetid: 7bd02e32-2416-4ac6-8a60-85525267fdb7
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 54329582abd36a8ca896ce731ce06ca4de58bbb0
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="centralized-payments-for-accounts-payable"></a>Miðstýrðar greiðslur fyrir viðskiptaskuldir

[!include[banner](../includes/banner.md)]


Fyrirtæki sem innihalda marga lögaðila geta stofnað og stjórnað greiðslum með því að nota einn lögaðila sem sér um allar greiðslur. Þess vegna þarf ekki að færa inn sömu greiðslur í marga lögaðila. Þessi skrá gefur dæmi sem sýna hvernig bókanir fyrir miðstýrðar greiðslur eru meðhöndlaðar í mismunandi aðstæðum.

Fyrirtæki sem innihalda marga lögaðila geta stofnað og stjórnað greiðslum með því að nota lögaðila sem sér um allar greiðslur. Þess vegna þarf ekki að færa inn sömu greiðslur í marga lögaðila. Þar að auki sparar fyrirtækið tíma þar sem greiðsluferlið er aðlagað.

Í miðstýrðum greiðslusamtökum eru margir lögaðila fyrir aðgerðir og hver rekstrareining lögaðila stjórnar eigin reikningum lánardrottins. Greiðslur fyrir allar rekstrareiningar lögaðila eru myndaðar úr einum lögaðila, sem kallast lögaðili greiðslunnar. Á meðan á jöfnunarferli stendur eru viðeigandi færslur til og frá eru myndaðar. Hægt er að tilgreina hvaða lögeining innan fyrirtækisins fái innleystar hagnaðar- eða innleystar tapfærslurnar og hvernig færslur staðgreiðsluafsláttar sem eru tengdar greiðslum á milli fyrirtækja eru meðhöndlaðar. 

Eftirfarandi dæmi sýna hvernig bókanir eru meðhöndlaðar í mismunandi tilvikum. Eftirfarandi skilgreining er notuð í öllum þessum dæmum:

-   Lögaðilarnir eru Fabrikam, Fabrikam East og Fabrikam West. Greiðslur eru gerðar úr Fabrikam.
-   Í reitnum **Bóka staðgreiðsluafslátt** á síðunni **Bókhald innan samstæðu** er stillt á **Lögaðili reikningsins**.
-   Í reitnum **Bóka hagnað eða tap af gjaldeyrisviðskiptum** á síðunni **Bókhald innan samstæðu** er stillt á **Lögaðili greiðslunnar**.
-   Lánardrottinn Fourth Coffee er settur upp sem lánadrottinn í öllum lögaðilum. Lánardrottnar frá ýmsum lögaðilum eru auðkenndir sem sami lánadrottinn þar sem þeir samnýta sömu altæku aðsetursbókarkenni.

| Skráasafnskenni | Lykill lánardrottins | Heiti          | Lögaðili  |
|--------------|----------------|---------------|---------------|
| 1050         | 3004           | Fourth Coffee | Fabrikam      |
| 1050         | 100            | Fourth Coffee | Fabrikam Austur |
| 1050         | 3004           | Fourth Coffee | Fabrikam Vestur |

## <a name="example-1-vendor-payment-of-invoice-from-another-legal-entity"></a>Dæmi 1: Lánadrottinsgreiðsla á reikning frá öðrum lögaðila
Fabrikam East hefur opinn reikning fyrir lánadrottinslykil 100, Fourth Coffee. Fabrikam færir inn og bókar greiðslu til Fabrikam lánadrottinslykils 3004, Fourth Coffee. Greiðslan er jöfnuð með opna reikningnum.

### <a name="invoice-is-posted-in-fabrikam-east-for-vendor-100"></a>Reikningur er bókaður í Fabrikam East fyrir lánadrottinn 100

| Lykill                          | Debet-upphæð | Kreditupphæð |
|----------------------------------|--------------|---------------|
| Kostnaður (Fabrikam East)          | 600,00       |               |
| Lánadrottnar (Fabrikam East) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Greiðsla er mynduð og bókuð í Fabrikam fyrir lánadrottinn 3004

| Lykill                     | Debet-upphæð | Kreditupphæð |
|-----------------------------|--------------|---------------|
| Lánadrottnar (Fabrikam) | 600,00       |               |
| Reiðufé (Fabrikam)             |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam-greiðsla er jöfnuð með Fabrikam East-reikningi

**Fabrikam-bókun**

| Lykill                           | Debet-upphæð | Kreditupphæð |
|-----------------------------------|--------------|---------------|
| Á gjalddaga frá Fabrikam East (Fabrikam) | 600,00       |               |
| Lánadrottnar (Fabrikam)       |              | 600,00        |

**Fabrikam East-bókun**

| Lykill                          | Debet-upphæð | Kreditupphæð |
|----------------------------------|--------------|---------------|
| Lánadrottnar (Fabrikam East) | 600,00       |               |
| Á gjalddaga frá (Fabrikam East)  |              | 600,00        |

## <a name="example-2-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>Dæmi 2: Lánadrottinsgreiðsla á reikning frá öðrum lögaðila með staðgreiðsluafslætti
Fabrikam East hefur opinn reikning fyrir lánadrottinn 100, Fourth Coffee. Reikningurinn er með tiltækan staðgreiðsluafslátt upp á 20,00. Fabrikam færir inn og bókar greiðslu upp á 580,00 fyrir Fabrikam lánadrottinn 3004, Fourth Coffee. Greiðslan er jöfnuð með opnum reikningum Fabrikam East. Staðgreiðsluafslátturinn er bókaður á reikningslögaðilann, Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Reikningur er bókaður í Fabrikam East fyrir Fabrikam East lánadrottinn 100

| Lykill                          | Debet-upphæð | Kreditupphæð |
|----------------------------------|--------------|---------------|
| Kostnaður (Fabrikam East)          | 600,00       |               |
| Lánadrottnar (Fabrikam East) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Greiðsla er mynduð og bókuð í Fabrikam fyrir Fabrikam lánadrottinn 3004

| Lykill                     | Debet-upphæð | Kreditupphæð |
|-----------------------------|--------------|---------------|
| Lánadrottnar (Fabrikam) | 580,00       |               |
| Reiðufé (Fabrikam)             |              | 580,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam-greiðsla er jöfnuð með Fabrikam East-reikningi

**Fabrikam-bókun**

| Lykill                           | Debet-upphæð | Kreditupphæð |
|-----------------------------------|--------------|---------------|
| Á gjalddaga frá Fabrikam East (Fabrikam) | 580,00       |               |
| Lánadrottnar (Fabrikam)       |              | 580,00        |

**Fabrikam East-bókun**

| Lykill                          | Debet-upphæð | Kreditupphæð |
|----------------------------------|--------------|---------------|
| Lánadrottnar (Fabrikam East) | 580,00       |               |
| Á gjalddaga til Fabrikam (Fabrikam East)  |              | 580,00        |
| Lánadrottnar (Fabrikam East) | 20,00        |               |
| Staðgreiðsluafsláttur (Fabrikam East)    |              | 20,00         |

## <a name="example-3-vendor-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-loss"></a>Dæmi 3: Lánadrottinsgreiðsla á reikningi frá öðrum lögaðila með uppfært gengistap
Fabrikam East hefur opinn reikning fyrir lánadrottinn 100, Fourth Coffee. Fabrikam færir inn og bókar greiðslu fyrir Fabrikam lánadrottinn 3004, Fourth Coffee. Greiðslan er jöfnuð með opna Fabrikam East-reikningnum. Gengistap á gjaldmiðli er myndað á meðan á jöfnunarferlinu stendur.

-   Gengi fyrir EUR til USD frá og með reikningsdagsetningunni: 1.2062
-   Gengi fyrir EUR í USD frá greiðsludagsetningu: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Reikningur er bókaður í Fabrikam East fyrir Fabrikam East lánadrottinn 100

| Lykill                          | Debet-upphæð            | Kreditupphæð           |
|----------------------------------|-------------------------|-------------------------|
| Kostnaður (Fabrikam East)          | 600,00 EUR / 723,72 USD |                         |
| Lánadrottnar (Fabrikam East) |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Greiðsla er mynduð og bókuð í Fabrikam fyrir Fabrikam lánadrottinn 3004

| Lykill                     | Debet-upphæð            | Kreditupphæð           |
|-----------------------------|-------------------------|-------------------------|
| Lánadrottnar (Fabrikam) | 600,00 EUR / 736,62 USD |                         |
| Reiðufé (Fabrikam)             |                         | 600,00 EUR / 736,62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam-greiðsla er jöfnuð með Fabrikam East-reikningi

**Fabrikam-bókun**

| Lykill                           | Debet-upphæð            | Kreditupphæð           |
|-----------------------------------|-------------------------|-------------------------|
| Á gjalddaga frá Fabrikam East (Fabrikam) | 600,00 EUR / 736,62 USD |                         |
| Lánadrottnar (Fabrikam)       |                         | 600,00 EUR / 736,62 USD |
| Rauntap (Fabrikam)          | 0,00 EUR / 12,90 USD    |                         |
| Á gjalddaga frá Fabrikam East (Fabrikam) |                         | 0,00 EUR / 12,90 USD    |

**Fabrikam East-bókun**

| Lykill                          | Debet-upphæð            | Kreditupphæð           |
|----------------------------------|-------------------------|-------------------------|
| Lánadrottnar (Fabrikam East) | 600,00 EUR / 736,62 USD |                         |
| Á gjalddaga til Fabrikam (Fabrikam East)  |                         | 600,00 EUR / 736,62 USD |
| Á gjalddaga til Fabrikam (Fabrikam East)  | 0,00 EUR / 12,90 USD    |                         |
| Lánadrottnar (Fabrikam East) |                         | 0,00 EUR / 12,90 USD    |

## <a name="example-4-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-loss"></a>Dæmi 4: Lánadrottinsgreiðsla á reikningi frá öðrum lögaðila með staðgreiðsluafslátt og uppfært gengistap
Fabrikam East hefur opinn reikning fyrir lánadrottinn 100, Fourth Coffee. Reikningurinn hefur tiltækan staðgreiðsluafslátt og VSK-færsla er mynduð. Fabrikam bókar greiðslu fyrir Fabrikam lánadrottinn 3004, Fourth Coffee. Greiðslan er jöfnuð með opna Fabrikam East-reikningnum. Gengistap á gjaldmiðli er myndað á meðan á jöfnunarferlinu stendur. Staðgreiðsluafslátturinn er bókaður á reikningslögaðilann (Fabrikam East) og gengistap gjaldmiðilsins er bókað á greiðslulögaðilann (Fabrikam).

-   Gengi fyrir EUR til USD frá og með reikningsdagsetningunni: 1.2062
-   Gengi fyrir EUR í USD frá greiðsludagsetningu: 1,2277

### <a name="invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-vendor-100"></a>Reikningurinn er bókaður og skattafærsla er mynduð í Fabrikam East fyrir lánadrottinn 100

| Lykill                          | Debet-upphæð            | Kreditupphæð           |
|----------------------------------|-------------------------|-------------------------|
| Kostnaður (Fabrikam East)          | 564,07 EUR / 680,38 USD |                         |
| Virðisaukaskattur (Fabrikam East)        | 35,93 EUR / 43,34 USD   |                         |
| Lánadrottnar (Fabrikam East) |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Greiðsla er mynduð og bókuð í Fabrikam fyrir lánadrottinn 3004

| Lykill                     | Debet-upphæð            | Kreditupphæð           |
|-----------------------------|-------------------------|-------------------------|
| Lánadrottnar (Fabrikam) | 588,72 EUR / 722,77 USD |                         |
| Reiðufé (Fabrikam East)        |                         | 588,72 EUR / 722,77 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam-greiðsla er jöfnuð með Fabrikam East-reikningi

**Fabrikam-bókun**

| Lykill                           | Debet-upphæð            | Kreditupphæð           |
|-----------------------------------|-------------------------|-------------------------|
| Á gjalddaga frá Fabrikam East (Fabrikam) | 588,72 EUR / 722,77 USD |                         |
| Lánadrottnar (Fabrikam)       |                         | 588,72 EUR / 722,77 USD |
| Rauntap (Fabrikam)          | 0,00 EUR / 12,66 USD    |                         |
| Á gjalddaga frá Fabrikam East (Fabrikam) |                         | 0,00 EUR / 12,66 USD    |

**Fabrikam East-bókun**

| Lykill                          | Debet-upphæð            | Kreditupphæð           |
|----------------------------------|-------------------------|-------------------------|
| Lánadrottnar (Fabrikam East) | 588,72 EUR / 722,77 USD |                         |
| Á gjalddaga til Fabrikam (Fabrikam East)  |                         | 588,72 EUR / 722,77 USD |
| Á gjalddaga til Fabrikam (Fabrikam East)   | 0,00 EUR / 12,66 USD    |                         |
| Lánadrottnar (Fabrikam East) |                         | 0,00 EUR / 12,66 USD    |
| Lánadrottnar (Fabrikam East) | 11,28 EUR / 13,61 USD   |                         |
| Staðgreiðsluafsláttur (Fabrikam East)    |                         | 11,28 EUR / 13,61 USD   |

## <a name="example-5-vendor-credit-note-with-primary-payment"></a>Dæmi 5: Kreditnóta lánadrottins með aðalgreiðslu
Fabrikam myndar greiðslu upp á 75,00 fyrir Fabrikam lánadrottinn 3004, Fourth Coffee. Greiðslan er jöfnuð með opnuð reikningi fyrir Fabrikam West lánadrottinn 3004 og opinni kreditnótu fyrir Fabrikam East lánadrottinn 100. Greiðslan er valin sem aðalgreiðsla í á **Jafna færslur** síðu.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Reikningur er bókaður til Fabrikam West fyrir lánadrottinn 3004

| Reikningur                          | Debet-upphæð | Kreditupphæð |
|----------------------------------|--------------|---------------|
| Kostnaður (Fabrikam West)          | 100,00       |               |
| Lánadrottnar (Fabrikam West) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Kreditnóta er bókuð til Fabrikam East fyrir lánadrottinn 100

| Lykill                          | Debet-upphæð | Kreditupphæð |
|----------------------------------|--------------|---------------|
| Lánadrottnar (Fabrikam East) | 25,00        |               |
| Innkaupaskil (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Greiðslan er bókuð til Fabrikam fyrir lánadrottinn 3004

| Lykill                     | Debet-upphæð | Kreditupphæð |
|-----------------------------|--------------|---------------|
| Lánadrottnar (Fabrikam) | 75,00        |               |
| Reiðufé (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam-greiðsla er bókuð með Fabrikam West-reikningi og Fabrikam East-kreditnótu

**Fabrikam-bókun**

| Lykill                           | Debet-upphæð | Kreditupphæð |
|-----------------------------------|--------------|---------------|
| Lánadrottnar (Fabrikam)       | 25,00        |               |
| Á gjalddaga til Fabrikam East (Fabrikam)   |              | 25,00         |
| Á gjalddaga frá Fabrikam West (Fabrikam) | 100,00       |               |
| Lánadrottnar (Fabrikam)       |              | 100,00        |

**Fabrikam East-bókun**

| Lykill                           | Debet-upphæð | Kreditupphæð |
|-----------------------------------|--------------|---------------|
| Á gjalddaga frá Fabrikam (Fabrikam East) | 25,00        |               |
| Lánadrottnar (Fabrikam East)  |              | 25,00         |

**Fabrikam West-bókun**

| Lykill                          | Debet-upphæð | Kreditupphæð |
|----------------------------------|--------------|---------------|
| Lánadrottnar (Fabrikam West) | 100,00       |               |
| Á gjalddaga til Fabrikam (Fabrikam West)  |              | 100,00        |

## <a name="example-6-vendor-credit-note-without-primary-payment"></a>Dæmi 6: Kreditnóta lánadrottins án aðalgreiðslu
Fabrikam myndar greiðslu upp á 75,00 fyrir Fabrikam lánadrottinn 3004, Fourth Coffee. Greiðslan er jöfnuð með opnuð reikningi fyrir Fabrikam West lánadrottinn 3004 og opinni kreditnótu fyrir Fabrikam East lánadrottinn 100. Greiðslan er ekki valin sem aðalgreiðsla á síðunni **Jafna færslur**.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Reikningur er bókaður til Fabrikam West fyrir lánadrottinn 3004

| Reikningur                          | Debet-upphæð | Kreditupphæð |
|----------------------------------|--------------|---------------|
| Kostnaður (Fabrikam West)          | 100,00       |               |
| Lánadrottnar (Fabrikam West) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Kreditnóta er bókuð til Fabrikam East fyrir lánadrottinn 100

| Lykill                          | Debet-upphæð | Kreditupphæð |
|----------------------------------|--------------|---------------|
| Lánadrottnar (Fabrikam East) | 25,00        |               |
| Innkaupaskil (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Greiðslan er bókuð til Fabrikam fyrir lánadrottinn 3004

| Lykill                     | Debet-upphæð | Kreditupphæð |
|-----------------------------|--------------|---------------|
| Lánadrottnar (Fabrikam) | 75,00        |               |
| Reiðufé (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam-greiðsla er bókuð með Fabrikam West-reikningi og Fabrikam East-kreditnótu

**Fabrikam-bókun**

| Lykill                           | Debet-upphæð | Kreditupphæð |
|-----------------------------------|--------------|---------------|
| Á gjalddaga frá Fabrikam West (Fabrikam) | 75,00        |               |
| Lánadrottnar (Fabrikam)       |              | 75,00         |

**Fabrikam East-bókun**

| Lykill                                | Debet-upphæð | Kreditupphæð |
|----------------------------------------|--------------|---------------|
| Á gjalddaga frá Fabrikam West (Fabrikam) | 25,00        |               |
| Lánadrottnar (Fabrikam East)       |              | 25,00         |

**Fabrikam West-bókun**

| Lykill                              | Debet-upphæð | Kreditupphæð |
|--------------------------------------|--------------|---------------|
| Lánadrottnar (Fabrikam West)     | 75,00        |               |
| Á gjalddaga til Fabrikam (Fabrikam West)      |              | 75,00         |
| Lánadrottnar (Fabrikam West)     | 25,00        |               |
| Á gjalddaga til Fabrikam East (Fabrikam West) |              | 25,00         |






