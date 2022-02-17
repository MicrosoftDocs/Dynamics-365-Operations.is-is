---
title: LIFO (síðast inn - fyrst út) með efnislegu virði og marki
description: Síðast inn, fyrst út (LIFO) er birgðalíkan þar sem síðustu (nýjustu) innhreyfingar eru úthreyfðar fyrst. Úthreyfingar úr birgðum eru jafnaðar á móti síðustu innhreyfingu í birgðir, samkvæmt dagsetningu birgðafærslunnar.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55021
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd57d58aa91aa87b1c2feff52a568296fc18ed9b
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092165"
---
# <a name="lifo-with-physical-value-and-marking"></a>LIFO (síðast inn - fyrst út) með efnislegu virði og marki

[!include [banner](../includes/banner.md)]

Síðast inn, fyrst út (LIFO) er birgðastjórnunar- og verðmatsaðferð þar sem birgðir sem voru framleiddar eða keyptar síðast eru seldar, notaðar eða fargað fyrst. Meðan á birgðalokunarferlinu stendur í Microsoft Dynamics 365 Supply Chain Management, kerfið mun búa til uppgjör þar sem síðasta kvittun er jafnað við fyrsta útgáfu o.s.frv. Uppgjörs- og samsvörunarreglan er byggð á fjárhagsdegi birgðafærslunnar. Hægt er að framkvæma bráðabirgðamat á uppgjörum og leiðréttingum með því að keyra endurútreikningsferlið birgða.

Hægt er að hnekkja LIFO meginreglunni með því að merkja birgðafærslur þannig að ákveðin vörumóttaka sé jöfnuð á móti tiltekinni útgáfu. Reglubundin birgðalokun er nauðsynleg þegar þú notar LIFO birgðalíkanið til að búa til uppgjör og aðlaga verðmæti útgáfur í samræmi við LIFO meginregluna. Þar til þú keyrir birgðalokunarferlið eru útgáfufærslur metnar á hlaupandi meðaltali þegar líkamlegar og fjárhagslegar uppfærslur áttu sér stað. Nema þú sért að nota merkingu er hlaupandi meðaltal reiknað út þegar líkamleg eða fjárhagsleg uppfærsla er framkvæmd.

Eftirfarandi dæmi sýna áhrif þess að nota LIFO með þremur mismunandi skilgreiningum:

- LIFO án valkostarins **Taka efnislegt virði með**
- LIFO með valkostinum **Taka efnislegt virði með**
- LIFO með merkingum

## <a name="lifo-without-the-include-physical-value-option"></a>LIFO án þess að efnislegt virði sé tekið með

Í þessu dæmi er **Taktu með líkamlegt gildi** gátreiturinn er hreinsaður í vörulíkanaflokknum fyrir útgefnu vöruna. Eftirfarandi skýringarmynd sýnir þessar færslur:

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 3b. Fjárhagsútgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 23.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna)
- 7\. Birgðalokun er framkvæmd. Byggt á LIFO-aðferðinni verður fyrsta fjárhagslega uppfærða útgáfan jöfnuð á móti síðustu fjárhagslega uppfærðu kvittun og svo framvegis. Í þessu dæmi er ein uppgjör búin til á milli 5b og 3b. Leiðrétting á USD 14.00 verður gerð í 3b og endanlegur kostnaður verður USD 30.00.

Eftirfarandi sýnidæmi sýnir áhrif birgðalíkans FIFO á þessar tegundir færslna þegar **Taka efnislegt virði með** valkosturinn er ekki notaður.

![LIFO án valkostarins Include efnislegt gildi.](./media/lifo-without-including-physical-value.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Líkamleg viðskipti eru táknuð með styttri ljósgráum örvum.
- Fjármálaviðskipti eru táknuð með lengri svörtum örvum.
- Kvittun í birgðum eru táknuð með lóðréttum örvum fyrir ofan ásinn.
- Útgáfur utan birgða eru táknaðar með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svörtu lóðréttri línu. Dagsetningin er tilgreind neðst á skýringarmyndinni.
- Birgðalokanir eru táknaðar með rauðri lóðréttri strikalínu.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="lifo-with-the-include-physical-value-option"></a>LIFO þar sem efnislegt virði er tekið með

Ef **Taktu með líkamlegt gildi** gátreiturinn er valinn fyrir hlut á **Hlutamódelhópar** síðu notar kerfið bæði efnislegar og fjárhagslegar kvittunarfærslur til að reikna út meðaltalskostnaðarverð. Þar sem við á, lagar kerfið einnig líkamlega uppfærða útgáfufærslu. Þegar **Taktu með líkamlegt gildi** gátreiturinn er hreinsaður, birgðalokun sem notar LIFO birgðalíkanið gerir uppgjör eingöngu fyrir færslur sem eru fjárhagslega uppfærðar.

Eftirfarandi skýringarmynd sýnir þessar færslur:

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal líkamlegra og fjárhagslega bókfærðra færslur).
- 3b. Fjárhagsútgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal líkamlegra og fjárhagslega bókfærðra færslna).
- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 23.67 (hlaupandi meðaltal líkamlegra og fjárhagslegra bókaða færslna).
- 7\. Birgðalokun er framkvæmd. Byggt á LIFO-aðferðinni verður fyrsta fjárhagslega uppfærða útgáfan jöfnuð á móti síðustu fjárhagslega uppfærðu kvittun og svo framvegis. Í þessu dæmi er ein uppgjör búin til á milli 3b og 5b. Leiðrétting á USD 14.00 verður gerð í 3b og endanlegur kostnaður verður USD 30.00. Að auki verður færsla 6a aðlöguð að kvittunarfærslukostnaði 4a. Kerfið mun ekki jafna þessar færslur þar sem innhreyfingin uppfærist efnislega en ekki fjárhagslega. Þess í stað verður aðeins leiðrétting á USD 1.33 bókuð á efnislega útgáfufærsluna og leiðréttur kostnaður sem myndast verður USD 25.00.

Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans LIFO á þessar tegundir færslna þegar **Taka efnislegt virði með** valkosturinn er notuð.

