---
title: Losa í vöruhús
description: Þessi grein veitir upplýsingar um losun í vöruhúsaferli. Það lýsir einingum sem eru búnar til þegar þú sendir pöntun í vöruhúsið og valkostum sem hægt er að nota til að hefja ferlið.
author: Mirzaab
ms.date: 8/13/2021
ms.topic: article
ms.search.form: WHSReleaseToWarehouse, WHSReleaseToWarehouseSalesOrder, WHSReleaseToWarehouseTransferOrder, WHSLoadPlanningWorkbench, WHSWaveTemplateTable, WHSWorkTemplateTable, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: caa38c4ed1c7fb8cf1ead3ba6534f8405a5ff57f
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428037"
---
# <a name="release-to-warehouse"></a>Losa í vöruhús

[!include [banner](../../includes/banner.md)]

Þessi grein veitir upplýsingar um losun í vöruhúsaferli. Það lýsir einingum sem eru búnar til þegar þú sendir pöntun í vöruhúsið og valkostum sem hægt er að nota til að hefja ferlið.

## <a name="release-to-warehouse-overview"></a>Yfirlit yfir losun í vöruhús

Losun í vöruhús er ferlið við að gera birgðir tilbúnar fyrir úrvinnslu sendingar. Þegar þú losar pöntun í vöruhúsið býr kerfið til hleðslulínur og sendingar. Ef sjálfvirk bylgjuvinnsla er sett upp eru hleðslur og nauðsynleg vinna líka stofnuð. Það fer eftir kerfisstillingum hver skilgreiningin er á einingunum. Í þessum hluta greinarinnar er farið yfir einingarnar sem eru stofnaðar við losun í vöruhúsaferlið og kerfisstillingarnar sem skilgreina þær.

*Sending* er hópur af sölupöntunar- eða flutningspöntunarlínum fyrir sama viðskiptavininn eða sama afhendingaraðsetrið.

*Hleðsla* er hópur af sölupöntunar- eða flutningspöntunarlínum sem eru flokkaðar saman og fara yfirleitt út í einum vörubíl, lestarvagni eða öðrum flutningsmáta. Hleðsla getur haft eina eða margar sendingar. Hægt er að stofna hleðslu handvirkt með því að bæta pöntunarlínum við nýja hleðslu. Í þessu tilviki er pöntunarlínum úthlutað til hleðslunnar áður en losunarferlið í vöruhúsið er sett í gang og aðeins er hægt að losa þær af síðunni **Vinnusvæði hleðsluáætlunar**.

*Vinna* vöruhúss er allar vöruhúsaaðgerðir sem starfsmaður í vöruhúsi framkvæmir. Yfirleitt samanstanda vinnsluaðgerðir vöruhúss af tveimur samhangandi aðgerðum: starfsmaður í vöruhúsi tekur til lagerbirgðir á einni staðsetningu og setur þær síðan á aðra staðsetningu.

Þegar pantanir eru losaðar í vöruhúsið býr kerfið til *hleðslulínur* og flokkar þær niður í sendingar. Sameiningarferli sendingar leyfir sjálfvirka sameiningu sendingar meðan á losunarferlinu stendur til vöruhússins. Frekari upplýsingar er að finna í [Yfirlit yfir samstæðureglur sendingar](about-shipment-consolidation-policies.md).

Kerfið notar *bylgjur* til að búa til tiltektarvinnu og hleðslur fyrir sendingu. *Bylgjusniðmát* verður að vera tiltækt fyrir gerð bylgju sem á að stofna og fyrir vöruhús pöntunarlínunnar. Bylgjusniðmát af gerðinni *Sending* eru notuð til að senda vörur fyrir sölupantanir og flutningspantanir.

