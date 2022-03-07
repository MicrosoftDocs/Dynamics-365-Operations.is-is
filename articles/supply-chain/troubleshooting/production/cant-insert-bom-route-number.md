---
title: Get ekki sett inn virka útgáfu af uppskrift og leiðarnúmerum
description: Ef sjálfgefið svæði og vöruhús eru þegar skilgreind fyrir valda afurð verður ekki beðið um að setja inn virka útgáfu af uppskrift og leiðarnúmerum.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 241618d70f01c85df946a48493f5d84e0964218e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476613"
---
# <a name="cant-insert-bill-of-material-and-route-when-creating-a-new-production-order"></a>Get ekki sett inn uppskrift og leið þegar ný framleiðslupöntun er stofnuð

## <a name="symptoms"></a>Einkenni

Þegar ný framleiðslupöntun er stofnuð þegar búið er að færa inn vörunúmerið eru reitirnir **Svæði** og **Vöruhús** sjálfkrafa stilltir á sjálfgefið svæði og vöruhús sem eru skilgreind á síðunni **Sjálfgefnar pöntunarstillingar** fyrir fullunna vöru. Auk þess er virkt uppskriftarnúmer og leiðarnúmer sjálfkrafa fært inn þannig að þú færð ekki eftirfarandi skilaboð sem biðja þig um þessi gildi:

> Á að setja inn virka útgáfu fyrir uppskrift og leið?

## <a name="resolution"></a>Lausn

Notandi er ekki beðinn um að setja inn uppskrift og leiðarnúmer ef afurð er valin sem svæði og vöruhús er þegar á síðunni **Sjálfgefnar pöntunarstillingar**. Beiðni birtist aðeins ef gildin eru ekki skilgreind fyrir valda afurð.
