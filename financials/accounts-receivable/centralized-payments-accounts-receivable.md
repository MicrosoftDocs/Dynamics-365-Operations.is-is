---
title: "Miðstýrðar greiðslur fyrir viðskiptakröfur"
description: "Fyrirtæki sem innihalda marga lögaðila geta stofnað og stjórnað greiðslum með því að nota einn lögaðila sem sér um allar greiðslur. Þess vegna þarf ekki að færa inn sömu færslu í marga lögaðila. Þessi skrá gefur dæmi sem sýna hvernig bókanir fyrir miðstýrðar greiðslur eru meðhöndlaðar í mismunandi aðstæðum."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 17a6a25d99bcefe88af3ced72c9e62e1f9393d14
ms.lasthandoff: 03/31/2017


---

# <a name="centralized-payments-for-accounts-receivable"></a>Miðstýrðar greiðslur fyrir viðskiptakröfur

[!include[banner](../includes/banner.md)]


Fyrirtæki sem innihalda marga lögaðila geta stofnað og stjórnað greiðslum með því að nota einn lögaðila sem sér um allar greiðslur. Þess vegna þarf ekki að færa inn sömu færslu í marga lögaðila. Þessi skrá gefur dæmi sem sýna hvernig bókanir fyrir miðstýrðar greiðslur eru meðhöndlaðar í mismunandi aðstæðum.

Fyrirtæki sem innihalda marga lögaðila geta stofnað og stjórnað greiðslum með því að nota lögaðila sem sér um allar greiðslur. Þess vegna þarf ekki að færa inn sömu færslu í marga lögaðila. Þar að auki sparar fyrirtækið tíma, þar sem ferli fyrir greiðslutillögur, jöfnun og breytingu opninna og lokaðra færslna fyrir miðstýrðar greiðslur eru aðlöguð. 

Í miðstýrðum greiðslusamtökum eru margir lögaðila fyrir aðgerðir og hver rekstrareining lögaðila stjórnar upplýsingum eigin reikninga til viðskiptavina. Greiðslur fyrir allar rekstrareiningar lögaðila eru mótteknar úr einum lögaðila, sem kallast lögaðili greiðslunnar. Á meðan á jöfnunarferli stendur eru viðeigandi færslur til og frá eru myndaðar. Hægt er að tilgreina hvaða fyrirtæki innan samtanna muni fá innleystu hagnaðar- eða innleystu tapsfærslurnar og hvernig staðgreiðsluafsláttarfærslur sem eru miðstýrðum greiðslum á milli fyrirtækja eru meðhöndlaðar. 

Eftirfarandi dæmi sýna hvernig bókanir eru meðhöndlaðar í mismunandi tilvikum. Eftirfarandi skilgreining er notuð í öllum þessum dæmum:

-   Lögaðilarnir eru Fabrikam, Fabrikam East og Fabrikam West. Greiðslur viðskiptavinar eru færðar inn í Fabrikam.
-   Í reitnum **Bóka staðgreiðsluafslátt** á síðunni **Bókhald innan samstæðu** er stillt á **Lögaðili reikningsins**.
-   Í reitnum **Bóka hagnað eða tap af gjaldeyrisviðskiptum** á síðunni **Bókhald innan samstæðu** er stillt á **Lögaðili greiðslunnar**.
-   Viðskiptavinur Fourth Coffee er settur upp sem lánadrottinn í öllum lögaðilum. Viðskiptavinir frá ýmsum lögaðilum eru auðkenndir sem sami viðskiptavinur þar sem þeir samnýta sömu altæku aðsetursbókarkenni.

| Kenni aðsetursbókar | Viðskiptavinalykill | Heiti              | Lögaðili  |
|-----------------|------------------|-------------------|---------------|
| 4050            | 4000             | Northwind Traders | Fabrikam      |
| 4050            | 4000             | Northwind Traders | Fabrikam Austur |
| 4050            | 10000            | Northwind Traders | Fabrikam Vestur |

