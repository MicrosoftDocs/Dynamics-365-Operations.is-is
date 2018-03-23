---
title: "Stjórnun afurðategundar"
description: "Í þessu efnisatriði er því lýst hvernig vörustjórar geta notað tegundir Retail afurða til að stjórna tengslum milli stigveldis Retail afurðar og upplýsinga um losaðar afurðir."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: is-is
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a>Betri stjórnun afurða og tegunda

[!include[banner](./includes/banner.md)]

Þetta efnisatriði lýsir betri leið til að stjórna tegundum Retail afurða og afurða í Dynamics 365 for Retail. Þessar viðbætur gera vörustjórum kleift að skoða algenga byggingu á eiginleikum afurðar milli stigveldis Retail afurðar og upplýsinga um losaðar afurðir.

Til að læra meira um stjórnun á tegundum Retail afurða skal fara í **Stigveldi Retail afurðar** frá vinnusvæðinu **Flokka- og afurðastjórnun** og athuga aukna byggingu á síðunni **Tegund Retail afurðar**.

![Vinnusvæði fyrir stjórnun tegunda og afurða](media/LaunchRetailProductHierarchy.png)

Í fyrri útgáfum var eiginleikum afurða skipt í **Grunneiginleika afurðar** og **Eiginleika Retail afurðar** byggt á hæfi þeirra. **Eiginleikar Retail afurðar** voru *altækir* út frá notkunareiginleikum þeirra sem þýðir að fyrir tiltekinn **Eiginleika Retail afurðar** er sama gildinu deilt þvert yfir alla lögaðila. **Grunneiginleikar afurðar** eru *sértæk lögaðila*. M.ö.o., fyrir tiltekinn **Grunneiginleika afurðar** getur gildið verið mismunandi þvert yfir lögaðila, byggt á einstökum viðskiptakröfum.

Með aukinni byggingu á tegundum Retail afurðar eru eiginleikar afurða röklega greindir í sundur eftir notkunareiginleikum þeirra innan hóps til að endurspegla byggingu skjámyndar fyrir upplýsingar um losaðar afurðir.

![Flokkun svæða byggt á gildissviði þeirra](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Hægt er að skipta á milli stjórnunar á eiginleikum tiltekinna lögaðila sem eiga við alla lögaðila og stjórnunar eiginleika sem eru sértækir fyrir tiltekinn lögaðila. Til að gera þetta skal velja annað hvort **Skoða/breyta fyrir alla lögaðila** eða **Skoða/breyta fyrir tiltekinn lögaðila**.

![Víxlaðu á milli yfirlits á einstaklingi og öllum lögaðilum](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Víxlaðu á milli yfirlits á einstaklingi og öllum lögaðilum](media/ToggleToEditForAllLegalEntities.PNG)  

Í samanburði við fyrri útgáfur getur vörustjóri í nýju byggingunni á tegundum Retail afurðar einnig skilgreint sjálfgildi fyrir viðbótarsett af eiginleikum afurðar á stigi einstakra tegunda. Við stofnun afurðar erfir afurð þessi sjálfgefnu eiginleikagildi afurða, byggt á tengslum þeirra við einstaka tegund í stigveldi Retail afurðar. Þessar erfðu eiginleikar afurðar er einnig hægt að breyta fyrir hverja afurð til að mæta einstökum viðskiptakröfum.

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a>Veldu eiginleika til að uppfæra afurðir af skjámyndinni tegund smásöluafurðar 
 
Hægt er að nota þessa nýju betrumbættu byggingu fyrir eiginleika afurðar til að velja hvaða uppfærðu eiginleikar afurðar á að flytja til tengdra afurða. 

![Nýtt betrumbætt yfirlit á uppfærðum afurðum](media/NewUpdateProductsEnhancedView.PNG) 

Stjórnendur smásölu geta breytt þessum arfgengu eiginleikum afurða fyrir hverja afurð til að mæta tilteknum viðskiptakröfum.


