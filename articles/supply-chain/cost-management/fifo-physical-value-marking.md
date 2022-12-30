---
title: Um FIFO með merkingu og efnislegt virði
description: Fyrst inn, fyrst út (FIFO) er birgðalíkan þar sem fyrstu innhreyfingar eru úthreyfðar fyrst. Fjárhagslega uppfærð vandamál úr birgðum eru jöfnuð á móti fyrstu fjárhagslega uppfærðu móttöku í birgðir, byggt á fjárhagsdagsetningu birgðafærslu.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 663dce9f871e96fec7017616732428c49b1224a0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676244"
---
# <a name="fifo-with-physical-value-and-marking"></a>Um FIFO með merkingu og efnislegt virði

[!include [banner](../includes/banner.md)]


Fyrst inn, fyrst út (FIFO) er birgðastjórnunar- og matsaðferð þar sem birgðir sem eru framleiddar eða keyptar fyrst eru seldar, notaðar eða fargað fyrst. Á meðan birgðahaldi stendur í Microsoft Dynamics 365 Supply Chain Management mun kerfið búa til uppgjör þar sem fyrsta kvittunin er borin saman við fyrstu útgáfu og svo framvegis.

Jafnanir og jöfnunarregla byggja á fjárhagsdagsetningu birgðafærslna. Hægt er að framkvæma bráðabirgðamat á uppgjörum og leiðréttingum með því að keyra endurreikningsferli birgða.

Hægt er að hnekkja LIFO reglunni með því að merkja birgðafærslur svo að tiltekin innhreyfing vöru sé jöfnuð gagnvart tiltekinni úthreyfingu. Reglubundin birgðalokun er nauðsynleg þegar notað er FIFO-birgðalíkan vegins meðaltals til að búa til uppgjör og breyta gildi úthreyfinga í samræmi við FIFO-reglu. Þar til þú keyrir birgðalokunarferli, eru úthreyfingarfærslur metnar á hlaupandi meðaltali þegar efnislegar og fjárhagslegar uppfærslur áttu sér stað. Nema ef merking er notuð þá er hlaupandi meðaltal reiknað út þegar efnisleg eða fjárhagsleg uppfærsla er framkvæmd. Eftirfarandi dæmi sýna áhrifin þess að nota LIFO með þremur mismunandi skilgreiningum:

- LIFO án valkostarins **Taka efnislegt virði með**
- FIFO með valkostinum **Taka efnislegt virði með**
- FIFO með merkingu

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO án valkostarins Taka efnislegt virði með

