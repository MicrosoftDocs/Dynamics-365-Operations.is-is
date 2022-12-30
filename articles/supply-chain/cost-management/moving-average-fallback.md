---
title: Hlaupandi meðaltal, röð varakostnaðar
description: Þessi grein veitir upplýsingar um  varakostnaðarraðir fyrir útreikning hlaupandi meðaltals í Microsoft Dynamics 365 Supply Chain Management.
author: JennySong-SH
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: ad67828e2608f4754a3dffd76c64292f6a91e95f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868015"
---
# <a name="moving-average-fallback-cost-sequence"></a>Varakostnaðarröð hlaupandi meðaltals

[!include [banner](../includes/banner.md)]

Ein leið til að reikna út kostnað við birgðir er með því að nota _hlaupandi meðaltal_. Hægt er að tengja allt að þrjú kostnaðargildi við hverja birgðavöru:

- **Síðasta úthreyfing** - Síðasti úthreyfingarkostnaður sem var úthlutað áður en birgðir urðu neikvæðar
- **Virkur kostnaður** - Síðasti kostnaður sem var virkjaður í kostnaðarútgáfu
- **Vöruverð** - Kostnaðurinn sem er tilgreindur fyrir útgefna afurð

Til að ákvarða hvert þessara kostnaðargilda skuli notað í útreikningum á meðaltali notar kerfið _varakostnaðarröð_ til að ákvarða forgangsröðun gildanna. Ef æskilegt kostnaðargildi ekki tiltækt notar kerfið næsta valið gildi og svo framvegis.

Í fyrri útgáfum af Microsoft Dynamics 365 Supply Chain Management notaði kerfið fasta varakostnaðarröð (_Síðasta úthreyfing - Virkur kostnaður - Vöruverð_). Í útgáfu 10.0.11 er þessi röð enn sjálfgefna röðin. Hins vegar getur þú einnig kveikt á eiginleikum sem gerir þér kleift að velja á milli þriggja tiltækra varakostnaðarraða. Þessi eiginleiki getur verið sérstaklega gagnlegur fyrir fyrirtæki sem nota reglulega neikvæð birgðagildi.

Til að gera val á varakostnaðarröð tiltæka verður þú (eða stjórnandi) að nota [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á eiginleikanum sem er nefndur _Varakostnaðarröð hlaupandi meðaltals_.

Fylgdu þessum skrefum til að velja varakostnaðarröð fyrir útreikninga á meðaltali.

1. Opnaðu síðuna **Færibreytur**.
2. Á flipanum **Birgðabókhald**, í hlutanum **Hlaupandi meðaltal**, stillirðu reitinn **Varakostnaðarröð** á eitt af eftirfarandi gildum:

    - **Síðasta úthreyfing - Virkur kostnaður - Verð vöru** - Þessi röð er sjálfgefin röð. Það er sama röð og er notuð ef ekki er kveikt á eiginleikanum _Varakostnaðarröð hlaupandi meðaltals_.
    - **Virkur kostnaður – síðasti kostnaður**
    - **Virkur kostnaður - Vöruverð** - Fyrirtæki gætu lent í afkomuvandamálum ef þau nota viðskiptaferla þar sem birgðir verða reglulega neikvæðar og færsluumfangið er um leið mikið. Þessi stilling getur hjálpað til við að draga úr þessum afkastavandamálum.

![Færibreytur birgðabókhalds.](media/inventory-accounting-parameters.png "Færibreytur birgðabókhalds")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]