---
title: Áfylling yfir staðsetningargetu
description: Í þessu efnisatriði er að finna upplýsingar um eiginleikann fyrir áfyllingu yfir staðsetningargetu. Þessi eiginleiki gerir kleift að búa til alla áfyllingarvinnu sem krafist er fyrir daginn og stjórnar framboði þessarar áfyllingarvinnu til að tryggja að birgðir í tiltektarstaðsetningunni hvorki tæmist né fari yfir getu.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 78bea4ee2429323a6e087c6433a8e496b08f4cea
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576113"
---
# <a name="replenishment-over-location-capacity"></a>Áfylling yfir staðsetningargetu

[!include [banner](../includes/banner.md)]

Sum vöruhús með mikið magn eða takmarkað rými verða að senda meira vörumagn á einu degi en sem kemst fyrir í tiltektarstaðsetningunni. Eiginleikinn *Áfylling yfir staðsetningargetu* gerir kleift að búa til alla áfyllingarvinnu sem krafist er fyrir daginn og stjórnar framboði þessarar áfyllingarvinnu til að tryggja að birgðir í tiltektarstaðsetningunni hvorki tæmist né fari yfir getu.

Eiginleikinn gerir klefit að búa til meiri áfyllingarvinnu en staðsetningin ræður við og hann kemur í veg fyrir að áfyllingarvinnu ljúki þegar staðsetningin er full. Þegar birgðir í tiltektarstaðsetningu fara niður fyrir skilgreind mörk verður boðið upp á meiri áfyllingarvinnu.

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a>Kveikja á eiginleikanum fyrir áfyllingu yfir staðsetningargetu

Til að gera þennan eiginleika tiltækan skaltu kveikja á eftirfarandi eiginleika í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (í þessari röð):

1. Vinnulokun fyrir allt fyrirtækið
1. Áfylling yfir staðsetningargetu

## <a name="set-up-the-feature-for-the-example-scenario"></a>Setja upp eiginleikann fyrir þetta sýnidæmi

Í þessum hluta eru leiðbeiningar og dæmi sem sýna hvernig á að setja upp þennan eiginleika og undirbúa sýnigögn fyrir sýnidæmið sem kemur fyrir seinna í þessu efnisatriði.

### <a name="enable-sample-data"></a>Virkja gögn sýnishorna