Í þessu dæmi er gátreiturinn **Taka efnislegt virði með** hreinsaður á síðu fyrir vörulíkanaflokk fyrir vöruna sem er losuð. Eftirfarandi skýringarmynd sýnir þessar færslur:

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 16,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 3b. Fjárhagsleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 16,00 USD á hverja (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 23,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 7\. Birgðalokun er framkvæmd. Á grundvelli FIFO aðferðarinnar, verður fyrsta fjárhagslega uppfærða úthreyfingin jöfnuð gagnvart fyrstu fjárhagslega uppfærðu innhreyfingunni og svo framvegis. Í þessu dæmi er búið til eitt uppgjör milli 1b og 3b. Leiðrétting upp á USD -6,00 verður gerð á 3b og endanlegur kostnaður verður 10,00 USD.

Nýja meðalkostnaðarverðið endurspeglar meðaltal fjárhagslega uppfærðu færslnanna. Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans FIFO á þessar tegundir færslna þegar **Taka efnislegt virði með** valkosturinn er ekki notuð.

![FIFO án valkostarins Taka efnislegt virði með.](./media/fifo-without-include-physical-value.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Efnislegar færslur eru táknaðar með styttri ljósgráum örvum.
- Fjárhagsfærslur eru táknaðar með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svartri lóðréttri línu. Dagsetningin er tekin fram neðst á skýringarmyndinni.
- Birgðalokanir eru sýndar með rauðri lóðréttri strikalínu.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO með valkostinum Taka efnislegt virði með

Ef reiturinn **Taka efnislegt virði með** er valinn fyrir vöru í skjámyndinni **Vörulíkanaflokkar**, mun kerfið nota bæði efnislegar og fjárhagslegar innhreyfingarfærslur til að reikna út meðalkostnaðarverðið. Það sem það á við mun kerfið einnig leiðrétta efnislega uppfærða úthreyfingarfærslu. Birgðalokun sem notar FIFO-birgðalíkanið jafnar aðeins færslur sem eru fjárhagslega uppfærðar. Eftirfarandi skýringarmynd sýnir þessar færslur:

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 16,00 USD (hlaupandi meðaltal fjárhagslega og efnislegra bókaðra færslna).
- 3b. Fjárhagsleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 16,00 USD á hverja (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 23,67 USD (hlaupandi meðaltal fjárhagslega og efnislegra bókaðra færslna).
- 7\. Birgðalokun er framkvæmd. Á grundvelli FIFO aðferðarinnar, verður fyrsta fjárhagslega uppfærða úthreyfingin jöfnuð gagnvart fyrstu fjárhagslega uppfærðu innhreyfingunni og svo framvegis. Í þessu dæmi er búið til eitt uppgjör milli 1b og 3b. Leiðrétting upp á USD -6,00 verður gerð á 3b og endanlegur kostnaður verður 10,00 USD. Auk þess verður færsla 6a leiðrétt í kostnað innhreyfingarfærslu 2b. Kerfið mun ekki jafna þessar færslur þar sem innhreyfingin uppfærist efnislega en ekki fjárhagslega. Í stað þess verður aðeins leiðrétting upp á -1,67 USD bókuð á efnislegu úthreyfingarfærsluna og leiðréttur kostnaður verður því 22,00 USD.

![FIFO með valkostinum Taka efnislegt virði með.](./media/fifo-with-include-physical-value.png)

Taktu eftir því að niðurstaðan af því að keyra birgðalokunarferlið verður sú sama burtséð frá því hvort þú valdir vakostinn **Taka efnislegt virði með** á síðunni **Vörulíkanaflokkur**. Valkosturinn **Taka efnislegt virði með** hefur aðeins áhrif á hlaupandi meðaltal.

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Efnislegar færslur eru táknaðar með styttri ljósgráum örvum.
- Fjárhagsfærslur eru táknaðar með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svartri lóðréttri línu. Dagsetningin er tekin fram neðst á skýringarmyndinni.
- Birgðalokanir eru sýndar með rauðri lóðréttri strikalínu.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="fifo-with-marking"></a>FIFO með merkingu

Merking er aðferð sem gerir mögulegt að tengja eða merkja úthreyfingarfærslu við innhreyfingarfærslu. Merking getur farið fram annað hvort áður eða eftir að færsla er bókuð. Hægt er að nota merkingu þegar þú vilt vera viss um að nákvæmur kostnaður birgðanna þegar færsla er bókuð eða birgðalokun er framkvæmd.

til dæmis þjónustudeild samþykkti flýtipöntun frá mikilvægum viðskiptavini. Þar sem þessi pöntun er flýtipöntun verðu að greiða meira fyrir vöruna til þess að geta uppfyllt beiðni viðskiptavinarins. Þá er nauðsynlegt að vera viss um að kostnaðurinn við þessa birgðavöru endurspeglist í framlegð, eða kostnaði seldra vara (COGS) á sölupöntunarreikningnum. Þegar innkaupapöntunin er bókuð, eru birgðir mótteknar með kostnaðinum 120,00 USD. Ef þetta skjal sölupöntunar er merkt við innkaupspöntunina áður en fylgiseðillinn eða reikningurinn er bókaður, er kostnaður seldra VARA 120,00 USD, en ekki núverandi meðaltal kostnaðar vörunnar. Ef að fylgiseðill sölupöntunarinnar eða reikningur er bókaður áður en merking á sér stað, mun kostnaður seldra vara verða bókaður á meðalkostnaðarverði. Áður en birgðalokun er framkvæmd er hægt að merkja þessar tvær færslur, hvora fyrir aðra.

Þegar innhreyfingarfærsla er merkt við úthreyfingarfærslu er ekki tekið tillit til villuleitaraðferðarinnar sem var skilgreind í vörulíkanaflokknum og kerfið jafnar þessar færslur hverja við aðra. Hægt er að merkja færslu handvirkt á móti sölupöntunarlínu á síðunni **Upplýsingar um sölupöntun** með því að velja **Birgðir \> Merking** í flýtiflipanum **Sölupöntunarlínur**. Hægt er að skoða opnar innhreyfingarfærslur á síðunni **Merking**. Hægt er að stemma eða merkja úthreyfingarfærslu fyrir opna innhreyfingarfærslu fyrir skráðan hlut úr bókaðri birgðaleiðréttingabók. Eftirfarandi skýringarmynd sýnir þessar færslur:

- 1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
- 1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
- 2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
- 2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 22,00 USD á hverja.
- 3a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 16,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 3b. Fjárhagsleg úthreyfing birgða fyrir magnið 1 með kostnaðarverð 16,00 USD á hverja (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 3c. Fjárhagsleg úthreyfing birgða fyrir 3b er merkt við fjárhagslega úthreyfing birgða fyrir 2b.
- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 23,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 7\. Birgðalokun er framkvæmd. Samkvæmt merkingarreglunni sem notar aðferðina FIFO eru merktu færslurnar jafnaðar á móti hvor annarri. Í þessu dæmi er 3b gerð upp á móti 2b og leiðrétting fyrir 6,00 USD er sett inn á 3b til að færa gildið í 22,00 USD. Í þessu dæmi eru engin viðbótarjafnanir gerð vegna þess að lokunin skapar einungis jafnanir fyrir fjárhagslega uppfærðar færslur.

Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans FIFO á þessar tegundir færslna þegar merkingar á milli úthreyfinga og innhreyfinga eru notaðar.

![FIFO með merkingu.](./media/fifo-with-marking.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Efnislegar færslur eru táknaðar með styttri ljósgráum örvum.
- Fjárhagsfærslur eru táknaðar með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svartri lóðréttri línu. Dagsetningin er tekin fram neðst á skýringarmyndinni.
- Birgðalokanir eru sýndar með rauðri lóðréttri strikalínu.
- Jafnanir og merkingar sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
