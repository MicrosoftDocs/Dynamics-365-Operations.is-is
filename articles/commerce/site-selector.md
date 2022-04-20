---
title: Vefsíðuvalseining
description: Þetta efni fjallar um síðuvalseininguna og lýsir því hvernig á að bæta henni við síðusíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: ad4d4d5f950d0631059d8f509e9e808a9106eb98
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551695"
---
# <a name="site-picker-module"></a>Vefsíðuvalseining

[!include [banner](includes/banner.md)]

Þetta efni fjallar um síðuvalseininguna og lýsir því hvernig á að bæta henni við síðusíður í Microsoft Dynamics 365 Commerce.

Þegar fyrirtæki er með ólík svæði á mörkuðum, svæði og staðhætti þurfa notendur svæðis að skipta á milli svæða og velja æskilegt verslunarsvæði á einfaldan hátt. Til að mæta þessari atburðarás gerir vefvalseiningin notendum kleift að vafra um margar síður. Einnig er mælt með vefsíðuvali þegar [landfræðileg uppgötvun og tilvísun](geo-detection-redirection.md) hafa verið innleiddar fyrir netverslunarsíðuna þína, svo að viðskiptavinir hafi leið til að hnekkja síðuvalinu sem þeir gefa til kynna með því að nota [land/svæðavals](country-region-picker-module.md) mát. 

Vefvalareiningin verður að vera stillt með lista yfir vefsvæði (markaðir, svæði eða staðsetningar) sem notendur vefsvæðisins geta skoðað. Eftirfarandi mynd sýnir dæmi um síðuvalseiningu sem er í haus síðusíðu.

![Dæmi um síðuvalseiningu í haus síðusíðu.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Eiginleikar vefvalseiningar

| Heiti eiginleika | Gildi                 | Lýsing |
|---------------|-----------------------|-------------|
| Yfirskrift       | Texti                  | Fyrirsögn einingarinnar. |
| Vefsvæðakostir  | Nafn, mynd, URL      | Þessi eiginleiki tilgreinir heiti, tengil á heimasíðu svæðisins og valfrjálsa mynd til að sýna fyrir hvert svæði sem er tekið með í einingunni. Myndin getur verið flagg eða einhver framsetning á markaði, svæði eða staðháttum. |

## <a name="add-a-site-picker-module-to-a-page"></a>Bættu síðuvalareiningu við síðu

Hægt er að bæta síðuvalseiningunni við **Vefsvæði velja** rifa á [hausareining](author-header-module.md). Eftir að síðuvalareiningu hefur verið bætt við geturðu skilgreint einingarfyrirsögnina og síðuvalkosti. Yfirleitt er hauseining innifalin í hausbroti sem hægt er að deila á netviðskiptasíður fyrir síðu. Í eftirfarandi dæmi hefur vefvalseiningunni verið bætt við **Vefsvæði velja** rauf á hauseiningu sem er að finna í hausbroti sem er nefnt **Header Container**.

![Dæmi um síðuvalseiningu í hausbroti.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Eining síðuhauss](author-header-module.md)

[Brauðmylsnueining](add-breadcrumb.md)

[Eining yfirlitsvalmyndar](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
