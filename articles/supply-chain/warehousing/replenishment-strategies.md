---
title: Áfyllingaráætlanir
description: Þetta efnisatriði veitir upplýsingar um áfyllingaráætlanir og útskýrir hvernig hægt er að nota svæðið áfyllingaráætlun í sniðmátslínum eftirspurnaráfyllingar bylgju til að velja hvernig áfyllingu er háttað.
author: mirzaab
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-29
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: d6baffd6ea6107c7f8f81a553f518e4298406899a1cbf35f5d6cdb74063bd1f9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734044"
---
# <a name="replenishment-strategies"></a>Áfyllingaráætlanir

[!include [banner](../includes/banner.md)]

Sniðmátin sem eru skilgreind á síðunni **Áfyllingarsniðmát** innihalda sniðmátslínur eftirspurnaráfyllingar bylgju sem gera þér kleift að velja hvernig áfyllingu er háttað. Hver lína inniheldur nú svæðið **Áfyllingaráætlun**.

Áætlunin *Eftirspurnarmagn bylgju* er sjálfgefna áætlunin. Þetta er áfyllingaráætlunin sem var notuð áður en svæðið **Áfyllingaráætlun** var kynnt til sögunnar. Svæðið notar staðsetningarleiðbeiningar áfyllingar til að finna staðsetningar sem hægt er að fylla á. Það fyllir svo á staðsetninguna þar til eftirspurn er náð.

Áætlunin *Hámarksafkastageta staðsetningar* kynnir nýja virkni til sögunnar. Eins og í áætluninni *Eftirspurnarmagn bylgju* notar þessi áætlun staðsetningarleiðbeiningar áfyllingar til að finna staðsetningar sem hægt er að fylla á og síðan er fyllt á viðkomandi staðsetningar þar til eftirspurn er náð. Hún er ólík áætluninni *Eftirspurnarmagn bylgju* að því leyti að allar áfylltar staðsetningar eru áfylltar að hámarkgetu eins og skilgreint er í birgðamörkum staðsetningarinnar. Áætlunin *Hámarksafkastageta staðsetningar* reynir að stofna vinnu til að færa inn umbeðið magn, auk tiltekins magns til viðbótar til að fylla staðsetningarnar sem verið er að fylla á. Slík tilraun gæti mistekist í sumum tilvikum. Til dæmis er hugsanlegt að biðstaðsetningar hafi ekki nægar birgðir fyrir aukamagninu. Í slíkum tilvikum greinir kerfið bilunina og gerir tilraun til endurheimtar.

Háannatími er eitt dæmi um aðstæður þar sem áætlunin *Hámarksafkastageta staðsetningar* er ákjósanlegri en áætlunin *Eftirspurnarmagn bylgju*. Á háannatíma er hugsanlegt að sumar vörur séu vinsælar. Þar af leiðandi er gagnlegt að fylla á viðeigandi tiltektarstaðsetningar fyrirfram eins og kostur er til að draga úr fjölda vinnukenna sem eru stofnuð fyrir áfyllingu.

> [!IMPORTANT]
> Til að nýta afkastagetu áætlunarinnar *Hámarksafkastageta staðsetningar* verður að endurskilgreina birgðamörk fyrir viðeigandi staðsetningar. Að öðru leyti virkar þessi áætlun á sama hátt og áætlunin *Eftirspurnarmagn bylgju*.

## <a name="turn-on-the-replenish-to-max-based-on-stocking-limits-feature"></a>Kveikið á Áfylling að hámarki samkvæmt eiginleikum birgðamarka

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Þar er eiginleikinn sýndur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Áfylling að hámarki samkvæmt birgðamörkum*

## <a name="set-up-replenishment-strategies"></a>Setja upp áætlanir áfyllingar

Til að opna sniðmátin skal fara í **Vöruhúsakerfi \> Uppsetningu \> Áfylling \> Áfyllingarsniðmát**. Í hlutanum **Yfirlit** skaltu velja eða stofna eftirspurnaráfyllingu bylgju þar sem svæðið **Gerð áfyllingar** er stillt á *Eftirspurn bylgju*. Síðan skal setja upp áfyllingarsniðmátslínur í hlutanum **Upplýsingar um áfyllingarsniðmát**. Fyrir hverja línu á svæðinu **Áfyllingaráætlun** skal velja áfyllingaráætlun sem ætlunin er að nota.

![Sniðmátssíða áfyllingar.](media/ReplenTempWaveDmdMaxLocCap.png "Sniðmátsíða áfyllingar")

Þegar dálkurinn **áfyllingaráætlunar** birtist ekki í hnitanetinu í hlutanum **Upplýsingar um áfyllingarsniðmát** verður að ganga úr skugga um að kveikt hafi verið á eiginleikanum og gerð áfyllingar á völdu áfyllingarsniðmáti sé *Eftirspurn bylgju*.

> [!NOTE]
> Áætlunin *Eftirspurnarmagn bylgju* er sjálfgefna áætlunin. Þar af leiðandi þarftu einungis að uppfæra áfyllingarsniðmátslínur þar sem nota á áætlunina *Hámarksafkastageta staðsetningar*.

## <a name="example-scenarios"></a>Dæmi um aðstæður

