---
title: "Uppsetning vörusendingar"
description: "Í þessu efnisatriði er útskýrt hvernig á að skilgreina aðgerðir vörusendingabirgða á innleið."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b8692a3033cd665402721ea18ba8c28557c049de
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017

---

# <a name="set-up-consignment"></a>Uppsetning vörusendingar

[!include[banner](../includes/banner.md)]


Í þessu efnisatriði er útskýrt hvernig á að skilgreina aðgerðir vörusendingabirgða á innleið. 

Vörusendingarbirgðir eru birgðir sem eru í eigu lánardrottinn en geymd á þínu svæði. Þegar þú ert tilbúinn að nota eða neyta birgða, tekurðu yfir eignarhald birgðanna. Þetta efnisatriði lýsir uppsetningu sem þarf til að virkja ferli vörusendingar. Frekari upplýsingar um hvernig ferli vörusendinga eru í [vörusending](consignment.md).

## <a name="inventory-owners"></a>Birgðaeigendur
Til að skrá efnislegar vörusendingabirgðir á innleið, þarf að skilgreina lánardrottinseiganda. Þetta er gert á **eigandi birgða** síðuna. Þegar velja **lánardrottnalykil** myndar þetta sjálfgefin gildi fyrir **Heiti** og **Eigandi** svæðum. Gildið í **Eiganda** svæði verður sýnilegt til lánadrottna, svo þú gætir viljað breyta þeim, ef nöfn á lánardrottnalykill eru ekki auðvelt fyrir utanaðkomandi fólki til að bera kennsl á. Mögulegt er að breyta á **Eigandi** svæði, en aðeins fram að þeim punkti þegar vista á **eigandi birgða** færslan. Í **Heiti** svæði er fyllt út með nafn þess aðila sem lánardrottnalykill er tengd við, og þessu er ekki hægt að breyta. 

[![birgðaeigendur](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Rakningarvíddarflokkur
Vörur sem nota á í ferli vörusendingar verður að tengjast við **rakningarvíddarflokkur** þar sem víddin **Eigandi** er stillt á **Virk**. Vídd eiganda hefur ávallt **Efnislegar birgðir** og **Fjárhagslegar birgðir** valkostir valinn. **Þekjuáætlun eftir vídd** er aldrei valin. 

[![rakningarvíddarflokkur](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>Færslubók eignarhaldsbreytingar birgða
**Birgðafærslubók fyrir breytingu á eignarhaldi** er notuð til að rekja flutninga á eignarhaldi vörusendingabirgða úr lánardrottni í núverandi lögaðila sem neytir þess. Eins og öllum birgðabók verður það að vera tilgreindur með heiti birgðabókar. Þessi nöfn eru stofnaðar á **heiti birgðabóka** síðuna og **færslubókargerð** verður að vera stillt á **breytingu á Eignarhaldi**. 

[![færslubók eignarhaldsbreytingar birgða](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Samstarf lánardrottna í ferli vörusendingar
Ef lánardrottnana þínir nota viðmót fyrir samstarf lánardrottna, geta þeir nota þetta að vakta notkun á birgðum á þínu svæði. Nánari upplýsingar um uppsetningu á lánardrottnum til að nota samstarf lánardrottna sjá[Skilgreining öryggis fyrir Notendur samstarfs lánardrottna](../procurement/configure-security-vendor-portal-users.md).




