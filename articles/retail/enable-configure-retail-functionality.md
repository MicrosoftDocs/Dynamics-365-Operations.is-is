---
title: "Frumstilla grunngögn í nýju Retail-umhverfi"
description: "Þessi grein lýsir gögnum sem búin eru til við frumstillingu fyrir Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7388324fe8a9abc8fc3d723b7c8df2c73d76a2ae
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Frumstilla grunngögn í nýju Retail-umhverfi

[!include[banner](includes/banner.md)]


Þessi grein lýsir gögnum sem búin eru til við frumstillingu fyrir Microsoft Dynamics 365 for Retail.

Þegar smásölulausn hefur verið virkjuð í Microsoft Dynamics Lifecycle Services (LCS), verður að frumstilla smásöluskilgreiningu til að stofna grunnskilgreiningargögn. **Mikilvægt:** Áður en grunnstilling smásölu er frumstillt þarf að ganga úr skugga um að tungumál og póstfang fyrir hvern lögaðila hafi verið tilgreint þar sem setja verður upp verslanir fyrir smásöluverslun. Ljúka verður við þessi skref fyrir hvern lögaðila sem er notaður fyrir smásölu. Fylgið eftirfarandi skrefum til að frumstilla skilgreiningar smásölu.

1.  Ræsa Dynamics 365 for Retail-biðlara.
2.  Smellt er á **Smásala** &gt; **Uppsetning höfuðstöðva** &gt; **Færibreytur** &gt; **Smásölufæribreytur**.
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

Þar að auki er skráning sem er tengd við greiðslukortageirann (PCI) virk fyrir Dynamics 365 for Retail-gagnagrunninn. **Ábending:** Það er valkostur til að skilgreina Retail verkraðara sérstaklega. Þessi valkostur gerir kleift að endurstilla skilgreiningu Retail verkraðara á sjálfgefnar stillingar. Þegar frumstillingu er lokið verður að skilgreina viðbótarupplýsingar smásölugagna. Hér eru nokkur dæmi:

-   Smásölufæribreytur
-   Færibreytur Retail Verkraðara
-   Smásölurásir
-   Afgreiðslukassar og tæki
-   Úrval





