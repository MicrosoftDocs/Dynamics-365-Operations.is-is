---
title: Setja upp reglur fyrir stigveldi innkaupategunda
description: Notið þetta ferli til að setja upp reglur til þess að panta afurðir í tegund.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1fdf357466de12bd0188fc43cd266c67af762c7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569915"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Setja upp reglur fyrir stigveldi innkaupategunda

[!include [task guide banner](../../includes/task-guide-banner.md)]

Notið þetta ferli til að setja upp reglur til þess að panta afurðir í tegund. Þessar reglur eru skilgreindar fyrir tiltekna innkaupastefnu. Regla tegundaraðgangs ákvarðar hvaða innkaupategundir starfsmenn hafa aðgang að þegar þeir stofna beiðnir. Þegar beiðni er stofnuð skal innkaupastefnu og reglu tegundaraðgangs sem á að nota vera ákvörðuð af lögaðilanum og rekstrareiningum sem starfsmaðurinn tilheyrir. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF. Þetta verk myndi venjulega vera framkvæmt af innkaupaaðila.


## <a name="find-the-procurement-policy"></a>Finna innkaupareglu
1. Fara í Innkaup og uppruni > Uppsetning > reglur > innkaupareglur.
2. Smelltu á tengil á innkaupastefnu USMF-stefna.
    * Þetta er reglan sem þú bætir reglu við. Hún verður að vera Virk regla.  

## <a name="create-a-category-access-rule"></a>Búa til reglu tegundaraðgangs
1. Veldu Stefnuregla tegundaraðgangs
    * Ef hnappur til að stofna stefnureglu er deyfður er það vegna þess að þegar er til staðar virk stefnuregla fyrir tegundaraðgang. Athuga dagsetningasvæði Virkrar dagsetningar og Lokadags til að ákvarða hvaða það er, svo velja hana og smella á hætta Við stefnureglu. Ef Stofna stefnureglu hnappur er tiltækur, þarf ekki að gera neitt.  
2. Smellt er á Stofna stefnureglu.
3. Færa inn dagsetningu og tíma í svæðinu gildisdagsetningu.
    * Tíminn má ekki skarast við aðra reglu sem er þegar virk.  
    * Velja tegund sem reglan mun eiga við. Taka niður athugasemd um það hvaða tegund þetta er – þú þarf hana síðar. Þegar flokkur er valinn, eru yfirflokkar eða yfirflokkur einnig settir á valinn tegundaalista.  
    * Viljirðu að reglan eigi við allar undirtegundir valinnar tegundar, Velja Innifela undirtegundir valkostinn.  
4. Smelltu á Bæta við.
    * Ef þú stillir valkostinn yfirskipuð regla á Já, er Stefnureglun sem skilgreind er fyrir yfirtegund er einnig úthlutað til baka í undirtegundir ef engin stefnuregla hefur verið skilgreind fyrir undirtegundir.  
5. Smellið á „Í lagi“.

## <a name="create-a-category-policy-rule"></a>Búa til tegundarstefnureglu
1. Veldu Stefnuregla tegundar
    * Ef hnappinn Stofna stefnureglu er deyfður, skal velja virka stefnureglu og smella á hætta Við stefnureglu.  
2. Smellt er á Stofna stefnureglu.
3. Færa inn dagsetningu og tíma í svæðinu gildisdagsetningu.
4. Smelltu á Bæta við.
5. Veljið sömu tegund sem notuð var fyrir reglu tegundaraðgangs.
6. Í reitnum Velja lánardrottin, skal velja valkost.
    * Velja reglu til að stjórna hvers konar lánardrottna má velja fyrir flokkinn þegar beiðnir eru stofnaðar.  
7. Smellið á „Loka“.
    * Þær stefnureglur sem skilgreindar hafa verið hafaverið fyrir beiðnir af gerðinni notkun. Ef óskað er að skilgreina reglur fyrir beiðnir af gerðinni Áfylling, myndirðu stofna regla fyrir stefnureglugerð sem kallast "Stefnuregla tegundaraðgangs fyrir áfyllingu".  

