---
title: Setja upp verktakamiða fyrir lánardrottna
description: Þetta ferli fer í gegnum stofnun á íslenskum verktakamiða.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport,  VendInvoiceDeclaration_IS
audience: Application User
ms.reviewer: kfend
ms.search.region: Iceland
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 412204bdb23594ce56949170813dd85bb7873ada9008e132401c5ce15a30d9bf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738408"
---
# <a name="set-up-an-invoice-declaration-for-vendors"></a>Setja upp verktakamiða fyrir lánardrottna

[!include [banner](../../includes/banner.md)]

Þetta ferli fer í gegnum stofnun á íslenskum verktakamiða. Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF með land aðalaðsetur lögaðila uppfært í Ísland.


## <a name="import-invoice-declaration-ger-configurations"></a>Flytja inn GER-skilgreiningar verktakamiða
1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
2. Smellt á Stilla sem virkt.
3. Smella á Geymslur.
4. Smellt er á Opin.
5. Smellt er á Sýna síur.
    * Vinsamlegast bættu við skilyrði til að sía eftir heiti grunnstillingar og færðu inn verktakamiða lánardrottins (IS) eða finndu skilgreiningu á listanum, veldu það og farðu í næsta skref.  
6. Nota eftirfarandi síur: %3
7. Smelltu á Flytja inn.
8. Smella á Já.
9. Bæta við síu
    * Bættu við skilyrði til að sía eftir heiti grunnstillingar og færðu inn skýrslu verktakamiða lánardrottins (IS) eða finndu skilgreiningu á listanum, veldu það og farðu í næsta skref.  
10. Nota eftirfarandi síur: %3
11. Smelltu á Flytja inn.
12. Smella á Já.

## <a name="enable-vendor-invoice-declaration"></a>Virkja reikningsskýrslu lánardrottins
1. Fara í Viðskiptaskuldir > Uppsetning > Verktakamiðar lánardrottins.
2. Smellið á „Nýtt“.
3. Í reitnum Reikningur skal slá inn 'SubC'.
4. Í reitnum Lýsing skal slá inn ‚Undirverktaki‘.
5. Í svæðinu fyrir Skýrslugerðakóði skal slá inn '06'.
6. Smellt er á Nýtt.
7. Færa skal inn 'Gjafakort' í svæðið Verktakamiðar.
8. Færa skal inn 'Gjafakort‘ í reitinn Lýsing.
9. Í svæðinu fyrir Skýrslugerðarkóða skal slá inn '34'.
10. Í reitnum Færslugerð skal velja ‚LA‘.
11. Smellið á „Vista“.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]