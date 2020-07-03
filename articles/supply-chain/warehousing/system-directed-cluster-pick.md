---
title: Kerfisstýrð klasatiltekt
description: Þetta efni veitir yfirlit yfir kerfisbundna klasatiltekt í Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b7ac243a04309a41ab0e06c1b2d4843ae8ac0e22
ms.sourcegitcommit: 7c32e4739c07d825a8562564ea9e78922db2ce38
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406382"
---
# <a name="system-directed-cluster-picking"></a>Kerfisstýrð klasatiltekt

[!include [banner](../includes/banner.md)]

Klasatiltekt er verk til að velja hluti sem gerir þér kleift að velja hluti fyrir margar pantanir á sama tíma með því að þjappa þeim í tiltektarklasa. Síðan verður þú að heimsækja tiltektarstaðinn aðeins einu sinni. Venjulega er þessi virkni notuð við litla pöntunartínslu eða magn sem er minna en tilfelli.

Þegar kerfisstýrð klasatiltekt er sett upp er hægt að klasatína vinnuhausa, byggð á kerfisframleiddum klasa. Kerfið klasatínir pantanir upp að fjölda staða sem tilgreindar eru í klasasniðinu. Þess vegna getur þú tínt margar pantanir á sama tíma án þess að þurfa að búa til klasa handvirkt.

Kerfisstýrð klasatiltekt býður annan valkost við handvirkra klasagerð, þar sem klasasnið er notað til að búa til klasa. Nokkrar uppsetningartengdar línur verða að vera skilgreindar í klasasniðinu áður en það er notað:

- **Fjöldi staða** samsvarar til fjölda pantana sem verða settar í klasa. Þess vegna samsvarar hann fjölda heildartölu.
- **Skipta klasaeiningu** ákvarðar hvenær skipta eigi klasaeiningunni.
- **Mynda klasaauðkenni** stjórnar því hvort klasakennið verði myndað af kerfinu eða fært inn af notandanum.
- **Gerð röðunarstaðfestingar** ákvarðar hvort staðfesting á stöðu sé nauðsynleg.

Nýtt valmyndaratriði fartækis er notað við kerfisstýrða klasatiltekt. Tilgreina verður **Forstillingarkenni klasa** fyrir valkostinn **Stjórnað af** sem var valinn. Að auki geta fyrirspurnir kerfisstýrðrar vinnuröðunar raðað saman pöntunum samkvæmt skilyrðum sem tengjast fyrirtæki. Þess vegna er hægt að fínstilla úthlutun vinnupantana enn frekar með því að tilgreina sérsniðin röðunarskilyrði með því að nota fyrirspurnir kerfisstýrðra vinnuröðunar.

Þegar kerfisstýrð klasatiltekt er virkjuð fá starfsmenn vöruhúss klasa þar sem tiltektarpantanir hafa verið fyrirfram úthlutaðar á klasastaðsetningar. Þess vegna geta starfskraftar byrjað að taka til vöru fyrir margar verkbeiðnir með því að heimsækja tiltektarstaðinn aðeins einu sinni. Tínsluferlið fyrir kerfisstýrða klasatiltekt er það sama og ferlið fyrir notendastýrða klasatiltekt.

## <a name="enable-the-system-directed-cluster-picking-feature"></a>Virkja eiginleika kerfisstýrðrar klasatiltektar

