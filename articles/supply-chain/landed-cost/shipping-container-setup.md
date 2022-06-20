---
title: Gámar
description: Þessi grein lýsir því hvernig á að setja upp sendingargáma fyrir kostnaðareininguna Landað.
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 345f815a4f85db30db18aba3f8a4d41835c2e3f2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860843"
---
# <a name="shipping-container-setup"></a>Uppsetning gáms

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir því hvernig á að setja upp sendingargáma fyrir **Landaður kostnaður** mát.

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a>Setja upp gámagerðir

Gámagerðir skilgreina gerðir gáma sem er hægt að nota í sendingum og ferðum.

Til að vinna með gámagerðirnar skal fara í **Heildarkostnaður \> Gámauppsetning \> Gámagerðir**. Þar er hægt að skoða, bæta við og fjarlægja færslur fyrir gámagerðirnar. Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.

| Svæði | lýsing |
|---|---|
| Gámagerð | Færið inn einkvæmt auðkennisheiti/númer fyrir gámagerðina. |
| lýsing | Færið inn lýsingu á gámagerðinni. |
| Magn | Sláið inn hámarksmagn sem leyft er í gámum af þessari gerð. |
| Vægi | Sláið inn hámarksþyngd sem leyfð er í gámum af þessari gerð. |
| Hægt að skila | Tilgreinið hvort hægt er að skila gámum af þessari gerð til lánardrottins þegar búið er að nota hann í ferð. Ef þessi valkostur er stilltur á *Já* gæti aukalegur kostnaður átt við um skil á gámum af þessari gerð til upprunalegrar hafnar. |

## <a name="set-up-shipping-containers"></a>Setja upp gáma

Gámafærslur eru notaðar til að bera kennsl á hvern gám sem notaður er í ferðum. Þegar ferð er stofnuð er hægt að velja tilgreindan gám fyrir hana í listanum yfir allar gámafærslur sem búið er að skilgreina hér. Þessi eiginleiki er mjög gagnlegur ef fyrirtækið á eigin gáma.

Ekki þarf að slá inn gámanúmerin fyrir gáma sem verða aðeins notaðir einu sinni. Í staðinn er hægt að bæta við gámanúmerinu þegar ferðin er stofnuð.

Gámafærslur eru aðeins notaðar í heildarkostnaði. Þær eru ekki í boði í staðlaðri **Flutningsstjórnun** einingu (TMS).

Til að vinna gáma skal fara í **Heildarkostnaður \> Gámauppsetning \> Gámar**. Þar er hægt að skoða, bæta við og fjarlægja færslur gámanna. Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.

| Svæði | lýsing |
|---|---|
| Gámur | Færið inn einkvæmt auðkennisheiti/númer fyrir gám. |
| Gámagerð | Velja gerð gáms. Fyrir frekari upplýsingar, sjá [Settu upp gerðir flutningsgáma](#shipping-container-types) kafla fyrr í þessari grein. |

> [!NOTE]
> - Uppsetning gáms er valfrjáls. Yfirleitt verður hún aðeins notuð ef fyrirtækið á eigin gáma eða notar oft sömu gámana.
> - Engar vartölur eru reiknaðar fyrir gámanúmer.

## <a name="set-up-unit-types"></a><a name="unit-types"></a>Setja upp einingagerðir

Einingagerðir setja á frekari flokkanir og auðkenningaraðferðir fyrir gáma. Einingagerðin er yfirleitt notuð til að auðkenna gerð gámsins sem vörum er pakkað í, t.d. bretti eða tunnur. Hægt er að velja einingagerð þegar gámur er settur upp á **Allir gámar** síðunni.

Einingargerðir eru aðeins notaðar í heildarkostnaði. Þetta er ekki í boði í TMS.

Til að vinna með einingargerðir skal fara í **Heildarkostnaður \> Gámauppsetning \> Einingagerðir**. Þar er hægt að skoða, bæta við og fjarlægja færslur fyrir einingagerðirnar. Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.

| Svæði | lýsing |
|---|---|
| Einingargerð | Færið inn einkvæmt auðkennisheiti/númer fyrir einingagerðina. |
| lýsing | Færa inn lýsingu á einingagerðinni. |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a>Setja upp kæligerðir

Kæligerðir setja á frekari flokkanir og auðkenningaraðferðir fyrir gáma (yfirleitt kæligáma). Hægt er að velja kæligerð þegar gámur er settur upp á síðunni **Allir gámar**.

Til að vinna með gerðir kælingar skal fara í **Heildarkostnaður \> Gámauppsetning \> Gerðir kælinga**. Þar er hægt að skoða, bæta við og fjarlægja færslur fyrir kæligerðirnar. Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.

| Svæði | lýsing |
|---|---|
| Gerð kælingar | Færið inn einkvæmt auðkennisheiti/númer fyrir kæligerðina. |
| lýsing | Færið inn lýsingu á kæligerðinni. |
