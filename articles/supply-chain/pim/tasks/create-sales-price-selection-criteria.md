--- 
title: "Stofna valskilyrði fyrir söluverð"
description: "Þessi verklýsing sýnir hvernig á að stofna valskilyrði söluverðs fyrir eigindabyggð söluverðslíkön."
author: YuyuScheller
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 59f6a4131f6a27c0089a1259e3f849f91a47bc87
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-sales-price-selection-criteria"></a>Stofna valskilyrði fyrir söluverð

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna valskilyrði söluverðs fyrir eigindabyggð söluverðslíkön. Þetta ferli krefst þess að að minnsta kosti eitt afbrigðalíkan afurðar sé tiltækt. Þetta dæmi notar verðlíkanið fyrir söluverðslíkan hátalaralausnar í sýnigagnafyrirtækinu USMF. Venjulega notar framleiðslustjóri þetta ferli.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Bæta við nýju skilyrði fyrir fyrirliggjandi söluverðlíkan
1. Smellið á Skilgreining afurðarafbrigðislíkans
2. Smella á Afbrigðalíkan afurðar
3. Á listanum velurðu línuna fyrir vörulíkan hátalaralausnar, en smelltu ekki á tengilinn fyrir heiti líkans.
4. Í aðgerðasvæðinu er smellt á líkan.
5. Smelltu á Skilyrði verðlíkans.
6. Smellið á „Nýtt“.
7. Í svæðið Heiti, slærðu inn 'Customer group 10'.
    * Heiti verðlíkans er notað til að finna undirliggjandi valskilyrði.  
8. Í reitinn Verðlíkan skal slá inn eða veldu gildi.
9. Í reitnum Gerð pöntunar velurðu Sölupöntun.
    * Gerð pöntunar ákvarðar gagnagrunnsvæði sem eru tiltæk fyrir valfyrirspurn.  
10. Færa skal inn dagsetningu í svæðinu Gildir frá.
11. Í reitinn Fella úr gildi, skal færa inn dagsetningu.
12. Smellið á „Vista“.

## <a name="create-the-query-for-the-selection-criteria"></a>Búa til fyrirspurn fyrir valskilyrði
1. Smellið á „Breyta“.
2. Í reitnum Tafla skal velja Viðskiptavini. 
3. Í reitnum Reitur er valið Viðskiptamannsflokkur.
    * Í þessu dæmi notum við tiltekinn viðskiptavinaflokk fyrir valskilyrði.  
4. Í reitnum Skilyrði er valið Customer group 10. 
5. Smellið á „Í lagi“.


