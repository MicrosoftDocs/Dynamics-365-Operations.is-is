---
title: Stofna áætlun fyrir svæði
description: Þessi verklýsing sýnir hvernig á að raða framleiðslupöntunum sem eru ekki enn hafnar fyrir svæði.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 070d8441700cd0051d421ea7e2210bcb668e8c22
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820371"
---
# <a name="create-a-schedule-for-a-site"></a>Stofna áætlun fyrir svæði

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]