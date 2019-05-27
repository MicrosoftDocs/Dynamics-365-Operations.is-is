---
title: Skráning raðnúmera í söluferli
description: Þetta efnisatriði útskýrir hvernig hægt er að skrá raðnúmer á fylgiseðla eða reikninga meðan á söluferli stendur. Þessi möguleiki er henturgur ef fyrirtæki vill sækja raðnúmer vegna þjónustu og ábyrgðar en þurfa ekki að vinna með raðnúmer í birgðum frá innhreyfingu til úthreyfingar.
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResTrackingDimensionGroup, InventTrackingRegisterTrans, SalesEditLines, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 28931
ms.assetid: 5d39630f-607e-492b-8c1e-790ca53effa0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e86c2f8d1d5920198db74dc3b64f2393c5e13ff7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555039"
---
# <a name="register-serial-numbers-in-the-sales-process"></a>Skráning raðnúmera í söluferli

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Þetta efnisatriði útskýrir hvernig hægt er að skrá raðnúmer á fylgiseðla eða reikninga meðan á söluferli stendur. Þessi möguleiki er henturgur ef fyrirtæki vill sækja raðnúmer vegna þjónustu og ábyrgðar en þurfa ekki að vinna með raðnúmer í birgðum frá innhreyfingu til úthreyfingar.

Mörg fyrirtæki vilja bara sækja raðnúmer vegna þjónustu og ábyrgðar og þurfa ekki að vinna með raðnúmer í birgðum frá innhreyfingu til úthreyfingar. Í þessum aðstæðum leyfir Microsoft Dynamics 365 for Finance and Operations að skrá raðnúmer á fylgiseðla eða reikninga þegar vörur eru seldar. Ef afurðum er skilað seinna er unnt að rekja hverja afurð til reiknings til að ákvarða hvort þú seldir afurðina og hvort þjónustu eða ábyrgð eru gildar.

Virkja þarf raðnúmer fyrir söluferlið með því að velja valkostinn **Í söluferli** á síðunni **Rakningarvíddarflokkar**. Eftirfarandi tilvik eiga sér svo stað í Microsoft Dynamics 365 for Finance and Operations:
-   Á flýtiflipanum **Raðnúmer** er valkosturinn **Raðnúmerastýring** valinn. Ef þessi gátreitur er valinn þarf að skrá eitt raðnúmer fyrir hverja vöru á fylgiseðli eða reikningi.
-   Allt val á rakningarvíddaflokk fyrir raðnúmer er hreinsað, nema gátreiturinn **Auð úthreyfing leyfð**. Hægt er að velja valkostinn **Auð úthreyfing leyfð** til að hnekkja raðnúmerastjórn og leyfa afurðum að vera pakkaðar og reikningsfærðar án þess að skrá raðnúmer.

## <a name="when-do-i-register-serial-numbers-during-the-sales-process"></a>Hvenær skrái ég raðnúmer í söluferlinu?
Hægt er að skrá raðnúmer annaðhvort á fylgiseðli sölupöntunar eða á reikningi. Þegar undirbúinn er reikningur fyrir raðaða vöru sem hefur verið send með fylgiseðli, er hægt að velja hvaða raðnúmer á fylgiseðlinum á að reikningsfæra. Fjöldi skráðra raðnúmera má ekki fara yfir magn vara sem eru sendar. Ef verið er að stofna hluta reiknings er hægt að velja færri raðnúmeraðar vörur en voru skráðar á fylgiseðlinum. Þegar fylgiseðill eða reikningur er bókaður, eru teknar með raðnúmerin sem voru skráð.

## <a name="can-i-enter-serial-numbers-by-scanning-them-or-do-i-have-to-type-them"></a>Get ég fært inn raðnúmer með því að skanna þau eða verð ég að færa þau inn?
Hægt er að skanna eða slá inn raðnúmer. Þegar skanni er notaður ákvarðar stilling skönnunar hvort raðnúmerum er bætt við eða fjarlægð af listanum yfir raðnúmer á reikningum eða fylgiseðlum. Ef óskað er að skanna raðnúmer, til dæmis með því að nota handbæran strikamerkjaskanna, skal stilla skanna til að senda Færa inn eða TAB-skipun á eftir raðnúmerinu. Þessi skipun mun tilgreina lok gagnaflæðis. Annars þarf að ýta á Enter eða TAB á lyklaborði eftir hvert skannað raðnúmer.

## <a name="if-i-enable-serial-numbers-for-the-sales-process-do-i-have-to-register-all-serial-numbers-for-all-items"></a>Ef ég virkja raðnúmer fyrir söluferlið, þarf ég að skrá öll raðnúmer fyrir allar vörur?
Uppsetning rakningarvíddarflokks sem er úthlutað á afurð ákvarðar hvort skrá verður raðnúmer fyrir allar vörur á fylgiseðli eða reikningi. Þegar raðnúmer fyrir söluferlið eru gerð virk, er gátreiturinn **Raðnúmerarstýring** sjálfvirkt valinn. Síðan þarf að skrá eitt raðnúmer eða skrá auða skráningu fyrir ólæsilegt númer fyrir hverja vöru á fylgiseðli eða reikningi. Ef ekki á að krefjast raðnúmer fyrir hverja vöru, veljið þá **Auð úthreyfing leyfð** á rakningarvíddaflokknum víddar sem er tengdur við vöruna. Þú getur þá skráð færri raðnúmer en magn af vörum sem eru sendar. Ef þú skráir fleiri raðnúmer en eru atriði sem á að senda, muntu ekki getað bókað fylgiseðil eða reikning.

