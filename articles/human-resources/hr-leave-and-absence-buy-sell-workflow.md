---
title: Búa til verkflæði fyrir beiðni um kaup og sölu á leyfisdögum
description: Stofna skal verkflæði fyrir beiðni um kaup og sölu á leyfisdögum til að stjórna betur beiðnum um kaup og sölu á leyfisdögum í Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9ec21cda4779fea8c28b73d25842219da900da9d
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271484"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a>Búa til verkflæði fyrir beiðni um kaup og sölu á leyfisdögum

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Hægt er að stofna verkflæði í Dynamics 365 Human Resources til að stjórna betur beiðnum um kaup og sölu á leyfisdögum. Verkflæði fyrir **Kaupa og selja leyfisdaga** gerir þér kleift að:

- Skilgreina verkefni
- Ákveða hverjir verða að klára verkefnin
- Tilgreina hverjir geta samþykkt eða hafnað beiðnum

## <a name="create-a-buy-and-sell-leave-request-workflow"></a>Búa til verkflæði fyrir beiðni um kaup og sölu á leyfisdögum

1. Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.

2. Undir **Skipulag**, veldu **Vinnuflæði mannauðs**.

3. Velja **Ný** og síðan velja **Beiðni um að kaupa og selja leyfisdaga**. 

4. Þegar **Opna þessa skrá?** skilaboðakassi birtist, veldu **Opið** og skráðu þig inn með persónuskilríki fyrirtækisins.

5. Notaðu verkflæðiritið til að búa til verkflæði fyrir leyfisbeiðnir þínar. Nánari upplýsingar um vinnu með verkflæði, sjá [Búðu til yfirlit yfir verkflæði](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Gagnaeiningar fyrir verkflæði leyfis- og fjarvistabeiðni

Hægt er að nota eftirfarandi gagnaeiningar til að stofna skilyrtar eða sjálfvirkar samþykktir í verkflæðum fyrir beiðnir um kaup og sölu á leyfisdögum:

- **Upphæð**
- **Regla um kaup og sölu leyfisdaga**
- **Fyrirt.**
- **Stofnað af**
- **Tími og dagsetning stofnunar**
- **Lokadagsetning**
- **Leyfisgerð**
- **Breytt hefur**
- **Breytt dagsetning og tími**
- **Beiðnikenni**
- **Upphafsdagsetning**
- **Staða** 
- **Dagsetning innsendingar**
- **Sent hefur**
- **Sent af mannauðsstjóra**
- **Sent af stjórnanda**
- **Sent fyrir hönd**
- **Starfsmaður**

## <a name="workflow-examples"></a>Dæmi um verkflæði

Þessi dæmi sýna hvernig hægt er að stofna mismunandi skilyrði verkflæðis með þessum gagnaeiningum:

- Notið **Sent af mannauðsstjóra** og **Sent af stjórnanda** í sjálfvirkri aðgerð til að samþykkja sjálfkrafa kaup og sölu leyfisbeiðna sem þessi hlutverk senda fyrir hönd starfsmanna. Frekari upplýsingar um sjálfvirkar aðgerðir er að finna í [Grunnstilla samþykktarferli í verkflæði](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- Nota skal **Leyfisgerðir** í skilyrtri setningu eða sjálfvirkri aðgerð til að hafa stjórn á því hvernig verkflæðisleiðir fara fram með tilteknum leyfisgerðum.

## <a name="see-also"></a>Sjá einnig

[Yfirlit yfir leyfi og fjarvistir](hr-leave-and-absence-overview.md)<br>
[Stjórna reglum fyrir kaup og sölu á leyfisdögum](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)<br>
[Kaupa og selja leyfisdaga](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
