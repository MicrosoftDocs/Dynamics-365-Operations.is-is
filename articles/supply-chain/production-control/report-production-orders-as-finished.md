---
title: Skrá framleiðslupöntun sem tilbúna
description: Bóka sem tilbúið er framleiðslustig. Á þessu stigi er endanleg vara skráð og flutt úr framleiðslupöntuninni í birgðir.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: kamaybac
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 40b2856e2495d2139664b75f747f023334a80d8c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235461"
---
# <a name="report-production-orders-as-finished"></a>Skrá framleiðslupöntun sem tilbúna

[!include [banner](../includes/banner.md)]

Bóka sem tilbúið er framleiðslustig. Á þessu stigi er endanleg vara skráð og flutt úr framleiðslupöntuninni í birgðir.

Þegar magn af tilbúnum vörum er tilkynnt sem lokið á framleiðslupöntun er það uppfært í birgðunum sem á lager. Hlutar af upphaflega áætluðu pöntunarmagni geta verið tilkynntir sem lokið. Einnig er mögulegt að tilkynna villumagn með tengdri villuástæðu þegar magn er tilkynnt sem lokið. Þegar framleiðslupöntun nær stiginu Tilkynnt sem lokið gefur það til kynna að ekki á eftir að tilkynna meira magn á framleiðslupöntunina.
Eftirfarandi einkenni eru einnig tengd við ferlið **Tilkynnt sem lokið**:
-   Hægt er að setja upp notkun á hráefni og tíma sem eru í hlutfalli við tilkynnt magn (bakalosun)
-   Frágangsvinna getur verið búin til fyrir hluti sem eru virkir fyrir ferli vöruhúsa.
-   Hægt er að setja upp áætlað eða staðlað kostnaðarvirði fullkláraðra vara sem tilkynna á á fjárhagslykla.
-   Hægt er að stofna gæðapöntun fyrir skráða magnið byggt á uppsetningu gæðatengingar.

Magnið er skráð á°frálagsstaðsetningu. Vöruhúsavinna er°þá°mynduð til að flytja magn úr staðsetningu°framleiðslufrálags á lokaáfangastaður skilgreint af staðsetningarleiðbeiningar fyrir°frágangsvinnu.

-   Hægt er að stofna gæðapöntun er þegar framleiðslupöntun er tilkynnt sem tilbúin ef gæðatenging hefur verið sett upp.

## <a name="set-a-production-order-to-reporting-as-finished"></a>Stilla framleiðslupöntun sem°Tilkynnt sem lokið
Hægt er að færa framleiðslupöntun í stöðuna **Tilkynnt sem lokið** með hefðbundinni uppfærsluaðgerð framleiðslupöntunar eða með leiðar- og vinnslupjaldsbókum eða í gegnum°færslubókina **Tilkynnt sem lokið**. Einnig er hægt að uppfæra stigið í°**Tilkynnt sem lokið** gegnum síðurnar afgreiðslustöð verkspjalda og verkspjaldssíðu í tæki°í síðustu vinnslu framleiðslupöntunar. Loks er hægt að virkja valkostinn **Tilkynnt sem lokið** sem ferli fyrir vöruhúsalófatölvur.  





[!INCLUDE[footer-include](../../includes/footer-banner.md)]