## <a name="example-1-customer-payment-of-invoice-from-another-legal-entity"></a>Dæmi 1: Greiðsla viðskiptavinar á reikningi frá öðrum lögaðila
Fabrikam fær greiðslu að upphæð 600.00 fyrir Fabrikam lykil viðskiptavinar 4000, Northwind Traders. Greiðslan er jöfnuð með opnum reikningi fyrir lykil viðskiptavinar 4000 í Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-customer-4000"></a>Reikningur er bókaður í Fabrikam East fyrir viðskiptavin 4000

| Lykill                             | Debetupphæð | Kreditupphæð |
|-------------------------------------|--------------|---------------|
| Viðskiptavinir (Fabrikam East) | 600,00       |               |
| Sala (Fabrikam East)               |              | 600,00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Greiðsla er móttekin og bókuð í Fabrikam fyrir viðskiptavin 4000

| Lykill                        | Debetupphæð | Kreditupphæð |
|--------------------------------|--------------|---------------|
| Reiðufé (Fabrikam)                | 600,00       |               |
| Viðskiptavinir (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam greiðsla er jöfnuð með Fabrikam East reikningi

**Fabrikam bókun**

| Lykill                         | Debetupphæð | Kreditupphæð |
|---------------------------------|--------------|---------------|
| Viðskiptavinir (Fabrikam)  | 600,00       |               |
| Á gjalddaga til Fabrikam East (Fabrikam) |              | 600,00        |

**Fabrikam East bókun**

| Lykill                             | Debetupphæð | Kreditupphæð |
|-------------------------------------|--------------|---------------|
| Á gjalddaga frá Fabrikam (Fabrikam East)   | 600,00       |               |
| Viðskiptavinir (Fabrikam East) |              | 600,00        |

## <a name="example-2-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>Dæmi 2: Greiðsla viðskiptavinar á reikningi frá öðrum lögaðila með staðgreiðsluafslætti
Fabrikam tekur á móti greiðslu að upphæð 580.00 fyrir Fabrikam viðskiptavin 4000, Northwind Traders. Fabrikam East hefur opinn reikning fyrir viðskiptavin 4000. Reikningurinn hefur 20.00 tiltækan staðgreiðsluafslátt. Greiðslan er jöfnuð með opnum reikningum Fabrikam East. Staðgreiðsluafslátturinn er bókaður á reikningslögaðilann, Fabrikam East.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Reikningur er bókaður á Fabrikam East fyrir Fabrikam East viðskiptavin 4000

| Lykill                             | Debetupphæð | Kreditupphæð |
|-------------------------------------|--------------|---------------|
| Viðskiptavinir (Fabrikam East) | 600,00       |               |
| Sala (Fabrikam East)               |              | 600,00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Greiðsla er móttekin og bókuð í Fabrikam fyrir Fabrikam viðskiptavin 4000

| Lykill                        | Debetupphæð | Kreditupphæð |
|--------------------------------|--------------|---------------|
| Reiðufé (Fabrikam)                | 600,00       |               |
| Viðskiptavinir (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam greiðsla er jöfnuð með Fabrikam East reikningi

**Fabrikam bókun**

| Lykill                         | Debetupphæð | Kreditupphæð |
|---------------------------------|--------------|---------------|
| Viðskiptavinir (Fabrikam)  | 580,00       |               |
| Á gjalddaga til Fabrikam East (Fabrikam) |              | 580,00        |

**Fabrikam East bókun**

| Lykill                             | Debetupphæð | Kreditupphæð |
|-------------------------------------|--------------|---------------|
| Á gjalddaga frá Fabrikam (Fabrikam East)   | 580,00       |               |
| Viðskiptavinir (Fabrikam East) |              | 580,00        |
| Staðgreiðsluafsláttur (Fabrikam East)       | 20,00        |               |
| Viðskiptavinir (Fabrikam East) |              | 20,00         |

## <a name="example-3-customer-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-gain"></a>Dæmi 3: Greiðsla viðskiptavinar á reikningi frá öðrum lögaðila með innleystum gengishagnaði
Fabrikam tekur á móti greiðslu að upphæð 600,00 evrur fyrir Fabrikam viðskiptavin 4000, Northwind Traders. Greiðslan er jöfnuð með opnum reikningi fyrir viðskiptavin 4000 í Fabrikam East. Færsla gengishagnaðar stofnast um leið og jöfnunarferlið á sér stað.

-   Gengi fyrir EUR í USD frá og með reikningsdagsetningunni: 1.2062
-   Gengi fyrir EUR í USD frá greiðsludagsetningu: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Reikningur er bókaður á Fabrikam East fyrir Fabrikam East viðskiptavin 4000

| Lykill                             | Debetupphæð            | Kreditupphæð           |
|-------------------------------------|-------------------------|-------------------------|
| Viðskiptavinir (Fabrikam East) | 600,00 EUR / 723,72 USD |                         |
| Sala (Fabrikam East)               |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Greiðsla er móttekin og bókuð í Fabrikam fyrir Fabrikam viðskiptavin 4000

| Lykill                        | Debetupphæð            | Kreditupphæð           |
|--------------------------------|-------------------------|-------------------------|
| Reiðufé (Fabrikam)                | 600,00 EUR / 736,62 USD |                         |
| Viðskiptavinir (Fabrikam) |                         | 600,00 EUR / 736,62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam greiðsla er jöfnuð með Fabrikam East reikningi

**Fabrikam bókun**

| Lykill                         | Debetupphæð            | Kreditupphæð           |
|---------------------------------|-------------------------|-------------------------|
| Viðskiptavinir (Fabrikam)  | 600,00 EUR / 736,62 USD |                         |
| Á gjalddaga til Fabrikam East (Fabrikam) |                         | 600,00 EUR / 736,62 USD |
| Á gjalddaga til Fabrikam East (Fabrikam) | 0,00 EUR / 12,90 USD    |                         |
| Innleystur gróði (Fabrikam)        |                         | 0,00 EUR / 12,90 USD    |

**Fabrikam East bókun**

| Lykill                             | Debetupphæð            | Kreditupphæð           |
|-------------------------------------|-------------------------|-------------------------|
| Á gjalddaga frá Fabrikam (Fabrikam East)   | 600,00 EUR / 736,62 USD |                         |
| Viðskiptavinir (Fabrikam East) |                         | 600,00 EUR / 736,62 USD |
| Viðskiptavinir (Fabrikam East) | 0,00 EUR / 12,90 USD    |                         |
| Á gjalddaga frá Fabrikam (Fabrikam East)   |                         | 0,00 EUR / 12,90 USD    |

## <a name="example-4-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-gain"></a>Dæmi 4: Greiðsla viðskiptavinar á reikningi frá öðrum lögaðila með staðgreiðsluafslætti og innleystum gengishagnaði
Fabrikam bókar greiðslu fyrir Fabrikam viðskiptavin 4000, Northwind Traders fyrir opinn reikning í Fabrikam East. Reikningurinn hefur tiltækan staðgreiðsluafslátt og VSK-færsla er mynduð. Greiðslan er jöfnuð með opna Fabrikam East-reikningnum. Færsla gengishagnaðar stofnast um leið og jöfnunarferlið á sér stað. Staðgreiðsluafslátturinn er bókaður á reikningslögaðilann (Fabrikam East) og gengishagnaður gjaldmiðilsins er bókaður á greiðslulögaðilann (Fabrikam).

-   Gengi fyrir EUR til USD frá og með reikningsdagsetningunni: 1.2062
-   Gengi fyrir EUR í USD frá greiðsludagsetningu: 1,2277

### <a name="free-text-invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-customer-4000"></a>Textareikningur er bókaður og skattafærsla er stofnuð í Fabrikam East fyrir viðskiptavin 4000

| Lykill                             | Debetupphæð            | Kreditupphæð           |
|-------------------------------------|-------------------------|-------------------------|
| Viðskiptavinir (Fabrikam East) | 638,22 EUR / 769,82 USD |                         |
| Sala (Fabrikam East)               |                         | 600,00 EUR / 723,72 USD |
| Virðisaukaskattur (Fabrikam East)           |                         | 38,22 EUR / 46,10 USD   |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Greiðsla er móttekin og bókuð í Fabrikam fyrir viðskiptavin 4000

| Lykill                        | Debetupphæð            | Kreditupphæð           |
|--------------------------------|-------------------------|-------------------------|
| Reiðufé (Fabrikam)                | 626,22 EUR / 768,81 USD |                         |
| Viðskiptavinir (Fabrikam) |                         | 626,22 EUR / 768,81 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam greiðsla er jöfnuð með Fabrikam East reikningi

**Fabrikam bókun**

| Lykill                         | Debetupphæð            | Kreditupphæð           |
|---------------------------------|-------------------------|-------------------------|
| Viðskiptavinir (Fabrikam)  | 626,22 EUR / 768,81 USD |                         |
| Á gjalddaga til Fabrikam East (Fabrikam) |                         | 626,22 EUR / 768,81 USD |
| Á gjalddaga til Fabrikam East (Fabrikam) | 0,00 EUR / 13,46 USD    |                         |
| Innleystur gróði (Fabrikam)        |                         | 0,00 EUR / 13,46 USD    |

**Fabrikam East bókun**

| Lykill                             | Debetupphæð            | Kreditupphæð           |
|-------------------------------------|-------------------------|-------------------------|
| Á gjalddaga frá Fabrikam (Fabrikam East)   | 626,22 EUR / 768,81 USD |                         |
| Viðskiptavinir (Fabrikam East) |                         | 626,22 EUR / 768,81 USD |
| Viðskiptavinir (Fabrikam East  | 0,00 EUR / 13,46 USD    |                         |
| Á gjalddaga frá Fabrikam (Fabrikam East)   |                         | 0,00 EUR / 13,46 USD    |
| Staðgreiðsluafsláttur (Fabrikam East)       | 12,00 EUR / 14,47 USD   |                         |
| Viðskiptavinir (Fabrikam East) |                         | 12,00 EUR / 14,47 USD   |

## <a name="example-5-customer-credit-note-with-primary-payment"></a>Dæmi 5: Kreditnóta viðskiptavinar með aðalgreiðslu
Fabrikam tekur á móti greiðslu að upphæð 75.00 frá viðskiptavini 4000, Northwind Traders. Greiðslan er jöfnuð með opnum reikningi fyrir Fabrikam West viðskiptavin 10000 og opinni kreditnótu fyrir Fabrikam East viðskiptavin 4000. Greiðslan er valin sem aðalgreiðsla í á **Jafna færslur** síðu.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Reikningur er bókaður á Fabrikam West fyrir viðskiptavin 10000

| Reikningur                             | Debetupphæð | Kreditupphæð |
|-------------------------------------|--------------|---------------|
| Viðskiptavinir (Fabrikam West) | 100,00       |               |
| Sala (Fabrikam West)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Kreditnóta er bókuð á Fabrikam East fyrir viðskiptavin 4000

| Lykill                             | Debetupphæð | Kreditupphæð |
|-------------------------------------|--------------|---------------|
| Söluvöruskil (Fabrikam East)       | 25,00        |               |
| Viðskiptavinir (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Greiðsla er bókuð á Fabrikam fyrir viðskiptavin 4000

| Lykill                        | Debetupphæð | Kreditupphæð |
|--------------------------------|--------------|---------------|
| Reiðufé (Fabrikam)                | 75,00        |               |
| Viðskiptavinir (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam greiðsla er jöfnuð með Fabrikam West reikningi og Fabrikam East kreditnótu

**Fabrikam bókun**

| Lykill                           | Debetupphæð | Kreditupphæð |
|-----------------------------------|--------------|---------------|
| Á gjalddaga frá Fabrikam East (Fabrikam) | 25,00        |               |
| Viðskiptavinir (Fabrikam)    |              | 25,00         |
| Viðskiptavinir (Fabrikam)    | 100,00       |               |
| Á gjalddaga til Fabrikam West (Fabrikam)   |              | 100,00        |

**Fabrikam East bókun**

| Lykill                             | Debetupphæð | Kreditupphæð |
|-------------------------------------|--------------|---------------|
| Viðskiptavinir (Fabrikam East) | 25,00        |               |
| Á gjalddaga frá (Fabrikam East)     |              | 25,00         |

**Fabrikam West bókun**

| Lykill                             | Debetupphæð | Kreditupphæð |
|-------------------------------------|--------------|---------------|
| Á gjalddaga frá Fabrikam (Fabrikam West)   | 100,00       |               |
| Viðskiptavinir (Fabrikam West) |              | 100,00        |

## <a name="example-6-customer-credit-note-without-primary-payment"></a>Dæmi 6: Kreditnóta viðskiptavinar án aðalgreiðslu
Fabrikam tekur á móti greiðslu að upphæð 75.00 frá viðskiptavini 4000, Northwind Traders. Greiðslan er jöfnuð með opnum reikningi fyrir Fabrikam West viðskiptavin 10000 og opinni kreditnótu fyrir Fabrikam East viðskiptavin 4000. Greiðslan er ekki valin sem aðalgreiðsla á síðunni **Jafna færslur**.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Reikningur er bókaður á Fabrikam West fyrir viðskiptavin 10000

| Reikningur                             | Debetupphæð | Kreditupphæð |
|-------------------------------------|--------------|---------------|
| Viðskiptavinir (Fabrikam West) | 100,00       |               |
| Sala (Fabrikam West)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Kreditnóta er bókuð á Fabrikam East fyrir viðskiptavin 4000

| Lykill                             | Debetupphæð | Kreditupphæð |
|-------------------------------------|--------------|---------------|
| Söluvöruskil (Fabrikam East)       | 25,00        |               |
| Viðskiptavinir (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Greiðsla er bókuð á Fabrikam fyrir viðskiptavin 4000

| Lykill                        | Debetupphæð | Kreditupphæð |
|--------------------------------|--------------|---------------|
| Reiðufé (Fabrikam)                | 75,00        |               |
| Viðskiptavinir (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam greiðsla er jöfnuð með Fabrikam West reikningi og Fabrikam East kreditnótu

**Fabrikam bókun**

| Lykill                         | Debetupphæð | Kreditupphæð |
|---------------------------------|--------------|---------------|
| Viðskiptavinir (Fabrikam)  | 75,00        |               |
| Á gjalddaga til Fabrikam West (Fabrikam) |              | 75,00         |

**Fabrikam East bókun**

| Lykill                              | Debetupphæð | Kreditupphæð |
|--------------------------------------|--------------|---------------|
| Viðskiptavinir (Fabrikam East)  | 25,00        |               |
| Á gjalddaga til Fabrikam West (Fabrikam East) |              | 25,00         |

**Fabrikam West bókun**

| Lykill                                | Debetupphæð | Kreditupphæð |
|----------------------------------------|--------------|---------------|
| Á gjalddaga frá Fabrikam (Fabrikam West)      | 75,00        |               |
| Viðskiptavinir (Fabrikam West)    |              | 75,00         |
| Á gjalddaga frá Fabrikam East (Fabrikam West) | 25,00        |               |
| Viðskiptavinir (Fabrikam West)    |              | 25,00         |






