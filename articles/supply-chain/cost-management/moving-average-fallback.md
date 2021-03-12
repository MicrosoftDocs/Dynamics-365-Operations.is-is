---
title: Varakostnaðarröð hlaupandi meðaltals
description: Þetta efni veitir upplýsingar um varakostnaðarraðir fyrir útreikninga á meðaltal í Microsoft Dynamics 365 Supply Chain Management.
author: AndersGirke
manager: tfehr
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 541b7ecca5c1c36999f573d6d0f2dc0c9e901631
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967584"
---
# <a name="moving-average-fallback-cost-sequence"></a>Varakostnaðarröð hlaupandi meðaltals

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

![Færibreytur birgðabókhalds](media/inventory-accounting-parameters.png "Færibreytur birgðabókhalds")
