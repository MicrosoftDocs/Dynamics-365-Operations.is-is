---
title: Skipulag afurðarlosunar
description: Þetta efnisatriði útskýrir hvernig hægt er að losa heildarskipulag afurðar ásamt því að losa afurðir með hönnunarútgáfum þeirra. Á þennan hátt er tryggt að auðvelt sé að endurnota afurðargögn sem tengjast hönnun í mismunandi lögaðilum.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductReleaseSiteBulkEdit, EngChgProductReleaseSendListPage, EngChgProductReleaseSendDetails,EngChgProductReleaseSelection,EngChgProductReleaseReceiveListPage, EngChgProductReleaseReceiveDetails, EngChgProductReleasePreviewPane, EngChgProductReleasePolicy, EngChgProductReleasePart, EngChgProductReleaseNote
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 68f091cca9c3c2baa03813553127ee41abe6d522
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/29/2020
ms.locfileid: "4430788"
---
# <a name="release-product-structures"></a>Skipulag afurðarlosunar

[!include [banner](../includes/banner.md)]

Til að tryggja að auðvelt sé að endurnota afurðargögn sem tengjast hönnun í mismunandi lögaðilum er hægt að losa heildarskipulag afurða ásamt því að losa afurðir með hönnunarútgáfum þeirra. Þar af leiðandi er hægt að losa uppskriftarskipulag á mörgum stigum ásamt yfireiningunni í einni losunaraðgerð. Í þessu tilvikum er uppskriftin og afurðin á neðra stigi einnig losuð.

Hönnunarafurðir eru stofnaðar og unnið með af hönnunarfyrirtækinu á þann hátt að þær uppfylli gæðakröfur meðan á hönnun stendur. Hvert rekstrarfyrirtæki sem framleiðir afurð þarf sömu afurð og undirliggjandi uppskrift. Það fer eftir framleiðslustaðnum, en leiðina er hugsanlega hægt að stofna á staðnum. Í því tilfelli verður leið ekki losuð ásamt afurðinni. Ekki er víst að uppskriftin sé nauðsynleg fyrir lögaðila sem vilja selja afurðirnar en ekki framleiða þær.

Til að gera ferlið skilvirkara er hægt að losa öll gögn sem tengjast hönnun til annarra rekstrarfyrirtækja samtímis. Þessi gögn innihalda afurðarskipulagið. Í losunarferlinu er hægt að velja hvaða hluta framleiðslugagnanna á að losa.

Frekari upplýsingar um hönnunarfyrirtæki og rekstrarfyrirtæki er að finna í [Hönnunarfyrirtæki og reglur um eignarrétt gagna](engineering-org-data-ownership-rules.md).

Athugið að hægt er að losa bæði staðlaðar afurðir og hönnunarafurðir ásamt skipulagi losaðrar afurðar. Í þessu ferli verður allt afurðarskipulagið losað, meira að segja uppskriftin og leiðin úr fyrirtækinu sem afurðirnar eru losaðar í.

