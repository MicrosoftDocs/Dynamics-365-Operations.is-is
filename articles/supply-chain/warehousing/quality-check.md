---
title: Gæðaskoðun
description: Þessi grein veitir upplýsingar um eiginleikann gæðaeftirlit. Þessi eiginleiki gerir starfsmönnum vöruhúss kleift að gera stuttar skoðanir á staðnum á meðan þeir taka á móti vörum á svæði innhliðs.
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: bc0e911eeccd1d4700f1f4daefd5fe1a4935cd80
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218713"
---
# <a name="quality-check"></a>Gæðaskoðun

[!include [banner](../includes/banner.md)]

Eiginleikinn *Gæðaskoðun* gerir starfsmönnum vöruhúss kleift að gera flýtiskoðanir á staðnum á meðan þeir taka á móti vörum á svæði innhliðs. Þessar skoðanir á staðnum eru gagnlegar þegar starfsmenn skoða pakkningar eða aðra hluta vöru sem auðvelt er að skoða. Eiginleikinn biður starfsmenn um að gera stutta skoðun til að sjá hvort eitthvað er augljóslega ekki í lagi eða skemmt áður en birgðunum er komið fyrir á lager í frágangsstaðsetningunni.

Þessi eiginleiki getur komið í stað hefðbundins gæðaskoðunarferlis. Hann býður upp á meiri sveigjanleika og hraðari úrvinnslu.

Þegar þessi eiginleiki er notaður fer koman og gæðaskoðun fram á eftirfarandi hátt:

1. Þegar sending kemur, mun starfkraftur í vöruhúsi skrá komuna. Starfsmaðurinn skannar einnig númeraplötu til að skrá staðsetninguna.
1. Starfsmaðurinn gerir stutta gæðaskoðun og skráir niðurstöðuna (stóðst eða stóðst ekki) fyrir þessa númeraplötu.
1. Ein af eftirfarandi aðgerðum á sér stað:

    - Ef gæðaskoðunin var í lagi er númeraplatan samþykkt og henni beint á móttökustaðsetningu eins og venjulega.
    - Ef gæðaskoðun var ekki í lagi er númeraplötunni hafnað og fyrirliggjandi frágangsvinna hennar er framsend á aðra staðsetningu til að gangast undir frekara eftirlit. Ný gæðapöntun er stofnuð. Til að skoða gæðapöntunina sem stofnuð er út frá gæðaskoðuninni sem var ekki í lagi er farið í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Gæðapantanir**.

Einnig er hægt að setja þetta ferli upp þannig að allar skannaðar númeraplötur séu fluttar á staðsetningu gæðaskoðunar.

## <a name="turn-the-quality-check-feature-on-or-off"></a>Kveiktu eða slökktu á eiginleikanum gæðaeftirlit

Til að nota virknina sem lýst er í þessari grein, *Gæðaskoðun* kveikt verður á eiginleikanum fyrir kerfið þitt. Frá og með Supply Chain Management 10.0.25 er þessi eiginleiki skylda og ekki hægt að slökkva á honum. Ef þú ert að keyra útgáfu eldri en 10.0.25 geta stjórnendur kveikt eða slökkt á þessari virkni með því að leita að *Gæðaskoðun* eiginleiki í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnurými.

## <a name="set-up-the-feature-for-the-example-scenario"></a>Setja upp eiginleikann fyrir þetta sýnidæmi

Þessi hluti veitir leiðbeiningar og dæmi sem sýnir hvernig á að setja upp *Gæðaskoðun* lögun og undirbúa sýnishornsgögn fyrir dæmið sem er að finna síðar í þessari grein.

### <a name="make-sample-data-available"></a>Gera sýnigögn tiltæk

