---
title: Frágangsklasar
description: Frágangsklasar bjóða upp á leið til að tína margar númeraplötur samtímis og ganga síðan frá þeim á mörgum staðsetningum. Þeir geta verið mjög gagnlegir fyrir smásölufyrirtæki þar sem númeraplötur eru yfirleitt ekki heil bretti af birgðum.
author: Mirzaab
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 297792e90b3d2da0d738f5cbaa14779bc17ea3c8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996199"
---
# <a name="putaway-clusters"></a>Frágangsklasar

[!include [banner](../includes/banner.md)]

Frágangsklasar bjóða upp á leið til að tína margar númeraplötur samtímis og ganga síðan frá þeim á mörgum staðsetningum. Þetta ferli er oft kallað *samflutningur*. Frágangsklasar geta verið mjög gagnlegir fyrir smásölufyrirtæki þar sem númeraplötur eru yfirleitt ekki heil bretti af birgðum. 

## <a name="turn-on-the-cluster-putaway-feature"></a>Kveikja á eiginleika frágangsklasa

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Þar er eiginleikinn sýndur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Eiginleiki fyrir frágang klasa*

## <a name="setup-for-the-example-scenario"></a>Uppsetning fyrir dæmi um aðstæður

### <a name="cluster-profiles"></a>Klasanotandaupplýsingar

Forstilling frágangsklasa ákvarðar hvert varan fer samkvæmt staðsetningunni sem vörunni er úthlutað þegar hún er móttekin. Ef krafist er mismunandi klasa skal stofna mismunandi frágangsklasa, einn fyrir hvert valmyndaratriði fartækis.

1. Farðu á **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Klasaforstillingar**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í **Haus** skal stilla eftirfarandi gildi:

    - **Forstillingarkenni frágangsklasa:** *Frágangur klasa*
    - **Heiti forstillingarkennis frágangsklasa:** *Frágangur klasa*
    - **Gerð klasa:** *Frágangur*
    - **Raðnúmer:** Samþykkja sjálfgildið.

1. Veljið **Vista** til að gera áskilda reiti í flýtiflipanum **Almennt** tiltæka.
1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Tímasetning á úthlutun klasa:** *Við móttöku*

        Þessir reitir skilgreina hvort eigi að úthluta frágangsklasa strax þegar tekið er á móti birgðum eða hvort eigi að flokka þá seinna.

    - **Úthlutunarregla klasa:** *Handvirkt*

        Þessi reitur skilgreinir hvort ákveða eigi úthlutun klasans sjálfkrafa af kerfinu eða handvirkt af notanda.

    - **Leiðbeiningarkóði:** Hafðu þetta svæði autt.
    - **Staður frágangsklasa:** *Kvittun*

        Eftirtalin gildi eru tiltæk:

        - **Kvittun** – Staðsetning finnst strax við móttöku.
        - **Klasalokun** – Staðsetning finnst þegar klasanum er lokað.
        - **Stýrt af notanda** - Staðsetning er fundin þegar númeraplatan er tínd úr klasanum fyrir frágang. Í þessu tilvikum er engin staðsetning tilgreind þegar frágangsvinna er stofnuð. Við sjálfan fráganginn verður notandinn að skanna númeraplötuna eða verkkennið til að hefja frágangsskrefið. Kerfið finnur síðan frágangsstaðsetninguna aftur og segir notandanum hvar á að ganga frá tiltektarmagninu.

    - **Frágangsklasi á hvern notanda:** *Nei*

        Þessi reitur skilgreinir hvort hver klasi eigi að vera einkvæmur fyrir notanda þegar klösum er úthlutað sjálfkrafa. Hann er aðeins í boði þegar reiturinn **Úthlutunarregla klasa** er stilltur á *Sjálfvirkur*.

    - **Takmörkun einingar:** Hafðu reitinn auðan.

        Þessi svæði skilgreinir eininguna sem verður að vera móttekin til að forstillingin sé gild. Ef þetta er skilið eftir autt eru allar einingar gildar.

    - **Skipting verkeiningar:** *Út af fyrir sig*

        Þessi reitur skilgreinir hvort allar birgðir eigi að vera sameinaðar (með því að nota klasakenni og númeraplötu) í eina númeraplötu þegar klasi er lokaður og hvort eigi að ganga frá þeim á einni númeraplötu eða aðskildar á númeraplötum sem tekið var á móti. Þessi reitur er ekki í boði þegar reiturinn **Staður frágangsklasa** er stilltur á *Móttaka*.

    - **heldur yfireiningu númeraplötu:** *Nei*

        Ef þessi valkostur er stilltur á *Já*, þegar frágangsskrefinu er lokið, verður klasakennið að yfireiningu númeraplötu og allar vörur í klasakenninu verða tengdar við þessa yfireiningu númeraplötunnar.

