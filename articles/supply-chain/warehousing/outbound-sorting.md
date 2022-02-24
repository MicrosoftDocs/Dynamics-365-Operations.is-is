---
title: Flokkun á útleið
description: Þetta efnisatriði gefur upplýsingar um flokkun á útleið. Þessi virkni auðveldar meðhöndlun lítilla gáma og hjálpar starfsmönnum vöruhúss að áætla og skipuleggja betur brettagetu í flutningabílnum.
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 2b0049269b69c0777420b3ecd9b1f649c4a1ab11
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963411"
---
# <a name="outbound-sorting"></a>Flokkun á útleið

[!include [banner](../includes/banner.md)]

Þessi virkni auðveldar meðhöndlun lítilla gáma og hjálpar starfsmönnum vöruhúss að áætla og skipuleggja betur brettagetu í flutningabílnum. Þegar flokkun á útleið er notuð er hægt að raða pökkuðum gámum á rétt bretti eftir að þeir hafa verið á pökkunarstöðinni. Einnig er hægt að búa til pökkunarstigveldi.

Þessi virkni gerir þér kleift að búa til bretti úr gámum sem eru pakkaðir í gegnum pökkunaraðgerðina. Gámurinn er ekki sendur á endanlegan sendingarstað eins og gerist í upprunalega pökkunarflæðinu. Í staðinn geta starfsmenn lokað gámnum og fært hann yfir í staðsetningu röðunargerðar. Þeir geta síðan raðað gámum á staðsetningar, hver staðsetning er með númeraplötu. Eftir að gámunum hefur verið raðað er hægt að búa til vinnu til að senda alla númeraplötuna að lokaafhendingarstað eða biðsvæðum byggt á staðsetningarleiðbeiningum viðskiptavina eða þínum eigin leiðbeiningum. Að auki getur lokun röðunarstaðsetningar flutt birgðirnar strax til lokaafhendingarstaðs og tínt hana fyrir pöntunina.

## <a name="turn-on-the-outbound-sorting-feature"></a>Kveikja á eiginleika flokkunar á útleið

Áður en hægt er að nota eiginleikann verður að vera kveikt á honum í kerfinu. Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Þar er eiginleikinn sýndur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Flokkun á útleið*

## <a name="setup"></a>Setja upp

Fyrir þessa atburðarás verður þú að nota hefðbundin sýnigögn **USMF** og vöruhús *62*. Einnig þarf að ljúka uppsetningunni sem lýst er í eftirfarandi undirköflum.

### <a name="set-up-a-wave-template"></a>Velja bylgjusniðmát

Þessi uppsetning vinnur sjálfkrafa úr bylgjunni og stofna vinnu þegar lína er losuð í vöruhús.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.
1. Í sniðmátslistanum velurðu **Vöruhús 62**.
1. Í flýtiflipanum **Almennt** skal ganga úr skugga um að valkosturinn **Vinna úr bylgju við losun í vöruhús** sé stilltur á *Já*.

### <a name="set-up-a-worker"></a>Setja upp starfskraft

Pökkunarstöðin er talin staðsetning. Starfsmenn vöruhúss sem skrá sig inn á pökkunarstöðinni sjá og vinna aðeins með sendingar og gáma sem áætlaðir eru á þessari tilteknu pökkunarstaðsetningu. Notandi sem skráir sig inn á Microsoft Dynamics 365 verður að vera settur upp sem starfsmaður í vöruhúsakerfi. Ef nafn notandans birtist ekki á listanum yfir vinnunotendur, skal nota eftirfarandi ferli til að bæta því við.

> [!NOTE]
> Þessi skref gera ráð fyrir að notandinn sé þegar til í kerfinu og hafi verið tengdur starfsmaður eða starfskraftur í einingunni **Mannauður**.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Starfskraftur**.
1. Veljið **Nýtt**.
1. Í reitnum **Starfskraftur** skal velja notandann í listanum yfir starfsmenn.
1. Veljið **Velja**.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Í flýtiflipanum **Notendur** skal velja **Nýr** til að stofna reikning í fartæki og stilla eftirfarandi gildi fyrir hann:

    - **Notandakenni:** Færðu inn einkvæmt kenni.
    - **Notandanafn:** Færið inn heiti fyrir auðkennið.
    - **Sjálfgefið vöruhús:** *62*
    - **Heiti valmyndar:** *Aðalvalmynd*

1. Í aðgerðarúðunni skal velja **Vista**.
1. Glugginn **Setja aðgangsorð** birtist þar sem hægt er að búa til einfalt aðgangsorð sem notandinn getur notað til að skrá sig inn í forrit fartækis. Stilla eftirfarandi gildi:

    - **Aðgangsorð:** Sláið inn einfalt aðgangsorð.
    - **Staðfesta aðgangsorð:** Sláið inn sama aðgangsorðið aftur.

1. Veldu **Stilla aðgangsorð**.

    Tilkynning í Aðgerðarmiðstöðinni upplýsir þig um að aðgangsorðið hafi verið stillt fyrir notandann sem þú bjóst til.

### <a name="create-a-location-type"></a>Stofna gerð staðsetningar

1. Opnaðu **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Gerðir staðsetninga**.
1. Veldu **Nýtt** á aðgerðasvæðinu til að búa til staðsetningargerð og stilltu eftirfarandi gildi fyrir hana:

    - **Gerð staðsetningar:** *SORT*
    - **Lýsing:** *Raða*

1. Í aðgerðarúðunni skal velja **Vista**.

