---
title: Uppsetning sendingarupplýsinga
description: Þessi grein lýsir því hvernig á að setja upp sendingarupplýsingar fyrir kostnaðareininguna Landað.
author: Weijiesa
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 62277f66a36817e83b4c0bf101aa7b6cc14ecccb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882635"
---
# <a name="shipping-information-setup"></a>Uppsetning sendingarupplýsinga

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir því hvernig á að setja upp sendingarupplýsingar fyrir **Landaður kostnaður** mát.

## <a name="description-of-goods"></a><a name="description-of-goods"></a>Lýsing á vörum

Vörulýsing hjálpar til við að auðkenna ferð, gám eða fólíó og vörurnar í þeim. Hægt er að velja lýsingu á vörum í haus gámsins eða fólíósins.

Til að vinna með lýsingar á vörum skal fara í **Heildarkostnaður \> Uppsetning sendingarupplýsinga \> Lýsing á vörum**. Þar er hægt að skoða, opna, stofna og eyða færslum fyrir lýsingar á vörum. Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.

| Svæði | lýsing |
|---|---|
| Lýsing á vörum | Færið inn einkvæmt auðkennisheiti/númer fyrir gerð varanna sem notar þessa lýsingu. |
| lýsing | Færið inn lýsingu á gerð varanna í þessum flokki. |

## <a name="vessels"></a><a name="vessels"></a>Skip

Skip er einkvæmt heiti á skipi sem flutningsfyrirtæki eða umboðsaðili notar. Þegar ferð er stofnuð þarf alltaf að annaðhvort velja eða færa inn skip hennar. Ef sama skipið er oft notað er hægt að flýta fyrir og auðvelda stofnun nýrrar ferðar með því að stofna færslu skips fyrir hverja þeirra og gera notendum þar með kleift að velja skipið úr lista frekar en að færa inn heiti eða númer handvirkt í hvert skipti.

Til að vinna með skip skal fara í **Heildarkostnaður \> Uppsetning sendingarupplýsinga \> Skip**. Þar er hægt að skoða, opna, stofna og eyða færslum fyrir skip. Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.

| Svæði | lýsing |
|---|---|
| Skip | Færið inn einkvæmt auðkennisheiti/númer fyrir skipið sem verður notað til að flytja vörur í ferð. |
| lýsing | Færðu inn lýsingu á skipinu. Yfirleitt kemur fram í þessari lýsingu heiti skipsins og flutningsfyrirtækisins/umboðsaðilans. |
| Afhendingarmáti | Veljið afhendingarmáta sem skipið notar (t.d. _Flug_, _Haf_ eða _Lest_). |

## <a name="exporters"></a>Útflutningsaðilar

Hver færsla útflutningsaðila tilgreinir lánardrottin eða útflutningsaðila sem hægt er að skilgreina sem lánardrottin ferðar. Hægt er að tengja útflutningsaðilann við ferð og nota hann í skýrslugerð.

Til að vinna með útflutningsaðila skal fara í **Heildarkostnaður \> Uppsetning sendingarupplýsinga \> Útflutningsaðilar**. Þar er hægt að skoða, opna, stofna og eyða færslum fyrir útflutningsaðila. Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.

| Svæði | lýsing |
|---|---|
| Útflutningsaðili | Færið inn einkvæmt auðkennisheiti/númer fyrir útflutningsaðila á vörum sem eru fluttar í ferð. |
| lýsing | Færðu inn lýsingu á útflytjanda. Yfirleitt auðkennir þessi lýsing fullt heiti flutningsfyrirtækisins/-aðilans. |

## <a name="commodity-codes"></a>Grunnvörukóðar

Vörukóðar eru notaðir til að aðstoða við auðkenningu tolla og útreikning innflutningsgjalda fyrir vörur í ferð. Hægt er að velja vörukóða á Síða **Útgefinna afurða**.

Til að vinna með vörukóða skal opna **Heildarkostnaður \> Uppsetning sendingarupplýsinga \> Vörukóðar**. Þar er hægt að skoða, opna, stofna og eyða færslum fyrir vörukóða. Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.

| Svæði | lýsing |
|---|---|
| Grunnvörukóði | Færið inn einkvæman kóða fyrir þessa gerð vöru. |
| lýsing | Færið inn lýsingu á vörutegundinni. |

## <a name="customs-description"></a>Lýsing tolls

Lýsing á tolli auðveldar að auðkenna vörur vegna tolla. Hægt er að velja tollalýsingu á síðunni **útgefnar afurðir** eða í innkaupapöntunarlínum.

Til að vinna með tolllýsingar skal fara í **Heildarkostnaður \> Uppsetning sendingarupplýsinga \> Lýsing tolls**. Þar er hægt að skoða, opna, stofna og eyða færslum fyrir sérstakar lýsingar. Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.

| Svæði | lýsing |
|---|---|
| Lýsing tolls | Færið inn einkvæman kóða fyrir þessa gerð tollflokkunar. Oft verður þessi kóði opinber lýsing sem er gefin út af tollayfirvöldum fyrir lýsingu og eigindleg gildi varanna. |
| lýsing | Færið inn lýsingu á tollaflokkun. |
