---
title: Setja upp reglur lánardrottnareikninga
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp reikningsreglur lánardrottins.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1f9707c7b283f42729126efa57e890e0df65ca8b
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109757"
---
# <a name="set-up-vendor-invoice-policies"></a>Setja upp reglur lánardrottnareikninga

[!include [banner](../../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að setja upp reikningsreglur lánardrottins. Reikningsreglur lánardrottins eru keyrðar þegar þú bókar reikning lánardrottins með því að nota **Reikningur seljanda** síðu og þegar þú opnar reikning lánardrottins **Brot á stefnu** síðu. Einnig er hægt að skilgreina verkflæði fyrir reikning lánardrottins til að keyra reikningsreglur lánardrottins í hvert skipti sem er sendur er reikning til verkflæðis. 

- Reikningsreglur lánardrottins eiga ekki við reikninga sem voru stofnaðar í komubók eða reikningabók.  
- Samsvörun reikninga notar ekki reikningsreglur lánardrottins, en er þess í stað sett upp í **Færibreytur viðskiptaskulda** síðu.  
- Þessi skráning notar sýnigögn USMF fyrirtækis hlutverk viðskiptaskuldastjóri eða aðalbókari myndi framkvæma þessi skrefum. Áður en þú byrjar skaltu ganga úr skugga um að **Samsvörun reikninga** stillingarlykill er valinn.


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