### <a name="set-up-warehouse-management-parameters"></a>Setja upp færibreytur vöruhúsakerfis

1. Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.
1. Í flipanum **Almennt**, í flýtiflipanum **Gerðir staðsetninga**, skal stilla reitinn **Flokkun á gerð staðsetningar** á *SORT*.
1. Í aðgerðarúðunni skal velja **Vista**.

### <a name="set-up-a-location-profile"></a>Setja upp staðsetningarforstillingu

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Forstillingar staðsetningar**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stilla eftirfarandi gildi í hausnum:

    - **Kenni staðsetningarforstillingar:** *Röðun*
    - **Heiti:** *Röðun*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Staðsetningarsnið:** *ASRB* (Aisle-Rack-Shelf-Bin)
    - **Gerð staðsetningar:** *SORT*
    - **Nota rakningu númeraplötu:** *Já*
    - **Heimila blandaðar vörur:** *Já* (Þegar þessi valkostur er settur á *Já*, verður valkosturinn **Heimila blandaðar birgðastöðurunur** sjálfkrafa stilltur á *Já* og er ekki hægt að breyta út af fyrir sig.)

1. Veljið **Vista**.

### <a name="set-up-a-location"></a>Setja upp staðsetningu

1. Opnaðu **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Staðsetningar**.
1. Í hausnum skal hreinsa gátreitinn **Mynda vartölur fyrir staðsetningu**.
1. Veldu **Nýtt** á aðgerðasvæðinu til að búa til staðsetningargerð og stilltu eftirfarandi gildi fyrir hana:

    - **Vöruhús:** *62*
    - **Staðsetning:** *SORT*
    - **Kenni staðsetningarforstillingar:** *SORTING*

1. Veljið **Vista**.

### <a name="set-up-an-outbound-sorting-template"></a>Setja upp flokkunarsniðmát á útleið

Flokkunarsniðmát á útleið ákvarðar hvort vinna er stofnuð út frá röðunarstaðsetningu og hvort röðun er gerð handvirkt eða sjálfkrafa.

Fyrir þessa atburðarás stofnarðu flokkunarsniðmát á útleið til að búa til bretti eftir pökkunarstöðina.

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Pökkun \> Flokkunarsniðmát á útleið**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stilltu eftirfarandi gildi í haus nýja sniðmátsins:

    - **Kenni fyrir flokkunarsniðmát á útleið:** *AutoWork*
    - **Lýsing:** *Sjálfvirk stofnun vinnu*
    - **Sniðmátsgerð flokkunar á útleið:** *Gámur*
    - **Vöruhús:** *62*
    - **Staðsetning:** *SORT*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Sannprófun röðunar:** *Skönnun stöðu*
    - **Stofna vinnu á lokun stöðu:** *Já*

        Ef þessi valkostur er stilltur á *Já*, þegar staðan er lokuð, verður vinna stofnuð til að færa birgðir á lokasendingarstaðinn. Ef hann er stilltur á *Nei* verða birgðir strax tíndar fyrir pöntunina þegar staðan er lokuð.

    - **Stöðuverkefni:** *Sjálfvirkt*

        Ef þessi reitur er stilltu rá *Handvirkt* verður notandi alltaf að tilgreina hvaða stöðu birgðir eiga að vera flokkaðar í. Ef hann er stilltur á *Sjálfvirkt* beinir kerfið birgðum sjálfkrafa að stöðu þegar það er í boði, á grunni sundurliðana sniðmátsflokkunar.

1. Veldu **Vista** til að bjóða upp á valkostinn **Breyta fyrirspurn** á aðgerðasvæðinu.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.
1. Í fyrirspurnarritlinum, í flipanum **Röðun**, skal bæta við línu sem er með eftirfarandi gildi:

    - **Tafla:** *Sendingar*
    - **Afleidd tafla:** *Sendingar*
    - **Reitur:** *Flutningsþjónusta*

        Þegar þetta gildi er valið gætu komið upp eftirfarandi skilaboð: „Reiturinn Flutningsþjónusta er ekki vísisreitur. Á að bæta við röðun á þetta?“ Velja skal **Já**.

    - **Leitarstefna:** *Hækkandi*

1. Veljið **Í lagi**.
1. Þú gætir fengið eftirfarandi skilaboð: „Flokkun verður endurstillt, á að halda áfram?" Velja skal **Já**.

    Hnappur **Sundurliðanir flokkunarsniðmáts á útleið** á aðgerðasvæðinu verður tiltækur.

1. Á aðgerðasvæðinu skal velja **Sundurliðanir flokkunarsniðmáts á útleið**.
1. Í glugganum **Skilyrði fyrir flokkun á útleið** skal stilla eftirfarandi gildi:

    - **Tilvísunartöflunafn:** *Sendingar*
    - **Heiti tilvísunarreits:** *Flutningsþjónusta*
    - **Flokka eftir reit:** Veljið þennan gátreit til að flokka sendingar eftir flutningsþjónustu.

1. Veldu **Í lagi** til að vista stillingarnar þínar og loka glugganum.

### <a name="set-up-container-packing-policies"></a>Setja upp pökkunarreglur geymis

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Gámar \> Pökkunarreglur gáms**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stilla eftirfarandi gildi í hausnum á nýju reglunni:

    - **Pökkunarregla geymis:** *Raða*
    - **Lýsing:** *Raða*