Áður en hægt er að nota þennan eiginleika þarf að virkja hann í kerfinu. Stjórnendur geta notað síðuna [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og virkjað hann ef þörf krefur. Hérna er eiginleikinn skráður sem:

- **Eining** - Vöruhúsakerfi
- **Heiti eiginleika** - Kerfisstýrð klasatiltekt

Þessi eiginleiki þarf einnig virkjun á háðum eiginleika. Háði eiginleikinn er:

- **Eining** - Vöruhúsakerfi
- **Heiti eiginleika** - Kerfisstýrð vinnuröðun fyrir alla stofnunina/fyrirtækið

## <a name="set-up-system-directed-cluster-picking"></a>Setja upp kerfisstýrða klasatiltekt

### <a name="create-cluster-profiles"></a>Stofna klasaforstillingar

Klasaforstillngar stjórna því hvernig kerfið býr til hvern klasa. Ef krafist er mismunandi klasa ætti að búa til mismunandi klasastillingar fyrir hvert valmyndaratriði fartækis.

1. Farðu á **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Klasaforstillingar**.
2. Veljið **Nýtt**.
3. Í reitnum **Auðkenni klasaforstillinga** slærðu inn **2 staða**.
4. Í reitinn **Heiti** skal færa inn **Staða 2**.
5. Á flýtiflipanum **Almennt** eru eftirfarandi upplýsingar slegnar inn:

    - **Mynda klasaauðkenni** - Veljið **Já**. Þessi valkostur ákvarðar hvort auðkenni klasans er sjálfkrafa búið til af kerfinu, eða hvort notandinn býr til það í upphafi tínslu. 
    - **Virkja stöður** - Veljið **Já**. Þessi valkostur ákvarðar hvort stöðuheiti séu sjálfkrafa mynduð út frá uppsetningu stöðuheitis. Ef þessi valkostur er stilltur á **Nei** er kenni númeraplötuð notað fyrir stöðuna.
    - **Fjöldi staða** - Veljið **2**. Þessi reitur ákvarðar hámarksfjölda staða sem klasinn getur haft (það er hámarksfjöldi kassa, heildartölur og svo framvegis).
    - **Heiti stöðu** - Veljið **Tölugildi** þannig að stöður eru nefndar með því að nota samfelld númer. Ef þú velur **Stafrófsröð** eru stöðurnar nefndar í stafrófsröð.
    - **Skipta klasa við** - Veljið **Frágangur**. Þessi reitur ákvarðar hvenær klasanum er skipt upp. 
    - **Raða staðfestingargerð** - Veljið **Skönnun stöðu**. Þessi reitur ákvarðar hvort staðfestingarþrepið sé staðfest.
        
6. Í flýtiflipanum **Klasaröðun** er röðunarskilyrði skilgreint með því að búa til nýja línu og slá inn eftirfarandi upplýsingar:

    - **Númer raðar** - Veljið **1**. Þessi reitur ákvarðar röðunina sem kerfið raðar eftir. Gildi er sjálfkrafa fært inn en hægt er að breyta því ef þörf krefur.
    - **Heiti reits** - Færið inn **WMSLocationId**. Þessi reitur ákvarðar reitinn sem línan notar sem röðunarviðmið.
    - **Röðun** - Veljið **Hækkandi**. Þessi reitur skilgreinir hvort röðunin sé gerð í hækkandi eða lækkandi röð.

### <a name="create-a-mobile-device-menu-item"></a>Stofna valmyndaratriði fartækis

Fylgdu þessum skrefum til að búa til nýjan valmyndaratriði fartæki fyrir kerfisstýrða klasatiltekt og tengja kenni klasaforstillinga við valmyndaratriði fartækis.

1. Fara í **Vöruhúsakerfi > Uppsetning > fartækis > Valmyndaratriði fartækis**.
1. Veljið **Nýtt**.
1. Færi inn eftirfarandi upplýsingar í haushlutanum:
    - **Heiti valmyndaratriðis** - SD-klasi
    - **Titill** - SD-klasi
    - **Stilling** -vinnu
    - **Nota fyrirliggjandi vinnu** - Já

1. Á flýtiflipanum **Almennt** eru eftirfarandi upplýsingar slegnar inn:
    - **Stjórnað af** - Kerfisstýrð klasatiltekt
    - **Mynda númeraplötu** - Já
    - **Forstillingarkenni klasa** - 2 staða

1. Á flýtiflipanum **Vinnuklasar** skaltu setja upp gildan vinnuklasa fyrir þetta valmyndaratriði fartækis með því að stilla eftirfarandi reiti:
    - **Auðkenni vinnuklasa:** - Sala
    - **Gerð verkpöntunar** - Sölupantanir

1. Á aðgerðasvæðinu **Valmyndaratriði fartækis** skal velja **Kerfisstýrðar fyrirspurnir vinnuröðunar** og fylgja þessum skrefum til að tilgreina nýja fyrirspurn kerfisstýrðrar vinnuröðunar:
    - Veljið **Ný** á aðgerðasvæðinu.
    - **Raðnúmer** - 1
    - **Lýsing** - Forgangur vinnu - Vinnukenni

1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**
1. Veljið flipann **Röðun**
1. Veljið **Bæta við** til að bæta við nýrri línu og færið inn eftirfarandi:
    - **Tafla** - Vnna
    - **Afleidd tafla** - Vinna
    - **Reitur** - Forgangur vinnu
    - **Leitarstefna** - Hækkandi
1. Veljið **Bæta við** til að bæta við annarri línu og færið síðan inn eftirfarandi:
    - **Tafla** - Vnna
    - **Afleidd tafla** - Vinna
    - **Reitur** - Vinnukenni
    - **Leitarstefna** - Hækkandi

1. Kerfið mun nú raða vinnukennum í klasanum, fyrst eftir forgangi vinnu og síðan eftir vinnukenni.

### <a name="set-up-a-mobile-device-menu"></a>Setja upp valmynd fartækja

1. Fara í **Vöruhúsakerfi > Uppsetning > fartækis > Valmynd fartækis**.
1. Bætið valmyndaratriðinu **SD-klasi** sem var búið til við valmynd fartækis.
1. Veljið valmyndina **Á útleið**.
1. Veljið **Breyta** á aðgerðasvæðinu.
1. Flettið þar til **SD-klasi** finnst.
1. Veljið **Sd-klasi**, örin sem bendir á listann **Valmyndaskipan** virkjast.
1. Veljið **örvarhnappinn** til að færa valmyndaratriðið **SD-klasi** í valmyndaskipanina **Á útleið**.
1. Veljið **SD-klasi** úr listanum **Valmyndaskipan**, veljið síðan örvarnar **UPP** eða **NIÐUR** til að færa valmyndaratriðið í æskilega stöðu í valmynd fartækis.

## <a name="scenario"></a>Aðstæður

### <a name="create-picking-work"></a>Stofna tiltektarvinnu

Áður en hægt er að setja upp kerfisstýrða klasatiltekt þarf að búa til gjaldgenga vinnu á útleið. Klasaforstillingin sem þú bjóst til áður tilgreinir tvær klasastöður. Þess vegna verður að búa til að minnsta kosti tvö vinnukenni. Í þessari atburðarás verða búnar til tvær sölupantanir, birgðir teknar frá, sölupantanir losaðar í vöruhúsið og unnið handvirkt úr bylgjunni.

1. Fara í **Sölu og markaðssetningu > sölupöntun > Allar sölupantanir**.
1. Veljið Velja **Nýtt** í aðgerðasvæði til að stofna fyrri sölupöntunina.
    - Valmyndin **Stofna sölupöntun** opnast, færið inn eftirfarandi upplýsingar:
        - Í flýtiflipanum **Viðskiptavinur** skal færa inn **Viðskiptamannalykill** - **US-004**.
        - Í flýtiflipanum **Almennt** skal færa inn **Vöruhús** - **62**.
        - Veljið **Í lagi** til að loka valmyndinni og stofna sölupöntunina.
    - Í flýtiflipanum **Sölupöntunarlínur** skal velja **Bæta við línu** ef nýrri línu er ekki sjálfkrafa bætt við og færa inn eftirfarandi:
        - **Vörunúmer** - A0001
        - **Magn** - 1
        - Veldu **Bæta við línu** til að bæta við annarri línu.
        - **Vörunúmer** - A0002
        - **Magn** - 3
    - Taka frá birgðir fyrir báðar línurnar sem verið var að stofna.
        - Velja **Lína 1**.
        - Á aðgerðasvæðinu **Sölupöntunarlínur** skal velja **Birgðir** og síðan velja **Frátekning** úr listanum.
        - Í skjámyndinni **Frátekning** skal velja **Frátektarlota** til að taka frá birgðirnar.
        - Lokið skjámyndinni **Frátekning** þegar frátekningunni er lokið.
        - Endurtakið þessi skref til að taka frá birgðir fyrir **Lína 2**.
1. Veljið Velja **Nýtt** í aðgerðasvæði til að stofna seinni sölupöntunina
    - Valmyndin **Stofna sölupöntun** opnast, færið inn eftirfarandi upplýsingar:
        - Í flýtiflipanum **Viðskiptavinur** skal færa inn **Viðskiptamannalykill** - **US-005**.
        - Í flýtiflipanum **Almennt** skal færa inn **Vöruhús** - **62**.
        - Veljið **Í lagi** til að loka valmyndinni og stofna sölupöntunina
    - Í flýtiflipanum **Sölupöntunarlínur** skal velja **Bæta við línu** ef nýrri línu er ekki sjálfkrafa bætt við og færa inn eftirfarandi upplýsingar:
        - **Vörunúmer** - A0001
        - **Magn** - 4
        - Veldu **Bæta við línu** til að bæta við annarri línu.
        - **Vörunúmer** - A0002
        - **Magn** - 2
    - Taka frá birgðir fyrir báðar línur sem verið var að stofna.
        - Velja **Lína 1**.
        - Á aðgerðasvæðinu **Sölupöntunarlínur** skal velja **Birgðir** og síðan velja **Frátekning** úr listanum.
        - Í skjámyndinni **Frátekning** skal velja **Frátektarlota** til að taka frá birgðirnar.
        - Lokið skjámyndinni **Frátekning** þegar frátekningunni er lokið.
        - Endurtakið þessi skref til að taka frá birgðir fyrir **Lína 2**.
    - Lokið sölupöntuninni og snúið aftur á listasíðuna **Allar sölupantanir**.
1. Finnið sölupantanirnar tvær sem voru stofnaðar (kannski þarf að uppfæra síðuna). Í töflunni skal velja báðar sölupantanirnar með því að nota gátmerkishlutann.
    - Á aðgerðasvæðinu **Allar sölupantanir** skal velja flipann **Vöruhús**.
    - Í flokknum **Aðgerðir** skal velja **Losa í vöruhús** til að losa báðar sölupantanirnar í vöruhúsið.
1. Þegar losunarferlið í vöruhús lýkur birtast upplýsandi skilaboð.
    - Sendingar verða stofnaðar fyrir hverja sölupöntun.
    - Bylgja verður búin til og báðum sendingum verður úthlutað á bylgjuna. Takið niður **Bylgjuauðkennið**.
1. Opnið **Vöruhúsastjórnun > Bylgjur á útleið > Sendingarbylgjur > Allar bylgjur**.
    - Í listanum **Allar bylgjur** skal finna og velja **Bylgjuauðkennið** sem var búið til í skrefinu á undan.
    - Á aðgerðasvæðinu skal velja flipann **Bylgja**.
    - Í flokknum **Bylgja** skal velja **Úrvinnsla** til að vinna úr bylgjunni og búa til **Verk**.
    - Upplýsingaboð verða búin til þegar úrvinnslu lýkur, sem segir að verk hafi verið stofnað og bylgja hefur verið bókuð.
1. **Valfrjálst**: Opnið **Vöruhúsakerfi > Verk > Upplýsingar um verk** til að skoða stofnað verk. Tvö mismunandi vinnukenni eru búin til. Hvert vinnukenni hefur tvær tínslulínur.

### <a name="run-the-mobile-device-flow"></a>Keyrðu fartækjaflæðið

1. Skráðu þig inn í fartækið fyrir notanda í vöruhúsi **62**.
1. Í **Aðalvalmyndinni** skal velja **Á útleið**.
1. Í valmyndinni **Á útleið** skal velja **SD-klasi** til að hefja tiltekt.
    - Klasi er búinn til og tvö vinnukenni sem voru stofnuð áður eru hengd við. Ef þú bjóst til fleiri en tvö vinnukenni er aðeins fyrstu tveimur bætt við klasann. Athugaðu að vinnukennum sé bætt við klasann í hækkandi röð eins og þú tilgreindir í fyrirspurnaruppsetningunni.

    > [!NOTE]
    > Nýi klasinn er sjálfkrafa aðeins myndaður ef nóg viðbótar vinnukenni hafa áður verið mynduð. Annars eru eftirfarandi skilaboð sýnd: "Ekki er hægt að finna næga vinnu fyrir klasann."

    - Eftir að þú hefur valið valmyndina birtist fyrsta valmyndin. Kerfið safnar saman öllum samsvarandi tiltektarlínum úr vinnukennunum tveimur og beinir þér til að heimsækja tiltektarstaðinn einu sinni, svo að þú getir fullnægt báðum pöntunum með því að nota eina tínslu. Þetta ferli er unnið á sama hátt og ferlið við notandastýrða klasatiltekt.

1. Staðfestið fyrstu staðsetningu og vöru tiltektar með því að velja **Í lagi**.
    - Magn tiltektarinnar verður samtala vörunnar sem birtist í sölupöntunum í klasanum.
1. Færið inn heiti stöðunnar (tölugildi eða bókstafur) til að staðfesta að magn vörunnar sem tínd var fyrir staðinn var sett á réttan stað.
1. Endurtakið þetta ferli þar til allt vörumagn hefur verið tekið til og það sett í rétta stöðu.
1. Lokaskrefið í fartækinu er að **Ganga frá** klasanum á lokastaðsetninguna. Veljið **Í lagi**.
    - Þegar frágangsaðgerðin er staðfest er klasanum lokað og skipt upp, byggt á gildinu sem var stillt fyrir reitinn **Skipta klasa við** í klasaforstillingunni. Vinnukennum er einnig lokað.
1. Skilaboðin „Klasa lokið“ eru sýnd á fartækinu.
