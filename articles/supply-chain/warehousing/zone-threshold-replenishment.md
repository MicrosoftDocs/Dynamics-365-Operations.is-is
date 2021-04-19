---
title: Áfyllingarmörk svæðis
description: Áfyllingarmörk svæðis notar lágmarks-/hámarkáfyllingarstefnu (lágm./hám.), en hún metur heil svæði í vöruhúsi í staðinn fyrir einstakar staðsetningar. Þar af leiðandi geta stjórnendur vöruhúsa skjótt komist að því þegar frekari birgða er krafist á tiltektarsvæði.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d0a97ed7b01a32e9276433713448a672f83f7d02
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814369"
---
# <a name="zone-threshold-replenishment"></a>Áfyllingarmörk svæðis

[!include [banner](../includes/banner.md)]

Áfyllingarmörk svæðis notar [lágmarks-/hámarkáfyllingarstefnu](replenishment.md) (lágm./hám.), en hún metur heil svæði í vöruhúsi í staðinn fyrir einstakar staðsetningar. Þar af leiðandi geta stjórnendur vöruhúsa skjótt komist að því þegar frekari birgða er krafist á tiltektarsvæði.

Uppsetningin fyrir þennan eiginleika líkist uppsetningunni fyrir áfyllingu miðað við staðsetningar. Hins vegar þegar þú setur upp sniðmát fyrir lágm./hám. áfyllingu geturðu einnig tilgreint hvort meta skal viðmiðunarmörkin fyrir hverja staðsetningu eða hvert svæði. Ef þú setur upp mat sem byggir á svæðum verður þú að bæta við sérstökum svæðum við fyrirspurn vals á svæði.

Líkt og lágm./hám. áfyllingar sem miðast við staðsetningar, miðast lágm./hám. áfylling miðað við svæði á lágmarksviðmiðunarmörk birgðar sem kallar fram áfyllingarvinnu fyrir valdar vörur. Þessi áfyllingarvinna eykur birgðir að tilgreindum hámarksviðmiðunarmörkum fyrir svæðið.

> [!NOTE]
> Áfyllingarferli svæða fyrir afurðarafbrigði eru ekki studd í núverandi útgáfu.


Ólíkt lágm./hám. áfyllingu miðað við staðsetningar, krefst lágm./hám. áfylling sem miðast við svæði ekki fastra staðsetninga til að meta hvort staðsetningar ættu að geyma tiltekna vöru. Þess vegna gerir áfylling sem miðast við svæði kleift að nota lágm./hám. áfyllingu jafnvel þó að þú hafir ekki fasta staðsetningu fyrir hverja vöru eða afurðarafbrigði í vöruhúsinu. Þegar magn á svæðinu fellur undir tilgreind lágmarksviðmiðunarmörk verður til áfyllingarvinna. Staðsetningarleiðbeiningar ákvarða staðsetninguna sem birgðunum er komið fyrir.

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a>Kveikja á eiginleikanum áfyllingarmörk svæðis

Áður en þú getur notað eiginleikann *Áfyllingarmörk svæðis*, verður að vera kveikt á því í kerfinu þínu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Áfyllingarmörk svæðis*

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a>Uppsetning á áfyllingu miðað við svæði

Til að setja upp áfyllingu miðað við svæði verður þú að grunnstilla nokkra hluta kerfisins. Þessi hluti kynnir ýmsar stillingar og gildi sýnigagna sem þú getur slegið inn ef þú vilt vinna í gegnum aðstæðurnar í lok þessa efnisatriðis.

### <a name="set-up-directive-codes"></a>Setja upp leiðbeiningarkóða

[Leiðbeiningarkóðar](control-warehouse-location-directives.md) gera þér kleift að vera nákvæmari þegar þú skilgreinir staðsetningarsniðmáts sem er notað í vinnusniðmáti. Hver kóði setur upp sameiginlegt gildi sem þú getur vísað til þegar þú grunnstillir hverja tegund sniðmáts fyrir sig.

#### <a name="view-and-edit-directive-codes"></a>Skoða og breyta leiðbeiningarkóðum

Opnaðu **Vöruhúsakerfi \> Uppsetning \> Leiðbeiningarkóðar** til að skoða eða breyta leiðbeiningarkóðunum.

#### <a name="prepare-demo-data-directive-codes"></a>Búa til leiðbeiningarkóða sýnigagna

