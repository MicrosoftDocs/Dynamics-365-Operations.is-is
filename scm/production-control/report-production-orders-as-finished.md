---
title: "Skýrslan framleiðslupantanir sem lokið"
description: "Tilkynna tilbúið er framleiðslustig. Á þessu stigi endanlegrar vöru er skráð og fluttar úr framleiðslupöntuninni í birgðir."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 19a777a8e58e3c8b848e878956b457a4a730f6e2
ms.lasthandoff: 03/31/2017


---

# <a name="report-production-orders-as-finished"></a>Skýrslan framleiðslupantanir sem lokið

Tilkynna tilbúið er framleiðslustig. Á þessu stigi endanlegrar vöru er skráð og fluttar úr framleiðslupöntuninni í birgðir.

Þegar magn af tilbúnum vörum er tilkynnt sem lokið á framleiðslupöntun er það uppfært í birgðunum sem á lager. Hlutar af upphaflega áætluðu pöntunarmagni geta verið tilkynntir sem lokið. Einnig er mögulegt að tilkynna villumagn með tengdri villuástæðu þegar magn er tilkynnt sem lokið. Þegar framleiðslupöntun nær stiginu Tilkynnt sem lokið gefur það til kynna að ekki á eftir að tilkynna meira magn á framleiðslupöntunina.
Eftirfarandi einkenni eru einnig tengd við ferlið **Tilkynnt sem lokið**:
-   Hægt er að setja upp notkun á hráefni og tíma sem eru í hlutfalli við tilkynnt magn (bakalosun)
-   Frágangsvinna getur verið búin til fyrir hluti sem eru virkir fyrir ferli vöruhúsa.
-   Hægt er að setja upp áætlað eða staðlað kostnaðarvirði fullkláraðra vara sem tilkynna á á fjárhagslykla.
-   Hægt er að stofna gæðapöntun fyrir skráða magnið byggt á uppsetningu gæðatengingar.

Magnið er skráð á°frálagsstaðsetningu. Vöruhúsavinna er°þá°mynduð til að flytja magn úr staðsetningu°framleiðslufrálags á lokaáfangastaður skilgreint af staðsetningarleiðbeiningar fyrir°frágangsvinnu.

-   Hægt er að stofna gæðapöntun er þegar framleiðslupöntun er tilkynnt sem tilbúin ef gæðatenging hefur verið sett upp.

## <a name="set-a-production-order-to-reporting-as-finished"></a>Stilla framleiðslupöntun sem°Tilkynnt sem lokið
Hægt er að færa framleiðslupöntun í stöðuna **Tilkynnt sem lokið**með hefðbundinni uppfærsluaðgerð framleiðslupöntunar eða með leiðar- og vinnslupjaldsbókum eða í gegnum°færslubókina **Tilkynnt sem lokið**. Einnig er hægt að uppfæra stigið í°**Tilkynnt sem lokið** gegnum síðurnar afgreiðslustöð verkspjalda og verkspjaldssíðu í tæki°í síðustu vinnslu framleiðslupöntunar. Loks er hægt að virkja valkostinn **Tilkynnt sem lokið** sem ferli fyrir vöruhúsalófatölvur.  