Hvert bylgjusniðmát inniheldur *bylgjuaðferðir*. Bylgjuaðferðir framkvæma aðgerðir, s.s. að stofna vinnu fyrir bylgjuna eða stofna hleðslur. Til dæmis getur bylgjusniðmát fyrir sendingarbylgjur innihaldið aðferðir til að búa til hleðslur, úthluta línum á bylgjur, fylla á og stofna tiltekt fyrir bylgjuna. Bylgjusniðmátið setur á stillingar sem skilgreina hvernig bylgjan verður búin til og unnið úr henni, hvaða skref þarf að gera handvirkt og hver þeirra þarf að gera sjálfkrafa. Frekari upplýsingar er að finna í [Bylgjusniðmát](wave-templates.md). Það fer því eftir uppsetningu bylgjusniðmátsins hvort bylgja sé búin til sjálfkrafa, unnið úr henni og losuð þegar þú losar pöntun í vöruhús, eða sumar eða allar þessar aðgerðir eru framkvæmdar handvirkt eftir að losun í vöruhúsið lýkur.

Þegar unnið er úr bylgju stofnar kerfið tiltektarvinnu sem byggir á hentugu *sniðmáti* og *staðsetningarleiðbeiningu* og gerir þá vinnu aðgengilega í fartækjum. Vinnusniðmátið ákvarðar hvernig vinnan er framkvæmd fyrir hvert vöruhúsaferli og staðsetningarleiðbeiningin tilgreinir tiltektar- og frágangsstaðsetningarnar fyrir birgðahreyfingu. Frekari upplýsingar er að finna í [Stýra vöruhúsavinnu með vinnusniðmátum og staðsetningarleiðbeiningum](control-warehouse-location-directives.md).

> [!NOTE]
> Sjálfgefið er að bylgjur séu unnar í runustillingu.

Við bylgjuvinnslu býr kerfið venjulega til nýjan farm fyrir hverja sendingu þar sem engum farmi hefur verið úthlutað. Ef þú vilt að kerfið úthluti óúthlutuðum sendingum til núverandi hleðslu í staðinn, getur þú notað virkni ítarlegrar hleðsluáætlunar bylgju. Frekari upplýsingar er að finna í [Viðbótarhleðsluáætlanir í bylgju](advanced-load-building-during-wave.md).

Á síðunum **Sölupantanir** og **Flutningspantanir** er hægt að fara yfir einingarnar sem eru búnir til fyrir pöntunarlínur í losunarferli vöruhúss.

- Síðan **Sölupantanir**:

    - Í flýtiflipanum **Sölupöntunarlínur** skal velja **Vöruhús** og svo í valmyndinni skal velja **Upplýsingar sendingar** til að opna viðeigandi sendingar, **Upplýsingar um hleðslu** til að opna viðeigandi hleðslur eða **Upplýsingar um verk** til að opna upplýsingar um viðeigandi verk.
    - Í flýtiflipanum **Línuupplýsingar** skal velja flipann **Hleðsla** til að yfirfara tengdar hleðslur.

- Síðan **Flutningspantanir**:

    - Á aðgerðasvæðinu, í flipanum **Senda**, skal velja **Upplýsingar sendingar** til að opna viðeigandi sendingar eða **Upplýsingar um hleðslu** til að opna viðeigandi hleðslur.
    - Í flýtiflipanum **Flutningspöntunarlínur** skal velja **Upplýsingar um verk** til að opna viðeigandi upplýsingar um verk.

Af því leiðir að þegar pöntun er losuð í vöruhúsið, virkar mest sjálfvirka flæðið á eftirfarandi hátt:

1. Kerfið býr til sendingu fyrir pöntunina og bylgju.
1. Unnið er úr bylgjunni.
1. Kerfið býr til álag og vinnukenni.

Það fer eftir bylgjusniðmátum, vinnusniðmátum og stillingum fyrir staðsetningarleiðbeiningar hvort sum skrefin í þessu flæði verða handvirk. Heildarflæðið helst þó óbreytt.

Þú hefur nokkra valkosti um hvernig þú losar pöntun í vöruhúsið. Hægt er að framkvæma aðgerðina handvirkt eða setja upp runuvinnslu. Farið er ítarlega yfir þá hluta þessarar greinar sem eftir eru, ýmsar leiðir til að framkvæma losunaraðgerð í vöruhús.

