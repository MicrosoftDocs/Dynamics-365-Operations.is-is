---
title: Úrræðaleit fyrir áfyllingar vöruhúss
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með áfyllingar vöruhúss í Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8940f729e1115405e8d6e50eccc92d9fffe37f3e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828083"
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