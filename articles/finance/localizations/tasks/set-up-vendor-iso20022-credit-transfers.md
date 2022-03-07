---
title: Setja upp lánardrottna og bankareikninga lánardrottna fyrir ISO20022-tmillifærslur
description: Þetta ferli sýnir hvernig á að setja upp lánardrottins og bankareikningsupplýsingar fyrir lánardrottinn sem þarf fyrir myndun ISO20022-greiðsluskrár fyrir millifærsla fjármuna eða hvers kyns aðra greiðsluskrá lánardrottins.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7a901591f9f3d1a892c29f92e59dc96c1f172143cae6bec571da33b4a50d274
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723720"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Setja upp lánardrottna og bankareikninga lánardrottna fyrir ISO20022-tmillifærslur

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]