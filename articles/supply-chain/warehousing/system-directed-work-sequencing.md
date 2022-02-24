---
title: Kerfisstýrð vinnuröðun
description: Þetta efnisatriði veitir upplýsingar um kerfisstýrða vinnuröðun. Þessi aðgerð gerir þér kleift að flokka og sía verkbeiðnir sem kerfið býður notendum til framkvæmdar. Það er gagnlegt við aðstæður þar sem þörf er á viðbótarskilyrðum til að keyra tiltektarferli vöruhússins.
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 3811486a31d079cac7f7c27ea6323f16de4478d5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970207"
---
# <a name="system-directed-work-sequencing"></a>Kerfisstýrð vinnuröðun

[!include [banner](../includes/banner.md)]

Kerfisstýrð vinnuröðun gerir þér kleift að flokka og sía verkbeiðnir sem kerfið býður notendum til framkvæmdar. Það er gagnlegt við aðstæður þar sem þörf er á viðbótarskilyrðum (t.d. tímasetningu sendingar, tiltektarsvæði, staðsetningarforstillingu eða sambland ólíkra skilyrða) til að keyra tiltektarferli vöruhússins.

Þessi virkni víkkar út núverandi kerfisstýrða tiltektaraðgerð með því að bæta við kerfisstýrðri fyrirspurnapöntun þar sem notendur geta sett upp röð og eina eða fleiri fyrirspurnir sem munu meta allar verkbeiðnir sem eru búnar til. Aðeins verkbeiðnir sem uppfylla skilyrðin sem eru tilgreind í uppsetningu valmyndaratriðis í fartækinu verða fangaðar og kynntar.

Þess vegna gerir þessi virkni kleift frekari fínstillingu á tiltektarferlum vöruhússins þar sem hún greinir verkbeiðnir sem samsvara tilgreindum skilyrðum, úthlutar þeim á rétt valmyndaratriði fartækisins og birtir síðan starfsmanni, miðað við tiltekinn hæfnigrunn, búnað við tiltekt eða önnur skilyrði.

> [!NOTE]
> Nota verður mörg valmyndaratriði fartækisins ef þörf er á öðrum skilyrðum.

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a>Kveikja á eiginleikanum kerfisstýrð vinnuröðun fyrir alla stofnunina/fyrirtækið

Áður en þú getur notað kerfisstýrða vinnuröðun verður að vera kveikt á eiginleikanum í kerfinu þínu. Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Þar er eiginleikinn sýndur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Kerfisstýrð vinnuröðun fyrir alla stofnunina/fyrirtækið*

## <a name="setup"></a>Setja upp

### <a name="make-demo-data-available"></a>Bjóða upp á sýnigögn

Til að vinna í gegnum aðstæðurnar með því að nota gildin sem eru kynnt í þessu efnisatriði verður þú að vinna á kerfi þar sem venjulegu sýnigögnin eru sett upp. Þar að auki verður þú að velja **USMF**-lögaðila. Aðstæðurnar nota vöruhús *51* úr sýnigögnunum.

> [!IMPORTANT]
> Áður en þú losar pantanir til vöruhússins skaltu ganga úr skugga um að tiltektarstaðsetningar hafi nægar birgðir fyrir öll atriðin á pöntunum.
>
> Sjálfgefin USMF-gögn ættu að styðja þessar aðstæður. Ef þú notar ekki sýnigögn skaltu skoða stillingu **Staðsetningarleiðbeininga** til að komast að því hvaða tiltektarstaðsetningar eru notaðar við tiltekt sölupöntunar. Ef þú verður að breyta birgðum geturðu búið til handvirkar birgðahreyfingar, notað áfyllingu eða notað hvaða annað flæði sem er.

