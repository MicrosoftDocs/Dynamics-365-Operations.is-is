---
title: Stofna beiðni sem notar tilboðsbeiðni
description: Þetta efni útskýrir hvernig á að bæta verð og upplýsingar um lánardrottin við innkaupabeiðni úr Tilboðsbeiðniferli.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e67dafd02a3b2a38832d8a4f0e9809adffcbb80
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211839"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Stofna beiðni sem notar tilboðsbeiðni

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig á að bæta verð og upplýsingar um lánardrottin við innkaupabeiðni úr Tilboðsbeiðniferli. Dæmi sem sýnd eru í þessari handbók má nota í USMF fyrirtækisins sýnigögnum og þú verður að vera skráður inn sem Kerfisstjóra til að ljúka við skrefin. Verkin í þessari handbók væri yfirleitt gert af innkaupasérfræðingum.


## <a name="create-a-requisition"></a>Stofna nýja beiðni
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Innkaup og aðföng > Innkaupabeiðnir > Innkaupabeiðnir sem ég hef búið til**.
2. Veljið **Nýtt**.
3. Í reitinn **Heiti** skal slá inn gildi.
4. Í reitinn **Umbeðin dagsetning** slærðu inn dagsetningu.
5. Í reitinn **Dagsetning reikningsskila** slærðu inn dagsetningu.
6. Veljið **Í lagi**.
7. Í reitinn **Ástæða** skal slá inn eða velja gildi.
8. Veldu **Bæta við línu**.
9. Í reitnum **Innkaupategund** skal velja flokk í trénu og velja síðan **Í lagi**.
10. Í reitinn **Afurðarheiti** skal slá inn gildi.
11. Í reitnum **Magn** slærðu inn tölu.
12. Í reitinn **Eining** skal slá inn eða velja gildi.
13. Veljið **Vista**.
14. Veldu **Verkflæði** til að opna felligluggann.
15. Veldu **Senda**.
16. Lokið síðunni.
17. Veldu **Senda**.

## <a name="reassign-a-workflow-task"></a>Endurúthluta verkflæðisverki
Næsta verki er að stofna beiðni um TILBOÐ til að fá tilboð frá lánardrottnum fyrir afurðina. Í sýnigögn USMF, er verkflæði fyrir beiðni sett upp með reglu þannig að ef lánardrottinn er ekki valinn, eða einingarverð er 0 fyrir línu, er verki úthlutað á tiltekinn starfsmann til að stofna beiðni um TILBOÐ. Til að halda áfram með þessari handbók, þarf að úthluta því verki til annars notanda (sjálfur). Það er aðeins mögulegt ef notandi er innskráður sem er Admin.  

1. Veldu **Verkflæði** til að opna felligluggann.
2. Veldu **Skoða sögu**.
3. Endurhlaðið síðuna.
4. Útvíkkaðu kaflann **Rakningarupplýsingar**.
5. Í trénu velurðu línuna sem hefst á „Línuverkflæði virkjað þann“.
6. Veldu **Skoða upplýsingar um verkflæði**.
7. Útvíkkaðu kaflann **Vinnuliðir**.
8. Velja **Endurúthluta**.
9. Í reitnum **Notandi** velurðu **Stjórnandi**.
10. Velja **Endurúthluta**.
11. Lokaðu síðunum tveimur.

## <a name="create-an-rfq"></a>Búa til beiðni um tilboð

1. Endurhlaðið síðuna.
2. Veldu **Beiðni um tilboð**.
3. Í reitnum **Innkaupalögaðili** velurðu **USMF**. Velja þarf sama lögaðila sem er í innkaupabeiðnilínunni.  
4. Í listanum skal merkja valda línu. Hafirðu haft margar línur á innkaupabeiðni þinni, veldu allar línur sem þú vilt bæta við beiðni um tilboð.  
5. Veljið **Í lagi**.
6. Endurhlaðið síðuna.
7. Passaðu að upplýsingareiturinn sé opinn og útvíkkaðu síðan hlutann **Tengd skjöl**.
8. Veldu tengilinn í reitnum **Beiðni um tilboð** til að opna beiðni um tilboð sem verið var að stofna.
9. Veldu **Haus**.
10. Veljið **Bæta við**.
11. Í reitinn **Lánardrottnalykill** skal færa inn eða velja gildi.
12. Veljið **Bæta við**.
13. Í reitinn **Lánardrottnalykill** skal færa inn eða velja gildi.
14. Veljið **Senda**.
15. Veljið **Í lagi**.
16. Veldu **Færa inn svar**.
17. Í aðgerðarúðunni skal velja **Svara**.
18. Veldu **Afrita gögn í svar**. Þetta afritar gögn, eins og magn og dagsetningar, frá beiðni um TILBOÐ í svarið.  
19. Í reitnum **Einingarverð** skal slá inn tölu. Þetta er verðið sem þú hefur fengið frá lánardrottni. Þú gætir einnig viljað færið inn viðbótarupplýsingar frá lánardrottni.  
20. Veljið **Samþykkja**.
21. Veljið **Í lagi**.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Staðfestið að verð og lánardrottinn hafa verið fluttar í beiðni.
1. Lokið síðunni.
2. Veldu **Línur**.
3. Veldu **Tengdar upplýsingar**.
4. Veldu **Innkaupabeiðni**.
5. Veldu sú lína sem var flutt á beiðni um tilboð. Staðfestið að verð og lánardrottinn hafa verið afritaðar í beiðni.  
6. Veldu **Verkflæði** til að opna felligluggann.
7. Velja Lokið.
8. Veldu síðuna.
9. Velja Lokið.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]