---
title: Stofna flutningspantanir úr vöruhúsaforriti
description: Þessi grein lýsir því hvernig á að búa til og vinna flutningspantanir úr vöruhúsastjórnun farsímaforritinu
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b9edc2d94aa1f4850d2e7fe2b4bdd1b092be944f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877451"
---
# <a name="create-transfer-orders-from-the-warehouse-app"></a>Stofna flutningspantanir úr vöruhúsaforriti

[!include [banner](../includes/banner.md)]

Þessi eiginleiki gerir starfsmönnum vöruhúss kleift að stofna og vinna úr flutningspöntunum beint úr farsímaforriti Warehouse Management. Starfskrafturinn byrjar á því að velja vöruhús áfangastaðar og síðan geta þeir skannað eina eða fleiri númeraplötur með því að nota forritið til að bæta númeraplötum við flutningspöntunina. Þegar starfsmaður í vöruhúsi velur **Ljúka við pöntun**, býr runuvinnsla til nauðsynlega flutningspöntun og pöntunarlínur samkvæmt skráðum lagerbirgðum fyrir þessar númeraplötur.

## <a name="turn-this-feature-on-or-off"></a><a name="enable-create-transfer-order-from-warehouse-app"></a> Kveiktu eða slökktu á þessum eiginleika

