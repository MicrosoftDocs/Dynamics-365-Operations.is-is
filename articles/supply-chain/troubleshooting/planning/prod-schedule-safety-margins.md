---
title: Framleiðsluröðun tekur ekki tillit til öryggismarka
description: Framleiðsluröðun tekur ekki til greina öryggismörk sem eru stillt á vöruþekju fyrir fest framboð
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 738296b7570ded0a4ee806e4445204a68e6a08c8
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476639"
---
# <a name="production-scheduling-doesnt-consider-the-safety-margins"></a>Framleiðsluröðun tekur ekki tillit til öryggismarka

## <a name="symptoms"></a>Einkenni

Aðaláætlanagerð áætlar öryggismörk. Hins vegar eru öryggismörk hunsuð um leið og áætlaðar framleiðslupantanir eru áætlaðar.

## <a name="resolution"></a>Lausn

Aðeins er tekið tillit til marka við aðaláætlanagerð, ekki við handvirka áætlanagerð. Mörk eiga að gegna hlutverki biðminnis við áætlunarferlið til að setja tiltekin „mörk“ fyrir raunverulega ferlið.

Til að fá æskilega útkomu er hægt að fjarlægja framlegðina. Síðan verður að uppfæra leiðina þannig að hún innihaldi tímann sem óskað er eftir (til dæmis, sem biðtími). Bæði aðaláætlanagerð og handvirk röðun ættu þá að búa til sömu niðurstöður.
