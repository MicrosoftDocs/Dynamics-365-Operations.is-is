---
title: Setja upp komuyfirlitsreglu fyrir vöru
description: Þessi grein fjallar um uppsetningu yfirlitsprófíls fyrir komu.
author: yufeihuang
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8517710f5d0be1859f86449152712d950281769a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872008"
---
# <a name="set-up-an-item-arrival-overview-profile"></a>Setja upp komuyfirlitsreglu fyrir vöru

[!include [banner](../../includes/banner.md)]

Þessi grein fjallar um uppsetningu yfirlitsprófíls fyrir komu. Komuyfirlitsreglu er safn reglna sem verður notað þegar síðan Komuyfirlit er opnað af notanda. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF. Þetta verk myndi venjulega vera framkvæmt af starfsmanni í móttöku.

1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Birgðastýring > Uppsetning > Dreifing > Komuyfirlitsreglur**.
2. Veljið **Nýtt**. Þar er þú vinnur nánast alltaf í sama vöruhús við hlaða af fullhlöðnum vörubíl , ætti að stofna komuyfirlitsregla til að auðvelda ferlið við að skrá mótteknar vörur.  
3. Í reitinn **Heiti komuyfirlitsreglu** skal færa inn gildi.
4. Í reitnum **Sýna línur** skal velja valkost. Veldu hvaða línur á að sýna fyrir innhreyfingarnar:  

    - **Allt** – Sýna allar línur óháð stöðu.   
    - **Í vinnslu** – Sýna línur fyrir innhreyfingar þar sem vinnslu er Lokið eða lokið að Hluta. Það þýðir að fyrir hverja línu hefur annaðhvort fullt magn eða hluti magns verið skráð í komubók.   
    - **Ekki lokið** – Sýna línur fyrir innhreyfingar þar sem vinnslustaða er Ekkert eða að Hluta. Þetta þýðir að ekkert magn eða aðeins hluti þess hefur verið skráður í komubók, fyrir hverja línu.  

5. Útvíkkaðu eða dragðu samann hlutann **Komutímavalkostir**.
6. Í reitinn **Dagar frá og með** skal slá inn gildi. Þetta stillir síu til að sýna línur innhreyfingar sem búist við að taka á móti innan nokkra daga (eftir því hvaða númer sett).  
7. Í reitinn **Dagar aftur í tímann** skal slá inn gildi. Þetta stillir síu til að sýna innhreyfingarlínur sem búist við að tekið sé á móti nokkrum dögum fyrir daginn í dag.  
8. Í reitinn **Vöruhús** skal slá inn gildi. Sía á eina eða fleiri vöruhúsum.  
9. Í reitnum **Afhendingarmáti** skal færa inn gildi. Þetta stillir síu til að sýna aðeins innhreyfingarlínur með þennan Afhendingarmáta.  
10. Í reitinn **Nafn** skal velja WHS.
11. Í reitnum **Vöruhús** skal velja vöruhús 24. Þetta er sjálfgefið vöruhús sem verður notað fyrir skráð innhreyfingarlínur sem nota þessa forstillingu.  
12. Í reitnum **Staðsetning** skal velja **Afgreiðsluhurð**. Þetta er sjálfgefið staðsetning sem verður notað fyrir skráð innhreyfingarlínur sem nota þessa forstillingu.  
13. Útvíkkaðu eða felldu saman hlutann **Upplýsingar um komufyrirspurn**.
14. Í reitnum **Takmarka við svæði** velurðu svæði 2. Þetta stillir síu til að sýna aðeins innhreyfingarlínur með þennan Stað.  
15. Stilltu valkostinn **Innkaupapantanir** á **Já**. Veljið innhreyfingarlínur úr innkaupapöntunum.  
16. Stilltu valkostinn **Flytja** pantanir á **Já**. Veljið innhreyfingarlínur úr flutningspöntun.  
17. Veljið **Vista**.
18. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