Þetta dæmi sýnir hvernig á að búa til leiðbeiningarkóða. Ef þú ætlar að vinna í gegnum aðstæðurnar í lok þessa efnisatriðis getur þú notað sýnigögnin sem koma fram hér. Annars skaltu nota þín eigin gildi.

1. Veldu **USMF**-lögaðilann til að vinna með sýnigögnin.
1. Opnaðu **Vöruhúsakerfi \> Uppsetning \> Leiðbeiningarkóðar**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.
1. Í nýju línunni skal stilla eftirfarandi gildi:

    - **Leiðbeiningarkóði:** _Áfylling svæða_
    - **Lýsing leiðbeininga:** _Áfylling svæða_

1. Veljið **Vista** til að vista nýja kóðann.

### <a name="set-up-replenishment-templates"></a>Setja upp sniðmát áfyllingar

[Sniðmát fyrir lágm./hám. áfyllingar](tasks/set-up-min-max-replenishment-process.md) er aðalverkfærið til að viðhalda ákjósanlegum gildum á tiltektarstaðsetningum. Í þessum sniðmátum verður þú að setja upp reglurnar sem verða notaðar til að fylla á birgðir í vöruhúsinu. Áfyllingin sem hægt er að nota sniðmátin fyrir inniheldur áfyllingu miðað við svæði.

#### <a name="view-and-edit-replenishment-templates"></a>Skoða og breyta áfyllingarsniðmátum

Áfyllingarsniðmát er safn reglna sem stjórna því hvernig og hvenær fyllt er á staðsetningu. Þú velur sniðmát til að stjórna hvenær og hvernig áfylling á sér stað. Opnaðu **Vöruhúsakerfi \> Uppsetning \> Áfylling \> Áfyllingarsniðmát** til að skoða eða breyta áfyllingarsniðmátum.

#### <a name="prepare-a-demo-data-replenishment-template"></a>Undirbúningur áfyllingarsniðmáts með sýnigögnum

Þetta dæmi sýnir hvernig á að undirbúa áfyllingarsniðmát. Ef þú ætlar að vinna í gegnum aðstæðurnar í lok þessa efnisatriðis getur þú notað sýnigögnin sem koma fram hér. Annars skaltu nota þín eigin gildi.

1. Veldu **USMF**-lögaðilann til að vinna með sýnigögnin.
1. Fara í **Vöruhúsakerfi \> Uppsetningu \> Áfylling \> Áfyllingarsniðmát**.
1. Veldu **Breyta** til að setja síðuna í breytingastillingu.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið **Yfirlit**.
1. Í nýju línunni skal stilla eftirfarandi gildi. Samþykktu sjálfgildin fyrir öll önnur svæði.

    - **Áfyllingarsniðmát:** _Lágm./hám. áfylling fyrir svæði_
    - **Lýsing:** _Lágm./hám. áfylling_
    - **Gerð áfyllingar:** _Lágmarks eða hámarks_

1. Veljið **Vista**.
1. Þó að nýja línan sé enn valin í hnitanetinu **Yfirlit** skaltu velja **Nýtt** fyrir ofan hnitanetið **Upplýsingar um áfyllingarsniðmát** til að bæta við línu sem er tengd við áfyllingarsniðmátið *Lágm./hám. áfylling fyrir svæði* sem þú varst að búa til.
1. Í nýju línunni skal stilla eftirfarandi gildi:

    - **Raðnúmer:** Sláðu inn _1_.
    - **Lýsing** Sláðu inn _Áfylling tiltektarsvæðis_.
    - **Áfyllingareining** Veldu _ea_.
    - **Tegund beiðni::** Hafðu þetta svæði autt.
    - **Staðsetningarleiðbeiningar:** Þetta svæði tengir áfyllingarsniðmátið við staðsetningarleiðbeiningarnar. Veldu staðsetningakóða sýnigagnanna sem þú bjóst til áður (_Áfylling fyrir svæði_).
    - **Vinnusniðmát:** Skildu þetta svæði eftir autt.
    - **Lágmarksmagn:** Þetta svæði setur upp magnið sem áfylling verður sett af stað. Færðu inn _50_.
    - **Hámarksmagn:** Þetta svæði stillir hámarksmagn vöru sem getur verið til staðar á svæði. Framleidd áfyllingarvinna eykur birgðirnar um þetta magn. Færðu inn _150_.
    - **Eining:** Þetta svæði úthluta einingu fyrir lágmarks- og hámarksgildi. Veldu _ea_.
    - **Aukning eftirspurnar:** Veldu _Námunda_.
    - **Fylla á auðar fastar staðsetningar:** Merktu í þennan gátreit.
    - **Fylla aðeins á fastar staðsetningar:** Hreinsaðu þennan gátreit.
    - **Fyrirspurnarstilling afurðar:** Veldu _Fyrirspurn afurðar_.
    - **Viðmiðunarmörk áfyllingar:**: Þetta svæði skilgreinir hvort sniðmátið eigi að meta eftir svæði eða eftir tiltekinni staðsetningu. Veldu _Svæði_.
    - **Vöruhús:** veldu _61_.

