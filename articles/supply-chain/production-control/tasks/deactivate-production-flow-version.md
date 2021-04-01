---
title: Gera útgáfu framleiðsluflæðis óvirka
description: Þegar virkrar framleiðsluflæðisútgáfu er ekki lengur þörf er hægt að afvirkja hana.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b062bcab17a708be0cd40f2cc6451707d6993a4b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257340"
---
# <a name="deactivate-a-production-flow-version"></a>Gera útgáfu framleiðsluflæðis óvirka

[!include [banner](../../includes/banner.md)]

Þegar virkrar framleiðsluflæðisútgáfu er ekki lengur þörf er hægt að afvirkja hana. Aðeins ætti að nota þennan valkost ef öllum kanban-reglum og verkþáttum hefur verið lokið og ekki verður gert virkt aftur. Athugið að lokadagsetning allra kanban-reglna sem tengjast þessari útgáfu framleiðsluflæðis verður uppfærð með núverandi dagsetningu og tími. 

Til að breyta virkri útgáfu framleiðsluflæðis skaltu íhuga að stilla lokadag fyrir virka útgáfu og búa til nýja útgáfu. Þetta leyfir að haldið sé áfram framleiðslaðgerðum við undirbúning á nýrri útgáfu og tengdum kanban-reglum. 

Til að fella virka framleiðsluflæðisútgáfu úr gildi þarf að setja inn lokadag. Í þeim skilningi er afvirkjun frekar undantekning en regla. 

Fyrir þetta ferli þarf framleiðsluflæði með útgáfu sem hægt er að gera óvirka. Reyndu þetta ekki í framleiðsluumhverfi nema þú sért 100% viss um að útgáfan sé alveg úrelt.


## <a name="deactivate-a-production-flow-version"></a>Gera útgáfu framleiðsluflæðis óvirka
1. Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæði.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Smellið á Afvirkja.
    * Ekki halda áfram ef notandi er ekki 100% viss um að þessi útgáfa framleiðsluflæðis sé úrelt. Með því að smella á í Lagi renna allar virkar kanban-reglur út og allar aðgerðir framleiðslu og áfyllingar stöðvast tafarlaust af þessari útgáfu framleiðsluflæðis.  
6. Smellið á „Í lagi“.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]