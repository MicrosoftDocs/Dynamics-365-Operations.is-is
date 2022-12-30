---
title: Setja upp tæki til að keyra viðmót fyrir framkvæmd á framleiðslugólfi
description: Keyrsluviðmót framleiðslugólfsins er sett upp fyrir sérhvert tæki á framleiðslugólfinu. Fyrirtæki setja venjulega upp hvert tæki á sinn hátt, fer allt eftir því hvaða tilgangi tækið þjónar. Til dæmis gæti fyrirtæki verið með eitt tæki á móttökusvæðinu, þar sem starfsmenn stimpla sig inn og út og annað í vinnusal, þar sem starfsmenn hafa umsjón með störfum sínum.
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution, HcmWorker, JmgProductionFloorExecutionDeviceConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0ae9ca901a7af8275db419e25a7297a77aab284e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857403"
---
# <a name="set-up-a-device-to-run-the-production-floor-execution-interface"></a>Setja upp tæki til að keyra viðmót fyrir framkvæmd á framleiðslugólfi

[!include [banner](../includes/banner.md)]

Keyrsluviðmót framleiðslugólfsins er sett upp fyrir sérhvert tæki á framleiðslugólfinu. Fyrirtæki setja venjulega upp hvert tæki á sinn hátt, fer allt eftir því hvaða tilgangi tækið þjónar. Til dæmis gæti fyrirtæki verið með eitt tæki á móttökusvæðinu, þar sem starfsmenn stimpla sig inn og út og annað í vinnusal, þar sem starfsmenn hafa umsjón með störfum sínum.

## <a name="set-the-configuration-and-filters-for-a-specific-device"></a>Stilla skilgreiningu og síur fyrir tiltekið tæki

Til að stilla skilgreiningu og vinnusíur fyrir tæki þarf að skrá sig inn á síðuna **Keyrsla framleiðslugólfs** með því að nota reikning sem er með öryggishlutverk sem inniheldur aðgangsheimildina *Vinna með tímastjórnun*. (Á meðal tilbúnu öryggishlutverkanna, þá hefur aðeins *Umsjónarmaður vinnusalar* þessa aðgangsheimild.) Síðan skal fylgja þessum skrefum.

1. Farið í tækið sem á að setja upp og skráið ykkur inn í Microsoft Dynamics 365 Supply Chain Management sem umsjónarmaður vinnusalar. Notið reikning sem inniheldur aðgangsheimildina *Vinna með tímastjórnun*.
1. Ganga skal úr skugga um að skilgreining sé tiltæk fyrir tækið sem verið er að setja upp. Ef engin skilgreining er þegar til er sjálfgefin skilgreining gefin upp. Frekari upplýsingar um hvernig setja á upp skilgreiningu er að finna í [Skilgreina keyrsluviðmót framleiðslugólfs](production-floor-execution-configure.md).
1. Farið í **Framleiðslustýring \> Framkvæmd framleiðslu \> Framkvæmd á framleiðslugólfi**.

    Ef keyrsluviðmót framleiðslugólfsins hefur þegar verið skilgreint að minnsta kosti einu sinni á núverandi tæki, þá birtist innskráningarsíða. Annars birtist kynningarsíða.

