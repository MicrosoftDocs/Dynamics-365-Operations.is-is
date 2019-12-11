---
title: Eiginleikaeining
description: Þetta efni fjallar um eiginleikaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785285"
---
# <a name="feature-module"></a>Eiginleikaeining 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni fjallar um eiginleikaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Eiginleikaeining er notuð til að markaðssetja vörur eða kynningar með blöndu af myndum og texta. Til dæmis getur smásali bætt eiginleikaeiningunni við upplýsingasíðu vöru til að varpa ljósi á eiginleika vörunnar.

Eiginleikaeining er knúin áfram af gögnum frá efnisstýringarkerfinu (CMS). Þetta er sjálfstæð eining sem er ekki háð öðrum einingum á síðunni. Hægt er að setja eiginleikaeiningar á hvaða síðu sem er þar sem smásali vill markaðssetja eða auglýsa eitthvað (til dæmis vörur, útsölu eða eiginleika).

## <a name="examples-of-feature-modules-in-e-commerce"></a>Dæmi um eiginleikaeiningar í rafrænum viðskiptum

Eiginleikaeiningu má nota á eftirfarandi síðum:

- Upplýsingar um vöru til að sýna fram á eiginleika vöru
- Heimasíðan, til að kynna vörur
- Flokkasíða, til að auðkenna vöruflokk

## <a name="feature-module-properties"></a>Eiginleikar eiginleikaeiningar

| Nafn eiginleika     | Gildi | Lýsing |
|-------------------|--------|-------------|
| Mynd             | Myndaskrá | Hægt er að nota mynd til að markaðssetja vöruna eða auglýsa. Hægt er að hlaða mynd inn í myndasafnið eða nota núverandi mynd. |
| Fyrirsögn           | Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Sérhver eiginleikaeining getur haft fyrirsögn. Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina. Hins vegar er hægt að breyta merkinu til að uppfylla kröfur um aðgengi. |
| Efnisgrein         | Texti efnisgreinar | Eiginleikaeiningar styðja málsgreinatexta með ríku textasniði. Stuðningur er við nokkra grunntextaeiginleika, eins og feitletrun, undirstrikun og skáletrun texta og tengla. Sumum af þessum eiginleikum er hægt að hnekkja með síðuþema sem er beitt á eininguna. |
| Tengill              | Tenglatexti, vefslóð tengils, ARIA-merki (Accessible Rich Internet Applications) og **Opnaðu hlekk í nýjum flipa** | Eiginleikaeiningar styðja einn eða fleiri „kalla til aðgerða“ tengla. Ef tengli er bætt við þarf tenglatexta, vefslóð og ARIA-merki. ARIA-merki ættu að vera lýsandi til að uppfylla kröfur um aðgengi. Hægt er að stilla tengla þannig að þeir séu opnaðir á nýjum flipa. |
| Staðsetning myndar   | **Hægri**, **Vinstri**, **Efst** eða **Neðst** | Þessi eiginleiki skilgreinir staðsetningu myndarinnar miðað við textann. Til dæmis, ef **hægri** er valið birtist myndin hægra megin við textann. |
| Dálkstærð myndar | Gildi frá **1** til og með **12** | Þessi eiginleiki skilgreinir stærð myndarinnar miðað við textann. Stærð er gefin upp sem fjöldi dálka á síðunni. Það eru 12 dálkar á síðunni. Sjálfgefið er að myndin og textinn hafi sömu stærð (sex dálkar hver). Hins vegar er hægt að breyta stærðinni eftir þörfum. |

## <a name="add-a-feature-module-to-a-new-page"></a>Bæta eiginleikaeiningu við nýja síðu 

Fylgdu þessum skrefum til að bæta eiginleikaeiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Farðu í **Sniðmát** og búðu til síðusniðmát sem heitir **eiginleikasniðmát**.
1. Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við eiginleikaeiningu.
1. Skráðu brotið út í sniðmátinu og birtu það.
1. Notaðu eiginleikasniðmátið sem þú bjóst til til að búa til síðu sem heitir **eiginleikasíða**.
1. Í hólfinu **Aðal** á sjálfgefnu síðunni velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.
1. Í vlmyndinni **Bæta við einingu** undir **Velja einingar** velurðu eiginleikaeiningu og velur síðan **Í lagi**.
1. Veldu eiginleikaeininguna í útlínutrénu til vinstri.
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

[Hetjueining](add-hero-module.md)

[Myndspilaraeining](add-video-player.md)
