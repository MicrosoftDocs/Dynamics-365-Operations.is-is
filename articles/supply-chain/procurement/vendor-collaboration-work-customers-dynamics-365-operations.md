---
title: Samstarf lánardrottna með viðskiptavinum
description: Í þessu efnisatriði er því lýst hvernig hægt er að nota samstarf lánardrottna til að vinna með innkaupapantanir og fylgjast með vörusendingabirgðum.
author: TaylorVH
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart, VendVendorProfileCard, PurchVendorPortalAllResponse, PurchVendorPortalPendingResponsesPart, PurchVendorPortalResponses, PurchVendorPortalConfirmedOpenOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: v-savanh
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 024bbaad45f320b8c82b20a52ced05322371e337
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575388"
---
# <a name="vendor-collaboration-with-customers"></a>Samstarf lánardrottna með viðskiptavinum

[!include [banner](../includes/banner.md)]

Þessi mál lýsir því hvernig hægt er að nota samstarf lánardrottna við viðskiptavini í Microsoft Dynamics 365 Supply Chain Management. Söluaðilar geta lokið röð viðskiptaferla úr eftirfarandi vinnusvæðum:

- **Innkaupapöntunum svarað** - Fylgjast með og bregðast við innkaupapöntunum.
- **Lánardrottinn tilboð** - Skoða beiðnir um tilboð (BUT) og svara þeim með því að færa inn tilboð.
- **Lánardrottnaupplýsingar** - Skoða og uppfæra lánardrottinssniðmát.
- **Invoicing** - Vinna með reikninga. Þetta efnisatriði nær ekki yfir vinnusvæðið **Invoicing**. Nánari upplýsingar um þetta vinnusvæði er að finna í [Vinnusvæði reikningsfærslur fyrir samstarf lánardrottna](../../finance/accounts-payable/vendor-portal-invoicing-workspace.md).

Lánardrottnar geta líka fylgst með upplýsingum um vörusendingarbirgðir.

## <a name="working-with-pos-in-the-purchase-order-confirmation-workspace"></a>Vinna með innkaupapantanir á vinnusvæði staðfestingar á innkaupapöntun

Í **Staðfesting á innkaupapöntun** vinnusvæði gerir þér kleift að svara innkaupapöntunum sem hafa verið sendar til þín til skoðunar. Það gerir einnig kleift að skoða upplýsingar um innkaupapantanir sem bíða eftir aðgerð frá viðskiptavininum og innkaupapantanir sem hafa verið staðfestar en eru enn opnar.

Það eru þrjár listum í **staðfesting á Innkaupapöntun** vinnusvæðis:

- **Innkaupapantanir fyrir yfirferð** -listinn sýnir innkaupapantanir sem hafa verið send að og bíða svars frá þér. Eftir að þú svarar, hverfur Innkaupapöntunin af listanum. Ef viðskiptavinurinn sendir þér ný útgáfa af innkaupapöntuninni áður en þú hefur getað svarað fyrri útgáfunni, birtist aðeins nýjustu útgáfuna.
- **Beðið eftir aðgerð viðskiptavinar** - Þessi listi sýnir allar innkaupapantanir sem þú hefur svarað en viðskiptavinur hefur enn ekki staðfest. Ef Innkaupapöntunin er samþykkt af þér, er hægt að fylgjast með henni í þessum lista þar til staðan breytist í **Staðfest**. Ef Innkaupapöntunin er hafnað eða samþykkt með breytingar, er hægt fylgjast með Innkaupapöntun hér þar til viðskiptavinar sendir nýja útgáfu.
- **Opna Staðfestar innkaupapöntunum** - Listinn inniheldur allar innkaupapantanir fyrir þinn reikninginn sem hafa stöðuna **Staðfest**. Þegar afurðir eða þjónustur eru móttekið að fullu gagnvart Innkaupapöntunin, hverfur Innkaupapöntunin úr listanum.

Hægt er að nota eftirfarandi síður til að vinna með innkaupapantanir:

