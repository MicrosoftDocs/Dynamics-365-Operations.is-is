---
title: Gæðastjórnun fyrir vöruhúsaferli
description: Þetta efnisatriði veitir upplýsingar um gæðastjórnun fyrir eiginleika vöruhúsaferlis. Þessi eiginleiki eykur getu gæðastjórnunar og gerir notendum kleift að samþætta stjórnun vörusýnatöku við móttökuferli vöruhúss með því að nota ítarlegt vöruhúsakerfi.
author: Henrikan
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-02
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 79eb7d750869ef365ad117ecc024afc8db2edbf7
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348830"
---
# <a name="quality-management-for-warehouse-processes"></a>Gæðastjórnun fyrir vöruhúsaferli

Eiginleikinn _Gæðastjórnun fyrir vöruhúsaferla_ gerir þér kleift að samþætta stjórnun vörusýnatöku við móttökuferli vöruhúss með því að nota ítarlegt vöruhúsakerfi. Vöruhúsavinnu er hægt að gera þannig að hún færi birgðir sjálfkrafa á staðsetningu gæðastjórnunar, byggt á prósentu eða föstu magni, eða byggt á *n* hverri númeraplötu. Eftir að lokið hefur verið við gæðapöntun, er hægt að gera vinnu þannig að hún færi birgðir sjálfkrafa á næstu staðsetningu í ferlinu, háð gæðaniðurstöðum.

Eiginleikinn _Gæðastjórnun fyrir vöruhúsaferla_ eykur möguleika eiginleika grunngæðastjórnunar. Hann býður upp á möguleika á að búa til gæðapantanir fyrir birgðirnar sem sendar eru á staðsetningu gæðastjórnunar, þótt gæðapantanir séu ekki alltaf nauðsynlegar. Þar af leiðandi býður hann upp á létt gæðastjórnunarferli sem byggist á vöruhúsavinnu.

## <a name="turn-on-the-quality-management-for-warehouse-processes-feature"></a>Kveikja á gæðastjórnun fyrir eiginleika vöruhúsaferlis

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Gæðastjórnun fyrir vöruhúsaferli*

## <a name="key-benefits"></a>Lykilávinningur

Eiginleikinn _Gæðastjórnun fyrir vöruhúsaferli_ býr sjálfkrafa til vinnu sem hluta af móttökuferlinu til að færa birgðamagnið sem þarf til gæðaeftirlits á gæðastjórnunarstað. Ef magnið sem er móttekið er hærra en það magn sem þarf fyrir gæðaeftirlit (samkvæmt uppsetningu á sýnatöku hlutarins) er umfram magnið flutt á heimleið sem er skilgreint í uppsetningu staðartilskipunar. Eftir að gæðapöntunin er staðfest er vinna búin til sjálfkrafa til að flytja magn gæðapöntunar á nýja staðsetningu innanhúss eða skilastaðsetningu, samkvæmt niðurstöðum staðfestingar og uppsetningu staðsetningarleiðbeiningar. Vinna sem sjálfkrafa er búin til, sem er aðeins með magnið sem verður að flytja til og frá gæðastjórnun, býður upp á samþætt ferli.

> [!NOTE]
> Þegar kveikt er á eiginleikanum _Gæðastjórnun fyrir vöruhúsaferli_ geturðu áfram nýtt þér handvirka aðferðina. Í handvirku ferli eru birgðahreyfingar og hreyfingar samkvæmt sniðmáti notaðar til að fá starfsmann vöruhúss til að setja í gang stofnun vöruhúsavinnu til að flytja birgðir frá staðsetningu gæðastjórnunar til nýrrar staðsetningar. Einnig er enn hægt að setja upp staðsetningarleiðbeiningar innanhúss sem flytja birgðir í heild sinni frá móttökustaðsetningu til staðsetningar gæðastjórnunar án þess að taka tillit til uppsetningu vörusýnatöku.

## <a name="quality-management-and-the-quality-management-for-warehouse-processes-feature"></a>Gæðastjórnun fyrir vöruhúsaferli og Gæðastjórnun fyrir vöruhúsaferli eiginleikinn

Þegar kveikt er á eiginleikanum _Gæðastjórnun fyrir vörugeymslur_ breytir það skipulagi lykilstjórnunar og gæðastjórnunaraðila. Eftirfarandi mynd sýnir yfirlit yfir einingarnar sem virkja gæðapantanir fyrir vöruhúsaferli. Texti í sviga tilgreinir ráðlagðar aðgerðir þegar gæðastjórnun var notuð áður en kveikt var á eiginleikanum _Gæðastjórnun fyrir vöruhúsakerfisferla_.

![Gæðastjórnunareiningar.](media/quality-management-entity-diagram.png "Gæðastjórnunareiningar")

## <a name="enablers-the-quality-item-sampling-and-quality-order-work-order-types"></a>Virkjarar: Vörusýnataka gæðaskoðunar og verkbeiðnigerðir gæðapöntunar

Eiginleikinn _Gæðastjórnun fyrir vöruhúsaferli_ er með tvær gerðir verkbeiðna sem virkja verkgerð:

- **Vörusýnataka gæðaskoðunar** - Þessi verkbeiðnigerð er notuð til að búa til vinnu sem flytur skráðar birgðir til gæðastjórnunar.
- **Gæðapöntun** - Þessi verkbeiðnigerð er notuð til að búa til vinnu sem flytur birgðir frá gæðastjórnun til nýrrar staðsetningar samkvæmt uppsetningu staðsetningarleiðbeiningar.

### <a name="work-classes-location-directives-and-work-templates"></a>Vinnuklasar, staðsetningarleiðbeiningar og vinnusniðmát

Verkbeiðnigerðirnar _Vörusýnataka gæðaskoðunar_ og _Gæðapöntun_ eru notaðar af staðsetningarleiðbeiningum, vinnuklösum og vinnusniðmátum.

Áður en hægt er að búa til vöruhúsavinnu til að sjálfkrafa flytja birgðir til gæðastjórnunar þarf að fylgja þessum skrefum til að setja upp kerfið.

1. Búa skal til aðskilda vinnuklasa fyrir verkbeiðnigerðirnar _Vörusýnataka gæðaskoðunar_ og _Gæðapöntun_. Með þessu móti tryggir þú að sjálfkrafa sé hægt að búa til viðeigandi vinnu á samkvæmt tveimur verkbeiðnigerðum og að þessa vinnu sé síðan hægt að keyra með því að nota farsímaforrit vöruhúsakerfis.
1. Þú getur sett upp vinnusniðmát fyrir hverja verkbeiðnistegund.

    - Settu upp vinnusniðmát sem notar verkbeiðnigerðina _Vörusýnataka gæðaskoðunar_ til að flytja sjálfkrafa skráðar birgðir til staðsetningar gæðastjórnunar.
    - Settu upp vinnusniðmát sem notar verkbeiðnigerðina _gæðapöntun_ til að flytja birgðir frá staðsetningu gæðastjórnunar eftir að gæðastjórnun lýkur.

1. Fyrir hverja verkbeiðnigerð skal setja upp staðsetningarleiðbeiningar sem nota réttar staðsetningar gæðastjórnunar sem færa á birgðirnar til. Þegar gæðastjórnun er lokið gengur verkbeiðnigerðin _Gæðapöntun_ úr skugga um að ný áfangastaðsetning verði valin svo að hægt sé að flytja birgðirnar úr staðsetningu gæðastjórnunar.
1. Settu upp viðeigandi valmyndaratriði fartækis til að styðja flutning á mótteknum birgðum til staðsetningar gæðastjórnunar og flutning birgða sem gæðastjórnun samþykkir eða hafnar úr staðsetningu gæðastjórnunar til nýrrar staðsetningar.

