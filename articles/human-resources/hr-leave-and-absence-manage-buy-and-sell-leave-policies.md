---
title: Stjórna reglum fyrir kaup og sölu á leyfisdögum
description: Hægt er að gera starfsmönnum kleift að kaupa og selja leyfisdaga í Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429014"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Stjórna reglum fyrir kaup og sölu á leyfisdögum

[!include [banner](includes/preview-feature.md)]

Hægt er að gera starfsmönnum kleift að kaupa leyfisdaga með því að búa til reglu um kaup á leyfisdögum.  

## <a name="enable-employees-to-buy-and-sell-leave"></a>Gera starfsmönnum kleift að kaupa og selja leyfisdaga

1. Á síðunni **Færibreytur leyfis og fjarvista** skal velja **Já** fyrir **Leyfa starfsmönnum að kaupa leyfisdaga**. 

## <a name="create-a-buy-leave-policy"></a>Búa til reglu um kaup á leyfisdögum

1. Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**. 

2. Veljið **Regla um kaup og sölu leyfisdaga**.

3. Veljið **Nýtt**.

4. Sláið inn **Heiti** og **Lýsing** fyrir regluna undir **Regla um kaup og sölu leyfisdaga**. 

5. Veljið **Gerð reglu**. 

   Tiltækar gerðir reglu eru **Fjöldi** og **Klukkustundir á viku**. Veljið **Fjöldi** til að færa inn **Fastan fjölda** fyrir þann hámarksfjölda sem starfsmenn geta keypt og selt. Ef valið er **Klukkustundir á viku** eru skilgreindar vinnustundir í úthlutuðu vinnutímadagatali starfsmanns notaðar til að ákveða hámarksfjölda fyrir regluna. 

6. Veljið **Upphafsdagsetning** og **Lokadagsetning** fyrir regluna. Beiðnir um að kaupa eða selja leyfi verða aðeins í boði fyrir innsendingu á þessum tímaramma. 

7. Undir **Regla um kaup** skal velja **Jafngildi fulls starfs** (JFS) til að hlutfallsskipta hámarksfjöldanum samkvæmt JFS sem skilgreint er fyrir stöðu starfsmanns. Ef gerð reglunnar er **Fjöldi** skal slá inn **Fastur hámarksfjöldi**. 

8. Veljið **Bæta við** til að bæta við leyfisgerðum fyrir starfsmenn til að kaupa leyfisdaga. Hægt er að bæta við mörgum leyfisgerðum í regluna. 

9. Færið inn **Starfsaldur í mánuðum** fyrir leyfisgerðina til að virkja mismunandi starfsaldur í mánuðum til að ákveða hámarksfjölda sem starfsmaður getur keypt. 

10. Færið inn **Hámarksfjöli** fyrir leyfisgerðina. 

11. Færið inn **Taxti** sem starfsmaður mun kaupa leyfisdaga á. 

12. Einnig er hægt að færa inn **Tekjukóði** til að nota við kaup á leyfisdögum. 

13. Valfrjálst er að stilla hvort nota eigi JFS til að ákveða hámarksfjölda fyrir leyfisgerðina. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Bæta reglu um kaup og sölu á leyfisdögum við leyfis- og fjarveruáætlun

1. Á síðunni **Leyfi og fjarvera** skal velja leyfis- og fjarveruáætlun.

2. Undir **Reglur** skal velja **Regla um kaup og sölu leyfisdaga**.

## <a name="see-also"></a>Sjá einnig

[Yfirlit yfir leyfi og fjarvistir](hr-leave-and-absence-overview.md)</br>
[Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md)</br>
[Uppsöfnunaráætlanir fyrir leyfi og fjarvistir](hr-leave-and-absence-accrue.md)</br>
[Kaupa og selja leyfisdaga](hr-employee-self-service-buy-sell-leave.md)