1. Veldu **Velja afurðir** fyrir ofan hnitanetið **Upplýsingar um áfyllingarsniðmát**.
1. Í svarglugga **Fyrirspurn afurðar** á flipanum **Svið** velur þú **Bæta við** til að bæta línu við hnitanetið.
1. Í nýju línunni skal stilla eftirfarandi gildi:

    - **Tafla:** _Vara_
    - **Afleidd tafla:** _Vara_
    - **Svæði:** _Vörunúmer_
    - **Skilyrði:** _A0001_

1. Velja skal **Í lagi** til að vista fyrirspurnina og loka glugganum.
1. Veldu **Svæði til að fylla á** fyrir ofan hnitanetið **Upplýsingar um áfyllingarsniðmát**.
1. Í svarglugga **Fyrirspurn afurðar** á flipanum **Svið** bætir þú línu við hnitanetið.
1. Í nýju línunni skal stilla eftirfarandi gildi:

    - **Tafla:** _Svæði í vöruhúsi_
    - **Afleidd tafla:** _Svæði í vöruhúsi_
    - **Reitur::** _Auðkenni svæðis_
    - **Skilyrði:** _GÓLF_

1. Velja skal **Í lagi** til að vista fyrirspurnina og loka glugganum.

### <a name="set-up-location-directives"></a>Setja upp staðsetningarleiðbeiningar

Ólíkt lágm./hám. áfyllingu miðað við staðsetningu, krefst lágm./hám. áfylling miðað við svæði þess að þú setjir bæði upp staðsetningarleiðbeiningar og leiðbeiningar fyrir frágangsstaðsetningar, vegna þess að kerfið metur allt svæðið í staðinn fyrir að tiltektarstaðsetninguna fyrir vinnu á útleið.

#### <a name="view-and-edit-location-directives"></a>Skoða og breyta staðsetningarleiðbeiningum

Opnaðu **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar** til að skoða eða breyta staðsetningarleiðbeiningunum þínum.

Fyrir dæmi sem sýna hvernig nota á stillingarnar til að búa til áskildar leiðbeiningar fyrir tiltektarstaðsetningar og leiðbeiningar fyrir frágangsstaðsetningar, sjá næsta kafla.

#### <a name="prepare-demo-data-location-directives"></a>Undirbúningur staðsetningarleiðbeininga úr sýnigögnum

Til að útbúa sýnigögn svo hægt sé að nota þau við aðstæðurnar í lok þessa efnisatriðis, verður þú að búa til tvær staðsetningarleiðbeiningar: eina fyrir tiltekt og eina fyrir frágang.

##### <a name="create-a-replenishment-pick-directive"></a>Búa til leiðbeiningar um tiltekt áfyllingar

1. Veldu **USMF**-lögaðilann til að vinna með sýnigögnin.
1. Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.
1. Stilltu svæðið **Gerð verkbeiðni** á _Áfylling_ í vinstri glugganum.
1. Veldu **Nýtt** á aðgerðasvæðinu til að búa til nýjar leiðbeiningar.
1. Stilla eftirfarandi gildi:

    - **Raðnúmer:** Samþykkja sjálfgildið.
    - **Heiti:** Sláðu inn _Tiltekt á svæði_.
    - **Tegund vinnu:** Veldu _Tiltekt_.
    - **Svæði:** Veldu _6_.
    - **Vöruhús:** veldu _61_.
    - **Leiðbeiningarkóði:** Hafðu þetta svæði autt.
    - **Margar birgðahaldseiningar:** Stilltu þennan möguleika á _Nei_.

