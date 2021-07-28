---
title: Áætluð dreifing frá dreifingarstöð
description: Þetta efnisatriði lýsir háþróaðri, áætlaðri dreifingu frá dreifingarstöð þar sem birgðamagninu sem þarf til pöntunar er strax við móttöku eða stofnun beint á rétt úthlið eða sviðsetningarsvæði. Öllum eftirstandandi birgðum frá upprunastaðnum á innleið verður beint að réttum geymslustað með hefðbundnu frágangsferli.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 9c31b8dd7d69fee40ecefb6c6bc81c9c2dd17ef7
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359078"
---
# <a name="planned-cross-docking"></a>Áætluð dreifing frá dreifingarstöð

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir háþróaðri, áætlaðri dreifingu frá dreifingarstöð. Dreifing frá dreifingarstöð er vöruhúsaferli þar sem birgðamagnið sem þarf til pöntunar er strax við móttöku eða stofnun beint á rétt úthlið eða sviðsetningarsvæði. Öllum eftirstandandi birgðum frá upprunastaðnum á innleið verður beint að réttum geymslustað með hefðbundnu frágangsferli.

Dreifing frá dreifingarstöð gerir starfsmönnum kleift að sleppa frágangi á innleið og tiltekt á útleið á birgðum sem þegar eru merktar fyrir pöntun á útleið. Þar af leiðandi er dregið úr fjölda skipta sem hreyft er við birgðum, þegar slíku er við komið. Þar að auki, vegna þess að minni samskipti eru við kerfið, eykst sparnaður á tíma og rými í vinnusal vöruhússins til muna.

Áður en hægt er að keyra dreifingu frá dreifingarstöð þarf að grunnstilla nýtt sniðmát fyrir dreifingu frá dreifingarstöð, þar sem birgðauppruni og önnur skilyrði fyrir dreifingu frá dreifingarstöð eru skilgreind. Þegar pöntunin á útleið er stofnuð verður línan að vera merkt á móti pöntun á innleið sem inniheldur sama atriði. Hægt er að velja reit leiðbeiningarkóða í sniðmáti dreifingar frá dreifingarstöð á svipaðan hátt og áfyllingar og innkaupapantanir eru settar upp.

Þegar tekið er á móti pöntun á innleið, auðkennir dreifing frá dreifingarstöð sjálfkrafa þörfina fyrir dreifingu frá dreifingarstöð og býr til birgðahreyfingu fyrir það magn sem krafist er, miðað við uppsetningu staðsetningarleiðbeininga.

> [!NOTE]
> Birgðafærslur eru *ekki* óskráðar þegar hætt er við dreifingu frá dreifingarstöð, jafnvel þó að kveikt sé á stillingunni fyrir þennan eiginleika í færibreytum vöruhúsakerfisins.

## <a name="turn-on-the-planned-cross-docking-features"></a>Kveikja á áætlaðri dreifingu frá dreifingarstöð

Ef kerfið inniheldur ekki eiginleikana sem lýst er í þessu efnisatriði skal fara í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eftirfarandi eiginleikum í eftirfarandi röð:

1. *Áætluð dreifing frá dreifingarstöð*
1. *Sniðmát dreifingar frá dreifingarstöð með staðsetningarleiðbeiningum*
    > [!NOTE]
    > Þessi eiginleiki virkjar reitinn **Leiðbeiningarkóði** til að vera tilgreindur í sniðmáti dreifingar frá drefingarstöð á svipaðan hátt og áfyllingarsniðmát eru sett upp. Að virkja þennan eiginleika kemur í veg fyrir að þú bætir við leiðbeiningarkóða í sniðmátslínur dreifingar frá dreifingarstöð fyrir síðustu *Frágangslínuna*. Þetta tryggir að hægt er að ákveða lokastaðsetningu frágangs meðan á stofnun vinnu stendur áður en vinnusniðmát eru tekin til greina.

## <a name="setup"></a>Setja upp

### <a name="regenerate-load-posting-methods"></a>Endurgera bókunaraðferðir farms

Áætluð dreifing frá dreifingarstöð er útfærð sem bókunaraðferð farms. Eftir að þú hefur kveikt á eiginleikanum verður þú að endurgera aðferðirnar.

