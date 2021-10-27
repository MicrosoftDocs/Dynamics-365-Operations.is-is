---
title: Hreinsunarvinnsla á uppfærsluferli sölu mistekst eða inniheldur vandamál sem tengjast afköstum
description: Hreinsunarrunuvinnsla sölusögu getur mistekist eða tekið mjög langan tíma ef mikið er af söluuppfærslugögnum.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 4f04dc204c705b40ed25fadc75118feaef4d6b6e
ms.sourcegitcommit: 42bd701179e664947b6eafcd1804c83a5e64abcb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2021
ms.locfileid: "7641465"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Hreinsunarvinnsla á uppfærsluferli sölu mistekst eða inniheldur vandamál sem tengjast afköstum

## <a name="symptoms"></a>Einkenni

Runuvinnslan **Hreinsunarvinnsla á uppfærsluferli sölu** mistekst eða inniheldur vandamál sem tengjast afköstum.  

## <a name="cause"></a>Orsök

Þetta getur átt sér stað þegar kerfið þitt inniheldur mikinn fjölda af söluuppfærslum sem getur leitt til mikils magns af söluuppfærslugögnum. Hreinsunarvinnslan reynir að hreinsa öll þessi gögn í einni færslu. Þar af leiðandi kann vinnslan að taka mjög langan tíma í keyrslu eða jafnvel mistakast.

## <a name="resolution"></a>Upplausn

Ný útgáfa af runuvinnslu **Hreinsun uppfærsluferil sölu** er tiltækt fyrir Supply Chain Management útgáfu 10.0.19 og nýrri útgáfur. Þessi eiginleiki er ekki virkur að sjálfgefnu. Frekari upplýsingar um hvernig hún virkar og hvernig hægt er að virkja hana í eiginleikastjórnun er að finna í [Afkastaendurbætur hreinsunar á sölusögu](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

