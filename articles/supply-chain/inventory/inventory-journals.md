---
title: Birgðabækur
description: Í þessu efnisatriði er fjallað um hvernig hægt er að nota birgðabækur til að bóka ýmsar gerðir af efnislegum birgðafærslum.
author: perlynne
manager: AnnBe
ms.date: 04/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 39d66bb9fd2e121b7ce842d869c2a0a0fa5fa8a5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553439"
---
# <a name="inventory-journals"></a>Birgðabækur

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Í þessu efnisatriði er fjallað um hvernig hægt er að nota birgðabækur til að bóka ýmsar gerðir af efnislegum birgðafærslum.

Birgðabækur í Microsoft Dynamics 365 for Finance and Operations eru notaðar til að bóka efnislegar birgðafærslur af mismunandi gerðum, svo sem bókun úthreyfinga og innhreyfinga, birgðahreyfingar, stofnun uppskriftir (BOMs) og afstemmingu efnislegra birgða. Allar þessar birgðabækur eru notaðar á svipaðan hátt en þeim er skipt niður í mismunandi gerðir.

## <a name="types-of-inventory-journals"></a>Gerðir birgðabóka
Eftirtaldar gerðir birgðabóka eru tiltækar:

-   Hreyfing
-   Leiðrétting birgða
-   Flytja
-   Uppskrift
-   Vörumóttaka
-   Framleiðsluinntak
-   Talning
-   Seðlatalning

### <a name="movement"></a>Hreyfing

Þegar birgðabók hreyfingar er notuð er hægt að bæta kostnaður við vöru þegar birgðum er bætt við, en þú verður að úthluta aukalegum kostnað handvirkt á tiltekinn fjárhagslykil með því að tilgreina mótlykil í fjárhag þegar færslubók er stofnuð. Þessi gerð birgðabókar er gagnleg ef þú vilt skrifa yfir sjálfgefna bókunarlykla.

### <a name="inventory-adjustment"></a>Leiðrétting birgða

Þegar leiðréttingarbók birgða er notuð er hægt að bæta kostnaður við vöru þegar birgðum er bætt við. Aukalegur kostnaður er sjálfvirkt bókaður á tiltekinn fjárhagslykil byggt á uppsetningu bókunarreglu vöruflokks. Nota þessa gerð birgðabókar til að uppfæra hagnaður og tap í birgðamagn þegar varan ætti að halda sínum sjálfgefinn mótlykil fjárhags. Þegar leiðréttingarbók birgða er bókuð er innhreyfing eða úthreyfing birgða bókuð, birgðagildi er breytt og fjárhagsfærslur stofnaðar.

### <a name="transfer"></a>Flytja

Hægt er að Nota flutningabækur til að flytja vörur milli staðsetningar birgðageymslu, runur eða afurðarafbrigði án þess að tengja neinn kostnað. Til dæmis er hægt að flytja vörur úr einu vöruhúsi í annað vöruhús innan sama fyrirtækis. Þegar flutningabók er notuð, verður að tilgreina bæði á "frá" og "til" birgðavíddir (til dæmis, fyrir Svæði og Vöruhúsa). Birgðir á lager fyrir skilgreindar birgðavíddir er breytt til samræmis. Birgðaflutning endurspegla tafarlausa hreyfingu efnis. Birgðir í flutningum eru ekki raktar. Ef rekja verður birgðir í flutningi, ætti frekar að nota flutningspöntun. Þegar flutningsbók er bókuð, eru tvær birgðafærslur stofnaðar fyrir hverja færslubókarlínu:

-   BirgðaÚthreyfing á "frá" staðsetningunni.
-   Þinnhreyfing birgða á "til" staðsetningunni.

### <a name="bom"></a>Uppskrift

Þegar þú skráir að uppskrift sé lokið, er hægt að stofna uppskriftarbók. Með því að nota uppskriftabók, er hægt að bóka Uppskrift beint. Þessi bókun myndar innhreyfingu birgða fyrir vöruna, ásamt tengda Uppskrift og úthreyfingu birgða fyrir afurðirnar sem eru innifalin í Uppskriftinni. Þessi gerð birgðabókar er gagnlegt fyrir einfalda framleiðsluaðstæður eða í miklu magni, þar sem leiðir ekki er krafist.

### <a name="item-arrival"></a>Vörumóttaka

Hægt er að nota vörukomubókina til að skrá innhreyfingar á vörum (til dæmis úr innkaupapantanir). Vörukomubók má stofna sem hluta af móttökustjórnun frá síðnni **Komuyfirlit**, eða þá að hægt er að stofna bókarfærslu af síðunni **Vörukoma**. Ef heiti vörukomubókar er virkjað til að leita að tiltektarstaðsetningum, leitar Finance and Operations að staðsetningu fyrir mótteknar vörur og, ef pláss er, myndar áfangastaði fyrir vörur á innleið.

### <a name="production-input"></a>Framleiðsluinntak

Framleiðsluílagsbækur virka eins og vörukomubókin en eru notaðar fyrir framleiðslupantanir.

### <a name="counting"></a>Talning

