---
title: Leiðrétta birgðastöðu í vöruhúsi (grunnvöruhús)
description: Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun birgðaleiðréttingabók til að leiðrétta geymslustig afurða í vöruhúsið.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d91c8901a4ff7df8ae6c3d9b98024db57e29f15b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209540"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a>Leiðrétta birgðastöðu í vöruhúsi (grunnvöruhús)

[!include [banner](../../includes/banner.md)]

Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun birgðaleiðréttingabók til að leiðrétta geymslustig afurða í vöruhúsið. Þú þarft að hafa með heiti birgðabókarinnar sett upp fyrir leiðréttingar á birgðum áður en þetta er hafið. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn. Þessi verkefni eru venjulega framkvæmd af starfsmanni í vöruhúsi.


## <a name="create-an-inventory-adjustment-journal"></a>Stofna heiti færslubóka fyrir birgðaleiðréttingu
1. Fara í Birgðastjórnun > Færslubókarfærslur > Vörur > Birgðaleiðrétting.
2. Smellið á „Nýtt“.
3. Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.
4. Á listanum smellirðu á heiti færslubókar fyrir birgðaleiðréttingu sem á að nota.
    * Sumir aðrir reitir verða fylltir út samkvæmt uppsetningu heitis færslubókar birgðaleiðréttingar sem var valið.  
5. Smellið á „Í lagi“.

## <a name="create-journal-lines"></a>Stofna færslubókarlínur
1. Smellið á „Nýtt“.
2. Í listanum merkirðu við reitinn Vörunúmer.
3. Í reitnum Vörunúmer velurðu vöru. Ef verið er að nota sýnigagnafyrirtækið USMF skal slá inn 'D0001'.
4. Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.
5. Í listanum velurðu Svæði.
6. Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.
7. Í listanum velurðu Vöruhús.
    * Ef þú hefur valið vöru með Staðsetningu sem áskilda vídd þarftu að tilgreina staðsetninguna hér.  
8. Færið inn númer í reitnum „Magn“.
    * Reiturinn Kostnaðarverð tilgreinir einingarkostnað fyrir innhreyfingar birgða. Ef kostnaður er ekki tilgreindur fyrir vörunúmer eða ef þú vildir breyta því handvirkt þá er það gert hér.  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a>Sannprófa og bóka færslubók fyrir leiðréttingu á birgðaskrá
1. Smella á Villuleita.
2. Smellið á „Í lagi“.
3. Smellið á „Bóka“.
    * Þegar þessi gerð færslubókar er bókuð er innhreyfing birgða eða vandamál bókað, birgðastigi og gildi er breytt og fjárhagsfærslur eru myndaðar.  
4. Smellið á „Í lagi“.
5. Lokaðu skjámyndinni.
6. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]