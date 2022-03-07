---
title: Ef hætt er við eftirstöðvar afhendingar verður innkaupapöntun flutt í staðfesta stöðu
description: Ef hætt er við eftirstöðvar afhendingar í innkaupapöntun þar sem kveikt er á breytingastjórnun, fer innkaupapöntunin í stöðuna Staðfest
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 1d8b331bc5699487dff3491d65daa36293f3212f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476672"
---
# <a name="cancelling-delivery-remainder-moves-purchase-order-to-a-confirmed-state"></a>Ef hætt er við eftirstöðvar afhendingar verður innkaupapöntun flutt í staðfesta stöðu

## <a name="symptoms"></a>Einkenni

Fyrir innkaupapöntun sem heyrir undir breytingastjórnun, ef eina breytingin sem beðið er um er afturköllun á eftirstöðvum afhendingar á einni eða fleiri línum, fer innkaupapöntunin beint í stöðuna *Staðfest* þegar hún er samþykkt og engin færslubók verður stofnuð.

## <a name="resolution"></a>Lausn

Afturköllun á eftirstöðvum afhendingar hefur ekki áhrif á innihald staðfestingarbókar. Nota ætti þessa virkni þegar búið er að taka á móti línunni að hluta til og hætta ætti við eftirstandandi magn í vinnsluskrefinu eftir að innkaupapöntunin hefur verið staðfest hjá lánardrottni.

Ef þetta á að koma fram á staðfestingu innkaupapöntunarinnar ætti að leiðrétta magnið í innkaupapöntunarlínunni svo staðfestingin verði nauðsynleg. Að öðrum kosti, ef ekkert hefur verið móttekið í línunni, er hægt að fjarlægja magnið. Í þessu tilfelli þarf að staðfesta aftur.