1. Stilltu eftirfarandi gildi á **Yfirlit** flipanum:

    - **Vöruhús:** *62*
    - **Sjálfgefin staðsetning fyrir flokkun:** *SORT*
    - **Þyngdareining:** *kg*
    - **Lokunarregla geymis:** *Sjálfvirk losun*
    - **Losunarregla geymis:** *Úthluta gámi flokkaðri staðsetningu á útleið*

1. Veljið **Vista**.

### <a name="set-up-packing-profiles"></a>Setja upp pökkunarforstillingar

Stofnið nýja pökkunarforstillingu sem verður notuð ásamt röðunarvirkninni.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Pökkun \> Forstillingar umbúða**.
1. Veljið **Nýtt** á aðgerðasvæðinu til að búa til línu og stillið eftirfarandi gildi fyrir hana:

    - **Forstillingarkenni pökkunar:** *Raða*
    - **Lýsing:** *Raða*
    - **Pökkunarregla geymis:** *Raða*
    - **Auðkennisstilling gáms:** *Sjálfvirkt*
    - **Gámagerð:** *Kassi-stór*
    - **Stofna sjálfvirkt gám þegar gámi er lokað:** Hreinsað (= *Nei*)

1. Veljið **Vista**.

### <a name="set-up-work-classes"></a>Setja upp vinnuklasa

Setjið upp vinnuklasa sem notaður verður ásamt röðun.

1. Fara í **Vöruhúsastjórnun \> Uppsetning \> Vinna \> Vinnuklasar**.
1. Veljið **Nýtt** á aðgerðasvæðinu til að búa til vinnuklasa fyrir röðun og stillið eftirfarandi gildi fyrir hann:

    - **Auðkenni vinnuklasa:** *Raða*
    - **Lýsing:** *Raða*
    - **Gerð verkbeiðni:** *Röðuð birgðatínsla*

1. Veljið **Vista**.

### <a name="set-up-mobile-device-menu-items"></a>Setja upp valmyndaratriði fartækis

#### <a name="set-up-a-new-pallet-menu-item"></a>Setja upp nýtt valmyndaratriði brettis

Búa til valmyndaratriði fartækis til að búa til bretti við röðun.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stilla eftirfarandi gildi í hausnum:

    - **Heiti valmyndaratriðis:** *Röðun á bretti*
    - **Titill:** *Röðun á bretti*
    - **Stilling:** *Óbein*
    - **Nota fyrirliggjandi vinnu:** *Nei*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Verkþáttarkóði:** *Röðun á útleið*

        Þegar þessi reitur er stilltur á *Röðun á útleið* birtist reiturinn **Auðkenni flokkunarsniðmáts á útleið**.

    - **Nota leiðbeiningar fyrir ferli:** *Já*

        Þegar reiturinn **Verkþáttarkóði** er stilltur á *Röðun á útleið* verður þessi valkostur sjálfkrafa stilltur á *Já*.

    - **Kenni fyrir flokkunarsniðmát á útleið:** *AutoWork*

1. Veljið **Vista**.

#### <a name="set-up-a-new-loading-menu-item"></a>Setja upp nýtt valmyndaratriði hleðslu

Næst skal búa til valmyndaratriði sem gerir notendum kleift að flytja raðaðar birgðavörur á sendingarstaðinn.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stilla eftirfarandi gildi í hausnum:

    - **Heiti valmyndaratriðis:** *Hleðsla frá röðun*
    - **Titill:** *Hleðsla frá röðun*
    - **Máti:** *Vinna*
    - **Nota fyrirliggjandi vinnu:** *Já*

1. Í flýtiflipanum **Almennt** skal stilla reitinn **Stjórnað af** á *Stýrt af notanda*.
1. Í flýtiflipanum **Vinnuklasar** skal velja **Nýr** og síðan stilla eftirfarandi gildi:

    - **Auðkenni vinnuklasa:** *SORT*
    - **Gerð verkbeiðni:** *Röðuð birgðatínsla*

1. Veljið **Vista**.

### <a name="set-up-the-mobile-device-menu"></a>Uppsetning á valmynd fartækis

Þú verður nú að bæta nýju valmyndaratriðunum við valmynd fartækis.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.
1. Veljið valmyndina **Á útleið**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Í dálknum **Tiltækar valmyndir og valmyndaratriði** skal finna og velja **Röðun á bretti**.
1. Smellið á hægri örvarhnappinn til að færa **Röðun á bretti** yfir í dálkinn **Valmyndarskipan**.
1. Notið hnappana fyrir upp- og niðurörina til að setja valmyndaratriðið **Röðun á bretti** í æskilega stöðu á valmyndaratriði fartækis.
1. Veljið **Vista**.
1. Endurtakið þetta ferli til að valmyndaratriðinu **Hleðsla frá röðun** við valmyndina **Á útleið**.

### <a name="set-up-location-directives"></a>Setja upp staðsetningarleiðbeiningar

*Staðsetningarleiðbeiningar* eru reglur sem hjálpa við auðkenningu tiltektar- og frágangsstaðsetninga fyrir birgðahreyfingar. Nú þarf að búa til reglu til að stjórna röðunarvinnunni.

#### <a name="set-up-a-single-sku-directive"></a>Setja upp leiðbeiningu fyrir eina birgðahaldseiningu

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.
1. Á vinstra svæðinu skal breyta gildinu á reitnum **Gerð verkbeiðni** í *Röðuð birgðatínsla*.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stilla eftirfarandi gildi í hausnum:

    - **Röð:** *1*
    - **Heiti:** *Útskot*

