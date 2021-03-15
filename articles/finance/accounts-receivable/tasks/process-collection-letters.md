---
title: Vinna úr innheimtubréfum
description: Þetta efni sýnir hvernig á að stofna, prenta og bóka innheimtubréf.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: a189bbdd360d07b2b5198fa357380fd9a89ac167
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992965"
---
# <a name="process-collection-letters"></a>Vinna úr innheimtubréfum

[!include [banner](../../includes/banner.md)]

Þetta efni sýnir hvernig á að stofna, prenta og bóka innheimtubréf. Þetta verkefni notar USMF-sýnifyrirtækið.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Setja upp röð innheimtubréfa á bókunarreglu
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Skuldir og innheimta > Uppsetning > Bókunarreglur viðskiptavina**.
2. Smellið á **Breyta**.
3. Veljið innheimtubréfaröð úr í fellilistanum. Ef ekki á að mynda innheimtubréf fyrir færslur með þessari bókunarreglu skal skilja svæðið eftir autt.  
4. Víkkaðu út flipann **Töflutakmarkanir** til að breyta því hvernig innheimtubréf eru unnin. Ef þetta svæði er stillt á **Já**, þá verða stofnuð innheimtubréf fyrir þessa bókunarreglu.  

## <a name="create-collection-letters"></a>Búa til innheimtubréf
1. Farðu í **Skoðunarrúða > Kerfiseiningar > Skuldir og innheimta > Innheimtubréf > Stofna innheimtubréf**.
2. Velja færslugerðir sem innheimta á bréf fyrir. Allar opnar færslur fyrir þessar gerðir verða teknar með í útreikningnum.  
3. Í reitnum **Innheimtubréf** skal velja valkost.
4. Í reitinn **Dagsetning innheimtubréfs** skaltu slá inn dagsetningu innheimtubréfsins.
5. Veljið bókunarreglu ef þú breyttir **Nota bókunarreglu úr** í **Velja**. Í boði eru tveir valmöguleikar fyrir bókunarreglu:   

   - **Reikningur** – Nota bókunarreglu sem er úthlutað til reikning viðskiptavinar fyrir hverja vaxtanótu.   
   - **Velja** – Notið bókunarregluna sem valin var á svæðinu **Bókunarregla**.  

6. Útvíkka **Færslur til að taka með** hlutann.
7. Velja **Síu**.
8. Í svæðinu **Skilyrði** skal færa inn auðkenni viðskiptavinar. Til dæmis, færið inn ‚US-001'.
9. Veljið **Í lagi**.
10. Veljið **Í lagi**.

## <a name="print-collection-letters"></a>Prenta innheimtubréf
1. Farðu í **Skoðunarrúða > Kerfiseiningar > Skuldir og innheimta > Innheimtubréf > Endurskoða og vinna innheimtubréf**.
2. Í reitnum **Staða** skal velja **Stofnað**.
3. Í reitnum **Prentað** skal velja **Ekki prentað**.
4. Velsu **Prenta**.
5. Veldu **Innheimtubréfsnóta**.
6. Í kaflanum **Færibreytur** skaltu slá inn lokadagsetningu fyrir bréf.
7. Stækkaðu kaflann **Færslur til að hafa með** og sláðu inn upplýsingar um innheimtubréfsnótuna.
8. Veldu **Í lagi** til að prenta innheimtubréfið.
9. Bóka innheimtubréfið.

    1. Veldu **Bóka**.
    1. Færð er inn bókunardagsetning fyrir innheimtubréf.
    1. Útvíkka **Færslur til að taka með** hlutann.
    1. Veljið **Í lagi**.
    1. Í reitnum **Staða** skal velja **Bókað**.
    1. Í reitnum **Prentað** skal velja valkost.

## <a name="control-collection-letters-at-the-customer-level"></a>Stjórna innheimtubréfum á stigi viðskiptavinar
Ef innheimtubréf eru sett upp á færslustiginu gætu mörg stafir verið útbúin fyrir viðskiptavin, byggð á aldursgreiningu færslu. Ef færslur birtast í mismunandi stafaröðum verða sérstök innheimtubréf búin til fyrir hvern hóp gjaldfallinna færslna fyrir viðskiptavininn. Þess vegna gæti einstök viðskiptavinur fengið til dæmis eitt innheimtubréf fyrir færslur sem eru 60 daga fram yfir gjalddaga og annað innheimtubréf fyrir færslur sem eru 90 daga yfir gjalddaga. 

Hvert innheimtubréf er einnig tengt innheimtubréfakóða. Innheimtubréfakóðinn er tengdur við stakar færslur og er notaður til að ákvarða hvenær næsta innheimtubréf skal myndað fyrir hverja færslu. Til dæmis, ef færsla er komin yfir 30 daga fram yfir gjalddaga ákvarðar innheimtubréfakóðinn að næsta innheimtubréf verði sent þegar færslan verður 60 daga fram yfir, ef hún hefur ekki verið greitt fyrir þann tíma. 

Einnig er hægt að setja upp innheimtubréf á viðskiptavinastigi. Í þessu tilviki er innheimtubréfakóðinn fyrir hverja færslu rakinn en úrvinnsla innheimtubréfs mun byggjast á einu stigi innheimtubréfs sem er geymt fyrir viðskiptavininn. Eitt stakt innheimtubréf mun innihalda allar færslur sem eru gjaldfallnar fyrir viðskiptavininn. Vegna þess að biðdagar eru nú raktir á stigi viðskiptavinar verður næsta innheimtubréf ekki sent fyrr en fjöldi biðdaga er liðinn fyrir næsta innheimtubréf í röðinni, jafnvel þótt færslur falla á gjalddaga eftir að síðasta innheimtubréf var sent. Þessi valkostur dregur úr fjölda innheimtubréfa sem þú verður að senda á hvern viðskiptavin.

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>Setja upp viðskiptavininn til að stjórna innheimtubréfum á stigi viðskiptavinar
1.  Farðu í **Skoðunarrúða > Kerfiseiningar > Skuldir og innheimta > Uppsetning > Færibreytur viðskiptakrafna** og veldu flipann **Innheimtur**. 
2.  Breyta gildinu á **Stofna innheimtubréf eftir** í **Viðskiptavinur**. 
3.  Farðu í **Skoðunarrúða > Kerfiseiningar > Skuldir og innheimta > Innheimtubréf > Endurskoða og vinna innheimtubréf**. Aðeins eitt innheimtubréf verður búið til fyrir viðskiptavin með öllum gjaldföllnum færslum.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Hunsa greiðslur og kreditreikninga við útreikning á innheimtubréfskóða
Ef þú hefur með greiðslur og kreditreikninga í færslunum sem verða hafðar með í innheimtubréfum, kann að vera að greiðslur eða kreditreikningar setji innheimtubréf af stað. Hægt er að stjórna því hvernig greiðslur og kreditreikningar stýra innheimtubréfakóðanum með því að breyta gildinu á færibreytunni **Hunsa greiðslur og kreditreikninga við útreikning á innheimtubréfskóða**. 

Til að hunsa greiðslur og kreditreikninga við útreikning á innheimtubréfakóðanum skal gera eftirfarandi.

1. Farðu í **Skoðunarrúða > Kerfiseiningar > Skuldir og innheimta > Uppsetning > Færibreytur viðskiptakrafna** og smelltu á flipann **Innheimtur**. 
2. Breyta gildinu á **Hunsa greiðslur og kreditreikninga við útreikning á innheimtubréfskóða** í **Já**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]