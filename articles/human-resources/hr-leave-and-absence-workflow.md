---
title: Stofna verkflæði fyrir beiðni um leyfi
description: Búðu til vinnuflæði fyrir leyfi og fjarveru til að stjórna stöðugt leyfisbeiðnum í Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a4ce8d0a121e2fa24e3c221a30eb13debd6e44ea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855087"
---
# <a name="create-a-leave-request-workflow"></a>Stofna verkflæði fyrir beiðni um leyfi

> [!Important]
> Virknin sem getið er um í þessari grein er eins og er í boði fyrir viðskiptavini á sjálfstætt Dynamics 365 Human Resources. Sum eða öll virknin verður í boði sem hluti af síðari útgáfu í tölvukerfi Finance eftir útgáfu 10.0.26 af Finance.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Hægt er að stofna vinnuflæði í Dynamics 365 Human Resources til að stjórna stöðugt leyfis- og fjarvistarbeiðnum þínum. Verkflæðið **Leyfi og fjarvera** gerir þér kleift að:

- Skilgreina verkefni
- Ákveða hverjir verða að klára verkefnin
- Tilgreina hverjir geta samþykkt eða hafnað beiðnum

## <a name="create-a-leave-and-absence-request-workflow"></a>Stofna verkflæði fyrir beiðni um leyfi og fjarveru

1. Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.

2. Undir **Skipulag**, veldu **Vinnuflæði mannauðs**.

3. Veldu **Nýtt** og veldu síðan **Beiðnir um leyfi og fjarveru**. 

4. Þegar **Opna þessa skrá?** skilaboðakassi birtist, veldu **Opið** og skráðu þig inn með persónuskilríki fyrirtækisins.

5. Notaðu verkflæðiritið til að búa til verkflæði fyrir leyfisbeiðnir þínar. Nánari upplýsingar um vinnu með verkflæði, sjá [Búðu til yfirlit yfir verkflæði](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Gagnaeiningar fyrir verkflæði leyfis- og fjarvistabeiðni

Hægt er að nota eftirfarandi gagnaeiningar til að stofna skilyrtar eða sjálfvirkar samþykktir í verkflæði fyrir beiðnir um leyfi og fjarvistir:

- **Upphæð**
- **Athugasemd**
- **Fyrirt.**
- **Búið til af**
- **Tími og dagsetning stofnunar**
- **Lokadagur**
- **Gerð leyfis**
- **Breytt hefur**
- **Breytt dagsetning og tími**
- **Ástæðukóði**
- **Beiðnikenni**
- **Upphafsdagsetning**
- **Staða** 
- **Sendidagur**
- **Sent af**
- **Sent af mannauðsstjóra**
- **Sent af stjórnanda**
- **Sent fyrir hönd**
- **Starfsmaður**
- **Gerð starfskrafts**

Þessi dæmi sýna hvernig hægt er að stofna mismunandi skilyrði verkflæðis með þessum gagnaeiningum:

- Notaðu **Ástæðukóði** í skilyrtri setningu til að beina leyfisbeiðnum með ástæðukóðanum **Skurðaðgerð** til samþykkis mannauðsdeildar, en alla aðra ástæðukóða til stjórnanda. Frekari upplýsingar um skilyrta setningu er að finna í [Skilgreina skilyrtar ákvarðanir í verkflæði](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md). 

- Notið **Sent af mannauðsstjóra** og **Sent af stjórnanda** í sjálfvirkri aðgerð til að samþykkja sjálfkrafa leyfisbeiðnir sem þessi hlutverk senda fyrir hönd starfsmanna. Frekari upplýsingar um sjálfvirkar aðgerðir er að finna í [Grunnstilla samþykktarferli í verkflæði](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- Nota skal **Leyfisgerðir** í skilyrtri setningu eða sjálfvirkri aðgerð til að hafa stjórn á því hvernig verkflæðisleiðir fara fram með tilteknum leyfisgerðum.

## <a name="see-also"></a>Sjá einnig

- [Yfirlit yfir leyfi og fjarvistir](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
