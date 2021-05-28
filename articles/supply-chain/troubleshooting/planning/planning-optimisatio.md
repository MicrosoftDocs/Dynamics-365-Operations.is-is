---
title: Áætluð innkaupapöntun er stofnuð þegar innkaup eru til innan neikvæðra daga
description: Ef tryggingarkóðinn er lágmark/hámark býr Planning Optimization til innkaupatillögu þegar innkaup eru til innan neikvæðra daga.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026615"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a>Áætluð innkaupapöntun er stofnuð þegar innkaup eru til innan neikvæðra daga

KB númer: 4614298

## <a name="symptoms"></a>Einkenni

Ef tryggingarkóðinn er *Lágmark/hámark* býr Planning Optimization til áætlaða innkaupatillögu þegar innkaup eru til innan neikvæðra daga.

## <a name="resolution"></a>Upplausn

Fínstilling áætlanagerðar styður ekki neikvæða daga. Hins vegar er ávallt tryggt að fyrirhugaðar pantanir séu ekki áætlaðar innan afhendingartíma miðað við núgildandi dagsetningu. Til dæmis er afhendingartími innkaupa 10 dagar og innkaupapöntun er væntanleg átta dögum frá deginum í dag. Í þessu tilfelli verður innkaupapöntunin notuð sem framboð fyrir eftirspurn sem er fimm dagar frá deginum í dag.

Þess vegna er mælt með því að afhendingartímum sé breytt þannig að þeir nái yfir allar (eða nánast allar) sviðsmyndirnar.
