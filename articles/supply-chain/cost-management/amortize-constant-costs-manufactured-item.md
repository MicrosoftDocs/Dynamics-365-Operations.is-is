---
title: "Afskriftir fasts kostnaðar framleiddrar vöru"
description: "Fastur kostnaður framleiddrar vöru endurspeglar uppsetningartíma og íhlutina sem eru með föstu magni eða fastri rýrnunartölu."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: AndersGirke
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: b5345fde8e77b75fd160d08153b19a9be01f18ab
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="amortize-constant-costs-for-a-manufactured-item"></a>Afskriftir fasts kostnaðar framleiddrar vöru

[!include[banner](../includes/banner.md)]


Fastur kostnaður framleiddrar vöru endurspeglar uppsetningartíma og íhlutina sem eru með föstu magni eða fastri rýrnunartölu. 

Hugtakið kostnaðarlotustærð er notað til að afskrifa þennan fasta kostnað í reiknuðum kostnaði framleiddrar vöru. Þetta hugtak er með nokkur samheiti, svo sem lotustærð bókhalds. Hugtakið afskrifaður fastur kostnaður hefur einnig ýmis samheiti, eitt af því hlutfallslegan fastan kostnað.

Magn kostnaðarlotustærðar fyrir framleidda vöru er notað í uppskrift. Magnið fer eftir því hvernig uppskriftarútreikningurinn er frumstilltur og gerður, eins og sést af eftirfarandi:

-   Sjálfgefið útreikningsmagn í uppskriftarútreikningi vöru − Staðlað pöntunarmagn vörunnar fyrir birgðir er sjálfgildi fyrir kostnaðarlotustærðina en sjálfgildið getur verið meira magn til að sýna pöntunarmagnsmargfeldi vörunnar. Hægt er að skilgreina staðlað pöntunarmagn vöru og margfeldi í sjálfgefnum pöntunarstillingum hennar eða svæðispöntunarstillingum hennar.
-   Tiltekið útreikningsmagn í uppskriftarútreikningi vöru − Tiltekna útreikningsmagnið þjónar sem kostnaðarlotustærð fyrir vöruna. Útreiknað magn notar upphaflega staðlað pöntunarmagn vörunnar, en hægt er að skrifa yfir sjálfgefið gildi. Tilgreint útreikningsmagn táknar kostnaðarlotustærð fyrir tilgreindu vöruna og fyrir framleidda íhluti með uppskriftarlínu af gerðinni framleiðsla. Þetta er þar sem gert er ráð fyrir því að það íhluturinn verði framleiddur í nákvæmu magni. Kostnaðarlotustærð annarra framleiddra þátta sem hafa línugerð uppskriftar vöru munu endurspegla staðlað pöntunarmagn.
-   Tiltekið útreikningsmagn eftir pöntun í uppskriftarútreikningi  vöru − Tiltekna útreikningsmagnið er haft sem kostnaðarlotustærð fyrir vöruna og framleidda íhluti hennar þegar uppskriftarútreikningar nota niðurbrotsaðferðina "eftir pöntun". Gert er ráð fyrir að íhlutirnir verði framleiddir í nákvæmu magni, rétt eins og framleiddur íhlutur sem hefur uppskriftarlínu af gerðinni framleiðsla.
-   Tiltekið útreikningsmagn í sérstökum uppskriftarútreikningi vegna pöntunar - Hægt er að gera sérstakan uppskriftarútreikning vegna pöntunar fyrir vörulínu í sölupöntun, sölutilboði eða þjónustupöntun. Sjálfgefið útreikningsmagn notar magnið í upphaflegu vörulínunni en hægt er að hnekkja sjálfgefna magninu. Hægt er að velja hvort sérstaki uppskriftarútreikningurinn vegna pöntunar notar niðurbrotsaðferðina samkvæmt pöntun eða margra stiga niðurbrot.

Reiknuð upphæð afskrifaðs fasts kostnaðar vöru fellur undir ýmis gjöld.






