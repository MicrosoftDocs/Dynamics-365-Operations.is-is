---
title: Altækur staðgreiðsluskattur
description: Þetta efnisatriði veitir upplýsingar um virkni altæks staðgreiðsluskatts og hvernig á að setja hana upp. Virkni altæks staðgreiðsluskatts er bætt fyrir færslur lánardrottins og viðskiptavinar þannig að staðgreiðsluskattur er reiknaður á vörustigi.
author: roschlom
ms.date: 01/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "15721"
- intro-internal
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 7a3bb3c8766c7dd591f66a663d8be17769bb7d53
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986177"
---
# <a name="global-withholding-tax"></a>Altækur staðgreiðsluskattur

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um virkni altæks staðgreiðsluskatts og útskýrir hvernig á að setja hana upp. Nýja virknin er í boði í útgáfu 10.0.17 og nýrri.

Virkni altæks staðgreiðsluskatts er bætt fyrir færslur lánardrottins og viðskiptavinar þannig að staðgreiðsluskattur er reiknaður á vörustigi. Staðan í staðgreiðsluskattslykli frá innkaupafærslum er hægt að jafna með því að keyra greiðsluvinnslu staðgreiðsluskatts á móti jöfnunarlykli staðgreiðsluskatts.

> [!NOTE]
> Altækur staðgreiðsluskattur styður ekki virknina **Vinna með gjöld** á síðum innkaupapöntunar, lánardrottnareikningis og sölupöntunar.

## <a name="turn-on-global-withholding-tax"></a>Kveikja á altækum staðgreiðsluskatti

1. Á vinnusvæðinu **Eiginleikastjórnun** skal velja **Altækur staðgreiðsluskattur** og síðan velja **Virkja núna**.
2. Farið í **Skattur \> Uppsetning \> Færibreytur \> Færibreytur fjárhags** og síðan í flipanum **Staðgreiðsluskattur** skal stilla valkostinn **Virkja altækan staðgreiðsluskatt** á **Já**.
3. Veljið **Vista**.
4. Uppfærið síðuna í vafranum.

> [!NOTE]
> Ekki er hægt að kveikja á virkni altæks staðgreiðsluskatts fyrir lönd/svæði þar sem staðbundnar lausnir staðgreiðsluskatts eru þegar til staðar. Þessi lönd eru m.a. Indland, Brasilía, Taíland, Sádi-Arabía, Írland, Stóra-Bretland og Bandaríkin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
