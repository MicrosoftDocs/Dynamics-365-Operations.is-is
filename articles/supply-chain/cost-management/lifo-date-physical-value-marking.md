---
title: LIFO dagsetning með efnislegt virði og merkingu
description: Síðast inn, Fyrst út  dagsetning (lifo-Dagsetning) er birgðalíkan sem byggist á lifo-grunnreglu. Úthreyfingar úr birgðum eru jafnaðar á móti síðustu innhreyfingu í birgðir, samkvæmt dagsetningu birgðafærslunnar. Hafi ekkert verið móttekið fyrir úthreyfinguna jafnast hún, sé notuð LIFO-dagsetning, við innhreyfingar sem kunna að verða eftir úthreyfingardagsetninguna. Fleiri en eina úthreyfingu innan sama dags má jafna í þeirri röð að sú síðasta jafnist við síðustu innhreyfingu.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 51592
ms.assetid: d9f13274-3268-444f-85c8-b686fd39286d
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2c06443532519ad5d6c36a6f4ed1f1c4d136664
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967634"
---
# <a name="lifo-date-with-physical-value-and-marking"></a>LIFO dagsetning með efnislegt virði og merkingu

[!include [banner](../includes/banner.md)]

Síðast inn, Fyrst út  dagsetning (lifo-Dagsetning) er birgðalíkan sem byggist á lifo-grunnreglu. Úthreyfingar úr birgðum eru jafnaðar á móti síðustu innhreyfingu í birgðir, samkvæmt dagsetningu birgðafærslunnar. Hafi ekkert verið móttekið fyrir úthreyfinguna jafnast hún, sé notuð LIFO-dagsetning, við innhreyfingar sem kunna að verða eftir úthreyfingardagsetninguna. Fleiri en eina úthreyfingu innan sama dags má jafna í þeirri röð að sú síðasta jafnist við síðustu innhreyfingu. 

Þegar þú notast við Síðast inn, Fyrst út dagsetninguna (LIFO-dagsetningu) birgðalíkan, Hafi ekkert verið móttekið fyrir úthreyfinguna jafnast hún við innhreyfingar sem kunna að verða eftir úthreyfingardagsetninguna. Fleiri en eina úthreyfingu innan sama dags má jafna í þeirri röð, síðasta úthreyfing, síðasta innhreyfing. Þegar lifo-Dagsetning er notuð, þarf ekki að nota LIFO-dagsetningarregluna. Þess í stað geturðu valið að merkja birgðafærslur svo að tiltekin innhreyfing vöru sé jöfnuð gagnvart tiltekinni úthreyfingu í stað þess að nota regluna um vegið meðaltal. 

Mælt er með reglulegri birgðalokun þegar FIFO birgðalíkanið er notað. 

Eftirfarandi dæmi sýna áhrifin þess að nota LIFO dagsetningu með þremur mismunandi skilgreiningum:

-   LIFO dagsetning án valkostarins **Taka efnislegt virði með**
-   LIFO-dagsetning með valkostinum **Taka efnislegt virði með**
-   LIFO-dagsetning með merkingu

## <a name="lifo-date-without-the-include-physical-value-option"></a>LIFO-dagsetning án valkostarins Taka efnislegt virði með
Í þessu dæmi, er birgðalíkanaflokkurinn ekki merktur til að innihalda efnislega virðið. Eftirfarandi skýringarmynd sýnir þessar færslur:

-   1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
-   1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
-   2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
-   2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 20,00 USD á hverja.
-   3a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
-   4a. Efnisleg úthreyfing birgða með magninu 1 á kostnaðarverðinu USD 15,00 (meðaltal fjárhagslegra uppfærðra færslna).
-   4b. Fjárhagsleg úthreyfing birgða með magninu 1 á kostnaðarverðinu USD 15,00 (meðaltal fjárhagslegra uppfærðra færslna).
-   5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
-   5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
-   6. Birgðalokun er framkvæmd. Á grundvelli LIFO dagsetningaraðferðarinnar, verður fyrsta fjárhagslega uppfærða úthreyfingin jöfnuð gagnvart fyrstu fjárhagslega uppfærðu innhreyfingunni samkvæmt dagsetningu. Leiðrétting upp á 5,00 USD er gerð á úthreyfingarfærslunni. Þessar færslur verða jafnaðar með hver annarri.

