---
title: Blöndun á afurðarvídd staðsetningar
description: Þetta efnisatriði inniheldur upplýsingar um blöndun á afurðarvídd staðsetningar. Þessi virkni staðsetningarforstillingar hjálpar til við að bæta staðsetningarstjórnun þegar afurðarafbrigði eða afurðir með víddir eru notaðar, svo sem í tískuiðnaðinum. Það gerir þér kleift að ákveða hvort hægt sé að blanda stillingum, litum, stílum og stærðum fyrir tiltekna staðsetningarforstillingu, eða hvort hægt sé að setja eina af þessum víddum eða samsetningu þeirra á sömu staðsetninguna.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 73519f3fe79d3d7d917d3044255f735640b8ccfd
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430656"
---
# <a name="location-product-dimension-mixing"></a>Blöndun á afurðarvídd staðsetningar

[!include [banner](../includes/banner.md)]

Blöndun á afurðarvídd staðsetningar er staðsetningarforstilling sem hjálpar til við að bæta staðsetningarstjórnun þegar afurðarafbrigði eða afurðir með víddir eru notaðar, svo sem í tískuiðnaðinum. Það gerir þér kleift að ákveða hvort hægt sé að blanda stillingum, litum, stílum og stærðum fyrir tiltekna staðsetningarforstillingu, eða hvort hægt sé að setja eina af þessum víddum eða samsetningu þeirra á sömu staðsetninguna.

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a>Kveikja á eiginleika blöndunar á afurðarvídd staðsetningar

Áður en þú getur notað blöndun á afurðarvídd staðsetningar verður að kveikja á eiginleikanum í kerfinu þínu. Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Þar er eiginleikinn sýndur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Blöndun á afurðarvídd staðsetningar*

## <a name="setup"></a>Setja upp

Hver staðsetning í vöruhúsi verður að hafa staðsetningarforstillingu tengda sem lýsir eiginleikum staðsetningar. Þess vegna verður hægt að blanda vöruvídd allra staðsetningar sem nota sömu staðsetningarforstillingu eftir að hún hefur verið sett upp.

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a>Stilla staðsetningarforstillingar til að leyfa blöndun á afurðarvídd

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Forstillingar staðsetningar**.
1. Smelltu á **MAGN** á lista staðsetningarforstillinga.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Á flýtiflipanum **Almennt** skaltu stilla valkostinn **Virkja tiltekna blöndun á afurðarvídd staðsetningar** á *Já*.

    > [!NOTE]
    > Þú getur aðeins stillt valkostinn á *Já* ef valkosturinn **Leyfa blandaðar afurðir** er stilltur á *Nei*.

1. Á flýtiflipanum **Leyfð blöndun á afurðarvídd** skaltu stilla valkostinn **Stærð** á *Já*. Við aðstæðurnar sem lýst er í þessu efnisatriði er aðeins hægt að blanda afurðum sem hafa mismunandi **Stærðarvíddir**. Aðrir valkostir eru einnig í boði.
1. Veljið **Vista**.

### <a name="create-a-new-product-master-and-product-variants"></a>Stofna nýtt afurðarsniðmát og ný afurðarafbrigði

1. Opna **upplýsingar um afurðastjórnun \> Afurðir \> Afurðarsniðmát**.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að stofna nýtt afurðarsniðmát.
1. Sláið inn eftirfarandi gildi í svarglugganum **Ný afurð**:

    - **Gerð afurðar:** *Afurð*
    - **Undirgerð afurðar:** *Afurðarsniðmát*
    - **Afurðarnúmer:** *B0001*
    - **Afurðarheiti:** *B0001 Stærð*
    - **Afurðavíddaflokkur:** *Stærð*
    - **Skilgreiningartækni:** *Forskilgreint afbrigði*

1. Veljið **Í lagi**.
1. Stilltu eftirfarandi gildi á síðunni **Upplýsingar um afurð** á flýtiflipanum **Almennt**:

    - **Búa til afbrigði sjálfkrafa** *Já*
    - **Stærðarflokkur:** *CASUALDHIR*

