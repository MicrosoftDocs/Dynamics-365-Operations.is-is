---
title: Kynning á eiginleikanum umsjón hönnunarbreytinga
description: Þessi grein veitir leiðsögn frá enda til enda sem sýnir hvernig á að vinna með verkfræðilega breytingastjórnun.
author: t-benebo
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 65ff30632a54b0b7cadbfe663698d466d41abe47
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334896"
---
# <a name="engineering-change-management-feature-walkthrough"></a>Kynning á eiginleikanum umsjón hönnunarbreytinga

[!include [banner](../includes/banner.md)]

Þessi grein veitir leiðsögn frá enda til enda sem sýnir hvernig á að vinna með verkfræðilega breytingastjórnun. Farið er í gegnum mikilvægustu þættina:

- Skilgreining á grunneiginleikum
- Hvernig hönnunarfyrirtæki stofnar nýja hönnunarafurð
- Hvernig hönnunarfyrirtæki gefur út hönnunarafurð til staðbundins fyrirtækis
- Hvernig staðbundið fyrirtæki getur yfirfarið og samþykkt afurð sem hönnunarfyrirtæki hefur gefið út til þess
- Hvernig staðbundið fyrirtæki getur notað hönnunarafurð í hefðbundnum færslum
- Hvernig á að bæta hönnunarafurð við sölupöntun
- Hvernig á að óska eftir breytingum á hönnunarafurð með því að stofna beiðni um hönnunarbreytingu
- Hvernig á að áætla og innleiða umbeðnar breytingar með því að stofna pöntun hönnunarbreytingar
- Hvernig á að gefa út afurð sem hefur verið breytt

Allar æfingar í þessari grein nota staðlað sýnishornsgögn sem eru veitt fyrir Microsoft Dynamics 365 Supply Chain Management. Auk þess byggir hver æfing á fyrri æfingunni. Þess vegna mælum við með því að þú farir í gegnum æfingarnar í réttri röð, frá upphafi til enda, sérstaklega ef þú hefur aldrei notað eiginleika hönnunarbreytingastjórnunar áður. Á þennan hátt öðlastu víðtækari skilning á eiginleikanum.

## <a name="set-up-for-the-sample-scenario"></a>Setja upp fyrir sýnidæmið

Til að fylgja sýnishorninu sem er að finna í þessari grein, verður þú fyrst að undirbúa eiginleikann með því að gera kynningargögn aðgengileg og bæta við nokkrum sérsniðnum færslum.

Áður en þú reynir að gera eitthvað af æfingunum í restinni af þessari grein skaltu fylgja leiðbeiningunum í öllum eftirfarandi undirköflum. Þessir undirkaflar kynna einnig til sögunnar nokkrar mikilvægar stillingasíður sem þú munt nota þegar þú setur upp umsjón hönnunarbreytinga fyrir þitt eigið fyrirtæki.

### <a name="make-standard-demo-data-available"></a>Gera stöðluð sýnigögn aðgengileg

Vinna á kerfi þar sem staðall [kynningargögn](../../fin-ops-core/fin-ops/get-started/demo-data.md) er sett upp. Stöðluð sýnigögn bæta við gögnum fyrir nokkrar sýniútgáfur af lögaðilum (fyrirtæki og stofnanir). Meðan þú fikrar þig áfram í gegnum æfingarnar, notarðu fyrirtækið hægra megin á yfirlitsstikunni til að skipta á milli fyrirtækis (*DEMF*) sem sett er upp sem *hönnunarfyrirtæki* og annars fyrirtækis (*USMF*) sem sett er upp sem *rekstrarfyrirtæki*.

### <a name="set-up-an-engineering-organization"></a>Setja upp hönnunarfyrirtæki

Hönnunarfyrirtæki á hönnunargögnin og er ábyrgt fyrir afurðarhönnun og afurðarbreytingum. Til að setja upp hönnunarfyrirtækin skal fylgja þessum skrefum.

1. Farið í **Umsjón hönnunarbreytinga &gt; Uppsetning &gt; Hönnunarfyrirtæki**.
1. Veljið **Ný** til að bæta nýrri línu við hnitanetið og stillið eftirfarandi gildi fyrir hana:

    - **Hönnunarfyrirtæki:** *DEMF*
    - **Heiti fyrirtækis:** *Contoso Entertainment System Germany*

    ![Hönnunarfyrirtæki bætt við.](media/engineering-org.png "Hönnunarfyrirtæki bætt við")

