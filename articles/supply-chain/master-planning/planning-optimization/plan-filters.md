---
title: Nota síur á áætlun
description: Þetta efni útskýrir hvernig á að nota síur á áætlun þegar virknin fínstillingu skipulagningar er notuð.
author: ChristianRytt
manager: tfehr
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 9ddf9934965bd06ec805731a1cc1a667846fa180
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430303"
---
# <a name="apply-filters-to-a-plan"></a>Nota síur á áætlun

[!include [banner](../../includes/banner.md)]

Þegar virknin fínstillingar áætlunargerðar er notuð geturðu notað síu á áætlun. **Áætlunarsíunni** verður alltaf beitt meðan á keyrslu aðaláætlunargerðar stendur. **Áætlunarsía** er gagnleg þegar þú vilt takmarka áætlun við ákveðinn hóp af vörum og ganga úr skugga um að engar aðrar vörur séu með sem hluti af aðaláætlunargerðinni sem er gerð.

Ef **áætlunarsía** er notuð og keyrslutímasíu er einnig beitt meðan á keyrslu aðaláætlunargerðar stendur er aðeins skörun síanna tveggja innifalin í áætlunarkeyrslunni.

Hægt er að fara í **áætlunarsíuna** úr **Aðaláætlunum** þegar fínstilling áætlunargerðar er notuð.

## <a name="example-scenario"></a>Dæmi

Áætlunarsía er sett upp sem inniheldur vörur A, B og C. Aðalskipulagningarkeyrslur eru síðan keyrðar fyrir sömu áætlun, en mismunandi keyrslutímasíur eru notaðar:

- **Keyrslutímasía sem inniheldur vöru D:** Engar vörur eru fyrirhugaðar þar sem engin skörun er á milli áætlunarsíunnar og keyrslutímasíunnar.
- **Keyrslutímasía sem inniheldur vöru A og D:** Aðeins vara A er innifalin í áætlunarkeyrslunni þar sem vara D er ekki hluti af áætlunarsíunni.
- **Keyrslutímasía sem inniheldur vöru B:** Aðeins vara B er innifalin í áætlunarkeyrslunni og fyrra úttaki áætlunargerðar fyrir vöru A er haldið.
- **Keyrslutímasía sem inniheldur allar vörur (auð sía):** Vörur A, B og C eru innifaldar í áætlunarkeyrslunni og fyrra úttak áætlanagerðar fyrir vörurnar A og B er yfirskrifað.

> [!NOTE]
> Þú ættir að forðast að setja áætlunarsíu á áætlunina sem er valin sem **Gildandi kvik aðaláætlun** á síðunni **Færibreytur áætlanagerðar**. Annars verður virkni kvikrar aðaláætlunar takmörkuð við síaðar vörur. Til dæmis, ef nettóþarfir eru uppfærðar fyrir vöru sem er ekki hluti af áætlunarsíunni, verður engin niðurstaða gefin.

## <a name="related-resources"></a>Tengd tilföng

[Yfirlit yfir fínstillingu skipulagningar](planning-optimization-overview.md)

[Byrjaðu með hagræðingu skipulags](get-started.md)

[Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md)

[Skoða áætlunarsögu og skipulagsskrár](plan-history-logs.md)

[Hætta við áætlunarvinnslu](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]