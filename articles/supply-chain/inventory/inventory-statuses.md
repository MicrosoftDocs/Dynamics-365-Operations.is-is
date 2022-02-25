---
title: Birgðastöður
description: Þessi grein lýsir því hvernig þú getur notað birgðastöðu til að flokka og fylgjast með birgðum.
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus, WHSWarehouseStatusChange
audience: Application User
ms.reviewer: kamaybac
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db15ad94355823c699e83c9e3f47660f813e1c9a
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103464"
---
# <a name="inventory-statuses"></a>Birgðastöður

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig þú getur notað birgðastöðu til að flokka og fylgjast með birgðum.

## <a name="set-up-and-use-inventory-statuses"></a>Setja upp og nota birgðastöður

Hægt er að nota birgðastöðu til að flokka birgðir. Síðan er hægt að hefja viðeigandi aðgerðir, eins og áfyllingu eða frágangsvinnu.

Hér eru nokkur dæmi um sem hægt er að nota birgðastöður:

- Stofna stöðuna fyrir birgðir á lager, færslur á innleið og færslur á útleið .
- Tilgreina sjálfgefna birgðastöðu fyrir færslur fyrir vöruhús.
- Breyta stöðu birgða í vörum fyrir komu vöru, við komu, eða þegar vörur eru frágangur við birgðahreyfingu.
- Notið birgðastöðu fyrir verðlagningu á vörum þegar þeim er skilað og til að áætla þekju fyrir vöru við aðaláætlanagerð.

Birgðastaða er ein af víddum í geymsluvíddaflokki. Hægt er að flokkað birgðastöðu sem tiltækt eða ekki tiltækt og hægt er að nota **birgðalæsingu** færibreytu til að læsa vörum sem hafa stöðuna ekki tiltækt í birgðum. Vörur með lokaða stöðu eru taldar raunbirgðir og ekki er hægt að nota þær í framleiðslupöntun, sölupöntun, millifærslupöntun eða útleiðarfærslu.

Hægt er að nota vörur í vöruhúsi með birgðastöðu tiltækt eða ekki tiltækt fyrir vinnu á innleið. Til dæmis stofnaður tiltæka stöðu sem heitir *tilbúinn*, ótiltæka stöðu sem heitir *skemmt* og lokaða stöðu sem heitir *lokað*. Þegar innkaupapöntun er stofnuð fyrir móttekið eða skilavörur, ef einhverjar vörur eru skemmt eða brotið, hægt að breyta birgðastöðu þær vörur *"Skemmt"* í innkaupapöntunarlínunni. Eftir að þessar vörur eru mótteknar staðan er sjálfkrafa stillt á *Læst*. Ef að þú skannar þessar skemmdu vörur með fartæki, getur Supply Chain Management nota staðsetningarleiðbeiningar og vinnusniðmát til að birta upplýsingar um viðeigandi staðsetning eða svið staðsetningar fyrir frágang þessara vara. Fyrir skilavörur er stofnuð *frátekning* fyrir úthreyfingar í skjámyndinni **Birgðafærslur**.

Hægt er að tilgreina hvaða birgðastöður eru lokunarstöður með því að nota **birgðalæsingu** gátreiti á síðunni **Birgðastöður**. Þú getur ekki notað birgðastöðu sem lokunarstöður fyrir sölupantanir, flutningspantanir eða samþættingar verks.

Fyrir verk á útleið er hæg tða nota aðrar birgðarstöður sem ekki eru lokunarstöður til að stýra í hvaða birgðum er tekið frá. Ef þú ert með vörur með stöðuna *Lokun* og aðaláætlanagerð er keyrð fyrir þessar vörur, er litið á þessar vörur þannig að þær vanti og birgðir eru endurnýjaðar sjálfkrafa. Fyrir gæðavörur með verk á útleið er ennfremur ekki hægt að uppfæra **Birgðastaða** sem hluta af staðfestingu gæðapöntunar.

