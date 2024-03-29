---
title: Dreifing frá dreifingarstöð frá framleiðslupöntunum í úthlið
description: Þessi grein lýsir því hvernig á að stjórna ferlinu við að dreifa efni frá dreifingarstöð sem hefur verið tilkynnt sem lokið frá framleiðslulínu til flutningsstöðvar.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockOpportunityPolicy, WHSReservationHierarchy, WHSInventTableReservationHierarchy, WHSItemGroupLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea3ae6cb83d6577ba76d7e2aff9a05973b314cfe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849330"
---
# <a name="cross-docking-from-production-orders-to-outbound-docks"></a>Dreifing frá dreifingarstöð frá framleiðslupöntunum í úthlið

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að stjórna ferlinu við að dreifa efni frá dreifingarstöð sem hefur verið tilkynnt sem lokið frá framleiðslulínu til flutningsstöðvar.

## <a name="introduction"></a>Inngangur

Dreifing frá dreifingarstöð úr framleiðslu í úthliðsstaðsetningu á við um framleiðendur sem framleiða mikið magn og vilja helst senda lokaafurð um leið og hún er skráð sem fullunnin úr framleiðslulínum. Tilgangurinn er að senda afurðir til dreifingarstöðva sem eru staðsettar eftir óskum viðskiptavinar, frekar en að safna upp birgðum á framleiðslustöð.

Sé ekki tafarlaus eftirspurn eftir afurð, verður að setja hana í vöruhúsastaðsetningu á framleiðslustað. Þetta ferli er einnig nefnt *tækifærisdreifing frá dreifingarstöð*, sem segir að ef það er þörf á að senda afurðina, ætti að nota þetta tækifæri í stað þess að ganga frá vörunni í innri geymslu.

Eftirfarandi dæmi sýnir þrjú afbrigði af flæði sem byrjar í lok framleiðslulínu (2).

Afurð er tilkynnt sem lokið hjá staðsetningu framleiðslufrálags (3) og starfsmaður á lyftara mun sækja brettið á þessum stað (3).

-   Ef fyrirhuguð virkni er til staðar (6) til að flytja afurðina frá framleiðslu (1) til dreifingarstöðvar (7), þá mun kerfið segja vörubílstjóranum að setja brettið við útskotsstaðsetningu (4).
-   Ef eftirvagni hefur þegar verið úthlutuð staðsetningin, þá verður vörubílstjóranum sagt að hlaða afurðinni beint á eftirvagninn.
-   Ef ekki er fyrirhuguð aðgerð til að flytja afurðina verður starfsmaður lyftarans sagt að koma afurðinni fyrir á staðsetningu í innra vöruhúsi (5).

[![tækifærisdreifing frá dreifingarstöð.](./media/scenario1.png)](./media/scenario1.png)

## <a name="configure-cross-docking"></a>Skilgreining dreifingar frá dreifingarstöð
Dreifing frá dreifingarstöð er skilgreind í **vinnureglum**. Vinnuregla inniheldur verkbeiðnigerð, staðsetningu og afurð. Í eftirfarandi dæmi er dreifing frá dreifingarstöð skilgreind fyrir afurð X og staðsetningu Y.

#### <a name="work-order-types"></a>Gerðir vinnupöntunar

-   Verkbeiðnigerð: Ganga frá fullunnum vörum
-   Skráningaraðferð vinnu: Dreifing frá dreifingarstöð
-   Regluheiti dreifingar frá dreifingarstöð: Flutningspantanir

#### <a name="inventory-locations"></a>Birgðastaðsetningar

-   Vöruhús: 51
-   Staðsetning: Y

#### <a name="products"></a>Afurðir

-   Vörunúmer: X

Eins og stendur er aðeins hægt að skilgreina dreifingu frá dreifingarstöð fyrir tvær verkbeiðnigerðir:

-   Frágangur á fullunnum vörum
-   Frágangur aukaafurða og hliðarafurða

Í **reglu fyrir dreifingu frá dreifingarstöð** er hægt að skilgreina hvaða skjalagerðir eru viðeigandi fyrir dreifingu frá dreifingarstöð. Sem stendur er **Flutningspantanir** eina skjalagerðin sem er studd. Eftirfarandi dæmi sýnir skilgreiningu á reglu fyrir dreifingu frá dreifingarstöð.

### <a name="cross-docking-policy-name-transfer-order"></a>Regluheiti dreifingar frá dreifingarstöð: Flutningspöntun

- Raðnúmer: 10
  -   Gerð verkbeiðni: Flutningsútgáfa
- Eftirspurn eftir dreifingu frá dreifingarstöð þarfnast staðsetningar: Rangt
- Áætlun fyrir dreifingu frá dreifingarstöð: Dagsetning og tími

### <a name="sequence-number"></a>Raðnúmer

**Raðnúmerið** tilgreinir forgang skjalagerðarinnar. Sem stendur er **Flutningsútgáfa** eina gerðin sem er studd. Því mun raðnúmer aðeins eiga við þegar fleiri verkbeiðnigerðir verða studdar.

