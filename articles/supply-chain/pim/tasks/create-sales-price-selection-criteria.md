---
title: Stofna valskilyrði fyrir söluverð
description: Þessi verklýsing sýnir hvernig á að stofna valskilyrði söluverðs fyrir eigindabyggð söluverðslíkön.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60a7c7230d4eb57d840121f6ee490bf829e0dc8f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999657"
---
# <a name="create-sales-price-selection-criteria"></a>Stofna valskilyrði fyrir söluverð

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að stofna valskilyrði söluverðs fyrir eigindabyggð söluverðslíkön. Þetta ferli krefst þess að að minnsta kosti eitt afbrigðalíkan afurðar sé tiltækt. Þetta dæmi notar verðlíkanið fyrir söluverðslíkan hátalaralausnar í sýnigagnafyrirtækinu USMF. Venjulega notar framleiðslustjóri þetta ferli.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Bæta við nýju skilyrði fyrir fyrirliggjandi söluverðlíkan
1. Smellið á Skilgreining afurðarafbrigðislíkans
2. Smella á Afbrigðalíkan afurðar
3. Á listanum velurðu línuna fyrir vörulíkan hátalaralausnar, en smelltu ekki á tengilinn fyrir heiti líkans.
4. Í aðgerðasvæðinu er smellt á líkan.
5. Smelltu á Skilyrði verðlíkans.
6. Smellið á Nýtt.
7. Í reitinn Heiti, slærðu inn „Customer group 10”.
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