1. Til að skoða forskilgreind afbrigði skaltu velja **Afurðarafbrigði** á aðgerðarsvæðinu.

    Síðan **Afurðarafbrigði** opnast og sýnir lista yfir afbrigði grunnstillingar stærðarflokksins.

### <a name="release-products-to-the-usmf-company"></a>Losa afurðir til USMF-fyrirtækisins

1. Smelltu á **Losa afurðir** á aðgerðasvæðinu.
1. Staðfestu á **Velja afurðir til losunar** að afurðarnúmer *B0001* sé á listanum og smelltu síðan á **Áfram**.
1. Smelltu á **Áfram** til að staðfesta afurðarafbrigði sem á að losa um.
1. Á síðunni **Velja fyrirtæki sem á að losa til** skaltu smella á *USMF* og síðan smella á **Áfram** til að staðfesta valið.
1. Á síðunni **Staðfesta val** smellir þú á **Ljúka** til að losa um.

    Þú færð skilaboðin „Aðgerð er lokið“.

### <a name="update-a-released-product-in-the-usmf-company"></a>Uppfæra afurð sem losað var um í USMF-fyrirtækinu

1. Gakktu úr skugga um að þú sért skráð(ur) inn á **USMF**-fyrirtækið.
1. Opnaðu **Afurðaupplýsingastjórnun \> Afurðir \> Losaðar afurðir** til að ljúka við að búa til losuðu afurðina.
1. Leitaðu að og veldu vörunúmer *B0001* til að opna síðuna **Upplýsingasíða um losaðar afurðir**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Á flýtiflipanum **Almennt** skal gæta þess að stilla svæðið **Vörulíkanaflokkur** á *FIFO*.
1. Á aðgerðasvæðinu, á flipanum **Afurð** í hópnum **Uppsetning** skal velja **Víddaflokka**.
1. Stilla eftirfarandi gildi:

    - **Geymsluvíddarflokkur:** *Afurð*
    - **Rakningarvíddarflokkur:** *Enginn*

1. Veljið **Í lagi**.
1. Á aðgerðasvæðinu, á flipanum **Afurð** í hópnum **Uppsetning** skal velja **Frátekningarstigveldi**.
1. Stilltu svæðið **Frátekningarstigveldi** á *Sjálfgefið* og smelltu síðan á **Í lagi**.
1. Athugaðu á flýtiflipanum **Almennt** í hlutanum **Stjórnun** hvort að valkostir þinir hafi verið uppfærðir.
1. Í flýtiflipanum **Kaup** í svæðinu **Verð** slærðu inn *10*.
1. Á flýtiflipanum **Stjórna kostnaði**, í reitnum **Vöruflokkur** skal slá inn *Hljóð*.
1. Í flýtiflipanum **Kaup** í svæðinu **Verð** slærðu inn *10*.
1. Á flýtiflipanum **Vöruhús** á svæðinu **Auðkenni röðunarflokks einingar** skaltu slá inn *ea*.
1. Veljið **Vista**.

### <a name="create-a-location-directive"></a>Stofna staðsetningarleiðbeiningar

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.
1. Í svæðinu **Gerð verkbeiðni** í vinstri glugganum velur þú *Innkaupapantanir*.
1. Veldu staðsetningarleiðbeiningar sem kallast *24 PO Direct* á listanum.
1. Á flýtiflipanum **Aðgerðir staðsetningarleiðbeininga** velur þú **Ný** til að bæta við nýrri línu í hnitanetið.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Raðnúmer:** *1*

        Nýja línan ætti að vera fyrir framan línuna sem fyrir er. Til að gera breytinguna skaltu nota hnappana **Færa upp** og **Færa niður** á tækjastikunni eða breyta **Raðnúmeragildi** núverandi línu í *2*.

    - **Heiti:** *Setja í staðsetningarforstillingu MAGNS*
    - **Notkun fastrar staðsetningar:** *Fastar og lausar staðsetningar*
    - **Leyfa neikvæðar birgðir:** *Hreinsa þennan gátreit (=Nei)*
    - **Runa virk:** *Hreinsa þennan gátreit (=Nei)*
    - **Áætlun:** *Engin*

