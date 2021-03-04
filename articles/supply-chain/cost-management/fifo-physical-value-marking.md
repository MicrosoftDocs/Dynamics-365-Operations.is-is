---
title: Um FIFO með merkingu og efnislegt virði
description: Fyrst inn, fyrst út (FIFO) er birgðalíkan þar sem fyrstu innhreyfingar eru úthreyfðar fyrst. Fjárhagslega uppfærð vandamál úr birgðum eru jöfnuð á móti fyrstu fjárhagslega uppfærðu móttöku í birgðir, byggt á fjárhagsdagsetningu birgðafærslu.
author: AndersGirke
manager: tfehr
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 54682
ms.assetid: dc0e2855-83a0-41a7-a398-3c7852597d1a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1322d43d536bf7ff4c40fcdecebbd95a46f70d2d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430313"
---
# <a name="fifo-with-physical-value-and-marking"></a>Um FIFO með merkingu og efnislegt virði

[!include [banner](../includes/banner.md)]

Fyrst inn, fyrst út (FIFO) er birgðalíkan þar sem fyrstu innhreyfingar eru úthreyfðar fyrst. Fjárhagslega uppfærð vandamál úr birgðum eru jöfnuð á móti fyrstu fjárhagslega uppfærðu móttöku í birgðir, byggt á fjárhagsdagsetningu birgðafærslu. 

Þegar FIFO er notuð, þarf ekki að nota FIFO-regla. Þess í stað geturðu valið að merkja birgðafærslur svo að tiltekin innhreyfing vöru sé jöfnuð gagnvart tiltekinni úthreyfingu í stað þess að nota regluna um vegið meðaltal. Mælt er með með reglulegri birgðalokun þegar FIFO birgðalíkan er notað. Eftirfarandi dæmi sýna áhrifin þess að nota LIFO með þremur mismunandi skilgreiningum:

-   LIFO án valkostarins **Taka efnislegt virði með**
-   FIFO með valkostinum **Taka efnislegt virði með**
-   FIFO með merkingu

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO án valkostarins Taka efnislegt virði með
Í þessu dæmi, er birgðalíkanaflokkurinn ekki merktur til að innihalda efnislega virðið. Eftirfarandi skýringarmynd sýnir þessar færslur:

-   1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
-   1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
-   2a. Efnisleg móttaka birgða fyrir magn upp á 2 á kostnað upp á 10 Bandaríkjadali stykkið.
-   2b. Fjárhagsleg úthreyfing birgða fyrir magn upp á 2 á kostnaðarverði upp á 10 Bandaríkjadali á stykkið.
-   3a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
-   4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
-   4b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
-   5a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn USD 20.00 á hverja (hlaupandi meðaltal fjárhagslega uppfærðra færslna).
-   5b. Fjárhagsleg úthreyfing birgða fyrir magnið 1 með kostnaðinn USD 15.00 á hverja (hlaupandi meðaltal fjárhagslega uppfærðra færslna).
-   6. Birgðalokun er framkvæmd. Á grundvelli FIFO aðferðarinnar, verður fyrsta fjárhagslega uppfærða úthreyfingin jöfnuð gagnvart fyrstu fjárhagslega uppfærðu innhreyfingunni. Leiðrétting upp á 5,00 USD er gerð á úthreyfingarfærslunni.

Nýja meðalkostnaðarverðið endurspeglar meðaltal fjárhagslega uppfærðu færslnanna. Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans FIFO á þessar tegundir færslna þegar **Taka efnislegt virði með** valkosturinn er ekki notuð. 

![FIFO án efnistlegs virðis](./media/fifowithoutincludephysicalvalue.gif) 

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

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO með valkostinum Taka efnislegt virði með
Ef reiturinn **Taka efnislegt virði með** er valinn fyrir vöru í skjámyndinni **Vörulíkanaflokkar**, mun kerfið nota bæði efnislegar og fjárhagslegar innhreyfingarfærslur til að reikna út meðalkostnaðarverðið. Kerfið gerir líka breytingar á uppfærðum úthreyfingafærslum, þar sem við á. Þegar gátreiturinn **taka efnislegt virði með** er hreinsaður munu birgðalokin með FIFO-birgðalíkanið aðeins gera uppgjör í þeim færslum sem hafa verið fjárhagslega uppfærðar. Eftirfarandi skýringarmynd sýnir þessar færslur:

-   1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
-   1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
-   2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
-   2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 20,00 USD á hverja.
-   3a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
-   4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
-   4b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
-   5a. Efnisleg úthreyfing birgða fyrir magnið 1 á kostnaðarverði USD 21,25 hver (rekstrarmeðaltal fjárhagslegra og efnislegra uppfærðra færslna).
-   5b. Fjárhagsleg úthreyfing birgða fyrir magnið 1 á kostnaðarverði USD 21,25 hver (rekstrarmeðaltal fjárhagslegra og efnislegra færslna sem hafa verið uppfærðar).
-   6a. Efnisleg úthreyfing birgða fyrir magn 1 með kostnaðinn 21,25 USD á hverja.
-   7. Birgðalokun er framkvæmd. Á grundvelli FIFO aðferðarinnar, verður fyrsta fjárhagslega úthreyfingarfærsla jöfnuð eða leiðrétt gagnvart fyrstu uppfærðu innhreyfingunni, annað hvort fjárhagslega eða efnislega.