### <a name="set-up-the-version-product-dimension-group"></a>Setja upp afurðavíddaflokk útgáfunnar

1. Farið í **Afurðaupplýsingastjórnun &gt; Uppsetning &gt; Vídda- og afbrigðaflokkar &gt; Afurðavíddaflokkur**.
1. Veljið **Nýr** til að stofna afurðavíddaflokk.
1. Stillið reitinn **Heiti** á *Útgáfa*.
1. Veljið **Vista** til að vista nýju víddina og hlaða gildunum í flýtiflipann **Afurðarvíddir**.
1. Í flýtiflipanum **Afurðarvíddir** skal stilla **Útgáfa** sem virka afurðarvídd.

    ![Afurðavíddaflokki bætt við.](media/product-dimension-groups.png "Afurðavíddaflokki bætt við")

### <a name="set-up-product-lifecycle-states"></a>Setja upp lífferilsstöður afurðar

Um leið og hönnunarafurð fer í gegnum líftíma sinn er mikilvægt að geta stjórnað hvaða færslur eru leyfðar fyrir hverja líftímastöðu. Til að setja upp lífferilsstöður afurðar skal fylgja þessum skrefum.

1. Farið í **Umsjón hönnunarbreytinga &gt; Uppsetning &gt; Lífferilsstaða afurðar**.
1. Veljið **Ný** til að bæta við lífferilsstöðu og stillið eftirfarandi gildi fyrir hana:

    - **Staða:** *Rekstur*
    - **Lýsing:** *Rekstur*

1. Veljið **Vista** til að vista nýju lífferilsstöðuna og hlaða gildum í flýtiflipann **Virkjaðir viðskiptaferlar**.
1. Í flýtiflipanum **Virkjaðir viðskiptaferlar** skal velja viðskiptaferlana sem eiga að vera aðgengilegir. Fyrir þetta dæmi skal hafa reitinn **Stefna** stilltan á *Virkjaður* fyrir alla viðskiptaferla.

    ![Viðskiptaferlar virkjaðir fyrir lífferilsstöðu.](media/product-lifecycle-states-1.png "Viðskiptaferlar virkjaðir fyrir lífferilsstöðu")

1. Veljið **Ný** til að bæta við annarri lífferilsstöðu og stillið eftirfarandi gildi fyrir hana:

    - **Staða:** *Frumgerð*
    - **Lýsing:** *Frumgerð*

1. Veljið **Vista** til að vista nýju lífferilsstöðuna og hlaða gildum í flýtiflipann **Virkjaðir viðskiptaferlar**.
1. Í flýtiflipanum **Virkjaðir viðskiptaferlar** skal velja viðskiptaferlana sem eiga að vera aðgengilegir. Í þessu dæmi skal stilla reitinn **Stefna** á *Virkjað með viðvörun* fyrir alla viðskiptaferla.

    ![Viðskiptaferlar virkjaðir (með viðvörun) fyrir lífferilsstöðu.](media/product-lifecycle-states-2.png "Viðskiptaferlar virkjaðir (með viðvörun) fyrir lífferilsstöðu")

### <a name="set-up-a-version-number-rule"></a>Setja upp reglu um útgáfunúmer

1. Farið í **Umsjón hönnunarbreytinga &gt; Uppsetning &gt; Regla um útgáfunúmer afurðar**.
1. Veljið **Ný** til að bæta við reglu og stillið eftirfarandi gildi fyrir hana:

    - **Heiti:** *Sjálfvirk*
    - **Númeraregla:** *Sjálfvirk*
    - **Snið:** *V-\#\#*

    ![Reglu um útgáfunúmer afurðar bætt við.](media/version-number-rule.png "Reglu um útgáfunúmer afurðar bætt við")

### <a name="set-up-a-product-release-policy"></a>Setja upp útgáfureglu afurðar

1. Farið í **Umsjón hönnunarbreytinga &gt; Uppsetning &gt; Útgáfustefnur afurðar**.
1. Veljið **Ný** til að bæta við útgáfustefnu og stillið eftirfarandi gildi fyrir hana:

    - **Heiti:** *Íhlutir*
    - **Lýsing:** *Íhlutir*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Gerð afurðar:** *Afurð*
    - **Nota sniðmát:** *Alltaf*
    - **Virkt:** *Já*

1. Í flýtiflipanum **Allar afurðir** skal velja **Bæta við** til að bæta við línu og stilla eftirfarandi gildi fyrir hana:

    - **Fyrirtæki:** *DEMF*
    - **Sniðmát losaðrar afurðar:** *D0006*

