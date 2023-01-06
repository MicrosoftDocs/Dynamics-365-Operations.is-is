---
title: Úrræðaleit vegna uppsetningar sjóðstreymisspár
description: Þessi grein veitir svör við spurningum sem gætu vaknað þegar verið er að skilgreina sjóðstreymisspár. Þar er svarað algengum spurningum um uppsetningu sjóðstreymis, uppfærslur á sjóðstreymi og sjóðstreymi Power BI.
author: angelad116
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 807a1da1906bdefec38954cea02ed29b0157d69e
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151402"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a>Úrræðaleit vegna uppsetningar sjóðstreymisspár

[!include [banner](../includes/banner.md)]

Þessi grein veitir svör við spurningum sem gætu vaknað þegar verið er að skilgreina sjóðstreymisspár. Þar er svarað algengum spurningum um uppsetningu sjóðstreymis, uppfærslur á sjóðstreymi og sjóðstreymi Power BI.

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

Gangið úr skugga um að mælingarnar „Sjóðstreymismæling V2“ og „LedgerCovLiquidityMeasurement“ úr einingaverslun hafi verið skilgreindar. Frekari upplýsingar um það hvernig á að vinna með gögn í einingaverslun er að finna í [Power BI samþætting við einingaverslun](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Gangið úr skugga um að búið sé að fara í gegnum öll skrefin sem þarf að taka til að skoða Power BI-efni. Frekari upplýsingar má finna á [Yfirlit yfir reiðufé Power BI efni](Cash-Overview-Power-BI-content.md).

## <a name="have-the-entity-store-entities-been-refreshed"></a>Hafa einingar einingaverslunar verið uppfærðar?

Nauðsynlegt er að uppfæra einingarnar reglulega til að tryggja að gögnin séu uppfærð og nákvæm. Til að uppfæra handvirkt tiltekna einingu skal fara í **Kerfisstjórnun \> Uppsetning \> Einingaverslun**, velja eininguna og því næst velja **Uppfæra**. Einnig er hægt að uppfæra gögnin sjálfkrafa. Á síðunni **Einingaverslun** skal stilla valkostinn **Virkja sjálfvirka uppfærslu** á **Já**.

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a>Hvaða útreikningsaðferð á að nota við útreikninga sjóðstreymisspár?

Útreikningsaðferð sjóðstreymisspár er með tvo mikilvæga valkosti. Valkosturinn **Ný** reiknar sjóðstreymisspár fyrir ný skjöl og skjöl sem hafa breyst síðan síðasta runuvinnsla var keyrð. Þessi valkostur keyrir oft hraðar því hann vinnur með minni undirmengi skjala.  **Samtala** valkosturinn mun endurreikna sjóðstreymisspár fyrir hvert skjal í kerfinu. Þessi valkostur tekur lengri tíma vegna þess að það er meiri vinna sem þarf að ljúka.

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a>Hvernig bæti ég afköst á endurtekinni runuvinnslu fyrir sjóðsstreymisspá?

Mælt er með því að sjóðstreymisspá sé keyrð á hverjum degi utan vinnutíma með því að nota **Nýja** útreikningsaðferð. Mælt er með þessari nálgun sex daga vikunnar. Svo skal keyra sjóðstreymisspá einu sinni í viku með því að nota **Samtals** útreikningsaðferðina á þeim degi sem minnst er að gera.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

