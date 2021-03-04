---
title: Notkun Samfelldniáætlana
description: Þetta ferli fer í gegnum að selja samfelldniáætlanir og vinna úr tengdar sölupantanir.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2baf0127a35cc62952fd78daaf8204d35ec8d2b3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413188"
---
# <a name="using-continuity-program"></a>Notkun Samfelldniáætlana

[!include [banner](../includes/banner.md)]

Þetta ferli fer í gegnum að selja samfelldniáætlanir og vinna úr tengdar sölupantanir. Til að ljúka við þetta ferli, þarf notandi að vera settur upp sem notandi símavers. Þessi aðferð notar USRT sýnigögn fyrirtækisins.

1. Fara í Retail og Commerce > viðskiptavinur > viðskiptavinur þjónusta.
2. Í svæðinu SearchText, færðu inn 'Karen' og styðja á Tab-lykil.
    * Svargluggi Ítarleg leit ætti að birtast. Ef það gerist ekki skal smella á Leit hægra megin við þetta svæði.  
3. Í listanum skal merkja valda línu.
    * Aðeins ætti að birtast ein línan með Karen Berg. Velja línuna með því að smella á gátmerki-dálknum lengst til vinstri í hnitanetinu.  
4. Smellið á Velja.
5. Smelltu á Ný sölupöntun
    * Gott er að taka niður númer sölupöntunar. Þarf hana síðar í þessu ferli.  
6. Í svæðinu vörunúmer, færðu inn '88000' og styðja á Tab-lykil.
    * Þetta er Samfelldnivara í sýnigögn USRT.  
7. Smelltu á Ljúka.
8. Færa inn "Visa" í svæðinu greiðslumáti.
9. Smelltu á Bæta við kreditkorti
    * Færðu inn nauðsynlegt upplýsingar um kreditkort á þessari síðu.  
10. Smellið á „Í lagi“.
11. Stækkið hlutann Greiðslur.
    * Til að senda pöntun símavers, þarf að færa inn greiðslur fyrir pöntuninni.  
12. Smellið á „Í lagi“.
13. Smelltu á Senda.
    * Þú ert búinn að stofna nýja samfelldnipöntun. Næst, muntu keyra tvær runuvinnslur sem eru notuð við vinnslu á samfelldnipöntunum.  
14. Lokið síðunni.
15. Fara í Retail og Commerce > Samfelldni > Vinnsla samfelldnigreiðslna.
16. Í svæðinu Samfelldnivara, færðu inn '88000' og styðja á Tab-lykil.
17. Smellt er á Í lagi.
18. Fara í Retail og Commerce > Samfelldni > Stofna samfelldni undirpantanir.
    * Þetta ferli mun stofna nýjar sölupantanir byggt á stillingum samfelldniáætlanir.  
19. Í svæðinu Samfelldnivara, færðu inn '88000' og styðja á Tab-lykil.
    * Vara "88000" er Samfelldnivara í sýnigögn USRT.  
20. Í reitinn sölupöntun skal slá inn eða velja gildi.
    * Færið inn númer sölupöntunar sem var tekið niður fyrr í ferlinu. Þetta mun halda vinnslutíma í lágmarki fyrir þetta ferli. Svæðið sölupöntun er valfrjáls - hægt er að vinna allar pantanir fyrir hverja staka áætlun.  
21. Smellið á „Í lagi“.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]