1. Opnaðu **Vöruhúsakerfi \> Uppsetning \> Bókunaraðferðir farms**.
1. Veldu **Endurgera aðferðir** á aðgerðasvæðinu.

    Þegar endurgerð er lokið ætti að birtast aðferð sem hefur **Aðferðarheitisgildið** *planCrossDocking*.

1. Lokið síðunni.

### <a name="create-a-cross-docking-template"></a>Búa til sniðmát fyrir dreifingu frá dreifingarstöð

1. Opnaðu **Vöruhúsakerfi \> Uppsetning \> Vinna \> Sniðmát dreifingar frá dreifingarstöð**.
1. Veldu **Nýtt** á aðgerðasvæðinu til að búa til sniðmát.
1. Stilla eftirfarandi gildi í hausnum:

    - **Röð:** *1*

        Þetta svæði skilgreinir röðina sem sniðmátin eru metin.

    - **Auðkenni sniðmáts fyrir dreifingu frá dreifingarmiðstöð:** *51*
    - **Lýsing:** *Vöruhús 51*
    - **Losunarregla eftirspurnar:** *Áður en tekið er við birgðum*
    - **Vöruhús:** *51*

1. Uppsetningin á flýtiflipanum **Skipulag** stýrir því hvernig sniðmátið virkar. Stilla eftirfarandi gildi:

    - **Eftirspurnarkröfur:** *Engar*

        Þetta svæði skilgreinir kröfur birgðaeftirspurnar. Ef eftirspurnin verður að vera tengd við birgðir áður en hún er losið skaltu velja *Merking*. Ef taka verður eftirspurnina frá birgðum áður en losun á sér stað, skaltu velja *Frátektarpöntun*.

    - **Gerð staðsetningar:** *Staðsetningar sendinga*

        Þetta svæði skilgreinir hvort að vinna við dreifingu frá dreifingarstöð ætti að nota sviðsetningar-/hleðslustaðsetningar sendingarinnar, eða hvort hún eigi að nota staðsetningarleiðbeiningar til að leita að eigin sviðsetningar- /hleðslustaðsetningum.

    - **Vinnusniðmát:** Skildu þetta svæði eftir autt.

        Þetta svæði skilgreinir vinnusniðmátið sem skal nota þegar vinna við dreifingu frá dreifingarstöð er búin til.

    - **Staðfesta aftur birgðarafhendingu:** *Nei*

        Þessi valkostur skilgreinir hvort staðfest skuli aftur birgðir við afhendingu. Ef þessi valkostur er stilltur á *Já* er bæði hámarkstímagluggi og dagsetningabil lokadaga athugaðir.

    - **Leiðbeiningarkóði:** Hafðu þetta svæði autt

        Þessi valkostur er virkjaður af eiginleikanum *Sniðmát dreifingar frá dreifingarstöð með staðsetningarleiðbeiningum*. Kerfið notar staðsetningarleiðbeiningar til að finna út bestu staðsetninguna til að dreifa birgðum frá dreifingarstöð. Hægt er að setja það upp með því að úthluta leiðbeiningarkóða á hvert sniðmát dreifingarstöðvar. Ef leiðbeiningarkóði er stilltur leitar kerfið í staðsetningarleiðbeiningum eftir leiðbeiningarkóða þegar vinna er búin til. Þannig er hægt að takmarka staðsetningarleiðbeiningar sem eru notaðar fyrir tiltekið sniðmát dreifingar frá dreifingarstöð.

    - **Staðfesta tímaglugga:** *Já*

        Þessi valkostur skilgreinir hvort að meta skuli hámarkstímagluga þegar birgðauppruni er valinn. Ef þessi valkostur er stilltur á *Já* verða svæðin sem tengjast hámarks- og lágmarkstímagluggum tiltækir.

    - **Hámarkstímagluggi:** *5*

        Þetta svæði skilgreinir leyfilegt hámarkstímabil á milli komu birgða og loka eftirspurnar.

    - **Eining fyrir hámarkstímaglugga:** *Dagar*
    - **Lágmarkstímagluggi:** *0*

        Þetta svæði skilgreinir leyfilegt lágmarkstímabil á milli komu birgða og loka eftirspurnar.

    - **Eining fyrir lágmarkstímaglugga:** *Dagar*
    - **Dagsetningabil lokadags:** *0*

        *Viðmið fyrir Fyrsta Lokadag Fyrst út (FEFO):* Þetta svæði skilgreinir hámarksfjölda daga á milli lokadags rununnar sem rennur fyrst út sem er núna í vöruhúsinu og rununnar sem verið er að taka á móti.

