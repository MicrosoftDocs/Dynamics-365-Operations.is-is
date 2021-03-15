---
title: Uppsetning afskriftabóka
description: Þessi aðferð gengur í gegnum ferlið við að búa til nýja afskriftabók og tengja hana við fastafjárhóp.
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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e1d934bffd0a5daacf27fcd5a2e00043fe3daf8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009219"
---
# <a name="set-up-depreciation-books"></a>Uppsetning afskriftabóka 

[!include [banner](../../includes/banner.md)]

Þessi aðferð gengur í gegnum ferlið við að búa til nýja afskriftabók og tengja hana við fastafjárhóp. 

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]