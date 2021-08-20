---
title: Úrræðaleit fyrir framleiðsluferli
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með framleiðsluferli.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 13eb50ef634de211a864a3f27defe2276cb66f411480e2074693c8b8972a284b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726706"
---
# <a name="troubleshoot-process-manufacturing"></a>Úrræðaleit fyrir framleiðsluferli

Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með framleiðsluferli.

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a>Þegar ég nota verkspjaldstækið til að skrá hlutamagn í síðustu vinnslu framleiðslupöntunar er öllum fyrri vinnslum á pöntuninni sem hafa stöðuna í vinnslu sjálfkrafa lokið.

Þessi hegðun er samkvæmt hönnuninni. Á síðunni **Sjálfgildi framleiðslupöntunar** á flipanum **Bóka sem tilbúið** er valkostur sem kallast **Merkja lok ferlis**. Þegar þetta efnisatriði er stillt á *Já* er færslubók leiðarspjalds bókuð þegar starfskraftur notar verkspjaldstækið eða afgreiðslustöð verkspjalds til að skrá síðustu aðgerðina. Þessi færslubók merkir alla aðgerðir sem lokið og lýkur öllum framleiðsluverkum. Þegar valkosturinn **Merkja lok ferlis** er stilltur á *Já* virðir kerfið ekki stöðu vinnslu sem starfskrafturinn valdi þegar hann tilkynnti um síðustu aðgerðina. Kerfið segir ekki til um það hvort starfskrafturinn sé að tilkynna um heildarmagn eða hluta.

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a>Þegar ég reyni að loka birgðum fæ ég eftirfarandi viðvörunarboð: „Engin aðgerð til að framkvæma útreikning bakfærslukostnaðaraðferðar með dagsetningu %1 samsvarandi tímabil hefur verið skráð“.

Við notkun útgáfa sem eru eldri en útgáfa 10.0.13 og þú notar ekki kostnaðarflæði í Lean-framleiðslu færðu eftirfarandi viðvörunarboð að ósekju við birgðalokun:

> Þú ert að fara að framkvæma birgðalokun með dagsetningu %1. Engin keyrsla á bakfærslukostnaðaraðferð útreiknings með dagsetningu %1 sem samsvarar tímabilslokum hefur verið skráð. Munið að keyra bakfærslukostnaðaraðferðar með dagsetningu á %1 sem samsvarar lokun tímabilsins. Mat á birgðum, kostnaði seldra vara og frávikum er mögulega ekki rétt í undirbók eða fjárhag fyrr en þetta hefur verið keyrt.

Leyst hefur verið úr vandamálinu í útgáfu 10.0.13 og nýrri. Frekari upplýsingar er að finna í [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]