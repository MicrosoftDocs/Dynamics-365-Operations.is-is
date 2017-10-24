--- 
title: "Stofna beiðni sem notar tilboðsbeiðni"
description: "Þessari handbók sýnir hvernig á að bæta verð og upplýsingar um lánardrottin við innkaupabeiðni úr Tilboðsbeiðniferli."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d97ccd15031b2f7398486eee4a716ecef5e9dafd
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Stofna beiðni sem notar tilboðsbeiðni

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessari handbók sýnir hvernig á að bæta verð og upplýsingar um lánardrottin við innkaupabeiðni úr Tilboðsbeiðniferli. Dæmi sem sýnd eru í þessari handbók má nota í USMF fyrirtækisins sýnigögnum og þú verður að vera skráður inn sem Kerfisstjóra til að ljúka við skrefin. Verkin í þessari handbók væri yfirleitt gert af innkaupasérfræðingum.


## <a name="create-a-requisition"></a>Stofna nýja beiðni
1. Fara í Innkaup og uppruni > Innkaupabeiðnir > Innkaupabeiðnir sem ég hef.
2. Smellið á „Nýtt“.
3. Í reitinn Heiti skal slá inn gildi.
4. Dagsetning er rituð í reitinn umbeðin dagsetning:.
5. Dagsetning er rituð í reitinn dagsetning reikningsskila.
6. Smellt er á Í lagi.
7. Í reitinn Ástæða skal slá inn eða veldu gildi.
8. Smellið á „Bæta við línu“.
9. Í reitnum Innkaupategund skal velja tegund í trénu og smella síðan á Í lagi.
10. Í reitinn Afurðarheiti skal slá inn gildi.
11. Færið inn númer í reitnum „Magn“.
12. Í reitinn eining skal slá inn eða velja gildi.
13. Smellið á „Vista“.
14. Smellt er á Verkflæði til að opna felligluggann.
15. Smelltu á Senda.
16. Lokið síðunni.
17. Smelltu á Senda.

## <a name="reassign-a-workflow-task"></a>Endurúthluta verkflæðisverki
    * Næsta verki er að stofna beiðni um TILBOÐ til að fá tilboð frá lánardrottnum fyrir afurðina. Í sýnigögn USMF, er verkflæði fyrir beiðni sett upp með reglu þannig að ef lánardrottinn er ekki valinn, eða einingarverð er 0 fyrir línu, er verki úthlutað á tiltekinn starfsmann til að stofna beiðni um TILBOÐ. Til að halda áfram með þessari handbók, þarf að úthluta því verki til annars notanda (sjálfur). Það er aðeins mögulegt ef notandi er innskráður sem er Admin.  
1. Smellt er á Verkflæði til að opna felligluggann.
2. Smella á Skoða sögu
3. Endurhlaðið síðuna.
4. Útvíkka hlutann rakningarupplýsingar.
5. Veljið "línu sem byrjar á"Verkflæði virkjað á"" á trénu.
6. Smella á Skoða upplýsingar um verkflæði
7. Útvíkka hlutann vinnuliðir.
8. Smellið á endurúthluta.
9. Í notandareitnum, velurðu „Admin“.
10. Smellið á endurúthluta.
11. Lokið síðunni.
12. Lokið síðunni.

## <a name="create-an-rfq"></a>Búa til beiðni um tilboð
1. Endurhlaðið síðuna.
2. Smella á beiðni um tilboð
3. Veldu USMF í reitnum lögaðili sem kaupir.
    * Velja þarf sama lögaðila sem er í innkaupabeiðnilína.  
4. Í listanum skal merkja valda línu.
    * Hafirðu haft margar línur á innkaupabeiðni þinni, veldu allar línur sem þú vilt bæta við beiðni um tilboð.  
5. Smellið á „Í lagi“.
6. Endurhlaðið síðuna.
7. Opna Upplýsingakassa og útvíkka svo hlutann Tengd skjöl.
    * Þú gætir hugsanlega nú þegar verið með Upplýsingakassa opinn. Leita að tákn með ör á, hægra megin við víxlhnappana Línur/Haus. Ef örin vísar til hægri er Upplýsingakassa þegar opinn. Ef ör vísar til vinstri, skal smella á til að opna Upplýsingakassa.  
8. Smelltu á tengil á svæðinu Beiðni um tilboð til að opna beiðni um TILBOÐ sem verið var að stofna.
9. Smellið á Haus.
10. Smelltu á Bæta við.
11. Færa inn eða veljið gildi í svæðinu lánardrottnalykill.
12. Smelltu á Bæta við.
13. Færa inn eða veljið gildi í svæðinu lánardrottnalykill.
14. Smellt er á Senda.
15. Smellið á „Í lagi“.
16. Smella á Færa inn svar
17. Smellið á Svara á aðgerðarúðunni.
18. Smella á Afrita gögn til að svara.
    * Þetta afritar gögn, eins og magn og dagsetningar, frá beiðni um TILBOÐ í svarið.  
19. Færið inn númer í reitnum „Einingarverð“.
    * Þetta er verðið sem þú hefur fengið frá lánardrottni. Þú gætir einnig viljað færið inn viðbótarupplýsingar frá lánardrottni.  
20. Smellið á Samþykkja.
21. Smellið á „Í lagi“.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Staðfestið að verð og lánardrottinn hafa verið fluttar í beiðni.
1. Lokið síðunni.
2. Smellið á „Línur“.
3. Smelltu á Tengdar upplýsingar.
4. Smella á innkaupabeiðni
5. Veldu sú lína sem var flutt á beiðni um tilboð.
    * Staðfestið að verð og lánardrottinn hafa verið afritaðar í beiðni.  
6. Smellt er á Verkflæði til að opna felligluggann.
7. Smelltu á Ljúka.
8. Lokið síðunni.
9. Smelltu á Ljúka.


