---
title: Frumstilla grunngögn í nýju Commerce-umhverfi
description: Þessi grein lýsir gögnum sem búin eru til við frumstillingu fyrir Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a12bd7a178d8d40db8c919410a00fbf021625f50
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238751"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a>Frumstilla grunngögn í nýju Commerce-umhverfi

[!include [banner](includes/banner.md)]

Þessi grein lýsir gögnum sem búin eru til við frumstillingu fyrir Dynamics 365 Commerce.

Þegar Commerce-lausn hefur verið virkjuð í Microsoft Dynamics Lifecycle Services (LCS), verður að frumstilla Commerce-skilgreiningu til að stofna grunnskilgreiningargögn.

> [!IMPORTANT]
> Áður en grunnstilling Commerce er frumstillt þarf að ganga úr skugga um að tungumál og póstfang fyrir hvern lögaðila hafi verið tilgreint þar sem settar verða upp verslanir fyrir verslun. Ljúka verður við þessi skref fyrir hvern lögaðila sem er notaður fyrir Commerce.

Fylgið eftirfarandi skrefum til að frumstilla skilgreiningar.

1. Ræsið Commerce-biðlarann.
2. Smelltu á **Retail og Commerce** &gt; **Uppsetning höfuðstöðva** &gt; **Færibreytur** &gt; **Commerce-færibreytur**.
3. Smellið á **Frumstilla**.

Frumstilling stofnar eftirfarandi sjálfgefin skilgreiningargögn:

- Vinnslur og undirvinnslur Commerce Verkraðara
- Skema fyrir viðskiptarás
- Dreifingaráætlanir Commerce
- Sjálfgefið útlit afgreiðsluskjás, sem inniheldur hnappahnit, myndir og þemu
- Upplýsingar um tímabelti
- Aðgerðir í sölustað (POS)
- Heimildir sölustaðar
- Skýrslur rásar
- Lýsigögn eiginda
- Sniðmát fyrir villuleit eininga
- Runuvinnsla til að hreinsa setuferil Commerce Data Exchange

Þar að auki er skráning sem er tengd við greiðslu korts atvinnugrein (PCI) er virk fyrir Commerce-gagnagrunninn.

> [!NOTE]
> Það er möguleiki á því að skilgreina verkröð Commerce sérstaklega. Þessi valkostur gerir kleift að endurstilla skilgreiningu Commerce verkraðara á sjálfgefnar stillingar.

Þegar frumstillingu er lokið verður að skilgreina viðbótarupplýsingar Commerce-gagna. Hér eru nokkur dæmi:

- Viðskiptafæribreytur
- Færibreytur viðskiptaverkraðara
- Commerce-rásir
- Afgreiðslukassar og tæki
- Úrval


[!INCLUDE[footer-include](../includes/footer-banner.md)]