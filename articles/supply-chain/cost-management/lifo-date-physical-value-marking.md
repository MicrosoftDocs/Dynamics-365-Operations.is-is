---
title: LIFO dagsetning með líkamlegu gildi og merkingu
description: Síðast inn, fyrst út dagsetning (LIFO dagsetning) er birgðalíkan sem byggir á LIFO meginreglunni. Úthreyfingar úr birgðum eru jafnaðar á móti síðustu innhreyfingu í birgðir, samkvæmt dagsetningu birgðafærslunnar. Með því að nota LIFO dagsetningu, ef það er engin kvittun fyrir útgáfu, er málið jafnað á móti öllum kvittunum sem eiga sér stað eftir útgáfudegi. Fleiri en eina úthreyfingu innan sama dags má jafna í þeirri röð að sú síðasta jafnist við síðustu innhreyfingu.
author: AndersGirke
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 51592
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6f5f447724ace473bece3007a96c4b56e90a908
ms.sourcegitcommit: addae271ddfc5a8b0721c23337f69916153db4cd
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/21/2022
ms.locfileid: "8330277"
---
# <a name="lifo-date-with-physical-value-and-marking"></a>LIFO dagsetning með líkamlegu gildi og merkingu

[!include [banner](../includes/banner.md)]

Síðast inn, fyrst út dagsetning (LIFO dagsetning) er birgðastjórnun og verðmatsaðferð þar sem birgðir sem voru framleiddar eða keyptar síðast eru seldar, notaðar eða fargað fyrst. Meðan á birgðalokunarferlinu stendur í Microsoft Dynamics 365 Supply Chain Management, Kerfið mun búa til uppgjör þar sem síðasta kvittun er borin saman við fyrstu útgáfu fyrir hverja tiltekna dagsetningu sem byrjar á elstu dagsetningu fyrst, og svo framvegis. Þegar þú notar síðasta inn, fyrst út dagsetningu (LIFO dagsetning) birgðalíkanið, ef engin kvittun er fyrir útgáfu, er útgáfan jafnað á móti öllum innhreyfingum sem eiga sér stað eftir útgáfudagsetningu. Uppgjörs- og samsvörunarreglan er byggð á fjárhagsdegi birgðafærslunnar. Þegar það eru fleiri útgáfur á sama degi eru þau gerð upp í röð síðustu útgáfu, síðustu móttöku. Hægt er að framkvæma bráðabirgðamat á uppgjörum og leiðréttingum með því að keyra endurútreikningsferlið birgða.

Hægt er að hnekkja LIFO dagsetningarreglunni með því að merkja birgðafærslur þannig að tiltekin vörumóttaka sé jöfnuð á móti tiltekinni útgáfu. Reglubundin birgðalokun er nauðsynleg þegar þú notar LIFO dagsetningu birgðalíkansins til að búa til uppgjör og aðlaga verðmæti útgáfur í samræmi við LIFO meginregluna. Þar til þú keyrir birgðalokunarferlið eru útgáfufærslur metnar á hlaupandi meðaltali þegar líkamlegar og fjárhagslegar uppfærslur áttu sér stað. Nema þú sért að nota merkingu er hlaupandi meðaltal reiknað út þegar líkamleg eða fjárhagsleg uppfærsla er framkvæmd.

Við mælum með reglubundinni lokun birgða þegar þú notar LIFO dagsetningu birgðalíkansins.

Eftirfarandi dæmi sýna áhrif þess að nota LIFO dagsetningu í þremur stillingum:

- LIFO dagsetning án **Taktu með líkamlegt gildi** valmöguleika
- LIFO dagsetning með **Taktu með líkamlegt gildi** valmöguleika
- LIFO dagsetning með merkingu

## <a name="lifo-date-without-the-include-physical-value-option"></a>LIFO dagsetning án valmöguleikans Innifalið líkamlegt virði

Í þessu dæmi, er birgðalíkanaflokkurinn ekki merktur til að innihalda efnislega virðið. Eftirfarandi skýringarmynd sýnir þessar færslur:

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
- 7\. Birgðalokun er framkvæmd. Byggt á LIFO dagsetningaraðferðinni verður fyrsta fjárhagslega uppfærða útgáfan jöfnuð á móti síðustu fjárhagslega uppfærðu kvittuninni sem hefst á fyrstu dagsetningu og svo framvegis. Í þessu dæmi er ein uppgjör búin til á milli 3b og 2b. Leiðrétting á USD 6.00 verður gerð í 3b og endanlegur kostnaður verður USD 22.00.

