---
title: Stjórna reglum fyrir kaup og sölu á leyfisdögum
description: Hægt er að gera starfsmönnum kleift að kaupa og selja leyfisdaga í Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
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
ms.openlocfilehash: 89563204cf1423ddce47d7bacace8f14edf87005
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115997"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Stjórna reglum fyrir kaup og sölu á leyfisdögum

Hægt er að gera starfsmönnum kleift að kaupa og selja leyfisdaga með því að búa til reglu um kaup og sölu á leyfisdögum. Hægt er að skilgreina þessar reglur til að nota verkflæði fyrir samþykktir, stilla hámarksfjárhæðir og taxta og stilla taxta fyrir kaup og sölur. 

## <a name="enable-employees-to-buy-and-sell-leave"></a>Gera starfsmönnum kleift að kaupa og selja leyfisdaga

1. Á síðunni **Færibreytur leyfis og fjarvista** skal velja **Já** fyrir **Leyfa starfsmönnum að kaupa leyfisdaga** og **Leyfa starfsmönnum að selja leyfisdaga**.

## <a name="create-a-buy-and-sell-leave-policy"></a>Búa til reglu um kaup og sölu leyfisdaga

1. Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**. 

2. Veljið **Regla um kaup og sölu leyfisdaga**.

3. Veljið **Nýtt**.

4. Sláið inn **Heiti** og **Lýsing** fyrir regluna undir **Regla um kaup og sölu leyfisdaga**. 

5. Veljið **Gerð reglu**. 

   Tiltækar gerðir reglu eru **Fjöldi** og **Klukkustundir á viku**. Veljið **Fjöldi** til að færa inn **Fastan fjölda** fyrir þann hámarksfjölda sem starfsmenn geta keypt og selt. Ef valið er **Klukkustundir á viku** eru skilgreindar vinnustundir í úthlutuðu vinnutímadagatali starfsmanns notaðar til að ákveða hámarksfjölda fyrir regluna. 

6. Veljið **Upphafsdagsetning** og **Lokadagsetning** fyrir regluna. Beiðnir um að kaupa eða selja leyfi verða aðeins í boði fyrir innsendingu á þessum tímaramma. 

7. Veljið **Kenni verkflæðis** fyrir regluna. Allar beiðnir um kaup og sölur munu nota þetta verkflæði fyrir yfirferð og samþykki. 

8. Undir **Regla um kaup** skal velja **Jafngildi fulls starfs** (JFS) til að hlutfallsskipta hámarksfjöldanum samkvæmt JFS sem skilgreint er fyrir stöðu starfsmanns. Ef gerð reglunnar er **Fjöldi** skal slá inn **Fastur hámarksfjöldi**. 

9. Veljið **Bæta við** til að bæta við leyfisgerðum fyrir starfsmenn til að kaupa leyfisdaga. Hægt er að bæta við mörgum leyfisgerðum í regluna. 

10. Færið inn **Starfsaldur í mánuðum** fyrir leyfisgerðina til að virkja mismunandi starfsaldur í mánuðum til að ákveða hámarksfjölda sem starfsmaður getur keypt. 

11. Færið inn **Hámarksfjöli** fyrir leyfisgerðina. 

12. Færið inn **Taxti** sem starfsmaður mun kaupa leyfisdaga á. 

13. Einnig er hægt að færa inn **Tekjukóði** til að nota við kaup á leyfisdögum. 

14. Valfrjálst er að stilla hvort nota eigi JFS til að ákveða hámarksfjölda fyrir leyfisgerðina. 

15. Til að búa til reglu um sölu skal fylgja skrefum 8 til 14 undir **Söluregla**. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Bæta reglu um kaup og sölu á leyfisdögum við leyfis- og fjarveruáætlun

1. Á síðunni **Leyfi og fjarvera** skal velja leyfis- og fjarveruáætlun.

2. Undir **Reglur** skal velja **Regla um kaup og sölu leyfisdaga**.

## <a name="see-also"></a>Sjá einnig

[Yfirlit yfir leyfi og fjarvistir](hr-leave-and-absence-overview.md)</br>
[Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md)</br>
[Uppsöfnunaráætlanir fyrir leyfi og fjarvistir](hr-leave-and-absence-accrue.md)</br>
[Kaupa og selja leyfisdaga](hr-employee-self-service-buy-sell-leave.md)

