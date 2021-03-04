---
title: Úrræðaleit fyrir áfyllingar vöruhúss
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með áfyllingar vöruhúss í Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e4d87e85520c2b6f2346fddf3b985d4e17fe35cb
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644874"
---
# <a name="troubleshoot-warehouse-replenishment"></a>Úrræðaleit fyrir áfyllingar vöruhúss

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með áfyllingar vöruhúss í Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>Ég fæ eftirfarandi villuboð: Ekki er hægt að opna fyrir vinnu %1 vegna þess að hún inniheldur ólokna áfyllingarvinnu.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Tiltektarvinna er lokuð vegna háðrar áfyllingarvinnu.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þegar eftirspurnaráfylling bylgju er notuð, ef fylla verður á tiltektarstaðsetningu til að uppfylla eftirspurn upprunapöntunar, stofnar kerfið bæði áfyllingarvinnu og tiltektarvinnu. Hins vegar lokar það tiltektarvinnu þar til áfyllingarvinnu er lokið. Þessi hegðun er innbyggð, vegna þess að tiltektarstaðsetningin mun ekki innihalda nægar birgðir nema áfyllingarvinnu sé lokið. Ljúka skal áfyllingarvinnu og vinna síðan tiltektarverk.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]