## <a name="manual-release-to-the-warehouse-from-the-sales-orders-and-transfer-orders-pages"></a>Handvirk losun í vöruhúsið af sölupöntunar- og flutningspöntunarsíðum

Hægt er að losa pöntun í vöruhúsið beint af síðunni **Sölupantanir** eða síðunni **Flutningspantanir** með því að velja **Losa í vöruhús**.

- Á síðunni **Sölupantanir** er hnappurinn í flipanum **Vöruhús** á aðgerðasvæðinu.
- Á síðunni **Flutningspantanir** er hnappurinn í flipanum **Senda** á aðgerðasvæðinu.

Á síðunni **Sölupantanir** getur þú losað nokkrar sölupantanir í einu.

## <a name="manual-release-to-the-warehouse-from-the-release-to-warehouse-pages"></a>Handvirk losun í vöruhúsið af síðunum Losa í vöruhús

Kerfið býður núna upp þrjár síður þar sem hægt er að fara yfir línur fyrir margar pantanir og losa þær í vöruhúsið:

- **Losa í vöruhús** (**Vöruhúsakerfi \> Losa í vöruhús \> Losa í vöruhús**) – Þessi síða gerir þér kleift að vinna með bæði sölupantanir og flutningspantanir. Afköst hennar eru þó minni en á hinum tveimur síðunum. Þessi síða verður fljótlega úrelt.
- **Losa sölupantanir í vöruhús** (**Vöruhúsakerfi \> Losa í vöruhús \> Losa sölupantanir í vöruhús**) – Þessi síða gerir þér aðeins kleift að vinna með sölupantanir. Hins vegar eru afköstin betri en á síðunni **Losa í vöruhús**.
- **Losa flutningspantanir í vöruhús** (**Vöruhúsakerfi \> Losa í vöruhús \> Losa flutningspantanir í vöruhús**) – Þessi síða gerir þér aðeins kleift að vinna með flutningspantanir. Hins vegar eru afköstin betri en á síðunni **Losa í vöruhús**.

Allar þrjár síðurnar bjóða upp á svipaða virkni, eins og lýst er í það sem eftir er af þessum hluta. Allar leyfa þér að velja pöntunarlínur eða heilar pantanir og síðan losa þær í vöruhúsið.

Hver síða samanstendur af efri hluta þar sem hægt er að velja pöntunarlínur og neðri hluta þar sem hægt er að hefja losunarferli vöruhúss. Hægt er að nota síur í efri hlutanum til að leita að sölupöntunarlínunum sem á að losa. Á síðunni **Losa í vöruhús** er sérstakur flipi fyrir sölupantanir og flutningspantanir í efri hlutanum, en hinar tvær síðurnar sýna aðeins eina tegund pöntunar.

Tækjastikan í efri hlutanum inniheldur eftirfarandi hnappa sem hægt er að nota til að velja pöntunarlínur til að losa í vöruhúsið:

- **Bæta við** – Veldu eina eða fleiri pöntunarlínur í efri hlutanum og veldu svo þennan hnapp til að færa línurnar í neðri hlutann.
- **Bæta við öllum** – Bæta öllum línum úr efri hlutanum í neðri hlutann.
- **Bæta við pöntun** – Veldu pöntun og veldu svo þennan hnapp til að bæta öllum línum úr þeirri pöntun við neðri hlutann.

Þegar þú hefur lokið við að bæta línum við neðri hlutann skaltu merkja hverja línu sem á að losa. Síðan velur þú **Losaí vöruhús** á tækjastikunni til að losa þessar línur í vöruhúsið.

## <a name="manual-release-to-the-warehouse-from-the-load-planning-workbench-page"></a>Handvirk losun í vöruhúsið af síðu vinnusvæðis fyrir hleðsluáætlun

Einnig er hægt að losa pantanir í vöruhúsið handvirkt með því að nota síðuna **Vinnusvæði hleðsluáætlunar**. Á þessari síðu er hægt að raða pöntunarlínum í hleðslur og losa síðan þessar hleðslur í vöruhúsið.

