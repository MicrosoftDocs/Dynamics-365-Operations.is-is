---
title: Stofna og flytja út greiðslur lánardrottna með ISO20022-greiðslusniði
description: Þetta ferli sýnir hvernig á að stofna greiðslulínur í greiðslubók lánardrottins og mynda greiðsluskrá lánardrottins með því að nota dæmi um ISO2022 millifærsla fjármuna.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b589d64a4446420164175b41f435cf48daac01a9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "340546"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Stofna og flytja út greiðslur lánardrottna með ISO20022-greiðslusniði

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta efnisatriði sýnir hvernig á að stofna greiðslulínur í greiðslubók lánardrottins og mynda greiðsluskrá lánardrottins með því að nota dæmi um ISO2022 millifærsla fjármuna.

Þetta fimmta ferli af fimm sem sýna greiðsluferlinu lánardrottins með því að nota grunnstillingar fyrir rafræna skýrslugerð. Notaðu DEMF-sýnigögnin til að ljúka þessu dæmi.

## <a name="example"></a>Dæmi

1.  Fara í **Viðskiptaskuldir > Greiðslur > Greiðslubók**.
2.  Smellt er á **Nýtt**.
3.  Sláið inn eða veldu gildi í reitnum **Heiti**.
4.  Smelltu á **Línur > Greiðslutillaga > Stofna greiðslutillögu**.
5.  Útvíkka **Færslur til að taka með** hlutann.
6.  Smella á **Sía**.
7.  Á listanum skal velja línuna fyrir töflu **Lánardrottna** og reitinn fyrir **Lánardrottnalykil**.
8.  Í reitinn **Skilyrði** skal slá inn eða velja gildi. Þú getur notað hvaða skilyrði sem er til að velja lánardrottnafærslur til að greiða, í þessu dæmi notaðu DE-001 sem lánardrottnalykil.
12. Smellið á **Í lagi**.
13. Smellið á **Í lagi**.
14. Smellt er á **Stofna greiðslur**.
15. Mynda ISO20022-greiðsluskrá.
    1.  Smelltu á **Mynda greiðslur**.
    2.  Færa inn eða velja gildi í reitnum **Greiðsluaðferð**.
    3.  Í reitinn **Skráarheiti** skal slá inn gildi. Fyrir þetta dæmi, vegna EUR greiðslu, verður myndaða skráin samhæf SEPA. Einnig er hægt að nota ISO20022 kreditfærslur ásamt öðrum greiðslusniðum lánardrottins til að búa til greiðslur í öðrum gjaldmiðlum.
    4.  Færa inn eða veljið gildi í svæðinu **Bankareikningur**.