1. Veljið **Bæta við** til að bæta við annarri línu og stillið eftirfarandi gildi fyrir hana:

    - **Kenni fyrirtækisreikninga:** *USMF*
    - **Sniðmát losaðrar afurðar:** *D0006*
    - **Taka á móti uppskrift:** Veljið þennan gátreit.
    - **Afrita samþykki uppskriftar:** Veljið þennan gátreit.
    - **Afrita virkjun uppskriftar:** Veljið þennan gátreit.
    - **Taka á móti leið:** Veljið þennan gátreit.
    - **Afrita samþykki leiðar:** Veljið þennan gátreit.
    - **Afrita leið virkjunar:** Veljið þennan gátreit.

    ![Útgáfureglu afurðar bætt við.](media/product-release-policy.png "Útgáfureglu afurðar bætt við")

### <a name="set-up-an-engineering-product-category"></a>Setja upp tegund hönnunarafurðar 

Flokkar hönnunarafurðar bjóða upp á grunninn til að stofna hönnunarafurðir (þ.e. afurðir sem fá úthlutaða útgáfu og er stýrt í gegnum umsjón hönnunarbreytingar). Til að setja upp flokka hönnunarafurða skal fylgja þessum skrefum.

1. Farið í **Umsjón hönnunarbreytinga &gt; Upplýsingar um flokka hönnunarafurða**.
1. Veldu **Nýtt** til að búa til flokk.
1. Í flýtiflipanum **Upplýsingar** skal stilla eftirfarandi gildi:

    - **Heiti:** *Íhlutir*
    - **Hönnunarfyrirtæki:** *DEMF*
    - **Gerð afurðar:** *Afurð*
    - **Rekja útgáfu í færslum:** *Já*
    - **Afurðavíddaflokkur:** *Útgáfa*
    - **Lífferilsstaða afurðar við stofnun:** *Rekstur*
    - **Númeraregla útgáfu:** *Sjálfvirk*
    - **Framfylgja virkni:** *Nei*
    - **Nota númerakerfi númerareglu:** *Nei*
    - **Nota nafnakerfi heitisreglu:** *Nei*
    - **Nota nafnakerfi lýsingarreglu:** *Nei*

1. Í flýtiflipanum **Útgáfustefna** skal stilla reitinn **Útgáfustefna afurðar** á *Íhlutir*.
1. Veldu **Vista**.

    ![Flokki hönnunarafurðar bætt við.](media/product-category-details.png "Flokki hönnunarafurðar bætt við")

### <a name="set-up-product-acceptance-conditions"></a>Setja upp skilyrði afurðasamþykktar

1. Nota skal fyrirtækjavalið hægra megin á yfirlitsstikunni til að skipta yfir í lögaðilann (fyrirtækið) *USMF*.
1. Farið í **Umsjón hönnunarbreytinga &gt; Uppsetning &gt; Færibreytur fyrir umsjón hönnunarbreytinga**.
1. Í flipanum **Útgáfustýring**, í hlutanum **Afurðasamþykki**, skal stilla reitinn **Afurðasamþykki** á *Handvirkt*.

    ![Skilyrði afurðasamþykkis sett upp.](media/engineering-change-management-parameters.png "Skilyrði afurðasamþykkis sett upp")

## <a name="create-a-new-engineering-product"></a>Stofna nýja hönnunarafurð

Hönnunarafurð er afurð sem er úthlutað útgáfu og stýrð í gegnum umsjón hönnunarbreytinga. Með öðrum orðum er hægt að hafa stjórn á breytingum meðan á líftíma hennar stendur og upplýsingar um breytingarnar verða vistaðar með því að nota pantanir hönnunarbreytinga. Til að stofna hönnunarafurðir skal fylgja þessum skrefum.

1. Gangið úr skugga um að vera í lögaðila hönnunarfyrirtækisins (*DEMF* fyrir þetta dæmi). Notið fyrirtækisvalið hægra megin á yfirlitsstikunni eftir þörfum.
1. Opnið **Útgefnar afurðir** með því að fylgja einu þessara skrefa:

    - Opna **Afurðaupplýsingastjórnun &gt; Afurðir &gt; Útgefnar afurðir**.
    - Farið í **Umsjón hönnunarbreytinga &gt; Almennt &gt; Útgefnar afurðir**.

