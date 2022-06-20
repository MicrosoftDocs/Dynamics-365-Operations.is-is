---
title: Aukin RCS-síun í RCS/altækri geymslu
description: Þessi grein lýsir aukinni síunargetu fyrir RCS Global geymsluna, sem hefur verið endurbætt til að innihalda viðbótarsíur.
author: JaneA07
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: a343b9f1af68a727cb2a8d1e390f85e10aab2d39
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901213"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>Auknir síuvalkostir RCS til að finna skilgreiningar í RCS/altækri geymslu

[!include [banner](../includes/banner.md)]

Þessi grein lýsir aukinni síunargetu fyrir Regulatory Configuration Services (RCS) alþjóðlega geymslu, sem hefur verið endurbætt til að fela í sér getu til að sía með eftirfarandi forsendum: 
- **Land/svæði** - Byggt á ISO-landsnúmerum  
- Gerðir **Merkis** fyrir:
  - Virkt svæði
  - Eiginleikasvæði
  - Iðnaður 
  - Viðskiptaskjal 

Til að gera það auðveldara að uppgötva sérstakar eða tengdar grunnstillingar er hægt að nota síur, annaðhvort einar og sér eða í hóp. Til að finna staka gerð af stillanlegum viðskiptaskjölum sem tengjast lánardrottnareikningum er til dæmis hægt að nota síuna **Gerð viðskiptaskjals** til að leita að slíku skjali. 

[![Síuhluti fyrir altæka geymslu.](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Þú getur fínstillt leitina enn frekar með því að velja gerð skjals, t.d. „lánardrottnareikningur“ og smella á **Nota síu**. Eftirfarandi dæmi sýnir niðurstöðurnar þegar síað er fyrir **Gerð viðskiptaskjals** með gerð skjals bætt við. 

[![Notuð sía og innflutningur fyrir gerð viðskiptaskjals.](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Hægt er að flytja síaðar niðurstöður inn í RCS geymslu notenda eða Dynamics 365 Finance umhverfi, annað hvort fyrir sig eða sem sett. Til að gera þetta skaltu velja hóp stillinga og smella á **Flytja inn**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]