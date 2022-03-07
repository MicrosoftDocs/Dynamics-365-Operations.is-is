---
title: Stofna áætlun fyrir svæði
description: Þessi verklýsing sýnir hvernig á að raða framleiðslupöntunum sem eru ekki enn hafnar fyrir svæði.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 146531217f7f596a5cb98e271b0356ffeb3d5547
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567248"
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