### <a name="example-1"></a>Dæmi 1

Í þessu dæmi er aðeins eitt áfyllingarsniðmát sem inniheldur aðeins eina línu fyrir áfyllingarsniðmát.

Þú stofnar sölupöntun fyrir 130 stykki af vöru A0001. Áður en pöntunin er losunin í vöruhúsið er vöruhúsið sett upp á eftirfarandi hátt:

- Aðeins ein biðstaðsetning er til staðar og er með 500 stk tiltæk í birgðum á lager.
- Þrjár tiltektarstaðsetningar eru til staðar og birgðamörk hverrar þeirra er 100 stk. (Hafa skal í huga að birgðamörk eru áskilin fyrir áætlunina *Hámarksafkastageta staðsetningar*.)
- Frágangsstaðsetningar áfyllingar eru hinar sömu og staðsetningar sölutiltektar.
- Áfyllingareiningin er box (1 box = 20 stk.).

Þegar pöntun er á pöntuninni eru eftirfarandi birgðir á lager á staðsetningum sölutiltektar:

- **Tiltekt-001:** 20 stk (1 box)
- **Tiltekt-002:** 0 stk
- **Tiltekt-003:** 0 stk

Upphaflega er áfyllingaráætlun stillt á *Eftirspurnarmagn bylgju*.

Þegar búið er að losa sölupöntunina í vöruhúsið, og bylgjuvinnsla er keyrð fyrir bylgjuna er hægt að sækja eftirfarandi áfyllingarvinnu:

- **Áfyllingarvinna 1:** Taka til 4 box á biðstaðsetningu og setja þau í tiltekt staðsetningar-001.
- **Áfyllingarvinna 2:** Taka til 2 box á biðstaðsetningu og setja þau í tiltekt staðsetningar-002.

Þú færð tvö vinnukenni áfyllingarvinnu því fylla verður á tvær staðsetningar og margskiptar áfyllingar eru ekki studdar.

Ef áfyllingaráætlun er stillt á *Hámarksafkastageta staðsetningar* í staðinn kemur upp eftirfarandi áfyllingarvinna:

- **Áfyllingarvinna 1:** Taka til 4 box á biðstaðsetningu og setja þau í tiltekt staðsetningar-001.
- **Áfyllingarvinna 2:** Taka til 5 box á biðstaðsetningu og setja þau í tiltekt staðsetningar-002.

[![Dæmi 1.](media/ReplenTemp_example_1.png "Dæmi 1")](media/ReplenTemp_example_1_large.png)

### <a name="example-2"></a>Dæmi 2

Þetta dæmi sýnir hvað gerist þegar biðstaðsetning er ekki með nógu margar birgðir til að ná yfir aukamagn. Það notar sömu atburðarás og dæmi 1, en biðstaðsetning er með 160 stk (8 box).

Áætlunin *Eftirspurnarmagn bylgju* stofnar sömu vinnu og gert var í dæmi 1.

Hins vegar, vegna þess að áætlunin *Hámarksafkastageta staðsetningar* reynir að búa til vinnukenni sem það gerði í dæmi 1, kann það að mistakast. Á þeim tímapunkti gerir kerfið tilraun til endurheimtar.

Miðað við stillingu valkostarins **Leyfa** á staðsetningarleiðbeiningum fyrir tiltekt áfyllingar koma tvær niðurstöður til greina:

- Þegar valkosturinn **Leyfa að skipta** er stilltur á *Já* er eftirfarandi áfyllingarvinna stofnuð:

    - **Áfyllingarvinna 1:** Taka til 4 box á biðstaðsetningu og setja þau í tiltekt staðsetningar-001.
    - **Áfyllingarvinna 2:** Taka til 4 box á biðstaðsetningu og setja þau í tiltekt staðsetningar-002.

- Þegar valkosturinn **Leyfa að skipta** er stilltur á *Nei* er eftirfarandi áfyllingarvinna stofnuð:

    - **Áfyllingarvinna 1:** Taka til 4 box á biðstaðsetningu og setja þau í tiltekt staðsetningar-001.
    - **Áfyllingarvinna 2:** Taka til 2 box á biðstaðsetningu og setja þau í tiltekt staðsetningar-002.

Niðurstöðurnar eru ólíkar miðað við tiltækar upplýsingar þegar vinnan er stofnuð. Þegar **Leyfa að skipta** er stillt á *Já* á staðsetningarleiðbeiningum fyrir tiltekt áfyllingar, færðu að vita að þú fannst 160 stk. Þess vegna er hægt að stofna vinnu fyrir það magn. Hins vegar, þegar valkosturinn **Leyfa** er stilltur á *Nei* getur þú ekki vitað um að 160 stk eru til staðar. Vegna þess að aukamagnið sem ákveðið var að fylla á voru 3 box er hægt að sleppa þessu aukamagni og reyna upprunalega magnið að nýju.

[![Dæmi 2.](media/ReplenTemp_example_2.png "Dæmi 2")](media/ReplenTemp_example_2_large.png)

Þar af leiðandi til að fá hámarksmagn á áfyllingarstaðsetningar, skal stilla valkostinn **Leyfa að skipta** á *Já* á staðsetningarleiðbeiningum fyrir áfyllingu tiltektar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]