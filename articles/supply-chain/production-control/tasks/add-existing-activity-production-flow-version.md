---
title: Bæta fyrirliggjandi verkþætti við útgáfu framleiðsluflæðis
description: Þegar nýjar útgáfur framleiðsluflæða eru stofnaðar, er hægt að velja að bæta við aðgerðum sem voru stofnaðar fyrir eldri útgáfur, við nýju útgáfuna.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f73274c6e102df3007793e027587793d87c4f83
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579305"
---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a>Bæta fyrirliggjandi verkþætti við útgáfu framleiðsluflæðis

[!include [banner](../../includes/banner.md)]

Þegar nýjar útgáfur framleiðsluflæða eru stofnaðar, er hægt að velja að bæta við aðgerðum sem voru stofnaðar fyrir eldri útgáfur, við nýju útgáfuna. Þessi verklýsing sýnir hvernig er ný útgáfa stofnuð fyrir fyrirliggjandi framleiðsluflæði, án þess að afrita verkþætti. Í næsta skref er fyrirliggjandi verkþáttar bætt við í nýju útgáfuna. 

Þetta verki krefst framleiðsluflæði með útgáfu og verkþætti sem þegar hafa verið stofnuð.


## <a name="create-a-new-production-flow-version"></a>Stofna nýja útgáfu framleiðsluflæðis
1. Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæði.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
4. Smella á Breyta.
5. Í listanum skal merkja valda línu.
6. Færa inn dagsetningu og tíma í dagsetningarsvæði Gildistíma.
    * Athugið að áður en stofnuð er nýja útgáfu framleiðsluflæðis, skal athuga lokadagsetningu- og tíma hinnar virku útgáfu. Ný útgáfa verður stofnuð með virka upphafsdagsetningu, sem tengist lokadagsetningu valinnar útgáfu.  
7. Smelltu á Bæta við.
8. Velja Nei fyrir í reitnum Afrita úr útgáfu.
    * Veljið Nei til að byrja auða útgáfu ef flestum verkþætti afrituðu útgáfu er skipt út fyrir nýjum verkþætti. Bæta við óbreyttum verkþætti til að bæta við núverandi aðgerðum í skjámyndinni Verkþættir handvirkt.  
9. Velja Nei í svæðinu gera eftirrit af kanban-reglum.
    * Þegar verkþættir eru ekki afritaðar í nýju útgáfuna, er ekki hægt að afrita kanban-reglur þegar verið er að stofna nýju útgáfuna.   Í staðinn muntu nota kanban-aðgerðina stofna útskiptingu síðar í skjámynd kanban-reglu, til að skipta út kanban-reglum hinnar gömlu útgáfu framleiðsluflæðis með kanban-reglum með því að nota aðgerðir hinnar nýju útgáfu.  
10. Smellið á „Í lagi“.
11. Í listanum skal finna og velja þá skráningu sem óskað er eftir.

## <a name="add-an-existing-activity"></a>Bæta við fyrirliggjandi verkþætti.
1. Smellt er á Verkþætti.
2. Smelltu á Bæta við núverandi til að opna felligluggann.
    * Finndu og veldu fyrirliggjandi verkþátt til að bæta við nýju útgáfu framleiðsluflæðis.  Athugið að listinn sýnir alla verkþætti sem hafa verið stofnaðar fyrir þessa framleiðsluflæði fyrir allar eldri útgáfur flæðis.  
3. Í reitinn verkþáttur skal slá inn eða velja gildi.
4. Smellið á „Í lagi“.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]