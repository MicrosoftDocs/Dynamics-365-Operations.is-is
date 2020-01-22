---
title: Staða skjala og líftíma
description: Þetta efni fjallar um hinar ýmsu skjalastöður blaðsíðuþátta í Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: edb81efc45fc5e7eed32cb7d9b8fda5ade987dd4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914888"
---
# <a name="document-states-and-lifecycle"></a>Staða skjala og líftíma

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni fjallar um hinar ýmsu skjalastöður blaðsíðuþátta í Microsoft Dynamics 365 Commerce.

## <a name="document-state-descriptions"></a>Lýsing skjalastöðu

Efnið [Síðueiningar](page-elements-overview.md) er með lista yfir ýmsar gerðir skjala í efnisstjórnunarkerfinu (CMS). Þessar skjalategundir geta haft nokkrar stöður í höfundatólinu. Skjalastöðurnar hjálpa til við að koma í veg fyrir árekstur gagna og framfylgja útgáfustjórnun. Þær ákvarða hverjir geta breytt skjölunum, hvenær hægt er að breyta skjölunum og hvenær aðrir geta skoðað breytingar.

Eftirfarandi tafla sýnir mögulegar skjalastöður síðueininga í Commerce.

| Staða skjals | Lýsing |
|---|---|
| Skráði sig út | Þegar CMS hlutur er skráður út til þín geta aðrir staðfestir kerfisnotendur ekki breytt honum. Allar breytingar sem þú gerir á hlutnum eru aðeins sýnilegar þér. |
| Skráð inn | Þegar CMS hlutur er innritaður eru allar breytingar sýnilegar öðrum staðfestum kerfisnotendum og þessir notendur geta síðan skoðað hlutinn og breytt honum. Hver innskráning býr til útgáfu skjals í sögu hlutarins. |
| Útgefið | Þegar CMS hlutur er gefinn út er honum ýtt á heimasíðuna þína og hægt verður að uppgötva hann á internetinu af utanaðkomandi notendum. Aðeins er hægt að birta hluti ef þeir hafa verið skráðir inn. |
| Vistuð | Hægt er að vista breytingar sem gerðar hafa verið á afrituðum CMS hlut á CMS áður en hluturinn er skráður inn eða birtur. Þessar vistuðu breytingar eru ekki sýnilegar öðrum staðfestum kerfisnotendum fyrr en hluturinn er skráður inn. Þær eru ekki sýnilegir fyrir utanaðkomandi notendur fyrr en hluturinn er birtur. |
| Fargað við útskráningu | Þegar útskráðri CMS-vöru er fargað er öllum vistuðum breytingum eytt og varan snýr aftur í þá útgáfu sem síðast var skráð inn. |

## <a name="additional-resources"></a>Frekari upplýsingar

[Leiðir til að bæta við efni](add-manage-content.md)

[Orðalisti síðulíkans](page-elements-overview.md)

[Unnið með birta hópa](publish-groups.md)

[Vinna með einingar](work-with-modules.md)

[Vinna með brot](work-with-fragments.md)

[Yfirlit yfir sniðmát og útlit](templates-layouts-overview.md)

[Sérstilla yfirlit svæðis](customize-site-navigation.md)