Dæmi um hvernig á að losa afurð er að finna í [Losa hönnunarafurð í staðbundið fyrirtæki](engineering-scenarios.md#release)

## <a name="released-data-for-a-product-when-the-release-product-structure-is-used"></a>Losa gögn fyrir afurð þegar skipulag losaðrar afurðar er notað

Eftirfarandi gögn eru tekin með í losun hönnunarafurða:

- **Afurðargögn** - Ný útgefin afurð er stofnuð.
- **Gögn hönnunarútgáfu** - Hönnunarútgáfan og gögn hennar eru stofnuð eða uppfærð. Athugið að ef sama hönnunarútgáfan er losuð aftur í rekstrarfyrirtækið, verður skrifað yfir hönnunargögnin.
- **Hönnunareigindir** - Hönnunareigindir og gildin þeirra eru stofnuð eða uppfærð.
- **Hönnunaruppskriftir** - Uppskrift hönnunar og línur hennar er hægt að stofna eða uppfæra. Frekari upplýsingar um eignarhald gagna er að finna í [Eigendur afurða](product-owner.md).
- **Leiðir hönnunar** - Leiðir hönnunar og aðgerðir þeirra er hægt að stofna eða uppfæra. Frekari upplýsingar um eignarhald gagna er að finna í [Eigendur afurða](product-owner.md).
- **Skjöl hönnunar** - Hönnunarskjölin sem tengjast hönnunarútgáfunni eru stofnuð eða uppfærð.

Þegar kveikt er á umsjón hönnunarbreytinga í kerfinu, verður skipulag afurðarlosunar tiltækt. Auk þess munu staðlaðar afurðir innihalda uppskriftir sínar og leiðir þegar þær eru losaðar.

## <a name="product-acceptance"></a>Samþykki afurðar

**Samþykki afurðar** er lykilfæribreyta sem hefur áhrif á losunarferlið. Hægt er að stilla þessa færibreytu fyrir hvert fyrirtæki með því að fara í **Umsjón hönnunarbreytinga \> Uppsetning \> Færibreytur fyrir umsjón hönnunarbreytinga**. Frekari upplýsingar er að finna í [Færibreytur fyrir umsjón hönnunarbreytinga](engineering-parameters.md).

### <a name="automatic-product-acceptance"></a>Sjálfvirkt samþykki afurðar

Hver losun af hönnunarafurðum hefst þegar einhver úr hönnunarfyrirtækinu velur afurð til að losa. Þegar færibreytan **Samþykki afurðar** er stillt á *Sjálfvirkt* ákveður notandinn í hönnunarfyrirtækinu hvaða afurðargögn eigi að losa sjálfkrafa í rekstrarfyrirtækin. Afurðin verður síðan losuð sjálfkrafa í fyrirtækin sem eru valin í leiðsagnarforriti losunar.

### <a name="manual-product-acceptance"></a>Handvirkt samþykki afurðar

Hver losun af hönnunarafurðum hefst þegar einhver úr hönnunarfyrirtækinu velur afurð til að losa. Þegar færibreytan **Samþykki afurðar** er stillt á *Handvirkt* ákveður notandinn í hönnunarfyrirtækinu hvaða afurðargögn eigi að losa í rekstrarfyrirtækin. Notandi frá hverju rekstrarfyrirtæki fer síðan yfir afurðargögnin og ákveður hvort eigi að samþykkja losunina. Notandi rekstrarfyrirtækisins getur stillt eftirfarandi valkosti þegar gögnin eru móttekin:

- Ef afurðirnar (uppfærslurnar) eiga ekki við um rekstrarfyrirtækið, getur notandinn valið að samþykkja ekki losunina.
- Notandinn getur breytt vörusniðmátinu fyrir nýjar afurðir.
- Notandinn getur valið hvort losa eigi afurðina ásamt uppskriftum sínum og/eða leiðum og hvort losa eigi þær sem samþykktar og virkar.
- Notandinn getur breytt frá dagsetningum þegar afurðirnar taka gildi.

Fyrir dæmi um hvernig á að samþykkja afurð skal skoða [Yfirfara og samþykkja afurðina áður en hún er gefin út í staðbundnu fyrirtæki](engineering-scenarios.md#accept).

> [!NOTE]
> Fyrir staðlaðar afurðir er hægt að losa frá öllum lögaðilum yfir í alla aðra lögaðila. Fyrir hönnunarafurðir er hönnunarfyrirtækið eini lögaðilinn sem hægt er að losa frá.

## <a name="release-policies"></a>Losunarreglur

Ekki þurfa öll rekstrarfyrirtæki sömu afurðargögnin. Almennt, rekstrarfyrirtæki sem framleiða hönnunarafurðir þurfa á uppskrift að halda, á meðan rekstrarfyrirtæki sem selja aðeins hönnunarafurðir þurfa ekki uppskrift. Hægt er að gefa út reglur til að setja á færibreyturnar sem eru notaðar fyrir losun á afurðum.

Fyrir hönnunarafurðir er losunarreglunni úthlutað á flokk hönnunarafurðar og reiturinn er áskilinn. Fyrir staðlaðar afurðir er reglunni úthlutað á samnýtta afurðina og svæðið er valfrjálst.

Frekari upplýsingar um flokka hönnunarafurða er að finna í [Hönnunarútgáfur og flokkar hönnunarafurðar](engineering-versions-product-category.md).

Í útgáfuferlinu er hægt að hafa áhrif á stillingar.

## <a name="create-and-manage-product-release-policies"></a>Stofna og stjórna reglum um afurðarlosun

Til að vinna með reglum um afurðarlosun skal fara í **Umsjón hönnunarbreytinga \> Uppsetning \> reglur um afurðarlosun**. Fylgið svo einu af eftirfarandi skrefum.

- Til að stofna nýjan flokk skal velja **Ný** á aðgerðasvæðinu og síðan stilla reitina eins og lýst er í eftirfarandi undirköflum.
- Til að breyta fyrirliggjandi reglu skal velja hana úr listasvæðinu, velja **Breyta** á aðgerðasvæðinu og síðan stilla reitina eins og lýst er í eftirfarandi undirköflum.
- Til að eyða fyrirliggjandi reglu skal velja hana á listasvæðinu, velja **Breyta** á aðgerðasvæðinu, og síðan í flýtiflipanum **Almennt** skal ganga úr skugga um að valkosturinn **Virkur** sé stilltur á *Nei*. Veljið svo **Eyða** á aðgerðasvæðinu.

### <a name="header"></a>Haus

Stillið eftirfarandi reiti á haus fyrir reglu afurðarlosunar.

| Svæði | lýsing |
|---|---|
| Nafn | Færið inn heiti fyrir regluna. |
| lýsing | Færðu inn lýsingu á reglunni. |

### <a name="general-fasttab"></a>Flýtiflipinn Almennt

Stillið eftirfarandi reiti á flipanum **Almennt** fyrir reglu afurðarlosunar.

| Svæði | lýsing |
|---|---|
| Gerð afurðar | Veljið hvort reglan eigi við um afurðir af gerðinni *Vara* eða *Þjónusta*. Ekki er hægt að breyta þessari stillingu eftir að búið er að vista færsluna. |
| Nota sniðmát | Velja skal einn eftirfarandi valkosta til að tilgreina hvort og hvernig eigin að nota sniðmát fyrir afurðarlosun þegar reglan er notuð:<ul><li>**Alltaf** – Alltaf verður að nota sniðmát losaðrar afurðar fyrir losanir. Ef þessi valkostur er valinn skal nota flýtiflipann **Allar afurðir** til að tilgreina sniðmátið sem er notað fyrir hvert fyrirtæki sem losað er til. Ef sniðmát er ekki tilgreint fyrir hvert fyrirtæki sem er sýnt í flýtiflipanum **Allar afurðir**, færðu villu þegar reynt er að vista regluna.</li><li>**Valfrjálst** - Ef sniðmát losaðrar afurðar er tilgreint fyrir fyrirtæki sem er sýnt í flýtiflipanum **Allar afurðir** verður það sniðmát notað þegar losað er í það fyrirtæki. Annars verður ekkert sniðmát notað. Ef þessi valkostur er valinn er hægt að vista regluna án þess að úthluta sniðmátum á öll fyrirtæki. (Engin viðvörun birtist.)</li><li>**Aldrei** – Ekkert sniðmát losaðrar afurðar verður notað fyrir nein fyrirtæki sem losað er til, jafnvel þótt sniðmát er tilgreint fyrir fyrirtæki sem eru sýnd í flýtiflipanum **Allar afurðir**. Dálkar sniðmáts verða ekki tiltækir.</li></ul> |
| Í gangi | Notið þennan valkost til að auðvelda að vinna með losunarreglurnar. Stillið hann á *Já* fyrir allar losunarreglur sem notaðar eru. Stillið þetta á *Nei* til að merkja losunarreglu sem óvirka þegar hún er ekki notuð. Athugið að ekki er hægt að gera losunarreglu óvirka sem er úthlutað á flokk hönnunarafurðar, og aðeins er hægt að eyða óvirkum undirbúningsreglum. |

### <a name="all-products-fasttab"></a>Flýtiflipi allra afurða

Í flýtiflipanum **Allar afurðir** skal bæta við línu fyrir hvert rekstrarfyrirtæki þar sem á að nota þessa reglu til að losa til. Notið hnappana í flýtiflipanum **Allar afurðir** til að bæta við og fjarlægja línur eftir þörfum. Stillið eftirfarandi reiti fyrir hverja línu sem er bætt við.

> [!NOTE]
> Stillingarnar í flýtiflipanum **Allar afurðir** eiga við um bæði hönnunarafurðir og staðlaðar afurðir.

| Svæði | lýsing |
|---|---|
| Kenni reikningsskila | Veljið fyrirtækið sem línan á við. Færibreyturnar á línunni munu eiga við þegar afurðir eru losaðar í þetta fyrirtæki. |
| Sniðmát losaðrar afurðar | Bæta við sniðmáti fyrir afurðina. |
| Afrita samþykki uppskriftar | Veljið þennan gátreit til að afrita samþykktarstöðu uppskriftar í viðtökufyrirtækið. |
| Afrita virkjun uppskriftar | Veljið þennan gátreit til að afrita virkjunarstöðu uppskriftar í viðtökufyrirtækið. |
| Afrita samþykki leiðar | Veljið þennan gátreit til að afrita samþykktarstöðu leiðar í viðtökufyrirtækið.|
| Afrita leið virkjunar | Veljið þennan gátreit til að afrita virkjunarstöðu leiðar í viðtökufyrirtækið. |

### <a name="option-parameters-for-engineering-products-fasttab"></a>Flýtiflipi valfrjálsra færibreyta fyrir hönnunarafurðir

Í hvert skipti sem línu er bætt við flýtiflipann **Allar afurðir** verður lína sem er með samsvarandi gildi fyrir **Kenni fyrirtækjareiknings** einnig stofnuð í flýtiflipanum **Valfrjálsar færibreytur fyrir hönnunarafurðir**. Síðan, ef lína er fjarlægð úr flýtiflipanum **Allar afurðir**, verður línan sem er með samsvarandi gildi fyrir **Kenni fyrirtækjareiknings** einnig fjarlægt úr flýtiflipanum **Valfrjálsar færibreytur fyrir hönnunarafurðir**.

Fyrir hverja línu sem er sýnd í flýtiflipanum **Valfrjálsar færibreytur fyrir hönnunarafurðir** skal stilla eftirfarandi reiti.

> [!NOTE]
> Stillingarnar í flýtiflipanum **Valfrjálsar færibreytur fyrir hönnunarafurðir** eiga bara við um hönnunarafurðir.

| Svæði | lýsing |
|---|---|
| Sniðmátsuppskrift | Þegar afurð sem er með uppskrift er losuð verður línum tilgreindrar sniðmátsuppskriftar bætt við. Þessi reitur er gagnlegur til að bæta staðbundnum íhlutum við, t.d. umbúðum eða leiðbeiningum á staðbundnu tungumáli. |
| Leið sniðmáts | Þegar afurð sem er með leið er losuð verður línum tilgreinds sniðmáts bætt við. |
| Afrita áhrif | Veljið hvort afrita eigi gildisdagsetningar úr hönnunarfyrirtækinu yfir í rekstrarfyrirtækið þegar afurðir eru losaðar. |
| Bæta sjálfkrafa við tillögu um losun | Veljið þennan gátreit fyrir afurðir sem á að losa sjálfkrafa í beiðni um hönnunarbreytingu. Á þennan hátt er hægt að losa sjálfkrafa afurðir sem tilheyra flokkum hönnunarafurða sem nota þessa losunarreglu í rekstrarfyrirtæki þar sem þessi valkostur er uppsettur. (Frekari upplýsingar eru í [Vinna með breytingar á hönnunarafurðum](engineering-change-management.md).)

### <a name="review-each-product-when-you-release-it"></a>Yfirfara hverja afurð þegar hún er losað

Þegar hönnunarafurðir sem eru með uppskriftir eða leiðir eru losaðar, verða færibreyturnar stilltar á sjálfgefin gildi, eins og tilgreint er í losunarreglunni. Sem notandi geturðu haft áhrif á þessa hegðun losunar þegar þú notar skipulag afurðarlosunar.

Til að losa hönnunarafurðir, á síðunni **Losaðar afurðir**, skal velja afurðirnar til að losa og síðan velja **Skipulag afurðarlosunar** til að opna leiðsagnarforrit losunar. Síðan **Veljið hönnunarafurð sem á að losa** sýnir afurðirnar. Velja skal eina afurð og síðan skal velja **Upplýsingar um losun** til að yfirfara upplýsingar um losun fyrir afurðina.

Á síðunni **Upplýsingar um losun** er hægt að breyta gildinu í reitunum **Taka á móti uppskrift**, **Afrita samþykki uppskriftar**, **Afrita virkjun uppskriftar**, **Taka á móti uppskrift**, **Afrita samþykki leiðar** og **Afrita virkjun leiðar**. Í push-pull kringumstæðum er hægt að breyta gildinu á sömu reitunum móttökumegin, svo lengi sem uppskriftin og leiðin hafa verið losuð.

## <a name="product-owners-and-product-releases"></a>Eigendur afurða og afurðarlosun

Vegna þess að eigendur afurða vita hvaða lögaðilar þurfa afurðirnar, er aðeins hægt að losa afurð ef meðlimir þeirrar afurðar eru í hópi eigenda þeirrar afurðar. Aðrir notendur geta ekki losað afurðir sem þeir eiga ekki.

Þessi hegðun á aðeins við þegar afurð er valin beint fyrir losun. Afurðir sem eru hluti af skipulagi annarrar afurðar í gegnum uppskrift *geta* verið losaðar af notendum sem eru ekki eigendur þegar þeir losa yfirafurðina, svo lengi sem þeir eiga yfireiningu afurðarinnar.

Til dæmis er afurð X úthlutað á afurðareigendahópinn *Hanna skápa*. Afurð X er einnig hluti af uppskrift afurðar Y, sem er úthlutað á afurðareigendahópinn *Hanna hátalara*. Ef notandi úr afurðareigendahópnum *Hanna hátalara* losar afurð Y og uppskrift hennar, verður afurð X losuð saman um leið og afurð Y.

Frekari upplýsingar er að finna í [Eigendur afurða](product-owner.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]