- **Innkaupapantanir til að fara yfir** - Þessi síða inniheldur sömu upplýsingar og **Innkaupapantanir til að fara yfir** listinn á vinnusvæðinu. Sjá lýsinguna fyrr í þessari efnisatriði.
- **Staðfestingarsögu lánardrottins fyrir innkaupapantanir** -Þessi síða inniheldur allar innkaupapantanir og útgáfur innkaupapantana sem hafa verið sendar til lánardrottins. Hún inniheldur einnig öll svör sem hafa borist frá lánardrottni.
- **Opnar staðfestar innkaupapantanir** - Þessi síða inniheldur sömu upplýsingar og **Opnar staðfestar innkaupapantanir** listinn á vinnusvæðinu. Sjá lýsinguna fyrr í þessari efnisatriði.
- **Allar staðfestar innkaupapantanir** - Þessi síða inniheldur allar innkaupapantanir sem hafa verið staðfestar. Á meðal innkaupapantana sem birtast á þessari síðu eru allar innkaupapantanir þar sem vörur eða þjónustu hafa verið mótteknar. Hægt er að nota þennan lista til að fylgjast með þeim innkaupöntunum sem er hægt að senda reikninga fyrir.

### <a name="responding-to-pos"></a>Svara innkaupapöntunum

Innkaupapantanir sem viðskiptavinurinn hefur sent þér til að fara yfir eru sýnilegir í **staðfesting á Innkaupapöntun** vinnusvæði og á **Innkaupapantanir fyrir yfirferð** síðuna. Eftir Innkaupapöntun er opnuð er hægt að samþykkja hana, hafna henni eða samþykkja hana með breytingum. Það gætu verið viðhengi á haus Innkaupapöntunar eða á einstakra lína. Líka er hægt að hengja upplýsingar við svar þínu á einstakar línur eða haus Innkaupapöntunar. Til dæmis gætu lagt til staðgengilsvöru fyrir ein línanna.

Forskoðun og prenta Innkaupapöntunina er mögulegt sem pdf-skrá með því að nota **Prenta /Forskoðun** valkostur. Það er líka hægt að nota **Birta víddir** aðgerðina til að fela eða sýna eftirfarandi víddardálka: **Svæði**, **Vöruhús**, **Litur**, **Stærð**, **Stíll**, og **Skilgreining**. 

Ef nota á **Samþykkja með breytingum** valkost er hægt að samþykkja eða hafna einstakar línur. Einnig er hægt að gera breytingar á eftirfarandi línum:

- Breyta dagsetningum eða magn. Til að uppfæra staðfestrar afhendingardagsetningar á öllum línum skal nota **Uppfæra afhendingardagsetningu** valkost á haus Innkaupapöntunar.
- Skipta línum fyrir mismunandi afhendingardagsetningar eða magn.
- Nota staðgengilsvöru. Í hlutanum **Línuupplýsingar** skal slá inn vörulýsingu og vörunúmer í reitinn **Ytri**.

Ekki er hægt að breyta verðupplýsingar eða gjöld, en hægt að gera tillögur um breytingar með því að nota athugasemdir.

Ef viðskiptavinur sendir þér nýja útgáfu af innkaupapöntun mun hún vera með útgáfuviðskeyti til að gefa til kynna að það sé breytt útgáfa af innkaupapöntun sem var áður send. Í **staðfestingarsögu innkaupapantana lánardrottins** síðu getur þú rekja sögu hverja pöntun.

## <a name="monitoring-consignment-inventory"></a>Fylgjast með vörusendingabirgðir

Ef verið er að nota vörusendingabirgðir, geta þú notað viðmót fyrir samstarf lánardrottna til að skoða upplýsingar um eftirfarandi síður:

- **Innkaupapantanir sem notar vörusendingabirgðir** - innkaupapantanir fyrir vörusendingabirgðir eru myndaðar þegar viðskiptavinur tekur yfir eignarhald á birgðum. Þessum innkaupapantanir vörusendinga birtast aðeins á þessari síðu. Þær eru ekki teknar með á **Allar staðfestar innkaupapantanir** síðuna.
- **Afurðir sem er tekið við úr vörusendingabirgðum** - Þessi síða inniheldur lista yfir allar færslur þar sem eignarhald afurða hefur verið flutt til fyrirtækis sem er að nota birgðirnar. Þú geta nota þessar upplýsingar til að reikningsfæra á viðskiptavininn.
- **Vörusendingarbirgðir á lager** - Þessi síða sýnir vörusendingarbirgðir á lager í eigu fyrirtækis þíns en er á lager í vöruhúsi viðskiptavinar.

