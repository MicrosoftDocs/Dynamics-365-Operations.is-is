---
title: "Aðferð við heildarúthlutun kostnaðar"
description: "Þessi grein veitir leiðbeiningar fyrir notkun á Heildarúthlutun kostnaðar (TCA). Heildarúthlutun kostnaðar er aðferð til að reikna kostnað á milli mælieiningar aðalformúluvöru fyrir runupöntun og aukaafurða sem skilgreindar eru fyrir formúluna."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConsistOf, PmfFormulaCoBy
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 83852
ms.assetid: 7c14c3e5-9476-4a79-a210-e77fc91cc7fc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c26dcc5a8caa461bce90f931bb5c584f1816526b
ms.lasthandoff: 03/31/2017


---

# <a name="total-cost-allocation-method"></a>Aðferð við heildarúthlutun kostnaðar

Þessi grein veitir leiðbeiningar fyrir notkun á Heildarúthlutun kostnaðar (TCA). Heildarúthlutun kostnaðar er aðferð til að reikna kostnað á milli mælieiningar aðalformúluvöru fyrir runupöntun og aukaafurða sem skilgreindar eru fyrir formúluna.

Heildarúthlutun kostnaðar (TCA) er aðferð til að reikna kostnað á milli mælieiningar aðalformúluvöru fyrir runupöntun og aukaafurða sem skilgreindar eru fyrir formúluna. Þessi aðferð er breytileg. Hún reiknar kostnað sem vegið meðaltal milli magnsins sem tilkynnt er sem tilbúnið fyrir formúluvöruna og aukaafurða. Þegar heildarúthlutun kostnaðar er notuð þarf ekki að endurskoða kostnaðarúthlutun fyrir hverja runupöntun. Ef heildarúthlutun kostnaðar er ekki notuð, notar formúluútreikningurinn fyrirliggjandi aðgerðir.

## <a name="using-tca-for-coproducts"></a>Notkun heildarúthlutunar kostnaðar fyrir aukaafurðir
Hér eru nokkrar leiðbeiningar fyrir notkun heildarúthlutunar kostnaðar fyrir aukaafurðir:

-   Ef sleðinn **Heildarúthlutun kostnaðar** er stilltur á **Já** fyrir formúluútgáfu,verða aukaafurðir að hafa kostnaðarverð sem er meira en 0 (núll). Hægt er að sækja virði úr virku kostnaðarútgáfunni fyrir sama svæði, eða fyrir fyrsta svæði formúlu sem er ekki staðarsértæk. Þetta skilyrði er sannprófað þegar formúla er samþykkt.
-   Ef sleðinn **Heildarúthlutun kostnaðar** er stilltur á **Já** fyrir formúluútgáfuna og eftirfarandi skilyrði eru uppfyllt, verður aðferð kostnaðarúthlutunar **Heildarúthlutun kostnaðar**, og hlutfall kostnaðarúthlutunar óbreytt:
    -   Aukaafurðum var bætt við.
    -   Önnur gerð kostnaðarúthlutunar var notuð fyrir aukaafurðir.
-   Ef sleðinn**Heildarúthlutun kostnaðar** er stilltur á **Nei** fyrir formúluútgáfuna og eftirfarandi skilyrði eru uppfyllt, er aðferð kostnaðarúthlutunar breytt í **Handvirkt**, og hlutfall kostnaðarúthlutunar er óbreytt:
    -   Aukaafurðum var bætt við.
    -   Hlutfall kostnaðarúthlutunar er meira en 0 (núll).
-   Áður en hægt er á árangursríkan hátt að framkvæma formúluútreikninga, verður að áætla prósentu kostnaðarúthlutunar. Hægt er að ljúka þessu skrefi handvirkt eða með því að nota **Meta kostnað** valkostinn á síðunni **Aukaafurðir**. **Athugasemd:** Valkosturinn **Meta kostnað** er aðeins tiltækur þegar sleðinn **Heildarúthlutun kostnaðar ** er stilltur á **Já** fyrir formúluútgáfuna. Hægt er að skoða væntanlega úthlutun ef magn runupöntunar sem er skráð sem lokið samsvarar magni sem birtist í formúlunni.
-   Þegar runupöntun er stofnuð handvirkt eða áætluð runupöntun er staðfest, verður gildið á sleðanum **Heildarúthlutun kostnaðar** fyrir formúluútgáfuna afritað í runupöntunina. Hins vegar er hægt að breyta þessari stillingu í runupöntuninni. Ef sleðinn **Heildarúthlutun kostnaðar** er stilltur á **Nei** fyrir formúluútgáfuna og síðan breytt í **Já** fyrir runupöntun, er aðferð kostnaðarúthlutunar fyrir hverja línu sem var stillt á **Handvirkt** breytt í **Heildarúthlutun kostnaðar**. Kostnaðarúthlutunin **Ekkert** er óbreytt. Ef sleðinn **Heildarúthlutun kostnaðar** er stilltur á **Já** fyrir formúluútgáfuna og síðan breytt í **Nei** fyrir runupöntun, er aðferð kostnaðarúthlutunar fyrir hverja aukaafurð af gerðinni **Framleiðsla** breytt í **Handvirkt**. Allt metið hlutfall kostnaðarúthlutunar er óbreytt.
-   Síðan **Kostnaðarúthlutun aukaafurðar** sýnir reiknað hlutfall kostnaðarúthlutunar. Hægt er að opna þessa síðu af síðunni **Runupöntun**. Þessar upplýsingar eru gagnlegar þegar skráðar afurðir og magn er frábrugðið áætluðu magni eða magni sem er komið af stað í runupöntuninni. Þegar kostnaði er lokið, eru þessar nýju hlutfallsúthlutanir úr Heildarúthlutun kostnaðar sýndar á síðunni **Kostnaðarúthlutun aukaafurðar**.

## <a name="calculating-the-burden-for-byproducts"></a>Reikna álag fyrir hliðarafurðir
Á svæðinu **Kostnaðarúthlutun hliðarafurðar** á síðunni **Aukaafurðir** er tölusett svæði sem er aðeins notað fyrir hliðarafurðir. Fyrir aukaafurðir er gildi þessa svæðis alltaf **Ekkert**. Fyrir línur hliðarafurða ákvarðar þetta svæði hvernig kostnaðarupphæð línu hliðarafurða er bætt við heildarkostnað framleiðslu. Eftirtaldir valkostir eru í boði:

-   **Ekkert** ─ Engri upphæð er bætt við heildarkostnað framleiðslu fyrir þessa línu hliðarafurða.
-   **Prósent** ─ Kostnaðarupphæðin er reiknuð sem prósenta af heildarkostnaði hráefnis sem er notað í framleiðslunni. Prósentugildi sem nota á við útreikning er slegið inn í svæðið.
-   **Á röð** ─ Kostnaðarupphæðin er reiknuð sem upphæð á staðlaða runustærð framleiðslupöntunar. Þessi upphæð er óháð skráðu magni í framleiðslunni. Upphæðin sem nota á við útreikning er slegin inn í svæðið.
-   **Á magn** ─ Kostnaðarupphæðin er reiknuð sem upphæð á skráð magn formúluvöru í framleiðslu. Upphæðin sem nota á við útreikning er slegin inn í svæðið.



