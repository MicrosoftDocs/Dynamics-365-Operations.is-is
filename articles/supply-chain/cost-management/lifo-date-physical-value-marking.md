---
title: Dagsetning LIFO (síðast inn - fyrst út) með efnislegt virði og merkingu
description: Síðast inn, Fyrst út  dagsetning (lifo-Dagsetning) er birgðalíkan sem byggist á lifo-grunnreglu. Úthreyfingar úr birgðum eru jafnaðar á móti síðustu innhreyfingu í birgðir, samkvæmt dagsetningu birgðafærslunnar. Hafi ekkert verið móttekið fyrir úthreyfinguna jafnast hún, sé notuð LIFO-dagsetning, við innhreyfingar sem kunna að verða eftir úthreyfingardagsetninguna. Fleiri en eina úthreyfingu innan sama dags má jafna í þeirri röð að sú síðasta jafnist við síðustu innhreyfingu.
author: JennySong-SH
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 51592
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ca344e6ca81814e787046f6ece97625d035346d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671451"
---
# <a name="lifo-date-with-physical-value-and-marking"></a>Dagsetning LIFO (síðast inn - fyrst út) með efnislegt virði og merkingu

[!include [banner](../includes/banner.md)]

Síðast inn, fyrst út dagsetning (LIFO date) er birgðastjórnunar- og matsaðferð þar sem birgðir sem voru framleiddar eða keyptar síðast eru seldar, notaðar eða fargað fyrst. Á meðan birgðahaldi er lokað í Microsoft Dynamics 365 Supply Chain Management mun kerfið búa til uppgjör þar sem síðasta kvittun er borin saman við fyrstu útgáfu fyrir hvern ákveðinn dag frá og með elsta degi fyrst og svo framvegis. Þegar þú notast við Síðast inn, Fyrst út dagsetninguna (LIFO-dagsetningu) birgðalíkan, Hafi ekkert verið móttekið fyrir úthreyfinguna jafnast hún við innhreyfingar sem kunna að verða eftir úthreyfingardagsetninguna. Jafnanir og jöfnunarregla byggja á fjárhagsdagsetningu birgðafærslna. Þegar nokkur mál koma upp sama daginn þá eru þau jöfnuð í röðinni síðasta úthreyfing, síðasta innhreyfing. Hægt er að framkvæma bráðabirgðamat á uppgjörum og leiðréttingum með því að keyra endurreikningsferli birgða.

Hægt er að hnekkja LIFO dagsreglunni með því að merkja birgðafærslur svo að tiltekin innhreyfing vöru sé jöfnuð gagnvart tiltekinni úthreyfingu. Reglubundin birgðalokun er nauðsynleg þegar notað er birgðalíkanið LIFO-dagsetning til að búa til jafnanir og breyta gildi úthreyfinga í samræmi við LIFO-regluna. Þar til þú keyrir birgðalokunarferli, eru úthreyfingarfærslur metnar á hlaupandi meðaltali þegar efnislegar og fjárhagslegar uppfærslur áttu sér stað. Nema ef merking er notuð þá er hlaupandi meðaltal reiknað út þegar efnisleg eða fjárhagsleg uppfærsla er framkvæmd.

Mælt er með reglulegri birgðalokun þegar FIFO birgðalíkanið er notað.

Eftirfarandi dæmi sýna áhrifin þess að nota LIFO dagsetningu með þremur mismunandi skilgreiningum:

-  LIFO dagsetning án valkostarins **Taka efnislegt virði með**
- LIFO-dagsetning með valkostinum **Taka efnislegt virði með**
- LIFO dagsetning með Merking

## <a name="lifo-date-without-the-include-physical-value-option"></a>LIFO-dagsetning án valkostarins Taka efnislegt virði með

