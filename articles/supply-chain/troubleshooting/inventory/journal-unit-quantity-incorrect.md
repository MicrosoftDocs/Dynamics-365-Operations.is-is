---
title: Eining og magn einingar virka ekki á réttan hátt í birgðabókinni
description: Eining og magn einingar virka ekki á réttan hátt í birgðabókinni
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 39f462ae325aa1104a25a8290daed70388e624ec
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476641"
---
# <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Eining og magn einingar virka ekki á réttan hátt í birgðabókinni

## <a name="symptoms"></a>Einkenni

Annað eða bæði þessi vandamál gætu komið upp þegar unnið er með einingar og magn í birgðabók:

- Ekki er hægt að breyta einingum eða magni í birgðabókinni á meðan umreikningseining er sett upp fyrir útgefna afurð og ekki er hægt að skipta um einingu í birgðabókinni.
- Reitirnir **Magn** og **Eining** sjást í birgðabókinni, en reiturinn **Magn einingar** sést ekki. Ef einingunni er breytt skal færa inn magn og bóka færslubókina, færslubókin sýnir enn upprunalega mælieininguna fyrir það magn.

## <a name="resolution"></a>Lausn

Til að laga þetta vandamál skal fylgja þessum skrefum.

1. Á vinnusvæðinu **Eiginleikastjórnun** skal ganga úr skugga um að kveikt sé á eiginleikanum *Notkun mælieiningar og einingarmagns í birgðabókum*. Þessi eiginleiki bætir reitunum **Eining** og **Magn einingar** við færslubókina.
1. Þegar kveikt hefur verið á eiginleikanum skal nota reitina **Magn**, **Magn einingar** og **Eining** á eftirfarandi hátt:

    - **Magn** – Tilgreinið magnið með því að nota sjálfgefna einingu sem er skilgreind fyrir útgefna afurð. Sjálfgefin eining er hins vegar ekki sýnd hér. Ef umreikningur er uppsettur milli sjálfgefinnar einingar og einingarinnar sem er valin í reitnum **Eining** verður reiturinn **Magn** uppfærður sjálfkrafa út frá því sem er valið í reitunum **Magn einingar** og **Eining**.
    - **Magn einingar** – Tilgreinið magnið með því að velja eininguna sem er valin í reitnum **Eining**.
    - **Eining** – Veljið eininguna sem á að nota fyrir gildið í reitnum **Magn einingar**.
