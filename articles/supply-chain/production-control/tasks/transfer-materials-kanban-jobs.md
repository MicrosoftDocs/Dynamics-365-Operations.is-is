---
title: Flytja efni innan kanban-vinnsla
description: Þetta ferli leggur áherslu á keyrslu kanban-afturköllunarvinnslu til að flytja efni.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e8808b168d2b3845b315e6bbcfb376e37f31fe4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981032"
---
# <a name="transfer-materials-with-kanban-jobs"></a>Flytja efni innan kanban-vinnsla

[!include [banner](../../includes/banner.md)]

Þetta ferli leggur áherslu á keyrslu kanban-afturköllunarvinnslu til að flytja efni. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta ferli er ætluð fyrir starfsmaður í vöruhúsi.


## <a name="display-transfer-jobs"></a>Birta flutningsvinnslur
1. Fara í Framleiðslustýring > Kanban > Kanban-spjald fyrir flutningsvinnslur.
2. Útvíkka eða draga saman hlutann Síur.
    * Í hlutanum Síur hægt er að tilgreina hvaða vinnslur sem óskað er að finna með því að sía á framleiðsluflæði, verkþáttarheitið, Úr vöruhús og staðsetning, og Til vöruhúss og staðsetningar.  
3. Færðu inn "11" í svæðið Úr vöruhúsi.
4. Í svæðinu Til staðsetningar, færið inn '12'.

## <a name="start-a-transfer-job"></a>Hefja flutningsvinnslu
1. Á listanum afvelja valinni línu - ef einhver.
2. Í listanum skal velja línu 4.
    * Veljið fyrsta vinnslan með stöðuna Ekki áætlaðar. Gangið úr skugga um að þetta er eina valda verkið.  
3. Smellið á „Byrja“.
    * Athugið að tákn tilgreinir vinnslan er nú hafin.  

## <a name="select-a-second-transfer-job-and-change-quantity"></a>Veljið seinni flutningsvinnslu og magni
1. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Hægt er að hafa margar vinnslur valdar en núna skal bara velja línu 5.  
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Gangið úr skugga um að vinnslu í fyrra skrefi er sú eina sem er valin. Afvelja öllum öðrum vinnslum.  
3. Takið niður gildið í reitnum verkmagn til síðari tilvísunar
4. Stilla verkmagn á '30'.
    * Athugið viðvörunarboðin! Ekki er leyfilegt að flytja 30. Samkvæmt uppsetningu kanban-reglan er aðeins hægt að flytja upphaflegt magn.  
5. Notið gildið sem tekið var niður í reitnum verkmagn
    * Stilla magn Vinnslu í fyrra gildið.  

## <a name="start-the-second-transfer-job"></a>Hefja seinni flutningsvinnslu
1. Smellið á „Byrja“.
    * Þetta hefur flutning vinnslu í línu 5.  

## <a name="complete-both-transfer-jobs"></a>Ljúka bæði flutningsvinnslur
1. Í listanum skal velja línu 4.
    * Nú tvær flutningsvinnslur valdar á röð 4 og 5 línu.  
2. Smelltu á Ljúka.
    * Þetta lýkur við flutning á bæði vinnslur.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]