### <a name="set-up-a-mobile-device-menu-item"></a>Setja upp valmyndaratriði fartækis

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Veldu **Tiltekt sölu – Kerfi** á listanum yfir valmyndaratriði fartækis. Áskilið valmyndaratriði ætti þegar að vera til. 
1. Staðfestið eftirfarandi stillingar:

    - Á flýtiflipanum **Almennt** ætti svæðið **Stjórnað af** að vera stillt á *Kerfisstýrt*.
    - Flýtiflipinn **Vinnuklasar** ætti að sýna eftirfarandi stillingar.

        | Auðkenni vinnuklasa | Gerð verkpöntunar |
        |---|---|
        | Sala | Sölupantanir |
        | Tiltekt sölupöntunar | Sölupantanir |

1. Á aðgerðarsvæðinu velur þú **Kerfisstýrðar fyrirspurnir vinnuröðunar**.
1. Veljið **Breyta**.
1. Eyða núverandi línu og staðfestu síðan aðgerðina með því að velja **Já**.
1. Veldu **Nýtt** á aðgerðasvæðinu til að búa til línu.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Raðnúmer:** *1*
    - **Lýsingarsvæði:** *Vinnumagn minna en 20 og fer minnkandi*

1. Veljið **Vista**.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.
1. Á flipanum **Samtengingar** skaltu stækka stigveldi samtengingar til að sýna töfluna **Vinnulínur**.
1. Veldu töflutenginguna **Vinnulínur**.
1. Velja **Bæta við töflusamtengingu**.
1. Finndu og veldu línuna á listanum sem birtist sem hefur eftirfarandi stillingar:

    - **Samtengingarstilling:** *n:1*
    - **Tengsl:** *Staðsetningar (Staðsetning)*

1. Veljið **Velja**.

    Staðsetningum er bætt við töflutenginguna.

1. Veldu **Bæta við** til að bæta við röð á flipanum **Röðun**.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Tafla:** *Vinnulínur*
    - **Afleidd tafla:** *Vinnulínur*
    - **Svæði:** *Vinnumagn* (Í skilaboðaglugganum sem birtist skaltu velja **Já** til að bæta flokkun við þetta svæði).
    - **Leitarstefna:** *Lækkandi*

1. Smellt er á flipann **Svið**.

    Ef aðeins skal hafa sérstök vinnuskilyrði í röðinni, geturðu tilgreint þau á flipanum **Svið**. Í þessu dæmi viltu aðeins taka með vinnu þar sem magnið er minna en 20 ea (lægsta mælieiningin).

    Athugaðu að tilteknar línur eru þegar innifaldar. Ekki ætti að fjarlægja þessar línur.

1. Smellið á **Bæta við** til að bæta við nýrri línu.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Tafla:** *Vinnulínur*
    - **Afleidd tafla:** *Vinnulínur*
    - **Svæði:** *Vinnumagn birgða*
    - **Skilyrði:** *\<20* (minna en 20)

1. Smellið á **Bæta við** til að bæta við annarri línu.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Tafla:** *Vinnulínur*
    - **Afleidd tafla:** *Vinnulínur*
    - **Svæði:** *Gerð vinnu*
    - **Skilyrði:** *Tiltekt*

1. Smellið á **Bæta við** til að bæta við annarri línu.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Tafla:** *Staðir*
    - **Afleidd tafla:** *Staðsetningar*
    - **Reitur:** *Auðkenni forstillingar staðsetningar*
    - **Skilyrði:** *!STIG*

        > [!IMPORTANT]
        > Gættu þess að setja upphrópunarmerki (*!*) fyrir framan *STIG*..

1. Veldu **Í lagi** til að vista og loka fyrirspurninni.
1. Veljið **Vista**.
1. Lokið síðunni til að fara aftur á síðuna **Valmyndaratriði fartækis**.