1. Á flýtiflipanum **Birgðaupprunar** skilgreinir þú birgðagerðirnar sem gilda fyrir þetta sniðmát. Veldu **Nýtt** og stilltu síðan eftirfarandi gildi:

    - **Raðnúmer:** *1*
    - **Birgðauppruni:** *Innkaupapöntun*

### <a name="create-a-work-class"></a>Stofna vinnuklasa

1. Fara í **Vöruhúsastjórnun \> Uppsetning \> Vinna \> Vinnuklasar**.
1. Veldu **Nýtt** á aðgerðasvæðinu til að búa til vinnuklasa.
1. Stilla eftirfarandi gildi:

    - **Auðkenni vinnuklasa:** *Dreifing frá dreifingarstöð*
    - **Lýsing:** *Dreifing frá dreifingarstöð*
    - **Gerð verkpöntunar:** *Dreifing frá dreifingarstöð*

### <a name="create-a-work-template"></a>Stofna sniðmát verks

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.
1. Stilltu svæðið **Gerð verkpöntunar** á *Dreifing frá dreifingarstöð*.
1. Veldu **Ný** á aðgerðasvæðinu til að bæta línu við flipann **Yfirlit**.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Raðnúmer:** *1*
    - **Vinnusniðmát:** *51 Dreifing frá dreifingarstöð*
    - **Lýsing á vinnusniðmáti:** *51 Dreifing frá dreifingarstöð*

1. Veldu **Vista** til að gera flýtiflipann **Upplýsingar um vinnusniðmát** tiltækan.
1. Á flýtiflipanum **Upplýsingar um vinnusniðmát** velur þú **Ný** til að bæta línu við hnitanetið.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Verkgerð:** *Tiltekt*
    - **Auðkenni vinnuklasa:** *Dreifing frá dreifingarstöð*

1. Veldu **Ný** til að bæta við annarri línu og stilltu eftirfarandi gildi fyrir hana:

    - **Tegund vinnu:** *Frágangur*
    - **Auðkenni vinnuklasa:** *Dreifing frá dreifingarstöð*

1. Veldu **Vista** og staðfestu að hakað sé í gátreitinn **Gilt** fyrir sniðmát *51 dreifingar frá dreifingarstöð*.

> [!NOTE]
> Vinnuklasakenni fyrir vinnugerðir *Tiltektar* og *Frágangs* verða að vera eins.

### <a name="create-location-directives"></a>Búa til staðsetningarleiðbeiningar

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.
1. Stilltu svæðið **Gerð verkpöntunar** á *Dreifing frá dreifingarstöð* í vinstri glugganum.
1. Veldu **Nýtt** á aðgerðasvæðinu og stilltu eftirfarandi gildi:

    - **Raðnúmer:** *1*
    - **Heiti:** *51 Frágangur dreifingar frá dreifingarstöð*
    - **Tegund vinnu:** *Frágangur*
    - **Svæði:** *5*
    - **Vöruhús:** *51*

1. Veldu **Vista** til að gera flýtiflipann **Línur** tiltækan.
1. Á flýtiflipanum **Línur** velur þú **Ný** til að bæta línu við hnitanetið.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Frá-magn:** *1*
    - **Til magn:** *1000000*

1. Veldu **Vista** til að gera flýtiflipann **Aðgerðir í staðsetningarleiðbeiningum** tiltækan.
1. Á flýtiflipanum **Aðgerðir staðsetningarleiðbeininga** velur þú **Ný** til að bæta við nýrri línu í hnitanetið.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Heiti:** *Útskot*
    - **Notkun fastrar staðsetningar:** *Fastar og lausar staðsetningar*

1. Veldu **Vista** til að gera hnappinn **Breyta fyrirspurn** á **Aðgerðir í staðsetningarleiðbeiningum** tækjastikunni aðgengilegan.
1. Veldu **Breyta fyrirspurn** til að opna fyrirspurnarritilinn.
1. Gakktu úr skugga um að eftirfarandi tvær línur séu stilltar á flipanum **Svið**:

    - Lína 1:

        - **Tafla:** *Staðir*
        - **Afleidd tafla:** *Staðsetningar*
        - **Svæði:** *Vöruhús*
        - **Skilyrði:** *51*

    - Lína 2:

        - **Tafla:** *Staðir*
        - **Afleidd tafla:** *Staðsetningar*
        - **Svæði:** *Staðsetning*
        - **Skilyrði:** *Útskot*

