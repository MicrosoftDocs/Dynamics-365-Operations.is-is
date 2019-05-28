---
title: Setja upp verktakamiða fyrir lánardrottna
description: Þetta ferli fer í gegnum stofnun á íslenskum verktakamiða.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport,  VendInvoiceDeclaration_IS
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Iceland
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90c34917ff885eca794d25042f3c924686f8869d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537991"
---
# <a name="set-up-an-invoice-declaration-for-vendors"></a>Setja upp verktakamiða fyrir lánardrottna

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