> [!NOTE]
> Þessi uppsetning skilgreinir skilyrðin sem verða notuð til að mata valmyndaratriði fartækis með tækri vinnu. Ef þú bætir fleiri skilyrðalínum við fyrirspurnina mun kerfið nota fyrirspurnalínuna sem hefur lægsta raðnúmer fyrst. Með öðrum orðum, öll tæk vinna fyrir raðnúmer 1 verða kynnt notandanum fyrst og síðan öll vinna fyrir raðnúmer 2. Þess vegna, ef nota þarf tiltekið svið og flokkun saman, ætti að tilgreina þau í sömu fyrirspurninni fyrir kerfisstýrðu vinnuröðina.
>
> Þessi uppsetning fangar alla vinnu sem hafa að minnsta kosti eina línu þar sem magnið er minna en 20 ea. Þess vegna, ef vinnan hefur línu þar sem magnið er nákvæmlega 20 ea eða meira en 20 ea, mun það vera gilt, að því tilskildu að það hafi einnig að minnsta kosti eina línu þar sem magnið er minna en 20 ea.

### <a name="location-directives"></a>Staðsetningarleiðbeiningar

Ef þú ert að nota sjálfgefin Contoso gögn þarf ekki að breyta fyrirspurninni um aðgerðir í staðsetningarleiðbeiningum. Hins vegar, til að ganga úr skugga um að staðsetningarleiðbeiningarnar fangi atriðin í sölupöntunum þegar þú notar aðgerðina í umhverfi sem ekki er frá Contoso skaltu búa til nýjar staðsetningarleiðbeiningar. Fylgdu þessum skrefum til að staðfesta stillingarnar í sýniútgáfuumhverfinu.

1. Farðu í **Vöruhúsakerfi** \> **Uppsetning** \> **Staðsetningarleiðbeiningar**.
1. Í reitnum **Gerð verkbeiðni** velurðu *Sölupantanir*.
1. Veldu staðsetningarleiðbeiningarnar sem heita *51 Tiltekt*.
1. Á flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** velur þú línuna fyrir aðgerðina **Tiltekt**.
1. Veldu **Breyta fyrirspurn** fyrir ofan hnitanetið.
1. Farðu aftur yfir fyrirspurnina **Svið**.

    1. Leitaðu að línunni þar sem svæðið **Svæði** er stillt á *Staðsetning*.
    2. Gakktu úr skugga um að svæðið **Skilyrði** sé autt (þ.e. að engar takmarkanir séu til staðar).

## <a name="scenario"></a>Aðstæður

### <a name="create-sales-order-picking-work"></a>Búa til tiltektarvinnu sölupöntunar

Áður en kerfisstýrð tiltekt er keyrð ætti að búa til einhverja vinnu á útleið. Fyrir þessar aðstæður muntu búa til fjórar sölupantanir sem eru byggðar á tilgreindum fyrirspurnum um kerfisstýrða vinnuröð.

Hægt er að taka frá birgðir sjálfkrafa fyrir hverja sölupöntun fyrir sig. Þar af leiðand er ekki hægt að taka fráteknar birgðir út úr vöruhúsi fyrir aðra pöntun nema birgðafrátektin eða hluti birgðafrátekningar sé afturkölluð.

Þú losar síðan hverja sölupöntun til vöruhússins til að búa til vinnu á útleið.

#### <a name="sales-order-1"></a>Sölupöntun 1

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Í aðgerðarúðunni velurðu **Nýtt** til að búa til sölupöntun 1.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - Í hlutanum **Viðskiptavinur** skaltu stilla svæðið **Viðskiptavinalykill** á *US-004*.
    - Í hlutanum **Almennt** stillir þú reitinn **Vöruhús** á *51*.

1. Veldu **Í lagi** til að loka svarglugganum. Skráið hjá ykkur sölupöntunarnúmerið.
1. Bættu línu við nýju sölupöntunina og stilltu eftirfarandi gildi:

    - **Vörunúmer:** *M9200*
    - **Magn:** *20*

1. Á valmyndinni **Birgðir** fyrir ofan hnitanetið smellir þú á **Frátekning**.
1. Í síðunni **Frátekning** skal velja **Frátektarlota** til að taka frá birgðirnar.
1. Lokaðu síðunni **Frátekning**.
1. Á aðgerðasvæðinu, á flipanum **Vöruhús**, skal velja **Losa í vöruhús** til að búa til vinnu fyrir vöruhúsið.

    Þú færð upplýsingaboð sem sýna bylgjuauðkennið og sendingarauðkennin sem voru búin til fyrir sölupöntunina.

