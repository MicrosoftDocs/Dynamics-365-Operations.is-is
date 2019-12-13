---
title: Hetjueining
description: Þetta efni fjallar um hetjueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785393"
---
# <a name="hero-module"></a>Hetjueining

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni fjallar um hetjueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Hetjueining er notuð til að markaðssetja vörur eða kynningar með blöndu af myndum og texta. Til dæmis getur smásali bætt hetjueiningu á heimasíðu svæðis fyrir rafræn viðskipti til að kynna nýja vöru og vekja athygli viðskiptavina.

Hetjueining er knúin áfram af gögnum frá efnisstýringarkerfinu (CMS). Þetta er sjálfstæð eining sem er ekki háð öðrum einingum á síðunni. Hægt er að setja hetjueiningar á hvaða síðu sem er þar sem smásali vill markaðssetja eða auglýsa eitthvað (til dæmis vörur, útsölu eða eiginleika).

## <a name="examples-of-hero-module-in-e-commerce"></a>Dæmi um hetjueiningu í rafrænum viðskiptum

- Hægt er að nota hetjueiningu á heimasíðu svæðis fyrir rafræn viðskipti til að varpa ljósi á kynningar og nýjar vörur.
- Hægt er að nota hetjueiningu á upplýsingasíðu vöru til að sýna upplýsingar um vöru.
- Hægt er að setja margar hetjueiningar í myndaræmueiningu til að varpa ljósi á margar vörur eða kynningar.

## <a name="hero-module-properties"></a>Eiginleikar hetjueiningar

| Nafn eiginleika  | Gildi | Lýsing |
|----------------|--------|-------------|
| Mynd          | Myndaskrá | Hægt er að nota mynd til að sýna vöruna eða auglýsa. Hægt er að hlaða mynd inn í myndasafnið eða nota núverandi mynd. |
| Fyrirsögn        | Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Sérhver hetjueining getur haft fyrirsögn. Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina. Hins vegar er hægt að breyta merkinu til að uppfylla kröfur um aðgengi. |
| Efnisgrein      | Texti efnisgreinar | Hetjueiningar styðja málsgreinatexta með ríku textasniði. Stuðningur er við nokkra grunntextaeiginleika, eins og feitletrun, undirstrikun og skáletrun texta og tengla. Sumum af þessum eiginleikum er hægt að hnekkja með síðuþema sem er beitt á eininguna. |
| Tengill           | Tenglatexti, vefslóð tengils, ARIA-merki (Accessible Rich Internet Applications) og **Opnaðu hlekk í nýjum flipa** | Hetjueiningar styðja einn eða fleiri „kalla til aðgerða“ tengla. Ef tengli er bætt við þarf tenglatexta, vefslóð og ARIA-merki. ARIA-merki ættu að vera lýsandi til að uppfylla kröfur um aðgengi. Hægt er að stilla tengla þannig að þeir séu opnaðir á nýjum flipa. |
| Staðsetning texta | **Efst til vinstri**, **Efst til hægri**, **Efsta fyrir miðju**, **Neðst til vinstri**, **Neðst til hægri**, **Neðst fyrir miðju**, **Miðja vinstri**, **Miðja hægri** eða **Miðja fyrir miðju** | Þessi eiginleiki skilgreinir staðsetningu myndarinnar miðað við textann. Til dæmis, ef **hægri** er valið birtist myndin hægra megin við textann. |
| Aðalefni texta     | **Ljóst** eða **Dökkt** | Hægt er að skilgreina litasamsetningu fyrir textann, byggt á bakgrunnsmyndinni. Til dæmis, ef myndin er með dökkan bakgrunn, er hægt að beita léttu þema til að gera textann sýnilegri og til að mæta andstæða litastigshlutfalla í aðgengisskyni. |
| Stigull       | **Satt** eða **Ósatt** | Hægt er að beita stigul á myndina til að uppfylla litaréttarhlutföll í aðgengisskyni. |

## <a name="add-a-hero-module-to-a-new-page"></a>Bæta hetjueiningu við nýja síðu

Fylgdu þessum skrefum til að bæta hetjueiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Farðu í **Sniðmát** og búðu til síðusniðmát sem heitir **hetjusniðmát**.
1. Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við hetjueiningu.
1. Skráðu brotið út í sniðmátinu og birtu það.
1. Notaðu hetjusniðmátið sem þú bjóst til að búa til síðu sem heitir **hetjusíða**.
1. Í hólfinu **Aðal** á sjálfgefnu síðunni velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.
1. Í valmyndinni **Bæta við einingu** undir **Velja einingar** velurðu hetjueiningu og velur síðan **Í lagi**.
1. Veldu hetjueininguna í útlínutrénu til vinstri.
1. Í eiginleikaglugganum til hægri velurðu **Bæta við mynd**. Veldu þá annaðhvort núverandi mynd eða hladdu upp nýrri mynd.
1. Veldu **Fyrirsögn**.
1. Í valmyndinni **Fyrirsögn** bætirðu við fyrirsagnartexta, velur hausstig og velur síðan **Í lagi**.
1. Undir **Sniðinn texti** bætirðu við texta eftir þörfum.
1. Veldu **Bæta við aðgerðartengli**.
1. Í valmyndinni **Aðgerðartengill** bætirðu við texta, slóð og ARIA-merki fyrir tengilinn og velur síðan **Í lagi**.
1. Vistaðu síðuna og forskoðaðu breytingarnar.
1. Athuga á síðunni og birtu hana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Viðvörunareining](add-alert.md)

[Myndaræmueining](add-carousel.md)

[Eining með fjölbreyttu efni](add-content-rich-block.md)

[Staðsetningareining efnis](add-content-placement-modules.md)

[Eiginleikaeining](add-feature-module.md)

[Myndspilaraeining](add-video-player.md)
