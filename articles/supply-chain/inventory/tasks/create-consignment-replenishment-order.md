---
title: Stofna áfyllingarpöntun vörusendingar
description: Þessi grein sýnir hvernig skal stofna áfyllingarpöntun vörusendingar þar sem hægt er að rekja áætlaða afhendingu frá lánardrottni inn í vörusendingabirgðir.
author: yufeihuang
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31a1d0a7d322b17d3d80dd9fade2b037dd148d9f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859374"
---
# <a name="create-a-consignment-replenishment-order"></a>Stofna áfyllingarpöntun vörusendingar

[!include [banner](../../includes/banner.md)]

Þessi grein sýnir hvernig skal stofna áfyllingarpöntun vörusendingar þar sem hægt er að rekja áætlaða afhendingu frá lánardrottni inn í vörusendingabirgðir. Hún sýnir einnig hvernig á að skrá innhreyfingar afurða þannig að vörusendingabirgðir eru skráðar sem lagerbirgðir í lánardrottins. Þetta ferli myndi er yfirleitt framkvæmt af innkaupaaðila. Hægt er að nota þessar leiðbeiningar í sýnifyrirtækinu USMF. Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.

## <a name="create-a-consignment-replenishment-order"></a>Stofna áfyllingarpöntun vörusendingar
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Innkaup og aðföng > Vörusending > Áfyllingarpantanir vörusendingar**.
2. Veljið **Nýtt**.
3. Í reitnum **Lánardrottnareikningur** velurðu lánardrottinn **US-104** (þú verður að velja lánardrottinn sem er skráður sem eigandi á síðunni **birgðaeigendur**). 
4. Veljið **Í lagi**.
5. Veldu **Bæta við línu**.
6. Í reitnum **Vörunúmer** slærðu inn `M9211CI` (þú verður að velja hlut sem er settur upp fyrir vörusendingarbirgðum).
7. Í reitnum **Magn** slærðu inn tölu.
8. Í reitinn **Umbeðin afhendingardagsetning** skal rita dagsetningu. Umbeðnar og staðfestar dagsetningar eru notaðar af MRP-vélinni (vél lánstímaálags) vegna áætlaðrar komu varningsins.  
9. Í reitnum **Staðfestur afhendingardagur** skal rita dagsetningu.
10. Útvíkkaðu hlutann **upplýsingar Línu**.
11. Veldu flipann **Birgðavíddir**.
12. Til að sýna eiganda í reitnum **Eigandi birgðavídda** skal endurnýja síðuna. Lánardrottininn US-104 er nú skráður sem eiganda.  

## <a name="check-the-inventory-transaction-status"></a>Athugaðu staða birgðafærslunnar.
1. Veldu **Birgðir**.
2. Veldu **Færslur**.
3. Í æskilegri línu skaltu athuga að reiturinn **Innhreyfinng** er stillt á **Pantað**.  
4. Lokið síðunni.

## <a name="receive-items"></a>Taka á móti vörum
1. Velja **Innhreyfingarskjal afurða**.
2. Í reitnum **Ytra innhreyfingarskjal afurða** skal rita gildi.
3. Í reitinn **Magn** skal slá inn tölu sem er lægri en talan sem er sýnd þar. 
4. Veljið **Í lagi**.

## <a name="check-the-on-hand-inventory"></a>Athuga birgðir á lager.
1. Veldu **Birgðir**.
2. Veldu **Á lager**.
3. Veldu **Yfirlit**. Vörur sem hafa verið mótteknar sem vörusendingabirgðir í eigu lánardrottins eru tiltæk á lager. Eftirstandandi magn á áfyllingarpöntun vörusendingar er birt í reitnum **Samtals pantað**.  
4. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]