#### <a name="sales-order-2"></a>Sölupöntun 2

1. Í aðgerðarúðunni velurðu **Nýtt** til að búa til sölupöntun 2.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - **Viðskiptavinalykill:** *US-007*
    - **Vöruhús:** *51*

1. Veldu **Í lagi** til að loka svarglugganum. Skráið hjá ykkur sölupöntunarnúmerið.
1. Bættu línu við nýju sölupöntunina og stilltu eftirfarandi gildi:

    - **Vörunúmer:** *M9200*
    - **Magn:** *5*

1. Veldu **Bæta við línu** til að bæta við annarri línu og stilltu eftirfarandi gildi:

    - **Vörunúmer:** *M9201*
    - **Magn:** *1*

1. Taka frá birgðir fyrir báðar línur.
1. Losa pöntun í vöruhúsið.

#### <a name="sales-order-3"></a>Sölupöntun 3

1. Í aðgerðarúðunni velurðu **Nýtt** til að búa til sölupöntun 3.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - **Viðskiptavinalykill:** *US-009*
    - **Vöruhús:** *51*

1. Veldu **Í lagi** til að loka svarglugganum. Skráið hjá ykkur sölupöntunarnúmerið.
1. Bættu línu við nýju sölupöntunina og stilltu eftirfarandi gildi:

    - **Vörunúmer:** *M9200*
    - **Magn:** *7*

1. Veldu **Bæta við línu** til að bæta við annarri línu og stilltu eftirfarandi gildi:

    - **Vörunúmer:** *M9202*
    - **Magn:** *8*

1. Taka frá birgðir fyrir báðar línur.
1. Losa pöntun í vöruhúsið.

#### <a name="sales-order-4"></a>Sölupöntun 4

1. Í aðgerðarúðunni velurðu **Nýtt** til að búa til sölupöntun 4.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - **Viðskiptavinalykill:** *US-010*
    - **Vöruhús:** *51*

1. Veldu **Í lagi** til að loka svarglugganum. Skráið hjá ykkur sölupöntunarnúmerið.
1. Bættu línu við nýju sölupöntunina og stilltu eftirfarandi gildi:

    - **Vörunúmer:** *M9200*
    - **Magn:** *25*

1. Veldu **Bæta við línu** til að bæta við annarri línu og stilltu eftirfarandi gildi:

    - **Vörunúmer:** *M9202*
    - **Magn:** *10*

1. Taka frá birgðir fyrir báðar línur.
1. Losa pöntun í vöruhúsið.

### <a name="get-work-ids-for-the-work-that-was-created"></a>Heimta vinnuauðkenni fyrir vinnuna sem var búin til

1. Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnu**.
1. Sía á svæðinu **Vöruhús** þannig að aðeins vinna fyrir vöruhús *51* birtist.
1. Fjögur vinnuauðkenni ættu að vera búin til. Skráið niður vinnuauðkenni hverrar sölupöntunar fyrir sig.

    | Kenni sölupöntunar | Vinnukenni | Vinnumagn |
    |---|---|---|
    | Sölupöntun 1 | Vinnuauðkenni 1 | 20 ea |
    | Sölupöntun 2 | Vinnuauðkenni 2 | 6 ea (summan af báðum línum) |
    | Sölupöntun 3 | Vinnuauðkenni 3 | 15 ea (summan af báðum línum) |
    | Sölupöntun 4 | Vinnuauðkenni 4 | 35 ea (summan af báðum línum) |

Áður en þú keyrir flæðið í fartækið skaltu ganga úr skugga um að aðeins vinnan sem þú varst að búa til hafi stöðuna *Opin* fyrir vöruhús *51* og gerð verkbeiðni fyrir *Sölupöntun*. Annars geta niðurstöður prófsins verið breytilegar, vegna þess kerfisstýrð tiltekt felur í sér alla tæka vinnu.

