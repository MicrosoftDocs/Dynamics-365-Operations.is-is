--- 
title: " Stofna afurðapakka fyrir innkaupapantanir"
description: "Þetta ferli fer í gegnum stofna Umbúðir afurðar og nota það í innkaupapöntun."
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 9d3ea8702c79d8aa6bb7cf7caa922277697610fa
ms.contentlocale: is-is
ms.lasthandoff: 11/14/2017

---
# <a name="create-product-packages-for-purchase-orders"></a> Stofna afurðapakka fyrir innkaupapantanir

[!include[task guide banner](../includes/task-guide-banner.md)]

Þetta ferli fer í gegnum stofna Umbúðir afurðar og nota það í innkaupapöntun. Innkaupapöntun verður notuð til að stofna pöntun fyrir fyrirfram skilgreindan afurðasett. Þessi aðferð notar USRT sýnigögn fyrirtækisins.


## <a name="create-a-product-package"></a>Stofna umbúðir vöru
1. Fara í Smásölu og viðskipti > Birgðastjórnun > Áfylling > Umbúðir afurðar.
2. Smellið á „Nýtt“.
3. Færa inn gildi í reitnum númer umbúða.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal smella á tengilinn í valinni línu.
7. Smelltu á Bæta við.
8. Í svæðið númers, færðu inn  '0160'.
9. Í reitnum Stærð skal smella á fellilistahnappinn til að opna leitina.
10. Í listanum skal smella á tengilinn í valinni línu.
11. Færið inn númer í reitnum „Magn“.
12. Smelltu á Bæta við.
13. Í svæðið númers, færðu inn  '0160'.
14. Í reitnum númer vöruvíddasamsetningar skal smella á fellilistahnappinn til að opna leitina.
15. Í listanum skal smella á tengilinn í valinni línu.
16. Færið inn númer í reitnum „Magn“.
17. Smelltu á Bæta við.
18. Í svæðið númer vöru, færðu inn '0175'.
19. Færið inn númer í reitnum „Magn“.
20. Smellið á „Vista“.
21. Lokið síðunni.

## <a name="add-package-to-purchase-order"></a>Bæta umbúðum við innkaupapöntun
1. Fara í Viðskiptaskuldir > Innkaupapantanir > Allar innkaupapantanir.
2. Smellið á „Nýtt“.
3. Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.
4. Á listanum, veljið sama lánardrottni og umbúðir afurðar var áður búið til fyrir, ef lánardrottinn var valinn.
5. Víxla útvíkkun á liðnum Almennt.
6. Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.
9. Í listanum skal smella á tengilinn í valinni línu.
10. Smellt er á Í lagi.
11. Víxla útvíkkun á liðnum línuupplýsingar.
12. Smellið á flipann umbúðir Vöru.
13. Smellt er á Innkaup Innkaupapöntunarlína
14. Smellt er á Stofna línur úr umbúðum
15. á listanum, Finna og velja umbúðir afurðar sem stofnaði í fyrra skrefi .
16. Í reitinn magn skal slá inn númer.
17. Smellið á „Stofna“.
18. Smellið á „Vista“.


