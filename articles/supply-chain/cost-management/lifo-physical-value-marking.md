---
title: LIFO (síðast inn - fyrst út) með efnislegu virði og marki
description: Síðast inn, fyrst út (LIFO) er birgðalíkan þar sem síðustu (nýjustu) innhreyfingar eru úthreyfðar fyrst. Úthreyfingar úr birgðum eru jafnaðar á móti síðustu innhreyfingu í birgðir, samkvæmt dagsetningu birgðafærslunnar.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 55021
ms.assetid: 49c492b0-b018-44e0-928f-9671e54eee20
ms.search.region: Global
ms.search.industry: Retail
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 792ff4d7b72ce092fe1ad92e53172cf40f0ecf26
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569272"
---
# <a name="lifo-with-physical-value-and-marking"></a>LIFO (síðast inn - fyrst út) með efnislegu virði og marki

[!include [banner](../includes/banner.md)]

Síðast inn, fyrst út (LIFO) er birgðalíkan þar sem síðustu (nýjustu) innhreyfingar eru úthreyfðar fyrst. Úthreyfingar úr birgðum eru jafnaðar á móti síðustu innhreyfingu í birgðir, samkvæmt dagsetningu birgðafærslunnar. 

Í Síðast inn, fyrst út (LIFO) birgðalíkaninu eru síðustu (nýjustu) innhreyfingar úthreyfðar fyrst. Úthreyfingar úr birgðum eru jafnaðar á móti síðustu innhreyfingu í birgðir, samkvæmt dagsetningu birgðafærslunnar. Þegar LIFO er notað, þarf ekki að nota LIFO-regluna. Þess í stað geturðu valið að merkja birgðafærslur svo að tiltekin úthreyfing vöru sé jöfnuð gagnvart tiltekinni innhreyfingu. Við mælum með reglulegri birgðalokun þegar notað er birgðalíkan LIFO. 

Eftirfarandi dæmi sýna áhrif þess að nota LIFO með þremur mismunandi skilgreiningum:

-   LIFO án valkostarins **Taka efnislegt virði með**
-   LIFO með valkostinum **Taka efnislegt virði með**
-   LIFO með merkingum

## <a name="lifo-without-the-include-physical-value-option"></a>LIFO án þess að efnislegt virði sé tekið með
Í þessu dæmi, er birgðalíkanaflokkurinn ekki merktur til að innihalda efnislega virðið. Eftirfarandi skýringarmynd sýnir þessar færslur:

-   1a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 10,00 USD á hverja.
-   1b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 10,00 USD á hverja.
-   2a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 20,00 USD á hverja.
-   2b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 20,00 USD á hverja.
-   3a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 25,00 USD á hverja.
-   4a. Efnisleg innhreyfing birgða fyrir magn 1 með kostnaðinn 30,00 USD á hverja.
-   4b. Fjárhagsleg innhreyfing birgða fyrir magnið 1 með kostnaðinn 30,00 USD á hverja.
-   5a. Efnisleg úthreyfing birgða fyrir magnið 1 með kostnaðinn USD 20.00 á hverja (hlaupandi meðaltal fjárhagslega uppfærðra færslna).
-   5b. Fjárhagsleg úthreyfing birgða fyrir magnið 1 með kostnaðinn USD 20.00 á hverja (hlaupandi meðaltal fjárhagslega uppfærðra færslna).
-   6. Birgðalokun er framkvæmd. Á grundvelli LIFO aðferðarinnar, verður síðasta fjárhagslega uppfærða úthreyfingin jöfnuð á móti síðustu fjárhagslega uppfærðu innhreyfingunni. Leiðrétting upp á 10,00 USD er gerð á úthreyfingarfærslunni.

Nýtt meðaltal kostnaðarverðs endurspeglar meðaltal færslna sem hafa verið uppfærðar fjárhagslega, 15,00 USD. Eftirfarandi sýnidæmi sýnir áhrif birgðalíkans LIFO á þessar tegundir færslna þegar **Taka efnislegt virði með** valkosturinn er ekki notaður. 

![LIFO án Taka efnislegt virði með](./media/lifowithoutincludephysicalvalue.gif) 

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
- Verðgildi brigðafærslunnar er tilgreint fyrir ofan (eða neðan) hverja lóðrétta línu með sniðinu magn@einingarverð.
- Birgðafærslugildi innan sviga bendir til þess að birgðafærslan sé efnislega bókuð í birgðir.
- Birgðafærslugildi sem er ekki innan sviga bendir til þess að birgðafærslan sé fjárhagslega bókuð í birgðir.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Birgðalokun eru sýndar með rauðri lóðréttri punktaðri línu og merkinu *birgðalokun*
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="lifo-with-the-include-physical-value-option"></a>LIFO þar sem efnislegt virði er tekið með
Ef reiturinn **Taka efnislegt virði með** er valinn fyrir vöru í skjámyndinni **Vörulíkanaflokkar**, mun kerfið nota bæði efnislegar og fjárhagslegar innhreyfingarfærslur til að reikna út meðalkostnaðarverðið. Kerfið gerir líka breytingar á uppfærðum úthreyfingafærslum, þar sem við á. Þegar gátreiturinn **taka efnislegt virði með** er hreinsaður munu birgðalokin með LIFO-birgðalíkanið aðeins gera uppgjör í þeim færslum sem hafa verið fjárhagslega uppfærðar. 