## <a name="can-i-register-serial-numbers-for-partial-invoices-and-partial-shipments"></a>Get ég skrá raðnúmer fyrir hluta reikninga og hlutasendingar?
Hægt er að stofna hluta reikninga og fylgiseðla fyrir sölupantanir og skrá aðeins raðnúmer fyrir vörurnar sem þessir reikningar og fylgiseðlar innihalda. Ef óskað er að stofna reikning að hluta og þú ert með fleiri en einn fylgiseðil fyrir sölupöntun er hægt að hafa með raðnúmer úr fleiri en einum fylgiseðli. Hins vegar það má aðeins vera einn fylgiseðill sem inniheldur ekki öll raðnúmer. Til dæmis, ef þú hefur þrjá fylgiseðla og hver fylgiseðill inniheldur tvær raðnúmeraðar vörur, er hægt að stofna hluta reiknings fyrir eina vöru úr hverjum fylgiseðli.

## <a name="what-do-i-do-when-a-serial-number-isnt-readable"></a>Hvað geri ég þegar raðnúmer er ólæsilegt?
Ef ekki er hægt að lesa eða skanna raðnúmer, er hægt að stofna auða línu fyrir vöru með því að smella á **Ekki læsilegt** á síðunni **Raðnúmer**. Ef raðnúmer verður tiltækt seinna er hægt að uppfæra reikninginn eða fylgiseðillinn. Nánari upplýsingar má nálgast í næsta hlutanum „Get ég leiðrétt eða breytt raðnúmerum sem ég hef skráð fyrir sölupöntun?“

## <a name="can-i-correct-or-change-the-serial-numbers-that-i-have-registered-for-a-sales-order"></a>Get ég leiðrétt eða breytt raðnúmerum sem ég hef skráð fyrir sölupöntun?
Já, hægt er að leiðrétta raðnúmer þegar eftirfarandi skilyrði eru uppfyllt:
-   **Reikningar**  - Hægt er að breyta raðnúmeri fyrir vörur sem þú hefur ekki enn komið í innheimtu. Síðan er fylgiseðillinn líka uppfærður. Hins vegar, ef sölupöntunarlína var leiðrétt eftir að neikvætt magn er skráð er hægt að breyta raðnúmerum fyrir sölupöntunarlínuna.
-   **Fylgiseðlar**  - Ekki er hægt að leiðrétta fylgiseðillínu að hluta, sem inniheldur vörur með raðnúmerum. Bakfæra þarf fullt magn fyrir línuna. Ef fylgiseðill hefur verið afturkallaður eða leiðréttur þarf ekki að skrá bakfærð raðnúmer aftur við stofnun nýs fylgiseðils fyrir sömu raðnúmeruðu vörurnar. Númer sem voru skráðar verður notuð.

## <a name="can-i-view-the-serial-numbers-that-were-shipped-together-with-a-specific-packing-slip-or-that-were-included-on-an-invoice"></a>Get ég skoðað raðnúmer sem voru send með tilgreindum fylgiseðli eða voru tekin með í reikningi?
Já, hægt er að keyra fyrirspurn á færslubókarlínu fylgiseðils eða reikningabókarlínu til að skoða lista yfir öll raðnúmer sem voru höfð með í skjalinu.

## <a name="can-i-view-the-serialized-items-that-i-have-on-hand"></a>Get ég skoðað raðrituð vörur sem ég á lager?
Nei, þú getur ekki skoðað raðnúmerað vörur sem þú hefur á lager þar sem raðnúmer eru ekki skráð fyrir vörur fyrr en þær eru seldar.

## <a name="can-i-register-serial-numbers-for-catchweight-items"></a>Get ég skrá raðnúmer fyrir atriði fyrir þyngd afurðar?
Nei, í söluferli getur þú ekki skráð raðnúmer fyrir atriði fyrir þyngd afurðar. Þar að auki, ef afurð er sett upp eins og atriði fyrir þyngd afurðar, er ekki hægt úthluta afuðinni til rakningarvíddarhópsins sem er settur upp fyrir notkun á raðnúmerum eingöngu á meðan söluferli stendur.

## <a name="can-i-register-serial-numbers-at-the-retail-pos"></a>Get ég skráð raðnúmer í Smásala POS?

Já, Smásala (POS) mun biðja notanda að færa inn raðnúmer þegar notandinn selur vöru sem er úthlutað til rakningarvíddarhópsins sem er settur upp fyrir notkun á raðnúmerum eingöngu á meðan söluferli stendur.

## <a name="what-security-roles-are-required-in-order-to-register-serial-numbers-during-the-sales-process"></a>Hvaða öryggishlutverka er krafist til að skrá raðnúmer í söluferli?
Þessi aðgerð er tiltæk fyrir öll hlutverk sem hægt er að viðhalda fylgiseðla og reikninga. Eftirfarandi skyldum leyfa starfsmönnum að leiðrétta raðnúmer og skrá auðar færslur fyrir raðnúmer sem ekki er hægt að lesa eða skanna:
-   Viðhalda raðnúmerleiðréttingum
-   Viðhalda skráningu á ólæsilegum raðnúmerum