1. Stilltu eftirfarandi gildi á flýtiflipanum **staðsetningarleiðbeiningar**:

    - **Tegund vinnu:** *Frágangur*
    - **Svæði:** *6*
    - **Vöruhús:** *62*
    - **Margar birgðahaldseiningar:** *Nei*

1. Veldu **Vista** til að gera tækjastikuna á flýtiflipanum **Línur** tiltækan.
1. Á flipanum **Línur** veldu **Nýtt** og stilltu síðan eftirfarandi gildi á nýju línunni. Samþykktu sjálfgildin fyrir öll önnur svæði.

    - **Röð:** *1*
    - **Frá:** *0*
    - **Til:** *1.000.000*

1. Veldu **Vista** til að gera tækjastikuna á flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** tiltækan.
1. Í flipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Ný** og stilla síðan eftirfarandi gildi í nýju línunni. Samþykktu sjálfgildin fyrir öll önnur svæði.

    - **Röð:** *1*
    - **Heiti:** *Útskot*

1. Veljið **Vista**.
1. Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Breyta fyrirspurn**.
1. Í fyrirspurnarritlinum, í flipanum **Svið**, skal finna línuna þar sem reiturinn **Svæði** er stilltur á *Staðsetning*. Stillið reitinn **Skilyrði** fyrir þessa línu á *Útskot*.
1. Veldu **Í lagi** til að vista stillingarnar þínar og loka fyrirspurnarritilinum.

#### <a name="set-up-a-multiple-sku-directive"></a>Setja upp leiðbeiningu fyrir margar birgðahaldseiningar

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.
1. Á vinstra svæðinu skal breyta gildinu á reitnum **Gerð verkbeiðni** í *Röðuð birgðatínsla*.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stilla eftirfarandi gildi í hausnum:

    - **Röð:** *2*
    - **Heiti:** *Mörg útskot*

1. Stilltu eftirfarandi gildi á flýtiflipanum **staðsetningarleiðbeiningar**:

    - **Tegund vinnu:** *Frágangur*
    - **Svæði:** *6*
    - **Vöruhús:** *62*
    - **Margar birgðahaldseiningar:** *Já*

1. Veldu **Vista** til að gera tækjastikuna á flýtiflipanum **Línur** tiltækan.
1. Á flipanum **Línur** veldu **Nýtt** og stilltu síðan eftirfarandi gildi á nýju línunni. Samþykktu sjálfgildin fyrir öll önnur svæði.

    - **Röð:** *1*
    - **Frá:** *0*
    - **Til:** *1.000.000*

1. Veldu **Vista** til að gera tækjastikuna á flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** tiltækan.
1. Í flipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Ný** og stilla síðan eftirfarandi gildi í nýju línunni. Samþykktu sjálfgildin fyrir öll önnur svæði.

    - **Röð:** *1*
    - **Heiti:** *Mörg útskot*

1. Veljið **Vista**.
1. Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Breyta fyrirspurn**.
1. Í fyrirspurnarritlinum, í flipanum **Svið**, skal finna línuna þar sem reiturinn **Svæði** er stilltur á *Staðsetning*. Stillið reitinn **Skilyrði** fyrir þessa línu á *Útskot*.
1. Veldu **Í lagi** til að vista stillingarnar þínar og loka fyrirspurnarritilinum.

### <a name="set-up-work-templates"></a>Setja upp vinnusniðmát

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.
1. Breytið gildinu í reitnum **Gerð verkbeiðni** í *Röðuð birgðatínsla*.
1. Veldu **Nýtt** á aðgerðasvæðinu til að búa til vinnusnið.
1. Í flipanum **Yfirlit** skal stilla eftirfarandi gildi:

    - **Röð:** *1*
    - **Vinnusniðmát:** *Raða*
    - **Lýsing á vinnusniðmáti:** *Flokka*

1. Veldu **Vista** til að gera flýtiflipann **Upplýsingar um vinnusniðmát** tiltækan.
1. Á flýtiflipanum **Upplýsingar um vinnusniðmát** velur þú **Ný** til að bæta við línu og stillir svo eftirfarandi gildi fyrir hana:

    - **Verkgerð:** *Tiltekt*
    - **Auðkenni vinnuklasa:** *SORT*

1. Veldu **Nýtt** til að bæta við annarri línu og stilltu eftirfarandi gildi fyrir hana:

    - **Tegund vinnu:** *Frágangur*
    - **Auðkenni vinnuklasa:** *SORT*

1. Veljið **Vista**.

## <a name="scenario"></a>Aðstæður

Þessi atburðarás líkir eftir aðstæðum þar sem raða ætti pökkuðum gámum sjálfkrafa á mismunandi staði (bretti) á eftir pökkunarstöðinni, samkvæmt því hver flutningsþjónustan er. Þegar öllum vörum hleðslunnar hefur verið pakkað og raðað eftir heimilisfangi, verða brettin færð yfir í útskotið.

### <a name="create-sales-orders-and-picking-work"></a>Búa til sölupöntun og tiltekt

#### <a name="create-sales-order-1"></a>Stofna sölupöntun 1

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - **Viðskiptavinalykill:** *US-005*
    - **Vöruhús:** *62*

1. Veldu **Í lagi** til að loka svarglugganum.

    Ný sölupöntun opnast.

1. Skiptið yfir í **Hausa** yfirlitið.
1. Í flýtiflipanum **Afhending**, í hlutanum **Flutningur**, skal stilla eftirfarandi gildi:

    - **Farmflytjandi:** *Flugfarmur*
    - **Flutningsþjónusta:** *flug*