Eftirfarandi mynd sýnir áhrif LIFO dagsetningabirgðalíkans þegar **Taktu með líkamlegt gildi** valmöguleikinn er ekki notaður.

![LIFO dagsetning án valmöguleikans Innifalið líkamlegt virði.](media/lifo-date-without-include-physical-value.png)

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

## <a name="lifo-date-with-the-include-physical-value-option"></a>LIFO dagsetning með valkostinum Innifalið líkamlegt virði

Ef **Taktu með líkamlegt gildi** gátreiturinn er valinn fyrir hlut á **Vörulíkanaflokkar** síðu notar kerfið bæði efnislegar og fjárhagslegar kvittunarfærslur til að reikna út hlaupandi meðalkostnaðarverð. Þar sem við á, lagar kerfið einnig líkamlega uppfærða útgáfufærslu. Þegar **Taktu með líkamlegt gildi** gátreiturinn er hreinsaður, birgðalokun sem notar LIFO dagsetningu birgðalíkansins gerir uppgjör aðeins fyrir færslur sem eru fjárhagslega uppfærðar.

Í þessu dæmi, er birgðalíkanaflokkurinn merktur til að innihalda efnislega virðið. 

Eftirfarandi skýringarmynd sýnir þessar færslur:

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal líkamlegra og fjárhagslegra bókaða færslna).
- 3b. Fjárhagsútgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 16.00 (hlaupandi meðaltal líkamlegra og fjárhagslegra færslna).
- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 23.67 (hlaupandi meðaltal líkamlegra og fjárhagslega bókfærðra færslna).
- 7\. Birgðalokun er framkvæmd. Byggt á LIFO dagsetningaraðferðinni verður fyrsta fjárhagslega uppfærða útgáfan jöfnuð á móti síðustu fjárhagslega uppfærðu kvittuninni fyrir hverja dagsetningu sem hefst á fyrstu dagsetningu og svo framvegis. Í þessu dæmi er ein uppgjör búin til á milli 2b og 3b. Leiðrétting á USD 6.00 verður gerð í 3b og endanlegur kostnaður verður USD 22.00. Að auki verður færsla 6a aðlöguð að kvittunarfærslukostnaði 5b. Kerfið mun ekki jafna þessar færslur vegna þess að kvittunin er uppfærð líkamlega en ekki fjárhagslega. Þess í stað verður aðeins leiðrétting á USD 6.33 bókuð á efnislega útgáfufærsluna og leiðréttur kostnaður sem myndast verður USD 30.00.

Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans Lifo þegar **Taka efnislegt virði með** valkosturinn er notuð.

![LIFO dagsetning með valkostinum Innifalið líkamlegt virði.](media/lifo-date-with-include-physical-value.png)

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

## <a name="lifo-date-with-marking"></a>LIFO dagsetning með merkingu

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
- 3c. Fjárhagsútgáfa birgða fyrir 3b er merkt við birgðafjárútgáfu fyrir 1b.
- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Raunveruleg útgáfa birgða fyrir magnið 1 á kostnaðarverðinu USD 23.00 (hlaupandi meðaltal fjárhagslega bókfærðra færslna)
- 7\. Birgðalokun er framkvæmd. Byggt á merkingarreglunni sem notar LIFO dagsetningaraðferðina eru merktu færslurnar jafnaðar á móti hvor öðrum. Í þessu dæmi er 3b jafnað upp á móti 1b og leiðrétting fyrir USD -6,00 er sett á 3b til að færa gildið í USD 10.00. Í þessu dæmi eru engar viðbótaruppgjörir gerðar, vegna þess að lokunin skapar aðeins uppgjör fyrir fjárhagslega uppfærðar færslur.

Eftirfarandi mynd sýnir áhrif LIFO dagsetningarbirgðalíkans þegar merking á milli útgáfu og kvittana er notuð. 

![LIFO stefnumót með merkingu.](media/lifo-date-with-marking.png)

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
