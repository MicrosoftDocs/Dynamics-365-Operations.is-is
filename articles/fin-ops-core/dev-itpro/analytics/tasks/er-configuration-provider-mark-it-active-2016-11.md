---
title: Stofna skilgreiningarveitendur og merkja þá sem virka
description: Í þessu efnisatriði er útskýrt hvernig notandi sem úthlutað er hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslugerðar getur stofnað skilgreiningarveitu.
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 835e35ef233ba5734e5a4d47f624629e95ae5b89
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092061"
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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]