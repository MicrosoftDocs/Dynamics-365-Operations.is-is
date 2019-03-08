---
title: Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (15. nóvember 2018)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0e9de5e36e67941ab09c773a63b0e7045105a07e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "304775"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-15-2018"></a>Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (15. nóvember 2018)

[!include [banner](includes/banner.md)]

**Smíði 8.1.2045**

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Core HR.

## <a name="other-changesfixes"></a>Aðrar breytingar/lagfæringar

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a>Ekki er hægt að breyta núverandi stöðu starfsmanns í opna stöðu í framtíðinni

Breyting hefur verið gerð til að virkja flutninga á stöðu þegar staðan er aðeins í boði í framtíðinni. 

### <a name="position-does-not-display-when-creating-a-new-employee"></a>Staða birtist ekki þegar nýr starfsmaður er búinn til

Breytingar hafa verið gerðar til að birta allar opnar stöður sem eru tiltækar til úthlutunar þegar nýir starfsmenn eru ráðnir í Talent. Þetta felur í sér eldri stöður eða ef stöðurnar hafa verið í dagsettar fram í tímann. Stöður birtast nú rétt á grundvelli upphafsdags ráðningar. 

### <a name="termination-date-is-displaying-based-on-user-settings"></a>Dagur starfsloka er birtur á grundvelli notandastillinga

Breyting hefur verið gerð á lista fyrri starfsmanna til að taka tillit til tímamismunar út af æskilegu tímabelti starfsmanna þegar starfslokadagar eru skoðaðir.

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a>Tenglar fyrir vinnuliði sem mér eru úthlutaðir birta ekki réttar upplýsingar

Með þessari breytingu mun fletting í upplýsingar einstakra vinnuliða í listanum birta réttar upplýsingar fyrir valinn lið. Þetta vandamál átti sér aðeins stað með ítarlegum öryggisvalkostum.


## <a name="known-issue"></a>Þekkt vandamál

- **Vandamál**: Þegar nýtt viðhengi er bætt við starfsmann eru hnapparnir **Nýtt** og **Breyta** skyggðir. 
- **Hjáleið:** Áður en þú opnar viðhengissíðu skaltu ganga úr skugga um að FactBoxes á síðunni **Starfsmenn** séu lokaðir. Ef upplýsingareitirnir eru lokaðir þegar síðan **Starfskraftar** er hlaðið inn verða viðhengishnapparnir gerðir virkir. (Þetta vandamál verður lagað í næstu verkvangsuppfærslu.)
