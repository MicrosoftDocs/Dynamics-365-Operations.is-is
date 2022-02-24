---
title: Skilgreina reglur og stefnur um hæfi til fríðinda
description: Þessi grein sýnir hvernig hægt er að stofna hæfnisreglur fríðinda og stefnur og síðan tengja reglur við Fríðindi.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: f46437fef342ab1a4e368063d8b74205ca8e8c05
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419016"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Skilgreina reglur og stefnur um hæfi til fríðinda

Þessi grein sýnir hvernig hægt er að stofna hæfnisreglur fríðinda og stefnur og síðan tengja reglur við Fríðindi.  

Gögn sýniútgáfu fyrirtækis sem er notað til að stofna þessa skráningu í USMF.


## <a name="create-benefit-eligibility-policy-rule-type"></a>Stofna Stefnureglugerðir um hæfni til fríðinda
1. Farið í Mannauður > Fríðindi > Hæfi > Fríðindi hæfi stefnureglugerðir.
2. Smellið á „Nýtt“.
3. Í reitinn Nafn reglu skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í reitnum Heiti fyrirspurnar skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal smella á tengilinn í valinni línu.
7. Smellið á „Vista“.
8. Lokið síðunni.

## <a name="benefit-eligibility-policy"></a>Regla um hæfni til fríðinda
1. Farið í Mannauður > Fríðindi > Hæfi > Fríðindi hæfi stefnur.
2. Veljið fyrirliggjandi stefmireglu fríðinda.
3. Í listanum skal smella á tengilinn í valinni línu.
4. Víxla útvíkkun hluta fyrirtækisreglu.  Hér er hægt að bæta við eða fjarlægja hvaða fyrirtæki sem á að taka með í reglunni.
5. Útvíkka eða draga saman hlutann stefnuregla.
6. Finna reglu sem áður hafa verið stofnaðar í listanum.
7. Smellt er á Stofna stefnureglu.
8. Færið inn dagsetninguna sem reglan á að taka gildi í svæðinu gildisdagsetningu.
    * Stilla virkar og lokadagsetningar gerir kleift að gera breytingar síðar á stefnureglur og fjarlægja þörfina á að koma aftur að þessari reglu þegar óskað er eftir að þessar breytingar taki gildi.  
9. 
    * Til dæmi ef reglan eiga aðeins við sölustjóra er hægt að stofna Hvar klausunni til að segja: þar sem stöðulýsing jafngildir Sölustjóri .  Hægt er að marfalda með Og Eða yrðingar saman í reglunni.  
10. Smellið á „Í lagi“.
11. Lokið síðunni.
12. Lokið síðunni.

## <a name="assign-rule-to-benefit"></a>Úthluta regla fríðinda
1. Farið í Mannauður > Fríðindi > Fríðindi.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
4. Útvíkka eða draga saman hlutann hæfnisreglur.
5. Smella á Breyta.
6. Velja Reglu sem byggð er á listanum í svæðinu Hæfni.
7. Í reitnum gerð reglu skal smella á fellilistahnappinn til að opna leitina.
8. Finna og velja reglu sem áður hafa verið stofnaðar í listanum.
9. Í listanum skal smella á tengilinn í valinni línu.
10. Smellið á „Vista“.
11. Lokaðu skjámyndinni.

