---
title: Áætla framleiðslupöntun með rekstrar- og vinnuröðun
description: Þessi grein fjallar um tímasetningu framleiðslupöntunar með aðgerðaáætlun og verkáætlun.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d82d5439e57c02ddc9db4222a946bd15f4ed67e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903928"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Áætla framleiðslupöntun með rekstrar- og vinnuröðun

[!include [banner](../../includes/banner.md)]

Þessi grein fjallar um tímasetningu framleiðslupöntunar með aðgerðaáætlun og verkáætlun. Engar vinnslur eru stofnaðar með aðgerðaröðun meðan störf eru stofnuð með vinnsluröðun. Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF. Þetta ferli er ætluð fyrir framleiðslustjóri skipuleggjandi framleiðslu eða vinnusalarstjórnun yfirmaður sem unnið er í framleiðsluumhverfi afmörkuð.


## <a name="create-a-production-order"></a>Stofna framleiðslupöntun
1. Í skoðunarsíðunni ferðu í **Kerfiseiningar > Framleiðslustýring > Framleiðslupantanir > Allar framleiðslupantanir**.
2. Veldu **Ný framleiðslupöntun**.
3. Í reitinn **Vörunúmer** skal slá inn eða velja gildi. Veldu vörunúmerið **D0001**.  
4. Velja **Stofna**.

## <a name="schedule-operations-for-the-production-order"></a>Ef framkvæma á aðgerðaröðun fyrir framleiðslupöntun.
1. Merktu nýstofnaða röð.      
2. Í aðgerðasvæðinu velurðu **Tímasetja**.
3. Veldu **Raða aðgerðum**.
4. Í reitnum **Röðunarstefna** er valið **Áfram frá röðunardagsetningu**.
5. Dagsetning er rituð í reitinn **Röðunardagsetning**. Velja dagsetningu í framtíðinni, til dæmis í dag plús ein vika. Með valda Röðun stefnu framleiðslupöntun verður raðað áfram frá þessari dagsetningu.  
6. Veljið **Í lagi**.
7. Í listanum skal merkja valda línu. Athugið að stöðu framleiðslu er breytt í **Tímasett**. 
8. Veldu **Allar vinnslur**. Athugið að engar vinnslur eru stofnaðar með aðgerðaröðun.  
9. Lokið síðunni.

## <a name="schedule-jobs-for-the-production-order"></a>Ef framkvæma á aðgerðaröðun fyrir framleiðslupöntun.
1. Í aðgerðasvæðinu velurðu **Tímasetja**.
2. Veldu **Röðunarverk**.
3. Í reitnum **Röðunarstefna** er valið **Áfram frá röðunardagsetningu**.
4. Dagsetning er rituð í reitinn **Röðunardagsetning**. Velja dagsetningu í framtíðinni, til dæmis í dag plús ein vika. Með valda Röðun stefnu framleiðslupöntun verður raðað áfram frá þessari dagsetningu.  
5. Veljið **Í lagi**.
6. Á aðgerðasvæðinu skal velja **Framleiðslupöntun**.
7. Veldu **Allar vinnslur**. Athugið samkvæmt virk leið 5 störf eru stofnuð með vinnsluröðun.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]