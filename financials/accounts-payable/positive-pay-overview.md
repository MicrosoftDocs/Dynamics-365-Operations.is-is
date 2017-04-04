---
title: "Yfirlit yfir jákvæða greiðslu"
description: "Þessi grein veitir upplýsingar um jákvæðar greiðslur, sem eru notaðar til að mynda rafræna lista yfir ávísanir sem eru innleystar í banka."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 1fd606817b06a05b9abaaedf20ea9872bd7edd5d
ms.openlocfilehash: cb4806a1f023c1e60311ff9d8facb4ef5717ad94
ms.lasthandoff: 03/31/2017


---

# <a name="positive-pay-overview"></a>Yfirlit yfir jákvæða greiðslu

Þessi grein veitir upplýsingar um jákvæðar greiðslur, sem eru notaðar til að mynda rafræna lista yfir ávísanir sem eru innleystar í banka. 

Hægt er að nota jákvæða greiðslu til að búa til rafræna lista yfir ávísanir sem eru innleystar í banka. Jákvæðar greiðsluskrár geta auðveldð bönkum að koma í veg fyrir ávísanafals. Þú setur upp jákvæða greiðslu til að mynda rafræna skrá yfir ávísanir í hvert sinn sem ávísanir eru prentaðar. Þegar ávísun er innleyst í bankanum ber bankinn ávísunina saman við lista yfir ávísanir sem þú hefur sent áður. Ef ávísunin stemmir við ávísun í listanum samþykkir bankinn ávísunina. Ef ávísunin stemmir ekki við ávísun í listanum heldur bankinn henni eftir til skoðunar.

Jákvæð greo‘sæa er einnig þekkt sem SafePay. 

Jákvæðu greiðsluskránni geta innihaldið viðkvæmar upplýsingar um greiðsluþegar og upphæðir ávísunar. Þess vegna skaltu vera viss um að nota viðeigandi öryggisráðstafanir frá þeim tíma sem skrárnar eru myndaðar og þar til þær eru mótteknar í bankanum. Jákvæðum greiðsluskrám er hlaðið niður í samræmi við leiðbeiningar um niðurhal í vefvafra. 

Jákvæð greiðsluskrár eru stofnaðar með því að nota gagnaeiningar. Áður en jákvæð greiðsluskrá er mynduð, verður að setja upp umbreytingasnið fyrir XML sem þýðir gögnin yfir á snið sem bankinn getur notað. 

Fyrir hvern bankareikning sem á að mynda jákvæðar greiðsluupplýsingar til, verður að úthluta jákvæða greiðslusniðinu. Eftir að greiðslur eru myndaðar er hægt að mynda jákvæða greiðsluskrá fyrir einn lögaðila og einn bankareikning. Hins vegar er hægt að mynda jákvæðar greiðsluskrár fyrir marga lögaðila og bankareikninga á sama tíma. 

Eftir að búið er að greiða ávísanir sem eru talin upp í jákvæðu greiðsluskránni berst staðfestingarnúmer frá bankanum. Hægt er að staðfesta síðan skal jákvæðu greiðsluskrána í Microsoft Dynamics 365 aðgerða. 

Ef nauðsynlegt er að breyta jákvæðri greiðsluskrá er hægt að afturkalla hana. Í þeim tilfellum er svæðið sem gefur til kynna hvort viðkomandi ávísun hefur verið tekin með í jákvæðri greiðsluskrá endurstillt fyrir hverja ávísun í jákvæðu greiðsluskránni.

Nánari upplýsingar, sjá [Sett upp og mynda jákvæðu greiðsluskránni](set-up-generate-positive-pay-files.md).


