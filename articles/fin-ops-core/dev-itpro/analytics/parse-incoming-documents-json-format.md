---
title: Þátta skjöl á innleið á JSON-sniði
description: Þetta efni skýrir hvernig á að setja upp rafræn skýrslugerðarsnið (ER) til að þátta skjöl á innleið í JavaScript Object Notation (JSON)-sniði.
author: kfend
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b4ed81bb5527ea8e02caaa1262a57960dd7cdf29
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685764"
---
# <a name="parse-incoming-documents-in-json-format"></a>Þátta skjöl á innleið á JSON-sniði

[!include[banner](../includes/banner.md)]

Hægt er að setja upp rafræn skýrslugerðarsnið (ER) til að þátta komandi rafræn skjöl sem tákna gögn á textasniði sem byggist á JavaScript (með öðrum orðum, skrár í JavaScript Object Notation \[JSON\]-sniði).

Til að læra meira um þennan eiginleika skaltu hlaða niður skrám í eftirfarandi töflu og spila síðan ER Stofna sniðmátsskilgreiningu til að flytja inn gögn úr utanaðkomandi JSON-skráarleiðbeiningar. Þetta verkefni fylgja sýnir hvernig hægt er að nota ER snið til að flokka innkominn JSON-skrá til að uppfæra forritsgögn.

| Titill                                  | Skrárnafn |
|----------------------------------------|-----------|
| ER Sníða skilgreiningu                | [Snið fyrir innflutning trans_JSON.xml lánardrottins](https://go.microsoft.com/fwlink/?linkid=874111) |
| Sýni af móttekinni skrá á .csv-sniði | [1099entries_JSON.txt](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a>Þarfir

Áður en þú klárar ER Stofna sniðstillingu til að flytja inn gögn úr utanaðkomandi JSON-skráarleiðbeiningum, verður að uppfylla eftirfarandi krafa:

- Yfireiningar í JSON-skránni geta aðeins verið hlutaeiningar.
- Faldaðar einingar fyrir hlut eiga að vera eiginleikaeiningar, svo að gilt JSON-skipulag sé búið til.
- JSON-fylki geta aðeins verið faldaðar einingar í eiginleikaeiningum hlutar.
- JSON-fylki geta aðeins innihaldið JSON-hluti. Þau geta ekki innihaldið bein strengja-/tölugildi og faldaðar fylkingar. Einingar í þessum fylkjum verða þáttaðar í röð, eins og þær eru tilgreindar í forminu. Tekið verður tillit til margfeldisstillinga á hvern JSON-hlut.

Að auki verður þú að ljúka verkleiðbeiningunum [ER Stofna nauðsynlegar skilgreiningar til að flytja inn gögn úr utanaðkomandi skrá](tasks/er-required-configurations-import-data.md) ef þú hefur ekki þegar lokið þeim. Sæktu eftirfarandi skrá til að ljúka verkefnaleiðbeiningunni.

| Titill                  | Skrárnafn |
|------------------------|-----------|
| Líkanaskilgreining rafrænnar skýrslugerðar | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=874111) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]