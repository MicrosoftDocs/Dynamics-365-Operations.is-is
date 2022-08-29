---
title: Stofna skilgreiningarveitendur og merkja þá sem virka
description: Þessi grein útskýrir hvernig notandi sem er úthlutað hlutverki kerfisstjóra eða rafrænnar skýrslugerðarframleiðanda getur búið til stillingaveitu.
author: kfend
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
ms.openlocfilehash: db5226720a4e0c0f167921a972429c0a5ecdd2e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267814"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Stofna skilgreiningarveitendur og merkja þá sem virka

[!include [banner](../../includes/banner.md)]

Þessi grein útskýrir hvernig notandi sem er úthlutað hlutverki kerfisstjóra eða þróunaraðila rafrænna skýrslugerðar getur búið til stillingarveitu fyrir rafrænar skýrslur (ER). Hverja skilgreiningu rafrænnar skýrslugerðar vísar til veitu sem höfund skilgreiningar. Í þessu dæmi, verður að stofna skilgreiningu fyrir dæmi um fyrirtæki, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja.

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

![Síðan Vinnusvæði rafrænnar skýrslugerðar.](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
