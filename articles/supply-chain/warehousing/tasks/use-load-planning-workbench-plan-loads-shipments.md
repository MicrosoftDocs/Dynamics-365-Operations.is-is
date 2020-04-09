---
title: Áætla farm og sendingar með vinnusvæðinu Farmáætlun
description: Þessi efni sýnir hvernig á að nota vinnusvæði farmáætlunar til að stofna hleðslu fyrir sölupöntun.
author: ShylaThompson
manager: AnnBe
ms.date: 07/08/2019
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
ms.openlocfilehash: 8a51031647e270662f37138848b0db9ed08d544e
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145884"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Áætla farm og sendingar með vinnusvæðinu Farmáætlun

[!include [banner](../../includes/banner.md)]

Þessi efni sýnir hvernig á að nota vinnusvæði farmáætlunar til að stofna hleðslu fyrir sölupöntun. Sem frumskilyrði stofnum við sölupöntunina fyrst. Þetta ferli er hluti af daglega vinnu fyrir samræmingaraðili flutninga. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="create-a-sales-order"></a>Stofna sölupöntun
1. Farðu í **Sloðunarrúða > Kerfiseiningar > viðskiptakröfur > Pantanir > Allar sölupantanir**.
2. Veljið **Nýtt**.
3. Í reitnum **Viðskiptavinalykill** velurðu fellilistahnappinn til að opna uppflettinguna.
4. Veldu lykilinn **US-004.**
5. Veljið **Í lagi**.
6. Í reitnum **Vörunúmer** velurðu fellilistahnappinn til að opna uppflettinguna.
7. Velja vöru **A0001**. **A0001** er virkt fyrir flutningsstjórnun.  
8. Í reitnum **Svæði** velurðu fellilistahnappinn til að opna leitina og velur síðan vöruna.
9. Í reitnum **Magn** slærðu inn tölu.
10. Í **Vöruhús** reitinn, sláðu inn '24' fyrir þetta dæmi. Þetta vöruhús er virkr fyrir ítarlegt vöruhúsakerfi og flutningsstjórnun.  
11. Veljið **Vista**.
12. Lokið síðunni.

## <a name="create-a-new-load"></a>Stofna nýja hleðslu
1. Fara í **Skoðunarrúðu > Kerfiseiningar > Flutningsstýring > Áætlanagerð > Vinnusvæði hleðsluáætlunar**.
2. Veldu flipann **Sölulínur**. Nú byggirðu hleðslu fyrir sölupöntunina sem var nýverið stofnuð. Hægt er að byggja upp hleðslur á grundvelli framboðs og eftirspurnar úr innkaupapöntunum, flutningspöntunum og sölupöntunum.  
3. Í aðgerðasvæðinu er smellt á **Framboð og eftirspurn**.
4. Veldu **Í nýja hleðslu**.
5. Í reitnum **Auðkenni hleðslusniðmáts** skal smella á fellilistahnappinn til að opna leitina. Sniðmát Hleðslu skilgreinir hámarks mælieiningar fyrir þyngd og rúmmál allrar hleðslunnar. Til dæmis gæti hleðslusniðmátsins staðið fyrir stærð vörubíls eða gáms. Veljið vöru.
6. Veljið **Í lagi**.

## <a name="rate-and-route-the-load"></a>Taxta og leið á hleðslu
1. Veldu **Mat og leiðir**.
2. Veldu **Taxti vinnusvæðis leiðar**.
3. Veldu **Meta verslun**.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Velja **Úthluta**.
6. Lokið síðunni.

