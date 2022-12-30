---
title: LIFO (síðast inn - fyrst út) með efnislegu virði og marki
description: Síðast inn, fyrst út (LIFO) er birgðalíkan þar sem síðustu (nýjustu) innhreyfingar eru úthreyfðar fyrst. Úthreyfingar úr birgðum eru jafnaðar á móti síðustu innhreyfingu í birgðir, samkvæmt dagsetningu birgðafærslunnar.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55021
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1acc103291c5d648ac7e179a598348cd9cc2a93
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135570"
---
# <a name="lifo-with-physical-value-and-marking"></a>LIFO (síðast inn - fyrst út) með efnislegu virði og marki

[!include [banner](../includes/banner.md)]

Síðast inn, fyrst út (LIFO) er birgðastjórnunar- og matsaðferð þar sem birgðir sem voru framleiddar eða keyptar síðast eru seldar, notaðar eða fargað fyrst. Á meðan birgðahaldi stendur í Microsoft Dynamics 365 Supply Chain Management mun kerfið búa til uppgjör þar sem síðasta kvittun er borin saman við fyrstu útgáfu og svo framvegis. Jafnanir og jöfnunarregla byggja á fjárhagsdagsetningu birgðafærslna. Hægt er að framkvæma bráðabirgðamat á uppgjörum og leiðréttingum með því að keyra endurreikningsferli birgða.

Hægt er að hnekkja LIFO reglunni með því að merkja birgðafærslur svo að tiltekin innhreyfing vöru sé jöfnuð gagnvart tiltekinni úthreyfingu. Reglubundin birgðalokun er nauðsynleg þegar notað er LIFO-birgðalíkan vegins meðaltals til að búa til uppgjör og breyta gildi úthreyfinga í samræmi við LIFO-reglu. Þar til þú keyrir birgðalokunarferli, eru úthreyfingarfærslur metnar á hlaupandi meðaltali þegar efnislegar og fjárhagslegar uppfærslur áttu sér stað. Nema ef merking er notuð þá er hlaupandi meðaltal reiknað út þegar efnisleg eða fjárhagsleg uppfærsla er framkvæmd.

Eftirfarandi dæmi sýna áhrif þess að nota LIFO með þremur mismunandi skilgreiningum:

- LIFO án valkostarins **Taka efnislegt virði með**
- LIFO með valkostinum **Taka efnislegt virði með**
- LIFO með merkingum

## <a name="lifo-without-the-include-physical-value-option"></a>LIFO án þess að efnislegt virði sé tekið með

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
- 7\. Birgðalokun er framkvæmd. Á grundvelli LIFO aðferðarinnar, verður fyrsta fjárhagslega uppfærða úthreyfingin jöfnuð á móti síðustu fjárhagslega uppfærðu innhreyfingunni o.s.frv. Í þessu dæmi er búið til eitt uppgjör milli 5b og 3b. Leiðrétting upp á USD 14,00 verður gerð á 3b og endanlegur kostnaður verður 30,00 USD.

Eftirfarandi sýnidæmi sýnir áhrif birgðalíkans FIFO á þessar tegundir færslna þegar **Taka efnislegt virði með** valkosturinn er ekki notaður.

