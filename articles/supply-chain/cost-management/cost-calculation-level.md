---
title: Kostnaðarútreikningsstig
description: Þetta efnisatriði útskýrir uppskriftarstig sem heitir kostnaðarútreikningsstig. Þetta uppskriftarstig tekur ekki mið af framleiðslu og runupöntunum í útreikningum sínum.
author: AndersGirke
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 41f2550ff22b838aa5d85022582fd9715917fe462aa34dbfc833941f5ada3325
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717391"
---
# <a name="cost-calculation-level"></a>Kostnaðarútreikningsstig

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