---
title: Um FIFO með merkingu og efnislegt virði
description: Fyrst inn, fyrst út (FIFO) er birgðalíkan þar sem fyrstu innhreyfingar eru úthreyfðar fyrst. Fjárhagslega uppfærð vandamál úr birgðum eru jöfnuð á móti fyrstu fjárhagslega uppfærðu móttöku í birgðir, byggt á fjárhagsdagsetningu birgðafærslu.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5280498a23df26873dda1f380f686796f5e1055f
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092141"
---
# <a name="fifo-with-physical-value-and-marking"></a>Um FIFO með merkingu og efnislegt virði

[!include [banner](../includes/banner.md)]


Fyrst inn, fyrst út (FIFO) er birgðastjórnun og verðmatsaðferð þar sem birgðir sem fyrst eru framleiddar eða keyptar eru seldar, notaðar eða fargað fyrst. Meðan á birgðalokunarferlinu stendur í Microsoft Dynamics 365 Supply Chain Management, Kerfið mun búa til uppgjör þar sem fyrsta kvittun er jafnað við fyrsta útgáfu o.s.frv.

Uppgjörs- og samsvörunarreglan er byggð á fjárhagsdegi birgðafærslunnar. Hægt er að framkvæma bráðabirgðamat á uppgjörum og leiðréttingum með því að keyra endurútreikningsferlið birgða.

Hægt er að hnekkja FIFO meginreglunni með því að merkja birgðafærslur þannig að ákveðin vörumóttaka sé jöfnuð á móti tiltekinni útgáfu. Reglubundin birgðalokun er nauðsynleg þegar þú notar FIFO birgðalíkanið til að búa til uppgjör og aðlaga verðmæti útgáfur í samræmi við FIFO meginregluna. Þar til þú keyrir birgðalokunarferlið eru útgáfufærslur metnar á hlaupandi meðaltali þegar líkamlegar og fjárhagslegar uppfærslur áttu sér stað. Nema þú sért að nota merkingu er hlaupandi meðaltal reiknað út þegar líkamleg eða fjárhagsleg uppfærsla er framkvæmd. Eftirfarandi dæmi sýna áhrifin þess að nota LIFO með þremur mismunandi skilgreiningum:

- LIFO án valkostarins **Taka efnislegt virði með**
- FIFO með valkostinum **Taka efnislegt virði með**
- FIFO með merkingu

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO án valkostarins Taka efnislegt virði með

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
- 7\. Birgðalokun er framkvæmd. Byggt á FIFO-aðferðinni verður fyrsta fjárhagslega uppfærða útgáfan jöfnuð á móti fyrstu fjárhagslega uppfærðu kvittuninni og svo framvegis. Í þessu dæmi er ein uppgjör búin til á milli 1b og 3b. Leiðrétting upp á USD –6.00 verður gerð á 3b og endanlegur kostnaður sem af þessu hlýst verður USD 10.00.

Nýja meðalkostnaðarverðið endurspeglar meðaltal fjárhagslega uppfærðu færslnanna. Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans FIFO á þessar tegundir færslna þegar **Taka efnislegt virði með** valkosturinn er ekki notuð.