![LIFO án þess að efnislegt virði sé tekið með.](./media/lifo-without-including-physical-value.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Efnislegar færslur eru táknaðar með styttri ljósgráum örvum.
- Fjárhagsfærslur eru táknaðar með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan ásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svartri lóðréttri línu. Dagsetningin er tekin fram neðst á skýringarmyndinni.
- Birgðalokanir eru sýndar með rauðri lóðréttri strikalínu.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="lifo-with-the-include-physical-value-option"></a>LIFO þar sem efnislegt virði er tekið með

Ef reiturinn **Taka efnislegt virði með** er valinn fyrir vöru í skjámyndinni **Vörulíkanaflokkar**, mun kerfið nota bæði efnislegar og fjárhagslegar innhreyfingarfærslur til að reikna út meðalkostnaðarverðið. Það sem það á við mun kerfið einnig leiðrétta efnislega uppfærða úthreyfingarfærslu. Þegar reiturinn **Taka með efnislegt virði** er hreinsaður, gerir birgðalokun sem notar LIFO-birgðalíkan aðeins gera jafnanir á færslum sem eru fjárhagslega uppfærðar.

Eftirfarandi skýringarmynd sýnir þessar færslur:

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
- 7\. Birgðalokun er framkvæmd. Á grundvelli LIFO aðferðarinnar, verður fyrsta fjárhagslega uppfærða úthreyfingin jöfnuð á móti síðustu fjárhagslega uppfærðu innhreyfingunni o.s.frv. Í þessu dæmi er búið til eitt uppgjör milli 3b og 5b. Leiðrétting upp á USD 14,00 verður gerð á 3b og endanlegur kostnaður verður 30,00 USD. Auk þess verður færsla 6a leiðrétt að kostnaði innhreyfingarfærslu 4a. Kerfið mun ekki jafna þessar færslur þar sem innhreyfingin uppfærist efnislega en ekki fjárhagslega. Í stað þess verður aðeins leiðrétting upp á 1,33 USD bókuð á efnislegu úthreyfingarfærsluna og leiðréttur kostnaður verður því 25,00 USD.

Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans LIFO á þessar tegundir færslna þegar **Taka efnislegt virði með** valkosturinn er notuð.

![LIFO þar sem efnislegt virði er tekið með.](./media/lifo-with-included-physical-value.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Efnislegar færslur eru táknaðar með styttri ljósgráum örvum.
- Fjárhagsfærslur eru táknaðar með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan ásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svartri lóðréttri línu. Dagsetningin er tekin fram neðst á skýringarmyndinni.
- Birgðalokanir eru sýndar með rauðri lóðréttri strikalínu.
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="lifo-with-marking"></a>LIFO með merkingu

Merking er aðferð sem gerir mögulegt að tengja eða merkja úthreyfingarfærslu við innhreyfingarfærslu. Merking getur farið fram annað hvort áður eða eftir að færsla er bókuð. Hægt er að nota merkingu þegar þú vilt vera viss um að nákvæmur kostnaður birgðanna þegar færsla er bókuð eða birgðalokun er framkvæmd. til dæmis þjónustudeild samþykkti flýtipöntun frá mikilvægum viðskiptavini. Þar sem þessi pöntun er flýtipöntun verður að greiða meira fyrir vöruna til þess að geta uppfyllt beiðni viðskiptavinarins.

Þá er nauðsynlegt að vera viss um að kostnaðurinn við þessa birgðavöru endurspeglist í framlegð, eða kostnaði seldra vara (COGS) á sölupöntunarreikningnum. Þegar innkaupapöntunin er bókuð, eru birgðir mótteknar með kostnaðinum 120,00 USD. Ef þetta skjal sölupöntunar er merkt við innkaupspöntunina áður en fylgiseðillinn eða reikningurinn er bókaður, er kostnaður seldra VARA 120,00 USD, en ekki núverandi meðaltal kostnaðar vörunnar. Ef að fylgiseðill sölupöntunarinnar eða reikningur er bókaður áður en merking á sér stað, mun kostnaður seldra vara verða bókaður á meðalkostnaðarverði.

Áður en birgðalokun er framkvæmd er hægt að merkja þessar tvær færslur, hvora fyrir aðra.

Hægt er að merkja úthreyfingarfærslu við innhreyfingu áður en færsla er bókuð. Hægt er að gera þessa merkingu úr sölupöntunarlínu á síðunni **Upplýsingar um sölupöntun** með því að velja **Birgðir \> Merking** í flýtiflipanum **Sölupöntunarlínur**. Hægt er að skoða opnar innhreyfingarfærslur á síðunni **Merking**.

Einnig er Hægt að merkja úthreyfingarfærslu við innhreyfingu eftir að færslan er bókuð. Hægt er að stemma eða merkja úthreyfingarfærslu fyrir opna innhreyfingarfærslu fyrir skráðan hlut úr bókaðri birgðaleiðréttingabók.

Eftirfarandi skýringarmynd sýnir þessar færslur:

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
- 7\. Birgðalokun er framkvæmd. Samkvæmt merkingarreglunni sem notar aðferðina LIFO eru merktu færslurnar jafnaðar á móti hvor annarri. Í þessu dæmi er 3b gerð upp á móti 2b og leiðrétting fyrir 6,00 USD er sett inn á 3b til að færa gildið í 22,00 USD. Í þessu dæmi eru engin viðbótarjafnanir gerð vegna þess að lokunin skapar einungis jafnanir fyrir fjárhagslega uppfærðar færslur.

Nýja meðalkostnaðarverðið sem er í gangi endurspeglar meðaltal fjárhagslegu og efnislegu uppfærðu færslnanna, 17,50 USD.

Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans LIFO á þessar tegundir færslna þegar merkingar á milli úthreyfinga og innhreyfinga eru notaðar.

![LIFO með merkingum.](./media/lifo-with-marking.png)

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Efnislegar færslur eru táknaðar með styttri ljósgráum örvum.
- Fjárhagsfærslur eru táknaðar með lengri svörtum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan ásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan ásinn.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Hver dagsetning á skýringarmyndinni er aðskilin með þunnri svartri lóðréttri línu. Dagsetningin er tekin fram neðst á skýringarmyndinni.
- Birgðalokanir eru sýndar með rauðri lóðréttri strikalínu.
- Jafnanir og merkingar sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
