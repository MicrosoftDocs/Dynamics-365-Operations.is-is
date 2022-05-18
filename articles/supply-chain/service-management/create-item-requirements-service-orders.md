---
title: Stofna vöruþörf fyrir þjónustupantanir
description: Þetta efnisatriði lýsir því hvernig á að stofna vöruþörf fyrir þjónustupantanir.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a92843a82093826822ab9865e43fee07d65e94c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677815"
---
# <a name="create-item-requirements-for-service-orders"></a>Stofna vöruþörf fyrir þjónustupantanir

[!include [banner](../includes/banner.md)]

Þú getur búið til þjónustupöntun til að fylgjast með og stjórna þjónustu sem þú veitir viðskiptavinum þínum. Ef nauðsynlegt er að taka til ákveðnar vörur fyrir þjónustupöntunina, hægt er að stofna birgðavöruþörf fyrir hana. Hægt er að neyta vörukröfu strax úr birgðum, eða hún getur hafið framleiðslupöntun fyrir vöruna.

Með því að nota vörukröfu í staðinn fyrir vörufærsla, geturðu áætlað afhendingu rétt áður en vara er raunverulega notuð, stofnað innkaupapöntun, haft vöruna með í ramma viðskiptasamkomulags og innifalið vörukröfuna í framleiðsluáætlun.

Liður kröfur um þjónustu pantanir eru unnin í gegnum verkefni. Til að stofna vöruþörf í þjónustupöntun verður að úthluta þjónustupöntunina við verk. Eftir að þú hefur búið til vörukröfu fyrir þjónustupöntun getur þú skoðað vörukröfuna í skjámynd **Verkefni** fyrir verkefnið sem er valið.

## <a name="create-an-item-requirement-for-a-service-order"></a>Stofna vöruþörf fyrir þjónustupöntun

1. Veljið **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.
1. Valin þjónustupöntunin sem útbúa á vöruþörf fyrir.
1. Á **Aðgerðasvæðinu**, í flipanum **Senda**, skal velja **Vöruþörf**.
1. Í **Vörukröfur** skjámynd, sláðu inn upplýsingar um vöruna sem krafist er. Fyrir frekari upplýsingar um tiltekna reiti, sjá [Vörukröfur (skjámynd)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Stofna vöruþörf fyrir þjónustusamning

1. Veljið **Þjónustustjórnun** \> **Almennt** \> **Þjónustusamningar** \> **þjónustusamningar**.
1. Opnaðu þjónustusamninginn sem stofna á vörukröfu fyrir.
1. Í flýtiflipanum **Línur** skal velja **Bæta við** til að búa til nýja línu.
1. Í **Færslugerð** reitnum skaltu velja **Vara**.
1. Í **Uppsetning vöru** reitnum, veldu **Vörukrafa**.
1. Í **vörunúmer** reitnum, velja vöruna sem þjónustusamningurinn krefst.
1. Á **Upplýsingar um línu** flýtiflipanum á flipanum **Afurðavídd** í reitnum **Svæði** skaltu velja birgðasvæði fyrir vöruna.
1. Til að búa til þjónustupöntun frá samningslínunni skaltu velja **Línur** Flýtiflipi, **Búa til þjónustupantanir** og sláðu síðan inn viðeigandi upplýsingar í **Búa til þjónustupantanir** skjámynd.

## <a name="see-also"></a>Sjá einnig

[Stofna þjónustupantanir sjálfkrafa](create-service-orders-automatically.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
