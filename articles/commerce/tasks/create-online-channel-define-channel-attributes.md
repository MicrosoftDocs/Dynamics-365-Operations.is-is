---
title: Stofna netrás og skilgreina eigindi rásar
description: Þetta ferli fer með þig í gegnum til að stofna nýja netrás og henni er bætt við stigveldi fyrirtækisins.
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f15b035c01801041d637a2d315d8a3ddcc9d6540
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413212"
---
# <a name="create-online-channel-and-define-channel-attributes"></a>Stofna netrás og skilgreina eigindi rásar

[!include [banner](../includes/banner.md)]

Þetta ferli fer með þig í gegnum til að stofna nýja netrás og henni er bætt við stigveldi fyrirtækisins. Þú verður að Stofna stigveldi fyrirtækis áður en hægt er að stofna nýja netrás. Þessi aðferð notar USRT sýnigögn fyrirtækisins.


## <a name="create-a-new-online-channel"></a>Stofna nýjan rás á netinu
1. Fara í Retail og Commerce > rásir > Netverslanir.
2. Smellið á Nýtt.
3. Í reitinn Heiti skal slá inn gildi.
4. Sláðu inn eða veldu gildi í reitnum Vöruhús.
5. Veljið valkost í svæðinu tímabelti Verslunar.
6. Færa inn eða velja gildi í svæðinu Sjálfgefinn viðskiptavin.
7. Færa inn eða veljið gildi í aðsetursbók viðskiptavinar.
8. Færa inn eða velja gildi í reitnum greiðsluskilmálar.
9. Færa inn eða velja gildi í reitnum greiðsluaðferð.
10. Færa inn eða veljið gildi í reit fyrir forstillingu tilkynninga Tölvupósts.
11. Útvíkka hlutann fjárhagsvíddir.
12. Færa inn eða veljið gildi í svæðinu BusinessUnit.
    * Stilla gildi fyrir allar aðrar sjálfgefnar víddir svipaðan hátt.  
13. Smellið á „Vista“.

## <a name="add-the-online-channel-to-organization-hierarchy"></a>Bæta við netrás í stigveldi fyrirtækis
1. Lokið síðunni.
2. Fara á fyrirtækisstjórnun > Fyrirtæki > stigveldi fyrirtækis.
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
4. Smellið á Skoða.
5. Smellið á „Breyta“.
    * Hægt er að velja hvaða stigveldishnút undir sem óskað er að setja inn nýja leið.  
6. Smellt er á Setja inn.
7. Smelltu á Commerce-rás.
8. Smellt er á Í lagi.
9. Smellt er á Birta til að opna felligluggann.
10. Færa inn dagsetningu og tíma í svæðinu gildisdagsetningu.
11. Smelltu á Birta.

## <a name="configure-orders-for-near-real-time-notification"></a>Stilla pantanir fyrir tilkynningu nálægt rauntíma
1. Farið í Retail og Commerce > Uppsetning höfuðstöðva > Færibreytur > Commerce-færibreytur.
2. Stilla rauntímaþjónustu fyrir stofnun eCommerce pöntunar á „Já“.
3. Keyra 1070 dreifingaráætlun til að samstilla breytingar við gagnagrunn rásar. 