1. Skiptið yfir í yfirlitið **Línur**.
1. Ef nýrri, tómri línu er ekki sjálfkrafa bætt við hnitanetið í flýtiflipanum **Sölupöntunarlínur**, skal velja **Bæta við línu** til að bæta einni við.
1. Stilltu eftirfarandi gildi á nýju pöntunarlínunni.

    - **Vörunúmer:** *A0001*
    - **Magn:** *2*

1. Með nýju pöntunarlínuna enn valda í flýtiflipanum **Sölupöntunarlínur**, í valmyndinni **Birgðir** fyrir ofan hnitanetið, skal velja **Frátekning**.
1. Í síðunni **Frátekning** skal velja **Frátektarlota** til að taka frá fullt magn af völdum línum í vöruhúsinu.
1. Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.
1. Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Aðgerðir**, velurðu **Losa í vöruhús**.
1. Þú færð upplýsingaboð sem sýna sendinguna og bylgjuna fyrir þessa pöntun. Skráið niður bylgjuauðkenni og sendingarnúmer.

#### <a name="sales-order-2"></a>Sölupöntun 2

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - **Viðskiptavinalykill:** *US-006*
    - **Vöruhús:** *62*

1. Veldu **Í lagi** til að loka svarglugganum.
1. Ný sölupöntun opnast. Hún ætti að innihalda nýja, auða línu í hnitanetinu í flýtiflipanum **Sölupöntunarlínur**. Í þessari pöntunarlínu skal stilla eftirfarandi gildi:

    - **Vara:** *A0001*
    - **Magn:** *1*

1. Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Afhending**, skal stilla reitinn **Flutningsmáti** á *Flowe-STD*.
1. Í flýtiflipanum **Sölupöntunarlínur** skal velja **Bæta við línu** og síðan stilla eftirfarandi gildi í næstu pöntunarlínu:

    - **Vara:** *A0002*
    - **Magn:** *1*

1. Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Afhending**, skal breyta gildinu í reitnum **Flutningsmáti** í *Air C-Air*.
1. Á flýtiflipanum **Sölupöntunarlínur** skal velja fyrstu pöntunarlínuna. Á valmyndinni **Birgðir** fyrir ofan hnitanetið velur þú svo **Frátekning**.
1. Í síðunni **Frátekning** skal velja **Frátektarlota** til að taka frá fullt magn af völdum línum í vöruhúsinu.
1. Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.
1. Á flýtiflipanum **Sölupöntunarlínur** skal velja aðra pöntunarlínuna. Á valmyndinni **Birgðir** fyrir ofan hnitanetið velur þú svo **Frátekning**.
1. Í síðunni **Frátekning** skal velja **Frátektarlota** til að taka frá fullt magn af völdum línum í vöruhúsinu.
1. Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.
1. Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Aðgerðir**, velurðu **Losa í vöruhús**.
1. Þú færð upplýsingaboð sem sýna sendinguna og bylgjuna fyrir þessa pöntun. Takið eftir því að tvö auðkennisnúmer bylgju og tvö auðkennisnúmer sendingar hafa verið búin til, eitt fyrir hvorn flutningsmáta sölupöntunarlínanna.

#### <a name="get-the-work-ids-from-the-work-details"></a>Ná í vinnukenni úr upplýsingum um vinnu

1. Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnu**.
1. Síðan sýnir vinnukenni sem hafa verið búin til úr sölupöntunum. Notið bylgjukennin og sendingarkennin úr stofnuðum sölupöntunum til að finna vinnukenni hvorrar bylgju og sendingar. Punktið hjá ykkur þessi vinnukenni því að nota þarf þau í næsta skrefi. Takið eftir því að tvö vinnukenni voru búin til fyrir seinni sölupöntunina. Ef mismunandi vörur eru tíndar úr mismunandi staðsetningum, verða búin til aðskilin vinnukenni.

### <a name="pick-items-for-the-sales-orders"></a>Tína atriði í sölupantanir

Ljúkið stofnaðri vinnu með því að nota fartækið til að færa vörurnar yfir í pökkunarstöðina.

1. Í fartækinu skal skrá sig inn í vöruhús *62* með því að nota notandakennið sem var stofnað fyrir þessa atburðarás (eða notandakennið fyrir notanda fyrirliggjandi sýnigagna).
1. Í aðalvalmyndinni skal velja **Á útleið**.
1. Í valmyndinni **Á útleið** skal velja **Sölutiltekt**.
1. Í reitinn **Auðkenni** skal slá inn vinnukennið sem búið var til fyrir sölupöntun 1.
1. Veljið **Í lagi**.
1. Á síðuna **Sölupantanir: Tiltekt** skal slá inn marknúmeraplötu sem var búin til fyrir sölupöntun 1. Takið eftir því að tiltektarstaðsetningin (*bulk-001*), vara (*A0001*) og magn (*2 stk*) eru sýnd.
1. Veljið **Í lagi**.
1. Skoðið upplýsingarnar á síðunni **Sölupantanir: Frágangur**. Reiturinn **Loc** á að sýna að tíndar vörur eru að fara á staðsetninguna *Pakka*.
1. Veljið **Í lagi**.

    Á síðunni **Skanna vinnukenni / kenni númeraplötu** birtast skilaboðin „Vinnu lokið“, sem gefur til kynna að vinnukennið fyrir sölupöntun 1 sé lokið.

    Þú velur nú sölupöntun 2.

