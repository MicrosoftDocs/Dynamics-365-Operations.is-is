---
title: Afkastaendurbætur á hreinsun söluferils
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
ms.openlocfilehash: 3c8ad7b0bd46c49fc989be091f44630a6a3eebc1
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985912"
---
# <a name="sales-history-cleanup-performance-improvements"></a>Afkastaendurbætur á hreinsun söluferils

[!include [banner](../includes/banner.md)]

Reglubundin runuvinnsla **Hreinsun uppfærsluferils sölu** getur tekið langan tíma ef hún er sjaldan keyrð í umhverfum þar sem er mikið um söluuppfærslur. Í þessum tilvikum geta *Endurbætur á afköstum hreinsunar á söluferli* eiginleikinn hjálpað til við að stytta keyrslutíma og bæta áreiðanleika.

Þessi eiginleiki bætir núverandi hreinsunarvinnslu á eftirfarandi hátt:

- Hann skiptir hreinsun í runur (hægt er að breyta runustærð í sérstillingum).
- Hann er keyrður að hámarki í 2 klukkustundir (hægt er að breyta tímalengd í sérstillingum).
- Ef mögulegt nýtir hann getu gagnagrunnsins til að lágmarka læsingu og forðast að sameina færslutöflur við hreinsun.

Eftir að eiginleikinn er virkjaður verður runuvinnslan **Hreinsun uppfærsluferils sölu** (**Sala og markaðssetning \> Tímabilsverk \> Hreinsun \> Hreinsun uppfærsluferils sölu**) keyrð eins og áður en með betri afköstum og að hámarki í 2 klukkustundir. Þetta þýðir að hún þarf kannski að keyra nokkrum sinnum til að hreinsa öll gögn fyrir tiltekinn varðveislutímaramma.

## <a name="turn-on-the-sales-history-cleanup-performance-improvements-feature"></a>Kveiktu á eiginleikanum til að bæta árangur fyrir hreinsun sölusögu

Kveikja þarf á þessum eiginleika í kerfinu til að hægt sé að nota hann. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Sala og markaðssetning*
- **Heiti eiginleika:** *Endurbætur á afköstum hreinsunar á söluferli*