1. Í flýtiflipanum **Klasaröðun** er hægt að skilgreina skilyrði frágangsröðunar. Veljið **Ný** í tækjastikunni til að bæta við línu og stillið síðan eftirfarandi gildi:

    - **Raðnúmer:** Samþykkja sjálfgildið.
    - **Heiti reits:** *WMSLocationId*

        Þessi reitur skilgreinir reitinn sem þessi lína á að nota sem röðunarskilyrði.

    - **Röðun:** - Veljið *Hækkandi*

        Þessi reitur skilgreinir hvort á að framkvæma röðun í hækkandi eða lækkandi röð.

1. Í flýtiflipanum **Vinnusniðmát klasa** skal velja **Ný** í tækjastikunni til að bæta við línu og stillið síðan eftirfarandi gildi:

    - **Gerð verkbeiðni:** *Innkaupapantanir*
    - **Vinnusniðmát:** *61 PO Direct*

1. Á aðgerðasvæðinu skal velja **Vista** og síðan velja **Breyta fyrirspurn**.
1. Í **Frágangur klasa** svarglugganum á flipanum **Svið** velur þú **Bæta við** til að bæta annari línu við fyrirspurnina. Uppfærið síðan fyrirspurnarlínurnar eins og sýnt er í eftirfarandi töflu.

    | Tafla | Afleidd tafla | Svæði | Skilyrði |
    |---|---|---|---|
    | Starf | Starf | Vöruhús | *61* |
    | Starf | Starf | Auðkenni vinnu | Hafa reitinn auðann. |

1. Veldu **Í lagi** til að vista fyrirspurnina og lokaðu glugganum.
1. Í aðgerðarúðunni skal velja **Vista** og loka síðunni.

> [!IMPORTANT]
> Reitir í klasaforstillingunni sem eru skyggðir þegar **Mynda klasaauðkenni** er stillt á *Já* eru ekki tiltækir og verða ekki notaðir þegar þessi eiginleiki er notaður.

### <a name="mobile-device-menu-items"></a>Valmyndaratriði fartækis

Tvö valmyndaratriði í fartæki eru tiltæk fyrir þennan eiginleika. Valmyndaratriðið **Taka á móti og raða klasa** er notað til að raða mótteknum birgðum í frágangsklasa við móttöku. Valmyndaratriðið **Frágangur klasa** er notað til að setja klasann í gang eftir að honum hefur verið úthlutað.

#### <a name="receive-and-sort-cluster"></a>Taka á móti og raða klasa

Stofnið nýtt valmyndaratriði fartækis til að taka á móti birgðum og raða þeim í klasa. Þetta valmyndaratriði stofnar vinnu á innleið eftir að birgðir hafa verið mótteknar, en það gefur til kynna að valmyndaratriðið móttöku verður notað fyrir frágangsklasa.

> [!NOTE]
> Hægt er að nota valmyndaratriðið **Taka á móti og raða klasa** með eftirfarandi valmyndaratriðum móttöku:
>
> - Móttaka innkaupapöntunarlínu
> - Móttaka innkaupapöntunarvöru
> - Móttaka farmvöru

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í **Haus** skal stilla eftirfarandi gildi:

    - **Heiti valmyndaratriðis:** *Taka á móti og raða klasa*
    - **Titill:** *Taka á móti og raða klasa*
    - **Máti:** *Vinna*
    - **Nota fyrirliggjandi vinnu:** *Nei*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Ferli verkstofnunar:** *Móttaka innkaupapöntunarvöru*
    - **Mynda númeraplötu:** *Já*
    - **Úthluta frágangsklasa:** *Já*

        > [!NOTE]
        > Valkosturinn **Úthluta frágangsklasa** er aðeins í boði fyrir eins skrefs aðgerðina *Ferli verkstofnunar* fyrir móttöku.

    Samþykkið sjálfgefin gildi fyrir reitina sem eftir eru.

