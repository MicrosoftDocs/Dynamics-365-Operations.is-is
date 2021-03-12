---
title: Setja upp reglur lánardrottnareikninga
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp reikningsreglur lánardrottins.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79cbabba74fdb76d8fcc0553d39e0f140aacf03e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995453"
---
# <a name="set-up-vendor-invoice-policies"></a>Setja upp reglur lánardrottnareikninga

[!include [banner](../../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að setja upp reikningsreglur lánardrottins. Reikningsreglur lánardrottins eru keyrðar þegar reikningur lánardrottins er bókaður með því að nota síðuna fyrir reikning Lánardrottins og þegar síðan fyrir brot á reikningsreglum lánardrottins er opnuð. Einnig er hægt að skilgreina verkflæði fyrir reikning lánardrottins til að keyra reikningsreglur lánardrottins í hvert skipti sem er sendur er reikning til verkflæðis. 

- Reikningsreglur lánardrottins eiga ekki við reikninga sem voru stofnaðar í komubók eða reikningabók.  
- Sannprófun á reikningsjöfnun notar ekki reikningsreglur lánardrottins, en er í staðinn sett upp á síðunni færibreytur viðskiptaskulda.  
- Þessi skráning notar sýnigögn USMF fyrirtækis hlutverk viðskiptaskuldastjóri eða aðalbókari myndi framkvæma þessi skrefum. Áður en hafist er handa þarf að ganga úr skugga um að skilgreiningarlykill reikningsjöfnunar sé valinn.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Undirbúa stofnun stefna um reikninga lánardrottins
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Viðskiptaskuldir > Uppsetning > Færibreytur viðskiptaskulda**.
2. Veldu flipann **Staðfesting reiknings**.
3. Veldu eða hreinsaðu gátreitinn **uppfæra sjálfvirkt stöðu fyrirsögn reiknings**.
4. Veljið **Í lagi**.
5. Í reitnum **Bóka reikning með misræmi** skal velja valkost.
6. Lokið síðunni.
7. Farðu Í **Skoðunarrúðu > Einingar > Viðskiptaskuldir > Regluuppsetning > Reikningrelgur lánardrottins**.
8. Velja **færibreytur**.
9. Veljið **Bæta við**.
10. Lokið síðunni til að fara aftur á heimasíðuna.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Stofna stefnureglugerðir fyrir reikninga lánardrottins
1. Farðu Í **Skoðunarrúðu > Einingar > Viðskiptaskuldir > Regluuppsetning > Reglugerðir reiknings lánardrottins**.
2. Veljið **Nýtt**.
3. Færið inn gildi í reitina **Heiti reglu** og **Lýsing**.
4. Í reitnum **Fyrirspurnarheiti** veldu fellivalmyndina til að opna leitina og veldu síðan viðeigandi skrá.
5. Veljið **Vista**.
6. Lokið síðunni til að fara aftur á heimasíðuna.

## <a name="define-a-vendor-invoice-policy"></a>Skilgreina stefna fyrir reikning lánardrottins
1. Farðu Í **Skoðunarrúðu > Einingar > Viðskiptaskuldir > Regluuppsetning > Reikningrelgur lánardrottins**.
2. Veljið **Nýtt**.
3. Færið inn gildi í reitina **Heiti** og **Lýsing**.
4. Útvíkka eða draga saman hlutann **fyrirtækisregla**.
5. Í trénu skal velja **Contoso Entertainment System USA**.
6. Veljið **Bæta við**.
7. Útvíkka eða draga saman hlutann **stefnuregla**.
8. Veldu **stefnureglu**.
9. í reitnum **Lýsing stefnuregla** skal slá inn gildi.
10. Velja **Síu**.
11. Veljið **Bæta við**. Velja virku æskilega skrá.
12. Í reitunum **Tafla**, **Afleidd tafla**, og **Reitur**, veldu eða sláðu inn valkosti í fellivalmyndunum.
13. Lokið síðunni.
14. Í reitnum **Skilyrði** skal slá inn gildi.
15. Veljið **Í lagi**.
16. Veljið **Í lagi**.
17. Lokið síðunum til að fara aftur á heimasíðuna.