1. Á aðgerðasvæðinu, í flipanum **Afurð**, í flokknum **Ný**, skal velja **Hönnunarafurð**.
1. Sláið inn eftirfarandi gildi í svarglugganum **Ný afurð**:

    - **Tegund hönnunarafurðar:** *Íhlutir*
    - **Afurðarnúmer:** *Z0001*
    - **Afurðarheiti:** *Hátalarasett*

    ![Hönnunarafurð bætt við.](media/new-product-dialog.png "Hönnunarafurð bætt við")

    Athugið að reiturinn **Útgáfa** er sjálfkrafa stilltur með því að nota númerareglu afurðarútgáfu sem sett var upp fyrr.

1. Veljið **Í lagi** til að stofna afurðina og loka svarglugganum.
1. Upplýsingasíða fyrir nýju afurðina er opnuð. Takið eftir að þegar er búið að fylla út gildi fyrir suma reiti á borð við **Geymsluvíddarflokk**, **Rakningarvíddarflokk** og/eða **Vörulíkanaflokk**. Þessir reitir voru sjálfkrafa stilltir vegna þess að verið er að gefa út afurðina í lögaðilanum *DEMF* og hún notar afurðarlosunarregluna *Íhlutir*, sem tengist hönnunarafurðartegundinni *Íhlutir*. Vegna þess að áður var notuð varan *D0006* sem sniðmát til að setja upp línu fyrir lögaðilann *DEMF*, voru gildin sem fyllt voru út tekin frá vöru *D0006*.

    ![Upplýsingar um losaðar afurðir.](media/product-details.png "Upplýsingar um losaðar afurðir")

1. Á aðgerðasvæðinu, í flipanum **Hönnun**, í flokknum **Umsjón hönnunarbreytinga**, skal velja **Hönnunarútgáfur** til að skoða útgáfur afurðarinnar.

    ![Hönnunarútgáfur.](media/engineering-versions-list.png "Hönnunarútgáfur")

1. Takið eftir að á síðunni **Hönnunarútgáfur** er aðeins ein útgáfa fyrir afurðina, og hún er virk.
1. Veljið útgáfuna til að skoða upplýsingar um hana.

    ![Upplýsingar um útgáfu hönnunar.](media/engineering-version-details.png "Upplýsingar um útgáfu hönnunar")

1. Á síðunni **Útgáfa hönnunar**, í flýtiflipanum **Uppskrift**, skal velja **Stofna uppskrift**.
1. Í svarglugganum **Stofna uppskrift** skal stilla eftirfarandi gildi:

    - **Númer uppskriftar:** Z0001
    - **Heiti:** Hátalarasett
    - **Svæði:** 1

    ![Stofna uppskrift.](media/create-bom.png "Stofna uppskrift")

1. Veljið **Í lagi** til að bæta uppskriftinni við og loka svarglugganum.
1. Í flýtiflipanum **Uppskriftir** skal velja **Uppskrift**.
1. Á síðunni **Uppskriftir**, í flýtiflipanum **Línur uppskriftar**, skal bæta þremur línum við, eina fyrir hvert vörunúmer *D0001*, *D0003* og *D0006*.

    ![Uppskriftarlínum bætt við.](media/bom.png "Uppskriftarlínum bætt við")

1. Veldu **Vista**.
1. Lokið síðunni.
1. Á síðunni **Útgáfa hönnunar**, í flýtiflipanum **Uppskrift**, skal velja **Samþykkja**.
1. Í svarglugganum sem birtist skal smella á **Í lagi**.

    ![Uppskrift samþykkt.](media/approve-dialog.png "Uppskrift samþykkt")

1. Á síðunni **Útgáfa hönnunar**, í flýtiflipanum **Uppskrift**, skal velja **Virkja**.
1. Takið eftir að gátreitirnir **Virk** og **Samþykkt** eru valin fyrir uppskriftina.

    ![Virk og samþykkt uppskrift.](media/approved-bom.png "Virk og samþykkt uppskrift")

1. Lokið síðunni.

## <a name="release-an-engineering-product-to-a-local-company"></a><a name="release"></a>Gefa út hönnunarafurð hjá staðbundnu fyrirtæki

Afurðin hefur nú verið hönnuð af hönnunardeildinni. Fyrir þetta dæmi er afurðin frumgerð sem hönnuður hefur hannað fyrir viðskiptavin. Vegna þess að viðskiptavinurinn er viðskiptavinur lögaðilans *USMF* þarf að gefa út afurðina í þeim lögaðila.