1. Í aðgerðarúðunni skal velja **Vista**.

#### <a name="cluster-putaway"></a>Frágangur klasa

Stofnið nýtt valmyndaratriði fartækis fyrir frágang klasans eftir að honum hefur verið úthlutað.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í **Haus** skal stilla eftirfarandi gildi:

    - **Nafn valmyndaratriðis:** *Frágangsklasi*
    - **Titill:** *Frágangur klasa*
    - **Máti:** *Vinna*
    - **Nota fyrirliggjandi vinnu:** *Já*

1. Í flýtiflipanum **Almennt** skal stilla reitinn **Stjórnað af** á *Frágangur klasa*. Samþykkið sjálfgefin gildi fyrir reitina sem eftir eru.
1. Í flýtiflipanum **Vinnuklasar** skal setja upp gildan vinnuklasa fyrir þetta valmyndaratriði fartækis:

    - **Auðkenni vinnuklasa:** *Innkaup*
    - **Gerð verkbeiðni:** *Innkaupapantanir*

1. Í aðgerðarúðunni skal velja **Vista**.

### <a name="mobile-device-menu"></a>Valmynd fartækis

Bætið valmyndaratriðunum sem voru stofnuð við valmynd fyrir á innleið í farsímaforritinu.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Í valmyndarlistanum skal velja **Á innleið**.
1. Í listanum **Tiltækar valmyndir og valmyndaratriði** skal finna og velja **Taka á móti og raða klasa**.
1. Veldu hægri örvarhnappinn til að færa valda valmyndaratriðið á listann **Valmyndarskipan**.
1. Notið örvarhnappana upp/niður til að færa valmyndaratriðið á æskilegan stað í valmyndinni.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Endurtakið skref 4 til 7 til að bæta við eftirstandandi valmyndaratriðum:

    - Úthluta klasa
    - Frágangur klasa

## <a name="example-scenario"></a>Dæmi

Þessar aðstæður herma eftir ferli frágangsklasa.

### <a name="create-a-purchase-order"></a>Stofna innkaupapöntun

1. Opnið **Viðskiptaskuldir \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Sláðu inn eftirfarandi gildi í svarglugganum **Búa til innkaupapöntun**:

    - **Lánardrottnalykill:** *1001*
    - **Vöruhús:** *61*

1. Veljið **Í lagi**.

    Síðan **Allar innkaupapantanir** birtist.

1. Á síðunni **Allar innkaupapantanir**, í flýtiflipanum **Innkaupapöntunarlínur**, skal nota hnappinn **Bæta við línu** til að bæta við eftirfarandi línum:

    - Innkaupapöntunarlína 1:

        - **Vörunúmer:** *A0001*
        - **Magn:** *10*

    - Innkaupapöntunarlína 2:

        - **Vörunúmer:** *A0002*
        - **Magn:** *20*

    - Innkaupapöntunarlína 3:

        - **Vörunúmer:** *M9215*
        - **Magn:** *30*

1. Í aðgerðarúðunni skal velja **Vista**.
1. Skráið niður innkaupapöntunarnúmerið.

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a>Taka við birgðum og ganga frá úr fartæki

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a>Taka við og raða birgðum í klasa

1. Skráðu þig inn í vöruhúsaforritið sem notandi sem er virkjaður fyrir vöruhús *61*.
1. Í aðalvalmyndinni skal velja **Á innleið**.
1. Í valmyndinni **Á innleið** skal velja **Taka á móti og raða klasa**.
1. Í reitinn **Ponum** skal slá inn innkaupapöntunarnúmerið.
1. Veljið **Í lagi** (hnappurinn með gátmerki).
1. Veljið reitinn **Vara**, færið inn vörunúmer *A0001* og veljið síðan **Í lagi**.
1. Veljið reitinn **Magn**, færið inn *10* með því að nota talnaborðið og veljið síðan gátmerkishnappinn.
1. Á verksíðunni **Magn** skal velja **Í lagi** (gátmerkishnappurinn) til að staðfesta magnið sem slegið var inn.
1. Á verksíðunni **Vara** skal velja **Í lagi** til að staðfesta að varan *A0001* hafi verið færð inn.
1. Veljið reitinn **Klasakenni** og færið inn gildi til að úthluta kenni fyrir klasann sem er stofnaður.

    Kennið sem var fært inn hér verður notað þegar tvær eftirstandandi vörur í innkaupapöntuninni eru mótteknar.