Fyrir nákvæmar leiðbeiningar sem sýna hvernig á að ljúka þessari uppsetningu skal skoða [dæmi um atburðarás](#example-scenario) í lokin á þessu efnisatriði.

## <a name="enable-a-warehouse-for-quality-management"></a>Virkja vöruhús fyrir gæðastjórnun

Áður en hægt er að nota eiginleikann _Gæðastjórnun fyrir vöruhúsaferli_ fyrir ákveðið vöruhús, þarf að fylgja þessum skrefum til að gera eiginleikann tiltækan fyrir þetta vöruhús.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Vöruhús**.
1. Veldu vöruhúsið sem nota á í gæðastjórnun.
1. Í flýtiflipanum **Vöruhús** skal stilla valkostinn **Virkja gæðapöntun fyrir vöruhúsaferli** á _Já_. (Athugið að aðeins er hægt að stilla þennan valkost á _Já_ fyrir vöruhús sem nota vöruhúsakerfisferli.)

Þegar valkosturinn **Virkja gæðapöntun fyrir vöruhúsaferli** er stilltur á _Já_ stjórnar uppsetning gæðatengingar því hvort eiginleikinn _Gæðastjórnun fyrir vöruhúsaferli_ sé í raun og veru notuð fyrir valið vöruhús. Hægt er að breyta valkostinum í _Nei_ hvenær sem er. Þá á eiginleikinn ekki lengur við fyrir vöruhúsið, óháð uppsetningu gæðatengingar.

## <a name="quality-control"></a>Gæðaeftirlit

Eiginleikinn _Gæðastjórnun fyrir vöruhúsaferli_ stjórnar nokkrum mikilvægum stillingum fyrir gæðatengingar og vörusýnatöku.

### <a name="quality-associations"></a>Gæðatengingar

Hver [gæðatengingafærsla](enable-quality-management.md) skilgreinir einnig prófanir, viðunandi gæðastig og úrtaksáætlun sem eiga við myndaðar gæðapantanir. Til að setja upp færslu gæðatengingar skal fylgja þessum skrefum:

1. Fara í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Gæðatengingar**.
1. Búðu til eða veldu færslu gæðatengingar fyrir vöruna eða flokkinn sem unnið er með, eða fyrir allar vörur.
1. Í flýtiflipanum **Skilmálar** skal stilla reitinn **Viðeigandi gerð vöruhúss** á eitt af eftirfarandi gildum:

    - **Gæðastjórnun fyrir vöruhúsaferli eingöngu** - Virkja eiginleikann _Gæðastjórnun fyrir vöruhúsaferli_. Aðeins er hægt að velja þetta gildi ef tilvísunargerðin er annaðhvort *Innkaup* eða *Framleiðsla*.
    - **Allt** – Óvirkjaðu _Gæðastjórnun fyrir vöruhúsaferli_ eiginleikinn. Veldu þetta gildi fyrir allar tilvísunargerðir nema *Innkaup* og *Framleiðsla*.

> [!NOTE]
> Eiginleikinn _Gæðastjórnun fyrir vöruhúsaferli_ tekur aðeins gildi ef varan í upprunaskjalslínunni notar ítarlegt vöruhúsakerfisferli og ef valkosturinn **Virkja gæðapöntun fyrir vöruhúsaferli** er stilltur á _Já_ fyrir vöruhúsið á upprunaskjalslínunni.

Þegar hver vara er skráð (eða gefin upp sem lokið) ákvarðar kerfið hvaða gæðatengingar eiga við.

Þegar kveikt er á eiginleikanum _Gæðastjórnun fyrir vöruhúsaferli_ er viðeigandi gerð vöruhúss sett inn í fjórða leitarhóp leitarstigveldis gæðatengingar. Eftirfarandi tafla sýnir röklega framsetningu leitarstigveldisins.

| Leit að „Hópur“ | lýsing |
|---|---|
| Flokkur 1 | Fyrir hverja gæðatengingu skal athuga gildin **Gerð tilvísunar**, **Gerð tilviks** og **Samsvörun keyrslu** með hliðsjón af vörunni. Ef það er samsvörun við upprunaskjalalínuna skaltu fara í flokk 2. |
| Flokkur 2 | Fyrir hverja gæðatengingu skal athuga gildið **Vörukóði** (_Tafla_, _Flokkur_ eða _Allt_) með hliðsjón af vörunni. _Tafla_ er sértækari en _Flokkur_ og _Flokkur_ er sértækari en _Allt_. Ef það er samsvörun fyrir _Tafla_ (tiltekna vöru) skal fara í flokk 3. Ef ekki er samsvörun fyrir _Tafla_ skal leita að samsvörun fyrir _Flokkur_. Ef ekki er samsvörun fyrir _Flokkur_ á _Allt_ við. Ef það er samsvörun skal fara í flokk 3. |
| Flokkur 3 | Fyrir hverja gæðatengingu skal athuga gildin **Lykilkóði** og **Tilfangakóði** með hliðsjón af vörunni. Reglan sem er notuð líkist reglunni sem er notuð fyrir gildið **Vörukóði**. |
| Flokkur 4 | Fyrir hverja gæðatengingu skal athuga gildið **Viðeigandi gerð vöruhúss** (_Gæðastjórnun fyrir vöruhúsaferli eingöngu_ eða _Allt_) með hliðsjón af vörunni. Ef valkosturinn **Virkja gæðapöntun fyrir vöruhúsaferli** er stilltur á _Já_ fyrir vöruhús upprunaskjalsins og varan í upprunaskjalslínunni er stillt á _Nota ferli vöruhúsakerfis_, eiga bæði tengingar þar sem er samsvörun fyrir _Gæðastjórnun fyrir vöruhúsaferli eingöngu_ og tengingar þar sem samsvörun fyrir _Allt_ við samhliða ef bæði er til staðar. Ef valkosturinn **Virkja gæðapöntun fyrir vöruhúsaferli** er stilltur á _Já_ fyrir vöruhús upprunaskjalsins og varan í upprunaskjalslínunni er stillt á _Nota ferli vöruhúsakerfis_ á aðeins gæðastjórnun við. |

Ef þú hefur til dæmis skilgreint vöruhús þar valkosturinn **Virkja gæðapöntun fyrir vöruhúsaferli** er stilltur á _Já_ og þú ert með tvær gæðatengingar sem eru skilgreindar fyrir tilvísunargerðina *Innkaup*: eina fyrir allar vörur og eina fyrir tilviksgerðina *Skráning*. Eini munurinn á milli gæðatenginganna tveggja er gildið **Viðeigandi gerð vöruhúss**: það er stillt á _Allt_ fyrir eina gæðatengingu og _Gæðastjórnun fyrir vöruhúsaferli eingöngu_ fyrir hina. Í þessu tilfelli eru báðar gæðatengingarnar jafn sérstækar og eiga báðar við.

Gildi reitsins **Prófunarflokkur** fyrir gæðatengingarnar er einnig stór þáttur. Þessi reitur skilgreinir prófunaraðferðina sem þarf að nota. Ef gildið **Prófunarflokkur** er það sama fyrir báðar gæðatengingarnar, verður aðeins ein gæðapöntun búin til fyrir gæðatenginguna þar sem gildið **Viðeigandi gerð vöruhúss** er _Gæðastjórnun fyrir vöruhúsaferli eingöngu_. Ef gildið **Prófunarflokkur** er ekki það sama fyrir báðar gæðatengingarnar verða tvær gæðapantanir búnar til. Fyrsta gæðapöntunin verður búin til fyrir gæðatenginguna þar sem gildið **Viðeigandi gerð vöruhúss** er _Gæðastjórnun fyrir vöruhúsaferli eingöngu_. Seinni gæðapöntunin verður búin til fyrir gæðatenginguna þar sem gildið **Viðeigandi gerð vöruhúss** er _Allt_.

> [!NOTE]
> Gildið _Gæðastjórnun fyrir vöruhúsaferli eingöngu_ er talið sértækara en _Allt_ þegar skilyrðið fyrir gæðatengingar fyrir flokk 1 og 2 er það sama og þegar prófunarflokkurinn er sá sami. Tvær gæðapantanir verða aðeins búnar til þegar prófhóparnir eru ólíkir.

#### <a name="reference-types"></a>Tilvísunargerðir

Þegar gildið **Tilvísunargerð** er _Innkaup_ og gildið **Viðeigandi gerð vöruhúss** er _Gæðastjórnun fyrir vöruhúsaferli eingöngu_ verður reiturinn **Tilviksgerð** í flýtiflipanum **Ferli** að vera stilltur á _Skráning_. _Skráning_ er eina studda tilviksgerðin fyrir tilvísunargerðina _Innkaup_ þegar eiginleikinn _Gæðastjórnun fyrir vöruhúsaferli_ er notaður.

#### <a name="quality-processing-policy"></a>Vinnureglur gæðamála

Eiginleikinn _Gæðastjórnun fyrir vörugeymsluferla_ gerir kleift að búa til vinnu eingöngu út frá vörusýni. Hann býður því upp á létt ferli. Vinnan sem birgðir búa til fer eftir vörusýnatökunni sem tengist gæðatengingunni. Þegar létta ferlið er notað, þegar starfsmaður setur magnið í staðsetningu gæðastjórnunar, getur gæðadeildin búið til gæðapöntun handvirkt ef gæðapöntun er nauðsynleg.

Reiturinn **Regla gæðaúrvinnslu** í flýtiflipanum **Ferli gæðapöntunar** stýrir því hvort gæðapöntun er einnig búin til þegar vinna er búin til til að flytja vöru á staðsetningu gæðastjórnunar. Hægt er að stilla þennan reit á _Stofna gæðapöntun_ eða _Stofna eingöngu verk_. Sjálfgefið gildi er _Stofna gæðapöntun_.

> [!NOTE]
> Óháð því hvort búnar séu til gæðapantanir handvirkt eða sjálfkrafa, býr kerfið sjálfkrafa til vinnu til að flytja vörur frá staðsetningu gæðastjórnunar þegar gæðapöntunin er merkt sem staðfest.

Stofnun gæðapöntunarvinnu er ekki tengd uppsetningu gæðatengingar. Ef vinnusniðmát er fyrir hendi sem hefur gildið **Verkbeiðnigerð** af *Gæðapöntun* og ef skilyrði fyrirspurnar er uppfyllt fyrir það vinnusniðmát, mun staðfesting á gæðapöntun setja af stað stofnun gæðapöntunarvinnu.

#### <a name="referenced-item-sampling"></a>Uppsetning vörusýna

Sérhver gæðatenging verður að vísa til vörusýnatöku. Vörusýnataka skilgreinir magnið sem verður sent til gæðastjórnunar. Hægt er að setja hana upp svo að hún eigi aðeins við um gæðatengingar þar sem gildið **Viðeigandi gerð vöruhúss** er _Gæðastjórnun fyrir vöruhúsaferli eingöngu_. Ef gildið **Umfang sýnatöku** fyrir vörusýnatöku er _Farmur_ eða _Sending_ eða gildið **Tilgreint magn** er _Full númeraplata_, geta gæðatengingar aðeins vísað til vörusýnatökunnar þar sem gildið **Viðeigandi gerð vöruhúss** er _Gæðastjórnun fyrir vöruhúsaferli eingöngu_.

Ef skilgreind er vörusýnataka sem notar viðeigandi vöruhúsagerð _Gæðastjórnun fyrir vöruhúsaferli eingöngu_ kemur upp villa ef reynt er að vísa til hennar frá gæðatengingu sem notar ekki eiginleikann _Gæðastjórnun fyrir vöruhúsaferli_.

> [!NOTE]
> Vörusýnataka sem notar algera stöðvun er ekki studd fyrir gæðatengingar þar sem reiturinn **Viðeigandi gerð vöruhúss** er stilltur á _Gæðastjórnun fyrir vöruhúsaferli eingöngu_.

### <a name="item-sampling"></a>Vörusýnishorn

Vörusýnataka stýrir því hversu oft vörur eru sendar í gæðastjórnun. Eiginleikinn _Gæðastjórnun fyrir vöruhúsaferli_ kynnir hugmyndina um _umfang vörusýnatöku_. Kerfið notar umfang vörusýnatöku þegar það metur hvort og hvernig eigi að stofna gæðapantanir og/eða gæðavinnu vörusýnatöku og gæðapöntunarvinnu.

Til að setja upp vörusýnatöku skal fara í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Vörusýnataka** og stilla reitinn **Umfang sýnatöku** á eitt af eftirfarandi gildum:

- **Pöntun** - Upprunaskjalslínan verður grunnurinn að mati á því hvort og hvernig gæðapantanir og/eða gæðavinna vörusýnatöku og gæðapöntunarvinna er stofnuð. Þetta gildi er sjálfgefið gildi og þegar það er valið virkar kerfið á sama hátt og það virkar þegar ekki er kveikt á eiginleikanum _Gæðastjórnun fyrir vöruhúsaferli_.
- **Farmur** - Farmar verða notaður sem grunnur að mati á því hvort og hvernig gæðapöntun og/eða vinna er stofnuð. Þetta gildi er aðeins tiltækt þegar kveikt er á eiginleikanum _Gæðastjórnun fyrir vöruhúsaferli_.
- **Sending** - Sendingar verða notaðar sem grunnur að mati á því hvort og hvernig gæðapöntun og/eða vinna er stofnuð. Þetta gildi er aðeins tiltækt þegar kveikt er á eiginleikanum _Gæðastjórnun fyrir vöruhúsaferli_.

> [!NOTE]
> Þegar reiturinn **Umfang sýnatöku** er stilltur á *Farmur* eða *Sending* verða einingar farms og sendingar notaðar ef þær eru í boði. Ef þær eru ekki í boði verður pöntunareiningin notuð.

Eiginleikinn _Gæðastjórnun fyrir vöruhúsaferli_ býður einnig upp á gildið *Full númeraplata* fyrir reitinn **Tilgreint magn**. Þetta gildi styður stofnun gæðapöntunarvinnu og gæðavinnu vörusýnatöku eftir númeraplötum. Þegar þetta gildi er valið gerast eftirfarandi breytingar:

- Valkosturinn **Skipta talningu eftir vöru** og reiturinn **Fyrir hverja n númeraplötu** í flýtiflipanum **Úrvinnsla** verður í boði.
- Reiturinn **Gildi** í flýtiflipanum **Magn sýnatöku** verður ekki í boði.
- Valkostirnir **Fyrir hvert uppfært magn**, **Staðsetning** og **Númeraplata** eru allir stilltir á *Já* og stillingunum er ekki hægt að breyta.

Valkosturinn **Skipta talningu eftir vöru** stýrir því hvort talning númeraplötu er metin eftir vöru eða öllum vörum í umfangi sýnatökunnar. Vöruafbrigði eru meðhöndluð sem sami hlutur. Þessi valkostur stjórnar einnig hvort fjöldi númeraplötunnar er endurstilltur fyrir hvern hlut.

Gildið í reitnum **Fyrir hverja n númeraplötu** stýrir því hversu oft gæðapantanir eru stofnaðar í tengslum við vörufjöldann sem er skráður. Til dæmis mun gildið *3* senda þriðju hverja vöru til gæðastjórnunar, sem hefst á fyrstu vörunni. Gildið verður að vera meira en 0 (núll).

Á meðan starfskraftar taka á móti vörum með því að nota farsímaforrit vöruhúsakerfis staðfestir kerfið hvort gæðatenging sé uppsett fyrir sérhverja vöru á innleið. Ef gæðatenging er sett upp, notar kerfið færslu vörusýnatöku sem stillt er fyrir gæðatengingu sem um ræðir til að ákvarða hvernig það mun stofna gæðapantanir, gæðavinnu vörusýnatöku og innkaupapöntunarvinnu.

> [!NOTE]
> Þegar móttökuskráningu lýkur í vefbiðlaranum (með því að nota litlu skráningasíðuna eða komubók vörunnar fyrir innkaupapöntunarlínur) verður engin gæðavinna vörusýnatöku eða innkaupapöntunarvinna stofnuð, burtséð frá uppsetningunni. Fyrir vörur sem passa við gæðatengingu verður tilvísuð vörusýnataka í staðinn notuð til að stjórna stofnun á gæðapöntunum eingöngu.

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Dæmi um sjálfvirka myndun þjónustupantana

Eftirfarandi dæmi sýna hvernig uppsetning gæðatengingar og tengd vörusýnataka hefur áhrif á stofnun gæðapantana þegar reiturinn **Viðeigandi gerð vöruhúss** er stilltur á _Gæðastjórnun fyrir vöruhúsaferli eingöngu_.

Þegar gildið **Tilgreint magn** er _Full númeraplata_ stjórnar reiturinn **Fyrir hverja n númeraplötu** því fyrir hvaða númeraplötur gæðavinna vörusýnatöku er stofnuð fyrir. Fyrsta númeraplatan fer alltaf í gæðastjórnun og tilgreinir gildi reitsins að í hvert *n* skipti skal númeraplata fara í sýnatöku.

Gildið **Tilvísunargerð** fyrir eftirfarandi dæmi er _Innkaup_ og gildið **Tilviksgerð** er *Skráning*.

| Umfang sýnatöku | Uppsetning magns | Uppfært magn á | Á geymsluvídd | Skipta talningu eftir vöru | Á x númeraplötu | Niðurstaða |
|---|---|---|---|---|---|---|
| Pöntun | Full númeraplata | Já _(læst/ekki hægt að breyta)_ | <p>Staðsetning: Já</p><p>Númeraplata: Já _(læst/ekki hægt að breyta)_</p> | Ekkert | 3 | <p>**Pöntunarlínamagn: 100 EA**</p><ol><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir 20 EA, LP1<p>Gæðavinna sýnatöku fyrir 20 EA</p><p>Gæðapöntun 1 fyrir 20 EA</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir 20 EA, LP2<p>Innkaupapöntunarvinna fyrir 20 EA (frágangur)</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir 20 EA, LP3<p>Innkaupapöntunarvinna fyrir 20 EA (frágangur)</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir 20 EA, LP4<p>Gæðavinna sýnatöku fyrir 20 EA</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir 20 EA, LP5<p>Innkaupapöntunarvinna fyrir 20 EA (frágangur)</p></li></ol> |
| Pöntun | Fast magn = 1 | Já | <p>Staðsetning: Já</p><p>Númeraplata: Já</p> | Ekkert | Ekki tiltækt | <p>**Pöntunarlínamagn: 100**</p><ol><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir 20 EA, LP1<p>Gæðavinna sýnatöku fyrir 1 EA</p><p>Gæðapöntun 1 fyrir 1 EA</p><p>Innkaupapöntunarvinna fyrir 19 EA (frágangur)</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir 20 EA, LP2<p>Gæðavinna sýnatöku fyrir 1 EA</p><p>Gæðapöntun 1 fyrir 1 EA</p><p>Innkaupapöntunarvinna fyrir 19 (frágangur)</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir 20 EA, LP3<p>Gæðavinna sýnatöku fyrir 1 EA</p><p>Gæðapöntun 1 fyrir 1 EA</p><p>Innkaupapöntunarvinna fyrir 19 EA (frágangur)</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir 20 EA, LP4<p>Gæðavinna sýnatöku fyrir 1 EA</p><p>Gæðapöntun 1 fyrir 1 EA</p><p>Innkaupapöntunarvinna fyrir 19 EA (frágangur)</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir 20 EA, LP5<p>Gæðavinna sýnatöku fyrir 1 EA</p><p>Gæðapöntun 1 fyrir 1 EA</p><p>Innkaupapöntunarvinna fyrir 19 EA (frágangur)</p></li></ol> |
| Pöntun | Prósenta = 10 | Ekkert | <p>Staðsetningin: Nei</p><p>Númeraplata: Nr.</p> | Ekkert | Ekki tiltækt | <p>**Pöntunarlínamagn: 100 EA**</p><ol><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir 50 EA, LP1<p>Gæðavinna sýnatöku fyrir 10 EA</p><p>Gæðapöntun 1 fyrir 10 EA</p><p>Innkaupapöntunarvinna fyrir 40 EA (frágangur)</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir 50 EA, LP2<p>Innkaupapöntunarvinna fyrir 50 EA (frágangur)</p></li></ol> |
| Sækja | Prósenta = 5 | Já _(læst/ekki hægt að breyta)_ | <p>Staðsetningin: Nei</p><p>Númeraplata: Nr.</p> | Ekkert | Ekki tiltækt | <p>**Pöntunarlínamagn: 500 EA**</p><p>**Tvær hleðslur: fyrri hleðsla 200 EA, seinni hleðsla 300 EA**</p><ol><li>Skrá kvittun í farsímaforrit vöruhúsakerfis fyrir fyrsta álag fyrir 100 EA<p>Gæðavinna sýnatöku fyrir 5 EA</p><p>Gæðapöntun 1 fyrir 5 EA</p><p>Innkaupapöntunarvinna fyrir 95 EA (frágangur)</p></li><li>Skrá kvittun í farsímaforrit vöruhúsakerfis fyrir fyrsta álag fyrir 100 EA<p>Gæðavinna sýnatöku fyrir 5 EA</p><p>Gæðapöntun 1 fyrir 5 EA</p><p>Innkaupapöntunarvinna fyrir 95 EA (frágangur)</p></li><li>Skrá kvittun í farsímaforrit vöruhúsakerfis fyrir seinni hleðsluna fyrir 300 EA<p>Gæðavinna sýnatöku fyrir 15 EA</p><p>Gæðapöntun 1 fyrir 15 EA</p><p>Innkaupapöntunarvinna fyrir 285 EA (frágangur)</p></li></ol> |
| Röð | Prósenta = 10 | Já | <p>Staðsetning: Já</p><p>Númeraplata: Já</p> | Ekkert | Ekki tiltækt | <p>**Pöntunarlínamagn: 100**</p><ol><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir 50 EA, LP1<p>Gæðavinna sýnatöku fyrir 5 EA</p><p>Gæðapöntun 1 fyrir 5 EA</p><p>Innkaupapöntunarvinna fyrir 45 EA (frágangur)</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir 50 EA, LP2<p>Gæðavinna sýnatöku fyrir 5 EA</p><p>Gæðapöntun 1 fyrir 5 EA</p><p>Innkaupapöntunarvinna fyrir 45 (frágangur)</p></li></ol> |
| Sækja | Full númeraplata | Já _(læst/ekki hægt að breyta)_ | <p>Staðsetning: Já</p><p>Númeraplata: Já _(læst/ekki hægt að breyta)_</p> | Ekkert | 3 | <p>**Tveir hlutir:**</p><ul><li>**Magn pöntunarlínu fyrir vöru A: 120 EA (4 bretti)**</li><li>**Pöntunarlínamagn fyrir atriði B: 90 EA (3 bretti)**</li></ul><p>**Ein hleðsla, tvær hleðslulínur með sitthvora pöntunarlínu**</p><ol><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir atriði A, 30 EA, LP1<p>Gæðavinna sýnatöku fyrir 30 EA</p><p>Gæðapöntun 1 fyrir 30 EA</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir atriði A, 30 EA, LP2<p>Innkaupapöntunarvinna fyrir 30 EA (frágangur)</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir atriði A, 30 EA, LP3<p>Innkaupapöntunarvinna fyrir 30 EA (frágangur)</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir atriði A, 30 EA, LP4<p>Gæðavinna sýnatöku fyrir 30 EA</p><p>Gæðapöntun 1 fyrir 30 EA</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir atriði B, 30 EA, LP5<p>Innkaupapöntunarvinna fyrir 30 EA (frágangur)</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir atriði B, 30 EA, LP6<p>Innkaupapöntunarvinna fyrir 30 EA (frágangur)</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir atriði A, 30 EA, LP7<p>Gæðavinna sýnatöku fyrir 30 EA</p><p>Gæðapöntun 1 fyrir 30 EA</p></li></ol> |
| Sækja | Full númeraplata | Já _(læst/ekki hægt að breyta)_ | <p>Staðsetning: Já</p><p>Númeraplata: Já _(læst/ekki hægt að breyta)_</p> | Já | 3 | <p>**Tveir hlutir:**</p><ul><li>**Magn pöntunarlínu fyrir vöru A: 120 EA (4 bretti)**</li><li>**Pöntunarlínamagn fyrir atriði B: 90 EA (3 bretti)**</li></ul><p>**Ein hleðsla, tvær hleðslulínur með sitthvora pöntunarlínu**</p><ol><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir atriði A, 30 EA, LP1<p>Gæðavinna sýnatöku fyrir 30 EA</p><p>Gæðapöntun 1 fyrir 30 EA</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir atriði A, 30 EA, LP2<p>Innkaupapöntunarvinna fyrir 30 EA (frágangur)</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir atriði A, 30 EA, LP3<p>Innkaupapöntunarvinna fyrir 30 EA (frágangur)</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir atriði A, 30 EA, LP4<p>Gæðavinna sýnatöku fyrir 30 EA</p><p>Gæðapöntun 1 fyrir 30 EA</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir atriði B, 30 EA, LP5<p>Gæðavinna sýnatöku fyrir 30 EA</p><p>Gæðapöntun 1 fyrir 30 EA</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir atriði B, 30 EA, LP6<p>Innkaupapöntunarvinna fyrir 30 EA (frágangur)</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir atriði A, 30 EA, LP7<p>Innkaupapöntunarvinna fyrir 30 EA (frágangur)</p></li></ol> |
| Sækja | Prósenta = 10 | Já _(læst/ekki hægt að breyta)_ | <p>Staðsetningin: Nei</p><p>Númeraplata: Nr.</p> | Ekkert | Ekki tiltækt | <p>**Pöntunarlínamagn: 100 EA**</p><p>**Engar hleðslur eru búnar til. Umfang pöntunar er notað.**</p><ol><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir 50 EA, LP1<p>Gæðavinna sýnatöku fyrir 5 EA</p><p>Gæðapöntun 1 fyrir 5 EA</p><p>Innkaupapöntunarvinna fyrir 45 EA (frágangur)</p></li><li>Skrá kvittun í farsímaforriti vöruhúsakerfis fyrir 50 EA, LP2<p>Gæðavinna sýnatöku fyrir 5 EA</p><p>Gæðapöntun 1 fyrir 5 EA</p><p>Innkaupapöntunarvinna fyrir 45 EA (frágangur)</p></li></ol> |

Þegar starfsmaður staðfestir eina af gæðapöntunum sem sýndar eru í fyrri töflu býr kerfið sjálfkrafa til gæðapöntunarvinnu til að flytja birgðir frá staðsetningu gæðastjórnunar til staðsetningarinnar sem skilgreind er í staðsetningarleiðbeiningunni fyrir verkbeiðnigerðina _Gæðapöntun_. Hægt er að setja upp hvaða staðsetningu sem er í þessum tilgangi, t.d. sem skila- eða geymslustaðsetningu, fer eftir niðurstöðu prófunar fyrir gæðapöntunina. Dæmi um þessa uppsetningu er að finna í [dæmi um atburðarás](#example-scenario) í lokin á þessu efnisatriði.

Hægt er að opna gæðapöntun sem hefur þegar verið staðfest, svo lengi sem að gæðapöntunarvinnan sem tengist því að flytja birgðirnar frá staðsetningu gæðastjórnunar sé ekki með gildið **Staða verks** sem *Lokuð* eða *Í vinnslu*.

## <a name="process-insights-when-multiple-quality-associations-coexist"></a>Innsýn í ferli þegar margar gæðatengingar eru til staðar

Hægt er að skilgreina og nota fleiri en eina gæðatengingu nota í upprunaskjalslínu og reitinn **Viðeigandi gerð vöruhúss** er hægt að stilla á _Gæðastjórnun fyrir vöruhúsaferli eingöngu_ fyrir sumar þessara gæðatenginga og _Allt_ fyrir annað.

Gildið **Tilvísunargerð** í eftirfarandi dæmi er _Innkaup_.

1. Fyrsta gæðatengingin er sett upp á eftirfarandi hátt:

    - **Virk gerð vöruhúss:** *Gæðastjórnun fyrir vöruhúsaferli eingöngu*
    - **Vörunúmer:** *A0001*
    - **Kóði lykils:** *Allt*
    - **Prófunarflokkur:** *Lokað rými*
    - **Vörusýnishorn:** *5 stykki*

1. Önnur gæðatengingin er sett upp á eftirfarandi hátt:

    - **Viðeigandi gerð vöruhúss:** *Allt*
    - **Vörukóði:** *Allt*
    - **Kóði lykils:** *Allt*
    - **Prófunarflokkur:** *Lokað rými*
    - **Vörusýnishorn:** *1 stykki*

1. Þriðja gæðatengingin er sett upp á eftirfarandi hátt:

    - **Virk gerð vöruhúss:** *Gæðastjórnun fyrir vöruhúsaferli eingöngu*
    - **Vörukóði:** *Allt*
    - **Kóði lykils:** *104*
    - **Prófunarflokkur:** *Viðnám*
    - **Vörusýnataka:** *Önnur hver númeraplata* (Þessi stilling þýðir að fyrsta, þriðja, fimmta númeraplata o.s.frv. sem mótteknar eru munu stofna gæðapöntun.)

1. Fjórða gæðatengingin er sett upp á eftirfarandi hátt:

    - **Viðeigandi gerð vöruhúss:** *Allt*
    - **Vörukóði:** *Allt*
    - **Kóði lykils:** *Allt*
    - **Prófunarflokkur:** *Viðnám*
    - **Vörusýnishorn:** *5 stykki*

1. Fimmta gæðatengingin er sett upp á eftirfarandi hátt:

    - **Viðeigandi gerð vöruhúss:** *Allt*
    - **Vörukóði:** *Allt*
    - **Kóði lykils:** *Allt*
    - **Prófunarflokkur:** *Keila*
    - **Vörusýnishorn:** *10%*

Innkaupapöntun með magn upp á 10 fyrir vöruna A0001 er nú stofnuð fyrir lánardrottin 104. Þá er innkaupapöntunarlína sem hefur magnið 10 skráð sem móttekin á einni númeraplötu með því að nota farsímaforrit vöruhúsakerfis. Niðurstaða er:

- Það er ein gæðapöntun frá fyrstu gæðatengingunni fyrir prófunarflokkinn *Lokað rými*. Magnið 5. Það er engin gæðapöntun frá seinni gæðatengingunni vegna þess að skilyrðið fyrir fyrstu gæðatenginguna er sértækara miðað við prófunarflokkinn *Lokað rými*.
- Það er ein gæðapöntun fyrir þriðju gæðatenginguna fyrir prófunarflokkinn *Viðnám*. Magnið 10. Það er engin gæðapöntun frá fjórðu gæðatengingunni vegna þess að skilyrðið fyrir fyrstu gæðatenginguna er sértækara en prófunarflokkurinn *Viðnám*.
- Það er ein gæðapöntun fyrir fimmtu gæðatenginguna fyrir prófunarflokkinn *Keila*. Magnið 1.

Í tengslum við stofnun einnar gæðapöntunar fyrir hverja gæðatengingu, er gæðavinna vörusýnatöku líka stofnuð. Skráð magn er aðeins 10. En vegna uppsetningar vörusýnatöku er samtala magns gæðapöntunar sem stofnuð er fyrir viðeigandi vöruhúsagerð *Gæðastjórnun fyrir vöruhúsaferli eingöngu* er 16, sem fer yfir skráð efnislegt magn upp á 10. Þess vegna verður vinna ekki búin til fyrir fulla gæðapöntun (16) vegna þess að aðeins 10 eru efnislega tiltækar til flutnings á staðsetningu gæðastjórnunar. Forgangsröðunin sem er notuð til að búa til gæðavinnu vörusýnatöku fylgir röð stofnunar gæðapantana:

- **Fyrsta gæðapöntun (magn = 5):** Gæðavinna vörusýnatöku er stofnuð fyrir 5. Magnið 5 (10 - 5) er nú eftir fyrir næstu stofnun á gæðavinnu vörusýnatöku.
- **Önnur gæðapöntun (magn = 10):** Gæðavinna vörusýnatöku er stofnuð fyrir 5. Magnið 0 (núll) er nú eftir fyrir næstu stofnun á gæðavinnu vörusýnatöku.
- **Þriðja gæðapöntun (magn = 1):** Engin gæðavinna vörusýnatöku er stofnuð.

Sem hluti af ferlinu við að búa til gæðapantanir er búin til birgðalæsing upp á 10. Birgðalæsingin vísar til hverrar gæðapöntunar fyrir sig. Samtala gæðapöntunarmagnsins er 16.

Þegar gæðapantanir eru staðfestar reynir kerfið að búa til gæðapöntunarvinnu fyrir hverja gæðapöntun sem er staðfest. Vegna þess að samtala magns gæðapöntunar fer umfram magnið sem er læst og þar af leiðandi tiltækt fyrir stofnun vinnu, er ekki hægt að stofna gæðapöntunarvinnu fyrir fullt magn gæðapöntunar eins og sýnt er hér. (Þetta dæmi heldur áfram með fyrra dæmið.)

1. **Staðfesta aðra gæðapöntun sem er stofnuð (magn = 10). Gæðapöntunarvinna er stofnuð fyrir magn upp á 4.**

    Stofnun gæðapöntunarvinnu er ræst af breytingu á magni birgðalæsingar. Þar sem samtala gæðapöntunarmagns var 16, leiðir staðfesting á magni upp á 10 til þess að eftirstandandi gæðapöntunarmagn verði staðfest sem jafnt og 6. Magn birgðalæsingar er minnkað úr 10 í 6. Minnkað magn um 4 úthlutað til stofnunar gæðapöntunarvinnu.

2. **Staðfesta fyrstu gæðapöntun sem er stofnuð (magn = 5). Gæðapöntunarvinna er stofnuð fyrir magn upp á 5.**

    Stofnun gæðapöntunarvinnu er ræst af breytingu á magni birgðalæsingar. Þar sem samtala gæðapöntunarmagns var 6, leiðir staðfesting á magni upp á 5 til þess að eftirstandandi gæðapöntunarmagn verði staðfest sem jafnt og 1. Magn birgðalæsingar er minnkað úr 6 í 1. Minnkað magn um 5 úthlutað til stofnunar gæðapöntunarvinnu.

3. **Staðfesta þriðju gæðapöntun sem er stofnuð (magn = 1). Gæðapöntunarvinna er stofnuð fyrir magn upp á 1.**

    Stofnun gæðapöntunarvinnu er ræst af breytingu á magni birgðalæsingar. Þar sem samtala gæðapöntunarmagns var 1, leiðir staðfesting á magni upp á 1 til þess að eftirstandandi gæðapöntunarmagn verði staðfest sem jafnt og 0 (núll). Birgðalæsing er fjarlægð (þ.e. magn birgðalæsingar er minnkað úr 1 í 0). Minnkað magn um 1 úthlutað til stofnunar gæðapöntunarvinnu.

> [!NOTE]
> Stofnun gæðapöntunarvinnu er háð magni birgðalæsingar sem vísar til einnar eða fleiri gæðapantana. Ef samtala gæðapöntunarmagns fer umfram tilvísað magn birgðalæsingar, ákvarðar pöntunin sem gæðapantanirnar eru staðfestar í stofnun gæðapöntunarvinnu.

## <a name="canceling-quality-item-sampling-work"></a>Hætt við gæðavinnu vörusýnatöku

Hægt er að hætta við vinnuna sem stofnuð er fyrir gæðavinnu vörusýnatöku. Til að stjórna því hvað gerist þegar hætt er við þessa vinnu skal fylgja þessum skrefum.

1. Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.
1. Í flipanum **Almennt**, í flýtiflipanum **Vinna** skal stilla valkostinn **Afskrá innhreyfingu þegar verk er afturkallað** á eitt af eftirfarandi gildum:

    - **Já** - Þegar hætt er við gæðavinnu vörusýnatöku er tengdri gæðapöntun eytt og birgðirnar afskráðar.
    - **Nei** - Þegar hætt er við gæðavinnu vörusýnatöku er tengdri gæðapöntun ekki eytt og birgðirnar ekki afskráðar.

## <a name="cross-docking"></a>Dreifing frá dreifingarstöð

Hægt er að vera með uppsetningu gæðatengingar sem stofnar vinnu vörusýnatöku. En þegar dreifing frá dreifingarstöð er til staðar samhliða gæðatengingu sem stofnar gæðavinnu vörusýnatöku, ef aðeins er nóg magn til að fullnægja dreifingu frá dreifingarstöð, er aðeins vinna vörusýnatöku stofnuð. Í tilfellum þar sem valkosturinn **Virkja gæðapöntun fyrir vöruhúsaferli** er stilltur á _Já_ fyrir vöruhús móttöku og reiturinn **Viðeigandi gerð vöruhúss** er stilltur á _Gæðastjórnun fyrir vöruhúsaferli eingöngu_ fyrir gæðatengingu, gengur stofnun gæðavinnu vörusýnatöku fyrir á kostnað stofnunar dreifingarvinnu frá dreifingarstöð. Ef magnið fer yfir kröfu fyrir dreifingu frá dreifingarstöð býr kerfið samt til vinnu vörusýnatöku eingöngu.

## <a name="destructive-testing"></a>Eyðileggingarprófun

Hægt er að skilgreina prófunarflokk sem framkvæmir eyðileggingarprófun. Ef um er að ræða eyðileggingarpróf er gert ráð fyrir því, óháð niðurstöðu prófunar, að magn vörunnar sem prófað er verði eyðilagt sem hluti af prófinu. Hvernig eiginleikinn _Gæðastjórnun fyrir vöruhúsaferli_ styður eyðileggingarprófun líkist því hvernig gæðastjórnun styður hana þegar ekki er kveikt á eiginleikanum. Áður en hægt er að staðfesta gæðapöntunina verður gæðastjórinn að tilgreina tiltektarstaðsetningu sem hefur verið eyðilögð. Hægt er að skrá tiltekt á síðu gæðapöntunar með því að velja **Birgðir \> Taka til** á aðgerðasvæðinu. Eftir að tiltekt gæðapöntunarmagns er skráð er hægt að ljúka staðfestingu.

## <a name="example-scenario"></a>Dæmi

### <a name="prepare-the-scenario"></a>Virkja aðstæðurnar?

Til að fara í gegnum þessa atburðarás verður þú að undirbúa kerfið þitt á eftirfarandi hátt:

- Ganga skal úr skugga um að sýnigögnin séu uppsett í kerfinu og velja lögaðilann **USMF**.
- Kveiktu á eiginleikanum _Gæðastjórnun fyrir vöruhúsaferli_ í [gæðastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Grunnstilla vöruhús 51 til að nota eiginleikann _Gæðastjórnun fyrir vöruhúsaferli_ með því að fylgja þessum skrefum:

    1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Vöruhús**.
    1. Velja vöruhús 51.
    1. Í flýtiflipanum **Vöruhús** skal stilla valkostinn **Virkja gæðapöntun fyrir vöruhúsaferli** á *Já*.

### <a name="quality-in-setup--move-to-the-quality-control-location"></a>Gæðauppsetning - Flytja til staðsetningar gæðastjórnunar

Nú þarf að undirbúa grunnuppsetningu sem gerir kerfinu kleift að styðja eiginleikann _Gæðastjórnun fyrir vöruhúsaferli_ fyrir vöruhús 51. (Sýnigögnin skilgreina staðsetningu gæðastjórnunar sem kallast *QMS*. Vísað er í þessa staðsetningu nokkrum sinnum í þessari atburðarás.) Þú þarft að undirbúa eftirfarandi þætti eins og lýst er í undirköflum í þessum hluta:

- Vinnuklasi
- Vinnusniðmát
- Staðsetningarleiðbeiningar
- Vörusýnishorn
- Gæðatenging
- Valmyndaratriði fartækis

#### <a name="work-class-for-quality-in"></a>Vinnuklasi fyrir gæðaskoðun

1. Fara í **Vöruhúsastjórnun \> Uppsetning \> Vinna \> Vinnuklasar**.
1. Búðu til vinnuflokk og stilltu eftirfarandi gildi:

    - **Auðkenni vinnuklasa:** _QualityIn_
    - **Lýsing:** _Vörusýnataka gæðaskoðunar_
    - **Verkbeiðnigerð:** _Vörusýnataka gæðaskoðunar_

#### <a name="work-template"></a>Vinnusniðmát

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.
1. Stilltu reitinn **Verkbeiðnigerð** á _Vörusýnataka gæðaskoðunar_.
1. Búðu til vinnusniðmát og stilltu eftirfarandi gildi:

    - **Vinnusniðmát:** _Gæðaskoðun 51_
    - **Lýsing á vinnusniðmáti:** _51 Gæði_

1. Bættu línu við vinnusniðmátið og stilltu eftirfarandi gildi:

    - **Tegund vinnu:** _Tínsla_
    - **Auðkenni vinnuklasa:** _QualityIn_

1. Bættu annarri línu við vinnusniðmátið og stilltu eftirfarandi gildi:

    - **Tegund vinnu:** _Frágangur_
    - **Auðkenni vinnuklasa:** _QualityIn_

#### <a name="location-directive"></a>Staðsetningarleiðbeiningar

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.
1. Stilltu reitinn **Verkbeiðnigerð** á _Vörusýnataka gæðaskoðunar_.
1. Búðu til staðsetningarleiðbeiningu og stilltu eftirfarandi gildi:

    - **Heiti:** _51 til gæðaskoðunar_
    - **Tegund vinnu:** _Frágangur_
    - **Svæði:** 5
    - **Vöruhús:** _51_

1. Bættu við línu fyrir staðsetningarleiðbeininguna og stilltu eftirfarandi gildi:

    - **Frá-magn:** _1_
    - **Til magn:** _1000000_

1. Búðu til aðgerð staðsetningarleiðbeiningar og stilltu eftirfarandi gildi:

    - **Heiti:** _Gæði_

1. Fyrir nýju aðgerð staðsetningarleiðbeiningar skal velja **Breyta fyrirspurn** og tilgreina færslu **Bil** sem er með eftirfarandi gildi:

    - **Tafla:** *Staðir*
    - **Reitur:** _Auðkenni forstillingar staðsetningar_
    - **Skilyrði:** *QMS*

1. Velja skal **Í lagi** til að vista fyrirspurnina og vista nýju staðsetningarleiðbeininguna.

Næst þarf að breyta röðinni á fyrirliggjandi staðsetningarleiðbeiningum innkaupapöntunar fyrir vöruhús 51. Sýnigögnin fela í sér tvær staðsetningarleiðbeiningar sem eru með gildið **Verkbeiðnigerð** fyrir _Innkaup_: ein heitir _51 QMS_ og hin heitir _51 PO Direct_. Til að tryggja að eiginleikinn *Gæðastjórnun fyrir vöruhúsaferli* sé notaður fyrir vöruhús 51 þarf að ganga úr skugga um að staðsetningarleiðbeiningin _51 QMS_ sé ekki notuð. Í stað þess að eyða þeirri staðsetningarleiðbeiningu (því að kannski viltu nota hana seinna) er einfaldlega hægt breyta röðinni.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.
1. Í reitnum **Gerð verkbeiðni** velurðu _Innkaupapöntun_.
1. Í listanum skal velja númeraröð 5 fyrir staðsetningarleiðbeininguna _51 PO Direct_.
1. Færðu valda númeraröð upp í númeraröð 4.
1. Staðfestu að númeraröð fyrir staðsetningarleiðbeiningu _51 QMS_ sé nú a.m.k. 5.

#### <a name="item-sampling"></a>Vörusýnishorn

Eiginleikinn _Gæðastjórnun fyrir vöruhúsaferli_ bætir við nokkrum nýjum möguleikum fyrir vörusýnatöku. Gildið **Umfang sýnatöku** getur nú verið _Pöntun_, _Sending_ eða _Hleðsla_ og gildið **Magn sýnishorna** getur nú verið _Full númeraplata_.

1. Farið í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Vörusýnishorn**.
1. Búðu til færslu vörusýnatöku og stilltu eftirfarandi gildi:

    - **Rakning vörusýnatöku:** _3rd LP_
    - **Lýsing:** _Þriðja hver númeraplata_
    - **Umfang sýnatöku:** _Pöntun_

1. Í flýtiflipanum **Magn sýnishorna** skal stilla reitinn **Tilgreint magn** á _Full númeraplata_.
1. Í flýtiflipanum **Úrvinnsla** skal stilla reitinn **Fyrir hverja n númeraplötu** á _3_.
1. Í hlutanum **Á geymsluvídd** skal virkja bæði **Vöruhús** og **Birgðastaða**.

#### <a name="quality-associations"></a>Gæðatengingar

Búðu til gæðatengingu sem notar nýju vörusýnatökuna.

1. Fara í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Gæðatengingar**.
1. Búðu til færslu gæðatengingar og stilltu eftirfarandi gildi:

    - **Tilvísunargerð:** _Kaup_
    - **Vörukóði:** _Tafla_
    - **Vara:** _M9201_
    - **Svæði:** _5_

1. Í flýtiflipanum **Úrvinnsla** skal stilla reitinn **Tilviksgerð** á *Skráning*.
1. Í flýtiflipanum **Skilyrði** skal stilla reitinn **Viðeigandi gerð vöruhúss** á *Gæðastjórnun fyrir vöruhúsaferli eingöngu*.
1. Í flýtiflipanum **Ferli gæðapöntunar** skal stilla reitinn **Regla gæðaferlis** á _Stofna gæðapöntun_.
1. Í flýtiflipanum **Verklýsingar** skal hægrismella á reitinn **Prófunarflokkur** og síðan velja **Skoða upplýsingar** til að opna síðuna **Prófunarflokkar**.
1. Á síðunni **Prófunarflokkar**, í flipanum **Yfirlit** í efra hnitanetinu, skal stofna prófunarflokk og stilla eftirfarandi gildi:

    - **Prófunarflokkur:** _QMS_
    - **Lýsing:** _QMS próf_
    - **Viðunandi magn:** _100_
    - **Vörusýnataka:** _Þriðja LP_ (Velja)

1. Í flipanum **Yfirlit** í neðra hnitanetinu skal bæta við færslu fyrir eitt próf og stilla eftirfarandi gildi:

    - **Röð:** *1*
    - **Próf:** *Mæling í lokuðu rými*

1. Í flipanum **Próf** í neðra hnitanetinu skal stilla eftirfarandi gildi:

    - **Prófunarbreytur:** *Samþykkt/hafnað*
    - **Sjálfgefin útkoma:** *Staðist*

1. Vistaðu nýja prófunarflokkinn og lokaðu síðunni **Prófunarflokkar**.
1. Á síðunni **Gæðatengingar**, í reitnum **Prófunarflokkur**, skal velja **QMS**.
1. Vistaðu færsluna.

#### <a name="mobile-device-menu-items-for-quality-in"></a>Valmyndaratriði fartækis

Til að ljúka uppsetningunni til að flytja vörur á staðsetningu gæðastjórnunar þarf að gera gæðavinnu vörusýnatöku tiltæka úr valmyndaratriði fartækis.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Veljið **Frágangur innkaupapöntunar** valmyndaratriði fartækis.
1. Í flýtiflipanum **Vinnuklasar** skal bæta við vinnuklasakenninu *QualityIn*.

#### <a name="summary-your-setup-to-move-goods-to-quality-control"></a>Samantekt: Uppsetningin þín til að flytja vörur til gæðastjórnunar

Þú hefur skilgreint gæðatengingu sem notar eiginleikann *Gæðastjórnun fyrir vöruhúsaferli* til að setja af stað stofnun gæðapöntunar. Þú hefur sett upp vinnu- og staðsetningargögn fyrir vöruhús 51 til að tryggja að ákveðið verk verði stofnað þegar innkaupaskráning er gerð fyrir vöru M9201. Þessi uppsetning tryggir að þriðja hver númeraplata sem er skráð verði flutt til gæðastaðsetningar (_QMS_) og að gæðapöntun verði stofnuð fyrir magn númeraplötunnar. Allt annað verður fært í frágang í stað staðsetningar gæðastjórnunar.

### <a name="process-quality-management-work"></a>Verk gæðastjórnunarferlis

1. Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Búðu til innkaupapöntun og stilltu eftirfarandi gildi:

    - **Tilgreindur lánardrottnareikningur:** *104*
    - **Vöruhús:** *51*

1. Bæta við innkaupapöntunarlína:

    - **Vara:** *M9201*
    - **Magn:** *20*
    - **UoM:** *ea*
    - **Vöruhús:** *51*

1. Skrifaðu niður númer innkaupapöntunar svo þú getir notað það seinna.
1. Farðu í fartæki eða hermi sem keyrir farsímaforrit vöruhúsakerfis og skráðu þig inn í vöruhús 51 með því að nota *51* sem notandakenni og *1* sem aðgangsorð.
1. Farðu í **Á innleið \> Móttaka innkaupa** og sláðu inn eftirfarandi gildi:

    - **PONum:** Númer innkaupapöntunarinnar sem var stofnuð
    - **Magn:** *5*
    - **Prófhópur:** *ea*

1. Haltu áfram að taka á móti fyrir línuna, *5 ea* í einu, þar til línan er móttekin að fullu. (Alls verða fjórar númeraplötur búnar til.)
1. Skrá út úr farsímaforrit vöruhúsakerfis.
1. Í vefþjóninum skal fara í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Finndu og opnaðu innkaupapöntunina.
1. Í hlutanum **Innkaupapöntunarlínur** skal velja línuna fyrir vörunúmerið *M9201* og síðan velja **Innkaupapöntunarlínur \> Upplýsingar um verk**.
1. Taktu eftir að annar og þriðji verkhausinn sem voru stofnaðir, eru hefðbundin frágangsvinna, en fyrsti og fjórði verkhausinn eru gæðavinna vörusýnatöku. Þessi niðurstaða er í samræmi við uppsetningu vörusýnatöku sem er skilgreind til að safna þriðju hverri númeraplötu.

#### <a name="move-to-the-quality-control-location"></a>Færðu á gæðastjórnunarstaðinn

Nú færir þú númeraplöturnar yfir á tilgreindar staðsetningar. Fyrsta og fjórða númeraplatan fer á staðsetningu gæðastjórnunar, en önnur og þriðja númeraplatan fer beint í geymslu.

1. Farðu í fartæki eða hermi sem keyrir farsímaforrit vöruhúsakerfis og skráðu þig inn í vöruhús 51 með því að nota *51* sem notandakenni og *1* sem aðgangsorð.
1. Farðu í **Á innleið \> Frágangur innkaupa** og gakktu frá hverri númeraplötu úr fyrra ferli þar til þú hefur lokað öllu verkinu.

#### <a name="summary-process-quality-management-work"></a>Samantekt: Vinna úr verki gæðastjórnunar

Nú hefurðu keyrt gæðavinnu vörusýnatöku fyrir fyrstu og fjórðu númeraplötuna með því að færa þær yfir á staðsetningu gæðastjórnunar. Þú hefur líka gengið frá annarri og þriðju númeraplötunni. Næsta skref er að framkvæma prófun og stýringu gæðapöntunar.

### <a name="quality-out-setup-move-from-the-quality-control-location-to-storage-or-return"></a>Uppsetning gæðaskoðunar: Færa frá staðsetningu gæðastjórnunar til geymslu eða skila

Þegar starfsmenn tilkynna niðurstöður gæðapöntunar býr kerfið sjálfkrafa til verk.

Nú heldurðu áfram með nauðsynlega grunnuppsetningu vinnuklasa, vinnusniðmáts og staðsetningarleiðbeiningar til að virkja gæðastjórnun fyrir vöruhúsaferli svo hægt sé að stofna nauðsynlega vinnu til að færa magn gæðapöntunar frá staðsetningu gæðastjórnunar til tilgreindrar staðsetningar vöruhúss.

#### <a name="work-class-for-quality-out"></a>Vinnuklasi fyrir gæðaskoðun á útleið

1. Fara í **Vöruhúsastjórnun \> Uppsetning \> Vinna \> Vinnuklasar**.
1. Búðu til vinnuflokk og stilltu eftirfarandi gildi:

    - **Auðkenni vinnuklasa:** *QualityOut*
    - **Lýsing:** *Gæðaskoðun á útleið*
    - **Gerð verkpöntunar:** *Gæðapöntun*

#### <a name="work-templates"></a>Vinnusniðmát

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.
1. Breyttu gildinu **Verkbeiðnigerð** í *Gæðapöntun*.
1. Búðu til vinnusniðmát og stilltu eftirfarandi gildi:

    - **Vinnusniðmát:** *51 gæðaskoðun á útleið*
    - **Lýsing á vinnusniðmáti:** *51 gæðaskoðun á útleið*

1. Stofnið línu og stillið eftirfarandi svæði.

    - **Verkgerð:** *Tiltekt*
    - **Auðkenni vinnuklasa:** **QualityOut**

1. Bættu við annarri línu og stilltu eftirfarandi gildi:

    - **Tegund vinnu:** *Frágangur*
    - **Auðkenni vinnuklasa:** *QualityOut*

#### <a name="location-directives"></a>Staðsetningarleiðbeiningar

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.
1. Breyttu gildinu **Verkbeiðnigerð** í *Gæðapöntun*.
1. Búðu til staðsetningarleiðbeiningu og stilltu eftirfarandi gildi:

    - **Heiti:** *51 Staðið*
    - **Tegund vinnu:** *Frágangur*
    - **Svæði:** *5*
    - **Vöruhús:** *51*

1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn** til að opna glugga fyrirspurnarritils.
1. Á flipanum **Leysari** skal stilla eftirfarandi gildi:

    - **Tafla:** *Gæðapantanir*
    - **Reitur:** *Staða*
    - **Skilyrði:** *Staðist*

1. Veldu **Í lagi** til að vista fyrirspurnina og lokaðu glugganum.
1. Í flýtiflipanum **Línur** skal bæta við línu og stilla eftirfarandi gildi:

    - **Frá-magn:** *1*
    - **Til magn:** *1000000*

1. Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal bæta við línu og stilla eftirfarandi gildi:

    - **Heiti:** *Staðið*

1. Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Breyta fyrirspurn** til að opna glugga fyrirspurnarritils.
1. Á flipanum **Leysari** skal stilla eftirfarandi gildi:

    - **Tafla:** *Staðir*
    - **Reitur::** *Auðkenni svæðis*
    - **Skilyrði** *Fjöldi*

1. Veldu **Í lagi** til að vista fyrirspurnina og lokaðu glugganum.
1. Á aðgerðasvæðinu skal velja **Vista** til að vista nýju staðsetningarleiðbeininguna.
1. Búðu til aðra staðsetningarleiðbeiningu og stilltu eftirfarandi gildi:

    - **Heiti:** *51 fallið*
    - **Tegund vinnu:** *Frágangur*
    - **Svæði:** *5*
    - **Vöruhús:** *51*

1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn** til að opna glugga fyrirspurnarritils.
1. Á flipanum **Leysari** skal stilla eftirfarandi gildi:

    - **Tafla:** *Gæðapantanir*
    - **Reitur:** *Staða*
    - **Skilyrði** *Mistókst*

1. Veldu **Í lagi** til að vista fyrirspurnina og lokaðu glugganum.
1. Í flýtiflipanum **Línur** skal bæta við línu og stilla eftirfarandi gildi:

    - **Frá-magn:** *1*
    - **Til magn:** *1000000*

1. Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal bæta við línu og stilla eftirfarandi gildi:

    - **Heiti:** *Fallið*

1. Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Breyta fyrirspurn** til að opna glugga fyrirspurnarritils.
1. Á flipanum **Leysari** skal stilla eftirfarandi gildi:

    - **Tafla:** *Staðir*
    - **Reitur::** *Auðkenni svæðis*
    - **Skilyrði:** *Skil*

1. Veldu **Í lagi** til að vista fyrirspurnina og lokaðu glugganum.
1. Á aðgerðasvæðinu skal velja **Vista** til að vista nýju staðsetningarleiðbeininguna.

#### <a name="mobile-device-menu-items-for-quality-out"></a>Valmyndaratriði fartækis

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Veljið **QMS frágangur** valmyndaratriði fartækis.
1. Í flýtiflipanum **Vinnuklasar** skal bæta við vinnuklasakenninu *QualityPut*.

Starfsmenn í vöruhúsi geta nú tekið til gæðapöntunarverk með því að nota valmyndaratriðið **QMS frágangur**. Vörur sem stóðust ekki gæðaskoðun er hægt að koma fyrir í skilastaðsetningu og vörur sem stóðust skoðun er hægt að setja í staðsetningu bulk-001.

#### <a name="summary-your-setup-to-move-goods-from-quality-control"></a>Samantekt: Uppsetningin þín til að flytja vörur frá gæðastjórnun

Þú hefur sett upp vinnu- og staðsetningargögn fyrir vöruhús 51 til að tryggja að vinna verði sjálfkrafa stofnuð þegar gæðapöntunum er lokið. Þessi uppsetning tryggir að hver gæðastjórnuð númeraplata er færð til annaðhvort magnstaðsetningu eða skilastaðsetningu.

### <a name="process-quality-management-work"></a>Verk gæðastjórnunarferlis

1. Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Gæðapantanir**.
1. Veldu fyrstu gæðapöntunina fyrir magnið sem var skráð.
1. Veldu **Staðfesta**. Staða prófunarinnar uppfærist í *Mistókst*.
1. Farðu í **Vöruhúsastjórnun \> Öll verk**.
1. Opnaðu verkið sem þú varst að búa til og taktu eftir að gildið **Verkbeiðnigerð** er *Gæðapöntun*. Verkið felur í sér línu þar sem frágangsstaðsetningin er *Skil* og staðan er *Fallið*. (Ef staða gæðapöntunarinnar væri *Staðið* yrði frágangsstaðsetningin *Magnstaðsetning* í staðinn.)
1. Farðu aftur í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Gæðapantanir**.
1. Veldu aðra gæðapöntunina fyrir vörurnar sem voru skráðar.
1. Veldu **Niðurstöður** fyrir ofan neðra hnitanetið. Uppfærðu gildið **Niðurstöðumagn** í *5* og staðfestu að gildið **Niðurstaða prófunar** sé breytt í gátmerki.
1. Veljið **Staðfesta** og lokið síðunni.
1. Aftur á síðunni **Gæðapantanir** skal velja **Staðfesta** og gera staðfestingu. Staða er uppfærð í *Staðist*.

    > [!NOTE]
    > Tilvik staðfestingar setur af stað stofnun gæðapöntunarverks til að færa magnið úr staðsetningu gæðastjórnunar til nýrrar staðsetningar.

1. Farðu í **Vöruhúsastjórnun \> Öll verk**.
1. Veldu verkið sem var nýlega stofnað og taktu eftir að annar verkhaus gæðapöntunar var búinn til þar sem frágangsstaðsetningin er *BULK-001*.
1. Farðu í fartæki eða hermi sem keyrir farsímaforrit vöruhúsakerfis og skráðu þig inn í vöruhús 51 með því að nota *51* sem notandakenni og *1* sem aðgangsorð.
1. Fara skal í **Gæðaskoðun \> Frágangur frá QMS** og vinna úr báðum númeraplötunum sem tengjast báðum verkunum þannig að allri vinnu er lokað.

> [!NOTE]
> Hugleiddu að bæta færslu gæðaskoðunar á útleið við valmyndaratriði fartækis þar sem virkjunarkóðinn er *Sýna opinn verkefnalisti*. Sjá til dæmis valmyndaratriði fartækis sem kallast **Verkefnalisti** í sýnigögnum. Bættu fyrst vinnuklasanum *Gæðapöntun* við notandamiðað valmyndaratriði því að þessi vinnuklasi nauðsynlegur til að vinna birtist í verkefnalistanum. Bættu síðan vinnuklasanum *Gæðapöntun* við valmyndaratriðið **Verkefnalisti**. Notendur sem hafa aðgang að verkefnalistanum geta þá tekið til og unnið úr verkinu sem er sjálfkrafa búið til af staðfestingu gæðapöntunar.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Stjórnunaryfirlit gæða og ósamkvæmni](quality-management-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]