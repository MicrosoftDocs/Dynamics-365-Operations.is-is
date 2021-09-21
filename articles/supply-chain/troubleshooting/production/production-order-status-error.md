---
title: Villa við að breyta stöðu úr „Tilkynna sem tilbúið“ í „Lokið“
description: Villa gæti komið upp við að breyta stöðu framleiðslupöntunar úr „Tilkynna sem tilbúið“ í „Lokið“. Á þessari síðu er útskýrt hvernig draga má úr vandamálinu.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 744637f5cccffe44b85f77c1a9df2034012fac40
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476666"
---
# <a name="error-when-changing-status-of-production-order-from-reported-as-finished-to-end"></a>Villa við að breyta stöðu framleiðslupöntunar úr „Tilkynna sem tilbúið“ í „Lokið“

## <a name="symptoms"></a>Einkenni

Þegar stöðu framleiðslupöntunar er breytt úr Tilkynna sem tilbúið í Lokið færð þú eftirfarandi villuboð:

> Uppfæra árekstur. Staðalkostnaður stemmir ekki við gildi fjárhagslegra birgða eftir uppfærsluna.

> Alvarleg villa varð í aðgerð InventCostMovement.checkVariance.

## <a name="cause"></a>Orsök

Þetta vandamál á sér stað vegna þess að undirliggjandi gögnum var breytt í öðru ferli. Ferlið mun reyna að uppfæra gögnin allt að fimm sinnum. Ef áreksturinn er enn til staðar eftir fimm tilraunir færðu eitt af skilaboðunum sem talin eru upp hér að ofan.

## <a name="resolution"></a>Lausn

Þessi hegðun er samkvæmt hönnuninni. Til að laga vandamálið skal halda áfram með runuvinnsluna. Það ætti að ljúka vinnslu.

Ef runuvinnslan mistekst endurtekið þegar henni er haldið áfram skal ganga úr skugga um að sléttunarnákvæmni fyrir sjálfgefinn gjaldmiðil fjárhags fylgi sléttunarreglum sem eru notaðar fyrir gildi í töflunni InventSum. Ef sléttunarnákvæmni hefur verið breytt í ósamræmanlegt gildi verður líklega að breyta henni aftur í samræmanlegt gildi. Leitið að **ModifiedDateTime**. Í þessu tilvikum sýnir gildið venjulega að sléttunarnákvæmni var breytt nýlega.