1. Veldu **Í lagi** til að loka fyrirspurnarritlinum.

### <a name="create-a-mobile-device-menu-item"></a>Stofna valmyndaratriði fartækis

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Veldu **Frágangur kaupa** í listanum yfir valmyndaratriði í glugganum til vinstri.
1. Veljið **Breyta**.
1. Á flýtiflipanum **Vinnuklasar** velur þú **Ný** til að bæta línu við hnitanetið.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Auðkenni vinnuklasa:** *Dreifing frá dreifingarstöð*
    - **Gerð verkpöntunar:** *Dreifing frá dreifingarstöð*

1. Veljið **Vista**.

## <a name="scenario"></a>Aðstæður

### <a name="create-a-purchase-order"></a>Stofna innkaupapöntun

Fylgdu eftirfarandi skrefum til að stofna innkaupapöntun sem birgðauppruna.

1. Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Sláðu inn eftirfarandi gildi í svarglugganum **Búa til innkaupapöntun**:

    - **Lánardrottnalykill:** *104*
    - **Vöruhús:** *51*

1. Veldu **Í lagi** og skráðu niður pöntunarnúmerið.
1. Nýrri línu er bætt við flýtiflipann **Innkaupapöntunarlínurnar**. Stilltu eftirfarandi gildi á þessari línu:

    - **Vörunúmer:** *A0001*
    - **Magn:** *5*

### <a name="create-a-sales-order"></a>Stofna sölupöntun

Fylgdu eftirfarandi skrefum til að stofna sölupöntun sem uppruna eftirspurnar.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - **Viðskiptavinalykill:** *US-002*
    - **Vöruhús:** *51*

1. Veljið **Í lagi**.
1. Nýrri línu er bætt við flýtiflipann **Sölupöntunarlínur**. Stilltu eftirfarandi gildi á þessari línu:

    - **Vörunúmer:** *A0001*
    - **Magn:** *3*

### <a name="create-planned-cross-docking"></a>Búa til áætlaða dreifingu frá dreifingarstöð

Fylgdu eftirfarandi skrefum til að búa til áætlaða dreifingu frá dreifingarstöð úr sölupöntuninni.

1. Á síðunni **Upplýsingar um sölupöntun** fyrir sölupöntunina sem þú varst að búa til, á aðgerðarglugganum, á flipanum **Vöruhús**, í flokknum **Aðgerðir**, velur þú **Losun í vöruhús**.

    Aðgerðin við að losa í vöruhús býr til sendingu og farmlínu á sölupöntunarlínunni og gerir tilraun til að úthluta birgðum.
    
    Þú færð upplýsingaboð. Þú færð einnig eftirfarandi viðvörunarboð: „Engin vinna var búin til fyrir bylgju XXXX. Frekari upplýsingar er að finna í erilannál vinnustofnunar“. Búist er við slíkri aðgerð vegna þess að engar birgðir eru í vöruhúsinu.

1. Á flýtiflipanum **Sölupöntunarlínur** á valmyndinni **Vöruhús** smellir þú á **Upplýsingar um sendingu**.

    Síðan **Upplýsingar sendingar** opnast og sýnir sendinguna sem stofnuð var fyrir sölupöntunina.

1. Skoðaðu flýtiflipann **Farmlínur** og athugaðu hvort að svæðið **Áætlað magn til dreifingar frá dreifingarstöð** sé stillt á *3*. Þar sem engar birgðir voru tiltækar í vöruhúsinu var magn dreifingar frá dreifingarstöð stofnað, en gildur birgðauppruni berst innan tímagluggans sem er skilgreindur í sniðmáti dreifingar frá dreifingarstöð.
1. Á flýtiflipanum **Farmlínur** velur þú **Áætlað til dreifingar frá dreifingarstöð** til að skoða frekari upplýsingar um dreifinguna frá dreifingarstöð sem var stofnuð.

## <a name="process-the-cross-docking"></a>Vinna úr dreifingu frá dreifingarstöð

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a>Móttaka innkaupapöntunar í farsímaforriti vöruhússins

