---
title: Búa til gerðir auglýsinga og viðmið fyrir stigagjöf fyrir tilboðsbeiðnir
description: Þessari handbók sýnir hvernig á að stofna gerð beiðni og tengja þetta við aðferð við stigagjöf.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b3876238a191cbbacc4e8c435bb798232e6fd6f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430438"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a>Búa til gerðir auglýsinga og viðmið fyrir stigagjöf fyrir tilboðsbeiðnir

[!include [banner](../../includes/banner.md)]

Þessari handbók sýnir hvernig á að stofna gerð beiðni og tengja þetta við aðferð við stigagjöf. Hún sýnir einnig hvernig á að nota gerð beiðni fyrir beiðni um tilboð (BUT) sem ákvarðar síðan sjálfgefna aðferð við stigagjöf. Þessum verkefnum myndi venjulega að framkvæma af Innkaupastjóra. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn. Þú þarft að hafa aðferð við stigagjöf tiltækt áður en byrjað er.


## <a name="create-a-solicitation-type"></a>Stofna gerð beiðnar
1. Farið í Innkaup og aðföng > Uppsetning > Tilboðsbeiðni > Gerð beiðni.
2. Smellið á „Nýtt“.
3. Í reitinn Heiti skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í svæðinu aðferð við Stigagjöf, skal velja stigagjöf sem á að nota fyrir þessa gerð beiðni.
6. Smellið á „Vista“.
7. Lokið síðunni.

## <a name="use-the-solicitation-type"></a>Nota Gerð beiðni
1. Fara í innkaup og aðföng > Beiðnir um tilboð > Allar beiðnir um tilboð.
2. Smellið á „Nýtt“.
3. Í reitnum gerð beiðni skal velja gerð beiðni sem þú varst að stofna. 
    *   
4. Smellið á „Í lagi“.
5. Afrita skilyrði fyrir stigagjöf
    * Sýndar stigagjafir eru þær sem koma úr aðferð við stigagjöf sem þú tengdir við gerð beiðninnar. Hægt er að velja að bæta við eða eyða skilyrði á þessari síðu. Einnig er hægt að bæta við nýjum skilyrði með því að afrita þær frá öðrum aðferðir við stigagjöf .  
6. Smella á Afrita skilyrði
7. Færa inn eða velja gildi í reitnum aðferð við stigagjöf.
8. Smellið á „Í lagi“.
9. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]