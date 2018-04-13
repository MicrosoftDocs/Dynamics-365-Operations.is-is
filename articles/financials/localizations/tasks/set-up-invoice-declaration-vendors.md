--- 
title: "Setja upp verktakamiða fyrir lánardrottinn (Ísland)"
description: "Þetta ferli fer í gegnum stofnun á íslenskum verktakamiða."
author: mrolecki
manager: AnnBe
ms.date: 05/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Iceland
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7ce7101270ae3e59a6484b2f0efe0bd06f4a7c45
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-an-invoice-declaration-for-vendors-iceland"></a>Setja upp verktakamiða fyrir lánardrottinn (Ísland)

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli fer í gegnum stofnun á íslenskum verktakamiða. Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF með land aðalaðsetur lögaðila uppfært í Ísland.


## <a name="import-invoice-declaration-ger-configurations"></a>Flytja inn GER-skilgreiningar verktakamiða
1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
2. Smellt á Stilla sem virkt.
3. Smella á Geymslur.
4. Smellt er á Opin.
5. Smellt er á Sýna síur.
    * Vinsamlegast bættu við skilyrði til að sía eftir heiti grunnstillingar og færðu inn verktakamiða lánardrottins (IS) eða finndu skilgreiningu á listanum, veldu það og farðu í næsta skref.  
6. Notaðu eftirfarandi síur: %3
7. Smelltu á Flytja inn.
8. Smella á Já.
9. Bæta við síu
    * Bættu við skilyrði til að sía eftir heiti grunnstillingar og færðu inn skýrslu verktakamiða lánardrottins (IS) eða finndu skilgreiningu á listanum, veldu það og farðu í næsta skref.  
10. Notaðu eftirfarandi síur: %3
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


