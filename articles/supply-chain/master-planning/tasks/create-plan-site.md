---
title: Stofna áætlun fyrir svæði
description: Framleiðslustjóri reiknar efnis- og afkastakröfur fyrir framleiðslu á tiltekinnar vöru.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01c8330fc15074eb59762dac73d0b176bd7faadc
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469506"
---
# <a name="create-a-plan-for-a-site"></a>Stofna áætlun fyrir svæði

[!include [banner](../../includes/banner.md)]

Framleiðslustjóri reiknar efnis- og afkastakröfur fyrir framleiðslu á tiltekinnar vöru. Eftir að tillögur um uppruna eru stofnaðar finnur hann pantanirnar á svæði sem hann er að gera áætlun fyrir og staðfestir pantanir, byrjar á þeim sem eru mest áríðandi. Mest áríðandi pantanir eru þær sem þarf að staðfesta á gildandi dagsetningu. Nota Sýnifyrirtækið USMF til að ljúka við þessi verk.


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a>Stofna efnis- og afkastaáætlun fyrir vöru
1. Smellt er á aðaláætlanagerð.
    * Þarf að fara á sjálfgefið yfirlit.  
2. Smellið á „Keyra“.
3. Útvíkka Færslur til að taka hluta.
4. Smellt er á Síu.
5. Í listanum skal merkja valda línu.
6. Í reitinn Skilyrði skal slá inn gildi.
    * Til dæmis: D0001  
7. Smellið á „Í lagi“.
8. Smellið á „Í lagi“.
    * Þetta getur tekið nokkrar mínútur...  
9. Endurhlaðið síðuna.

## <a name="identify-the-urgent-planned-orders-for-the-item"></a>Auðkenna áríðandi áætlaðar pantanir fyrir vöru
1. Opna vörunúmerasíu fyrir dálkur.
2. Notið síu í reitnum „vörunúmer“ með gildinu „D0001“ og notið til þess „byrjar á“ síu virknitákn
3. Opnið dálkasíu pöntunardagsetningar.
4. Nota síu á "Pöntunardagsetningu" svæðið, með gildandi dagsetningu, með síuvirkjanum "er nákvæmlega".

## <a name="firm-all-the-urgent-orders-for-the-item"></a>Staðfesta áríðandi pantanir fyrir vöru
1. Merkið eða afmerkið allar línur í listanum.
2. Smellið á „Fastáætla“.
3. Smellið á „Í lagi“.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]