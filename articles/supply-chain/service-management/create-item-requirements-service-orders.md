---
title: Stofna vöruþörf fyrir þjónustupantanir
description: Ef nauðsynlegt er að taka til ákveðnar vörur fyrir þjónustupöntunina, hægt er að stofna birgðavöruþörf fyrir hana.
author: ShylaThompson
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 650d02d2160757d9629e4deb1e9217c85e9d01df
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831627"
---
# <a name="create-item-requirements-for-service-orders"></a>Stofna vöruþörf fyrir þjónustupantanir 

[!include [banner](../includes/banner.md)]


Þú getur búið til þjónustupöntun til að fylgjast með og stjórna þjónustu sem þú veitir viðskiptavinum þínum. Ef nauðsynlegt er að taka til ákveðnar vörur fyrir þjónustupöntunina, hægt er að stofna birgðavöruþörf fyrir hana. Hægt er að neyta vörukröfu strax úr birgðum, eða hún getur hafið framleiðslupöntun fyrir vöruna.

Með því að nota vörukröfu í staðinn fyrir vörufærsla, geturðu áætlað afhendingu rétt áður en vara er raunverulega notuð, stofnað innkaupapöntun, haft vöruna með í ramma viðskiptasamkomulags og innifalið vörukröfuna í framleiðsluáætlun.

Liður kröfur um þjónustu pantanir eru unnin í gegnum verkefni. Til að stofna vöruþörf í þjónustupöntun verður að úthluta þjónustupöntunina við verk. Eftir að þú hefur búið til vörukröfu fyrir þjónustupöntun getur þú skoðað vörukröfuna í skjámynd **Verkefni** fyrir verkefnið sem er valið.

## <a name="create-an-item-requirement-for-a-service-order"></a>Stofna vöruþörf fyrir þjónustupöntun

1.  Smelltu á **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.

2.  Valin þjónustupöntunin sem útbúa á vöruþörf fyrir.

3.  Á **Aðgerðarúða**, á flipanum **Afgreiða**, skal smella á **Vörukrafa**.

4.  Í **Vörukröfur** skjámynd, sláðu inn upplýsingar um vöruna sem krafist er. Fyrir frekari upplýsingar um tiltekna reiti, sjá [Vörukröfur (skjámynd)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Stofna vöruþörf fyrir þjónustusamning

1.  Smellið á **Þjónustustjórnun** \> **Almennt** \> **Þjónustusamningar** \> **þjónustusamningar**.

2.  Opnaðu þjónustusamninginn sem stofna á vörukröfu fyrir.

3.  Á **Línur** Flýtiflipanum skaltu smella á **Bæta við** til að búa til nýja línu.

4.  Í **Færslugerð** reitnum skaltu velja **Vara**.

5.  Í **Uppsetning vöru** reitnum, veldu **Vörukrafa**.

6.  Í **vörunúmer** reitnum, velja vöruna sem þjónustusamningurinn krefst.

7.  Á **Upplýsingar um línu** flýtiflipanum á flipanum **Afurðavídd** í reitnum **Svæði** skaltu velja birgðasvæði fyrir vöruna.

8.  Til að búa til þjónustupöntun frá samningslínunni skaltu smella á **Línur** Flýtiflipi, **Búa til þjónustupantanir** og sláðu síðan inn viðeigandi upplýsingar í **Búa til þjónustupantanir** skjámynd. 


## <a name="see-also"></a>Sjá einnig

[Stofna þjónustupantanir sjálfkrafa](create-service-orders-automatically.md).

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]