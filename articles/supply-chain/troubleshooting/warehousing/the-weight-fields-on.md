---
title: Þyngdarreitirnir í farmlínum passa ekki við þyngdarreitina í farminum
description: Þyngdarreitirnir í farmlínum passa ekki við þyngdarreitina í farminum
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 639b82a9d46b74f179d6904d2c3b8e7dfb813b58
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924352"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a>Þyngdarreitirnir í farmlínum passa ekki við þyngdarreitina í farminum

Villukóðar: WHSLoadWeightOnLinesDoNotMatchLoadWarning

## <a name="symptoms"></a>Einkenni

Kerfið sýnir eftirfarandi villuboð:

> Þyngdarreitirnir í hleðslulínum stemma ekki við þyngdarreitina í hleðslu %1. Keyra samræmisathugun hleðsluþyngdar vöruhúss til að endurreikna þyngdarreiti.

## <a name="cause"></a>Orsök

Reitirnir **Nettóþyngd** og **Töruþyngd** eru stilltir á *0* (núll) í hleðslulínunni. Þyngdarreitir eru þó ekki stilltir á *0* fyrir þyngdarmælingar á vörunni. Þegar þyngdarreitir eru ekki stilltir í hleðslulínunni geta allar leiðréttingar á magninu á hleðslulínunni valdið röngum þyngdarútreikningi á hleðslunni. Þetta vandamál gæti komið upp ef þyngd vörunnar hefur verið breytt síðan hleðslulínan var stofnuð.

## <a name="resolution"></a>Upplausn

Sjálfgefið er að þegar hleðslulína er stofnuð eru þyngdarreitir vörunnar færðir inn á hana. Ef þyngdin er núll er hægt að endurreikna hana með virkninni *Samræmisathugun á hleðsluþyngd vöruhúss*.

1. Farið í **Kerfisstjórnun \> Reglubundin verkefni \> Gagnagrunnur \> Samræmisathugun**.
1. Í **Samræmisathugun** glugganum skal stilla **Eining** á *Vöruhúsastjórnun*.
1. Stillið reitinn **Athuga/Laga** á *Laga villu*.
1. Í lista yfir gátreiti skal velja gátreitinn **Samræmisathugun á hleðsluþyngd vöruhúss** og ganga úr skugga um að aðeins línan fyrir þennan gátreit sé auðkennd.
1. Efst á gátreitinum skal velja úrfellingarhnappinn (**...**) og velja svo **Svargluggi** á valmyndinni.
1. Veljið eftirtalda reiti í glugganum **Samræmisathugun á hleðsluþyngd vöruhúss** til að tilgreina viðmiðin sem samræmisathugun á að kanna:

    - **Hleðslukenni:** Tilgreindu hleðslukenni. Skiljið þetta eftir autt til að athuga öll kenni hleðslu.
    - **Vörunúmer:** Tilgreindu vörunúmer. Skildu þetta eftir autt til að athuga allar vörur.
    - **Alltaf endurreikna þyngd á hleðslum:** Stilltu þennan valkost á *Já*
    - **Leyfa að skrifa yfir þyngd á hleðslulínum:** Stillið þennan valkost á *Já*.

1. Velja skal **Í lagi** til að loka glugganum **Samræmisathugun á hleðsluþyngd vöruhúss**.
1. Veljið úrfellingarhnappinn og veljið **Keyra** í valmyndinni.

Þyngdin er endurreiknuð á grundvelli skilyrðanna sem tilgreind voru. Veljið tengilinn **Skilaboðaupplýsingar** til að skoða niðurstöður samræmiskoðunarinnar.