## <a name="working-with-rfqs-in-the-vendor-bidding-workspace"></a>Vinna með Beiðnir um tilboð á vinnusvæði fyrir Lánardrottnatilboð

**Lánardrottnatilboð** vinnusvæðið gerir þér kleift að skoða beiðnir um tilboð sem fyrirtæki þínu hefur verið boðið að svara. Einnig er hægt að svara Beiðnum um tilboð. 

Vinnusvæðið sýnir líka allar Beiðnir um tilboð sem þú hefur tapað eða unnið. Að auki, ef kerfið er grunnstillt fyrir hið opinbera, sýnir vinnusvæðið þær Beiðnir um tilboð sem eru opinber.

### <a name="viewing-rfqs"></a>Beiðnir um tilboð skoðaðar

Opna vinnusvæðið **lánardrottnatilboð** til að fá aðgang að eftirfarandi upplýsingum:

- Velja **Nýtt boð um kauptilboð** til að skoða Beiðnir um tilboð sem fyrirtæki þínu hefur verið boðið að svara. Héðan geturðu skoðað Beiðni um tilboð og hafið tilboðsferlið. Þú getur einnig séð lagfærðar Beiðnir um tilboð sem senda þarf inn nýtt kauptilboð fyrir.
- Velja **Kauptilboð sem hefur verið skilað** til að sjá Beiðnir um tilboð sem viðskiptamaðurinn hefur skilað til þín, svo þú getir boðið fram frekari upplýsingar til að uppfæra kauptilboðið.
- Velja **Kauptilboð í vinnslu** til að sjá Beiðnir um tilboð sem þú eða tengiliður fyrirtækis þíns hefur verið að vinna að, en ekki er búið að senda inn.
- Velja **Veitt kauptilboð** til að sjá hvenær viðskiptamaður hefur veitt a.m.k. einu línuatriði til þíns kauptilboðs.
- Velja **Töpuð kauptilboð** til að sjá kauptilboð þar sem öllum línum hefur verið hafnað.
- Velja **Beiðnir um tilboð** hlekkinn til að sjá lista yfir öll boð um lánardrottnabeiðnir og öll kauptilboð sem hafa verið send inn. **Beiðni um tilboð** síðan sýnir allar Tilboðsbeiðnir sem lánardrottinn hefur verið viðriðinn. Þú getur leita út frá stöðu.
- Velja **Kauptilboð sem hefur verið hafnað** hlekkinn til að sjá lista yfir allar Tilboðsbeiðnir þar sem tengiliður lánardrottins hefur hafnað því að gera kauptilboð.

### <a name="working-with-rfqs-that-are-publicly-available"></a>Vinna með opinberar tilboðsbeiðnir

Fólk sem vinnur hjá hinu opinbera getur séð opnar og útrunnar Tilboðsbeiðnir sem hafa verið gerðar opinberar.

- Velja **Opnar opinberar tilboðsbeiðnir** hlekkur til að sjá lista yfir opnar beiðnir um tilboð sem eru opinberar. Opin tilboðsbeiðni er óútrunnin tilboðsbeiðni. Á haus tilboðsbeiðninnar er að finna dag- og tímasetningu gildisloka.

    Ef þér hefur verið boðið að gera kauptilboð, geturðu fundið sömu tilboðsbeiðnina á **Boð um að gera nýtt kauptilboð** síðunni. Stundum gætirðu viljað gera kauptilboð í opna tilboðsbeiðni, en ekki hefur verið boðið að gera kauptilboð. Í slíku tilfelli er hugsanlegt að þú getir boðið sjálfum þér, að því gefnu að viðskiptamaður hafi virkjað sjálfsboð fyrir tilboðsbeiðnitilfellið.

    Aukið aðgengi **Opna útgefnar tilboðsbeiðnir** tengilsins með því að kveikja á eiginleikanum **Sýna tengilinn „Opna birtar tilboðsbeiðnir“ sem reit**. Þessi eiginleiki breytir tengli í reit og flytur hann á áberandi stað, þannig að auðvelt sé að finna hann.

