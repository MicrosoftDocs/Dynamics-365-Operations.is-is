---
title: Virkja launaferli fyrir tíma og mætingu
description: Þessi verklýsing sýnir hvernig á að virkja launavinnslu í tími og mæting.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5805cc31bf9c7c2231defab63dc9a1e67f82622a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206957"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a>Virkja launaferli fyrir tíma og mætingu

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að virkja launavinnslu í tími og mæting. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="create-a-pay-type-with-a-related-pay-rate"></a>Stofna launagerð með tengdum launataxta
1. Tími og viðvera > Setja upp > Laun > Launagerð
2. Smellið á „Nýtt“.
3. Í reitinn launagerð skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Smellið á „Vista“.
6. Smellt er á Taxta.
    * Taxtar fyrir launagerðir eru settar upp fyrir tiltekin tímabil, og einstakir taxtar má stofna fyrir starfsmenn Það er ekki alltaf nauðsynlegt að stofna taxta fyrir launagerðir fyrir tími og mæting. Þessar upplýsingar gætu þegar verið til staðar í launakerfi sem notað til að mynda laun.  
7. Smellið á „Nýtt“.
8. Í listanum skal merkja valda línu.
9. Í reitinn taxtar skal slá inn númer.
10. Smellið á „Vista“.

## <a name="create-a-pay-agreement"></a>Stofna launasamning
1. Lokið síðunni.
2. Lokið síðunni.
3. Fara á launasamninga.
    * Tími og viðvera > Setja upp > Launagerð  
4. Smellið á „Nýtt“.
5. Færa inn gildi í svæðinu launasamningur.
6. Sláið inn gildi í reitnum „Lýsing“.
7. Smellið á „Vista“.
8. Smellið á samningslínur.
9. Smellið á „Nýtt“.
10. Í listanum skal merkja valda línu.
11. Færa inn eða veljið gildi í svæðinu gerð forstillingar.
12. Færa inn eða veljið gildi í svæðinu launagerð.

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a>Setja upp launasamning fyrir tíma og skráningu starfsmann
1. Lokið síðunni.
2. Lokið síðunni.
3. Fara í starfsmaður sem sinnir tímaskráningu
    * Tími og viðvera > Setja upp > Starfsmaður sem sinnir tímaskráningu  
4. Í listanum skal smella á tengilinn í valinni línu.
5. Smellið á flipann Ráðningar.
6. Útvíkka hlutann tímaskráning.
7. Smellið á „Breyta“.
8. Sláðu inn eða veldu gildi í reitnum launasamningur.