1. Veldu **Vista** til að búa til leiðbeiningar sem hafa stillingarnar sem þú hefur grunnstillt hingað til.
1. Á flýtiflipanum **Línur** velur þú **Ný** til að bæta línu við hnitanetið.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Raðnúmer:** Sláðu inn _1_.
    - **Frá-magn:** Sláðu inn _0_.
    - **Til-magn** Enter _10000000_.
    - **Eining:** Hafðu þetta svæði autt.
    - **Finna magn:** Veldu _Ekkert_.
    - **Takmarka eftir einingu:** Hreinsaðu þennan gátreit.
    - **Námunda eftir einingu:** Hreinsaðu þennan gátreit.
    - **Finna umbúðarmagn:** Hreinsaðu þennan gátreit.
    - **Leyfa að skipta:** Hakið í þennan gátreit.

1. Veljið **Vista** til að vista nýju línuna.
1. Þó að nýja línan þín sé enn valin á hnitanetinu **Línur** skaltu velja **Nýtt** á flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** til að bæta línu við hnitanetið.
1. Í nýju línunni skal stilla eftirfarandi gildi:

    - **Raðnúmer:** Sláðu inn _1_.
    - **Heiti:** Sláðu inn _Tiltekt úr lausu_.
    - **Notkun fastrar staðsetningar:** Veldu _Fastar og lausar staðsetningar_.
    - **Leyfa neikvæðar birgðir:** Hreinsaðu þennan gátreit.
    - **Runa virk:** Hreinsaðu þennan gátreit.
    - **Áætlun:** Veldu _Engin_.

1. Veljið **Vista** til að vista nýju aðgerðina.
1. Þó að nýja aðgerðin þín sé enn valin skaltu velja **Breyta fyrirspurn** fyrir ofan hnitanetið **Aðgerðir í staðsetningarleiðbeiningum**.
1. Svargluggi fyrirspurnar birtist þar sem þú getur valið staðsetningarnar sem skal fylla á úr. Veldu **Bæta við** til að bæta við röð á flipanum **Svið** til að bæta línu við hnitanetið.
1. Í nýju línunni skal stilla eftirfarandi gildi:

    - **Tafla:** _Staðir_
    - **Afleidd tafla:** _Staðsetningar_
    - **Reitur::** _Auðkenni svæðis_
    - **Skilyrði:** _BULK_

1. Velja skal **Í lagi** til að vista fyrirspurnina og loka glugganum.
1. Smelltu á **Vista** til að vista staðsetningarleiðbeiningarnar þínar.

##### <a name="create-a-replenishment-put-directive"></a>Búa til leiðbeiningar um frátekt áfyllingar

1. Á síðunni **Staðsetningarleiðbeiningar** í vinstri glugganum skaltu ganga úr skugga um að svæðið **Gerð verkbeiðni** sé enn stilltur á _Áfyllingu_.
1. Veldu **Nýtt** á aðgerðasvæðinu til að búa til aðrar nýjar leiðbeiningar.
1. Stilla eftirfarandi gildi:

    - **Raðnúmer:** Samþykkja sjálfgildið.
    - **Heiti:** Sláðu inn _Frágangur á svæði_.
    - **Gerð verkbeiðni:** Veldu _Frágangur_.
    - **Svæði:** Veldu _6_.
    - **Vöruhús:** veldu _61_.
    - **Leiðbeiningarkóði:** Veldu _Áfylling á svæði_ til að tengja þessar staðsetningarleiðbeiningar við áfyllingarsniðmátið sem þú bjóst til áður með því að nota kóðann sem þú bjóst til áður.
    - **Margar birgðahaldseiningar:** Stilltu þennan möguleika á _Nei_.

1. Veldu **Vista** til að búa til leiðbeiningar sem hafa stillingarnar sem þú hefur grunnstillt hingað til.
1. Á flýtiflipanum **Línur** velur þú **Ný** til að bæta línu við hnitanetið.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Raðnúmer:** Sláðu inn _1_.
    - **Frá-magn:** Sláðu inn _0_.
    - **Til-magn** Enter _10000000_.
    - **Eining:** Hafðu þetta svæði autt.
    - **Finna magn:** Veldu _Ekkert_.
    - **Takmarka eftir einingu:** Hreinsaðu þennan gátreit.
    - **Námunda eftir einingu:** Hreinsaðu þennan gátreit.
    - **Finna umbúðarmagn:** Hreinsaðu þennan gátreit.
    - **Leyfa að skipta:** Hakið í þennan gátreit.