1. Meðan nýja línan er enn valin skaltu velja **Breyta fyrirspurn** fyrir ofan hnitanetið.
1. Í svarglugga ritilsins á flipanum **Svið** velur þú **Bæta við** til að bæta línu við hnitanetið.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Tafla:** *Staðir*
    - **Afleidd tafla:** *Staðsetningar*
    - **Reitur:** *Auðkenni forstillingar staðsetningar*
    - **Skilyrði:** *BULK*

1. Veljið **Í lagi**.
1. Á síðunni **Staðsetningarleiðbeiningar** á aðgerðasvæðinu velur þú **Vista**.

> [!NOTE]
> Á flýtiflipanum **Aðgerðir staðsetningarleiðbeiningar** á svæðinu **Áætlun** ef notuð er staðsetningarleiðbeiningarnar *Sameina* er uppsetning á flýtiflipanum **Leyfðar blandanir afurðarvíddar** á **Staðsetningarforstillingum** hunsuð og afurðir settar í sömu staðsetningu, þó að uppsetning leyfi ekki slíka aðgerð.

### <a name="create-a-mobile-device-menu-item"></a>Stofna valmyndaratriði fartækis

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að stofna nýtt valmyndaratriði til að nota við flokkun.
1. Stilla eftirfarandi gildi í hausnum:

    - **Heiti valmyndaratriðis:** *Móttaka innkaupapöntunarlínu*
    - **Titill:** *Móttaka innkaupapöntunarlínu*
    - **Máti:** *Vinna*
    - **Nota fyrirliggjandi vinnu:** *Nei*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Stofnunarferli vinnu:** *Móttaka og frátekning innkaupapöntunarlínu*
    - **Mynda númeraplötu:** *Já*

1. Veljið **Vista**.

### <a name="configure-the-mobile-device-menu"></a>Grunnstilling valmyndar fartækisins

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.
1. Veldu **Á innleið** á valmyndinni.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Á listanum **Tiltækar valmyndir og valmyndaratriði** skaltu finna og velja valmyndaratriðið **Móttaka innkaupapöntunarlínu**.
1. Smelltu á hægri örvarhnappinn til að færa valmyndaratriðið **Móttaka innkaupapöntunarlínu** yfir á listann **Valmyndarskipan**. Á þennan hátt bætirðu nýjum valmyndaratriðum við valda valmynd.
1. Veljið **Vista**.

## <a name="scenario"></a>Aðstæður

Þessar sýniaðstæður sýna hvernig hægt er að setja tvö mismunandi afurðarafbrigði á sömu staðsetningu þegar staðsetningarforstillingin leyfir ekki blandaða hluti, en eiginleikinn *Blöndun á afurðarvídd staðsetningar* er virkur. Í þessu tilfelli muntu nota **stærðarafbrigðið** sem viðmiðun.

Áður en þú byrjar skaltu ganga úr skugga um að tómar staðsetningar séu til staðar í vöruhúsi *24* sem nota staðsetningarforstillinguna *MAGN*.

### <a name="create-a-purchase-order"></a>Stofna innkaupapöntun

Þú verður að búa til innkaupapöntun sem hefur þrjár línur: tvær línur fyrir sama afurðarnúmer en mismunandi **stærðarafbrigði** og þriðja lína fyrir aðra afurð sem hefur engin afbrigði.

1. Opnið **Viðskiptaskuldir \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Sláðu inn eftirfarandi gildi í svarglugganum **Búa til innkaupapöntun**:

    - **Lánardrottnalykill:** *1001*
    - **Vöruhús:** *24*

1. Veljið **Í lagi**.
1. Innkaupapöntunin er búin til og ný lína er bætt við flýtiflipann **Innkaupapöntunarlínur**. Skráið niður innkaupapöntunarnúmerið.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Vörunúmer:** *B0001*
    - **Stærð** *L*
    - **Magn:** *2*

1. Veldu **Bæta við línu** fyrir ofan hnitanetið til að bæta við annarri innkaupapöntunarlínu og stilltu eftirfarandi gildi:

    - **Vörunúmer:** *B0001*
    - **Stærð** *XL*
    - **Magn:** *2*

