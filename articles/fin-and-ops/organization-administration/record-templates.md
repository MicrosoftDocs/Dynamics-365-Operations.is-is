---
title: "Færslusniðmát"
description: "Þessi grein kynnir hugtakið skýrslusnið og útskýrir hvernig hægt er að nota þau til að stofna skýrslur sem deila upplýsingum."
author: pvillads
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e89e4a74550597a4e497a1128fe91c07e766d697
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="record-templates"></a>Færslusniðmát

[!include[banner](../includes/banner.md)]


Þessi grein kynnir hugtakið skýrslusnið og útskýrir hvernig hægt er að nota þau til að stofna skýrslur sem deila upplýsingum.

Færslusniðmát geta hjálpað til við að stofna færslur hraðar í Microsoft Dynamics 365 for Finance and Operations. Aðeins er hægt að stofna færslusniðmát fyrir sumar af færslugerðunum í Microsoft Dynamics 365 for Finance and Operations. 

Til dæmis hugsum okkur að verið sé að færa inn upplýsingar um leigu bílaleigufyrirtækis sem er staðsett í San Francisco. Þar sem flestir viðskiptavina eru líklega frá San Francisco svæðinu, væri gott ef hægt væri að fylla sjálfkrafa út gildi°fyrir°**Fylki**, **Land**, og **Borg** svæðin á leiguskjámyndinni. 

> [!Note]
> Aðeins er hægt að nota sniðmát fyrir þau svæði Finance and Operations sem viðkomandi hefur aðgang að. Hins vegar eru öll sniðmátsheiti sýnileg öllum notendum þegar ný færsla er stofnuð, ef verið er að stofna sniðmát sem verða svo aðgengileg fyrir alla notendur. Gætið þess að þetta í huga þegar sniðmát eru nefnd. Til dæmis ætti að forðast að nota heiti með orðum eins og „kaupauki“ ef það er trúnaðarmál að sumir starfsmenn fá greidda kaupauka. 

Þegar eitt eða fleiri sniðmát sem viðkomandi hefur aðgang að eru til fyrir tiltekna skjámynd og reynt er að stofna nýja færslu í skjámyndinni birtist **Velja sniðmát** síðan. Þegar sniðmát er valið úr listanum er nýja færslan stofnuð og inniheldur hún sjálfgefnar upplýsingar sem eru byggðar á sniðmátinu sem valið er. Ef ekki á að nota sniðmát þegar nýjar færslur eru stofnaðar skal velja **Ekki spyrja aftur** gátreit á síðunni **Velja sniðmát fyrir**. Til að birta svargluggann fyrir sniðmátsval aftur skal hægrismella á hvaða færslu sem er, smella svo á **Færsluupplýsingar**, og svo á **Sýna sniðmátsval**.