Færsla 5b verður jöfnuð við innhreyfingarfærslu 1b. Það verður neikvæð jöfnun upp á 11,25 USD til þessarar úthreyfingarfærslu. Nýja meðalkostnaðarverðið sem er í gangi endurspeglar meðaltal fjárhagslegu og efnislegu uppfærðu færslnanna, 27,50 USD. Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans FIFO á þessar tegundir færslna þegar **Taka efnislegt virði með** valkosturinn er notuð. 

![FIFO með Taka efnislegt virði með](./media/fifowithincludephysicalvalue.gif) 

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

## <a name="fifo-with-marking"></a>FIFO með merkingu
Merking er aðferð sem gerir mögulegt að tengja eða merkja úthreyfingarfærslu við innhreyfingarfærslu. Merking getur farið fram annað hvort áður eða eftir að færsla er bókuð. Hægt er að nota merkingu þegar þú vilt vera viss um að nákvæmur kostnaður birgðanna þegar færsla er bókuð eða birgðalokun er framkvæmd. til dæmis þjónustudeild samþykkti flýtipöntun frá mikilvægum viðskiptavini. Þar sem þessi pöntun er flýtipöntun verðu að greiða meira fyrir vöruna til þess að geta uppfyllt beiðni viðskiptavinarins. Þá er nauðsynlegt að vera viss um að kostnaðurinn við þessa birgðavöru endurspeglist í framlegð, eða kostnaði seldra vara (COGS) á þessum sölupöntunarreikningi. Þegar innkaupapöntunin er bókuð, eru birgðir mótteknar með kostnaðinum 120,00 USD. Ef þetta skjal sölupöntunar er merkt við innkaupspöntunina áður en fylgiseðillinn eða reikningurinn er bókaður, er kostnaður seldra VARA 120,00 USD, en ekki núverandi meðaltal kostnaðar vörunnar. Ef að fylgiseðill sölupöntunarinnar eða reikningur er bókaður áður en merking á sér stað, mun kostnaður seldra vara verða bókaður á meðalkostnaðarverði. Áður en birgðalokun er framkvæmd er hægt að merkja þessar tvær færslur, hvora fyrir aðra. Þegar innhreyfingarfærsla stemmir við úthreyfingarfærslu er ekki tekið tillit til villuleitaraðferðarinnar sem var skilgreind í vörulíkanaflokknum og kerfið jafnar þessar færslur hverja við aðra. Hægt er að merkja úthreyfingarfærslu við innhreyfingu áður en færsla er bókuð. Hægt er að gera þetta frá sölupöntunarlínu á síðunni **Ítarupplýsingar sölupöntunar**. Hægt er að skoða opnar innhreyfingarfærslur á síðunni **Merking**. Einnig er Hægt að merkja úthreyfingarfærslu við innhreyfingu eftir að færslan er bókuð. Hægt er að stemma eða merkja úthreyfingarfærslu fyrir opna innhreyfingarfærslu fyrir skráðan hlut úr bókaðri birgðaleiðréttingabók. Eftirfarandi skýringarmynd sýnir þessar færslur:

-   1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
-   1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
-   2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
-   2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 20,00 USD á hverja.
-   3a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
-   4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
-   4b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
-   5a. Efnisleg úthreyfing birgða fyrir magnið 1 á kostnaðarverði USD 21,25 hver (rekstrarmeðaltal fjárhagslegra og efnislegra uppfærðra færslna).
-   5b. Fjárhagsleg úthreyfing birgða fyrir magn upp á 1 er merkt á innhreyfingu birgða 2b aður en færslan er bókuð. Þessi færsla er bókuð á kostnaðarverðinu 20,00 USD.
-   6a. Efnisleg úthreyfing birgða fyrir magn 1 með kostnaðinn 21,25 USD á hverja.
-   7. Birgðalokun er framkvæmd. Þar sem fjárhagslega uppfærð FIFO-færsla er merkt á fyrirliggjandi móttöku eru þessar færslur jafnaðar hvor við aðra og engin leiðrétting er gerð.

Nýja meðalkostnaðarverðið sem er í gangi endurspeglar meðaltal fjárhagslegu og efnislegu uppfærðu færslnanna, 27,50 USD. Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans FIFO á þessar tegundir færslna þegar merkingar á milli úthreyfinga og innhreyfinga eru notaðar. 

![FIFO með Merking](./media/fifowithmarking.gif) 

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






[!INCLUDE[footer-include](../../includes/footer-banner.md)]