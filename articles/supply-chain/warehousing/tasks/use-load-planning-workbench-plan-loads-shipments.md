---
title: Áætla farm og sendingar með vinnusvæðinu Farmáætlun
description: Þessi gerli sýnir hvernig á að nota vinnusvæði farmáætlunar til að stofna hleðslu fyrir sölupöntun.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1927cff48beb30f934bd066c32ab48dfb9d06f74
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "343904"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Áætla farm og sendingar með vinnusvæðinu Farmáætlun

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi gerli sýnir hvernig á að nota vinnusvæði farmáætlunar til að stofna hleðslu fyrir sölupöntun. Sem frumskilyrði stofnum við sölupöntunina fyrst. Þetta ferli er hluti af daglega vinnu fyrir samræmingaraðili flutninga. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="create-a-sales-order"></a>Stofna sölupöntun
1. Farið í Viðskiptakröfur > Pantanir > Allar sölupantanir.
2. Smellið á „Nýtt“.
3. Í reitnum Reikningur viðskiptavina skal smella á fellilistahnappinn til að opna leitina.
4. Velja lykilinn US-004.
5. Smellt er á Í lagi.
6. Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.
7. Velja vöru A0001.
    * A0001 er virkt fyrir flutningsstjórnun.  
8. Í listanum skal smella á tengilinn í valinni línu.
9. Færið inn númer í reitnum „Magn“.
10. Í reitnum Vöruhús skal færa inn ‚24‘.
    * Í þessu dæmi skal velja vöruhúsið 24. Þetta vöruhús er virkr fyrir ítarlegt vöruhúsakerfi og flutningsstjórnun.  
11. Smellið á „Vista“.
12. Lokið síðunni.

## <a name="create-a-new-load"></a>Stofna nýja hleðslu
1. Fara í flutningsstjórnun > Áætlanagerð > Vinnusvæði hleðsluáætlunar.
2. Smellt er á flipanum sölulína.
    * Nú byggirðu hleðslu fyrir sölupöntunina sem var nýverið stofnuð. Hægt er að byggja upp hleðslur á grundvelli framboðs og eftirspurnar úr innkaupapöntunum, flutningspöntunum og sölupöntunum.  
3. Í aðgerðasvæðinu er smellt á Framboð og eftirspurn.
4. Smellt er á Í nýja hleðslu.
5. Í reitnum Auðkenni hleðslusniðmáts skal smella á fellilistahnappinn til að opna leitina.
    * Sniðmát Hleðslu skilgreinir hámarks mælieiningar fyrir þyngd og rúmmál allrar hleðslunnar. Til dæmis gæti hleðslusniðmátsins staðið fyrir stærð vörubíls eða gáms.  
6. Í listanum skal smella á tengilinn í valinni línu.
7. Smellið á „Í lagi“.

## <a name="rate-and-route-the-load"></a>Taxta og leið á hleðslu
1. Smellt er á Mat og leið.
2. Smellt er á Taxti vinnusvæðis leiðar.
3. Smellt er á Taxti verslunar.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Smellið á úthluta.
6. Lokið síðunni.
7. Lokið síðunni.