Nýtt meðaltal kostnaðarverðs endurspeglar meðaltal færslna sem hafa verið uppfærðar fjárhagslega á 15,00 USD. 

Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans Lifo-dagsetningar þegar **Taka efnislegt virði með** valkosturinn er ekki notuð. ![LIFO dagsetning með Taka efnislegt virði með](./media/lifodatewithoutincludephysicalvalue.gif) 

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
- Fyrir ofan (eða fyrir neðan) Hvert Lóðrétt ör er virði birgðafærslu tilgreint í sniðinu Quantity@Unitprice.
- Birgðafærslugildi innan sviga bendir til þess að birgðafærslan sé efnislega bókuð í birgðir.
- Birgðafærslugildi sem er ekki innan sviga bendir til þess að birgðafærslan sé fjárhagslega bókuð í birgðir.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Birgðalokun eru sýndar með rauðri lóðréttri punktaðri línu og merkinu *birgðalokun*
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="lifo-date-with-the-include-physical-value-option"></a>LIFO-dagsetning með valkostinum Taka efnislegt virði með
Hægt er að velja gátreit **Taka efnislegt virði með** fyrir vöru í skjámyndinni **vörulíkanaflokkur**. Í þessi tilfelli notar kerfið bæði efnislegar og fjárhagslegar innhreyfingarfærslur til að reikna út meðalkostnaðarverðið. Kerfið gerir líka breytingar á uppfærðum úthreyfingafærslum, þar sem við á. Þegar reiturinn **Taka með efnislegt virði** er hreinsaður, gerir birgðalokun sem notar LIFO-dagsetningarbirgðalíkani aðeins gera jafnanir á færslum sem eru fjárhagslega uppfærðar. 

Í þessu dæmi, er birgðalíkanaflokkurinn merktur til að innihalda efnislega virðið. 

Eftirfarandi skýringarmynd sýnir þessar færslur:

-   1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
-   1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
-   2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
-   2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 20,00 USD á hverja.
-   3a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
-   4a. Efnisleg úthreyfing birgða með magninu 1 á kostnaðarverðinu 18,33 USD (meðaltal fjárhagslegra uppfærðra færslna).
-   4b. Fjárhagsleg úthreyfing birgða með magninu 1 á kostnaðarverðinu 18,33 USD (meðaltal fjárhagslegra uppfærðra færslna).
-   5a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
-   5b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
-   6. Birgðalokun er framkvæmd. Á grundvelli LIFO dagsetningaraðferðarinnar, verður síðasta uppfærða úthreyfingin leiðrétt eða jöfnuð gagnvart síðustu uppfærðu innhreyfingunni samkvæmt dagsetningu. Þessar færslur verða ekki jafnaðar við hvor aðra þar sem fjárhagslegu innhreyfingarfærslunni er jafnað í efnislega uppfærða færslu. Í stað þess, aðeins Leiðrétting upp á 6,67 USD er gerð á úthreyfingarfærslunni.

Nýtt meðaltal kostnaðarverðs endurspeglar meðaltal færslna sem hafa verið uppfærðar fjárhagslega á 20,00 USD. 

Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans Lifo þegar **Taka efnislegt virði með** valkosturinn er notuð. ![LIFO dagsetning með Taka efnislegt virði með](./media/lifodatewithincludephysicalvalue.gif) 

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
- Fyrir ofan (eða fyrir neðan) Hvert Lóðrétt ör er virði birgðafærslu tilgreint í sniðinu Quantity@Unitprice.
- Birgðafærslugildi innan sviga bendir til þess að birgðafærslan sé efnislega bókuð í birgðir.
- Birgðafærslugildi sem er ekki innan sviga bendir til þess að birgðafærslan sé fjárhagslega bókuð í birgðir.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Birgðalokun eru sýndar með rauðri lóðréttri punktaðri línu og merkinu *birgðalokun*
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="lifo-date-with-marking"></a>LIFO-dagsetning með merkingu
Merking er aðferð sem gerir mögulegt að tengja eða merkja úthreyfingarfærslu við innhreyfingarfærslu. Merking getur farið fram annað hvort áður eða eftir að færsla er bókuð. Hægt er að nota merkingu þegar þú vilt vera viss um að nákvæmur kostnaður birgðanna þegar færsla er bókuð eða birgðalokun er framkvæmd. 

