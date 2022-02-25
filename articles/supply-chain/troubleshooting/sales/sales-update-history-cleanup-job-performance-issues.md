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
ms.openlocfilehash: 371a8c7178cd7c5091d6dd9a91d0ee03b943a269
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103189"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Hreinsunarvinnsla á uppfærsluferli sölu mistekst eða inniheldur vandamál sem tengjast afköstum

## <a name="symptoms"></a>Einkenni

Runuvinnslan **Hreinsunarvinnsla á uppfærsluferli sölu** mistekst eða inniheldur vandamál sem tengjast afköstum.  

## <a name="cause"></a>Orsök

Þetta getur átt sér stað þegar kerfið þitt inniheldur mikinn fjölda af söluuppfærslum sem getur leitt til mikils magns af söluuppfærslugögnum. Hreinsunarvinnslan reynir að hreinsa öll þessi gögn í einni færslu. Þar af leiðandi kann vinnslan að taka mjög langan tíma í keyrslu eða jafnvel mistakast.

## <a name="resolution"></a>Upplausn

Ný útgáfa af runuvinnslu **Hreinsun uppfærsluferil sölu** er tiltækt fyrir Supply Chain Management útgáfu 10.0.19 og nýrri útgáfur. Sjálfgefið er ekki kveikt á þessum eiginleika. Fyrir upplýsingar um hvernig það virkar og hvernig á að virkja það í eiginleikastjórnun, sjá [Endurbætur á árangri í hreinsun sölusögu](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