1. Opnaðu **Vöruhúsakerfi \> Vinna \> Á útleið \> Opin söluvinna**.
1. Í hnitanetinu **Opin söluvinna** síaðu svæðið **Vöruhús** þannig að aðeins vinna fyrir vöruhús *51* birtist.
1. Gakktu úr skugga um að aðeins birtist vinnuauðkennin fjögur sem þú bjóst til áður.
1. Lokaðu síðunni **Vinna**.

### <a name="mobile-device-flow-execution"></a>Framkvæmd flæðis í fartæki

Miðað við uppsetninguna fæðir kerfið notanda vinnunni sem er raðað frá mesta magni vinnulínu til þeirrar lægstu. Magnið á hverri línu verður minna en 20 ea.

Hafðu í huga að þessi uppsetning fangar alla vinnu sem hafa að minnsta kosti eina línu þar sem magnið er minna en 20 ea. Þess vegna, ef verkið hefur aðra línu þar sem magnið er nákvæmlega 20 ea eða meira en 20 ea, mun það einnig gilda.

#### <a name="mobile-app"></a>Fartækjaforrit

1. Skráðu þig inn í vöruhúsaforritið sem notandi í vöruhúsi *51*.
1. Opnaðu **Á útleið \> Sölutiltekt - Kerfi**.

    Tiltektarskrefið fyrir vinnuauðkenni *4* birtist. Þetta vinnuauðkenni birtist fyrst vegna uppsetningarinnar á kerfisstýrðri fyrirspurnarpönun, þar sem þú tilgreindir að vinnan ætti að vera raðað miðað við lækkandi magn vinnulínu.

1. Ljúktu valinni tiltekt og frágangi til að loka vinnuauðkenninu.

    Næst birtist vinnuauðkenni *3*. Ein af vinnulínum hennar er næst í röðinni, byggð á magni vinnulínunnar.

1. Ljúktu tiltekt og frágangi til að loka vinnuauðkenninu.

    Næst birtist vinnuauðkenni *2*. Tiltektarlína þessarar vinnu er næst í röðinni.

1. Ljúktu tiltekt og frágangi til að loka vinnuauðkenninu.

    Þú ættir ekki að sjá frekari vinnu birtast. Vinnuauðkenni *1* er ekki gjaldgengt fyrir þetta valmyndaratriði fartækis, því fyrirspurnin tilgreinir að vinnuhausar séu einungis taldir ef magn á vinnulínunum er minna en 20 ea.

## <a name="tips"></a>Ábendingar

Fyrirspurnir um kerfisstýrða vinnuröð eru *sameiginlegar*. Mikilvægt er að þú hafir slíkt í huga við tilteknar uppsetningar. Til dæmis viltu að tiltekinn valmyndaratriði vinni aðeins úr vinnu þar sem vinnueiningin er *ea*, og þú tilgreinir þá takmörkun á flipanum **Svið** á fyrirspurninni. Í þessu tilfelli verður starfsmaðurinn mataður á allri vinnu þar sem að minnsta kosti ein vinnulína hefur vinnueininguna stillta á *ea*. Þess vegna gæti þessi vinna einnig falið í sér vinnu þar sem vinnulínur eru með aðrar vinnueiningar en *ea* (eins og *kassa* eða *vörubretti*). Fyrirspurnin útilokar eingöngu vinnu þar sem engin vinnulína hefur vinnueininguna stillt á *ea*.

Þess vegna, í dæminu við þessar aðstæður, var vinnuauðkenni *4* einnig fangað af fyrirspurninni. Þegar það var búið var tveimur línum bætt við: ein fyrir 25 ea og önnur fyrir 10 ea. Vinnan birtist notandanum samt sem áður, því að minnsta kosti ein vinnulína hefur minna magn en 20 ea.

Miðað við aðstæðurnar, getur þú komið í veg fyrir þessa aðgerð með því að nota vinnuhlé.