1. Veljið **Í lagi**.

    Verksíðan **Ponum** birtist og sýnir skilaboðin „Vinnu lokið“.

    Vara *A0001* hefur nú verið móttekin á staðsetningu *RECV* og úthlutað á klasakenni sem fært var inn í skrefi 10.

1. Endurtakið skref 4 til 11 til að fá eftirstandandi tvær vörur úr innkaupapöntuninni og úthluta þeim á klasakennið:

    - Magn upp á *20* fyrir atriði *A0002*
    - Magn upp á *30* fyrir atriði *M9215*

#### <a name="close-the-cluster"></a>Loka klasa

Áður en hægt verður að ganga frá vörunum, verður að loka klasanum.

1. Í Supply Chain Management skal fara í **Vöruhúsakerfi \> Verk \> Á útleið \> Verkklasar**.
1. Á síðunni **Verkklasar**, í hlutanum **Verkklasi**, skal leita í reitnum **Klasakenni** að klasakenninu sem var fært inn hér á undan.
1. Ef klasinn birtist ekki, gæti þegar verið búið að loka honum. Til að komast að því hvort klasanum hafi verið lokað skal velja gátreitinn **Sýna lokað verk** og leita að klasakenninu sem fært var inn hér á undan. Fylgið síðan einu af eftirfarandi skrefum:

    - Ef klasanum hefur verið lokað skal hoppa yfir skrefin sem eftir eru í ferlinu og fara yfir í næsta ferli, [Ganga frá klasa](#put-the-cluster-away).
    - Ef klasanum hefur ekki verið lokað skal fara í gegnum skrefin sem eftir eru í þessu ferli til að loka klasanum handvirkt. Færðu þig svo yfir í næsta ferli.

1. Í hlutanum **Verkklasi** skal velja klasakennið sem fært var inn hér á undan.
1. Á aðgerðasvæðinu skal velja **Loka klasa**.

    Þegar klasanum hefur verið lokað, birtist hann ekki lengur í hlutanum **Verkklasi** (nema ef gátreiturinn **Sýna lokað verk** er valinn).

#### <a name="put-the-cluster-away"></a>Ganga frá klasa

1. Skráðu þig inn í vöruhúsaforritið sem notandi sem er virkjaður fyrir vöruhús *61*.
1. Í aðalvalmyndinni skal velja **Á innleið**.
1. Á valmyndinni **Á innleið** skal velja **Frágangur klasa**.
1. Veljið **Klasakenni** og færið inn klasakennið sem var fært inn áður fyrir lokaða klasann.
1. Veljið **Í lagi**.

    Síðan **Klasafrágangur: Tiltekt** opnast. Hún sýnir klasakennið, tiltektarstaðsetninguna, vörurnar (gildið *Margfalt* verður sýnt) og heildarmagnið í klasanum sem verður að tína.

1. Veljið **Í lagi**.

    Síðan **Klasafrágangur: Frágangur** opnast. Leiðbeiningarnar fyrir **Frágang** bera kennsl á klasakennið, frágangsstaðsetninguna, vörurnar, heildarmagnið og númeraplötukennin fyrir vörurnar sem tekið hefur verið á móti í klasanum.

    Þú ert með hefðbundnu valkostina til að hunsa eða hoppa yfir þetta skref.

    ![Frágangur klasa: Frágangssíða](media/Cluster_putaway-Put.png "Frágangur klasa: setja síðu")

1. Veljið **Í lagi** til að staðfesta frágang klasans.

    Skilaboðin „Klasa lokið“ birtast.

## <a name="notes-and-tips"></a>Athugasemdir og ábendingar

Í tilvikum þar sem klasakennið verður að yfireiningu númeraplötunnar fyrir faldað bretti, verður frágangsstaðurinn sjálfkrafa gefinn þegar klasakennið er skannað. Ekki þarf frekari skönnun númeraplötu, jafnvel þótt myndun númeraplötu sé stillt á handvirkt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]