Til að vinna í gegnum [sýniaðstæðurnar](#example-scenario) með því að nota sýnskrárnar og sýnigildin sem eru kynnt í þessu efnisatriði verður þú að vinna á kerfi þar sem venjulegu [sýnigögnin](../../fin-ops-core/fin-ops/get-started/demo-data.md) eru sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

### <a name="quality-check-template"></a><a name="quality-template"></a>Sniðmát gæðaskoðunar

Sniðmát gæðaskoðunar skilgreinir reglurnar fyrir gæðaskoðun á staðnum við móttöku.

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Sniðmát gæðaskoðunar**.
1. Veljið **Nýtt** til að bæta sniðmáti við hnitanetið.
1. Stillið eftirfarandi gildi til að skilgreina nýja sniðmátið:

    - **Heiti sniðmáts gæðaskoðunar:** *Móttökuskoðun*

        Sláið inn heiti sem auðkennir reglurnar sem eru notaðar fyrir þetta sniðmát.

    - **Samþykktarregla:** *Birta notanda kvaðningu*

        Tilgreinið hvort notendur eigi að fá kvaðningu um að samþykkja eða hafna gæðum birgða meðan þeir vinna verkið eða hvort gæðunum skuli sjálfkrafa hafnað. Tiltækir valmöguleikar eru *Sjálfvirk höfnun* og *Birta notanda kvaðningu*.

    - **Vinnuregla gæðamála:** *Stofna gæðapöntun*

        Veljið regluna sem á að nota þegar gæðum birgða er hafnað. Eftirtaldir valkostir eru í boði:

        - *Stofna vinnu eingöngu* – Eingöngu stofna vinnu til að auðvelda birgðahreyfingu.
        - *Stofna gæðapöntun* – Stofna gæðapöntun til að auðvelda gæðaprófanir.

    - **Prófunarflokkur:** *Lokað rými*

        Tilgreinið prófunarflokkinn sem á að nota í gæðapöntun sem er stofnuð. Prófunarflokkar eru settir upp í einingunni **Birgðastjórnun**.

        Hafið slökkt á valkostinum **Förgunartexti** fyrir prófunarflokkinn. Þessi valkostur skilgreinir hvort farga skuli sýninu sem hluti af prófunum innan prófunarflokksins. Ef prófun með förgun er notuð býr kerfið til birgðafærslu þegar gæðapöntun er stofnuð fyrir vöru. Ný birgðafærslu spáir fyrir um birgðalækkun fyrir prófunarmagnið. Birgðaminnkun á sér stað þegar gæðapöntun lýkur í gegnum staðfestingarskrefið. Birgðafærslan er auðkennd sem gæðapöntun.

### <a name="work-class--quality-check"></a><a name="work-class"></a>Vinnuklasi – Gæðaskoðun

Vinnuklasar eru notaðir til að beina og/eða takmarka gerð vinnupöntunarlína sem starfskraftur í vöruhúsi getur unnið í farsíma.

1. Fara í **Vöruhúsastjórnun \> Uppsetning \> Vinna \> Vinnuklasar**.
1. Veljið **Nýr** til að búa til vinnuklasa.
1. Stilla eftirfarandi gildi í hausnum:

    - **Auðkenni vinnuklasa:** *Gæðaeftirlit*

        Sláið inn heiti sem auðkennir vinnuklasann.

    - **Lýsing:** *Gæðaeftirlit*

        Færið inn stutta lýsingu sem gefur til kynna hvað vinnuklasinn er notaður fyrir.

    - **Gerð verkbeiðni:** *Gæði í gæðaskoðun*

        Veljið gerð verkbeiðni sem vinnuklasinn stofnar. Þegar gæðastjórnunarvinna er sett upp skal alltaf velja *Gæði í gæðaskoðun*.

1. Í flýtiflipanum **Gildar gerðir frágangsstaðsetningar** skal skilja reitinn **Gerð staðsetningar** eftir auðan.

    Ef valin er staðsetningargerð, eru staðsetningarnar takmarkaðar þar sem hægt er að setja vörur eftir að þær hafa verið tíndar. Þessi reitur er notaður þegar staðsetningarleiðbeiningar reynir að leysa úr staðsetningu, eða ef starfsmaður vöruhússins tilgreinir staðsetningu handvirkt fyrir valmyndaratriði fartækis.

Frekari upplýsingar um vinnuklasa og hvernig á að stofna þá er að finna í [Stofna vinnuklasa](tasks/create-work-class.md).

### <a name="work-template"></a>Vinnusniðmát

Vinnusniðmát gerir það mögulegt að skilgreina vinnsluaðgerðir sem þarf að framkvæma í vöruhúsinu. Yfirleitt samanstanda vinnsluaðgerðir vöruhúss af aðgerðarpari: starfsmanns í vöruhúsi tekur til lagerbirgðir á einni staðsetningu og setur síðan tíndu birgðirnar niður á annarri staðsetningu. Vinnusniðmát fyrir gæðastjórnun skilgreinir vinnuaðgerðir fyrir athugun á gæðum.

#### <a name="purchase-orders"></a>Innkaupapantanir

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.
1. Í hausnum skal stilla reitinn **Gerð verkbeiðni** á *Innkaupapantanir*.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Veljið vinnusniðmát sem á að innihalda skref gæðaskoðunar. Í hlutanum **Yfirlit**, í reitnum **Vinnusniðmát**, skal velja *51 Innhreyfing innkaupapöntunar*.
1. Athugið að í hlutanum **Upplýsingar vinnusniðmáts** er hnitanetið með tvær línur fyrir: eina fyrir *Tiltekt* og hina fyrir *Frágang*.
1. Í hlutanum **Upplýsingar vinnusniðmáts** skal velja **Ný** til að bæta línu fyrir gæðastjórnun við hnitanetið. Takið eftir að reiturinn **Línunúmer** fyrir nýju línuna er stilltur á *3*.
1. Stilltu eftirfarandi gildi á nýju línunni. Samþykkið sjálfgefin gildi fyrir reitina sem eftir eru.

    - **Vinnugerð:** *Gæðaskoðun*
    - **Auðkenni vinnuklasa:** *Innkaup*
    - **Heiti sniðmáts gæðaskoðunar:** *Móttökuskoðun*

        Veljið einkvæmt auðkenni fyrir vinnuklasann. Nota þetta gildi til að skilgreina valmyndaratriðin á fartækið og gerðir vinnu sem hægt er að vinna þessar valmyndaratriði.

1. Á aðgerðasvæðinu skal velja **Vista** til að vista vinnuna sem er komin.

    Upplýsingaboð birtast þar sem stendur: „Ógilt - Gæðaskoðun verður að koma strax á eftir tiltekt.“ Þess vegna þarf að breyta gildinu fyrir **Línunúmer** fyrir línuna sem var bætt við.

1. Fylgið þessum skrefum til að breyta gildinu fyrir **Línunúmer** fyrir nýju línuna:

    1. Í hlutanum **Upplýsingar vinnusniðmáts** skal velja línuna þar sem reiturinn **Vinnugerð** er stilltur á *Gæðaskoðun*.
    2. Veljið hnappinn **Færa upp** eða **Færa niður** til að færa línuna *Gæðaskoðun* þannig að hún komi á eftir línu *Tiltektar*.

1. Í aðgerðarúðunni skal velja **Vista**.

#### <a name="quality-in-quality-check"></a>Gæði í gæðaskoðun

Næst skal stofna vinnusniðmát fyrir gæðaskoðun.

1. Í haus síðunnar **Vinnusniðmát** skal breyta gildinu í reitnum **Gerð verkbeiðni** í *Gæði í gæðaskoðun*.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið í hlutanum **Yfirlit**.
1. Í nýju línunni skal stilla eftirfarandi gildi:

    - **Vinnusniðmát:** *51 Gæðaskoðun*

        Færa skal inn heiti á sniðmátið.

    - **Lýsing á vinnusniðmáti:** *51 Gæðaskoðun*

1. Á aðgerðasvæðinu skal velja **Vista** til að gera hlutann **Upplýsingar um vinnusniðmát** tiltækan.
1. Á meðan nýja sniðmátið er enn valið í hlutanum **Yfirlit**, skal velja **Ný** í hlutanum **Upplýsingar um vinnusniðmát** til að bæta línu við hnitanetið þar.
1. Í nýju línunni skal stilla eftirfarandi gildi:

    - **Verkgerð:** *Tiltekt*
    - **Auðkenni vinnuklasa:** *Gæðaeftirlit*

        Veljið heiti [vinnuklasans](#work-class) sem var stofnaður hér á undan fyrir vinnu gæðastjórnunar.

1. Í hlutanum **Upplýsingar um vinnusniðmát** skal aftur velja **Ný** til að bæta við annarri línu.
1. Í nýju línunni skal stilla eftirfarandi gildi:

    - **Tegund vinnu:** *Frágangur*
    - **Auðkenni vinnuklasa:** *Gæðaeftirlit*

        Veljið heiti [vinnuklasans](#work-class) sem var stofnaður hér á undan fyrir vinnu gæðastjórnunar.

1. Í aðgerðarúðunni skal velja **Vista**.

Frekari upplýsingar um vinnusniðmát er að finna í [Stýra vöruhúsavinnu með vinnusniðmátum og staðsetningarleiðbeiningum](control-warehouse-location-directives.md)

### <a name="location-directive--quality-failures"></a>Staðsetningarleiðbeining – Stenst ekki gæði

Staðsetningarleiðbeiningar eru reglur sem hjálpa við auðkenningu tiltektar- og frágangsstaðsetninga fyrir birgðahreyfingar. Til dæmis, í sölupöntunarfærslu, ákvarða staðsetningarleiðbeiningar hvar vörurnar verða teknar til og hvar tilteknar vörur verða að setja. Setja þarf á reglu staðsetningarleiðbeiningar til að skilgreina hvernig meðhöndla á það sem stenst ekki gæðaskoðun.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.
1. Á svæðinu vinstra megin skal stilla reitinn **Gerð verkbeiðni** á *Innkaupapantanir* til að vinna með staðsetningarleiðbeiningar af þeirri gerð.
1. Á aðgerðasvæðinu skal velja **Ný** til að búa til staðsetningarleiðbeiningu fyrir gæðaskoðanir.
1. Stilla eftirfarandi gildi í hausnum:

    - **Raðnúmer:** Samþykkja sjálfgildið.
    - **Heiti:** *51 til gæðaskoðunar*

1. Stilltu eftirfarandi gildi á flýtiflipanum **staðsetningarleiðbeiningar**. Samþykkið sjálfgefin gildi fyrir reitina sem eftir eru.

    - **Tegund vinnu:** *Frágangur*
    - **Svæði:** *5*
    - **Vöruhús:** *51*

1. Í aðgerðasvæðinu skal velja **Vista** til að vista leiðbeininguna og gera flýtiflipann **Línur** tiltækan.
1. Á flýtiflipanum **Línur** velur þú **Ný** til að bæta línu við hnitanetið.
1. Stilltu eftirfarandi gildi á nýju línunni. Samþykkið sjálfgefin gildi fyrir reitina sem eftir eru.

    - **Frá-magn:** *1*
    - **Til magn:** *1000000*

1. Á aðgerðasvæðinu skal velja **Vista** til að vista nýju línuna og gera flýtiflipann **Aðgerðir í staðsetningarleiðbeiningum** tiltækan.
1. Á meðan nýja línan er enn valin í flýtiflipanum **Línur**, skal velja **Ný** í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** til að bæta línu við hnitanetið þar, þannig að hægt sé að setja upp aðgerð fyrir línuna.
1. Í nýju línunni skal stilla reitinn **Heiti** á *Gæði*. Samþykkið sjálfgefin gildi fyrir reitina sem eftir eru.
1. Á aðgerðasvæðinu skal velja **Vista** til að gera hnappinn **Breyta fyrirspurn** í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** tiltækan.
1. Á meðan línan sem var bætt við er enn valin í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum**, skal velja **Breyta fyrirspurn** til að opna svarglugga þar sem hægt er að breyta fyrirspurninni fyrir aðgerðina.
1. Í flipanum **Svið** skal velja **Bæta við** til að bæta línu við fyrirspurnina.
1. Í nýju línunni skal stilla eftirfarandi gildi:

    - **Tafla:** *Staðir*
    - **Afleidd tafla:** *Staðsetningar*
    - **Svæði:** *Staðsetning*
    - **Skilyrði:** *QMS*

    Staðsetning *QMS* er vöruhúsastaðsetning fyrir gæði.

1. Veldu **Í lagi** til að loka svarglugganum.
1. Nú þarf að breyta röðinni á staðsetningarleiðbeiningum innkaupapöntunar fyrir vöruhús *51*. Vistið nýju staðsetningarleiðbeininguna *51 Til gæðaskoðunar*, uppfærið síðuna, og veljið staðsetningarleiðbeininguna í listanum. Notið síðan hnappana **Færa upp** og **Færa niður** á aðgerðasvæðinu til að ganga frá staðsetningarleiðbeiningunni fyrir vöruhús *51* í eftirfarandi röð. (Áður en valið er **Færa upp** eða **Færa niður** þarf að velja staðsetningarleiðbeiningu í listanum.)

    1. 51 Til gæðaskoðunar
    2. 51 PO Direct
    3. 51 QMS

### <a name="mobile-device-menu-items"></a>Valmyndaratriði fartækis

Skilgreinið valmyndaratriði þannig að fartæki geti framkvæmt aðgerðina **Gæðaskoðun**.

#### <a name="purchase-putaway"></a>Frágangur innkaupa

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Í listanum skal velja valmyndaratriðið **Frágangur innkaupa**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Í hlutanum **Vinnuklasar** skal velja **Ný** til að bæta línu við hnitanetið.
1. Í nýju línunni skal stilla eftirfarandi gildi:

    - **Auðkenni vinnuklasa:** *Gæðaeftirlit*

        Færið inn heiti [vinnuklasans](#work-class) sem var stofnaður hér á undan fyrir vinnu gæðastjórnunar.

    - **Gerð verkbeiðni:** *Gæði í gæðaskoðun*

1. Í aðgerðarúðunni skal velja **Vista**.

#### <a name="purchase-order-line-receiving"></a>Móttaka innkaupapöntunarlínu

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stilla eftirfarandi gildi í hausnum:

    - **Heiti valmyndaratriðis:** *Móttaka innkaupapöntunarlínu*
    - **Titill:** *Móttaka innkaupapöntunarlínu*
    - **Máti:** *Vinna*
    - **Nota fyrirliggjandi vinnu:** *Nei*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**. Samþykkið sjálfgefin gildi fyrir reitina sem eftir eru.

    - **Stofnunarferli vinnu:** *Móttaka og frágangur innkaupapöntunarlínu*
    - **Mynda númeraplötu:** *Já*
    - **Vinnusniðmát:** *51 Innhreyfing innkaupapöntunar*

1. Í aðgerðarúðunni skal velja **Vista**.

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Bæta valmyndaratriði við valmynd fartækis

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.
1. Á svæðinu vinstra megin skal velja valmyndina **Á innleið**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Í dálknum **Tiltækar valmyndir og valmyndaratriði** skal velja nýja valmyndaratriðið **Móttaka innkaupapöntunarlínu**.
1. Smellið á hægri örvarhnappinn til að færa **Móttaka innkaupapöntunarlínu** yfir í dálkinn **Valmyndarskipan**.
1. Í dálknum **Valmyndaskipan** skal velja **Móttaka innkaupapöntunarlínu** og síðan velja uppörina eða niðurörina til að færa valmyndaratriðið á æskilega staðsetningu í valmynd fartækisins.
1. Í aðgerðarúðunni skal velja **Vista**.

## <a name="example-scenario"></a><a name="example-scenario"></a>Dæmi

Þegar búið er að gera öll sýnigögnin hér á undan tiltæk og setja þau upp, er hægt að fara í gegnum þetta sýnidæmi til að prófa eiginleikann *Gæðaskoðun*. Gildin sem eru sýnd í þessari atburðarás gera ráð fyrir að þú sért að vinna með stöðluðu kynningargögnin, að þú hafir valið **USMF** lögaðila og að þú hafir útbúið sýnishornsskrárnar sem lýst er fyrr í þessari grein. Þetta sýnidæmi er einnig dæmi um hvernig hægt er að nota eiginleikann í framleiðsluumhverfi.

### <a name="create-a-purchase-order"></a>Stofna innkaupapöntun

1. Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Sláðu inn eftirfarandi gildi í svarglugganum **Búa til innkaupapöntun**:

    - **Lánardrottnalykill:** *104*
    - **Vöruhús:** *51*

1. Veljið **Í lagi** til að loka svarglugganum og opnið nýju innkaupapöntunina.
1. Í flýtiflipanum **Innkaupapöntunarlínur** inniheldur hnitanetið nýja, auða línu. Stilltu eftirfarandi gildi á þessari línu:

    - **Vörunúmer:** *M9203*
    - **Magn:** *3*
    - **Eining:** *VÖRUBRETTI*

1. Í aðgerðarúðunni skal velja **Vista**.

### <a name="process-quality-check-receiving"></a>Vinna úr gæðaskoðun móttöku

Þegar innkaupapöntunin hefur verið stofnuð er hægt að taka á móti henni með því að nota valmyndaratriðið **Móttaka innkaupapöntunarlínu** og virknina fyrir eiginleikann *Gæðaskoðun*.

#### <a name="receive-pallet-1"></a>Móttaka vörubrettis 1

1. Skráðu þig inn í farsímaforrit vöruhúsakerfis sem notandi fyrir vöruhús *51*. (Sláið inn *51* sem notandakennið og *1* sem aðgangsorðið.)
1. Farið í **Á innleið \> móttaka innkaupapöntunarlínu**.
1. Í reitinn **PONUM** skal slá inn innkaupapöntunarnúmerið.
1. Staðfestið innkaupapöntunarnúmerið.
1. Í reitinn **LINENUM** skal slá inn fjölda innkaupapöntunarlína sem tekið er á móti. Þar sem pöntunin er aðeins með eina línu í þessu sýnidæmi, skal slá inn *1* í reitinn **LINENUM** fyrir hvert móttökuskref.
1. Staðfestið línunúmerið.
1. Í reitinn **Magn** skal slá inn magnið sem á að móttaka. Þar sem innkaupapöntunin er fyrir þrjú bretti (*PL*) í þessu sýnidæmi og það eru þrjú móttökuskref, skal slá inn *1* í reitinn **Magn** fyrir hvert móttökuskref.
1. Staðfestu magnið.

    Síðan **Gæðaskoðun** sem birtist er með enga innsláttarreiti. Hún er aðeins með staðfestingarhnappinn (gátmerki) neðst og valmyndarhnappinn (**≡**) efst. (Valmyndarhnappurinn er stundum kallaður hamborgari eða hamborgarahnappur.) Til að flýta fyrir gæðaskoðunarferlinu, þegar brettið stenst gæðaskoðun, staðfestir notandinn bara síðuna **Gæðaskoðun**.

    ![Gæðaskoðunarsíða.](media/quality-check.png "Gæðaskoðunarsíða")

1. Veljið staðfestingarhnappinn til að samþykkja gæðaskoðun fyrir bretti 1 úr línu 1.

    Síðan **Innkaupapantanir: Frágangur** sem birtist sýnir upplýsingar um frágangsvinnuna:

    - **STAÐ:** Staðsetning sem kerfið ákveður

        Þessi staðsetning er útnefnd frágangsstaðsetning fyrir móttöku innkaupapöntunar.

    - **NP:** Kenni númeraplötu sem kerfið býr til
    - **Vara:** *M9203*
    - **Magn:** *1 NP: 100 ea*

    Vörulýsingin er einnig sýnd.

1. Staðfestið frágangsvinnuna.

    Á síðunni **Verk** fyrir móttöku innkaupapöntunarlínu birtast skilaboðin „Vinnu lokið“. Reiturinn **LINENUM** er tiltækur þannig að hægt sé að taka á móti næsta bretti.

#### <a name="receive-pallet-2"></a>Móttaka vörubrettis 2

Í þessu sýnidæmi verður bretti 2 hafnað.

1. Í reitinn **LINENUM** skal slá inn *1* og staðfesta línunúmerið.
1. Reiturinn **Magn** er nú tiltækur. Sláið inn *1* og staðfestið magnið.

    Síðan **Gæðaskoðun** birtist. Fyrir þessa innhreyfingu verður brettinu hafnað vegna gæða og því komið fyrir á gæðastaðsetningunni *QMS*.

1. Veljið valmyndarhnappinn (**≡**) efst á síðunni og síðan, í valmyndinni, skal velja **Hafna**.
1. Á síðunni **Verk** sem birtist skal slá inn **QMS** sem staðsetningu *Frágangs* þar sem senda á brettið til að gangast undir frekara eftirlit.

    Síðan **Gæði í gæðaskoðun: Frágangur** sem birtist sýnir upplýsingar um frágangsvinnuna:

    - **STAÐ:** *QMS*

        Þessi staðsetning er útnefnd frágangsstaðsetning fyrir móttöku á því sem gæðaskoðun hafnar.

    - **NP:** Kenni númeraplötu sem kerfið býr til
    - **Vara:** *M9203*
    - **Magn:** *1 NP: 100 ea*

    Vörulýsingin er einnig sýnd.

1. Staðfestið frágangsvinnuna.

    Á síðunni **Verk** fyrir móttöku innkaupapöntunarlínu birtast skilaboðin „Vinnu lokið“. Reiturinn **LINENUM** er tiltækur þannig að hægt sé að taka á móti næsta bretti.

Gæðaskoðuninni hefur nú verið lokið og gæðapöntun stofnuð fyrir hafnaða brettið. Til að skoða pöntuina sem var stofnuð skal fara í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Gæðapantanir**.

Nú er hægt að vinna úr prófun gæðapöntunar. Ekki er fjallað um gæðapróf í þessari grein.

Frekari upplýsingar um gæðastjórnun má finna í [Gæðastjórnunaryfirlit](../inventory/enable-quality-management.md)

#### <a name="receive-pallet-3"></a>Móttaka vörubrettis 3

Í þessu sýnidæmi verður bretti 3 samþykkt.

1. Í reitinn **LINENUM** skal slá inn *1* og staðfesta línunúmerið.
1. Reiturinn **Magn** er nú tiltækur. Sláið inn *1* og staðfestið magnið.

    Síðan **Gæðaskoðun** birtist. Fyrir þessa innhreyfingu verður brettið samþykkt í gæðaskoðun og því komið fyrir magnstaðsetningu frágangs.

1. Veljið staðfestingarhnappinn til að samþykkja gæðaskoðun.

    Síðan **Innkaupapantanir: Frágangur** sem birtist sýnir upplýsingar um frágangsvinnuna:

    - **STAÐ:** Staðsetning sem kerfið ákveður

        Þessi staðsetning er útnefnd frágangsstaðsetning fyrir móttöku innkaupapöntunar.

    - **NP:** Kenni númeraplötu sem kerfið býr til
    - **Vara:** *M9203*
    - **Magn:** *1 NP: 100 ea*

    Vörulýsingin er einnig sýnd.

1. Staðfestið frágangsvinnuna.

    Á síðunni **Verk** fyrir móttöku innkaupapöntunarlínu birtast skilaboðin „Vinnu lokið“. Reiturinn **LINENUM** er tiltækur þannig að hægt sé að taka á móti næsta bretti.

1. Veljið valmyndarhnappinn (**≡**) efst á síðunni og síðan, í valmyndinni, skal velja **Hætta við** til að fara aftur í valmyndina.

Nú má loka fartækjaforritinu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]