---
title: "Frumstilla grunngögn í nýju Retail-umhverfi"
description: "Þessi grein lýsir gögnum sem búin eru til við frumstillingu fyrir Microsoft Dynamics 365 for Operations - Retail."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 137c675781cf75d9ce621a84c89224019c161362
ms.lasthandoff: 03/31/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Frumstilla grunngögn í nýju Retail-umhverfi

[!include[banner](includes/banner.md)]


Þessi grein lýsir gögnum sem búin eru til við frumstillingu fyrir Microsoft Dynamics 365 for Operations - Retail.

Þegar smásölulausn hefur verið virkjuð í Microsoft Dynamics Lifecycle Services (LCS), verður að frumstilla smásöluskilgreiningu til að stofna grunnskilgreiningargögn. **Mikilvægt:** Áður en grunnstilling smásölu er frumstillt þarf að ganga úr skugga um að tungumál og póstfang fyrir hvern lögaðila hafi verið tilgreint þar sem setja verður upp verslanir fyrir smásöluverslun. Ljúka verður við þessi skref fyrir hvern lögaðila sem er notaður fyrir smásölu. Fylgið eftirfarandi skrefum til að frumstilla skilgreiningar smásölu.

1.  Ræsa Dynamics 365 for Operations-biðlara.
2.  Smellt er á **Smásala og viðskipti** &gt; **Uppsetning höfuðstöðva** &gt; **Færibreytur** &gt; **Smásölufæribreytur**.
3.  Smellið á **Frumstilla**.

Frumstilling stofnar eftirfarandi sjálfgefin skilgreiningargögn:

-   Vinnslur og undirvinnslur Retail Verkraðara
-   Skema smásölurásar
-   Dreifingaráætlanir smásölu
-   Sjálfgefið útlit afgreiðsluskjás, sem inniheldur hnappahnit, myndir og þemu
-   Upplýsingar um tímabelti
-   Aðgerðir í sölustað (POS)
-   Heimildir sölustaðar
-   Skýrslur rásar
-   Lýsigögn eiginda
-   Sniðmát fyrir villuleit eininga
-   Runuvinnsla til að hreinsa setuferil Commerce Data Exchange

Þar að auki er skráning sem er tengd við greiðslukortageirann (PCI) virk fyrir Dynamics 365 for Operations-gagnagrunninn. **Ábending:** Það er valkostur til að skilgreina Retail verkraðara sérstaklega. Þessi valkostur gerir kleift að endurstilla skilgreiningu Retail verkraðara á sjálfgefnar stillingar. Þegar frumstillingu er lokið verður að skilgreina viðbótarupplýsingar smásölugagna. Hér eru nokkur dæmi:

-   Smásölufæribreytur
-   Færibreytur Retail Verkraðara
-   Smásölurásir
-   Afgreiðslukassar og tæki
-   Úrval





