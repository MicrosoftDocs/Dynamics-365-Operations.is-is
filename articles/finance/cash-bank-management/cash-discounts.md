---
title: Staðgreiðsluafslættir
description: Staðgreiðsluafslættir eru uppsettir og samnýttir fyrir viðskiptakröfur og Viðskiptaskuldir.  Tiltækur staðgreiðsluafsláttur er hægt að tilgreina á reikning viðskiptavinar eða á reikning lánardrottins og verður tekinn ef reikningurinn er greiddur innan dagsetningu staðgreiðsluafsláttar.
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: roschlom
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d4f6d5bdf4f2fdc4529d9f51515ed2ac4b5b3b5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985313"
---
# <a name="cash-discounts"></a>Staðgreiðsluafslættir

[!include [banner](../includes/banner.md)]

Staðgreiðsluafslættir eru uppsettir og samnýttir fyrir viðskiptakröfur og Viðskiptaskuldir.  Tiltækur staðgreiðsluafsláttur er hægt að tilgreina á reikning viðskiptavinar eða á reikning lánardrottins og verður tekinn ef reikningurinn er greiddur innan dagsetningu staðgreiðsluafsláttar. 

## <a name="cash-discounts"></a>Staðgreiðsluafslættir

Hægt er að stofna staðgreiðsluafslátt fyrir bæði viðskiptavini eða lánardrottna á síðunni staðgreiðsluafslætti. Hægt er að skilgreina einnig , með því að nota Næsta afsláttarkóðasvæði , röð af staðgreiðsluafsláttum sem koma í kjölfar hver annars sem þegar fyrri staðgreiðsluafsláttardagsetningar renna út. Nánari upplýsingar eru í "Dæmi: Röð af staðgreiðsluafslættum" síðar í þessu efnisatriði. Ef reikningur, kreditfærsla (annað hvort í greiðslu eða kreditnótu) eða bæði eru færð inn í öðrum gjaldmiðli en bókhaldsgjaldmiðli lögaðilans er staðgreiðsluafsláttur reiknaður með því að nota gengi byggt á dagsetningu greiðslu eða kreditnótu. Ef reiknings- og kreditskjalið eru færðar inn í mismunandi lögaðila og ef gjaldmiðlar bókhalds fyrir lögaðila er mismunandi, er gengið tekið úr lögaðili reikningsins, frá og með dagsetningu kreditskjals . Nánari upplýsingar eru í "Dæmi: gengi fyrir staðgreiðsluafslættum" síðar í þessu efnisatriði.

## <a name="defaulting-order-of-cash-discount-main-account"></a>Sjálfgefin röðun staðgreiðsluafsláttar fyrir aðallykil

Ef reikningur er jafnaður með fyrirvara svo veittur sé staðgreiðsluafsláttur, þá er afslátturinn bókaður sjálfkrafa í aðallykil staðgreiðsluafsláttar, samkvæmt eftirfarandi sjálfgefinni forgangsröðun :
1.  Aðallykillinn sem tilgreindur er í svæðinu Annar staðgreiðsluafsláttur á síðu Jafna opnar færslur fyrir viðskiptavini eða á síðu Jafna opnar færslur fyrir lánardrottna.
2.  Aðallykillinn sem er tilgreindur á svæðinu staðgreiðsluafsláttur viðskiptavinar eða svæði staðgreiðsluafsláttur lánardrottins fyrir fjárhagsbókunarflokksins sem er úthlutað fyrir VSK-kóða reikningsins. Setja upp fjárhagsbókunarflokka á síðunni fyrir fjárhagsbókunarflokks og úthluta þeim á vsk-kóða á síðunni vsk-kóða.
3.  Aðal bókunarlykillinn á síðu staðgreiðsluafsláttar í annað hvort svæði aðallykils fyrir afslætti viðskiptavinar eða svæðinu aðallykils fyrir afslætti lánardrottins fyrir kóða staðgreiðsluafsláttar sem er á jafnaða reikningnum.
4.  Aðallykill fyrir staðgreiðsluafslátt, eins og skilgreint er í lyklar fyrir sjálfvirkar færslur síðu.

## <a name="example-series-of-cash-discounts"></a>Dæmi: Röð af staðgreiðsluafslætti
Setjið upp þrjá staðgreiðsluafsláttarkóða eins og hér segir:
-   Kóði 5D10% - 10% staðgreiðsluafsláttur þegar upphæðin er greidd innan 5 daga.
-   Kóði 10D5% - 5% staðgreiðsluafsláttur þegar upphæðin er greidd innan 10 daga.
-   Kóði 14D2% - 2% staðgreiðsluafsláttur þegar upphæðin er greidd innan 14 daga.

Í næsta afsláttarkóðasvæði:
-   Fyrir kóðann 5D10% veljið 10D5%.
-   Fyrir kóðann 10D5% veljið 14D2%.
-   Fyrir kóðann 14D2% er reiturinn Næsti afsláttarkóði hafður auður.

Í staðgreiðsluafsláttarnir þrír taka við hver af öðrum þegar dagsetning greiðslu líður fram yfir fyrri dagsetningu staðgreiðsluafsláttar á reikningnum. Einungis einn staðgreiðsluafsláttur er veittur þegar reikningurinn er greiddur, samkvæmt dagsetningu staðgreiðsluafsláttar sem er eftir í röðinni af staðgreiðsluafslætti.

## <a name="example-exchange-rates-for-cash-discounts"></a>Dæmi: gengi fyrir staðgreiðsluafslátt
Bókhaldsgjaldmiðill fyrir við lögaðilann er EUR og eftirfarandi gengi eru tilgreindar fyrir USD:
-   Febrúar 1 = 110
-   Mars 1 = 80

Reikningur fyrir 1000 USD með skilmála staðgreiðsluafsláttar 20D2% er bókaður á 15. febrúar. Gjaldmiðilsupphæð reiknings er 1100 EUR. Greiðsla fyrir 980 USD er jöfnuð með reikningi 1. mars. Upphæð staðgreiðsluafsláttar er 20 USD. Upphæð bókhaldsgjaldmiðils fyrir greiðslu er 784 EUR. Gjaldmiðilsupphæð staðgreiðsluafsláttar er reiknuð með því að nota gengið frá 1. mars: 20 \* 80 / 100 = 16 EUR.

> [!NOTE]
> Ef Reikna staðgreiðsluafslætti fyrir hlutagreiðslur valkostur er valinn í færibreytum viðskiptakrafa eða færibreytur viðskiptaskulda síðunum, er notað gengi sem er í gildi á þeim degi sem hver hlutagreiðsla er notuð. 