Kerfið fær magnið 5 frá innkaupapöntuninni á móttökustaðinn og býr til tvær vinnueiningar.

Fyrsta vinnuauðkennið sem er búið til hefur gildi **Gerðar verkpöntunar** af gerð *Dreifingar frá dreifingarstöð* og er tengt sölupöntuninni. Það hefur magnið 3 og er beint á endanlega flutningsstaðsetningu svo hægt sé að senda hann strax út.

Annað vinnuauðkennið sem er búið til hefur gildi **Gerðar verkpöntunar** af gerð *Innkaupapantanir* og er tengt innkaupapöntuninni. Það inniheldur magnið 2 sem eftir er sem var ekki í dreifingu úr dreifingarstöð og er beint í frágang í geymslu.

1. Skráðu þig inn í fartækið sem notandi í vöruhúsi *51*.
1. Opnaðu **Á innleið \> Móttaka innkaupa**.
1. Sláðu inn innkaupapöntunarnúmer þitt á svæðin **PONum**.
1. Í reitinn **Magn** skaltu slá inn *5*.
1. Veljið **Í lagi**.
1. Á næstu síðu skaltu stilla svæðið **Atriði** á *A0001*.
1. Veljið **Í lagi**.
1. Á næstu síðu staðfestir þú gildi **Sölupöntunarnúmersins**, **Atriðsins** og **Magnsins** með því að velja **Í lagi**.

    Skilaboðin „Vinnu er lokið“ birtast.

1. Veldu **Hætta við** til að hætta.

### <a name="put-away-to-cross-docking-and-bulk"></a>Frágangur dreifingar frá dreifingarstöð og magns

Sem stendur hafa bæði vinnuauðkennin sömu marknúmeraplötu. Til að ljúka næstu skrefum verðurðu að fá vinnuauðkenni og marknúmeraplötu. Þú færð þessar upplýsingar úr upplýsingum um innkaupapöntunarlínu og sölupöntunarlínu. Að öðrum kosti er hægt að fara í **Vöruhúsakerfi \> Vinna \> Upplýsingar um vinnu** og sía fyrir vinnu þar sem gildi **Vöruhúss** er *51*.

1. Farðu í fatækið og farðu í **Á innleið \> Frágangur innkaupa** og sláðu inn marknúmeraplötu vinnunnar.
1. Í svæðið **Auðkenni** skaltu slá inn auðkenni marknúmeraplötunnar úr upplýsingunum um vinnu.

    Tiltektarsíða dreifingar frá dreifingarstöð birtir tiltektarstaðsetninguna (*RECV*), marknúmeraplötuna (*númeraplata*), atriði (*A0001*) og magn (*3*).

1. Veljið **Í lagi**.
1. Í reitinn **Marknúmeraplata** skal færa inn kenni marknúmeraplötuna fyrir auðkenni númeraplötunnar sem skal koma fyrir (dreifa frá dreifingarstöð) til sendingarstaðsetningarinnar. Hægt er að velja hvaða auðkenni númeraplötu sem er.
1. Veljið **Í lagi**.
1. Á næstu síðu á svæðinu **Auðkenni** slærðu inn auðkenni marknúmeraplötunnar.
1. Veljið **Í lagi**.
1. Staðfestu vinnuna fyrir tiltektina á magninu sem eftir er 2 og veldu síðan **Í lagi**.
1. Veldu **Lokið** á næstu síðu til að ljúka tiltektarferlinu og hefja frágangsferlið.

    Farsímaforritið birtir staðsetninguna og númeraplötuna til að setja atriðið á.

1. Staðfestu **Frágang** magngeymslu með því að velja **Í lagi**.
1. Staðfestu **Frágang** dreifingar frá dreifingarstöð á næstu síðu með því að velja **Í lagi**.

    Skilaboðin „Vinnu er lokið“ birtast.

1. Veldu **Hætta við** til að hætta.

Eftirfarandi skýringarmynd sýnir hvernig vinna við dreifingu frá dreifingarstöð gæti birst í Microsoft Dynamics 365 Supply Chain Management.

![Vinnu við dreifingu frá dreifingarstöð er lokið.](media/PlannedCrossDockingWork.png "Vinnu við dreifingu frá dreifingarstöð er lokið")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]