1. Í reitinn **Auðkenni** skal slá inn vinnukennið sem búið var til fyrir sölupöntun 2, þar sem lína 1 er með vöru *A0001*.
1. Veljið **Í lagi**.
1. Á síðuna **Sölupantanir: Tiltekt** skal slá inn marknúmeraplötu. Takið eftir því að tiltektarstaðsetningin (*bulk-001*), vara (*A0001*) og magn (*1 stk*) eru sýnd.
1. Veljið **Í lagi**.
1. Skoðið upplýsingarnar á síðunni **Sölupantanir: Frágangur**. Reiturinn **Loc** á að sýna að tíndar vörur eru að fara á staðsetninguna *Pakka*.
1. Veljið **Í lagi**.

    Á síðunni **Skanna vinnukenni / kenni númeraplötu** birtast skilaboðin „Vinnu lokið“. Þessi skilaboð gefa til kynna að vinnukennið úr línu 1 fyrir sölupöntun 2 sé lokið.

1. Í reitinn **Auðkenni** skal slá inn vinnukennið sem búið var til fyrir sölupöntun 2, þar sem lína 2 er með vöru *A0002*.
1. Veljið **Í lagi**.
1. Á síðuna **Sölupantanir: Tiltekt** skal slá inn marknúmeraplötu. Takið eftir því að tiltektarstaðsetningin (*bulk-002*), vara (*A0001*) og magn (*1 stk*) eru sýnd.
1. Veljið **Í lagi**.
1. Skoðið upplýsingarnar á síðunni **Sölupantanir: Frágangur**. Reiturinn **Loc** á að sýna að tíndar vörur eru að fara á staðsetninguna *Pakka*.
1. Veljið **Í lagi**.

    Á síðunni **Skanna vinnukenni / kenni númeraplötu** birtast skilaboðin „Vinnu lokið“. Þessi skilaboð gefa til kynna að vinnukennið úr línu 2 fyrir sölupöntun 2 sé lokið.

### <a name="pack-sales-orders-into-containers"></a>Pakka sölupöntunum í gáma

#### <a name="pack-sales-order-1-into-containers"></a>Pakka sölupöntun 1 í gáma

1. Fara skal í **Vöruhúsakerfi \> Pökkun og gámun \> Pakka**.

    Svarglugginn **Velja pökkunarstöð** birtist. Sjálfgefið er að reiturinn **Starfskraftur** verði stilltur á heiti starfskrafts sem var settur upp hér áður.

1. Stilltu eftirfarandi gildi til að skoða og vinna við sendingar og gáma sem eru fyrirhugaðar á tilteknum pökkunarstað:

    - **Svæði:** *6*
    - **Vöruhús:** *62*
    - **Staðsetning:** *Pakka*
    - **Forstillingarkenni pökkunar:** *Raða*

1. Veldu **Í lagi** til að loka svarglugganum.
1. Á síðuna **Pakka**, í reitinn **Númeraplata eða sending**, skal slá inn marknúmeraplötuna fyrir sölupöntun 1. Ýtið síðan á **Tab** eða **Enter** á lyklaborðinu til að fara úr reitnum.
1. Á aðgerðasvæðinu skal velja **Nýr gámur**.
1. Samþykkið allar sjálfgefnar stillingar og veljið **Í lagi**. Punktið niður gámakennið.
1. Í flýtiflipanum **Vörupökkun** skal stilla eftirfarandi gildi:

    - **Magn:** *1*
    - **Kennimerki:** Atriði *A0001*

1. Á aðgerðasvæðinu skal velja **Loka gámi**.
1. Í svarglugganum **Loka gámi** skal velja **Fá þyngd kerfis** til að fá kerfið til að uppfæra reitinn **Brúttóþyngd**.
1. Veljið **Í lagi**. Gámurinn er fluttur á staðsetninguna *SORT* og er tilbúinn til röðunar.
1. Búðu til annan gám til að bæta öðrum hlut frá númeraplötu fyrir sölupöntun 1 í nýjan gám.
1. Á aðgerðasvæðinu skal velja **Nýr gámur**.
1. Samþykkið allar sjálfgefnar stillingar og veljið **Í lagi**. Punktið niður gámakennið.
1. Í flýtiflipanum **Vörupökkun** skal stilla eftirfarandi gildi:

    - **Magn:** *1*
    - **Kennimerki:** Atriði *A0001*

1. Á aðgerðasvæðinu skal velja **Loka gámi**.
1. Í svarglugganum **Loka gámi** skal velja **Fá þyngd kerfis** til að fá kerfið til að uppfæra reitinn **Brúttóþyngd**.
1. Veljið **Í lagi**. Gámurinn er fluttur á staðsetninguna *SORT* og er tilbúinn til röðunar.

#### <a name="pack-sales-order-2-into-containers"></a>Pakka sölupöntun 2 í gáma

1. Á síðuna **Pakka**, í reitinn **Númeraplata eða sending**, skal slá inn marknúmeraplötuna fyrir línu 1 í sölupöntun 2. Ýtið síðan á **Tab** eða **Enter** á lyklaborðinu til að fara úr reitnum.
1. Á aðgerðasvæðinu skal velja **Nýr gámur**.
1. Samþykkið allar sjálfgefnar stillingar og veljið **Í lagi**. Punktið niður gámakennið.
1. Í flýtiflipanum **Vörupökkun** skal stilla eftirfarandi gildi:

    - **Magn:** *1*
    - **Kennimerki:** Atriði *A0001*