Til að opna síðuna **Vinnusvæði hleðsluáætlunar** skal fara í **Vöruhúsakerfi \> Hleðslur**. Einnig er hægt að opna það af síðunum **Sölupantanir** og **Flutningspantanir**. Í efri hluta síðunnar er hægt að velja sölupöntunarlínur í flipanum **Sölulínur** og flutningspöntunarlínur í flipanum **Flutningslínur** og bæta svo línunum við nýja eða núverandi hleðslu.

Flipinn **Framboð og eftirspurn** á aðgerðasvæðinu inniheldur eftirfarandi hnappa sem þú getur notað til að bæta pöntunarlínum í efri hlutanum við hleðslu:

- **Í nýja hleðslu** – Veldu pöntunarlínur í efri hlutanum og veldu svo þennan hnapp til að búa til nýja hleðslu og bættu þessum línum við hana.
- **Í fyrirliggjandi hleðslu** – Veldu pöntunarlínur í efri hlutanum og veldu svo þennan hnapp til að bæta þessum línum við fyrirliggjandi hleðslu.
- **Öll pöntun í nýja hleðslu** – Veldu pantanir og veldu svo þennan hnapp til að búa til nýja hleðslu og bættu öllum línum úr þessum pöntunum við hana.
- **Öll pöntun í fyrirliggjandi hleðslu** – Veldu pöntun og veldu svo þennan hnapp til að bæta öllum línum úr þeirri pöntun við fyrirliggjandi hleðslu.

Í neðri hlutanum er hægt að fara yfir hleðslurnar sem eru búnar til. Til að losa hleðslur í vöruhúsið skal velja þær og velja síðan **Losa \> Losa í vöruhús** á tækjastikunni. Ef þú ert að nota sjálfvirka bylgjuvinnslu vegna þess að búið er að úthluta hleðslum til pöntunarlína býr kerfið til sendingar og vinnukenni þegar losunaraðgerð vöruhúss er framkvæmd.

## <a name="automatic-release-to-the-warehouse"></a>Sjálfvirk losun í vöruhúsið

Til að losa sjálfkrafa pantanir í vöruhúsið skal nota verkin **Sjálfvirk losun á sölupöntunum** og **Sjálfvirk losun á flutningspöntunum**.

Til að setja upp runuvinnslu sem losar sölupantanir skal fylgja þessum skrefum.

1. Farið í **Vöruhúsakerfi \> Losa í vöruhús \> Sjálfvirk losun sölupantana**.
1. Í svarglugganum **Sjálfvirk losun á sölupöntunum**, í flýtiflipanum **Færibreytur**, skal stilla eftirfarandi reiti:

    - **Magn sem á að losa** – Veldu hvort eigi að losa allt magnið eða aðeins efnislega frátekið magn í vöruhúsið.
    - **Leyfa losun pantana sem hafa verið losaðar að hluta** – Tilgreindu hvort eftirstandandi magn fyrir pantanir sem hafa verið losaðar að hluta til eigi að vera losaðar í vöruhúsið.
    - **Halda frátekningum á losun sem mistekst** – Tilgreindu hvort magn sem var sjálfkrafa tekið frá fyrir sölupöntun eigi að vera áfram frátekið ef losunarferlið í vöruhúsið mistekst.
    - **Flokka losanir eftir viðskiptavini** – Tilgreinið hvort kerfið eigi að vinna birgðasendingar í vöruhúsarekstur sérstaklega fyrir hvern viðskiptavin eða gefa út allar sölupantanir á sama tíma. Þegar þessi valkostur er stilltur á *Já* mun kerfið safna öllum sölupöntunarlínum fyrir valinn viðskiptavin, losa þessar pantanir í vöruhúsið og síðan afgreiða næsta viðskiptavin. Þegar þessi valkostur er stilltur á *Nei* mun kerfið losa allar tiltækar sölupöntunarlínur í einni losun í vöruhúsaaðgerð. Með því að virkja þennan valkost getur þú hjálpað til við að bæta árangur og viðnámsþrótt losunarinnar í vöruhúsaferlinu. Hins vegar verður þú að fara varlega þegar þú notar þennan valkost með bylgjusniðmátum sem eru skilgreind til að vinna úr bylgjum við losun í vöruhús því að þessi samsetning gæti búið til margar bylgjur fyrir stakan viðskiptavin, sem hver fyrir sig er með vinnu sem hefur verið búin til eingöngu fyrir þann viðskiptavin. Ef þú vilt búa til vinnu sem sameinar sendingar fyrir marga viðskiptavini ættir þú annaðhvort að slökkva á valkostinum *Flokka losanir eftir viðskiptavini* eða stilla bylgjusniðmátin til að nota frestaðar vinnslur.
    - **Meðhöndlun læstra pantana** – Veldu hvernig kerfið á að meðhöndla sölupantanir sem eru læstar vegna þess að aðrir notendur eða ferlar eru að breyta þeim:

        - *Bíða eftir því að pantanir fari úr lás* – Kerfið ætti að bíða eftir að pantanirnar verði teknar úr lás áður en það losar þær í vöruhúsið. Í því tilviki gæti losunarferli í vöruhús tekið lengri tíma.
        - *Sleppa læstum pöntunum* – Kerfið á að sleppa læstum pöntunum.

    - **Gildar gerðir pantana** – Veldu gerðir sölupantana til að hafa með í rununni.
    - **Gerð lánamarks** – Veldu hvort athuganir á lánamarki eigi að fara fram meðan losunarferli í vöruhús stendur yfir og, ef gera á athuganir, færsluupplýsingarnar sem eiga að fylgja þeim.

