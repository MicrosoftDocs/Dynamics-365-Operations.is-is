---
title: Stofna skilgreiningarveitendur og merkja þá sem virka
description: Þetta efni útskýrir hvernig notandi sem er úthlutað á hlutverk kerfisstjóra eða þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarveitu fyrir rafræna skýrslugerð (ER).
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5f238a492dbc3f9318b1bd1d3ea5657e92b33fb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142110"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Stofna skilgreiningarveitendur og merkja þá sem virka

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig notandi sem er úthlutað á hlutverk kerfisstjóra eða þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarveitu fyrir rafræna skýrslugerð (ER). Hverja skilgreiningu rafrænnar skýrslugerðar vísar til veitu sem höfund skilgreiningar. Í þessu dæmi, verður að stofna skilgreiningu fyrir dæmi um fyrirtæki, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja.

## <a name="create-a-provider"></a>Búa til veitu
1. Farðu í **skoðunarrúðu** efst í vinstra horninu og veldu **Fyrirtækisstjórnun**.
2. Farðu í **Vinnusvæði > Rafræn skýrslugerð**.
3. Farðu í **Skyldir tenglar> Skilgreiningarveitur**.
4. Veljið **Nýtt**.
    - Skrá veitu er einkvæmt hvað varðar heiti og vefslóð. Yfirfarið innihald þessarar síðu og sleppið ferlinu ef færsla fyrir Litware, Inc. (https://www.litware.com) er þegar til.  
5. Í svæðið Heiti skaltu færa inn `Litware, Inc.`.
6. Í reitinn Vefsvæði skal slá inn `https://www.litware.com`.
7. Veljið **Vista**.
8. Lokið síðunni.

## <a name="select-as-an-active-provider"></a>Veljið sem virka veitu
1. Velja “Litware, Inc.” veitu
2. Veldu **Stilla sem virkt**.

![Síðan Vinnusvæði rafrænnar skýrslugerðar](../media/GER-Task-ActiveProvider-1.png)