### <a name="cross-docking-policy"></a>Regla fyrir dreifingu frá dreifingarstöð

Stefna fyrir dreifingu frá dreifingarstöð segir til um stefnu fyrir forgangsröðun á flutningspantanakröfu. Til dæmis, ef margar flutningspantanir eru til fyrir sömu afurðina, ákvarðar áætluð dagsetning og tími sem er stilltur fyrir hleðsluna, og tengdur er við flutningspöntunina, forgangsröðun milli pantana. Hægt er að stilla áætlaða dagsetningu og tíma beint á hleðsluna, en einnig er hægt að stilla **verkröðun** sem er tengd við hleðsluna. Forgangsröðun ákvarðast af áætlun fyrir dreifingu frá dreifingarstöð. Sem stendur er aðeins ein áætlun: **Dagsetning og tími**.

### <a name="cross-docking-demand-requires-location"></a>Eftirspurn eftir dreifingu frá dreifingarstöð þarfnast staðsetningar.

Í reglu fyrir dreifingu frá dreifingarstöð er hægt að setja upp skilyrði sem krefjast þess að flutningspantanir hafi úthlutaða staðsetningu, svo þær séu gjaldgengar fyrir dreifingu frá dreifingarstöð. Þetta skilyrði er sett í reitnum **Eftirspurn eftir dreifingu frá dreifingarstöð þarfnast staðsetningar**. Staðsetning á verkröðun sem tengist hleðslunni er notuð sem lokastaðsetning fyrir vörurnar sem á að dreifa úr dreifingarstöð. Lokastaðsetning fyrir vörurnar sem á að dreifa úr dreifingarstöð ákvarðast af staðsetningarleiðbeiningum fyrir **Flutningsútgáfu** fyrir verkbeiðnigerðina **Frágangur**. Það gæti verið gagnlegt að stilla reitinn **Eftirspurn eftir dreifingu frá dreifingarstöð þarfnast staðsetningar** í aðstæðum þar sem fullunnum vörum ætti að vera dreift frá dreifingarstöð, aðeins ef tengivagn er settur á útkeyrsluhurð. Í slíku tilfelli eru vörur færðar beint frá framleiðslulínu í tengivagn. Þegar tengivagn er settur á útkeyrsluhurð, setur notandi staðsetninguna á viðeigandi verkröðun og gerir staðsetninguna því viðeigandi fyrir dreifingu frá vöruhúsi. Í eftirfarandi köflum er farið í gegnum tvö dæmi.

#### <a name="scenario-1--cross-docking-from-production-to-transfer-orders"></a>Dæmi 1 - Dreifing frá dreifingarstöð úr framleiðslu til flutningspantana

Þegar afurð er skráð sem fullunnin í framleiðslulínu er hún flutt að útkeyrsluhurð þar sem hún er sett í flutningabíl og flutt á dreifingarstöð. Nota USMF fyrirtækis.

1.  Virkja nýja númeraröð fyrir dreifingu frá dreifingarstöð. Farðu á síðuna **Númeraraðir** og veldu hnappinn **Mynda**. Leiðsagnarforrit leiðir þig í gegnum ferlið.
2.  Stofna stefnu fyrir dreifingu frá dreifingarstöð. Farðu á síðuna **Stefna fyrir dreifingu frá dreifingarstöð** og stofnaðu nýja stefnu sem heitir **Dreifing frá dreifingarstöð í flutningspöntun**. Athugaðu að eina verkbeiðnigerðin sem þú getur valið er **Flutningsútgáfa** og eina áætlunin fyrir dreifingu frá dreifingarstöð sem er í boði er **Dagsetning og tími**.
3.  Stofna vinnureglu. Farðu á síðuna **Vinnureglur** og stofnaðu nýja vinnureglu sem heitir **Dreifing frá dreifingarstöð L0101**.
4.  Settu upp hleðslur þannig að þær séu stofnaðar sjálfkrafa fyrir flutningspantanir. Í vöruhúsafæribreytum eru hleðslur stilltar þannig að þær séu stofnaðar sjálfkrafa þegar flutningspantanir eru stofnaðar. Hleðsla er forsenda þess að flutningspöntun sé gerð gjaldgeng fyrir dreifingu frá dreifingarstöð.
5.  Setja upp hleðsluvörpun vöru. Farðu á síðuna **Hleðsluvörpun vöru** og settu upp staðlað hleðslusniðmát fyrir vöruhópinn **CarAudio**. Þessi vörpun setur hleðslusniðmátið sjálfkrafa á hleðsluna þegar flutningspöntunin er stofnuð.
6.  Stofna flutningspöntun Búðu til flutningspöntun fyrir vörunúmer L0101. Magn = 20.
7.  Losaðu flutningspöntunina úr vinnusvæði hleðsluáætlunar. Veldu valmyndaratriðið fyrir vinnusvæði hleðsluáætlunar á flipanum **Senda** og á valmyndinni **Losun** í hleðslulínu skaltu velja **Losa í vörugeymslu**. Bylgjulína af gerðinni **Flutningsútgáfa** er nú til fyrir flutningspöntunina.
8.  Stofna framleiðslupöntun Farðu á listasíðuna **Framleiðslupöntun** og stofnaðu framleiðslupöntun fyrir afurð L0101. Magn = 20. Áætlaðu og settu framleiðslupöntunina í gang. Athugaðu að reiturinn **Bóka tiltektarlistann nú** er áfram stilltur á **Nei**.
9.  Skrá sem tilbúið úr fartæki. Farðu í gátt fartækisins og veldu valmyndaratriðið **Bóka sem tilbúið og ganga frá**. Skráðu nú sem fullunnið L0101 úr lófatækinu. Magn = 10. Athugaðu að frágangsstaðsetning er **BAYDOOR**. Þessa staðsetningu er hægt að finna í staðsetningarleiðbeiningunum **Flutningsútgáfa** fyrir verkbeiðnigerðina **Frágangur**. Athugaðu einnig að verk af gerðinni **Flutningsútgáfa** hefur verið stofnuð og lokið við. Farðu í upplýsingar um verk flutningspöntunar til að staðfesta verkið.
10. Tilkynntu nú um 10 stykki til viðbótar úr farsímanum. Athugaðu að frágangsstaðsetning aftur er **BAYDOOR**. Athugaðu einnig að nýtt verk af gerðinni **Flutningsútgáfa** hefur verið stofnað fyrir 10 stykki.
11. Reyndu nú að byrja með 20 stykkjum meira í framleiðslupöntuninni og reyndu síðan að tilkynna 20 ea sem búið með því að nota handbúnaðinn. Í þetta sinn er staðsetningin **LP 001** lögð til sem frágangsstaðsetning. Þessi staðsetning er fundin út frá staðsetningarleiðbeiningunum **Frágangur á fullunnum vörum**. Þessar staðsetningarleiðbeiningar eru notaðar vegna þess að ekkert tækifæri til dreifingar frá dreifingarstöð er til staðar. Flutningspöntunin fyrir LP-001 var algjörlega uppfyllt með tveimur dreifingaraðgerðum frá dreifingarstöð í 9. og 10. skrefi. Athugið að verk af gerðinni **Frágangur á fullunnum vörum** var stofnað og unnið.

