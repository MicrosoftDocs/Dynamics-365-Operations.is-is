---
title: Stofna og flytja út greiðslur lánardrottna með ISO20022-greiðslusniði
description: Þetta ferli sýnir hvernig á að stofna greiðslulínur í greiðslubók lánardrottins og mynda greiðsluskrá lánardrottins með því að nota dæmi um ISO2022 millifærsla fjármuna.
author: mrolecki
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ac84055586eff678ea489b35198b1c2dfab13658
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856468"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Stofna og flytja út greiðslur lánardrottna með ISO20022-greiðslusniði

[!include [banner](../../includes/banner.md)]

Þessi grein útskýrir hvernig á að búa til greiðslulínur í greiðslubók lánardrottins og búa til greiðsluskrá lánardrottins með því að nota ISO2022 Kreditmillifærslu dæmi.

Þetta fimmta ferli af fimm sem sýna greiðsluferlinu lánardrottins með því að nota grunnstillingar fyrir rafræna skýrslugerð. Notaðu DEMF-sýnigögnin til að ljúka þessu dæmi.

## <a name="example"></a>Dæmi

1.    Fara í **Viðskiptaskuldir > Greiðslur > Greiðslubók**.
2.    Smellt er á **Nýtt**.
3.    Sláið inn eða veldu gildi í reitnum **Heiti**.
4.    Smelltu á **Línur > Greiðslutillaga > Stofna greiðslutillögu**.
5.    Útvíkka **Færslur til að taka með** hlutann.
6.    Smella á **Sía**.
7.    Á listanum skal velja línuna fyrir töflu **Lánardrottna** og reitinn fyrir **Lánardrottnalykil**.
8.    Í reitinn **Skilyrði** skal slá inn eða velja gildi. Þú getur notað hvaða skilyrði sem er til að velja lánardrottnafærslur til að greiða, í þessu dæmi notaðu DE-001 sem lánardrottnalykil.
12.    Smellið á **Í lagi**.
13.    Smellið á **Í lagi**.
14.    Smellt er á **Stofna greiðslur**.
15. Mynda ISO20022-greiðsluskrá.
    1.    Smelltu á **Mynda greiðslur**.
    2.    Færa inn eða velja gildi í reitnum **Greiðsluaðferð**.
    3.    Í reitinn **Skráarheiti** skal slá inn gildi. Fyrir þetta dæmi, vegna EUR greiðslu, verður myndaða skráin samhæf SEPA. Einnig er hægt að nota ISO20022 kreditfærslur ásamt öðrum greiðslusniðum lánardrottins til að búa til greiðslur í öðrum gjaldmiðlum.
    4.    Færa inn eða veljið gildi í svæðinu **Bankareikningur**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]