![FIFO án valmöguleikans Taka með líkamlegt virði.](./media/fifo-without-include-physical-value.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Líkamleg viðskipti eru táknuð með styttri ljósgráum örvum.
- Fjármálaviðskipti eru táknuð með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svörtu lóðréttri línu. Dagsetningin er tilgreind neðst á skýringarmyndinni.
- Birgðalokanir eru táknaðar með rauðri lóðréttri strikalínu.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO með valkostinum Taka efnislegt virði með

Ef **Taktu með líkamlegt gildi** gátreiturinn er valinn fyrir hlut á **Vörulíkanahópur** síðu notar kerfið bæði efnislegar og fjárhagslegar kvittunarfærslur til að reikna út hlaupandi meðalkostnaðarverð. Þar sem við á, lagar kerfið einnig líkamlega uppfærða útgáfufærslu. Birgðalokun sem notar FIFO birgðalíkanið gerir uppgjör eingöngu fyrir færslur sem eru fjárhagslega uppfærðar. Eftirfarandi skýringarmynd sýnir þessar færslur:

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
- 7\. Birgðalokun er framkvæmd. Byggt á FIFO-aðferðinni verður fyrsta fjárhagslega uppfærða útgáfan jöfnuð á móti fyrstu fjárhagslega uppfærðu kvittuninni og svo framvegis. Í þessu dæmi er ein uppgjör búin til á milli 1b og 3b. Leiðrétting upp á USD –6.00 verður gerð á 3b og endanlegur kostnaður sem af þessu hlýst verður USD 10.00. Að auki verður færsla 6a aðlöguð að kvittunarfærslukostnaði 2b. Kerfið mun ekki jafna þessar færslur þar sem innhreyfingin uppfærist efnislega en ekki fjárhagslega. Þess í stað verður aðeins leiðrétting upp á USD -1,67 bókuð á efnislega útgáfufærsluna og leiðréttur kostnaður sem af því leiðir verður USD 22.00.

![FIFO með valkostinum Innifalið líkamlegt virði.](./media/fifo-with-include-physical-value.png)

Taktu eftir að niðurstaðan af því að keyra birgðalokunarferlið er sú sama, óháð því hvort þú velur **Taktu með líkamlegt gildi** valmöguleika á **Vörulíkanahópur** síðu. The **Taktu með líkamlegt gildi** valkosturinn hefur aðeins áhrif á hlaupandi meðaltal.

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Líkamleg viðskipti eru táknuð með styttri ljósgráum örvum.
- Fjármálaviðskipti eru táknuð með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svörtu lóðréttri línu. Dagsetningin er tilgreind neðst á skýringarmyndinni.
- Birgðalokanir eru táknaðar með rauðri lóðréttri strikalínu.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="fifo-with-marking"></a>FIFO með merkingu

Merking er aðferð sem gerir mögulegt að tengja eða merkja úthreyfingarfærslu við innhreyfingarfærslu. Merking getur farið fram annað hvort áður eða eftir að færsla er bókuð. Hægt er að nota merkingu þegar þú vilt vera viss um að nákvæmur kostnaður birgðanna þegar færsla er bókuð eða birgðalokun er framkvæmd.

til dæmis þjónustudeild samþykkti flýtipöntun frá mikilvægum viðskiptavini. Vegna þess að þessi pöntun er flýtipöntun verður þú að borga meira fyrir þessa vöru til að uppfylla beiðni viðskiptavinarins. Þú verður að ganga úr skugga um að kostnaður við birgðavöru endurspeglast í framlegð, eða kostnaði við seldar vörur (COGS), fyrir sölupöntunarreikninginn. Þegar innkaupapöntunin er bókuð, eru birgðir mótteknar með kostnaðinum 120,00 USD. Ef sölupöntunarskjalið er merkt við innkaupapöntunina áður en fylgiseðillinn eða reikningurinn er bókaður, verður COGS USD 120.00, ekki núverandi meðalkostnaður vörunnar. Ef að fylgiseðill sölupöntunarinnar eða reikningur er bókaður áður en merking á sér stað, mun kostnaður seldra vara verða bókaður á meðalkostnaðarverði. Áður en birgðalokun er framkvæmd er hægt að merkja þessar tvær færslur, hvora fyrir aðra.

Þegar innhreyfingarfærsla er merkt við útgáfufærslu er virðismatsaðferðin sem er skilgreind í vörulíkanaflokknum hunsuð og kerfið jafnar þessar færslur hver við annan. Hægt er að merkja færslu handvirkt á móti sölupöntunarlínu á **Upplýsingar um sölupöntun** síðu með því að velja **Birgðir \> Merking** á **Sölupöntunarlínur** Flýtiflipi. Hægt er að skoða opnar innhreyfingarfærslur á síðunni **Merking**. Hægt er að jafna eða merkja útgáfufærslu við opna innhreyfingarfærslu fyrir birgðavöru úr bókaðri birgðaleiðréttingarbók. Eftirfarandi skýringarmynd sýnir þessar færslur:

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
- 7\. Birgðalokun er framkvæmd. Byggt á merkingarreglunni sem notar FIFO aðferðina eru merktu færslurnar jafnaðar hver á móti öðrum. Í þessu dæmi er 3b jafnað á móti 2b og leiðrétting fyrir USD 6.00 er sett á 3b til að færa gildið í USD 22.00. Í þessu dæmi eru engar viðbótaruppgjörir gerðar, vegna þess að lokunin skapar aðeins uppgjör fyrir fjárhagslega uppfærðar færslur.

Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans FIFO á þessar tegundir færslna þegar merkingar á milli úthreyfinga og innhreyfinga eru notaðar.

![FIFO með merkingu.](./media/fifo-with-marking.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Líkamleg viðskipti eru táknuð með styttri ljósgráum örvum.
- Fjármálaviðskipti eru táknuð með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svörtu lóðréttri línu. Dagsetningin er tilgreind neðst á skýringarmyndinni.
- Birgðalokanir eru táknaðar með rauðri lóðréttri strikalínu.
- Uppgjör og merkingar sem eru framkvæmdar með lokun birgða eru táknaðar með rauðum skástrikuðum örvum sem fara frá kvittun í útgáfu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
