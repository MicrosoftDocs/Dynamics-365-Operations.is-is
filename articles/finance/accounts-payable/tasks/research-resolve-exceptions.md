---
title: Rannsaka eða leysa úr undantekningum
description: Reikningsreglur lánardrottins eru keyrðar þegar reikningur lánardrottins er bókaður með því að nota síðuna fyrir reikning Lánardrottins og þegar síðan fyrir brot á reikningsreglum lánardrottins er opnuð.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32ff53198f61e1d1af3c437e9488c2a246cf820a
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2022
ms.locfileid: "8110020"
---
# <a name="research-or-resolve-exceptions"></a>Rannsaka eða leysa úr undantekningum

[!include [banner](../../includes/banner.md)]

Reikningsreglur lánardrottins eru keyrðar þegar **reikningur lánardrottins** er bókaður með því að nota síðuna fyrir reikning Lánardrottins og þegar síðan fyrir **brot á reikningsreglum** lánardrottins er opnuð. Einnig er hægt að skilgreina verkflæði fyrir reikning lánardrottins til að keyra reikningsreglur lánardrottins í hvert skipti sem er sendur er reikning til verkflæðis. 

Reikningsreglur lánardrottins eiga ekki við reikninga sem voru stofnaðar í **Komubók** eða **Reikningabók**. 

Sannprófun á reikningsjöfnun notar ekki reikningsreglur lánardrottins, en er sett upp á síðunni **Færibreytusíða viðskiptaskulda**.

Þessi skráning notar sýnigögn USMF fyrirtækis hlutverk viðskiptaskuldastjóri eða aðalbókari myndi framkvæma þessi skrefum. Áður en hafist er handa þarf að ganga úr skugga um að **Skilgreiningarlykill reikningsjöfnunar** sé valinn.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Undirbúa stofnun stefna um reikninga lánardrottins
1. Farðu í **Viðskiptaskuldir > Uppsetning > Færibreytur fyrir viðskiptaskuldir.**
2. Smellið á flipann **Staðfesting reiknings**.
3. Veldu eða hreinsaðu gátreitinn **Uppfæra sjálfvirkt stöðu fyrirsögn reiknings**.
4. Smellt er á **OK**.
5. Í reitnum **Bóka reikning með misræmi** skal velja valkost.
6. Lokið síðunni.
7. Fara í **Viðskiptaskuldir > Uppsetning reglu > Reikningsreglur lánardrottins**.
8. Smellt er á **Færibreytur**.
9. Smelltu á **Bæta við**.
10. Lokið síðunni.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Stofna stefnureglugerðir fyrir reikninga lánardrottins
1. Fara í **Viðskiptaskuldir > Uppsetning reglu > Stefna fyrir reikning lánardrottins**.
2. Smellt er á **Nýtt**.
3. Í reitinn **Heiti reglu** skal slá inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Í reitnum **Heiti fyrirspurnar** skal smella á fellilistahnappinn til að opna leitina.
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Smelltu á **Vista**.
9. Lokið síðunni.

## <a name="define-a-vendor-invoice-policy"></a>Skilgreina stefna fyrir reikning lánardrottins
1. Fara í **Viðskiptaskuldir > Uppsetning reglu > Reikningsreglur lánardrottins**.
2. Smellt er á **Nýtt**.
3. Í reitinn **Heiti** skal slá inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Útvíkka eða draga saman hlutann **fyrirtækisregla**.
6. Veljið 'Contoso Entertainment System USA', í trénu.
7. Smelltu á **Bæta við**.
8. Útvíkka eða draga saman hlutann **stefnuregla**.
9. Smelltu á **Stofna stefnureglu**.
10. í reitnum **Lýsing stefnuregla** skal slá inn gildi.
11. Smella á **Sía**.
12. Smelltu á **Bæta við**.
13. Í listanum skal merkja valda línu.
14. Í reitnum **Tafla** skal smella á fellilistahnappinn til að opna leitina.
15. Í listanum skal smella á tengilinn í valinni línu.
16. Í reitnum **Afleidd tafla** skal smella á fellilistahnappinn til að opna leitina.
17. Í listanum skal smella á tengilinn í valinni línu.
18. Í reitnum **Reitur** skal smella á fellilistahnappinn til að opna leitina.
19. Í reitinn **Reitur** skal slá inn gildi.
20. Lokið síðunni.
21. Í reitnum **Skilyrði** skal slá inn gildi.
22. Smellt er á **OK**.
23. Smellt er á **OK**.
24. Lokið síðunni.
25. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