Til að vinna í gegnum [sýniaðstæðurnar](#example-scenario) með því að nota sýnskrárnar og sýnigildin sem eru kynnt í þessu efnisatriði verður þú að vinna á kerfi þar sem venjulegu [sýnigögnin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) eru sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

### <a name="location-profile"></a>Forstillingar staðsetningar

Kveikið á virkninni fyrir áfyllingu yfir staðsetningargetu í staðsetningarforstillingunni.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Forstillingar staðsetningar**.
1. Á svæðinu vinstra megin skal velja **PICK-06**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Í flýtiflipanum **Áfylling** skal stilla eftirfarandi gildi:

    - **Fara yfir afkastagetu staðsetningar:** *Já*

        Þegar virkjuð heimilar áfyllingarvinna að farið sé umfram hámarksafköst staðsetningar. Þetta virkjar einnig aðra reiti í flýtiflipanum **Áfylling**.

    - **Gerð viðmiðunarmarka fyrir vinnuframboð:** *Magn*

        Þessi reitur skilgreinir aðferðina sem er notuð til að ákvarða hvenær ætti að losa meiri vinnu. Hægt er að losa eftir annaðhvort magni eða prósentu:

        - *Prósenta* – Veljið þennan valkost til að nota prósentugetu sem byggir á birgðamörkum eða rúmmáli. Ef þessi valkostur er valinn, virkjar það reitinn **Prósenta yfirflæðis** og slekkur á reitunum tveimur sem tengjast magni, **Magn yfirflæðis** og **Eining yfirflæðis**.

            Hægt er að nota þennan valkost ef tiltektarstaðsetningarnar nota rúmmál.

            Ef þessi valkostur er valinn skal stilla reitinn **Prósenta yfirflæðis** á þá prósentu þegar meiri áfyllingarvinna er gerð tiltæk.

        - *Magn* – Veljið þennan valkost til að nota tiltekið gildi fyrir magn. Ef þessi valkostur er valinn slokknar á **Prósenta yfirflæðis** og reitirnir **Magn yfirflæðis** og **Eining yfirflæðis** virkjast.

            Notið þennan valkost þegar rúmmál er ekki notað fyrir staðsetningar sem fyllt er á, eða þegar birgðamagnið sem fyllt er á staðsetninguna er stöðugt.

           Ef þessi valkostur er valinn skal stilla magn reitina **Magn yfirflæðis** og **Eining yfirflæðis** á magnið og eininguna þegar meiri áfyllingarvinna er gerð tiltæk.

    - **Magn yfirflæðis:** *0,65*

        Þessi reitur skilgreinir magnið þegar verður yfirflæði á staðsetningunni.

        Vinna verður alltaf tiltæk þegar samanlagt magn af lagerbirgðum á staðsetningunni og vinnumagni er undir þessu gildi. Öll áfyllingarvinna fyrir ofan þetta gildi verður lokað fyrir og verður að opna fyrir hana handvirkt.

        Birgðamörk staðsetningar eru tekin til greina þegar vinnumagnið er reiknað.

    - **Eining yfirflæðis:** *PL*

        Þessi reitur skilgreinir eininguna sem tengist magni yfirflæðis.

        Í þessu tilfelli verður frekari áfyllingarvinna tiltæk þegar staðsetningin fer niður fyrir 0,65 bretti (PL).

    - **Hlutfall yfirflæðis**

        Þessi reitur skilgreinir hlutfallið þegar verður yfirflæði á staðsetningunni.

        Vinna verður alltaf tiltæk þegar samanlagt magn af lagerbirgðum á staðsetningunni og vinnumagni er undir þessu hlutfalli. Öll áfyllingarvinna fyrir ofan þetta hlutfall verður lokað fyrir og verður að opna fyrir hana handvirkt.

        Birgðamörk staðsetningar eru tekin til greina þegar hlutfall vinnumagnsins er reiknað. Ef engin birgðamörk staðsetningar eru skilgreind, verður hlutfall vinnumagns reiknað eftir rúmmáli ef takmarkanir rúmmáls eru skilgreindar fyrir staðsetningarforstillinguna.

> [!IMPORTANT]
> Ef sýnigögnin eru notuð fyrir lögaðilann **USMF** og búið er að kveikja á eiginleikanum *Númeraplötustaða staðsetningar*, þarf að slökkva á stillingunni **Virkja staðsetningu númeraplötu** fyrir staðsetningarforstillinguna **BUK-06** til að ljúka skrefum fartækis í þessu sýnidæmi.

### <a name="wave-step-code"></a>Kóði bylgjuskrefs

> [!NOTE]
> Til að setja upp bylgjuskrefskóða eins og lýst er gæti fyrst þurft að nota [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á eiginleikanum sem kallast *Kóði bylgjuskrefs fyrir allt fyrirtækið*.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjuskrefakóðar**.
1. Veljið **Nýtt** og stillið eftirfarandi gildi:

    - **Kóði bylgjuskrefs:** *Áfyll*
    - **Lýsing á bylgjuskrefi:** *Áfylling*
    - **Gerð bylgjuskrefs:** *Áfylling*

1. Veljið **Vista**.

### <a name="replenishment-template"></a>Sniðmát áfyllingar

Áfyllingarsniðmát er safn af reglum sem stjórna því hvenær og hvernig fyllt er á staðsetningu.

1. Fara í **Vöruhúsakerfi \> Uppsetningu \> Áfylling \> Áfyllingarsniðmát**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Í hlutanum **Yfirlit** skal velja línuna þar sem reiturinn **Áfyllingarsniðmát** er stilltur á *Áfylling samkvæmt eftirspurn*.
1. Stilla eftirfarandi gildi:

    - **Kóði bylgjuskrefs:** *Áfyll*
    - **Leyfa bylgjueftirspurn að nota magn sem ekki er frátekið:** *Já*

1. Veljið **Vista**.

### <a name="wave-template"></a>Bylgjusniðmát

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.
1. Á svæðinu vinstra megin skal stilla reitinn **Gerð bylgjusniðmáts** á *Sending*.
1. Veljið sniðmát **61 Sending** í listanum.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Í flýtiflipanum **Almennt** skal stilla valkostinn **Gera losun áfyllingarvinnu sjálfvirka** á *Já*.

    Stillið þennan valkost á *Já* til að stofna áfyllingarvinnu byggða á eftirspurn og losa hana sjálfkrafa. Verður að bæta bylgjuaðferð áfyllingar við bylgjusniðmátið og stofna áfyllingarsniðmát af gerðinni **Bylgjueftirspurn**. Setjið upp áfyllingarsniðmát á síðunni **Áfyllingarsniðmát**. Til að setja upp áfyllingarsniðmát þarf að bæta áfyllingaraðferðinni við bylgjusniðmátið.

1. Í flýtiflipanum **Aðferðir**, í dálknum **Valdar aðferðir**, skal finna eftirfarandi línu:

    - **Heiti aðferðar:** *fylla á*
    - **Heiti:** *Áfylling*

1. Stillið reitinn **Kóði bylgjuskrefs** fyrir þessa línu á *Áfyll*.
1. Veljið **Vista**.

## <a name="example-scenario"></a>Dæmi

Þegar búið er að gera öll sýnigögnin hér á undan tiltæk og setja þau upp, er hægt að fara í gegnum þetta sýnidæmi til að prófa eiginleikann *Áfylling yfir staðsetningargetu*. Gildin sem eru sýnd í þessu sýnidæmi gera ráð fyrir því að verið sé að vinna með stöðluð sýnigögn, að lögaðilinn **USMF** hafi verið valinn og að sýniskrárnar sem lýst var fyrr í þessu efnisatriði hafi verið undirbúnar. Þetta sýnidæmi er einnig dæmi um hvernig hægt er að nota eiginleikann í framleiðsluumhverfi.

### <a name="create-replenishment-work"></a>Stofna áfyllingarvinnu

#### <a name="create-sales-order-1"></a>Stofna sölupöntun 1

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Á aðgerðasvæðinu skal velja **Ný** til að opna svarglugga til að stofna nýja sölupöntun.
1. Í svarglugganum skal stilla eftirfarandi gildi:

    - **Viðskiptavinalykill:** *US-007*
    - **Vöruhús:** *61*

1. Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.
1. Ný sölupöntun opnast. Hún inniheldur nýja, auða línu í flýtiflipanum **Sölupöntunarlína**. Stilltu eftirfarandi gildi á þessari línu:

    - **Vörunúmer:** *T0100*
    - **Magn:** *40*

1. Í flýtiflipanum **Sölupöntunarlínur** skal velja **Birgðir \> Frátekning**.
1. Á síðunni **Frátekning** skal velja **Frátektarlota**.
1. Lokið síðunni.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.

    Upplýsingaboð birtast sem sýna auðkenni bylgju og sendingar sem voru búin til. Áfyllingarbylgja er einnig stofnuð.

    Einnig birtast viðvörunarboð sem segja: „Vinnukenni XXXX er ekki hægt að útiloka því að það er með ókláraða áfyllingarvinnu.“

#### <a name="create-sales-order-2"></a>Stofna sölupöntun 2

1. Á síðunni **Allar sölupantanir**, á aðgerðasvæði, skal velja **Ný** til að opna svarglugga til að stofna nýja sölupöntun.
1. Í svarglugganum skal stilla eftirfarandi gildi:

    - **Viðskiptavinalykill:** *US-001*
    - **Vöruhús:** *61*

1. Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.
1. Ný sölupöntun opnast. Hún inniheldur nýja, auða línu í flýtiflipanum **Sölupöntunarlína**. Stilltu eftirfarandi gildi á þessari línu:

    - **Vörunúmer:** *T0100*
    - **Magn:** *60*

1. Í flýtiflipanum **Sölupöntunarlínur** skal velja **Birgðir \> Frátekning**.
1. Á síðunni **Frátekning** skal velja **Frátektarlota**.
1. Lokið síðunni.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.

    Upplýsingaboð birtast sem sýna auðkenni bylgju og sendingar sem voru búin til. Áfyllingarbylgja er einnig stofnuð.

    Einnig birtast viðvörunarboð sem segja: „Vinnukenni XXXX er ekki hægt að útiloka því að það er með ókláraða áfyllingarvinnu.“

#### <a name="create-sales-order-3"></a>Stofna sölupöntun 3

1. Á síðunni **Allar sölupantanir**, á aðgerðasvæði, skal velja **Ný** til að opna svarglugga til að stofna nýja sölupöntun.
1. Í svarglugganum skal stilla eftirfarandi gildi:

    - **Viðskiptavinalykill:** *US-004*
    - **Vöruhús:** *61*

1. Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.
1. Ný sölupöntun opnast. Hún inniheldur nýja, auða línu í flýtiflipanum **Sölupöntunarlína**. Stilltu eftirfarandi gildi á þessari línu:

    - **Vörunúmer:** *T0100*
    - **Magn:** *30*

1. Í flýtiflipanum **Sölupöntunarlínur** skal velja **Birgðir \> Frátekning**.
1. Á síðunni **Frátekning** skal velja **Frátektarlota**.
1. Lokið síðunni.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.

    Upplýsingaboð birtast sem sýna auðkenni bylgju og sendingar sem voru búin til. Áfyllingarbylgja er einnig stofnuð.

    Einnig birtast viðvörunarboð sem segja: „Vinnukenni XXXX er ekki hægt að útiloka því að það er með ókláraða áfyllingarvinnu.“

#### <a name="view-work-details"></a>Skoða vinnuupplýsingar

1. Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnu**.
1. Í hlutanum **Yfirlit** skal sía dálkinn **Vöruhús** fyrir vöruhús *61*.
1. Þá ætti að sjást að sjö vinnukenni hafa verið búin til fyrir þrjár sölupantanir eftirspurnar.

    - Þrjú af þessum sjö vinnukennum eru með gildi **Gerð verkbeiðni** sem *Áfylling* og fjögur þeirra eru með gildi **Gerð verkbeiðni** sem *Sölupantanir*.
    - Öll þrjú vinnukennin sem eru með gildi **Gerð verkbeiðni** sem *Áfylling* eru með sömu staðsetningar fyrir *Tiltekt* og *Frágang* í hlutanum **Línur**.

        - **Tiltekt:** *02A01R5S1B*
        - **Frágangur:** *06A01R2S1B*

    - Tvö vinnukenni voru stofnuð fyrir sölupöntun 1.

1. Skráið niður vinnukennin fyrir sölupantanirnar.

Það fer eftir magni á lager, en það getur verið örlítill munur á vinnumagninu. Hins vegar ættu vinnuhausarnir sem stofnaðir eru að samsvara þessu sýnidæmi.

#### <a name="on-hand-inventory-license-plate-id"></a>Númeraplötukenni lagerbirgða

Síðar í þessu dæmi verður farsímaforrit vöruhúsakerfis notað (eða hermiforrit), þar sem þarf að bera kennsl á númeraplötuna til að ljúka sýnidæmunum fyrir tiltekt og áfyllingu.

Til að finna númeraplötukennin sem þarf að nota seinna meir, skal fylgja þessum skrefum.

1. Farið í **Birgðastjórnun \> Fyrirspurnir og skýrslur \> Lagerlisti**.
1. Veljið hnappinn **Sýna síur** til að opna síusvæðið.
1. Sláið inn eftirfarandi síuskilyrði til að sækja númeraplöturnar fyrir dæmið. Notið síuna *hefst á*.

    - **Vörunúmer:** *T0100*
    - **Vöruhús:** *61*

1. Veljið **Bæta við**.
1. Á aðgerðasvæðinu skal velja **Víddir**.
1. Í svarglugganum **Birting vídda**, í hlutanum **Geymsluvíddir**, skal velja öll gildin.
1. Í hlutanum **Færslur** skal velja **Vörunúmer** og **Magn \<\> 0**.
1. Þegar þessu er lokið skal velja **Í lagi** til að loka svarglugganum.
1. Hnitanetið **Á lager** sýnir númeraplötunúmerin fyrir vöru *T0100* í hverri staðsetningu. Skráið niður númeraplötuna sem er á hverri staðsetningu, því að nota þarf upplýsingarnar síðar.
1. Lokið síðunni.

### <a name="process-steps"></a>Ferlisskref

Áfylling á staðsetningu vöruhúss verður framkvæmd fyrir fyrstu tvö vinnukennin. Lokað verður fyrir vinnu á þriðju áfyllingarvinnunni þar til birgðastaða tiltektarstaðsetningarinnar fer undir mörkin.

#### <a name="replenishment"></a>Áfylling

1. Skráðu þig inn í farsímaforrit vöruhúsakerfis sem notandi í vöruhúsi *61*. (Sláið inn *61* sem notandakennið og *1* sem aðgangsorðið.)
1. Farið í **Birgðir \> Áfylling**.

    Beðið er um að ljúka fyrstu áfyllingarvinnunni. Vörunúmerið, magnið og staðsetningin fyrir tiltektina er sýnt.

1. Í reitinn **NP** skal færa númeraplötunúmerið fyrir vöruna í staðsetningunni sem er sýnd.
1. Velja skal hnappinn **Í lagi** (gátmerkistákn).

    Kerfið býr til númer marknúmeraplötu fyrir nýju númeraplötuna fyrir tínda vöru.

1. Veljið **Í lagi** til að staðfesta gildið.

    Frágangsvinna er sýnd sem segir notandanum að setja marknúmeraplötuna á áfyllingarstaðsetninguna. Staðsetning *Frágangs* á að vera **06A01R2S1B**.

1. Staðfestið upplýsingar um frágang og veljið **Í lagi**.

    Skilaboðin „Vinnu er lokið“ birtast og upplýsingar um næsta tiltektarverk áfyllingar eru sýndar: vörunúmerið, magnið og staðsetningin sem tína á úr. Tiltektarstaðsetningin verður sú sama og fyrsta áfyllingarstaðsetningin. Þess vegna verður númeraplatan með sama númeraplötukennið og var notað fyrir verk fyrstu áfyllingarvinnunnar.

1. Endurtakið fyrri skref til að ljúka áfyllingarvinnu fyrir næsta vinnuverk. Magn og marknúmeraplata verða frábrugðin magni og marknúmeraplötu fyrir fyrsta vinnuverkið.

Þegar næstu áfyllingarvinnu lýkur birtast skilaboðin „Vinnu er lokið“. Fartækið upplýsir einnig að engin vinna er í boði, jafnvel þótt einhver áfyllingarvinna sé eftir. Þessi hegðun gerist vegna þess að áfyllingarvinnan er með stöðuna *Í bið* og er þar af leiðandi merkt sem **Lokað fyrir**.

Staðan *Í bið* var ræst vegna þess að staðsetningarforstillingin fyrir tiltektarstaðsetninguna sem vinnunni er úthlutað á er með gildi á **Magn yfirflæðis** sem *0,65 PL*. Tvö fyrri áfyllingarverkin fylltu staðsetninguna næstum upp að mörkum yfirflæðis fyrir vöru *T0100*. (Umreikningur einingar fyrir vöruna er *1 PL = 100 ea*.) Eftirstandandi áfyllingarvinna myndir þar af leiðandi leiða til þess að staðsetningin færi yfir mörk yfirflæðis.

Þar til nægar birgðir eru tíndar úr staðsetningunni til að koma henni undir mörk losunarvinnu í valmyndaratriði fartækis, verður áfram lokað fyrir þessa áfyllingarvinnu.

#### <a name="sales-order-pick"></a>Tiltekt sölupöntunar

Áður en hægt er að ljúka við eftirstandandi áfyllingarvinnu verða birgðir tiltektarstaðsetningarinnar að minnka niður í það sem þarf til að opnað fyrir eftirstandandi áfyllingarvinnu. Með öðrum orðum, samanlagt magn lagerbirgða í staðsetningunni og áfyllingarmagn má ekki fara yfir gildið **Magn yfirflæðis**. Þegar þetta samanlagða magn er minna en magn yfirflæðis, verður opnað fyrir eftirstandandi áfyllingarvinnu.

1. Skráðu þig inn í farsímaforrit vöruhúsakerfis sem notandi í vöruhúsi *61*. (Sláið inn *61* sem notandakennið og *1* sem aðgangsorðið.)
1. Opnaðu **Á útleið \> Sölutiltekt**.
1. Færið inn fyrsta vinnukennið fyrir sölupöntun 1.

    Notið vinnukennin fyrir sölupantanir sem skráð voru niður hér á undan, á síðunni **Upplýsingar um vinnu**. Vinnukennið sem fært er inn hér býr til tiltektarvinnu fyrir magn upp á 10 ea frá tveimur aðskildum staðsetningum.

1. Veljið **Í lagi**.

    Verksíðan **Sölupantanir: Tiltekt** sýnir vörunúmerið, magnið og staðsetninguna sem tína á úr fyrir fyrstu staðsetninguna.

1. Í reitinn **NP** skal færa númeraplötunúmerið fyrir vöruna í staðsetningunni sem er sýnd.
1. Velja skal hnappinn **Í lagi** (gátmerkistákn).

    Verksíðan **Sölupantanir: Tiltekt** sýnir vörunúmerið, magnið og staðsetninguna sem tína á úr fyrir næstu staðsetningu.

1. Í reitinn **NP** skal færa númeraplötunúmerið fyrir vöruna í staðsetningunni sem er sýnd.
1. Velja skal hnappinn **Í lagi** (gátmerkistákn).

    Síðan **Sölupantanir: Frágangur** gefur fyrirskipun um að ganga frá báðum loknu tiltektarvinnunum á geymslustaðsetningu á útleið.

1. Veljið **Í lagi**.

    Skilaboðin „Vinnu er lokið“ birtast.

1. Færið inn næsta vinnukenni fyrir sölupöntun 1.

    Aðeins er eitt tiltektarverk fyrir þetta vinnukenni.

1. Veljið **Í lagi**.

    Verksíðan **Sölupantanir: Tiltekt** sýnir vörunúmerið, magnið og staðsetninguna sem tína á úr.

1. Í reitinn **NP** skal færa númeraplötunúmerið fyrir vöruna í staðsetningunni sem er sýnd.

    Númeraplatan sem tilgreind er verður ein af númeraplötunum sem kerfið býr til í verkum áfyllingarvinnu. Til að ganga úr skugga um að rétt kenni númeraplötu sé sótt, skal athuga birgðirnar á síðunni **Lagerlisti** fyrir vöruna, staðsetninguna og magnið.

1. Velja skal hnappinn **Í lagi** (gátmerkistákn).
1. Staðfestið leiðbeiningar um frágangsverk á geymslustaðsetningu á útleið.
1. Veljið **Í lagi**.

    Skilaboðin „Vinnu er lokið“ birtast.

Lokað er fyrir tiltekt fyrir sölupöntun 2 vegna þess að áfyllingarverkið sem hún er tengd við er ekki lokið. Sem stendur er enn magn upp á 30 ea í tiltektarstaðsetningunni og áfyllingarmagnið fyrir sölupöntun 2 er 60 ea. Samtala lagerbirgða og áfyllingarbirgða (90 ea) fer yfir magn yfirflæðis upp á 0,65 PL (eða 65 ea). Áður en hægt er að ljúka við áfyllingarvinnu verður að tína sölupöntun 3.

1. Færið inn vinnukennið fyrir sölupöntun 3.

    Aðeins er eitt tiltektarverk fyrir þetta vinnukenni.

1. Veljið **Í lagi**.

    Verksíðan **Sölupantanir: Tiltekt** sýnir vörunúmerið, magnið og staðsetninguna sem tína á úr.

1. Í reitinn **NP** skal færa númeraplötunúmerið fyrir vöruna í staðsetningunni sem er sýnd.

    Númeraplatan sem tilgreind er verður ein af númeraplötunum sem kerfið býr til í verkum áfyllingarvinnu. Til að ganga úr skugga um að rétt kenni númeraplötu sé sótt, skal athuga birgðirnar á síðunni **Lagerlisti** fyrir vöruna, staðsetninguna og magnið.

1. Velja skal hnappinn **Í lagi** (gátmerkistákn).
1. Staðfestið leiðbeiningar um frágangsverk á geymslustaðsetningu á útleið.
1. Veljið **Í lagi**.

    Skilaboðin „Vinnu er lokið“ birtast.

Um leið og samtala lagerbirgða í tiltektarstaðsetningunni og áfyllingarmagns er undir mörkum, verður hægt að vinna úr eftirstandandi áfyllingarvinnu.

Farið aftur á síðuna **Upplýsingar um vinnu** og takið eftir að tiltækileiki áfyllingarvinnu fyrir síðasta hluta áfyllingar (fyrir sölupöntun 2) er *Opin*, því að nóg pláss er í staðsetningunni til að samþykkja áfyllinguna.

Nú er hægt að vinna þessa áfyllingarvinnu með fartækinu.

1. Farið í **Birgðir \> Áfylling**.

    Beðið er um að ljúka eftirstandandi áfyllingarvinnu. Vörunúmerið, magnið og staðsetningin fyrir tiltektina er sýnt.

1. Í reitinn **NP** skal færa númeraplötunúmerið fyrir vöruna í staðsetningunni sem er sýnd.
1. Velja skal hnappinn **Í lagi** (gátmerkistákn).

    Kerfið býr til númer marknúmeraplötu fyrir nýju númeraplötuna fyrir tínda vöru.

1. Veljið **Í lagi** til að staðfesta gildið.

    Frágangsvinna er sýnd sem segir notandanum að setja marknúmeraplötuna á áfyllingarstaðsetninguna. Staðsetning *Frágangs* á að vera **06A01R2S1B**.

1. Staðfestið upplýsingar um frágang og veljið **Í lagi**.

    Skilaboðin „Vinnu lokið“ og „Engin vinna tiltæk“ birtast.

Þú getur nú valið sölupöntun 2. Opnað var fyrir hana þegar áfyllingarvinnunni sem tengd er við sölupöntunina var lokið.

1. Færið inn vinnukennið fyrir sölupöntun 2.

    Aðeins er eitt tiltektarverk fyrir þetta vinnukenni.

1. Veljið **Í lagi**.

    Verksíðan **Sölupantanir: Tiltekt** sýnir vörunúmerið, magnið og staðsetninguna sem tína á úr.

1. Í reitinn **NP** skal færa númeraplötunúmerið fyrir vöruna í staðsetningunni sem er sýnd.

    Númeraplatan sem tilgreind er verður númeraplatan sem kerfið býr til í verki áfyllingarvinnu. Til að ganga úr skugga um að rétt kenni númeraplötu sé sótt, skal athuga birgðirnar á síðunni **Lagerlisti** fyrir vöruna, staðsetninguna og magnið.

1. Velja skal hnappinn **Í lagi** (gátmerkistákn).
1. Staðfestið leiðbeiningar um frágangsverk á geymslustaðsetningu á útleið.
1. Veljið **Í lagi**.

    Skilaboðin „Vinnu er lokið“ birtast.

## <a name="notes-and-tips"></a>Athugasemdir og ábendingar

- Þessi aðgerði virkar með öllum gerðum áfyllingar: bylgjueftirspurn, lágmarki/hámarki, hleðslueftirspurn og hólfaskiptingu.
- Hægt er að hnekkja tiltækileika áfyllingarvinnu handvirkt fyrir hvern vinnuhaus af síðunni **Upplýsingar um vinnu** ef þess er óskað.
- Þegar kerfið stillir tiltækileika áfyllingarvinnu, tekur það allar birgðir til greina sem eru þegar í staðsetningunni áður en vinnu er lokið
- Hver hluti sölupöntunarvinnu er tengdur við tiltekna áfyllingarvinnu. Ekki er til nein samsvarandi virkni fyrir tiltækileika söluvinnu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]