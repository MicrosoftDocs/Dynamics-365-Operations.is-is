---
title: Útreikningar afbrigðalíkans afurðar
description: Þetta efnisatriði lýsir því hvernig á að stofna útreikninga fyrir einingar í afbrigðalíkani afurðar
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f0806a5b36b04e77a5a6d10f3c2eb3d7ba680e75
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356417"
---
# <a name="product-configuration-model-calculations"></a>Útreikningar afbrigðalíkans afurðar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að stofna útreikninga fyrir einingar í afbrigðalíkani afurðar.

## <a name="prerequisites"></a>Forkröfur

Útreikningarnir eru notaðir í afbrigðalíkani afurðar til að reikna út grunnstillingargildi fyrir vöru. Áður en hægt er að setja upp útreikninga verður tengt afbrigðalíkan vörunnar að vera til staðar. Fyrir yfirlit yfir uppsetningarferlið fyrir afbrigðalíkön og tengd verk skal skoða [Setja upp afbrigðalíkan afurðar](set-up-maintain-product-configuration-model.md).

## <a name="create-a-calculation"></a>Stofna útreikning

Útreikningur samanstendur af segð og markmiðseigind. Frekari upplýsingar eru í [Algengar spurningar um afbrigðalíkan afurðar](calculate-product-configuration-models.md).

Fylgið þessum skrefum til að búa til útreikning fyrir fyrirliggjandi vörulíkan.

1. Farið í **Upplýsingastjórnun afurða \> Almennt \> Afbrigðalíkan afurðar**.
1. Opnið afbrigðalíkan afurðar og smellið síðan á **Breyta**.
1. Í flýtiflipanum **Útreikningar** skal velja **Bæta við** til að bæta við útreikningi og stillið síðan eftirfarandi reiti:

    - **Heiti** – Færið inn heiti fyrir útreikninginn.
    - **Lýsing** – Færið inn lýsingu á útreikningnum.
    - **Markeigind** – Select the attribute that you're making the calculation for.

1. Veljið **Breyta segð**.
1. Í svarglugganum **Færa inn útreikning** skal bæta nauðsynlegum eiginleikum, virkjum og gildum við segðina. Frekari upplýsingar um það hvernig vinna á með þessar einingar má finna í [Segðarskorður og töfluskorður í afbrigðalíkönum afurðar](expression-constraints-table-constraints-product-configuration-models.md).
1. Þegar segðin er tilbúin skal velja **Í lagi**.

## <a name="calculation-examples"></a>Dæmi um útreikning

Í þessum hluta eru nokkur dæmi sem sýna hvernig útreikningar virka.

### <a name="example-1"></a>Dæmi 1

Markeigindin er Boole-gildi og útreikningurinn notar eftirfarandi skilyrta segð:

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

Þessi segð skilar gildinu *Rétt* á markmiðseigindina ef `decimalAttribute2` er hærra en eða jafnt og `decimalAttribute1`. Að öðrum kosti skilar hún Boolean *Rangt*.

### <a name="example-2"></a>Dæmi 2

Þetta dæmi notar textaeigindina `textFixedList` sem markeigind. Þessi eigind inniheldur eftirfarandi fastan lista.

| Virði | Gildi leysara |
|---|---|
| A | 1a |
| V | 2b |
| K | 2c |

Eftirfarandi skjámynd sýnir hvernig stillingar fyrir þessa eigind gætu litið út í kerfinu þínu.

![Stillingar eigindargerðar fyrir dæmi 2.](media/model-calculations-example2.png "Stillingar eigindargerðar fyrir dæmi 2")

Eigindin er notuð í eftirfarandi skilyrtu yfirliti:

`If[integerAttribute < 150, 0, 2]`

Ef `integerAttribute` er minna en 150 skilar þetta yfirlit textagildi fyrstu færslunnar í fasta listanum, *A*. Annars skilar það textagildi þriðju færslunnar í fasta listanum, *C*.

> [!NOTE]
> Fasti listinn jafngildir núllgrunnsupptalningu (fasttexta) og gildi hans eru fengin með viðeigandi heiltölu. Þess vegna er fyrsta gildi fasta listans (*A*) samsvarað við *0*, annað gildið (*B*) er samsvarað við *1* og þriðja gildið (*C*) er samvarað við *2*.

### <a name="example-3"></a>Dæmi 3

Þetta dæmi notar `textFixedList` markeigindina úr fyrra dæminu. Það notar einnig aðra textaeigind, `textAttribute`, sem inniheldur eftirfarandi fastan lista.

| Virði | Gildi leysara |
|---|---|
| AA | 1aa |
| BB | 2bb |

Eftirfarandi skjámynd sýnir hvernig stillingar fyrir þessa eigind gætu litið út í kerfinu þínu.

![Stillingar eigindargerðar fyrir dæmi 3.](media/model-calculations-example3.png "Stillingar eigindargerðar fyrir dæmi 3")

Gildið fyrir `textFixedList` eigindina er reiknað með eftirfarandi skilyrtu yfirliti:

`If[textAttribute == "1aa", 0, 2]`

Ef `textAttribute` gildið er með leysigildi sem jafngildir *1aa*, skilar þessi segð textagildi fyrstu færslunnar í `textFixedList` fasta listanum, *A*. Annars skilað það textagildi þriðju færslunnar í `textFixedList` fasta listanum, *C*.

> [!NOTE]
> - Skilyrta yfirlitið verður að nota leysigildi eigindarinnar.
> - Aðeins er hægt að nota textaeigindir fasts lista í útreikningum.

## <a name="see-also"></a>Sjá einnig

- [Algengar spurningar um afbrigðalíkan afurðar](calculate-product-configuration-models.md)
- [Bæta skorðu á segð við afbrigðalíkan afurðar](tasks/add-expression-constraint-product-configuration-model.md)
- [Yfirlit afbrigðalíkön afurðar](product-configuration-models.md)