> [!NOTE]
> Ekki er hægt að breyta stöðu birgða á staðsetningum þar sem opin vinna er til staðar. Til dæmis, ef tekið var á móti innkaupum fyrir vöru, en frágangsskrefið var ekki gert, þá yrði opin vinna vera til fyrir móttökustaðsetninguna og ekki kæmi upp villa ef reynt væri að breyta stöðu birgðanna á þeirri staðsetningu. Með því að ljúka við eða hætta við tengda vinnu er hægt að breyta stöðunni.
>
> Yfirleitt er stöðu lagerbirgða sem tengjast opinni vöruhúsavinnu aðeins breytt með því að starfskraftar noti farsímaforrit vöruhúsakerfis, til dæmis við keyrslu á hreyfingarferli.

Eftir að þú hefur sett upp birgðastöðu er hægt að stilla sjálfgefna birgðastöðu fyrir síðu, vöru og vöruhús. Einnig er hægt að stilla sjálfgefna stöðu fyrir sölu, flutning, og innkaupapantanir. Sjálfgefin staða fyrir sölupantanir og flutningspöntun á útleið getur ekki haft **birgðalæsingu** valkostur stilltan á *Já*. Birgðastöðu sem er erft frá sjálfgefnar stillingar á setri, vöruhúsi, vöru, innkaupapöntun, flutningspöntun eða sölupöntun er hægt að breyta með því að nota fartækið eða á innkaupapöntun, sölupöntun eða flutningspöntunarlínu.

Til að áætla þekju fyrir vörur sem hafa stöðuna tiltækar birgðir skal velja **þekjuáætlun eftir vídd** valkostinn fyrir geymsluvídd á í **geymsluvíddaflokka** síðu. Þegar opnar **Vöruþekju** leiðsagnarforritið birtast vörur sem hafa stöðuna tiltækt á **Stöðu** síðu. Til að stofna þekjustillingar fyrir þessar vörur er að velja birgðastöðukenni fyrir tiltæka birgðastöðu. Samkvæmt þekjustillingar hægt að reikna vöruþarfir og spá framboð og eftirspurn tiltækar vörur með við áætlanagerð. Ekki er hægt að stofna uppsetningu vöruþekju með læsta birgðastöðu. Að öðrum kosti notarðu **vöruþekju** síðu til að stofna eða breyta tryggingafæribreytum vöru.

## <a name="change-inventory-statuses"></a>Breyta birgðastöðum

Hægt er að breyta birgðastöðu annaðhvort með því að nota síðuna **Á lager eftir staðsetningu** eða með því að nota reglubundnu vinnsluna *Breyting á birgðastöðu*.

- Þegar reglubundna vinnslan *Breyting á birgðastöðu* er notuð er hægt að velja hvaða færslur skal taka með og stilla vinnsluna á að keyra í rununni á tilteknu tímabili.
- Til að breyta birgðastöðu sem tilfallandi ferli skaltu opna síðuna **Á lager eftir staðsetningu**, velja viðeigandi færslur og síðan smella á hnappinn **Breyting á birgðastöðu**.

> [!NOTE]
> Eiginleiki *Breyta birgðastöðu atriða sem er stjórnað af rakningarvíddum* gerir notendum kleift að breyta birgðastöðu á vörum sem rakningarvíddir stýra, þ.m.t. möguleikanum á að uppfæra aðeins valdar færslur. Frá og með Supply Chain Management 10.0.25 er þessi eiginleiki skylda og ekki hægt að slökkva á honum. Ef þú ert að keyra útgáfu eldri en 10.0.25 geta stjórnendur kveikt eða slökkt á þessari virkni með því að leita að *Breyta birgðastöðu vara sem stjórnað er af rakningarvíddum* eiginleiki í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnurými. Ef eiginleikinn er virkur geturðu gert eftirfarandi:
>
> - Á síðunni **Á lager eftir staðsetningu** er hægt að flokka línurnar út frá birtum víddunum með því að nota hnappinn **Sýna víddir** og breyta stöðunni fyrir völdu línurnar.
> - Á síðunni **Á lager eftir staðsetningu** er hægt að velja margar færslur og nota svo hnappinn **Breyting á birgðastöðu** til að breyta öllum í einu.
> - Á reglubundna verkefninu **Breyting á birgðastöðu** er hægt að sía eftir rakningarvíddunum.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
