--- 
title: "Setja upp lánardrottna og bankareikninga lánardrottna fyrir ISO20022-tmillifærslur"
description: "Þetta ferli sýnir hvernig á að setja upp lánardrottins og bankareikningsupplýsingar fyrir lánardrottinn sem þarf fyrir myndun ISO20022-greiðsluskrár fyrir millifærsla fjármuna eða hvers kyns aðra greiðsluskrá lánardrottins."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 147d8fa82bf15c984ad263cada42789038fa7371
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Setja upp lánardrottna og bankareikninga lánardrottna fyrir ISO20022-tmillifærslur

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli sýnir hvernig á að setja upp lánardrottins og bankareikningsupplýsingar fyrir lánardrottinn sem þarf fyrir myndun ISO20022-greiðsluskrár fyrir millifærsla fjármuna eða hvers kyns aðra greiðsluskrá lánardrottins. 

Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF.
Þetta fjórða ferli af fimm sem sýna greiðsluferlinu lánardrottins með því að nota grunnstillingar fyrir rafræna skýrslugerð. Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="set-up-bank-details"></a>Setja upp upplýsingar um banka
1. Farið í Viðskiptaskuldir > Lánardrottnar > Allir lánardrottnar.
2. Nota flýtiafmörkun til að finna færslur Til dæmis, sía svæðið Lánardrottins með gildið 'DE-001'.
3. Smellt er á DE-001 til að opna upplýsingar um lánardrottin.
4. Í aðgerðasvæðinu er smellt á lánardrottinn.
5. Smellt er á bankareikninga.
6. Smellið á „Breyta“.
    * Ef engin bankareikningurinn er tiltækur, þarf að stofna nýja.  
7. Í svæðinu swift-kóði færðu inn 'COBADEFFXXX' .
8. Í reitinn IBAN skal slá inn 'DE36200400000628808808'.
9. Lokið síðunni.

## <a name="set-up-a-method-of-payment-for-the-vendor"></a>Setja upp greiðsluhátt fyrir lánardrottinn
1. Smellið á „Breyta“.
2. Stækka eða fella saman hlutann Greiðsla.
3. Í reitnum greiðsluaðferð skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal smella á tengilinn í SEPA CT línu.
5. Smellið á „Vista“.