1. Á aðgerðasvæðinu skal velja **Loka gámi**.
1. Í svarglugganum **Loka gámi** skal velja **Fá þyngd kerfis** til að fá kerfið til að uppfæra reitinn **Brúttóþyngd**.
1. Veljið **Í lagi**. Gámurinn er fluttur á staðsetninguna *SORT* og er tilbúinn til röðunar.
1. Í reitinn **Númeraplata eða sending** skal slá inn marknúmeraplötuna fyrir línu 2 í sölupöntun 2. Ýtið síðan á **Tab** eða **Enter** á lyklaborðinu til að fara úr reitnum.
1. Á aðgerðasvæðinu skal velja **Nýr gámur**.
1. Samþykkið allar sjálfgefnar stillingar og veljið **Í lagi**. Punktið niður gámakennið.
1. Í flýtiflipanum **Vörupökkun** skal stilla eftirfarandi gildi:

    - **Magn:** *1*
    - **Auðkennireitur:** Atriði *A0002*

1. Á aðgerðasvæðinu skal velja **Loka gámi**.
1. Í svarglugganum **Loka gámi** skal velja **Fá þyngd kerfis** til að fá kerfið til að uppfæra reitinn **Brúttóþyngd**.
1. Veljið **Í lagi**. Gámurinn er fluttur á staðsetninguna *SORT* og er tilbúinn til röðunar.

Til að skoða upplýsingar um gáminn skal fara í **Vöruhúsakerfi \> Pökkun og gámun \> Gámar** og leita að gámakennum sem búin voru til við pökkun.

### <a name="sort-the-containers"></a>Raða gámum

> [!IMPORTANT]
> Þegar farið er í valmyndaratriðið **Röðun á bretti** í fartækjaforritinu til að gera röðun á útleið, sést hnappur sem merktur er **Fullhlaðið**. *Ekki nota hnappinn **Fullhlaðið** til að raða eða loka stöðunni.*
>
> Hnappurinn **Fullhlaðið** kemur sjálfgefið fram og er ekki hægt að óvirkja eða fjarlægja af síðunni. Hann er ekki notaður fyrir eiginleikann *Röðun á útleið*.

#### <a name="sort-the-first-container"></a>Raða fyrsta gámnum

1. Í fartækinu skal skrá sig inn í vöruhús *62* með því að nota notandakennið sem var stofnað fyrir þessa atburðarás (eða notandakennið fyrir notanda fyrirliggjandi sýnigagna).
1. Í aðalvalmyndinni skal velja **Á útleið**.
1. Í valmyndinni **Á útleið** skal velja **Röðun á bretti**.
1. Í reitinn **NP/Gám** skal slá inn fyrsta gámakennið sem tengist sölupöntun 1.
1. Veljið **Í lagi**.
1. Fyrst að engir röðunarstaðir eru til sem stendur, þarf að tilgreina einn. Í reitinn **Staðsetningarkenni röðunar** skal slá inn *SP01*.
1. Fyrst að engin númeraplata sem tengist röðunarstað *SP01* er til sem stendur, þarf að tilgreina einn. Í reitinn **NP** skal slá inn *PLP01*.
1. Veljið **Í lagi**.
1. Kveikt er á sannprófun röðunarstaðs og því þarf að slá inn staðsetningarkenni röðunar aftur. Í reitinn **Staðsetningarkenni röðunar** skal slá inn *SP01*.
1. Veljið **Í lagi**.

    Skilaboðin „Vinnu er lokið“ birtast.

> [!TIP]
> Til að skoða röðunarstaðinn og númeraplötuna í henni skal fara í **Vöruhúsakerfi \> Pökkun og gámun \> Úthlutanir á staðsetningum röðunar á útleið**.
>
> Síðan **Úthlutanir á staðsetningum röðunar á útleið** sýnir alla röðunarstaði sem eru virkir sem stendur. Reiturinn **Færslur röðunarstaðs** sýnir númeraplötuna sem tengist hverri röðunarstöðu og gámana sem eru í röðunarstöðunni. Takið eftir því að ein röðunarstaðan er til og að flýtiflipinn **Skilyrði röðunarstaðs** sýnir skilyrði **Sending - Flutningsþjónusta - Flug**.

#### <a name="sort-the-remaining-containers"></a>Raða gámunum sem eftir eru

1. Í fartækinu skal skrá sig inn í vöruhús *62* með því að nota notandakennið sem var stofnað fyrir þessa atburðarás (eða notandakennið fyrir notanda fyrirliggjandi sýnigagna).
1. Í aðalvalmyndinni skal velja **Á útleið**.
1. Í valmyndinni **Á útleið** skal velja **Röðun á bretti**.
1. Í reitinn **NP/Gám** skal slá inn næsta gámakennið sem tengist sölupöntun 1.
1. Veljið **Í lagi**. Fyrst að flokkunarsniðmát er uppsett til að raða sjálfkrafa, og röðunarstaður sem er með samsvarandi skilyrði er þegar til, verður þér sjálfkrafa vísað á réttan röðunarstað.
1. Veljið **Í lagi**.
1. Staðfestið staðsetningarkenni röðunar til að gefa til kynna að birgðirnar séu á réttum stað. Í reitinn **Staðsetningarkenni röðunar** skal slá inn *SP01*.
1. Veljið **Í lagi**.

    Vinnu er lokið við annan gáminn úr sölupöntun 1. Þú munt nú raða gámunum sem eftir eru úr sölupöntun 2.

