---
title: Regulatory Configuration Service (RCS) – Eyða RCS-umhverfi
description: Þetta efnisatriði útskýrir hvernig kerfisstjóri Regulatory Configuration Service (RCS) getur eytt RCS-umhverfi og tengdum gögnum.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: cf82abbe5493eac9665323738441fa016205e9ef
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355008"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) – Eyða RCS-umhverfi

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig kerfisstjóri Regulatory Configuration Service (RCS) getur eytt RCS-umhverfi og tengdum gögnum.

Áður en hægt er að klára ferlið í þessu efnisatriði þarf að uppfylla eftirfarandi skilyrði:

- Nauðsynlegt er að vera með hlutverkið **Kerfisstjóri** úthlutað fyrir RCS-umhverfið.
- Hlutverkið **Kerfisstjóri** verður að vera með hlutverkið **RCSDeleteEnvironmentDuty** úthlutað.

## <a name="delete-an-rcs-environment"></a>Eyða RCS-umhverfi

1. Opnið RCS og veljið vinnusvæðið **Rafræn skýrslugerð**.
2. Í hlutanum **Tengdir tenglar** skal velja **Eyða RCS-umhverfi**.

    ![Eyða tengli RCS-umhverfis í hlutanum um tengda tengla.](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. Í svarglugganum sem birtist skal yfirfara skilaboðin um umfang eyðingar á umhverfi.

    ![Skilaboð í svarglugganum Eyða RCS-umhverfi.](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > Ekki er hægt að afturkalla eyðingu RCS-umhverfis.
    >
    > Aðgerðin eyðir völdu RCS-umhverfi og tengdum gögnum, þar á meðal eiginleikum og grunnstillingum sem eru vistaðar í altækri geymslu. Hætt verður að samnýta eiginleika og grunnstillingar sem er deilt með öðrum fyrirtækjum og þeim verður eytt ef þeir eru ekki tengdir við neitt. Eiginleikar og grunnstillingar sem eru tengdar öðru verða merktar sem hætt í notkun.

4. Í reitnum sem er gefinn upp skal færa inn altækt einkvæmt kennimerki (GUID) fyrir RCS-umhverfið til að staðfesta að það eigi að eyða því. GUID umhverfisins er með í skilaboðum um eyðingu.
5. Veljið **Eyða umhverfi**.
    
RCS-umhverfinu þínu og öllum tengdum gögnum hefur nú verið eytt.

> [!IMPORTANT]
> Eftir að RCS-umhverfi er eytt er engin leið til að endurheimta gögnin. Hægt er að búa til nýtt RCS-umhverfi á öllum tiltækum RCS-svæðum.
