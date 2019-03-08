---
title: Stofna áætlun fyrir svæði
description: Þessi verklýsing sýnir hvernig á að raða framleiðslupöntunum sem eru ekki enn hafnar fyrir svæði.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54bb2532534d5567239dad4fab7fd74fa50d2826
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "330058"
---
# <a name="create-a-schedule-for-a-site"></a>Stofna áætlun fyrir svæði

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að raða framleiðslupöntunum sem eru ekki enn hafnar fyrir svæði.  Nota Sýnigögn fyrirtækisins fyrir að ljúka þetta ferli er USMF.


## <a name="identify-production-orders-that-are-not-started"></a>Auðkenndu framleiðslupantanir sem eru ekki hafnar.
1. Fara í Framleiðslustýringar > Framleiðslupantanir > Allar framleiðslupantanir.
2. Nota flýtiafmörkun til að finna færslur Til dæmis, sía á reitnum svæði með gildinu '1'.
    * 1 táknar svæði í USMF. Ef ekki er verið að nota USMF skal velja svæði úr þínu eigin fyrirtækið.  
3. Opnið dálkasía Stöðu.
4. Notið síu á reitnum „Staða“ með gildinu „áætlað“ og notið til þess síuvirknitáknið „er nákvæmlega“.

## <a name="create-a-schedule"></a>Stofna áætlun.
1. Merkið eða afmerkið allar línur í listanum.
2. Í Aðgerðarrúðunni er smellt á Áætlun.
3. Smellt er á Raða vinnslum.
4. Í reitnum Stefna tímasetningar er valið „Afturábak frá afhendingardagsetningu“.
5. Veljið Nei í svæðinu Takmarkaða afkastaveita.
6. Veljið Nei í svæðinu Takmarkað efni.
7. Smellið á „Í lagi“.
    * Þetta gæti tekið nokkra stund.  

## <a name="view-the-result-of-scheduled-production-orders"></a>Skoða niðurstaða raðaðra framleiðslupantana.
1. Í listanum skal merkja valda línu.
    * Hægt er að merkja hvaða línu sem er.  
2. Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.
3. Smellt er á Allar vinnslur.
    * Á þessari síðu er hægt að sjá lista yfir verk. Á flipanum Röðun er hægt að sjá upphafsdagsetningu og lokadagsetningu fyrir verk.  
4. Smellt er á Efnum.
    * Á þessari síðu er hægt að sjá metin efnisnotkun fyrir aðgerðir á gildandi tiltækum birgðum og framleiðslupöntun.  