#### <a name="scenario-2---cross-docking-from-production-to-transfer-orders-with-an-appointment-schedule"></a>Dæmi 2 - Dreifing frá dreifingarstöð frá framleiðslu í flutningspantanir með verkröðun.

Eftir að afurð hefur verið tilkynnt sem lokið við framleiðslulínuna er hún flutt á staðsetningu útskots, sem er auðkennt með tímabókun fyrir staðsetningar útskots. Nota USMF fyrirtækis.

1.  Breyta um stefnu fyrir dreifingu frá dreifingarstöð. Breyttu um stefnu fyrir dreifingu frá dreifingarstöð sem þú stofnaðir í dæmi 1 með því að velja gátreitinn **Eftirspurn eftir dreifingu frá dreifingarstöð þarfnast staðsetningar**.
2.  Stofna nýja flutningspöntun.
3.  Opnaðu **Vinnusvæði hleðsluáætlunar**.
4.  Úr vinnusvæði hleðsluáætlunar skaltu fara í hlutann **Hleðslur** og velja **Verkröðun** í valmyndinni **Flutningur** til að stofna nýja verkröðun. Athugaðu að verkröðun hefur tilvísun í flutningspöntunina í reitnum **Pöntunarnúmer**. Í reitnum **Áætluð upphafsdagsetning/tími staðsetningar** er hægt að stilla dagsetningu og verkröðun. Þessi dagsetning og tími verða svo notuð þegar eftirspurn um dreifingu frá dreifingarstöð er forgangsraðað í dreifingarstöðvarferlinu. Sú dagsetning og tími sem þú setur í þennan reit mun uppfæra reitinn **Áætluð dagsetning og tími á sendingu hleðslu** fyrir samsvarandi hleðslu. Staðsetningin á flýtiflipanum **Sendingarupplýsingar** ákvarðar staðsetninguna sem flutningspöntunin er send frá.
5.  Losaðu á vöruhúsið á **Vinnusvæði hleðsluáætlunar**.
6.  Búðu til framleiðslupöntun fyrir vörunúmer **L0101** og stilltu stöðuna á **Hafið** með magn upp á 20.
7.  Skrá sem tilbúið úr fartæki.
8.  Farðu í gátt fartækisins og veldu valmyndaratriðið **Bóka sem tilbúið og ganga frá**.
9.  Skráðu vörunúmerið **L0101** sem fullunnið úr lófatækinu. Athugaðu að frágangsstaðsetning er nú **BAYDOOR 2**. Þessa staðsetningu er hægt að finna frá verkröðuninni í stað staðsetningarleiðbeininganna **Flutningsinnhreyfing**.

### <a name="additional-information"></a>Viðbótarupplýsingar

-   Dæmið um dreifingu úr dreifingarstöð er stutt fyrir rað- og runuvinnslu, þar sem bæði víddir fyrir runu- og raðnúmer eru skilgreindar með staðsetningum fyrir ofan og neðan í frátektarstigveldi. 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]