- Velja **Lokaðar opinberar tilboðsbeiðnir** hlekkur til að sjá lista yfir lokaðar beiðnir um tilboð sem eru opinberar. Lokuð tilboðsbeiðni er útrunnin tilboðsbeiðni. Á haus tilboðsbeiðninnar er að finna dag- og tímasetningu gildisloka.

    Lokuð tilboðsbeiðni sýnir öll kauptilboð lánardrottna niður á línustig. Upplýsingar í lokuðum tilboðsbeiðnum endurspegla það þegar kauptilboðum er úthlutað eða þeim hafnað. Öll viðhengi sem eru höfð með í kauptilboðinu eru líka tiltæk.

> [!NOTE]
> Þessi virkni er aðeins í boði ef kveikt er á grunnstillingu fyrir hið opinbera.

### <a name="bidding"></a>Tilboð

- Veljið **Kauptilboð** til að byrja að gera kauptilboð í beiðni um tilboð.

    Þegar opnað er fyrir möguleikann á breytingum í kauptilboðsreitunum á haus og línu tilboðsbeiðni, geturðu fært inn kauptilboð þitt beint í hnitanetið. Þú þarft einnig að gæta að öllum upplýsingar um viðbótarkauptilboð sem skal bæta inn í línuupplýsingarnar.

    Þegar þú byrjar að vinna að kauptilboði, birtist það í **Kauptilboð í vinnslu** hlutanum.

    Hvenær sem er á undan lokadagsetningunni, geturðu vistað kauptilboð. Þú getur síðan komið aftur síðar til að klára og senda inn kauptilboðið. Eftir að þú hefur sent inn kauptilboð, geturðu kallað það fram aftur og uppfært það, alveg upp að lokadagsetningu.

- Velja **Endurstilla frá tilboðsbeiðni** til að endurstilla gögnin sem þú færðir inn fyrir kauptilboð og snúa aftur til upphaflegrar tilboðsbeiðni. Þú getur endurstillt hausinn eða línuna.
- Velja **Bæta við staðgengli** eða **Fjarlægja staðgengil** í hnitanetinu til að vinna með staðgengla.

    Sumar tilboðsbeiðnir leyfa staðgenglakauptilboð. Þú getur tilgreint staðgenglakauptilboð aðeins fyrir línur af **Tegund** flokknum, vegna þess að ekki er hægt að bæta tilgreindum atriðum við sem staðgenglum. 

- Velja **Viðhengi tilboðsbeiðni** eða **Línuviðhengi tilboðsbeiðni** til að opna öll viðhengi sem viðskiptamaður hefur bætt við tilboðsbeiðni. Til að hlaða upp viðhengjum um leið og kauptilboði skaltu velja **Tilboðsviðhengi** eða **Tilboðslínuviðhengi**.

    Þú gætir hugsanlega þurft að svara spurningalistum áður en þér er gefið leyfi til að senda inn kauptilboð.

- Velja **Hafna** ef þú vilt ekki gera kauptilboð. Eftir að þú velur **Hafna**, er ekki hægt að kalla aðgerðina aftur fram og færa inn kauptilboð.

Ef tilboðsbeiðni er lagfærð, verður þú að færa inn nýtt kauptilboð. Þú getur fundið upplýsingar um lagfæringuna á **Lagfæringar** flipanum á tilboðsbeiðnisíðunni. Lagfærðar tilboðsbeiðnir birtast á **Boð um ný kauptilboð** síðunni.

## <a name="accessing-vendor-master-data-in-the-vendor-information-workspace"></a>Fá aðgang að lánardrottinssniðmáti á vinnusvæði fyrir upplýsingar um lánardrottinn

Sem lánardrottinn, geturðu fengið aðgang að hluta upplýsinganna sem viðskiptamaðurinn er að vinna með í aðalskrá lánardrottins. Þar af leiðandi geturðu haldið upplýsingunum nýjum. Til að uppfæra upplýsingarnar verður þú að hafa (ytri) hlutverk kerfisstjóra lánardrottins.

Aðgengilegu upplýsingarnar eru nafn lánardrottins, aðsetur, tengslaupplýsingar, tengiliðir og þeirra tengslaupplýsingar, auðkennisnúmer, skattskráningarnúmer, innkaupaflokkar sem lánardrottinn er samþykktur til að selja til viðskiptamanns í, og upplýsingar um vottanir.

## <a name="additional-resources"></a>Frekari upplýsingar

[Stjórnun notenda samstarfs lánardrottna](manage-vendor-collaboration-users.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]