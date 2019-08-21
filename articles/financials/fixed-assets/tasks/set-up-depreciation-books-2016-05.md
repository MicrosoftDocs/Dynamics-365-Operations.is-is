---
title: Setja upp afskriftabók (maí 2016)
description: Þessi leiðarvísi fyrir verk stofna nýja afskriftabók og tengja hana við eignaflokk.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6840e211847494598a81cd3228dbd3796447e18c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839858"
---
# <a name="set-up-depreciation-books-may-2016"></a>Setja upp afskriftabók (maí 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi leiðarvísi fyrir verk stofna nýja afskriftabók og tengja hana við eignaflokk.  Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.


## <a name="create-a-depreciation-book"></a>Stofna afskriftarbók
1. Fara í Eignir > Uppsetning > Afskriftarbækur.
2. Smellið á „Nýtt“.
3. Færa inn gildi í svæðinu afskriftarbók.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Merkja eða afmerkja gátreit Reikna afskrift.
6. Í reitnum afskriftarregla skal smella á fellilistahnappinn til að opna leitina.
7. Í listanum skal finna og velja þá afskriftarregla sem óskað er eftir.
8. Í listanum skal smella á tengilinn í valinni línu.
9. Í reitnum önnur afskriftarregla skal smella á fellilistahnappinn til að opna leitina.
10. Á listanum, skal velja viðeigandi afskriftarregla.
11. Í listanum skal smella á tengilinn í valinni línu.
    * Óregluleg afskriftaregla er notuð fyrir aukalega afskrift af eign við óvenjulegar aðstæður. Til dæmis er hægt að nota þetta til að skrá niðurstöður úr náttúruhamfarir afskrift.  
12. Merkja eða afmerkja gátreit Stofna afskriftaleiðréttingar með grunnleiðréttingar .
13. Í reitnum dagatal skal smella á fellilistahnappinn til að opna leitina.
14. Í listanum skal smella á tengilinn í valinni línu.

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a>Tengið afskriftarbók við eignaflokkur
1. Smella á eignaflokkar.
2. Í reitnum eignaflokkur skal smella á fellilistahnappinn til að opna leitina.
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Veljið valkost í svæðinu afskriftarregla.
6. Í reitinn líftími skal slá inn númer.
    * Sjáðu að svæðisgildi afskriftartímabils er reiknaður eftir uppsetningu líftíma.  