1. Í reitinn **NP/Gám** skal slá inn gámakenni gámsins í sölupöntun 2 sem er með vöruna *A0001*. Fyrst að flutningsþjónustan er ekki sú sama er beðið um að færa inn nýjan röðunarstað og úthluta númeraplötu á þá staðsetningu. Notið röðunarstað *SP02* og númeraplötu *PLP02*.
1. Veljið **Í lagi**.
1. Staðfestið röðunarstaðinn með því að slá inn *SP02* í reitinn **Staðsetningarkenni röðunar**.
1. Veljið **Í lagi**.

    Vinnu er lokið við gáminn.

1. Í reitinn **NP/Gám** skal slá inn gámakenni fyrir eftirstandandi gám í sölupöntun 2 sem er með vöruna *A0002*. Fyrst að flutningsþjónustan er sú sama og flutningsþjónusta sölupöntunar 1, sýnir kerfið fyrirliggjandi röðunarstað sem er með samsvarandi skilyrði.
1. Veljið **Í lagi**.
1. Staðfestið röðunarstaðinn með því að slá inn *SP01* í reitinn **Staðsetningarkenni röðunar**.
1. Veljið **Í lagi**.

    Vinnu er lokið við gáminn.

### <a name="close-the-outbound-sorting-positions"></a>Loka röðunarstöðum á útleið

Þegar búið er að raða öllum birgðum verður að loka staðnum áður en hægt er að búa til vinnu. Röðuð birgðatínsluvinna verður búin til að fara með birgðirnar í útskotið.

#### <a name="close-a-position-from-the-mobile-device"></a>Loka staðsetningu úr fartækinu

1. Í fartækinu skal skrá sig inn í vöruhús *62* með því að nota notandakennið sem var stofnað fyrir þessa atburðarás (eða notandakennið fyrir notanda fyrirliggjandi sýnigagna).
1. Í aðalvalmyndinni skal velja **Á útleið**.
1. Í valmyndinni **Á útleið** skal velja **Röðun á bretti**.
1. Í reitinn **NP/Gám** skal slá inn gámakenni sem var raðað fyrir röðunarstaðinn *SP01*.
1. Veljið **Í lagi**.
1. Eftirfarandi skilaboð birtast: „Gámnum hefur þegar verið raðað á staðsetninguna SP01. Loka staðsetningunni? Veljið **Loka**.

    Vinnu er lokið.

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a>Loka staðsetningu í úthlutunum á röðunarstað á útleið

1. Fara skal í **Vöruhúsakerfi \> Pökkun og gámun \> Úthlutanir á röðunarstað á útleið**.
1. Í vinstri dálknum skal velja **SP02**. Þessi lína röðunarstaðs á útleið er sú sem á að loka.
1. Á aðgerðasvæðinu skal velja **Loka staðsetningu**. Færsla röðunarstaðs er lokað og hún ekki lengur sýnd.

    > [!TIP]
    > Til að sýna allar færslur lokaðra staðsetninga skal velja gátreitinn **Sýna lokaðar**.

### <a name="sorted-inventory-picking"></a>Tiltekt í flokkuðum birgðum

Ljúka þarf tiltekt flokkaðra birgða. Þegar henni er lokið verða birgðir tíndar fyrir sölupöntunina. Á þeim tímapunkti eiga öll önnur vöruhúsaferli við.

1. Í fartækinu skal skrá sig inn í vöruhús *62* með því að nota notandakennið sem var stofnað fyrir þessa atburðarás (eða notandakennið fyrir notanda fyrirliggjandi sýnigagna).
1. Í aðalvalmyndinni skal velja **Á útleið**.
1. Í valmyndinni **Á útleið** skal velja **Hleðsla frá röðun**.
1. Sláið inn auðkenni marknúmeraplötu úr fyrsta röðunarstaðnum, *SP01*. Stilltu reitinn **Kenni** á *PLP01*.
1. Veljið **Í lagi**.
1. Síðan **Tiltekt í flokkuðum birgðum** sýnir tiltektarvinnuna sem þarf að gera. Veljið úr staðsetningunni *SORT* og marknúmeraplötunni *PLP01*, sem er með margar vörur og magn upp á *3*.
1. Veljið **Í lagi**.
1. Síðan **Tiltekt í flokkuðum birgðum** sýnir frágangsvinnuna sem þarf að gera. Gangið frá í staðsetninguna *Útskot* og marknúmeraplötuna *PLP01*, sem er með margar vörur og magn upp á *3*.
1. Veljið **Í lagi**.

    Vinnu er lokið.

1. Sláið inn kenni marknúmeraplötu úr seinni röðunarstaðnum *SP02*. Stilltu reitinn **Kenni** á *PLP02*.
1. Veljið **Í lagi**.
1. Síðan **Tiltekt í flokkuðum birgðum** sýnir tiltektarvinnuna sem þarf að gera. Tínið úr staðsetningunni *SORT* og marknúmeraplötunni *PLP02*, sem er með margar vörur og magn upp á *1*.
1. Veljið **Í lagi**.
1. Síðan **Tiltekt í flokkuðum birgðum** sýnir frágangsvinnuna sem þarf að gera. Gangið frá í staðsetninguna *Útskot* og marknúmeraplötuna *PLP02*, sem er með margar vörur og magn upp á *1*.
1. Veljið **Í lagi**.

    Vinnu er lokið.

Héðan í frá eiga öll önnur vöruhúsaferli við.
