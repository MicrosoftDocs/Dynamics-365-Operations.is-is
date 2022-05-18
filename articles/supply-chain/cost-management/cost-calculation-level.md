---
title: Kostnaðarútreikningsstig
description: Þetta efnisatriði útskýrir uppskriftarstig sem heitir kostnaðarútreikningsstig. Þetta uppskriftarstig tekur ekki mið af framleiðslu og runupöntunum í útreikningum sínum.
author: JennySong-SH
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 563d866c93e9205914f633f3435ef4b46f85b814
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679556"
---
# <a name="cost-calculation-level"></a>Kostnaðarútreikningsstig

[!include [banner](../includes/banner.md)]

Uppskriftarstigið sem heitir **Kostnaðarútreikningsstig** tekur ekki mið af framleiðslupöntunum og runupöntunum í útreikningum sínum. Kerfið notar þetta stig þegar kostnaðarútreikningar eru keyrðir í kostnaðarútgáfum. Í úrvinnslum á borð við endurútreikningum og birgðalokunum notar kerfið uppskriftarstigið **Kostnaðarútreikningsstig** í staðinn.

Eftirfarandi einföld atburðarás sýnir muninn milli uppskriftarstiganna **Kostnaðarútreikningsstig** og **Kostnaðarstig**.

Þú ert með þrjár afurðir: A, B og C. Afurð C er hluti af afurð B, og afurð B er hluti af afurð A.

- **Kostnaðarstig** úthlutar eftirfarandi uppskriftarstigum:

    - **Vara A:** 0
    - **Afurð B:** 1
    - **Afurð C:** 2

- **Kostnaðarútreikningsstig** úthlutar eftirfarandi uppskriftarstigum:

    - **Vara A:** 0
    - **Afurð B:** 1
    - **Afurð C:** 2

Framleiðslupöntun fyrir afurð C er þá stofnuð og afurð A er bætt við uppskrift framleiðslupöntunar. Eftir að pöntun er áætluð eru uppskriftarstig uppfærð á eftirfarandi hátt:

- **Kostnaðarstig** úthlutar eftirfarandi uppskriftarstigum:

    - **Afurð B:** 1
    - **Afurð C:** 2
    - **Vara A:** 3

- **Kostnaðarútreikningsstig** úthlutar eftirfarandi uppskriftarstigum:

    - **Vara A:** 0
    - **Afurð B:** 1
    - **Afurð C:** 2

Þessi hegðun tryggir að breytingar á uppskriftum framleiðslupantana hafa ekki áhrif á væntanlega kostnaðarútreikninga.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]