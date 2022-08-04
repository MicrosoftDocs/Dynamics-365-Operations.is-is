---
title: Dæmi um aðstæður reglulegrar talningar
description: Þessi grein veitir safn af atburðarásum sem skoða lotutalningareiginleika Microsoft Dynamics 365 Supply Chain Management.
author: GalynaFedorova
ms.date: 06/08/2021
ms.topic: article
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f6f3f2db6efcc4d4d6ae3d278751a230fca9a64
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068597"
---
# <a name="cycle-counting-example-scenarios"></a>Dæmi um aðstæður reglulegrar talningar

[!include [banner](../includes/banner.md)]

Þessi grein veitir safn af atburðarásum sem skoða lotutalningareiginleika Microsoft Dynamics 365 Supply Chain Management. Þar er fyrst lýst kröfum fyrir núverandi umhverfi Supply Chain Management. Síðan er útskýrt hvernig á að skilgreina reglulega talningu og öllum stigum reglulegrar talningar er lýst. Þegar því er lokið ættir þú að hafa góðan skilning á reglulegri talningu, þ.m.t. leiðbeindri reglulegri talningu, blindri reglulegri talningu, reglulegri talningu á staðnum, þröskuldi reglulegrar talningar og áætlunum reglulegrar talningar.

## <a name="prerequisites"></a>Forkröfur

### <a name="make-demo-data-available"></a>Bjóða upp á sýnigögn

Hver atburðarás í þessari grein vísar til gilda og færslur sem eru innifalin í stöðluðum kynningargögnum sem eru veitt fyrir Supply Chain Management. Ef nota á gildin sem er boðið upp á hér þegar farið er í gegnum aðstæðurnar skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett og stilla lögaðilann (fyritækið) á **USMF** áður en hafist er handa.

### <a name="turn-on-support-for-the-warehouse-management-mobile-app"></a>Kveikja á stuðningi fyrir farsímaforrit Warehouse Management

Til að nota Warehouse Management farsímaforritið, *Notendastillingar, tákn og þrepaheiti fyrir nýja vöruhúsaforritið* kveikt verður á eiginleikanum í kerfinu þínu. Frá og með Supply Chain Management 10.0.25 er þessi eiginleiki skylda og ekki hægt að slökkva á honum. Ef þú ert að keyra útgáfu eldri en 10.0.25 geta stjórnendur kveikt eða slökkt á þessari virkni með því að leita að *Notendastillingar, tákn og þrepaheiti fyrir nýja vöruhúsaforritið* eiginleiki í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnurými.

### <a name="prepare-demo-data-for-the-scenarios"></a><a name= "prepare-demo-data"></a>Útbúa sýningargögn fyrir aðstæður

Fylgið þessum skrefum til að staðfesta að öll sýnigögn sem þarf fyrir aðstæðurnar séu tiltæk í USMF-fyrirtækinu í kerfinu. Búið til færslur eða gildi sem vantar.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Starfskraftur**.
1. Á listasvæðinu skal velja **Julia Funderburk**.
1. Í flýtiflipanum **Notendur** skal velja línuna sem er með eftirfarandi gildi. Ef engin núverandi lína hefur þessi gildi skaltu búa hana til.

    - **Notandakenni:** *61*
    - **Notandanafn:** *WH61*
    - **Sjálfgefið vöruhús:** *61*
    - **Heiti valmyndar:** *Aðalvalmynd*

