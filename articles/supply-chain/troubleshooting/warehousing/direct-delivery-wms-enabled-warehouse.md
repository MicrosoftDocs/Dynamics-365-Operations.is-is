---
title: Bein afhending getur ekki sinnt úrvinnslu fyrir vöruhús virkjað af vöruhúsakerfi
description: Ef vöruhúsið er með vöruhúsakerfi virkjað styður það ekki beina afhendingu. Til að nota beina afhendingu skal velja vöru sem er ekki WMS og vöruhús.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 090e17091e9fb92c2065679bb9b04637214e2eea
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476712"
---
# <a name="direct-delivery-not-able-to-process-for-wms-enabled-warehouse"></a>Bein afhending getur ekki sinnt úrvinnslu fyrir vöruhús virkjað af vöruhúsakerfi

## <a name="symptoms"></a>Einkenni

Ef vöru er bætt við sölulínu fyrir beina afhendingu úr vöruhúsi þar sem vöruhúsakerfi (WMS) er virkjað færðu eftirfarandi villuboð þegar sölulínan er uppfærð:

> Ekki er hægt að vinna úr beinni afhendingu fyrir vöruhús 1% því vöruhúsakerfi er virkt. Tilgreinið annað vöruhús sem er ekki virkt fyrir vöruhúsastjórnun.

## <a name="resolution"></a>Lausn

Microsoft hefur metið þetta mál og hefur ákvarðað að þetta sé takmörkun eiginleika. Sem stendur styður vöruhúsakerfi ekki beina afhendingu. Til að nota beina afhendingu skal því velja vöru sem er ekki WMS og vöruhús.