1. Veldu **Bæta við línu** til að bæta við þriðju innkaupapöntunarlínu og stilltu eftirfarandi gildi:

    - **Vörunúmer:** *A0001*
    - **Magn:** *1*

1. Veljið **Vista**.

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a>Taka á móti innkaupapöntunarlínum í vöruhúsaforritinu

1. Skráðu þig inn í vöruhúsaforritið sem notandi sem er virkjaður fyrir vöruhús *24*.
1. Veldu valmyndina **Á innleið**.
1. Veldu **Móttaka innkaupapöntunarlínu**.
1. Veldu svæðið **PONUM** og sláðu síðan inn númer innkaupapöntunar.
1. Staðfestu innsláttinn með því að smella á staðfestingarhnappinn (✔) neðst á síðunni.
1. Sláðu inn línunúmerið í innkaupapöntuninni sem verið er að taka á móti. Veldu svæðið **LINENUM** og sláðu inn *1* með talnaborðinu.
1. Staðfestu færsluna.
1. Færðu inn magnið sem á að taka við. Veldu hnappinn með plúsmerkinu (**+**) tvisvar til að hækka gildið á svæðinu **Magn** í *2*.
1. Skráðu færsluna þína með því að velja hnappinn (✔) neðst á síðunni og staðfestu síðan færsluna með því að velja hnappinn (✔) aftur.
1. Skoða upplýsingar á síðunni **Innkaupapantanir: Frágangur**. Þessi síða birtir vinnuna sem var stofnuð fyrir fráganginn (Vinna 1).

    Birt er staðsetningin sem gengið er frá móttekinni afurð, númeraplatan, afurðin, stærðin og magn verksins **Móttaka innkaupapöntunarlínu** sem nýlokið var við.

1. Staðfestu vinnuna við frágang.
1. Endurtakið skref 4 til 11 fyrir innkaupapöntunarlínu 2. Hins vegar tilgreinir þú magn *1* í skrefi 8.

    Ný vinna við frágang (Vinna 2) er búin til fyrir sömu staðsetningu og Vinna 1.

1. Endurtakið skref 4 til 11 aftur fyrir innkaupapöntunarlínu 2. Í þrepi 8, tilgreindu magnið sem eftir er af *1*.

    Ný vinna við frágang (Vinna 3) er búin til fyrir sömu staðsetningu og Vinna 1 og Vinna 2. Þessi aðgerð verður vegna þess að staðsetningarleiðbeiningar um *Sameiningu* eru notaðar og uppsetningin á flýtiflipanum **Leyfð blöndun á afurðarvídd** á *staðsetningarforstillingum* **Magns** leyfir blöndun á afbrigðinu **Stærð** á staðsetningu.

1. Endurtakið skref 4 til 11 fyrir innkaupapöntunarlínu 3. Í þrepi 8, tilgreindu magn *1* fyrir afurðarnúmer *A0001*.

    Ný vinna við frágang (Vinna 4) er búin til fyrir aðra staðsetningu en staðsetningin sem er notuð fyrir innkaupapöntunarlínur 1 og 2. Þessi aðgerð verður vegna þess að staðsetningarforstillingin leyfir ekki blandaðar afurðir, en það gerir ráð fyrir blönduðum víddum sama afurðarsniðmáts.

1. Veldu valmyndarhnappinn efst á síðunni (stundum kallaður hamborgari eða hamborgarahnappur) og veldu síðan **Hætta við** til að loka **Móttöku innkaupapöntunarlínu**.

> [!TIP]
> Þú getur endurtekið þessar aðstæður, en í þetta sinn skaltu stilla **Stærð** - *Nei* fyrir neðan **Leyfa blöndun á afurðarvídd** flýtiflipann á *Staðsetningarforstillingar* **Magns**, þannig að ekki sé hægt að blanda saman afurðarvíddum. Í þessu tilfelli, þegar þú færð innkaupapöntunina, verður hvert afurðarafbrigði sett á nýja staðsetningu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]