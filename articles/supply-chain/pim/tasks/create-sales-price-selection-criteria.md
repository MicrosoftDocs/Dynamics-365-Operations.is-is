---
title: Stofna valskilyrði fyrir söluverð
description: Þessi verklýsing sýnir hvernig á að stofna valskilyrði söluverðs fyrir eigindabyggð söluverðslíkön.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47ea7ea2093c540a88d9fd7249b470009c7595d40e2a727d8fcd3bb4b5d74bac
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750077"
---
# <a name="create-sales-price-selection-criteria"></a>Stofna valskilyrði fyrir söluverð

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að stofna valskilyrði söluverðs fyrir eigindabyggð söluverðslíkön. Þetta ferli krefst þess að að minnsta kosti eitt afbrigðalíkan afurðar sé tiltækt. Þetta dæmi notar verðlíkanið fyrir söluverðslíkan hátalaralausnar í sýnigagnafyrirtækinu USMF. Venjulega notar framleiðslustjóri þetta ferli.

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Bæta við nýju skilyrði fyrir fyrirliggjandi söluverðlíkan

1. Farið í **Afurðarupplýsingastjórnun \> Afurðir \> Afbrigðalíkön afurða**.
1. Á listanum velurðu línuna fyrir vörulíkan hátalaralausnar, en smelltu ekki á tengilinn fyrir heiti líkans.
1. Í aðgerðarúðunni skal velja **Tegund**.
1. Veljið **Skilyrði verðlíkans.**
1. Veljið **Nýtt**.
1. Í svæðið **Heiti**, slærðu inn Viðskiptavinaflokkur 10.
    * Heiti verðlíkans er notað til að finna undirliggjandi valskilyrði.  
1. Í reitinn **Verðlíkan** skal slá inn eða veldu gildi.
1. Í reitnum **Gerð pöntunar** velurðu *Sölupöntun*.
    * Gerð pöntunar ákvarðar gagnagrunnsvæði sem eru tiltæk fyrir valfyrirspurn.  
1. Færa skal inn dagsetningu í svæðinu **Gildir frá**.
1. Í reitinn **Fella úr gildi**, skal færa inn dagsetningu.
1. Veljið **Vista**.

## <a name="create-the-query-for-the-selection-criteria"></a>Búa til fyrirspurn fyrir valskilyrði

1. Veljið **Breyta**.
2. Í reitnum **Tafla** skal velja *Viðskiptavinir*.
3. Í reitnum **Reitur** er valið *Viðskiptavinaflokkur*.
    * Í þessu dæmi notum við tiltekinn viðskiptavinaflokk fyrir valskilyrði.  
4. Í reitnum **Skilyrði** er valið *Viðskiptavinaflokkur 10*.
5. Veljið **Í lagi**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]