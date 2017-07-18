---
title: "Skrá uppskriftir sem tilbúnar"
description: "Þessi grein veitir upplýsingar um skráningu uppskrifta sem tilbúnar."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMReportFinish, BOMReportFinishMax
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 53251
ms.assetid: 510d05a3-0073-438d-b0c4-b6a6df1882ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 26b5029068904d4af5849eab9135f50b3291f642
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017

---

# <a name="report-boms-as-finished"></a>Skrá uppskriftir sem tilbúnar

[!include[banner](../includes/banner.md)]


Þessi grein veitir upplýsingar um skráningu uppskrifta sem tilbúnar.

**Bóka sem tilbúið** og **Hám. bóka sem lokið** síður eru notaðar til að skrá uppskriftir (BOMs) sem lokið. Í raun er ferli til að tilkynna Uppskrift sem lokið er sú sama og ferli við tilkynna framleiðslupöntun sem lokið. Þetta ferli er hægt að nota í, til dæmis, einfalda samsetningu og ferli við að búa til sett þar sem ítarlegri getu framleiðslupantana er ekki krafist. Í **Bóka sem tilbúið** síðu gerir þér kleift að tilkynna margar Uppskriftir sem tilbúnar í runu. Í **Hám. þess sem má Bóka sem tilbúið** síðu gerir þér kleift að bóka einungis ein Uppskrift sem tilbúna í einu. Síðan **Bóka sem tilbúið** er tiltæk frá valmyndaratriði í birgðastjórnun og báðar síðurnar eru tiltækar sem valmyndaratriðunum á **Útgefnar afurðir**.

## <a name="report-as-finished-page"></a>Síðan Bóka sem tilbúið
Ef opnuð er **Bóka sem tilbúið** síðu úr útgefin afurð, stingur síðan uppá að þú tilkynninr staðlað sjálfgefið magn birgða sem lokið. Sjálfgefið er virka uppskriftaútgáfan sýnt, en hægt er að breyta uppskriftarútgáfuna séu til staðar öðrum samþykktum útgáfum. Síðan leyfir einnig að eyða færslum og stofna nýjar færslur fyrir útgefnar afurðir sem skráð ætti sem lokið. Til að Nota fyrirspurn til að velja afurðir, smellið á **Velja** valmyndaratriði. Handvirkt er hægt að staðfesta skráningu sem lokið fyrir valdar afurðir með því að smella **í lagi**. Einnig er hægt að setja upp ferlið til að keyra í runu. Þegar bóka sem tilbúið ferlið er staðfest, myndar kerfið uppskriftabók þar sem bókun í birgðir er unnin. Þessi færslubók samanstendur af eina línuvöru fyrir tilbúin afurð og línuvöru fyrir hverja uppskriftarlínu. Hægt er að stjórna hvort færslubókina er sjálfkrafa bókuð eða hvort hún er skilin eftir opin fyrir viðbótar leiðréttingar.

## <a name="max-report-as-finished-page"></a>Hám. síðan Bóka sem tilbúið
Á **Hám. þess sem bóka má tilbúið** síðu, hver uppskriftarlínu sýnir fjölda stykki af vöru sem hægt er að bóka sem tilbúið. Þessi útreikningur byggist á efnislegar tiltækar lagerbirgðir fyrir hverja efnislínu. Í eftirfarandi dæmi notar einu stykki af vörunúmerinu FG tvö stykki af hráefni RM10 og eitt stykki RM20 hráefni. Þar sem eru aðeins 10 stykki af RM10 á lager, er hámarksfjölda FG sem hægt er að bóka sem tilbúið fimm stykki. Þetta gildi er sýndur í á **Hám. sem bóka má sem tilbúið** svæði.

| Stig | Vörunúmer | Magn | Á lager | Hám. Bóka tilbúið |
|-------|-------------|----------|---------|-------------------------|
| 0     | FG          |  1       | 0       | 5                       |
| 1     | RM10        | -2       | 10      | 5                       |
| 1     | RM20        | -1       |  8      | 8                       |

## <a name="boms-that-have-multiple-levels"></a>Uppskriftir sem hafa mörg stig
Þegar Uppskrift hefur mörg stig, er hægt að stjórna hvernig gert er grein fyrir efni á öllum stigum með því að nota í **Niðurbrot** svæði. Þetta svæði er tiltækt bæði í **bóka sem tilbúið** síðu og **Hám. þess em bóka má sem tilbúið** síðu. Eftirtaldir valkostir eru í boði:

-   **Aldrei** – undirliggjandi uppskriftir eru ekki brotnar niður ef skortur er á efnum.
-   **Alltaf** – allar undirliggjandi uppskriftir eru brotnar niður að fullu. Þess vegna er hvers kyns lausar lagerbirgðir fyrir hálfkláraðar hlutur vöru ekki notaðar.
-   **Skortur** – undirliggjandi uppskriftir eru aðeins brotnar niður ef allt magn efnis sem óskað er eftir er ekki tiltækt.

### <a name="example"></a>Dæmi

Í þessu dæmi eru þrjár stykki tilbúinnar afurðar (vörunúmer FG) tilbúnar til að bóka sem lokið. Það er til staðar tveggja stiga Uppskrift, eins og sýnt er hér.

| Stig | Vörunúmer | Línumagn uppskriftar | Á lager |
|-------|-------------|-------------------|---------|
| 0     | FG          |                   |         |
| 1     | COMP        | 1                 | 2       |
| 1     | RM          | 1                 |         |

Eftirfarandi töflur sýna hvernig stilling **Niðurbrot** svæðis hefur áhrif á hvernig færslubókarlínur Uppskriftar eru myndaðar. **Niðurbrot: Aldrei**

| Stig | Vörunúmer | Magn |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | COMP        | - 3       |

Eins og fyrri taflan sýnir, telst aðeins vörunúmer COMP afdregið í færslubókinni. Vörunúmer RM, sem er hluti af COMP, er ekki brotið niður í færslubókarlínuna og tvö stykki á lager fyrir COMP eru ekki tekin til greina. **Niðurbrot: Alltaf**

| Stig | Vörunúmer | Magn |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | RM          | - 3       |

Í þessu tilfelli er vörunúmer COMP brotin niður í hennar hráefni, vörunúmer RM. Tvö stykki á lager fyrir COMP eru ekki tekin til greina fyrir magn af RM til að nota. **Niðurbrot: Skortur**

| Stig | Vörunúmer | Magn |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | COMP        | -2       |
| 1     | RM          | -1       |

Í þessu tilfelli eru tvö stykki á lager fyrir vörunúmer COMP tekin til greina. Hins vegar þar sem þörf er á þremur stykki af vörunúmer FG, er einu stykki af vörunúmer RM einnig nauðsynlegt til að búa til einu viðbótar stykki af COMP.