1. Veljið **Vista** til að vista nýju línuna.
1. Þó að nýja línan þín sé enn valin á hnitanetinu **Línur** skaltu velja **Nýtt** á flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** til að bæta línu við hnitanetið.
1. Í nýju línunni skal stilla eftirfarandi gildi:

    - **Raðnúmer:** Sláðu inn _1_.
    - **Heiti:** Sláðu inn _Frágangur á svæði_.
    - **Notkun fastrar staðsetningar:** Veldu _Fastar og lausar staðsetningar_.
    - **Leyfa neikvæðar birgðir:** Hreinsaðu þennan gátreit.
    - **Runa virk:** Hreinsaðu þennan gátreit.
    - **Áætlun:** Veldu _Sameina_.

1. Veljið **Vista** til að vista nýju aðgerðina.
1. Veldu nýju aðgerðina þína og veldu **Breyta fyrirspurn** fyrir ofan hnitanetið **Aðgerðir í staðsetningarleiðbeiningum**.
1. Svargluggi fyrirspurnar birtist þar sem þú getur valið svæðið sem á að fylla á. Þetta svæði ætti að vera sama svæði og er tilgreint í áfyllingarsniðmátinu. Veldu **Bæta við** til að bæta við röð á flipanum **Svið** til að bæta línu við hnitanetið.
1. Í nýju línunni skal stilla eftirfarandi gildi:

    - **Tafla:** _Staðir_
    - **Afleidd tafla:** _Staðsetningar_
    - **Reitur::** _Auðkenni svæðis_
    - **Skilyrði:** _GÓLF_

1. Velja skal **Í lagi** til að vista fyrirspurnina og loka glugganum.
1. Smelltu á **Vista** til að vista staðsetningarleiðbeiningarnar þínar.

## <a name="scenario"></a>Aðstæður

Þessi hluti fjallar um sýniaðstæður sem sýna hvernig á að vinna með eiginleikann.

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a>Undirbúið áskilin sýnigögn fyrir sýniaðstæðurnar

Áður en byrjað er að vinna í gegnum aðstæðurnar verður þú að virkja sýnigögn og setja upp eiginleikann eins og lýst er í þessum kafla og fyrri köflum í þessu efnisatriði.

#### <a name="use-the-usmf-legal-entity"></a>Nota USMF-lögaðilann

Til að vinna í gegnum aðstæðurnar með því að nota sýnskrárnar og sýnigildin sem eru kynnt í þessu efnisatriði verður þú að vinna á kerfi þar sem venjulegu [sýnigögnin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) eru sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

#### <a name="prepare-additional-sample-data"></a>Undirbúningur viðbótarsýnigagna

