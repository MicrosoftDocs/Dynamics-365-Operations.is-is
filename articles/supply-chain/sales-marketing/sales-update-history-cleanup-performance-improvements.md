---
title: Endurbætur á afköstum hreinsunar á söluferli
description: Þetta efnisatriði lýsir eiginleika fyrir endurbætur á afköstum hreinsunar á sölusögu og hvernig á að virkja hann.
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
ms.openlocfilehash: 563ac90dc8c037066b8ccd6d8986e089a66245af
ms.sourcegitcommit: 42bd701179e664947b6eafcd1804c83a5e64abcb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2021
ms.locfileid: "7641466"
---
# <a name="saleshistorycleanupperformanceimprovements"></a>Endurbætur á afköstum hreinsunar á söluferli

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Reglubundin runuvinnsla **Hreinsun uppfærsluferils sölu** getur tekið langan tíma ef hún er sjaldan keyrð í umhverfum þar sem er mikið um söluuppfærslur. Í þessum tilvikum geta *Endurbætur á afköstum hreinsunar á söluferli* eiginleikinn hjálpað til við að stytta keyrslutíma og bæta áreiðanleika.

Þessi eiginleiki bætir núverandi hreinsunarvinnslu á eftirfarandi hátt:

- Hann skiptir hreinsun í runur (hægt er að breyta runustærð í sérstillingum).
- Hann er keyrður að hámarki í 2 klukkustundir (hægt er að breyta tímalengd í sérstillingum).
- Ef mögulegt nýtir hann getu gagnagrunnsins til að lágmarka læsingu og forðast að sameina færslutöflur við hreinsun.

Eftir að eiginleikinn er virkjaður verður runuvinnslan **Hreinsun uppfærsluferils sölu** (**Sala og markaðssetning \> Tímabilsverk \> Hreinsun \> Hreinsun uppfærsluferils sölu**) keyrð eins og áður en með betri afköstum og að hámarki í 2 klukkustundir. Þetta þýðir að hún þarf kannski að keyra nokkrum sinnum til að hreinsa öll gögn fyrir tiltekinn varðveislutímaramma.

## <a name="turn-on-the-saleshistorycleanupperformanceimprovements-feature"></a>Kveikja á eiginleikanum fyrir endurbætur á afköstum hreinsunar á söluferli

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Sala og markaðssetning*
- **Heiti eiginleika:** *Endurbætur á afköstum hreinsunar á söluferli*