Talningarbækur leyfa þér að leiðrétta gildandi birgðir á lager sem eru skráðar fyrir vörur eða vöruflokka og bóka síðan efnislega rauntalningu, þannig að hægt er að gera leiðréttingar sem er krafist til að stemma af mismun. Hægt er að tengja talninarreglur við talningaflokka til að aðstoða við að flokka vörur sem hafa mismunandi einkenni, svo að hægt er að taka með þau atriði í talningarbók. Til dæmis er hægt að setja upp talningarflokk til að telja vörur með tilteknu tíðni, eða til að telja vörur þegar birgðir fara niður í ákveðnu stig. Fyrir upplýsingar um hvernig á að skilgreina talningarflokka, sjá [Skilgreina ferli birgðatalningar](tasks/define-inventory-counting-processes.md).

### <a name="tag-counting"></a>Seðlatalning

Talningabækur merkja eru notaðar til að úthluta númeruðu merki á talningalotu. Merkið ætti að innihalda merkjanúmer, vörunúmer og magn vörunnar. Til að tryggja að merki sé notað aðeins einu sinni, og að öll merki séu notuð, ætti hvert vörunúmer að hafa einkvæmt sett merkja sem hefur sína eigin númeraröð. Hægt er að setja þrjár stöðugildi fyrir hvert merki:

-   **Notað** – Vörunúmer er talið fyrir þetta merki.
-   **Ógilt** – Vörunúmer er ógilt fyrir þetta merki.
-   **Vantar** – Vörunúmer vantar fyrir þetta merki.

Þegar merkjatalningabók er bókuð, er ný talningarbók stofnuð á grundvelli talningarbókarlínum merkja. Frekari upplýsingar um merkjatalningar eru í [birgðamerkjatalning](inventory-tag-counting.md).

## <a name="working-with-journals"></a>Unnið með færslubækur
Færslubók getur aðeins einn notandi fengið aðgang að í einu. Ef nokkrir notendur verður fá aðgang að færslubókum í einu til að stofna færslubókarlínur, verða notendur að velja færslubækur sem eru ekki í notkun til að forðast að skrifað sé yfir upplýsingar. Í aðstæðum þar sem margar deildir nota sömu færslubókargerðina, er gagnlegt að stofna mörg færslubókarheiti (til dæmis, einn fyrir hverja deild). Það getur einnig verið gagnlegt að skipta færslubókum svo að hver bókun sé skráð í sína einkvæmu birgðafærslubók. Fyrir bókunarforskriftir sem tengjast birgðafærslum skal stofna eina færslubók með reglubundnum birgðaleiðréttingum og aðra fyrir birgðatalningu.

## <a name="posting-journal-lines"></a>Bókunarbókarlínur
Hægt er að bóka færslubókarlínur sem eru stofnaðar hvenær sem er þar til þú hefur læst afurð frá aukalegum færslum. Gögnin sem færð er inn í færslubók geymast í færslubókinni, jafnvel þótt þú loka færslubókinni án þess að bóka línur.

## <a name="data-entity-support-for-inventory-journals"></a>Stuðningur gagnaeininga fyrir birgðabækur

Gagnaeiningar styðja eftirfarandi gerðir af samþættingaraðstæðum:
-    Samstillt þjónusta (OData)
-  Ósamstillt samþætting

Nánari upplýsingar er að finna í [Gagnaeiningar](../../dev-itpro/data-entities/data-entities.md).

> [!NOTE]
> Ekki eru allar birgðabækur Odata-virkar og er því ekki hægt að nota Excel-gagnatengið til að fá gögn birt, uppfærð og flutt aftur inn í Dynamics 365 for Finance and Operations. 

Annar munur milli gagnaeininga færslubókar er hæfnin til að nota samsettar einingar sem innihalda bæði haus og línugögn. Eins og er getur þú notað samsettar einingar fyrir:
-   Birgðaleiðréttingabók
-   Birgðahreyfingabók

Þessar tvær birgðabækur styðja aðeins aðstæðurnar *Frumstilla birgðir* sem hluta af innflutningsverkefni gagnastjórnunar:
-  Þegar númer færslubókarhauss er ekki tilgreint, en númeraröð er tilgreind fyrir færslubókargerðina, mun innflutningsvinnan sjálfkrafa búa til færslubókarhausa fyrir hverjar 1000 línur. Til dæmis munu innflutningur á 2020 línur leiða til eftirfarandi þriggja færslubókarhausa:
    -  Haus 1: mun innihalda 1000 línur
    -  Haus 2: mun innihalda 1000 línur
    -  Haus 3: mun innihalda 20 línur
-  Gert er ráð fyrir að einkvæmar línuupplýsingar séu fyrir hendi á hverja birgðavídd, ​​sem getur verið afurð, geymsla og rakningarvídd. Þess vegna er ekki hægt að flytja inn færslubókarlínur þar sem aðeins dagsetningarreiturinn er frábrugðin á línunum innan sama innflutningsverkefnis.

## <a name="additional-resources"></a>Frekari upplýsingar

[Gagnaeiningar](../../dev-itpro/data-entities/data-entities.md)
