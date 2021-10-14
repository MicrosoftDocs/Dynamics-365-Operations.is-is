---
title: Setja upp reglur fyrir stigveldi innkaupategunda
description: Notið þetta ferli til að setja upp reglur til þess að panta afurðir í tegund.
author: Henrikan
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee056d7c2a8bdc9bcd2f5a0f4b96a7bf69c8c862
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577097"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Setja upp reglur fyrir stigveldi innkaupategunda

[!include [banner](../../includes/banner.md)]

Notið þetta ferli til að setja upp reglur til þess að panta afurðir í tegund. Þessar reglur eru skilgreindar fyrir tiltekna innkaupastefnu. Regla tegundaraðgangs ákvarðar hvaða innkaupategundir starfsmenn hafa aðgang að þegar þeir stofna beiðnir. Þegar beiðni er stofnuð skal innkaupastefnu og reglu tegundaraðgangs sem á að nota vera ákvörðuð af lögaðilanum og rekstrareiningum sem starfsmaðurinn tilheyrir. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF. Þetta verk myndi venjulega vera framkvæmt af innkaupaaðila.


## <a name="find-the-procurement-policy"></a>Finna innkaupareglu
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Innkaup og aðföng > Uppsetning > Reglur > Innkaupareglur**.
2. Smelltu á tengil á innkaupastefnu USMF-stefna. Þetta er reglan sem þú bætir reglu við. Hún verður að vera Virk regla.  

## <a name="create-a-category-access-rule"></a>Búa til reglu tegundaraðgangs
1. Stækka flýtiflipann **Sefnuregla**.
2. Í **Gerð stefnureglu** lista, veldu **Regla um aðgang að flokkum**. Ef hnappurinn **Stofna stefnureglu** er deyfður er það vegna þess að þegar er til staðar virk stefnuregla fyrir tegundaraðgang. Athuga reitina **Virkt** og **Gildislok** til að ákvarða hvaða það er, svo velja hana og smella á **hætta Við stefnureglu**. Ef **Stofna stefnureglu** hnappur er tiltækur, þarf ekki að gera neitt.  
3. Smelltu á **Stofna stefnureglu**.
4. Í retinum **Gildisdagsetningu** færirðu inn dagsetningu og tíma. Tíminn má ekki skarast við aðra reglu sem er þegar virk.  
5. Velja tegund sem reglan mun eiga við. Taka niður athugasemd um það hvaða tegund þetta er – þú þarf hana síðar. Þegar flokkur er valinn, eru yfirflokkar eða yfirflokkur einnig settir á valinn tegundaalista. Viljirðu að reglan eigi við allar undirtegundir valinnar tegundar, Velja **Innifela undirtegundir** valkostinn.
6. Smelltu á hægri örina til að bæta við **Valdir flokkar** lista.  
4. Smellt er á **OK**. Ef þú stillir valkostinn **Innifela yfirregla** á Já, er Stefnureglun sem skilgreind er fyrir yfirtegund er einnig úthlutað til baka í undirtegundir ef engin stefnuregla hefur verið skilgreind fyrir undirtegundir.

## <a name="create-a-category-policy-rule"></a>Búa til tegundarstefnureglu
1. Í listanum **Gerð stefnureglu** veldu **Stefnuregla tegunda**. Ef hnappinn **Stofna stefnureglu** er deyfður, skal velja virka stefnureglu og smella á **hætta Við stefnureglu**.  
2. Smelltu á **Stofna stefnureglu**.
3. Í retinum **Gildisdagsetningu** færirðu inn dagsetningu og tíma.
4. Smelltu á **Bæta við**.
5. Í reitnum **Flokkur** skal velja sama flokk og var notaður fyrir **reglu tegundaraðgangs**.
6. Í reitnum **Velja lánardrottinn** skal velja valkost. Velja reglu til að stjórna hvers konar lánardrottna má velja fyrir flokkinn þegar beiðnir eru stofnaðar.  
7. Smellið á **Loka**. Þær stefnureglur sem skilgreindar hafa verið hafaverið fyrir beiðnir af gerðinni notkun. Ef óskað er að skilgreina reglur fyrir beiðnir af gerðinni Áfylling, myndirðu stofna regla fyrir stefnureglugerð sem kallast „Stefnuregla tegundaraðgangs fyrir áfyllingu”.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]