1. Haldið lögaðilanum stilltum á *DEMF*. (Nota skal fyrirtækisvalið hægra megin á yfirlitsstikunni eftir þörfum.)
1. Opna **Afurðaupplýsingastjórnun &gt; Afurðir &gt; Útgefnar afurðir**.
1. Veljið afurð *Z0001*.
1. Á aðgerðasvæðinu, í flipanum **Afurð**, í flokknum **Vinna með**, skal velja **Gefa út skipulag afurðar** til að opna leiðsagnarforritið **Gefa út afurðir**.
1. Á síðunni **Velja hönnunarafurðir til að gefa út** skal velja gátreitinn **Velja** fyrir afurð *Z0001*.

    ![Hönnunarafurðir valdar til útgáfu.](media/select-eng-product-to-release.png "Hönnunarafurðir valdar til útgáfu")

1. Veljið **Upplýsingar um útgáfu**.
1. Síðan **Upplýsingar um útgáfu afurðar** birtist, þar sem hægt er að fara yfir upplýsingar afurðarinnar sem verður gefin út og skipulag afurðarinnar. Takið eftir að valkosturinn **Senda uppskrift** er stilltur á *Já*. Þess vegna verður bæði afurðin *Z0001* og allar vörur undir henni í uppskriftinni gefnar út.

    Hægt er að velja hvaða undirvöru sem er á svæðinu vinstra megin til að fara yfir upplýsingar hennar. Ef einhver undirvara er með uppskrift, er einnig hægt að velja um að gefa út uppskrift þeirrar undirvöru.

    ![Upplýsingar um útgáfu afurðar yfirfarnar.](media/product-release-details.png "Upplýsingar um útgáfu afurðar yfirfarnar")

1. Lokið síðunni til að fara aftur í leiðsagnarforritið **Gefa út afurðir**.
1. Veljið **Áfram** til að opna síðuna **Velja afurðir til útgáfu**. Ef valdar voru staðlaðar (ekki hannaðar) afurðir, munu þær birtast á þessari síðu. Hafa skal í huga að þegar staðalafurð er gefin út með því að velja **Gefa út skipulag afurðar**, er uppskrift hennar og leið einnig gefin út.

    ![Staðlaðar afurðir valdar til útgáfu.](media/select-std-product-to-release.png "Staðlaðar afurðir til að gefa út valdar")

1. Veljið **Áfram** til að opna síðuna **Velja afurðarafbrigði til útgáfu**. Í þessu dæmi eru engin afbrigði.
1. Veljið **Áfram** til að opna síðuna **Velja fyrirtæki**.
1. Veljið fyrirtækin sem gefa á út afurðina í. Í þessu dæmi skal velja gátreitinn fyrir **USMF**.

    ![Fyrirtækin valin sem gefa á út í.](media/select-release-companies.png "Fyrirtækin valin sem gefa á út í")

1. Veljið **Áfram** til að opna síðuna **Staðfesta val**.
1. Veljið **Ljúka**.

## <a name="review-and-accept-the-product-before-you-release-it-in-the-local-company"></a><a name="accept"></a>Yfirfara og samþykkja afurðina áður en hún er gefin út í staðbundnu fyrirtæki

Tæknideildin hefur nú gefið út upplýsingarnar í staðbundnu fyrirtækjunum þar sem afurðin verður notuð. Í þessu dæmi er staðbundna fyrirtækið *USMF*.

Vegna þess að reiturinn **Samþykki afurðar** er stilltur á *Handvirkt* á síðunni **Færibreytur fyrir umsjón hönnunarbreytinga** fyrir fyrirtækið *USMF*, verður að samþykkja afurðir handvirkt áður en þær eru gefnar út í því fyrirtæki. Með öðrum orðum þá verður að yfirfara þær og samþykkja áður en þær verða að útgefnum afurðum.

Til að fara yfir og gefa út afurðina í fyrirtækinu *USMF* skal fylgja þessum skrefum.

1. Stillið lögaðilann á *USMF*. (Nota skal fyrirtækisvalið hægra megin á yfirlitsstikunni.)
1. Farið í **Umsjón hönnunarbreytinga &gt; Almennt &gt; Útgáfur afurða &gt; Opna afurðarútgáfur**.

    Síðan **Opna afurðarútgáfur** sýnir afurð *Z0001* sem er með stöðuna *Bíður samþykkis*.

    ![Opna losanir afurðar.](media/open-product-releases.png "Opna losanir afurðar")

