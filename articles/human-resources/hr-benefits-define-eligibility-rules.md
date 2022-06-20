---
title: Skilgreina reglur og stefnur um hæfi til fríðinda
description: Þetta efnisatriði útskýrir hvernig hægt er að stofna hæfnisreglur fríðinda og stefnur og síðan úthluta reglum á fríðindi.
author: twheeloc
ms.date: 08/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 4781a00ae63bb2d27df0610a1886cc43e52798f9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861190"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Skilgreina reglur og stefnur um hæfi til fríðinda


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein útskýrir hvernig á að búa til hæfisreglur og stefnur og úthluta síðan reglum til fríðinda.  

## <a name="create-benefit-eligibility-policy-rule-type"></a>Stofna Stefnureglugerðir um hæfni til fríðinda

1. Farið í **Mannauður > Fríðindi > Hæfi > Fríðindi hæfi stefnureglugerðir**.
2. Veljið **Nýtt**.
3. Í reitinn **Heiti reglu** skal slá inn gildi.
4. Sláið inn gildi í reitnum **Lýsing**.
5. Í reitnum **Heiti fyrirspurnar** skal velja fellilistahnappinn til að opna leitina.
6. Í listanum skal velja tengilinn í valinni línu.
7. Veljið **Vista**.
8. Lokið síðunni.

## <a name="benefit-eligibility-policy"></a>Regla um hæfni til fríðinda

1. Farið í **Mannauður > Fríðindi > Hæfi > Fríðindi hæfi stefnur**.
2. Veljið fyrirliggjandi stefmireglu fríðinda.
3. Í listanum skal velja tengilinn í valinni línu.
4. Víxla útvíkkun hluta **fyrirtækisreglu**. Hægt er að bæta við eða fjarlægja hvaða fyrirtæki sem á að taka með í reglunni.
5. Útvíkka eða draga saman hlutann **stefnuregla**.
6. Finna reglu sem áður hafa verið stofnaðar í listanum.
7. Veldu **stefnureglu**.
8. Færið inn dagsetninguna sem reglan á að taka gildi í svæðinu **gildisdagsetningu**.
    * Að stilla virkar lokadagsetningar gerir kleift að gera breytingar síðar á stefnureglum þannig að ekki þurfi að fara aftur í regluna þegar ætlunin er að þessar breytingar taki gildi.  
9. Ef þörf krefur skal bæta where-klausu við reitinn **Bæta við skilyrði**.
    * Til dæmi ef reglan eiga aðeins við sölustjóra er hægt að stofna Hvar klausunni til að segja: þar sem stöðulýsing jafngildir Sölustjóri. Hægt er að bæta mörgum where-skipunum saman í reglunni.  
10. Veljið **Í lagi**.
11. Lokið síðunni.

## <a name="assign-rule-to-benefit"></a>Úthluta regla fríðinda

1. Farið í **Mannauður > Fríðindi > Fríðindi**.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal velja tengilinn í valinni línu.
4. Útvíkka eða draga saman hlutann **hæfnisreglur**.
5. Veljið **Breyta**.
6. Í reitnum **Hæfi** skal velja reglu.
7. Í reitnum **Gerð reglu** skal velja regluna sem var verið að búa til.
9. Í listanum skal velja tengilinn í valinni línu.
10. Veljið **Vista**.
11. Lokaðu skjámyndinni.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
