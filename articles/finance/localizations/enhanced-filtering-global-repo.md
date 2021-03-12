---
title: Aukin RCS-síun í RCS/altækri geymslu
description: Þetta efni lýsir aukinni síunargetu fyrir RCS Global geymsluna sem hefur verið bætt til að innihalda viðbótarsíurnar.
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: a67a4345271cbeffc100fc1d9077cc866846a4d4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005843"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>Auknir síuvalkostir RCS til að finna skilgreiningar í RCS/altækri geymslu

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir aukinni síunargetu fyrir altæka geymslu RCS (Regulatory Configuration Services) sem hefur verið bætt til að fela í sér hæfileika til að sía með eftirfarandi skilyrðum: 
- **Land/svæði** - Byggt á ISO-landsnúmerum  
- Gerðir **Merkis** fyrir:
  - Virkt svæði
  - Eiginleikasvæði
  - Iðnaður 
  - Viðskiptaskjal 

Til að gera það auðveldara að uppgötva sérstakar eða tengdar grunnstillingar er hægt að nota síur, annaðhvort einar og sér eða í hóp. Til að finna staka gerð af stillanlegum viðskiptaskjölum sem tengjast lánardrottnareikningum er til dæmis hægt að nota síuna **Gerð viðskiptaskjals** til að leita að slíku skjali. 

[![Sía hluti fyrir altæka geymslu](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Þú getur fínstillt leitina enn frekar með því að velja gerð skjals, t.d. „lánardrottnareikningur“ og smella á **Nota síu**. Eftirfarandi dæmi sýnir niðurstöðurnar þegar síað er fyrir **Gerð viðskiptaskjals** með gerð skjals bætt við. 

[![Notuð sía og innflutningur fyrir gerð viðskiptaskjala](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Síaðar niðurstöður er hægt að flytja inn í RCS-geymslu notenda eða í Dynamics 365 Finance-umhverfi, annaðhvort hverja fyrir sig eða saman. Til að gera þetta skaltu velja hóp stillinga og smella á **Flytja inn**.