1. Veljið gildið í dálknum **Afurðarnúmer** til að opna síðuna **Upplýsingar um útgáfu afurðar**. Athugið eftirfarandi upplýsingar:

    - Flýtiflipinn **Almennt** sýnir upplýsingar um útgáfu afurðar, t.d. fyrirtæki útgáfunnar (*DEMF* í þessu dæmi), útgáfustaðinn (*1*) og móttökustaðinn (*1*). Vegna þess að þú tilgreindir ekki móttökusíðu í **Gefa út vörur** töframaður, gildi útgáfusíðunnar er afritað á móttökusíðuna.
    - Flýtiflipinn **Upplýsingar um útgáfu** sýnir upplýsingar um afurðina og útgáfuna sem var gefin út. Hér er hægt að breyta stillingum á borð við gildisdagsetningar.
    - Flýtiflipinn **Leið** sýnir leið afurðarinnar. Í þessu dæmi voru hinsvegar ekki engar leiðar gefnar út.

    ![Upplýsingar um útgáfu afurðar.](media/product-release-details-2.png "Upplýsingar um útgáfu afurðar")

1. Þegar búið er að fara yfir upplýsingarnar, er kominn tími til að samþykkja afurðina og, á þennan hátt, gefa hana út í fyrirtækinu *USMF*. Á aðgerðasvæðinu skal velja **Aðgerðir &gt; Samþykkja**.
1. Nú er búið að gefa út afurðina í fyrirtækinu *USMF*. Opna **Afurðaupplýsingastjórnun &gt; Afurðir &gt; Útgefnar afurðir**. Þú ættir að sjá vöru *Z0001*.

## <a name="use-the-product-in-transactions-in-the-local-company"></a>Nota afurðina í færslum í staðbundnu fyrirtæki

Stjórnandi aðalgagna fyrir fyrirtækið *USMF* vill ganga úr skugga um að afurðin sé með stöðuna *Frumgerð* til að tryggja að notendur verðir varaðir við ef þeir bæta henni óvart við ferli sem þeir eru að vinna í.

1. Opna **Afurðaupplýsingastjórnun &gt; Afurðir &gt; Útgefnar afurðir**.
1. Veljið afurð *Z0001* til að opna upplýsingasíðu hennar. (Hægt er að nota síuna til að finna afurðina.)
1. Á aðgerðasvæðinu, í flipanum **Hönnun**, í flokknum **Umsjón hönnunarbreytinga**, skal velja **Hönnunarútgáfur**.
1. Á síðunni **Hönnunarútgáfur** skal velja útgáfunúmer *V-01* til að opna upplýsingasíðu hennar.
1. Á aðgerðasvæðinu, í flipanum **Afurð**, í flokknum **Líftímastaða**, skal velja **Breyta líftímastaða**.
1. Í fellilista svargluggans **Breyta líftímastöðu** skal stilla reitinn **Staða** á *Frumgerð* og síðan velja **Í lagi**.

    ![Líftímastöðunni breytt.](media/change-lifecycle-state.png "Líftímastöðunni breytt")

## <a name="add-the-engineering-product-to-a-sales-order"></a>Bæta hönnunarafurðinni við sölupöntun

Nú er hægt að selja viðskiptavini afurðina. Til að bæta afurðinni við sölupöntun skal fylgja þessum skrefum.

1. Farðu í **Sölu og markaðssetningu &gt; Sölupöntun &gt; Allar sölupantanir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í svarglugganum **Stofna sölupöntun** skal stilla reitinn **Reikningur viðskiptavinar** á *US-0002* og síðan velja **Í lagi**.
1. Ný sölupöntun opnast. Í flýtiflipanum **Sölupöntunarlínur** skal bæta við línu og stilla reitinn **Vörunúmer** á *Z000* fyrir hana.
1. Í aðgerðarúðunni skal velja **Vista**.

    Þú færð viðvörunarboð sem segir að varan sé með stöðuna *Frumgerð*. En þar sem skilaboðin eru aðeins viðvörun, verður sölupöntunin samt sem áður stofnuð.

    ![Sölupöntun fyrir hönnunarafurð.](media/sales-order-eng-product.png "Sölupöntun fyrir hönnunarafurð")

## <a name="request-changes-in-the-engineering-product"></a>Biðja um breytingar á hönnunarafurð

