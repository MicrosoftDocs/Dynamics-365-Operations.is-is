---
title: Uppsetning vörusendingar
description: Í þessu efnisatriði er útskýrt hvernig á að skilgreina aðgerðir vörusendingabirgða á innleið.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bcc5ce7d9b9031fe8e9589798e07162106277767
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987280"
---
# <a name="set-up-consignment"></a>Uppsetning vörusendingar

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að skilgreina aðgerðir vörusendingabirgða á innleið.

Vörusendingarbirgðir eru birgðir sem eru í eigu lánardrottinn en geymd á þínu svæði. Þegar þú ert tilbúinn að nota eða neyta birgða, tekurðu yfir eignarhald birgðanna. Þetta efnisatriði lýsir uppsetningu sem þarf til að virkja ferli vörusendingar. Frekari upplýsingar um hvernig ferli vörusendinga eru í [Setja upp vörusendingu](consignment.md).

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
Ef lánardrottnana þínir nota viðmót fyrir samstarf lánardrottna, geta þeir nota þetta að vakta notkun á birgðum á þínu svæði. Nánari upplýsingar um uppsetningu á lánardrottnum til að nota samstarf lánardrottna er að finna í [Öryggi notanda í gátt lánardrottins](../procurement/configure-security-vendor-portal-users.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]