1. Í flýtiflipanum **Vinna** skal stilla eftirfarandi gildi fyrir notendur *61* ef þau eru ekki þegar stillt:

    - **Er stjórnandi reglulegrar talningar:** *Nei*
    - **Hámarksprósenta:** *0*
    - **Hámarksmagn:** *0*
    - **Hámarksgildi:** *0*

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnuhópar**.
1. Vinnuhópar eru notaðir til að aðgreina vöruhúsavinnu, byggt á gerð vinnu (í þessu tilfelli vinnu reglulegrar talningar). Gangið úr skugga um að færsla sé til sem er með eftirfarandi stillingar:

    - **Auðkenni vinnuhóps:** *CycleCount*
    - **Lýsing:** *Regluleg talning*

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Á listasvæðinu skal velja færsluna sem heitir *Regluleg talning*. Ef engin fyrirliggjandi færsla er með það heiti skal búa hana til. Staðfestið eða stillið eftirfarandi gildi fyrir færsluna:

    - **Nafn valmyndaratriðis:** *Regluleg talning*
    - **Titill:** *Regluleg talning með leiðsögn*
    - **Máti:** *Vinna*
    - **Nota fyrirliggjandi vinnu:** *Já*
    - **Stjórnað af:** *Kerfisstýrt* (Þetta gildi segir að Supply Chain Management muni úthluta vinnukenni reglulegrar talningar til starfsmanns.)
    - **Birta birgðastöðu:** *Já*

1. Á aðgerðasvæðinu skal velja **Regluleg talning**.
1. Í svarglugganum **Regluleg talning fartækis** skal staðfesta eða stilla eftirfarandi gildi:

    - **Birta vörunúmer:** *Já*
    - **Birta númeraplötu:** *Yes*
    - **Fjöldi tilrauna:** *1*

1. Veldu **Í lagi** til að loka svarglugganum.
1. Á listasvæðinu skal velja færsluna sem heitir *Blind regluleg talning*. Ef engin fyrirliggjandi færsla er með það heiti skal búa hana til. Staðfestið eða stillið eftirfarandi gildi fyrir færsluna:

    - **Nafn valmyndaratriðis:** *Blind regluleg talning*
    - **Titill:** *Blind regluleg talning*
    - **Máti:** *Vinna*
    - **Nota fyrirliggjandi vinnu:** *Já*
    - **Stjórnað af:** *Flokkun reglulegrar talningar* (Þetta gildi segir að starfmaðurinn geti flokkað vinnukenni reglulegrar talningar sem eiga við um ákveðna staðsetningu, svæði eða vinnuhóp.)

1. Á aðgerðasvæðinu skal velja **Regluleg talning**.
1. Í svarglugganum **Regluleg talning fartækis** skal staðfesta eða stilla eftirfarandi gildi:

    - **Birta vörunúmer:** *No*
    - **Birta númeraplötu:** *Nei*
    - **Fjöldi tilrauna:** *0*

1. Veldu **Í lagi** til að loka svarglugganum.
1. Á listasvæðinu skal velja færsluna sem heitir *Telja á staðnum*. Ef engin fyrirliggjandi færsla er með það heiti skal búa hana til. Staðfestið eða stillið eftirfarandi gildi fyrir færsluna:

    - **Nafn valmyndaratriðis:** *Talning á staðnum*
    - **Titill:** *Talning á staðnum*
    - **Máti:** *Vinna*
    - **Nota fyrirliggjandi vinnu:** *Nei*
    - **Ferli verkstofnunar** ─ *Regluleg talning á staðnum* (Þetta gildi segir að starfsmaðurinn getur talið vörur á staðsetningu vöruhúss hvenær sem er án þess að búa til vinnu reglulegrar talningar. Til að gera reglulega talningu á staðnum á staðsetningu skal starfsmaðurinn færa inn staðsetningarauðkennið.)

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.
1. Á listasvæðinu skal velja færsluna sem heitir *Birgðir*. Ef engin fyrirliggjandi færsla er með það heiti skal búa hana til. Staðfestið að eftirfarandi valmyndaratriði reglulegrar talningar birtist í dálknum **Valmyndaskipan**:

    - Regluleg talning
    - Blind regluleg talning
    - Talning á staðnum

1. Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.
1. Í flipanum **Regluleg talning** skal stilla eftirfarandi gildi:

    - **Leiðréttingargerð sjálfgefinnar reglulegrar talningar:** *Regluleg talning* (Þessi reitur tilgreinir færslubókargerðina sem er bókuð þegar reglulegri talningu lýkur.)
    - **Klasakenni vinnu sjálfgefinnar reglulegrar talningar:** *CCount* (Þessi reitur tilgreinir vinnuklasann sem er notaður fyrir reglulega talningu.)
    - **Forgangur vinnu á sjálfgefinni reglulegri talningu:** *50* (Þessi reitur setur forganginn sem vinna reglulegrar talningar hefur í tengslum við aðrar vinnugerðir í vöruhúsinu. Ef sett er inn lægri tala en talan sem er slegin inn fyrir aðrar gerðir vinnu hækkar það forgang vinnu reglulegrar talningar.)

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Birgðir \> Leiðréttingargerðir**.
1. Á síðunni **Leiðréttingargerðir** er hægt að búa til kóða fyrir mismunandi leiðréttingar á innleið og útleið sem gætu átt sér stað. Staðfestið að færsla sé til sem er með eftirfarandi stillingar:

    - **Gerð birgðaleiðréttingar:** *Regluleg talning*
    - **Lýsing:** *Regluleg talning*
    - **Heiti:** *ICnt*

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Uppsetning vöruhúss \> Vöruhús**.
1. Á listasvæðinu skal velja vöruhús *61*. Ef engin fyrirliggjandi færsla er með það heiti skal búa hana til.
1. Í flýtiflipanum **Vöruhús** skal stilla eftirfarandi gildi:

    - **Notaðu vöruhússtjórnunarferli:** *Já* (Þetta gildi gerir vöruhúsinu kleift fyrir vöruhússtjórnunarferli (WMS).)
    - **Leyfa hreyfingar númeraplötu við reglulega talningu:** *Já* (Þetta gildi gerir starfsmönnum kleift að flytja númeraplötur við reglulega talningu.)

## <a name="scenario-1-guided-cycle-counting"></a>Aðstæður 1: Regluleg talning með leiðsögn

Áður en regluleg talning með leiðsögn getur átt sér stað þarf að stofna vinnu. Þessi vinna mun leiða úthlutaðan einstakling í gegnum vöruhúsið, frá staðsetningu til staðsetningar, til að ljúka talningunum sem eru settar upp í vinnunni.

### <a name="create-cycle-counting-work-for-scenario-1"></a>Stofna vinnu reglulegrar talningar fyrir aðstæður 1

Fylgið þessum skrefum til að stofna vinnu reglulegrar talningar frá vörustaðsetningu *01A02R2S2B* (BULK-06) í vöruhúsi *61*.

1. Farið í **Vöruhúsakerfi \> Regluleg talning \> Vinna reglulegrar talningar eftir staðsetningu**.
1. Í svarglugganum **Stofna vinnu reglulegrar talningar eftir staðsetningu** skal stilla reitinn **Auðkenni vinnuhóps** á *CycleCount*.
1. Á flýtiflipanum **Færslur til að hafa með** velurðu **Sía**.
1. Í svarglugga fyrirspurnarritils í flipanum **Svið** skal fylgja þessum skrefum:

    - Fyrir línuna þar sem reiturinn **Reitur** er stilltur á *Vöruhús* skal stilla reitinn **Skilyrði** á *61*.
    - Fyrir línuna þar sem reiturinn **Reitur** er stilltur á *Staðsetning* skal stilla reitinn **Skilyrði** á *01A02R2S2B*.

1. Veldu **Í lagi** til að loka svarglugga fyrirspurnarritils.
1. Veljið **Í lagi** til að loka svarglugganum **Stofna vinnu reglulegrar talningar eftir staðsetningu**.

    Þegar ferli vinnustofnunar er lokið birtast skilaboð í aðgerðamiðstöðinni.

1. Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnu**.
1. Finnið nýlega stofnaða vinnu með því að stilla síu í dálknum **Auðkenni vinnuhóps** til að finna færslur sem eru með gild fyrir *CycleCount*.