Afurðin var send til viðskiptavinar en viðskiptavinurinn var ekki fullkomlega sáttur og kemur með ábendingu sem felur í sér tillögur um hvernig má bæta úr því. Á meðan viðskiptavinurinn talar við sölufulltrúa í símann, getur sölufulltrúinn óskað eftir breytingunni sem viðskiptavinurinn er að útskýra.

1. Farðu í **Sölu og markaðssetningu &gt; Sölupöntun &gt; Allar sölupantanir**.
1. Finnið og opnið sölupöntunina sem var stofnuð í fyrri æfingu.
1. Í flýtiflipanum **Sölupöntunarlínur** skal velja **Umsjón hönnunarbreytinga &gt; Ný beiðni um hönnunarbreytingu**.

    ![Beiðni um hönnunarbreytingu stofnuð úr sölupöntun.](media/sales-order-eng-change-request.png "Beiðni um hönnunarbreytingu stofnuð úr sölupöntun")

1. Fyllið út beiðni um hönnunarbreytingu sem byggir á ábendingu viðskiptavinarins. Í þessu dæmi skal stilla eftirfarandi gildi:

    - **Beiðni um breytingu:** *555*
    - **Titill:** *Z0001 breyting viðskiptavinar*
    - **Forgangur:** *lágur*
    - **Flokkur:** stilla breytingu
    - **Alvarleiki:** *Miðlungs*

1. Í flýtiflipanum **Upplýsingar** skal velja **Ný &gt; Athugasemd** til að bæta nýrri athugasemd við hnitanetið.
1. Í reitnum **Lýsing** fyrir nýju athugasemdina skal gefa til kynna að eyða eigi vöru *D0003* úr uppskriftinni. Ef reynist nauðsynlegt að bæta við meiri upplýsingum fyrir athugasemdina, er hægt að slá inn texta í reitinn **Athugasemdir**.

    ![Beiðni um hönnunarbreytingu.](media/eng-change-request.png "Beiðni um hönnunarbreytingu")

1. Í aðgerðarúðunni skal velja **Vista**.
1. Takið eftir að vörunni hefur verið sjálfkrafa bætt við flýtiflipann **Afurðir** og upprunastað beiðni um hönnunarbreytingu (sölupöntunin) hefur verið bætt við flýtiflipann **Upprunastaður**.

## <a name="make-changes-to-the-product-by-using-an-engineering-change-order"></a>Gera breytingar á afurðinni með því að nota pöntun hönnunarbreytingu

Sölufulltrúi veit að afurðin er mikilvæg og var sérstaklega hönnuð fyrir þennan viðskiptavin. Þess vegna hringir sölufulltrúinn í hönnuð í fyrirtækinu *DEMF* og lætur hann vita af breytingabeiðninni. Þannig getur hönnuðurinn hraðað ferlinu.

Hönnuðurinn fer nú yfir beiðni viðskiptavinarins og stofnar breytingapöntun fyrir afurðina.

1. Vegna þess að hönnuðurinn starfar í fyrirtækinu *DEMF* skal stilla lögaðilann á *DEMF*. (Nota skal fyrirtækisvalið hægra megin á yfirlitsstikunni.)
1. Farið í **Umsjón hönnunarbreytinga &gt; Almennt &gt; Beiðnir um hönnunarbreytingu**.
1. Opnið breytingabeiðni *555*.
1. Farið yfir upplýsingarnar og samþykkið síðan breytinguna. Á aðgerðasvæðinu, í flipanum **Beiðni um breytingu**, í flokknum **Breytingastaða**, skal velja **Samþykkja**.
1. Farið í **Umsjón hönnunarbreytinga &gt; Almennt &gt; Pantanir hönnunarbreytinga**.
1. Á aðgerðasvæðinu skal velja **Ný** til að stofna breytingapöntun og stilla eftirfarandi gildi fyrir hana:

    - **Breytingapöntun:** *555*
    - **Titill:** *Z0001 breyting viðskiptavinar*
    - **Flokkur:** *Breyting viðskiptavinar*
    - **Forgangur:** *Lágur*
    - **Alvarleiki:** *Miðlungs*

1. Í flýtiflipanum **Afurðir sem verða fyrir áhrifum** skal velja **Ný &gt; Bæta við fyrirliggjandi afurð** til að bæta línu við hnitanetið og stilla eftirfarandi gildi fyrir hana:

    - **Afurð:** *Z0001*
    - **Áhrif:** *Ný útgáfa*

    ![Pöntun hönnunarbreytingar stofnuð.](media/eng-change-order.png "Pöntun hönnunarbreytingar stofnuð")

