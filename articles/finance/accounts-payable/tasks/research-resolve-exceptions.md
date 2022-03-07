---
title: Rannsaka eða leysa úr undantekningum
description: Reikningsreglur lánardrottins eru keyrðar þegar reikningur lánardrottins er bókaður með því að nota síðuna fyrir reikning Lánardrottins og þegar síðan fyrir brot á reikningsreglum lánardrottins er opnuð.
author: abruer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d35504ab2fe6b8143d040bda505a904ab179b6137472073d788515f392faaef9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722888"
---
# <a name="research-or-resolve-exceptions"></a>Rannsaka eða leysa úr undantekningum

[!include [banner](../../includes/banner.md)]

Reikningsreglur lánardrottins eru keyrðar þegar reikningur lánardrottins er bókaður með því að nota síðuna fyrir reikning Lánardrottins og þegar síðan fyrir brot á reikningsreglum lánardrottins er opnuð. Einnig er hægt að skilgreina verkflæði fyrir reikning lánardrottins til að keyra reikningsreglur lánardrottins í hvert skipti sem er sendur er reikning til verkflæðis. 

Reikningsreglur lánardrottins eiga ekki við reikninga sem voru stofnaðar í komubók eða reikningabók. 

Sannprófun á reikningsjöfnun notar ekki reikningsreglur lánardrottins, en er í staðinn sett upp á síðunni færibreytur viðskiptaskulda.

Þessi skráning notar sýnigögn USMF fyrirtækis hlutverk viðskiptaskuldastjóri eða aðalbókari myndi framkvæma þessi skrefum. Áður en hafist er handa þarf að ganga úr skugga um að skilgreiningarlykill reikningsjöfnunar sé valinn.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Undirbúa stofnun stefna um reikninga lánardrottins
1. Fara í Viðskiptaskuldir > Uppsetning > Færibreytur viðskiptaskulda.
2. Smellið á flipann Staðfesting reiknings.
3. Veldu eða hreinsaðu gátreitinn uppfæra sjálfvirkt stöðu fyrirsögn reiknings.
4. Smellt er á Í lagi.
5. Í svæðinu Bóka reikning með misræmi skal velja valkost.
6. Lokið síðunni.
7. Fara í Viðskiptaskuldir > Uppsetning reglu > Reikningsreglur lánardrottins.
8. Smellt er á Færibreytum.
9. Smellt er á btnAdd.
10. Lokið síðunni.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Stofna stefnureglugerðir fyrir reikninga lánardrottins
1. Fara í Viðskiptaskuldir > Uppsetning reglu > Stefna fyrir reikning lánardrottins.
2. Smellið á „Nýtt“.
3. Í reitinn Nafn reglu skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í reitnum Heiti fyrirspurnar skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Smellið á „Vista“.
9. Lokið síðunni.

## <a name="define-a-vendor-invoice-policy"></a>Skilgreina stefna fyrir reikning lánardrottins
1. Fara í Viðskiptaskuldir > Uppsetning reglu > Reikningsreglur lánardrottins.
2. Smellið á „Nýtt“.
3. Í reitinn Heiti skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Útvíkka eða draga saman hlutann fyrirtækisregla
6. Í trénu skal velja 'Contoso Entertainment System USA'.
7. Smelltu á Bæta við.
8. Útvíkka eða draga saman hlutann stefnuregla.
9. Smellt er á Stofna stefnureglu.
10. Í reitinn Lýsing stefnuregla skal slá inn gildi.
11. Smellt er á Síu.
12. Smelltu á Bæta við.
13. Í listanum skal merkja valda línu.
14. Í reitnum Tafla skal smella á fellilistahnappinn til að opna leitina.
15. Í listanum skal smella á tengilinn í valinni línu.
16. Í reitnum Afleidd tafla skal smella á fellilistahnappinn til að opna leitina.
17. Í listanum skal smella á tengilinn í valinni línu.
18. Í reitnum Reitur skal smella á fellilistahnappinn til að opna leitina.
19. Í reitinn Reitur skal slá inn gildi.
20. Lokið síðunni.
21. Í reitinn Skilyrði skal slá inn gildi.
22. Smellið á „Í lagi“.
23. Smellið á „Í lagi“.
24. Lokið síðunni.
25. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]