1. Til að stýra því hvaða pantanir eigi að vinna úr skal í flýtiflipanum **Færslur til að taka með** velja **Sía**. Hefðbundin svargluggi fyrirspurnar birtist þar sem hægt er að skilgreina valskilyrði, röðunarskilyrði og tengingar. Reitirnir virka á sama hátt og fyrir aðrar gerðir fyrirspurna í Microsoft Dynamics 365 Supply Chain Management.
1. Í flýtiflipanum **Keyra í bakgrunni** skal velja hvort vinnslan keyri í runustillingu og/eða setja upp endurtekna áætlun. Reitirnir virka rétt eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management.
1. Veldu **Í lagi** til að virkja stillingarnar þínar og hefja losunarferli í vöruhús.

Til að setja upp runuvinnslu sem losar flutningspantanir skal fylgja þessum skrefum.

1. Farið í **Vöruhúsakerfi \> Losa í vöruhús \> Sjálfvirk losun sölupantana**.
1. Í svarglugganum **Sjálfvirk losun á flutningspöntunum**, í flýtiflipanum **Færibreytur**, skal stilla eftirfarandi reiti:

    - **Magn sem á að losa** – Veldu hvort eigi að losa allt magnið eða aðeins efnislega frátekið magn í vöruhúsið.
    - **Leyfa losun pantana sem hafa verið losaðar að hluta** – Tilgreindu hvort eftirstandandi magn fyrir pantanir sem hafa verið losaðar að hluta til eigi að vera losaðar í vöruhúsið.
    - **Flokka losanir eftir viðtökuvöruhúsi** – Tilgreindu hvort kerfið eigi að losa allar flutningspantanir samtímis eða hvort það eigi að flokka flutningspöntunarlínur eftir viðtökuvöruhúsi og síðan losa hvern flokk fyrir sig í vöruhúsið.

1. Til að stýra því hvaða pantanir eigi að vinna úr skal í flýtiflipanum **Færslur til að taka með** velja **Sía**. Hefðbundin svargluggi fyrirspurnar birtist þar sem hægt er að skilgreina valskilyrði, röðunarskilyrði og tengingar. Reitirnir virka á sama hátt og fyrir aðrar gerðir fyrirspurna í Supply Chain Management.
1. Í flýtiflipanum **Keyra í bakgrunni** skal velja hvort vinnslan keyri í runustillingu og/eða setja upp áætlun fyrir endurtekningu. Reitirnir virka rétt eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management.
1. Veldu **Í lagi** til að virkja stillingarnar þínar og hefja losunarferli í vöruhús.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