Eftir að þú hefur valið **USMF**-lögaðilann skaltu bæta við viðbótarsýnigögnum sem krafist er, eins og lýst er í hlutanum [Uppsetning á áfyllingu miðað við svæði](#setup) fyrr í þessu efnisatriði.

#### <a name="check-your-on-hand-inventory"></a>Athuga lagerbirgðir

Fylgdu þessum skrefum til að ganga úr skugga um að kerfið þitt sé með nægar birgðir til að styðja sýniaðstæðurnar.

1. Gakktu úr skugga um að lagerbirgðir séu til staðar fyrir vöruna *A0001* á tveimur mismunandi staðsetningum á tiltektarsvæðinu (*GÓLFI*) sem er tilgreint í áfyllingarsniðmátinu. Samt sem áður ættu heildarbirgðirnar að vera minni en áskilið lágmarksmagn (*50*) sem er tilgreint í áfyllingarsniðmátinu. Á þennan hátt er hægt að líkja eftir því hvernig útreikningur á sér stað fyrir allt svæðið í stað einnar staðsetningar. **Notaðu hvaða vöruhúsaferli sem er til að breyta birgðunum eftir þörfum.**
1. Gakktu úr skugga um að nægar birgðir séu fyrir vöru *A0001* á fjöldastaðsetningu sem er tilgreint í staðsetningarleiðbeiningu tiltektar á svæði þar sem áfyllingarvinnan skal taka til vörur á svæðisauðkenni *MAGN*. Heildarbirgðir verða að vera meiri en áskilið hámarksmagn (*150*) sem er tilgreint í áfyllingarsniðmátinu.
1. Valfrjálst en ráðlagt: Fylgdu eftirfarandi skrefum til að búa til leiðréttingabók birgða:

    1. Farið í **Birgðastjórnun \> Færslubókarfærslur \> Vörur \> Leiðrétting birgða**.
    1. Veljið **Nýtt**.
    1. Í svarglugganum **Stofna birgðabók** á svæðinu **Vöruhús** velur þú *61*.
    1. Veljið **Í lagi**.
    1. Á flýtiflipanum **Færslubókarlínur** notar þú hnappinn **Ný** til að bæta við þremur línum við töfluna og stilla eftirfarandi gildi. Eftir að þú hefur lokið við að setja upp hverja línu skaltu velja **Vista**.

        - **Lína 1:**

            - **Vörunúmer:** *A0001*
            - **Svæði:** *6*
            - **Vöruhús:** *61*
            - **Staðsetning:** *02A01R1S1B*
            - **Númeraplata:** Veldu fyrirliggjandi númeraplötu á listanum eða búðu til nýja númeraplötu.
            - **Magn:** *1000*

        - **Lína 2:**

            - **Vörunúmer:** *A0001*
            - **Svæði:** *6*
            - **Vöruhús:** *61*
            - **Staðsetning:** *07A01R2S1B*
            - **Númeraplata:** Veldu fyrirliggjandi númeraplötu á listanum eða búðu til nýja númeraplötu.
            - **Magn:** *15*

        - **Lína 3:**

            - **Vörunúmer:** *A0001*
            - **Svæði:** *6*
            - **Vöruhús:** *61*
            - **Staðsetning:** *07A01R1S1B*
            - **Númeraplata:** Veldu fyrirliggjandi númeraplötu á listanum eða búðu til nýja númeraplötu.
            - **Magn:** *10*

    1. Veldu **Villuleita** á aðgerðasvæðinu. Leiðréttu allar villur sem koma í ljós áður en þú ferð í næsta skref.
    1. Veldu **Bóka** á aðgerðarsvæðinu til að bóka birgðir í vöruhúsið.

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a>Sýniaðstæður: Keyra lágm./hám. áfyllingu miðað við svæði

Þegar öll áskilin sýnigögn eru til staðar, getur þú hrint af stað áfyllingu með því að fylgja þessum skrefum.

1. Fara í **Vöruhúsakerfi \> Áfylling \> Áfyllingar**.
1. Í svarglugganum **Áfylling** á flýtiflipanum **Færslur sem á að taka með** velur þú **Sía**.
1. Í svarglugganum **Fyrirspurn** á flipanum **Svið** breytir þú sjálfgefnu töflulínunni á eftirfarandi hátt:

    - **Tafla:** Veldu _Áfyllingarsniðmát_.
    - **Afleidd tafla:** Veldu _Áfyllingarsniðmát_.
    - **Svæði:** Veldu _Áfyllingarsniðmát_.
    - **Skilyrði:** Veldu _Lágm./hám. áfylling á svæði_. Þetta áfyllingarsniðmát er áfyllingarsniðmátið sem þú bjóst til meðan þú varst að undirbúa sýnigögnin fyrir þessar aðstæður.

1. Veldu **Í lagi** til að vista fyrirspurnina og opna aftur svargluggann **Áfylling**.
1. Smelltu á **Í lagi** til að keyra áfyllingarsniðmátið.

Nú er áfyllingarvinna sköpuð til að taka til birgðir af svæðinu *MAGN* og fylla það á svæðið *GÓLF*.

## <a name="notes-and-tips"></a>Athugasemdir og ábendingar

Hér eru nokkrar athugasemdir og ábending til að vinna með eiginleikann:

- Til að setja upp áfyllingarvinnu sem fer á viðeigandi svæði er hægt að tengja línur áfyllingarsniðmátsins og staðsetningarleiðbeiningar á tvo vegu:

    - Breyttu fyrirspurninni í haus staðsetningarleiðbeininganna og síaðu valda línur áfyllingarsniðmátsins.
    - Notaðu leiðbeiningarkóða í línu áfyllingarsniðmátsins og láttu hann passa við staðsetningarleiðbeiningar frágangs.

- Ef þú ert að nota kvikar staðsetningar verður áfyllingarvinnan búin annað hvort til fyrir fyrsta tiltæka staðsetningu eða fyrir staðsetningu sem er þegar með birgðum, ef aðgerð í staðsetningarleiðbeiningum er sett upp til að nota áætlun um **Sameiningu**.
- Ef þú ert að nota fasta staðsetningar í stað svæða, ættir þú að nota [venjulega lágm./hám. áfyllingu](tasks/set-up-min-max-replenishment-process.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]