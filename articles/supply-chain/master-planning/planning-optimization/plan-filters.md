---
title: Nota síur á áætlun
description: Þessi grein útskýrir hvernig á að nota síur á áætlun þegar hagræðing skipulags er notuð.
author: t-benebo
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: c2df379be0876225bc7b0301d21f4e6660b04eb6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875305"
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
> Ef þú stillir áætlunarsíu á áætlunina sem er valin sem **Núverandi kraftmikið aðalskipulag** á **Aðalskipulagsfæribreytur** síðu, þá verður kraftmikil aðaláætlunarvirkni takmörkuð við síuðu atriðin. Til dæmis, ef nettóþarfir eru uppfærðar fyrir vöru sem er ekki hluti af áætlunarsíunni, verður engin niðurstaða gefin.

## <a name="related-resources"></a>Tengd tilföng

[Yfirlit yfir fínstillingu skipulagningar](planning-optimization-overview.md)

[Byrjaðu með hagræðingu skipulags](get-started.md)

[Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md)

[Skoða áætlunarsögu og skipulagsskrár](plan-history-logs.md)

[Hætta við áætlunarvinnslu](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