![LIFO með valkostinum Innifalið líkamlegt virði.](./media/lifo-with-included-physical-value.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Líkamleg viðskipti eru táknuð með styttri ljósgráum örvum.
- Fjármálaviðskipti eru táknuð með lengri svörtum örvum.
- Kvittun í birgðum eru táknuð með lóðréttum örvum fyrir ofan ásinn.
- Útgáfur utan birgða eru táknaðar með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svörtu lóðréttri línu. Dagsetningin er tekin neðst á skýringarmyndinni.
- Birgðalokanir eru táknaðar með rauðri lóðréttri strikalínu.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="lifo-with-marking"></a>LIFO með merkingu

Merking er aðferð sem gerir mögulegt að tengja eða merkja úthreyfingarfærslu við innhreyfingarfærslu. Merking getur farið fram annað hvort áður eða eftir að færsla er bókuð. Hægt er að nota merkingu þegar þú vilt vera viss um að nákvæmur kostnaður birgðanna þegar færsla er bókuð eða birgðalokun er framkvæmd. til dæmis þjónustudeild samþykkti flýtipöntun frá mikilvægum viðskiptavini. Vegna þess að þessi pöntun er flýtipöntun verður þú að borga meira fyrir hlutinn til að uppfylla beiðni viðskiptavinarins.

Þú verður að ganga úr skugga um að kostnaður við birgðavöru endurspeglast í framlegð, eða kostnaði við seldar vörur (COGS), fyrir sölupöntunarreikninginn. Þegar innkaupapöntunin er bókuð, eru birgðir mótteknar með kostnaðinum 120,00 USD. Ef þetta skjal sölupöntunar er merkt við innkaupspöntunina áður en fylgiseðillinn eða reikningurinn er bókaður, er kostnaður seldra VARA 120,00 USD, en ekki núverandi meðaltal kostnaðar vörunnar. Ef að fylgiseðill sölupöntunarinnar eða reikningur er bókaður áður en merking á sér stað, mun kostnaður seldra vara verða bókaður á meðalkostnaðarverði.

Áður en birgðalokun er framkvæmd er hægt að merkja þessar tvær færslur, hvora fyrir aðra.

Hægt er að merkja úthreyfingarfærslu við innhreyfingu áður en færsla er bókuð. Þú getur gert þessa merkingu úr sölupöntunarlínu á **Upplýsingar um sölupöntun** síðu með því að velja **Birgðir \> Merking** á **Sölupöntunarlínur** Flýtiflipi. Hægt er að skoða opnar innhreyfingarfærslur á síðunni **Merking**.

Einnig er Hægt að merkja úthreyfingarfærslu við innhreyfingu eftir að færslan er bókuð. Hægt er að stemma eða merkja úthreyfingarfærslu fyrir opna innhreyfingarfærslu fyrir skráðan hlut úr bókaðri birgðaleiðréttingabók.

Eftirfarandi skýringarmynd sýnir þessar færslur:

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 3b. Fjárhagsútgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna).
- 3c. Fjárhagsútgáfa birgða fyrir 3b er merkt við birgðafjárútgáfu fyrir 2b.
- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 23.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna)
- 7\. Birgðalokun er framkvæmd. Byggt á merkingarreglunni sem notar LIFO aðferðina eru merktu færslurnar jafnaðar hver á móti öðrum. Í þessu dæmi er 3b jafnað á móti 2b og leiðrétting fyrir USD 6.00 er sett á 3b til að færa gildið í USD 22.00. Í þessu dæmi eru engar viðbótaruppgjörir gerðar, vegna þess að lokunin skapar aðeins uppgjör fyrir fjárhagslega uppfærðar færslur.

Nýja meðalkostnaðarverðið sem er í gangi endurspeglar meðaltal fjárhagslegu og efnislegu uppfærðu færslnanna, 27,50 USD.

Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans LIFO á þessar tegundir færslna þegar merkingar á milli úthreyfinga og innhreyfinga eru notaðar.

![LIFO með merkingu.](./media/lifo-with-marking.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Líkamleg viðskipti eru táknuð með styttri ljósgráum örvum.
- Fjármálaviðskipti eru táknuð með lengri svörtum örvum.
- Kvittun í birgðum eru táknuð með lóðréttum örvum fyrir ofan ásinn.
- Útgáfur utan birgða eru táknaðar með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svörtu lóðréttri línu. Dagsetningin er tilgreind neðst á skýringarmyndinni.
- Birgðalokanir eru táknaðar með rauðri lóðréttri strikalínu.
- Uppgjör og merkingar sem eru framkvæmdar með lokun birgða eru táknaðar með rauðum skástrikuðum örvum sem fara frá kvittun í útgáfu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
