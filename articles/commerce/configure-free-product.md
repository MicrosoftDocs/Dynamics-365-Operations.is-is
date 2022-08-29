---
title: Grunnstilla afurð sem á að kaupa án endurgjalds
description: Þessi grein lýsir því hvernig á að stilla vöru þannig að hægt sé að kaupa hana ókeypis í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 88370085de047a5e0be773dde218770cfa242d14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280365"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>Grunnstilla afurð sem á að kaupa án endurgjalds

[!include [banner](includes/banner.md)]


Þessi grein lýsir því hvernig á að stilla vöru þannig að hægt sé að kaupa hana ókeypis í Microsoft Dynamics 365 Commerce.

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