Áður en hægt er að nota þennan eiginleika, þarf að virkja hann og skilyrði hans í kerfinu. Stjórnendur geta notað síðuna [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og virkjað hann ef þörf krefur.

1. Virkjaðu eftirfarandi tvo eiginleika (í röð) í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnurými. Frá og með Supply Chain Management útgáfu 10.0.25 er sjálfgefið kveikt á báðum þessum eiginleikum.
    1. *Vinna úr viðburðum vöruhúsaforrits*
    1. *Stofna og vinna úr flutningspöntunum úr vöruhúsaforriti*
1. Til að gera sjálfvirka vinnslu á sendingar á útleið verður þú einnig að virkja [Staðfestu sendingar á útleið frá runuvinnu](confirm-outbound-shipments-from-batch-jobs.md) eiginleiki.

## <a name="set-up-a-mobile-device-menu-item-to-create-transfer-orders"></a><a name="setup-warehouse-app-menu"></a>Setja upp valmyndaratriði fartækis til að stofna flutningspantanir

Hér eru almennar leiðbeiningar til að setja upp valmyndaratriði fartækis til að stofna flutningspöntun. Skilgreiningarnar sem verða virkjaðar, fara eftir viðskiptaþörfum fyrir stig sjálfvirkni sem er sett á þegar notendur stofna flutningspantanir á gólfinu. Aðstæður í þessu skjali munu lýsa einni slíkri skilgreiningu.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Veljið **Nýtt** til að bæta við nýju valmyndaratriði. Stilltu síðan eftirfarandi til að hefjast handa:

    - **Heiti valmyndaratriðis** - Úthlutið heiti eins og það á að birtast í Supply Chain Management.
    - **Titill** - Úhlutið heiti valmyndar eins og það á að birtast starfmönnum í farsímaforriti Warehouse Management.
    - **Stilling** - Stillið á *Óbeint* (þetta valmyndaratriði mun ekki búa til verk).
    - **Verkþáttarkóði** - Stillið á *Stofna flutningspöntun úr númeraplötum* til að gera starfsmanni vöruhúss kleift að stofna flutningspöntun sem byggir á einni eða fleiri skönnuðum númerplötum.

1. Notið stillinguna **Regla um stofnun flutningspöntunarlínu** til að hafa stjórnun á því hvernig flutningspöntunarlínur verða búnar til í þessu valmyndaratriði. Línurnar verða stofnaðar/uppfærðar samkvæmt lagerbirgðum sem skráðar eru fyrir skannaðar númeraplötur. Veldu eitt af eftirfarandi gildum:

    - **Engin frátekt** - Flutningspöntunarlínur verða ekki teknar frá.
    - **Leitt af númerplötu með línufrátekt** – Flutningspöntunarlínur verða teknar frá og nota leiðsagnaraðferð númeraplötu, sem geymir viðeigandi númeraplötukenni sem tengjast pöntunarlínunum. Staðsett gildi númeraplötukenna er því hægt að nota sem hluta af stofnferli verks fyrir flutningspöntunarlínur.

1. Notið stillinguna **Regla um sendingu á útleið** til að bæta meiri sjálfvirkni við sendingarferli flutningspantana á útleið eftir því sem þörf krefur. Þegar starfsmaður velur hnappinn **Ljúka við pöntun**, býr forritið til tilvikið *Ljúka við pöntun* í vöruhúsaforritinu, sem vistar valið gildi hér í reitnum **Regla um sendingu á útleið** fyrir hverja línu í núverandi flutningspöntun. Síðar, þegar unnið er úr tilviksröðinni með runuvinnslu til að stofna flutningspöntunina, getur runuvinnslan lesið gildið sem vistað er í þessum reit og getur þannig haft stjórn á því hvernig vinnslan vinnur hverja línu. Veljið um eitt af eftirfarandi:

    - **Ekkert** - Ekkert sjálft ferli fer af stað.
    - **Losa í vöruhús** - Gerir losunarferlið í vöruhús sjálfvirkt.
    - **Sending staðfest** - Gerir staðfestingarferli sendingar sjálfvirkt.
    - **Losa og staðfesta sendingu** - Gerir bæði losunarferli í vöruhús og staðfestingarferli sendingar sjálfvirkt.

## <a name="add-the-mobile-device-menu-item-to-a-menu"></a>Bæta valmyndaratriði fartækis við valmynd

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**
1. Veljið **Breyta**.
1. Veljið fyrirliggjandi valmynd eftir val á nýja valmyndaratriðinu undir **Tiltækar valmyndir og valmyndaratriði**. Bætið valmyndaratriðinu við með því að velja hægri örvarhnappinn.

## <a name="create-a-transfer-order-based-on-license-plates"></a>Flutningspöntun stofnuð sem byggir á númeraplötum

Farsímaforrit Warehouse Management er með einfalt ferli til þess að stofna flutningspantanir sem byggja á númeraplötum. Til að gera þetta gerir starfsmaðurinn eftirfarandi með því að nota farsímaforrit Warehouse Management:

1. Stofnið flutningspöntunina og auðkennið vöruhús áfangastaðar.
1. Auðkennið hverja númeraplötu sem á að senda.
1. Veljið **Ljúka við pöntun**.

>[!NOTE]
> Mögulegt er fyrir marga starfsmenn að úthluta númeraplötum sem ætluð eru fyrir sömu flutningspöntunina með því nota hnappinn **Velja flutningspöntun** til að velja fyrirliggjandi, óunnið flutningspöntunarnúmer úr tilvikaröð vöruhúsaforritsins. Upplýsingar um hvernig á að finna gildi flutningspöntunarnúmersins er að finna í [Spyrjast fyrir um tilvik vöruhúsaforrits](#inquire-the-warehouse-app-events).

## <a name="example-scenario"></a>Dæmi

Þetta dæmi veitir yfirlit yfir ferlið við að ná í flutningspantanir sem eru stofnaðar og sjálfkrafa unnið úr samkvæmt lagerbirgðum sem skráðar eru á valdar númeraplötur.

Til að vinna í gegnum þetta dæmi með því að nota ráðlögð gildi, þarf að vinna í kerfi með sýnigögnum uppsettum og velja lögaðilann *USMF* áður en hafist er handa.

Þetta tilvik gerir ráð fyrir að þegar sé búið að virkja bæði möguleikann [Stofna og vinna úr flutningspöntunum úr vöruhúsaforriti](#enable-create-transfer-order-from-warehouse-app) og [Vinnsla tilvika í vöruhúsaforriti](warehouse-app-events.md).

Ásamt því að setja upp stofnun flutningspöntunar í valmyndaratriðum fartækis, verða önnur sniðmát, staðsetningarleiðbeiningar og runuvinnslur einnig að vera sett upp og virkjað.

### <a name="example-scenario-blueprint"></a>Grunndæmi

Þú ert smásali og ert með margar númeraplötur, sem hver inniheldur blöndu af vörum sem eru staðsettar á tiltekinni staðsetningu í einu af vöruhúsunum þínum (*Vöruhús 51*). Þig langar til að virkja ferlið sem gerir starfsmönnum kleift að stofna flutningspöntun á annað vöruhús (*Vöruhús 61*) fyrir safn af skönnuðum númeraplötum. Þú munt sjálfkrafa uppfæra sendingu flutningspöntunarinnar um leið og síðasta númeraplata pöntunarinnar hefur verið auðkennd.

![Dæmi um sjálfvirkt flutningspöntunarferli.](media/create-transfer-order-from-app-example.png "Dæmi um sjálfvirkt flutningspöntunarferli")

### <a name="create-a-mobile-device-menu-item-for-creating-transfer-orders"></a>Stofna valmyndaratriði fartækis til að stofna flutningspantanir

Í þessum hluta er útskýrt hvernig á að stofna valmyndaratriði fartækis til að stofna flutningspantanir. Setjið **Stilling** á *Óbeint* og **Verkþáttarkóði** á *Stofna flutningspöntun úr númeraplötum*.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Veljið **Nýtt**.
1. Í reitinn **Heiti valmyndaratriðis** skal færa inn heitið *Stofna FP*.
1. Í reitinn **Titill** skal færa inn lýsinguna *Stofna FP*.
1. Í reitnum **Stilling** velurðu *Óbeint*.
1. Í **Verkþáttarkóði** skal velja *Stofna flutningspöntun úr númeraplötum*
1. Í **Regla um stofnun pöntunarlínu** skal velja *Leitt af númerplötu með línufrátekt*.
1. Í **Regla um sendingu á útleið** skal velja *Losa og staðfesta sendingu*.
1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.
1. Veljið **Breyta**.
1. Veljið núverandi valmyndina **Birgðir** og veljið síðan nýja valmyndaratriðið undir **Tiltækar valmyndir og valmyndaratriði**. Bætið valmyndaratriðinu við valmyndina **Birgðir** með því að velja hægri örvarhnappinn.

### <a name="set-up-work-templates-to-auto-process-and-break-work-by-located-license-plate"></a>Setja upp vinnusniðmát til að vinna sjálfvirkt úr og sundurliða vinnu með því að staðsetja númeraplötu

Þessi hluti útskýrir hvernig á að virkja vinnusniðmát til að vinna sjálfkrafa úr vinnu sem sniðmátið býr til þegar bylgja er losuð.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.
1. Í reitnum **Gerð verkbeiðni** skal velja *Flutningsútgáfa*.
1. Velja skal **Nýtt** til að búa til nýtt vinnusniðmát.
1. Í reitinn **Vinnusniðmát** skal færa inn *51 Vinna sjálfvirkt úr NP*.
1. Í reitinn **Lýsing á vinnusniðmáti** skal færa inn *51 Vinna sjálfvirkt úr NP*.
1. Veljið gátreitinn **Sjálfvirk úrvinnsla**. Þetta verður að velja til að hægt sé að vinna úr sjálfvirkum skrefum.
1. Í sýnigögnunum er þegar til vinnusniðmát *51 Flutningur*, breytið reitnum **Raðnúmer** þannig að nýja sniðmátið sé með lægra raðnúmer en fyrirliggjandi vinnusniðmát *51 Flutningur*.
1. Veljið **Vista** í tækjastikunni til að virkja flýtiflipann **Upplýsingar vinnusniðmáts**.
1. Í flýtiflipanum **Upplýsingar vinnusniðmáts** skal velja **Nýtt** í tækjastikunni. Tveimur línum verður bætt við.
1. Í reitnum **Vinnutegund** velurðu *Tína*.
1. Í reitinn **Vinnuklasakenni** skal velja *TransfOut*.
1. Veljið **Nýtt** í tækjastikunni **Upplýsingar vinnusniðmáts**.
1. Í reitnum **Verkbeiðni** velurðu *Frágangur*.
1. Í reitinn **Vinnuklasakenni** skal velja *TransfOut*.
1. Veljið **Vista** til að virkja reitinn **Leiðbeiningarkóði**.
1. Í **Verkgerð**, línunni *Frágangur*, skal velja **Leiðbeiningarkóði** *Útskot*. Ganga skal úr skugga um að þetta nýja vinnusniðmát fái lægsta **Raðnúmerið**.
1. Í tækjastikunni skal velja **Breyta fyrirspurn** til að opna fyrirspurnarritilinn.
1. Í flipanum **Svið** skal velja **Bæta við**.
1. Í línunni sem bætt er við, í **Svæði**, skal velja *Vöruhús*.
1. Í reitnum **Skilyrði** skal velja *51*.
1. Veljið flipann **Röðun**.
1. Veljið **Bæta við** og stillið **Svæði** á *Staðsett númeraplötukenni*. Ef þessi reitur er valinn verður tækjastikuhnappurinn **Vinnuhausaskil** virkjaður.
1. Veljið **Í lagi** og síðan **Já** til að endurstilla flokkunina og fara aftur á síðuna **Vinnusniðmát**.
1. Veljið **Vinnuhausaskil** og virkjið **Flokka eftir þessum reit** fyrir **Staðsett númeraplötukenni** og lokið.

> [!NOTE]
> Ekki er hægt að vinna sjálfkrafa úr öllum uppsetningum, til dæmis vörur með framleiðsluþyngd og notkun blandaðrar rakningarvíddar.

### <a name="set-up-location-directives-for-the-license-plate-guided-strategy"></a>Setja upp staðsetningarleiðbeiningar fyrir aðferð númeraplötuleiðsagnar

Í þessum hluta er útskýrt hvernig á að setja upp tínsluferli staðsetningarleiðbeiningar til að nota aðferðina **Leitt af númerplötu**.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.
1. Veljið **Breyta**.
1. Í haus flettilistans skal velja **Gerð verkbeiðni** *Flutningsútgáfa*.
1. Í flettilistanum skal velja fyrirliggjandi staðsetningarleiðbeiningu **51 Tiltekt FP**.
1. Í flýtiflipanum **Línur** skal velja gátreitinn **Leyfa að skipta**.
1. Í flýtiflipanum **Aðgerðir staðsetningarleiðbeininga** skal velja **Ný** til að bæta við nýrri aðgerðarlínu.
1. Í reitinn **Heit** skal færa inn *Leitt af NP*.
1. Í reitnum **Aðferð** skal velja *Leitt af númerplötu*. Þessi aðgerð þarf lægsta raðnúmerið.
1. Veljið **Vista** í tækjastikunni.
1. Veljið síðutáknið **Endurhlaða** á tækjastikunni.
1. Í flýtiflipanum **Aðgerðir staðsetningarleiðbeininga** skal velja línuna *Tiltekt FP*.
1. Á tækjastikunni **Aðgerðir staðsetningarleiðbeininga** skal velja **Færa niður** til að breyta raðnúmerinu þannig að það verði hærra en raðnúmerið fyrir aðgerðina *Leitt af NP* sem var stofnað í rétt í þessu.

> [!NOTE]
> Aðferð númeraplötustýringar reynir að taka frá og stofna tiltekt fyrir staðsetningarnar sem geyma umbeðnar númeraplötur sem hafa verið tengdar við flutningspöntunarlínurnar. En ef þetta er ekki mögulegt og ætlunin er enn að stofna tiltekt, ætti að fara til baka í aðra aðgerð staðsetningarleiðbeiningar og hugsanlega leita einnig að birgðum á öðru svæði vöruhússins, eftir því hvað viðskiptaferlið þarf á að halda.

### <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Setja upp runuvinnslu til að vinna úr viðburðum vöruhúsaforrits

Í þessum hluta er útskýrt hvernig á að setja upp áætlaða runuvinnslu til að vinna úr tilvikum vöruhúsaforritsins.

1. Farið í **Vöruhúsakerfi \> Reglubundin verk \> Vinna úr viðburðum vöruhúsaforrits**.
2. Í svarglugganum skal virkja **Runuvinnslu** undir hlutanum **Keyra í bakgrunni**.
3. Veljið **Endurtekning** og setjið upp runuvinnsluna fyrir úrvinnslu samkvæmt tímabilinu sem reksturinn þarf á að halda.
4. Smellið á **Í lagi** til að fara aftur á aðalskjá.
5. Veljið **Í lagi** í aðalglugganum til að bæta vinnslunni við runuröðina.

### <a name="set-up-a-batch-job-to-release-transfer-orders-automatically"></a>Setja upp runuvinnslu til að losa flutningspantanir sjálfkrafa

Í þessum hluta er útskýrt hvernig á að setja upp áætlaða runuvinnslu til að losa flutningspantanir sem hafa verið merktar sem „tilbúnar til losunar“.

1. Farið í **Vöruhúsakerfi \> Losa í vöruhús \> Sjálfvirk losun sölupantana**.
1. Í svarglugganum skal stækka hlutann **Færslur til að taka með**.
1. Veljið **Sía** undir hlutanum **Færslur til að taka með**.
1. Á fyrirspurnarsíðunni **WHSTransferAutoRTWQuery**, í flipanum **Svið**, skal velja **Bæta við** til að bæta nýrri línu við fyrirspurnina.
1. Í nýju línu reitsins **Tafla** skal velja fellivalmyndina og velja töfluna **Flutningslínulosun í vöruhús**.
1. Í fellivalmyndinni **Svæði** skal velja **Regla um sendingu á útleið**.
1. Í reitnum **Skilyrði** skal velja **Losa og staðfesta sendingu**.
1. Í línunni þar sem **Svæði** er stillt á *Frá vöruhúsi*, í reitnum **Skilyrði**, skal velja *51*.
1. Veljið **Í lagi** til að fara aftur í aðalgluggann.
1. Stækkið hlutann **Keyra í bakgrunni** til að setja upp runuvinnslu.
1. Virkjið **Runuvinnslu** undir hlutanum **Keyra í bakgrunni**.
1. Veljið **Endurtekning** og setjið upp runuvinnsluna fyrir úrvinnslu samkvæmt tímabili sem reksturinn þarf á að halda.
1. Smellið á **Í lagi** til að fara aftur á aðalskjá.
1. Veljið **Í lagi** í aðalglugganum til að bæta runuvinnslunni við runuröðina.

### <a name="set-up-the-process-outbound-shipment-batch-job"></a>Setja upp runuvinnsluna „Vinna úr sendingu á útleið“

Í þessum hluta er útskýrt hvernig á að setja upp áætlaða runuvinnslu til að keyra staðfestingu á sendingu á útleið fyrir farma sem eru tilbúnir til afhendingar í tengslum við flutningspöntunarlínur sem eru „tilbúnar til afhendingar“:

1. Farið í **Vöruhúsakerfi \> Reglubundin verk \> Vinna úr sendingum á útleið**.
1. Útvíkka **Færslur til að taka með** hlutann.
1. Velja **Síu**.
1. Í fyrirspurninni **WHSLoadShipConfirm** skal velja flipann **Samtengingar**.
1. Víkkið út töflustigveldið þannig að **Hleðslur** og **Upplýsingar um hleðslu** hafa verið stækkuð.
1. Veljið töfluna **Upplýsingar um hleðslu**.
1. Velja skal hnappinn **Bæta við töflusamtengingu**.
1. Í listanum yfir töfluvensl, skal sía eða leita í dálknum **Vensl** fyrir *Flutningspöntunarlínur (Tilvísun)*.
1. Leggið áherslu á töfluvenslin í listanum og ýtið síðan á hnappinn **Velja**.
1. Veljið töfluna **Flutningspöntunarlínur**.
1. Velja skal hnappinn **Bæta við töflusamtengingu**.
1. Í listanum yfir töfluvensl, skal sía eða leita í dálknum **Vensl** fyrir *Viðbótarreitir birgðaflutnings (færslukenni)*.
1. Leggið áherslu á töfluvenslin í listanum og ýtið síðan á hnappinn **Velja**.
1. Smellt er á flipann **Svið**.
1. Í fyrirspurnartöflum **Sviðs** skal setja upp þrjú svið fyrirspurnarskilyrða. Veldu **Bæta við**-hnappinn til að bæta við línu.
1. Bætið sviði við fyrir töfluna **Hleðslur**. Stillið **Svæði** á *Hleðslustaða* og stillið **Skilyrði** á *Hlaðið*.
1. Bætið við öðru sviði fyrir töfluna **Viðbótarreitir birgðaflutnings**. Stillið **Svæði** á *Regla um sendingu á útleið* og stillið **Skilyrði** á *Losa og staðfesta sendingu*.
1. Bætið við öðru sviði fyrir töfluna **Upplýsingar um hleðslu**. Stillið **Svæði** á *Tilvísun* og stillið **Skilyrði** á *Sending flutningspöntunar*.
1. Veljið **Í lagi** til að fara aftur í aðalgluggann.
1. Stækkaðu hlutann **Keyra í bakgrunni**.
1. Gera **runukeyrslu óvirka**
1. Veljið **Endurtekning** og setjið upp runuvinnsluna fyrir úrvinnslu samkvæmt tímabili sem reksturinn þarf á að halda.
1. Smellið á **Í lagi** til að fara aftur á aðalskjá.
1. Veljið **Í lagi** í aðalglugganum til að bæta runuvinnslunni við runuröðina.

> [!NOTE]
> Frekari upplýsingar er að finna á [Staðfesta sendingar á útleið úr runuvinnslum](confirm-outbound-shipments-from-batch-jobs.md).

## <a name="processing-the-example-for-create-transfer-order-from-the-warehouse-app"></a>Unnið úr dæminu fyrir „Stofna flutningspantanir úr vöruhúsaforriti“

### <a name="add-on-hand-on-a-license-plate"></a>Bæta lager við númeraplötu

Sem upphafspunkt fyrir þetta dæmi þarf að hafa númeraplötu sem inniheldur efnislegar tiltækar birgðir á lager.

| vara | Vöruhús | Birgðastaða | Staður | Númeraplata | Magn |
| --- | --- | --- | --- | --- | --- |
| A0001 | 51 | Við | LP-010 | LP10 | 1 |
| A0002 | 51 | Við | LP-010 | LP10 | 2 |

Bætið efnislegum lagerbirgðum við magn með því að nota eftirfarandi gildi:

> [!NOTE]
> Stofna þarf númeraplötuna og nota staðsetningar sem gera kleift að taka blandaðar vörur eins og NP-010.

### <a name="create-and-process-transfer-orders-from-the-warehouse-app"></a>Stofna og vinna úr flutningspöntunum úr vöruhúsaforriti

1. Opnaðu forritið og skráðu þig inn sem notandi *51*. Núverandi vöruhús notanda verður 51.
1. Veljið valmyndaratriðið **Stofna FP** úr staðsetningu valmyndar sem bætt var við við uppsetningu.
1. Stofnið flutningspöntun með því að færa inn vöruhús áfangastaðar (Til vöruhús) í reitnum **Vöruhús** og færið inn *61*. Nýja flutningspöntunin fer frá núverandi vöruhúsi 51 (Frá vöruhús) til vöruhúss áfangastaðar *61*.
1. Veljið **Í lagi**.
1. Skannið númeraplötu kenni í reitnum **Númeraplata**. Færið inn númeraplötu birgða sem bætt var við í fyrra skrefi, *NP10*.
1. Veljið **Í lagi**.
1. Veljið valmyndarhnappinn og veljið síðan **Ljúka við pöntun** til að ljúka við stofnun flutningspöntunar fyrir vöruhúsaforrit.

Fyrir uppgefið dæmi eru tvö **Tilvik vöruhúss** (*Stofna flutningspöntun* og *Ljúka flutningspöntun*) notuð.

### <a name="inquire-the-warehouse-app-events"></a><a name="#inquire-the-warehouse-app-events"></a>Spyrjast fyrir um tilvik vöruhúsaforrits

Hægt er að skoða viðburðaröðina og viðburðaskilaboðin sem farsímaforrit Warehouse Management býr til með því að fara í **Vöruhúsakerfi \> Fyrirspurnir og skýrslur \> Kladdar fartækis \> Viðburðir vöruhúsaforrits**.

Tilviksskilaboðin *Stofna flutningspöntun* fá stöðuna *Í bið*, sem þýðir að runuvinnslan **Vinna úr viðburðum vöruhúsaforrits** mun ekki taka til og vinna úr skilaboðum tilvika. Um leið og tilviksskilaboð uppfærast í stöðuna *Í biðröð* mun runuvinnslan vinna úr tilvikunum. Þetta gerist á sama tíma og stofnun tilviksins *Ljúka flutningspöntun* (þegar starfmaður velur hnappinn **Ljúka við pöntun** í farsímaforriti Warehouse Management). Þegar búið er að vinna úr tilviksskilaboðunum *Stofna flutningspöntun*, er staðan uppfærð í *Lokið* eða *Tókst ekki*. Þegar staðan *Ljúka flutningspöntun* er uppfærð í *Lokið*, er öllum tengdum tilvikum eytt úr biðröðinni.

Þar sem runuvinnslan mun ekki vinna úr **Tilviki vöruhúsaforrits** fyrir stofnun flutningspöntunargagna áður en skilaboðin eru uppfærð í stöðuna *Í biðröð*, þarf að fletta upp á umbeðnum flutningspöntunarnúmerum sem hluti af reitnum **Kennimerki**. Reiturinn **Kennimerki** er í haus síðunnar **Tilvik vöruhúsaforrits**.

Sem hluti af úrvinnslu vöruhúsatilvika, gæti stofnun flutningspöntunarlínunnar mistekist. Í slíku tilfelli verður staða tilviksskilaboðanna uppfærð í *Tókst ekki* og hægt er að nota upplýsingarnar **Runukladdi** til að komast að ástæðunni og grípa til aðgerða til að leiðrétta einhver vandamál.

Dæmigerð vandamál gætu tengst uppsetningu sem vantar fyrir ferlið, eins og flutningsvöruhúsið sem vantar fyrir tilvikið *Stofna flutningspöntun*. Í dæmi eins og þessu yrði flutningsvöruhúsi bætt við sendingarvörhúsið og valkosturinn **Endurstilla** yrði notaður til að breyta stöðunni fyrir öll tilviksskilaboð vöruhúsaforritsins úr *Tókst ekki* í *Í biðröð*, sem þýðir að runuvinnslan mun vinna úr skilaboðum tilvika aftur eftir gögn uppsetningar hafa verið lagfærð.

Í vinnsluumhverfi tengjast undantekningarnar meira úrvinnslu, t.d. að vera með umbeðna númeraplötu, sem á úrvinnslutíma runuvinnslunnar er tóm og eru þar af leiðandi engar flutningspöntunarlínur stofnaðar. Hægt er að fjarlægja þessi misheppnuðu tilvikaboð með því að nota valkostinn **Eyða** eða bæta við nauðsynlegum efnislegum birgðum númeraplötunnar og nota valkostinn **Endurstilla** fyrir öll tengd tilviksskilaboð.

Frekari upplýsingar er að finna í [Úrvinnsla á tilviki vöruhúsaforrits](warehouse-app-events.md).

### <a name="follow-up-on-the-example-scenario-processing"></a>Fylgja eftir úrvinnslu á sýnidæminu

Í þessari atburðarás kom eftirfarandi fram:

1. Með því að nota farsímaforrit Warehouse Management var valmyndaratriði valið sem notar verkþáttarkóðann **Stofna flutningspöntun úr númeraplötum**.
1. Forritið bað um að valið yrði vöruhús áfangastaðar fyrir flutningspöntunina. Upprunavöruhúsið er alltaf það sem notandi er skráður inn á sem starfsmaður.
1. Við val á vöruhúsi áfangastaðar tók kerfið frá auðkennisnúmeri fyrir komandi flutningspöntun (byggt á númeraröð flutningspöntunar sem skilgreind er í kerfinu) en stofnaði ekki flutningspöntunina enn sem komið er.
1. Þegar númeraplatan *NP10* var skönnuð, sem inniheldur lagerbirgðir sem á að flytja í nýja vöruhúsið, var **Tilviki vöruhúsaforrits** bætt við biðröð tilvika sem á að vinna síðar. Vöruhúsatilvikið innihélt skilaboð um skönnunina, þ.m.t. ætlað flutningspöntunarnúmer.
1. Í farsímaforriti Warehouse Management, þegar hnappurinn **Ljúka við pöntun** er valinn, er nýtt tilvik vöruhúsaforrits **Ljúka flutningspöntun** stofnað og tengt fyrirliggjandi tilvik, **Stofna flutningspöntun**, breytti stöðunni í **Í biðröð**.
1. Í bakvinnslunni er náði **Runuvinnsla fyrir úrvinnslu á tilvikum vöruhúsaforrits** í tilvikið **Í biðröð** og safnaði lagerbirgðum sem tengjast skannaðri númeraplötu. Byggt á lagerbirgðum, var færsla raunverulegrar flutningspöntunar og tengdar línur stofnað. Vinnslan fyllti einnig út reitinn **Regla um sendingu á útleið** fyrir flutningspöntunina með gildinu sem byggir á skilgreindri aðferð *Losa og staðfesta sendingu* og tengdi númeraplötuna við línurnar fyrir aðferðina **Leitt af númerplötu**.
1. Byggt reitargildinu **Regla um sendingu á útleið** fyrir flutningspöntunarlínuna, leiddi fyrirspurnin **Runuvinnsla sjálfvirkrar losunar á flutningspöntunum** nú til losunar á flutningspöntuninni til sendingarvöruhússins. Og vegna uppsetningarinnar fyrir notað **Bylgjusniðmát**, **Vinnusniðmát**, og **Staðsetningarleiðbeiningar**, fékk vinnan sjálfvikar úrvinnslur sem leiddi til þess að **Hleðslustaða** var uppfærð í *Hlaðið*.
1. **Runuvinnsla á úrvinnslu sendingar á útleið** er keyrð fyrir hleðsluna, sem leiðir til þess að flutningspöntunin verður send og fyrirframtilkynning um sendingu verður búin til.
1. Tímasetning allra þessara tilvika er háð stillingunum fyrir **Endurtekning** fyrir stofnaðar runuvinnslur.

## <a name="frequently-asked-questions"></a>Algengar spurningar

### <a name="mobile-device-menu-item-setup"></a>Uppsetning á valmyndaratriði fartækis

#### <a name="why-cant-i-see-create-transfer-order-from-license-plate-in-the-menu-item-work-activity-drop-down-list"></a>Hvers vegna get ég ekki séð „Stofna flutningspöntun úr númeraplötu“ í fellilista verkþáttar í valmyndaratriði?

Virkja þarf eiginleikinn *Stofna og vinna úr flutningspöntunum úr vöruhúsaforriti*. Frekari upplýsingar er að finna í [Virkja stofnun flutningspantana úr vöruhúsaforriti](#enable-create-transfer-order-from-warehouse-app).

### <a name="warehouse-management-mobile-app-processes"></a>Ferli farsímaforrits Warehouse Management

#### <a name="why-cant-i-see-the-menu-button-complete-order"></a>Hvers vegna get ég ekki séð valmyndarhnappinn „Ljúka við pöntun“?

Úthluta þarf að minnsta kosti einni númeraplötu á flutningspöntunina.

#### <a name="can-several-warehouse-management-mobile-app-users-add-license-plates-to-the-same-transfer-order-at-the-same-time"></a>Geta nokkrir fleiri en einn notandi farsímaforrit Warehouse Management bætt númeraplötum við sömu flutningspöntunina á sama tíma?

Já, margir starfsmenn vöruhúss geta skannað númeraplötur í sömu flutningspöntunina.

#### <a name="can-the-same-license-plate-be-added-to-different-transfer-orders"></a>Er hægt að bæta sömu númeraplötunni við mismunandi flutningspantanir?

Nie, aðeins er hægt að bæta númeraplötu við eina flutningspöntun í einu.

#### <a name="after-having-selected-the-complete-order-button-can-i-then-add-more-license-plates-for-that-transfer-order"></a>Þegar búið er að velja hnappinn „Ljúka við pöntun“, get ég þá bætt við fleiri númeraplötum fyrir þá flutningspöntun?

Nei, ekki er hægt að bæta fleiri númeraplötum við flutningspöntun sem er með tilvikið **Ljúka flutningspöntun** í vöruhúsaforritinu.

#### <a name="how-can-i-find-existing-transfer-orders-to-be-used-via-the-select-transfer-order-button-in-the-warehouse-management-mobile-app-if-the-order-has-not-yet-been-created-in-the-backend-system"></a>Hvernig get ég fundið fyrirliggjandi flutningspantanir sem á að nota með hnappnum „Velja flutningspöntun“ í farsímaforriti Warehouse Management, ef pöntunin hefur enn ekki verið stofnuð í bakvinnslukerfinu?

Sem stendur er ekki hægt að fletta upp flutningspöntum í forritinu, en hægt er að finna númer flutningspantana á síðunni **Tilvik vöruhúsaforrits**. Frekari upplýsingar er að finna í [Spyrjast fyrir um tilvik vöruhúsaforrits](#inquire-the-warehouse-app-events).

#### <a name="can-i-manually-select-the-transfer-order-number-to-be-used-from-the-warehouse-management-mobile-app"></a>Get ég valið handvirkt númer flutningspöntunar sem á að nota úr farsímaforriti Warehouse Management?

Aðeins sjálfkrafa mynduð flutningspöntunarnúmer í gegnum númeraraðir eru studdar.

### <a name="background-processing"></a>Bakgrunnsvinnsla

#### <a name="how-should-i-clean-up-records-in-my-warehouse-app-events-queue-message-tables"></a>Hvernig á ég að hreinsa færslur í skilaboðatöflum tilvikaraðar í vöruhúsaforritinu?

Hægt er að skoða og vinna með þetta á síðunni **Tilvik vöruhúsaforrits**. Frekari upplýsingar er að finna í [Spyrjast fyrir um tilvik vöruhúsaforrits](#inquire-the-warehouse-app-events).

#### <a name="why-is-the-transfer-order-receipt-date-not-updated-according-to-my-delivery-date-control-setup"></a>Hvers vegna er „Móttökudagsetning“ flutningspöntunar ekki uppfærð í samræmi við uppsetninguna mína á „Stýring afhendingardagsetningar“?

Flutningspantanirnar eru búnar til án þess að nota möguleikann **Stýring afhendingardagsetninga**.

#### <a name="can-i-use-a-license-plate-having-physical-negative-inventory-on-hand"></a>Get ég notað númeraplötu með neikvæðar efnislegar birgðir?

Eiginleikinn styður aðeins jákvætt efnislegt magn á lager á stigi númeraplötu, en hægt er að vera með neikvætt efnislegt magn á hærri stigum vöruhúss og birgðastöðu þegar númeraplötum er úthlutað á flutningspantanir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]