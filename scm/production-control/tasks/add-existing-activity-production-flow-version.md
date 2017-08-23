--- 
title: "Bæta fyrirliggjandi verkþætti við útgáfu framleiðsluflæðis"
description: "Þegar nýjar útgáfur framleiðsluflæða eru stofnaðar, er hægt að velja að bæta við aðgerðum sem voru stofnaðar fyrir eldri útgáfur, við nýju útgáfuna."
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 2708ae5d7e2601fa8d86367470e196d4b2503c01
ms.contentlocale: is-is
ms.lasthandoff: 07/28/2017

---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a>Bæta fyrirliggjandi verkþætti við útgáfu framleiðsluflæðis

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


