---
title: "Stjórnun afurðategundar"
description: "Þetta efnisatriði lýsir því hvernig vörustjórar geta notað flokka smásöluafurða til að stjórna tengslum milli stigveldis smásöluafurðar og upplýsinga um losaðar afurðir."
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2246024d7d70947690173f3d0768292abe43efd7
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="manage-retail-product-categories-and-products"></a>Stjórna flokkum smásöluafurða og afurða

[!INCLUDE [banner](./includes/banner.md)]

Þetta efnisatriði lýsir betri leið til að stjórna flokkum smásöluafurða og afurða í Microsoft Dynamics 365 for Retail. Viðbæturnar gera vörustjórum kleift að skoða byggingu á eiginleikum afurðar sem er deilt milli stigveldis smásöluafurðar og upplýsinga um losaðar afurðir.

Til að læra meira um stjórnun á flokkum smásöluafurða í vinnusvæðinu **Flokka- og afurðastjórnun** skal velja reitinn **Stigveldi smásöluafurðar**.

Takið eftir aukinni uppbyggingu á síðunni **Stigveldi smásöluafurðar** sem birtist. Í fyrri útgáfum Retail var eiginleikum afurða skipt niður í *grunneiginleika afurðar* og *eiginleika smásöluafurðar* byggt á notkunareiginleikum þeirra. Eiginleikar smásöluafurðar eru *altækir* í notkunareiginleikum þeirra. Með öðrum orðum, fyrir tiltekinn eiginleika smásöluafurðar er sama gildi deilt með öllum lögaðilum. Hins vegar eru grunneiginleikar afurðar *sértækir fyrir hvern lögaðila*. Með öðrum orðum, fyrir tiltekinn grunneiginleika afurðar getur gildið verið mismunandi milli lögaðila, fer allt eftir einstökum viðskiptakröfum hvers lögaðila.

Með aukinni byggingu á flokkum smásöluafurðar eru eiginleikar afurða röklega greindir í sundur eftir notkunareiginleikum þeirra innan hóps til að endurspegla byggingu skjámyndar fyrir upplýsingar um losaðar afurðir.

![Svæði flokkuð á grundvelli notkunareiginleika](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Hægt er að skipta á milli þess að stjórna sértækum eiginleikum lögaðila yfir alla lögaðila og stjórna þeim fyrir tiltekinn lögaðila.

Til að stjórna eiginleikum yfir alla lögaðila skal velja **Skoða fyrir alla lögaðila** (eða **Breyta fyrir alla lögaðila**).

![Skoða/breyta fyrir alla lögaðila](media/ToggleBackToEditForSpecificLegalEntity.PNG)

Til að stjórna eiginleikum fyrir tiltekinn lögaðila skal velja **Skoða fyrir tiltekinn lögaðila** (eða **Breyta fyrir tiltekinn lögaðila**).

![Skoða/breyta fyrir tiltekinn lögaðila](media/ToggleToEditForAllLegalEntities.PNG)

Auk þess getur vörustjóri í betrumbættu byggingunni á flokkum smásöluafurðar nú einnig skilgreint sjálfgildi fyrir viðbótarsett af eiginleikum afurðar á stigi einstakra flokka. Þegar afurðir eru síðan búnar til öðlast þær sjálfgefið gildi fyrir afurðaeiginleika þeirra sem byggist á tengslum þessara eiginleika við einstakan flokk í stigveldi smásöluafurðar. Þessir erfðu eiginleikar afurðar er einnig hægt að breyta fyrir hverja afurð til að uppfylla einstakar viðskiptakröfur.

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a>Val á eiginleikum til að uppfæra afurðir á síðunni Stigveldi smásöluafurðar

Hægt er að nota nýju betrumbættu bygginguna fyrir eiginleika afurðar til að velja hvaða uppfærðu eiginleikar afurðar á að flytja til tengdra afurða. Á síðunni **Stigveldi smásöluafurðar**, skal velja á aðgerðasvæðinu **Flokkur** og síðan velja **Uppfæra afurðir** til að opna svargluggann **Uppfæra afurðir**.

![Uppfæra svarglugga afurða](media/NewUpdateProductsEnhancedView.PNG)


