---
title: Niðurbrot uppskriftar hagar sér öðruvísi fyrir staðfestar og áætlaðar framleiðslupantanir
description: Niðurbrot uppskriftar hegðar sér á annan hátt fyrir staðfestar framleiðslupantanir og fyrir áætlaðar framleiðslupantanir fyrir vinnu sem er búið að stofna handvirkt
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
ms.openlocfilehash: 94d4b00ea30396923a61b2748cf1aaeedc0af8af
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476657"
---
# <a name="bom-explosion-behaves-differently-for-firmed-and-estimated-production-orders"></a>Niðurbrot uppskriftar hagar sér öðruvísi fyrir staðfestar og áætlaðar framleiðslupantanir

## <a name="symptoms"></a>Einkenni

Þegar framleiðslupöntun er staðfest eru vörurnar ekki brotnar niður þegar þú brýtur uppskriftirnar niður. Hins vegar þegar þú stofnar verkbeiðni handvirkt og áætlar síðan framleiðslupöntunina eru vörurnar brotnar niður.

### <a name="resolution"></a>Lausn

Niðurbrotið sem verður þegar framleiðslupöntunin er staðfest vísar á áætlaða pöntun en áætlaða pöntunin virðist ekki vera staðfest í þessu tilviki. Ef framleiðslupöntunin hefur hins vegar verið metin er niðurbrotið ræst af útgefnu framleiðslupöntuninni þegar engin áætluð pöntun er til staðar.