### <a name="do-cycle-counting-work-for-scenario-1"></a>Gera vinnu reglulegrar talningar fyrir aðstæður 1

Þegar búið er að stofna vinna reglulegrar talningar er hægt að gera vinnuna með því að telja vörur á staðsetningu vöruhúss og síðan nota fartæki til að færa niðurstöðurnar inn í Supply Chain Management. Fylgið þessum skrefum til að gera vinna reglulegrar talningar í farsímaforriti Warehouse Management.

1. Skráðu þig inn í Vöruhússtjórnun farsímaforritið sem vinnunotandinn sem þú setur upp í [Undirbúa kynningargögn fyrir atburðarásina](#prepare-demo-data) kafla fyrr í þessari grein. Fyrir dæmið í þessari grein er notandinn nefndur *Julia Funderburk* og er sett upp fyrir lager *61*. (Sýnigögn USMF leyfa þér að skrá þig inn sem þessi vinnunotandi með því að slá inn *61* sem notandakennið og *1* sem aðgangsorð.)
1. Í aðalvalmyndinni skal velja **Birgðir**.
1. Í valmyndinni **Birgðir** skal velja **Regluleg talning með leiðsögn**.
1. Veljið reitinn **Magn**, færið inn *9* með því að nota talnaborðið og veljið síðan **Í lagi** (gátmerkishnappinn).
1. Kerfið átti von á að þú færðir inn talningu upp á 10 stykki fyrir þessa vöru, staðsetningu og númeraplötu. Þess vegna er beðið um endurtalningu. Veljið reitinn **Magn**, færið aftur inn *9* með því að nota talnaborðið og veljið síðan **Í lagi** (gátmerkishnappinn). Í seinni tilrauninni er talningin þín samþykkt.

    > [!NOTE]
    > Þegar kerfið greindi mismun á milli væntanlegra lagerbirgða og magns sem var slegið inn, biður það um aðra talningu vegna þess að reiturinn **Fjöldi tilrauna** er stilltur á *1* fyrir valmyndaratriðið **Regluleg talning með leiðsögn** í fartækinu. Farið var með þig á tiltekið vörunúmer og númeraplötunúmer vegna þess að bæði valkosturinn **Birta vörunúmer** og **Birta númeraplötu** eru stilltir á *Já* fyrir valmyndaratriði fartækis.

1. Veljið **Í lagi** (hnappurinn með gátmerki).

### <a name="review-the-cycle-counting-differences-for-scenario-1"></a>Farið yfir muninn á reglulegri talningu fyrir aðstæður 1

Fylgið þessum skrefum til að fara yfir mismun á reglulegri talningu.

1. Farið aftur í Supply Chain Management.
1. Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnu**.
1. Finnið og veljið vinnu reglulegrar talningar sem var skoðuð áður. (Setjið til dæmis síu á dálkinn **Auðkenni vinnuhóps** til að finna færslur sem eru með gildi fyrir *CycleCount*.) Takið eftir að reiturinn **Staða verks** fyrir þessa vinnu er nú stilltur á *Bíður yfirferðar*.

    > [!NOTE]
    > Fyrir notandareikning vinnunnar sem var notaður til að gera talningarvinnuna er valkosturinn **Yfirmaður reglulegrar talningar** stilltur á *Nei* og reitirnir **Hámarksprósenta**, **Hámarksmagn** og **Hámarksgildi** stilltir á *0* (núll). Því þarf allur munur á talningu sem notandi tilkynnir að vera samþykktur handvirkt og reiturinn **Staða verks** fyrir tengda vinnu er stilltur á *Bíður yfirferðar*. Ef talið gildi var innan vikmarka (eins og tilgreind eru í reitunum **Hámarksprósenta** eða **Hámarksmagn** á síðunni **Verknotendur**) eða ef valkosturinn **Yfirmaður reglulegrar talningar** er stilltur á *Já* fyrir notandann, hefði vinnunni verið lokað sjálfkrafa.

1. Á aðgerðasvæðinu, í flipanum **Vinna**, skal velja **Regluleg talning**.
1. Veldu **Samþykkja talningu** á aðgerðasvæðinu.

    Mismunurinn er bókaður með staðlaðri talningarbók og ný verkbeiðni er búin til.

1. Á síðunni **Færslur reglulegrar talningar**, á aðgerðasvæðinu, skal velja **Afleidd vinna** til að finna vinnuna sem var búin til fyrir samþykktan mun.

## <a name="scenario-2-blind-cycle-counting"></a>Aðstæður 2: Blind regluleg talning

Þessar aðstæður krefjast þess að búið sé að ljúka við aðstæður 1 í kerfinu.

### <a name="create-cycle-counting-work-for-scenario-2"></a>Stofna vinnu reglulegrar talningar fyrir aðstæður 2

Áður en blind regluleg talning getur átt sér stað þarf að stofna vinnu. Fylgið þessum skrefum til að stofna vinnu reglulegrar talningar frá vörustaðsetningu *01A02R2S2B* (BULK-06) í vöruhúsi *61*.

1. Farið í **Vöruhúsakerfi \> Regluleg talning \> Vinna reglulegrar talningar eftir vöru**.
1. Í svarglugganum **Stofna vinnu reglulegrar talningar eftir vöru** skal stilla reitinn **Auðkenni vinnuhóps** á *CycleCount*.
1. Á flýtiflipanum **Færslur til að hafa með** velurðu **Sía**.
1. Í svarglugga fyrirspurnarritils í flipanum **Svið** skal bæta við þremur línum sem eru með eftirfarandi stillingar:

    - Lína 1.

        - **Tafla:** *Vara*
        - **Svæði:** *Vörunúmer*
        - **Skilyrði:** *L0101*

    - Lína 2:

        - **Tafla:** *Birgðavíddir*
        - **Svæði:** *Vöruhús*
        - **Skilyrði:** *61*

    - Lína 3:

        - **Tafla:** *Birgðavíddir*
        - **Svæði:** *Staðsetning*
        - **Skilyrði:** *01A02R2S2B*

1. Veldu **Í lagi** til að loka svarglugga fyrirspurnarritils.
1. Veljið **Í lagi** til að loka svarglugganum **Stofna vinnu reglulegrar talningar eftir vöru**.

    Þegar ferli vinnustofnunar er lokið birtast upplýsingaboð.

### <a name="do-cycle-counting-work-for-scenario-2"></a>Gera vinnu reglulegrar talningar fyrir aðstæður 2

Þegar búið er að stofna vinna reglulegrar talningar skal fylgja þessum skrefum til að gera vinnuna í farsímaforrit Warehouse Management.

1. Skráðu þig inn í Vöruhússtjórnun farsímaforritið sem vinnunotandinn sem þú setur upp í [Undirbúa kynningargögn fyrir atburðarásina](#prepare-demo-data) kafla fyrr í þessari grein. Fyrir dæmið í þessari grein er notandinn nefndur *Julia Funderburk* og er sett upp fyrir lager *61*. (Sýnigögn USMF leyfa þér að skrá þig inn sem þessi vinnunotandi með því að slá inn *61* sem notandakennið og *1* sem aðgangsorð.)
1. Í aðalvalmyndinni skal velja **Birgðir**.
1. Í valmyndinni **Birgðir** skal velja **Blind regluleg talning**.
1. Veljið reitinn **Svæðiskenni**, færið inn *BULK06* og veljið síðan **Í lagi** (gátmerkishnappurinn).
1. Veljið reitinn **Vara**, færið inn *L0101* og veljið síðan **Í lagi** (gátmerkishnappurinn).
1. Veljið reitinn **Númeraplata**, færið inn *NP\_BULK\_06\_01* og veljið síðan **Í lagi** (gátmerkishnappurinn).
1. Veljið reitinn **Magn**, færið inn *10* og veljið síðan **Í lagi** (gátmerkishnappurinn).

    > [!NOTE]
    > Þótt kerfið hafi greint mismun á milli væntanlegra lagerbirgða og magns sem var skannað, biður það ekki um aðra talningu vegna þess að reiturinn **Fjöldi tilrauna** er stilltur á *0* (núll) fyrir valmyndaratriðið **Blind regluleg talning** í fartækinu. Beðið var um að skanna vörunúmerið og númeraplötuna vegna þess að bæði valkosturinn **Birta vörunúmer** og **Birta númeraplötu** eru stilltir á *Nei* fyrir valmyndaratriði fartækis.

1. Veljið **Í lagi** (hnappurinn með gátmerki).

### <a name="review-the-cycle-counting-differences-for-scenario-2"></a>Farið yfir muninn á reglulegri talningu fyrir aðstæður 2

Fylgið þessum skrefum til að fara yfir mismun á reglulegri talningu.

1. Farið aftur í Supply Chain Management.
1. Farið í **Vöruhúsakerfi \> Almennt \> Vinna \> Vinna reglulegrar talningar bíður yfirferðar**.
1. Á aðgerðasvæðinu, í flipanum **Vinna**, skal velja **Regluleg talning**.
1. Á aðgerðasvæðinu skal velja **Hafna talningu**.

    Vinnu er lokað vegna þess að mun á talningu var hafnað.

## <a name="scenario-3-spot-cycle-counting"></a>Aðstæður 3: Reglubundin talning á staðnum

Lagerfærslurnar segja að til eru lagerbirgðir af vöru *L0101* á staðsetningu *01A02R2S2B*. Starfsmaður í vöruhúsi er á stað *01A02R2S1B*. Þessi staðsetning ætti að vera auð en hún er full. Starfsmaður í vöruhúsi gerir því strax talningu á staðnum á þessari staðsetningu.

### <a name="do-cycle-counting-work-for-scenario-3"></a>Gera vinnu reglulegrar talningar fyrir aðstæður 3

Fylgið þessum skrefum til að gera vinna reglulegrar talningar í farsímaforriti Warehouse Management.

1. Skráðu þig inn í Vöruhússtjórnun farsímaforritið sem vinnunotandinn sem þú setur upp í [Undirbúa kynningargögn fyrir atburðarásina](#prepare-demo-data) kafla fyrr í þessari grein. Fyrir dæmið í þessari grein er notandinn nefndur *Julia Funderburk* og er sett upp fyrir lager *61*. (Sýnigögn USMF leyfa þér að skrá þig inn sem þessi vinnunotandi með því að slá inn *61* sem notandakennið og *1* sem aðgangsorð.)
1. Í aðalvalmyndinni skal velja **Birgðir**.
1. Í valmyndinni **Birgðir** skal velja **Talning á staðnum**.
1. Veldu reitinn **Staðsetning**, sláið inn *01A02R2S1B* og veljið svo **Í lagi** (gátmerkishnappurinn).

    Kerfið greinir að staðsetningin er tóm í Supply Chain Management.

1. Veljið **Bæta við númeraplötu eða vöru**.
1. Veljið reitinn **Vara**, færið inn *L0101* og veljið síðan **Í lagi** (gátmerkishnappurinn).
1. Veljið reitinn **Númeraplata**, færið inn *NP\_BULK\_06\_01* og veljið síðan **Í lagi** (gátmerkishnappurinn).
1. Veljið reitinn **Magn**, færið inn *9* og veljið síðan **Í lagi** (gátmerkishnappurinn).

    Þar sem kerfið greinir að tilgreind númeraplata er þegar tiltæk á öðrum stað í Supply Chain Management, verður sú númeraplata færð á núverandi staðsetningu. Þess vegna biður kerfið þig um að staðfesta hreyfinguna.

1. Veljið **Í lagi** (hnappurinn með gátmerki).

### <a name="review-the-cycle-counting-differences-for-scenario-3"></a>Farið yfir muninn á reglulegri talningu fyrir aðstæður 3

Fylgið þessum skrefum til að fara yfir niðurstöður talningar.

1. Farið aftur í Supply Chain Management.
1. Farið í **Vöruhúsakerfi \> Almennt \> Upplýsingar um verk**.
1. Veljið gátreitinn **Sýna lokað** efst í hnitanetinu.
1. Stillið síuna fyrir dálkinn **Gerð verkbeiðni** á *Birgðahreyfing*.

    Kerfið bar sjálfkrafa kennsl á þessa talningu sem birgðahreyfingu. Þessi hreyfing er leyfð vegna þess að valkosturinn **Leyfa tilfærslu númeraplötu við reglulega talningu** er stilltur á *Já* fyrir vöruhús *61* á síðunni **Vöruhús**.

## <a name="scenario-4-define-cycle-count-thresholds"></a>Aðstæður 4: Skilgreina þröskulda reglulegrar talningar

Ein leið til að búa til vinnu reglulegrar talningar er að nota þröskulda. Þröskuldur reglulegrar talningar tilgreinir mörk magns eða prósentu birgðavara. Vinna reglulegrar talningar er stofnuð sjálfkrafa þegar þröskuldi er náð.

Til dæmis eru 60 vörur á staðsetningu þar sem þröskuldur reglulegrar talningar er 40. Við sölupöntunarfærslu, eru 25 vörur teknar frá staðsetningu og settar inn í sviðsetningarstaðsetningu. Þar sem nýr fjöldi vörunnar, 35, er minna en magnþröskuldur er vinna reglulegrar talningar stofnuð sjálfkrafa fyrir staðsetningu.

Fylgið þessum skrefum til að setja upp þröskulda reglulegrar talningar.

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Regluleg talning \> Þröskuldar reglulegrar talningar**.
1. Veljið **Nýtt** á aðgerðasvæðinu til að búa til þröskuld og stillið eftirfarandi gildi fyrir hann:

    - **Auðkenni þröskulds fyrir reglulega talningu:** *L0101*
    - **Lýsing:** *Þröskuldur L0101*
    - **Magnþröskuldur:** *2*
    - **Prófhópur:** *ea*
    - **Þröskuldur afkastagetu byggður á prósentu:** *0,00*
    - **Gerð þröskulds fyrir reglulega talningu:** *Magn*
    - **Vinna strax úr reglulegri talningu:** *Já*
    - **Dagar á milli reglulegrar talningar:** *1*
    - **Auðkenni vinnuhóps:** *CycleCount*

1. Á aðgerðasvæðinu skal velja **Valdar vörur**.
1. Í svarglugga fyrirspurnarritilsins, í flipanum **Svið**, skal finna línuna þar sem reiturinn **Svæði** er stilltur á *Vörunúmer*. Stillið reitinn **Skilyrði** fyrir þessa línu á *L0101*.
1. Veldu **Í lagi** til að loka svarglugga fyrirspurnarritils.

    Þú hefur nú skilgreint þröskuld fyrir reglulega talningu á vöru *L0101*.

Nú verður stofnuð regluleg talning fyrir vöru *L0101* á hvaða staðsetningu sem er ef lagerbirgðir eru minni en 2 og ef dagsetning síðustu reglulegu talningar fyrir staðsetninguna er ekki í dag.

## <a name="scenario-5-define-cycle-count-plans"></a>Aðstæður 5: Skilgreina áætlanir reglulegrar talningar

Áætlanir um reglulega talningu gera kleift að gera stofnun á vinnu reglulegrar talningar sjálfvirka. Hægt er að setja upp hverja áætlun reglulegrar talningar fyrir sig með tilteknum fyrirspurnum um vöru og staðsetningu. Þegar runuvinnslan keyrir mun hún búa til vinnu reglulegrar talningar fyrir allar staðsetningar sem passa við skilyrði vöru og staðsetningar (upp að hámarksfjölda talninga sem er tilgreindur fyrir áætlunina). Þegar regluleg talning er stofnuð inniheldur vinnulína talningar upplýsingar um staðsetningu sem verður að telja. Ekki er lokað á lagerbirgðirnar sem tengjast þeirri staðsetningu. Þær eru þar af leiðandi tiltækar fyrir frátekningu og vinnslu á útleið, jafnvel þótt opin talningarvinna sé til staðar.

Fylgið þessum skrefum til að setja upp áætlun reglulegrar talningar.

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Regluleg talning \> Áætlanir um reglulega talningu**.
1. Veljið **Ný** á aðgerðasvæðinu til að bæta nýrri línu við hnitanetið og stillið eftirfarandi gildi fyrir hana:

    - **Auðkenni áætlunar um reglulega talningu:** *BULK06*
    - **Lýsing:** *Talning á staðsetningu fyrir BULK06*
    - **Auðkenni vinnuhóps:** *CycleCount*
    - **Hámarksfjöldi reglulegrar talningar:** *10*
    - **Dagar á milli reglulegrar talningar:** *10*
    - **Tómar staðsetningar:** *Útiloka tómar*
    - **Vinnusniðmát:** Skildu þetta svæði eftir autt.

1. Veljið **Velja staðsetningar** á aðgerðasvæðinu.
1. Venjulegur svargluggi fyrirspurnarritils birtist. Í flipanum **Svið** skal bæta við línu og stilla eftirfarandi gildi fyrir hana:

    - **Tafla:** *Staðir*
    - **Reitur::** *Auðkenni svæðis*
    - **Skilyrði:** *BULK06*

1. Veldu **Í lagi** til að loka svarglugga fyrirspurnarritils.
1. Á aðgerðasvæðinu skal velja **Vinna úr áætlun um reglulega talningu**.
1. Í svarglugganum **Áætlanir um reglulega talningu**, í flýtiflipanum **Keyra í bakgrunni**, skal stilla valkostinn **Runuvinnsla** á *Já*.
1. Veljið **Endurtekning**.
1. Í svarglugganum **Skilgreina endurtekningu** skal setja upp runuvinnslu þannig að hún hefjist strax og keyri á mínútu fresti, og þannig að engin lokadagsetning sé til staðar.
1. Veljið **Í lagi** til að loka svarglugganum **Skilgreina endurtekningu**.
1. Veljið **Í lagi** til að loka svarglugganum **Áætlanir um reglulega talningu**.

    Skilaboð gefa til kynna að vinnslunni hafi verið bætt við runuröðina.

1. Farið í **Vöruhúsakerfi \> Almennt \> Áætlunargerð reglulegrar talningar**. Áætlunin hefst strax og skapar talningarvinnu. Þar sem ekki er búið að ljúka talningarvinnu er reiturinn **Staða** stilltur á *Í vinnslu*. Eftir eina mínútu breytist gildið í **Samtala reglulegra talninga** í *1*.

    > [!NOTE]
    > Vinna reglulegrar talningar verður ekki búin til ef fjöldi daga frá síðustu reglulegu talningu er minni en gildið sem stillt var fyrir reitinn **Dagar á milli reglulegrar talninga** fyrir áætlun um reglulega talningu. Til dæmis ef gildið sem er skilgreint í **Dagar á milli reglulegrar talninga** er *5* verður vinna reglulegrar talningar stofnuð á fimm daga fresti. Hins vegar ef unnið er úr vinnu reglulegrar talningar á degi 3 mun næsta reglulega talning stofnast fimm dögum eftir að síðasta reglulega talning var unnin, á degi 8.

1. Á aðgerðasvæðinu skal velja **Vinna** til að skoða talningarvinnuna sem var búin til.
