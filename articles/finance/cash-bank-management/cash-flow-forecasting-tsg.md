---
title: Úrræðaleit vegna uppsetningar sjóðstreymisspár
description: Þetta efnisatriði veitir svör við spurningum sem gætu vaknað þegar verið er að skilgreina sjóðstreymisspár. Þar er svarað algengum spurningum um uppsetningu sjóðstreymis, uppfærslur á sjóðstreymi og sjóðstreymi Power BI.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 89eb2f1bcfc73a6a7171a275532b2356e858e87c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985288"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a>Úrræðaleit vegna uppsetningar sjóðstreymisspár

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir svör við spurningum sem gætu vaknað þegar verið er að skilgreina sjóðstreymisspár. Þar er svarað algengum spurningum um uppsetningu sjóðstreymis, uppfærslur á sjóðstreymi og sjóðstreymi Power BI.

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a>Hvers vegna er sjóðstreymi sýnd fyrir aðeins einn lögaðila?

Sjóðstreymisspá er skilgreind og reiknuð fyrir hvern lögaðila fyrir sig. Power BI-skýrslur og möguleiki sjóðsstreymisspáa í Fjármálainnsýn sýna niðurstöðurnar.

Setja verður upp sjóðstreymisspá fyrir hvern lögaðila sem á að skoða spá fyrir. Farið yfir skilgreiningu sjóðstreymisspár í öllum lögaðilum. Að öðrum kosti skal fara yfir skilgreiningu allra lögaðila fyrir sjóðstreymisspá og ganga úr skugga um að þær séu rétt stilltar.

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a>Hvers vegna sýnir Power BI ekki öll sjóðstreymisgögnin?

Ljúka þarf nokkrum skrefum áður en sjóðstreymisspár geta birst í Power BI-yfirlitum. Farið yfir eftirfarandi gátlista og gangið úr skugga um að öllum skrefum sé lokið:

- Setjið upp sjóðstreymi fyrir hvern lögaðila.
- Í færibreytum fjárhags skal stilla gjaldmiðil kerfisins og gerð gengisins.
- Stillið fjárhagsbókhaldsgjaldmiðilinn og gerð gengisins.
- Færið inn gengið milli færslugjaldmiðils og bókhaldsgjaldmiðils.
- Færið inn gengið milli bókhaldsgjaldmiðils og kerfisgjaldmiðils.
- Færið inn gengið milli bókhaldsgjaldmiðils og hvers bankagjaldmiðils fyrir sig.

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a>Hvers vegna virkaði sjóðstreymi Power BI í fyrri útgáfum en er nú autt?

Gangið úr skugga um að mælingarnar „Sjóðstreymismæling V2“ og „LedgerCovLiquidityMeasurement“ úr einingaverslun hafi verið skilgreindar. Frekari upplýsingar um hvernig á að vinna með gögn í einingaverslun er að finna í [Power BI samþætting við einingaverslun](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Gangið úr skugga um að búið sé að fara í gegnum öll skrefin sem þarf að taka til að skoða Power BI-efni. Frekari upplýsingar má finna á [Yfirlit yfir reiðufé Power BI efni](Cash-Overview-Power-BI-content.md).

## <a name="have-the-entity-store-entities-been-refreshed"></a>Hafa einingar einingaverslunar verið uppfærðar?

Nauðsynlegt er að uppfæra einingarnar reglulega til að tryggja að gögnin séu uppfærð og nákvæm. Til að uppfæra handvirkt tiltekna einingu skal fara í **Kerfisstjórnun \> Uppsetning \> Einingaverslun**, velja eininguna og því næst velja **Uppfæra**. Einnig er hægt að uppfæra gögnin sjálfkrafa. Á síðunni **Einingaverslun** skal stilla valkostinn **Virkja sjálfvirka uppfærslu** á **Já**.