1. Takið eftir því að vegna þess að reiturinn **Áhrif** var stilltur á *Ný útgáfa*, sýnir reiturinn **Ný útgáfa** í flipanum **Upplýsingar** í flýtiflipanum **Upplýsingar um afurð** hvaða nýja útgáfunúmerið verður (*V-02* í þessum dæmi).

    ![Upplýsingar um afurð fyrir pöntun hönnunarbreytingar.](media/eng-change-order-product-details.png "Upplýsingar um afurð fyrir pöntun hönnunarbreytingar")

1. Í aðgerðarúðunni skal velja **Vista**.
1. Í flýtiflipanum **Upplýsingar um afurð**, í flipanum **Uppskrift**, skal velja **Línur** til að opna uppskriftina fyrir útgáfu *V-01* fyrir afurð *Z0001*.

    ![Uppskriftarlínur hönnunarafurðar.](media/eng-product-bom-lines.png "Uppskriftarlínur hönnunarafurðar")

1. Veljið línuna fyrir vörunúmer *D0003* og síðan, á aðgerðasvæðinu, skal velja **Eyða**. Gildið í reitnum **Gerð breytingar** fyrir þessa línu breytist í *Eytt*.
1. Í aðgerðarúðunni skal velja **Vista**.

    ![Breyttar uppskriftarlínur hönnunarafurðar.](media/eng-product-bom-lines-modified.png "Breyttar uppskriftarlínur hönnunarafurðar")

1. Lokið síðunni **Uppskriftarlína** til að fara aftur á síðuna **Pöntun hönnunarbreytingar**.
1. Takið eftir að í flýtiflipanum **Upplýsingar um afurð**, í flipanum **Uppskrift**, er gildið fyrir reitinn **Gerð breytingar** fyrir uppskrift *Z0001* núna *Breytt*.

    ![Pöntun hönnunarbreytingar sem inniheldur breytta uppskrift.](media/eng-change-order-changed-bom.png "Pöntun hönnunarbreytingar sem inniheldur breytta uppskrift")

    Nú þarf að samþykkja pöntunina áður en hægt er að vinna úr breytingunum. Þegar unnið er úr breytingunum eru afurðirnar uppfærðar með breytingunum sem eru innifaldar í pöntun hönnunarbreytingar. Í þessu dæmi er sá sem stofnar pöntun hönnunarbreytingar tilgreindur sem samþykktaraðilinn.

1. Á aðgerðasvæðinu, í flipanum **Breytingapöntun**, í flokknum **Breytingastaða**, skal velja **Samþykkja**.
1. Veljið **Vinna úr** til að uppfæra upplýsingar um afurðina.

## <a name="release-the-changed-product"></a>Gefa út breytta afurð

Nú er hægt að gefa út afurðina aftur í fyrirtækinu *USMF* og senda hana til viðskiptavinarins. Til að gefa út afurðina beint úr pöntun hönnunarbreytingar skal fylgja þessum skrefum.

1. Opnið pöntun hönnunarbreytingar sem var stofnuð í fyrri æfingu, ef hún er ekki þegar opin.
1. Á aðgerðasvæðinu, í flipanum **Breytingapöntun**, í flokknum **Útgáfur afurða**, skal velja **Leita**.
1. Leitarniðurstöðurnar sýna hvaða fyrirtæki tilheyrandi afurðir hafa verið gefnar út í. Loka leitarniðurstöðum.
1. Á aðgerðasvæðinu, í flipanum **Breytingapöntun**, í flokknum **Útgáfur afurða**, skal velja **Yfirlit** til að opna svargluggann **Útgáfur**, þar sem hægt er að skoða niðurstöður fyrri leitar.
1. Veljið öll fyrirtækin sem gefa á út afurðir í.
1. Veljið **Í lagi** til að loka svarglugganum **Útgáfur** og fara aftur í breytingapöntunina.
1. Á aðgerðasvæðinu, í flipanum **Breytingapöntun**, í flokknum **Útgáfur afurða**, skal velja **Vinna úr** til að gefa út tilheyrandi afurðir í völdum fyrirtækjum. Að öðrum kosti skal velja **Gefa út skipulag afurðar** til að hefja útgáfuferlið.

## <a name="complete-the-change-order"></a>Ljúka breytingapöntun

Til að merkja breytingapöntun sem lokið, sem gefur til kynna að engar frekari aðgerðir séu eftir, skal velja **Ljúka** á aðgerðasvæðinu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