Eftirfarandi skýringarmynd sýnir þessar færslur:

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
-   7. Birgðalokun er framkvæmd. Á grundvelli LIFO aðferðarinnar, verður síðasta úthreyfingarfærslan leiðrétt eða jöfnuð á móti síðustu uppfærðu innhreyfingunni.

Færsla 6a verður leiðrétt að innhreyfingarfærslu 4b. Kerfið mun ekki jafna þessar færslur þar sem innhreyfingin uppfærist efnislega en ekki fjárhagslega. Í stað þess verður aðeins leiðrétting upp á 8,75 USD bókuð á efnislegu úthreyfingarfærsluna. Færsla 5b verður jöfnuð við efnislega innhreyfingafærslu 3a. Kerfið mun ekki jafna þessar færslur þar sem þær eru ekki báðar fjárhagslega uppfærðar. Í stað þess verður aðeins leiðrétting upp á 3,75 USD gerð á úthreyfingarfærslunni. Nýja meðalkostnaðarverðið sem er í gangi endurspeglar meðaltal fjárhagslegu og efnislegu uppfærðu færslnanna, 20,00 USD. 

Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans LIFO á þessar tegundir færslna þegar **Taka efnislegt virði með** valkosturinn er notuð. 

![LIFO með Taka efnislegt virði með](./media/lifowithincludephysicalvalue.gif) 

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
- Verðgildi brigðafærslunnar er tilgreint fyrir ofan (eða neðan) hverja lóðrétta línu með sniðinu magn@einingarverð.
- Birgðafærslugildi innan sviga bendir til þess að birgðafærslan sé efnislega bókuð í birgðir.
- Birgðafærslugildi sem er ekki innan sviga bendir til þess að birgðafærslan sé fjárhagslega bókuð í birgðir.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Birgðalokun eru sýndar með rauðri lóðréttri punktaðri línu og merkinu *birgðalokun*
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="lifo-with-marking"></a>LIFO með merkingum
Merking er aðferð sem gerir mögulegt að tengja eða merkja úthreyfingarfærslu við innhreyfingarfærslu. Merking getur farið fram annað hvort áður eða eftir að færsla er bókuð. Hægt er að nota merkingu þegar þú vilt vera viss um að nákvæmur kostnaður birgðanna þegar færsla er bókuð eða birgðalokun er framkvæmd. til dæmis þjónustudeild samþykkti flýtipöntun frá mikilvægum viðskiptavini. Þar sem þessi pöntun er flýtipöntun verðu að greiða meira fyrir vöruna til þess að geta uppfyllt beiðni viðskiptavinarins. 

Þá er nauðsynlegt að vera viss um að kostnaðurinn við þessa birgðavöru endurspeglist í framlegð, eða kostnaði seldra vara (COGS) á þessum sölupöntunarreikningi. Þegar innkaupapöntunin er bókuð, eru birgðir mótteknar með kostnaðinum 120,00 USD. Ef þetta skjal sölupöntunar er merkt við innkaupspöntunina áður en fylgiseðillinn eða reikningurinn er bókaður, er kostnaður seldra VARA 120,00 USD, en ekki núverandi meðaltal kostnaðar vörunnar. Ef að fylgiseðill sölupöntunarinnar eða reikningur er bókaður áður en merking á sér stað, mun kostnaður seldra vara verða bókaður á meðalkostnaðarverði. 

Áður en birgðalokun er framkvæmd er hægt að merkja þessar tvær færslur, hvora fyrir aðra. 

Hægt er að merkja úthreyfingarfærslu við innhreyfingu áður en færsla er bókuð. Hægt er að gera þetta frá sölupöntunarlínu á síðunni **Ítarupplýsingar sölupöntunar**. Hægt er að skoða opnar innhreyfingarfærslur á síðunni**Merking**. 

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
-   7. Birgðalokun er framkvæmd. Þar sem fjárhagslega uppfærð FIFO-færsla er merkt á fyrirliggjandi móttöku eru þessar færslur jafnaðar hvor við aðra og engin leiðrétting er gerð.

Nýja meðalkostnaðarverðið sem er í gangi endurspeglar meðaltal fjárhagslegu og efnislegu uppfærðu færslnanna, 27,50 USD. 

Eftirfarandi sýnidæmi sýnir áhrifum birgðalíkans LIFO á þessar tegundir færslna þegar merkingar á milli úthreyfinga og innhreyfinga eru notaðar. 

![LIFO með Merking](./media/lifowithmarking.gif) 

**Lykill að skýringarmynd**

- Birgðafærslur eru táknaðar með lóðréttum örvum.
- Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
- Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
- Verðgildi brigðafærslunnar er tilgreint fyrir ofan (eða neðan) hverja lóðrétta línu með sniðinu magn@einingarverð.
- Birgðafærslugildi innan sviga bendir til þess að birgðafærslan sé efnislega bókuð í birgðir.
- Birgðafærslugildi sem er ekki innan sviga bendir til þess að birgðafærslan sé fjárhagslega bókuð í birgðir.
- Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
- Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur til kynna bókunarröð birgðafærslna á tímaásnum .
- Birgðalokun eru sýndar með rauðri lóðréttri punktaðri línu og merkinu *birgðalokun*
- Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

