---
title: Grunnstilla afurð sem á að kaupa án endurgjalds
description: Þetta efnisatriði lýsir því hvernig á að stilla afurð þannig að hægt sé að kaupa hana án endurgjalds í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/27/2021
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2ad96a3dde93a48694aee418ecfbbd33dc9830d6
ms.sourcegitcommit: 6bf9e18989e6d77497a9dda1c362f324b3c2fbf2
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/27/2021
ms.locfileid: "7713886"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>Grunnstilla afurð sem á að kaupa án endurgjalds

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efnisatriði lýsir því hvernig á að stilla afurð þannig að hægt sé að kaupa hana án endurgjalds í Microsoft Dynamics 365 Commerce.

## <a name="configure-the-product"></a>Grunnstilla afurðina

Til að selja afurð án endurgjalds í Dynamics 365 Commerce þarf að stilla verð hennar á 0 (núll). Að auki þarf að grunnstilla stillinguna **Núllverð leyfilegt** fyrir afurðina.

Til að grunnstilla stillinguna **Núllverð leyfilegt** í Commerce Headquarters skal fylgja þessum skrefum.

1. Fara í **Smásölu og viðskipti \> Afurðir og tegundir \> Losaðar afurðir eftir flokki**.
1. Farðu í afurðina sem á að selja án endurgjalds. 
1. Í hlutanum **Commerce** á síðu afurðar skal stilla valkostinn **Núllverð leyfilegt** á **Já**.

Eftirfarandi mynd sýnir dæmi um afurð þar sem valkosturinn **Núllverð leyfilegt** er stilltur á **Já**.

![Dæmi um afurð þar sem valkosturinn Núllverð leyfilegt er stilltur á Já.](./media/Zero-price.png)

## <a name="configure-the-online-stores-functionality-profile"></a>Grunnstilla virknireglu netverslunar

Áður en hægt er að vinna úr endurgjaldslausum færslum ætti að grunnstilla stillinguna **Leyfa kaup án greiðslna** fyrir virknireglu netverslunarinnar þannig að færslur sem eru með engum greiðslum séu leyfðar. Frekari upp um hvernig á að búa til virknireglur er að finna í [Búa til virkniforstillingu á netinu](online-functionality-profile.md).

Til að grunnstilla stillinguna **Leyfa kaup án greiðslna** í Commerce Headquarters skal fylgja þessum skrefum.

1. Farið í **Retail og Commerce \> Uppsetning rásar \> Uppsetning netverslunar**.
1. Á síðunni fyrir virknireglu verslunarinnar, undir **Ljúka kaupum**, skal stilla valkostinn **Leyfa kaup án greiðslna** á **Já**.

Eftirfarandi mynd sýnir dæmi um forstillingu netverslunar þar sem valkosturinn **Leyfa kaup án greiðslna** er stilltur á **Já**.

![Dæmi um forstillingu netverslunar þar sem valkosturinn Leyfa kaup án greiðslna er stilltur á Já.](./media/Zero-price-profile.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Stjórnun smásöluverðs](price-management.md)

[Búa til virkniforstillingu á netinu](online-functionality-profile.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