Í þessu dæmi, er birgðalíkanaflokkurinn ekki merktur til að innihalda efnislega virðið. Eftirfarandi skýringarmynd sýnir þessar færslur:

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
- 7\. Birgðalokun er framkvæmd. Á grundvelli aðferðar LIFO-dagsetningar verður fyrsta fjárhagslega uppfærða úthreyfingin jöfnuð gagnvart fyrstu fjárhagslega uppfærðu innhreyfingunni sem hefst á fyrsta deginum og svo framvegis. Í þessu dæmi er búið til eitt uppgjör milli 3b og 2b. Leiðrétting upp á 6,00 USD verður gerð á 3b og endanlegur kostnaður verður 22,00 USD.

Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans Lifo-dagsetningar þegar **Taka efnislegt virði með** valkosturinn er ekki notuð.

![LIFO-dagsetning án valkostarins Taka efnislegt virði með.](media/lifo-date-without-include-physical-value.png)

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

## <a name="lifo-date-with-the-include-physical-value-option"></a>LIFO-dagsetning með valkostinum Taka efnislegt virði með

Ef reiturinn **Taka efnislegt virði með** er valinn fyrir vöru í skjámyndinni **Vörulíkanaflokkar**, mun kerfið nota bæði efnislegar og fjárhagslegar innhreyfingarfærslur til að reikna út meðalkostnaðarverðið. Það sem það á við mun kerfið einnig leiðrétta efnislega uppfærða úthreyfingarfærslu. Þegar reiturinn **Taka með efnislegt virði** er hreinsaður, gerir birgðalokun sem notar LIFO-dagsetningarbirgðalíkani aðeins gera jafnanir á færslum sem eru fjárhagslega uppfærðar.

Í þessu dæmi, er birgðalíkanaflokkurinn merktur til að innihalda efnislega virðið. 

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
- 7\. Birgðalokun er framkvæmd. Á grundvelli aðferðar LIFO-dagsetningar verður fyrsta fjárhagslega uppfærða úthreyfingin jöfnuð gagnvart fyrstu fjárhagslega uppfærðu innhreyfingunni fyrir hvern dag sem byrjar á fyrsta deginum og svo framvegis. Í þessu dæmi er búið til eitt uppgjör milli 2b og 3b. Leiðrétting upp á 6,00 USD verður gerð á 3b og endanlegur kostnaður verður 22,00 USD. Auk þess verður færsla 6a leiðrétt að kostnaði innhreyfingarfærslu 5b. Kerfið mun ekki jafna þessar færslur þar sem innhreyfingin uppfærist efnislega en ekki fjárhagslega. Í stað þess verður aðeins leiðrétting upp á 6,33 USD bókuð á efnislegu úthreyfingarfærsluna og leiðréttur kostnaður verður því 30,00 USD.

Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans Lifo þegar **Taka efnislegt virði með** valkosturinn er notuð.

![LIFO-dagsetning með valkostinum „Taka efnislegt virði“ með.](media/lifo-date-with-include-physical-value.png)

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

## <a name="lifo-date-with-marking"></a>LIFO dagsetning með Merking

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
- 3c. Fjárhagsleg úthreyfing birgða fyrir 3b er merkt við fjárhagslega úthreyfing birgða fyrir 1b.
- 4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
- 5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
- 5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
- 6a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn 23,00 á hverja USD (hlaupandi meðaltal fjárhagslega bókaðra færslna).
- 7\. Birgðalokun er framkvæmd. Samkvæmt merkingarreglunni sem notar FIFO dagaaðferðina eru merktu færslurnar jafnaðar á móti hvor annarri. Í þessu dæmi er 3b gerð upp á móti færslu 1b og leiðrétting fyrir -6,00 USD er bókuð á færslu 3b til að færa gildið í 10,00 USD. Í þessu dæmi eru engin viðbótarjafnanir gerð vegna þess að lokunin skapar einungis jafnanir fyrir fjárhagslega uppfærðar færslur.

Eftirfarandi sýnidæmi sýnir áhrifum dagsetningar LIFO birgðalíkans  þegar merking á milli úthreyfinga og innhreyfinga er notuð. 

![LIFO dagsetning með Merking.](media/lifo-date-with-marking.png)

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
