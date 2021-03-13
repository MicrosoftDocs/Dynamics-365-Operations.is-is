---
title: Undirbúa lýsigögn umsóknar til notkunar í RCS
description: Í þessu efnisatriði er lýst hvernig eigi að stofna nýja skýrsluskilgreiningu sem inniheldur lýsigögn forrits.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5f55d089a88642cb2bda70274472ad0f0e45cd7
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094241"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a>Undirbúa lýsigögn umsóknar til notkunar í RCS
[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslulausnar getur búið til nýjar skilgreiningar rafrænnar skýrslugerðar (ER) sem innihalda lýsigögn forritsins til að setja upp ER-líkanavörpunarskilgreiningar í Regulatory Configuration Service (RCS). Þessi skilgreining verður notuð til að setja upp sýnisskilgreiningu ER-líkanavörpunar sem er búið til í þessu dæmi verður notað til að fá aðgang að utanríkisviðskiptum. Í þessu dæmi muntu stofna skilgreiningu fyrir sýnifyrirtækið, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er. Til að ljúka þessum skrefum verður fyrst að ljúka skrefunum í efninu [Stofna skilgreiningaveitur og merkja þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md).

## <a name="prerequisites"></a>Forkröfur
1.    Farðu í **Fyrirtækisstjórnun** > **Vinnusvæði** > **Rafræn skýrslugerð**. 
2.    Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt **Virk**. Ef þú sérð skilgreiningarveituna ekki skaltu klára skrefin í ferlinu [Stofna skilgreiningaveitur og merkja þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md). 
3.    Smelltu á **Skilgreiningu lýsigagna**. 
4.    Gerðu ráð fyrir að RCS verði notað til að setja upp ER-lausn fyrir forritið Finance and Operations, sem verður notuð til að búa til rafræn skjöl sem innihalda upplýsingar úr umdæmi utanríkisviðskipta. Til að tilgreina vörpun milli ER-gagnalíkans og uppruna nauðsynlegra gagna, verðuum við að hafa aðgang að forritslýsigögnum í RCS fyrir forritið Finance and Operations. Þess vegna er hluti af uppsetningu á ER-lausn að við skilgreinum nýja ER-lýsigagnaskilgreiningu sem innihalda öll lýsigögnin sem þarf eins og stendur til að mynda ER-skýrslur fyrir valið viðskiptalén. 

## <a name="add-metadata-configuration"></a>Bæta við skilgreiningu lýsigagna 
1.    Smellið á **Stofna skilgreiningu** til að opna felligluggann. 
2.    Í reitinn **Heiti** slærðu inn „Lýsigögn utanríkisverslunar“. 
3.    Smellið á **Stofna skilgreiningu**. 
4.    Smellið á **Hönnuður**. 
5.    Smelltu á **Bæta við**. 
  
> [!NOTE]
> Þú getur valið öll lýsigögn fyrir allt forritið eða fyrir valin líkön eða valdar einingar. Hafðu í huga að í þessu dæmi verður eftirfarandi lýsigögnum sjálfkrafa bætt við: töflum yfir skrár, talningum og lengd gagnategunda. Þegar fleiri tegundir lýsigagna er þörf verður að bæta þeim við á handvirkan hátt. 
 
Við erum með lýsigögn sem tengjast utanríkisviðskiptafærslum með því að velja atriði lýsigagna á handvirkan hátt. 
  
6.    Smelltu **Bæta við gagnagjafa**. 
7.    Smelltu á **Töflufærslur**. 
8.    Notaðu flýtiafmörkun til að sía í reitnum **Heiti** með gildinu „Intrastat“. 
9.    Veldu **Intrastat**-töflu. 
10.    Smellt er á **OK**.
  
Við bættum við lýsigögnum um Intrastat-skráatöfluna. 
  
11.    Í trénu víkkarðu út **Töflufærslur Intrastat**\>**Vensl**. 
12.    Í trénu velurðu **Töflufærslur Intrastat**\>**Vensl\IntrastatCommodity (Töflufærslur EcoResCategory)**.     
13.    Smelltu á **Bæta við lýsigögnum**. 
  
> [!NOTE]
> Bæta verður lýsigögnum um nauðsynleg vensl fyrir valda skráatöflu við á handvirkan hátt. 
  
16.    Smelltu **Bæta við gagnagjafa**. 
17.    Smelltu á **Upptalning**. 
18.    Notaðu flýtiafmörkun til að sía í reitnum **Heiti** með gildinu „IntrastatDirection“. 
19.    Veldu skrána **IntrastatDirection upptalning**. 
20.    Smellt er á **OK**. 
21.    Smellt er á **Vista**.  
22.    Lokið síðunni. 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a>Ljúktu drögunum að útgáfu skilgreiningar lýsigagna
1.    Smelltu á **Breyta stöðu**. 
2.    Smelltu á **Ljúka**. 
3.    Smellt er á **OK**. 
4.    Veldu fullgerða útgáfu **1**. 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a>Flyttu út fullgerða útgáfu lýsigagnauppsetningar úr forritinu sem XML-skrá
1.    Smelltu á **Skipta út**. 
2.    Smelltu á **Flytja út sem XML-skrá**. 
3.    Smellt er á **OK**. 
    
Uppsett ER lýsigagnaskilgreining er vistuð sem XML-skrá sem hægt er að flytja inn í RCS og notuð sem upplýsingaveita um lýsigögn fyrir viðskiptalén utanríkisviðskipta. Samkvæmt þessum upplýsingum getum við tilgreint vörpun á milli lýsigagna forritsins og ER-gagnalíkansins.