1. Á innskráningarsíðunni er kynningarsíðunni skal velja **Skilgreina**.
1. Veljið skilgreiningu á listanum.
1. Veljið **Næst**.
1. Veljið eina eða fleiri síur sem nota á í núgildandi tæki. Þessar síur hjálpa til við að tryggja að aðeins viðeigandi verk séu sýnd í tækinu. Til að stilla síu skal velja síugerðina til að opna lista yfir gildi og síðan velja gildið sem á að sía. Eftirfarandi síur eru í boði:

    - **Framleiðslueining** - Þessi sía er sía á hæsta stigi. Hún á yfirleitt við um stórt vinnusvæði sem er með nokkra tilfangaflokka og stök tilföng á því.
    - **Tilfangaflokkur** - Þessi sía er sía á miðstigi. Hún á yfirleitt við safn tengdar tilfanga á afmörkuðu svæði á vinnusvæðinu. Ef sían **Framleiðslueining** er valin fyrst, sýnir listinn yfir tilfangaflokka aðeins flokka úr þeirri einingu. Að öðrum kosti sýnir hún alla tiltæka tilfangaflokka.
    - **Tilfang** - Þessi sía er sértækasta sían. Hún á yfirleitt við tiltekna vél eða annað stakt tilfang. Ef sían **Tilfangaflokkur** og/eða **Framleiðslueining** er valin fyrst, sýnir listinn yfir tilföng aðeins tilföng úr þeim flokki og/eða einingu. Að öðrum kosti sýnir hún öll tiltæk tilföng.

1. Veljið **Í lagi**.
1. Innskráningarsíðan birtist og tækið er tilbúið til notkunar.

## <a name="allow-a-worker-to-override-the-default-filters"></a>Leyfa starfsmanni að hnekkja sjálfgefnu síunum

Hægt er að veita tilteknum starfsmönnum heimild til að breyta síustillingum á því tæki sem þeir nota. Fyrir starfsmenn sem hafa þessa heimild, býður keyrsluviðmót framleiðslugólfs upp á hnappinn **Sía** á síðunum **Allar vinnslur** og **Virk vinnsla**.

> [!NOTE]
> Ef starfsmaður breytir síu gildir nýja sían frá þeim tímapunkti fyrir alla notendur sem skrá sig inn í tækið.

Til að leyfa starfsmanni að hnekkja sjálfgefnum vinnslusíum sem hafa verið settar upp fyrir tæki skal fylgja þessum skrefum.

1. Farið í **Tími og viðvera \> Uppsetning \> Starfskraftar sem sinna tímaskráningu**.
1. Veljið starfsmann úr listanum til að opna síðuna **Starfsmenn tímaskráningar** fyrir þann starfsmann.
1. Í flipanum **Tímaskráning** skal stilla valkostinn **Stilla síur** á *Já*.

## <a name="run-the-interface-in-full-screen-mode"></a>Keyra viðmótið í heilskjásstillingu

Oft er keyrsluviðmót framleiðslugólfs keyrt á tæki sem er notað eingöngu í þeim tilgangi. Þess vegna gæti verið skynsamlegt að keyra viðmótið í heilskjásstillingu án þess að sýna yfirlit og/eða chrome-vafrann.

- Til að fela yfirlitssvæðið sem er sýnt í Supply Chain Management skal bæta eftirfarandi texta við lok vefslóðar í veffangastiku vafrans: `\&limitednav=true`.
- Til að fela einnig veffangastiku vefrans skal nota heilskjásstillingu vafrans. (Til að fá leiðbeiningar skal skoða fylgigögn vafrans.)

Efri hluti eftirfarandi myndar sýnir hvernig viðmótið lítur út að sjálfgefnu. Neðri hlutinn sýnir hvernig það lítur út á öllum skjánum þegar yfirlitssvæðið er falið.

![Hefðbundið viðmót í samanburði við heilan skjá.](media/pfei-full-screen.png "Hefðbundið viðmót í samanburði við heilan skjá")

## <a name="extend-the-session-past-12-hours"></a>Lengja lotuna fram yfir 12 klukkustundir

Að sjálfgefnu mun keyrsluviðmót framleiðslugólfs sjálfkrafa skrá sig út ef enginn notar það í 12 klukkustundir. Notandi Supply Chain Management verður þá að skrá sig inn aftur. Hins vegar er hægt að lengja tímamörkin upp í allt að 90 daga.

Til að lengja tímamörkin skal skrá sig inn í Supply Chain Management og fara í **Kerfisstjórnun \> Notendur \> Lengingar á lotu**. Tilgreinið notandareikning Supply Chain Management sem er notaður til að skrá sig inn í tækið og fjölda klukkustunda sem lotan á að vera virk í.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