til dæmis þjónustudeild samþykkti flýtipöntun frá mikilvægum viðskiptavini. Þar sem þessi pöntun er flýtipöntun þarf að greiða meira fyrir vöruna til þess að geta uppfyllt beiðni viðskiptavinarins. Þá er nauðsynlegt að vera viss um að kostnaðurinn við þessa birgðavöru endurspeglist í framlegð, eða kostnaði seldra vara (COGS) á þessum sölupöntunarreikningi. 

Þegar innkaupapöntunin er bókuð, eru birgðir mótteknar með kostnaðinum 120,00 USD. Ef þetta skjal sölupöntunar er merkt við innkaupspöntunina áður en fylgiseðillinn eða reikningurinn er bókaður, er kostnaður seldra VARA 120,00 USD, en ekki núverandi meðaltal kostnaðar vörunnar. Ef að fylgiseðill sölupöntunarinnar eða reikningur er bókaður áður en merking á sér stað, mun kostnaður seldra vara verða bókaður á meðalkostnaðarverði. 

Áður en birgðalokun er framkvæmd er hægt að merkja þessar tvær færslur, hvora fyrir aðra. 

Til dæmis, Innhreyfingarfærsla er merkt við úthreyfingarfærslu. Í þessu tilfelli, villuleitaraðferðarinnar sem var skilgreind í vörulíkanaflokk vöru er hunsuð, og kerfið jafnar þessar færslur hverja við aðra. 

Hægt er að merkja úthreyfingarfærslu við innhreyfingu áður en færsla er bókuð. Hægt er að gera þetta frá sölupöntunarlínu á síðunni **Ítarupplýsingar sölupöntunar**. Hægt er að skoða opnar innhreyfingarfærslur á síðunni **Merking**. 

Einnig er Hægt að merkja úthreyfingarfærslu við innhreyfingu eftir að færslan er bókuð. Hægt er að stemma eða merkja úthreyfingarfærslu fyrir opna innhreyfingarfærslu fyrir skráðan hlut úr bókaðri birgðaleiðréttingabók. 

Eftirfarandi skýringarmynd sýnir þessar færslur:

-   1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
-   1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
-   2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
-   2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 20,00 USD á hverja.
-   3a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
-   4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
-   4b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
-   5a. Efnisleg úthreyfing birgða fyrir magnið 1 á kostnaðarverði USD 21,25 hver (rekstrarmeðaltal fjárhagslegra og efnislegra uppfærðra færslna).
-   5b. Fjárhagsleg úthreyfing birgða fyrir magn upp á 1 er merkt á innhreyfingu birgða 2b aður en færslan er bókuð. Þessi færsla er bókuð með kostnaðinum USD 20,00 fyrir hverja.
-   6a. Efnisleg úthreyfing birgða fyrir magn 1 með kostnaðinn 21,25 USD á hverja.
-   7. Birgðalokun er framkvæmd. Þar sem fjárhagslega uppfærð Fyrst inn fyrst út, FIFO-færsla, er merkt á fyrirliggjandi móttöku eru þessar færslur jafnaðar hvor við aðra og engin leiðrétting er gerð.

Nýtt meðaltal kostnaðarverðs endurspeglar meðaltal færslna sem hafa verið uppfærðar fjárhagslega og efnislega á 27,50 USD. 

Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans Lifo þegar merking á milli úthreyfinga og innhreyfinga er notuð. ![LIFO dagsetning með Merking](./media/lifodatewithmarking.gif) 

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
- Fyrir ofan (eða fyrir neðan) Hvert Lóðrétt ör er virði birgðafærslu tilgreint í sniðinu Quantity@Unitprice.
- Birgðafærslugildi innan sviga bendir til þess að birgðafærslan sé efnislega bókuð í birgðir.
- Birgðafærslugildi sem er ekki innan sviga bendir til þess að birgðafærslan sé fjárhagslega bókuð í birgðir.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Birgðalokun eru sýndar með rauðri lóðréttri punktaðri línu og merkinu *birgðalokun*
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.




