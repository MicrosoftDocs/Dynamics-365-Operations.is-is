---
title: Takmarka aðgang að starfsmönnum eftir lögaðila
description: Þessi grein útskýrir hvernig á að setja upp starfsmannaaðgang eftir lögaðila.
author: twheeloc
ms.date: 11/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fadd2c34d31bbd259255596c06a8e7517f7a774b
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780300"
---
# <a name="restrict-access-to-workers-by-legal-entity"></a>Takmarka aðgang að starfsmönnum eftir lögaðila

Þessi grein útskýrir hvernig á að setja upp starfsmannaaðgang eftir lögaðila.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Starfsmenn eru ráðnir í lögaðila. Hér eru nokkur dæmi:

- Aaron Con er starfandi í USSI lögaðilanum.
- Ahmed Barnett er starfandi í USMF lögaðilanum.
- Alicia Thornber er starfandi í GLSI og USMF lögaðilum.

Það fer eftir hlutverki notanda í fyrirtækinu, þeir gætu þurft aðgang til að skoða alla starfsmenn í öllum lögaðilum. Að öðrum kosti gæti þurft að takmarka notanda, þannig að þeir geti aðeins skoðað starfsmenn í lögaðilanum sem þeir hafa aðgang að. Til að stjórna hvaða starfsmenn notandi getur skoðað skaltu velja **Takmarka aðgang að upplýsingum starfsmanna** breytu á **Mannauður sameiginlegar breytur** síðu.

Til dæmis hefur notandi aðgang að **Vinnumaður** síðu og hefur aðeins aðgang að USMF lögaðilanum. Í þessu tilviki getur notandinn skoðað eftirfarandi upplýsingar fyrir starfsmenn á listanum á undan:

- Ef eiginleiki til að takmarka aðgang að upplýsingum starfsmanna er ekki virkur getur notandinn skoðað upplýsingar um Aaron, Ahmed og Alicia.
- Ef aðgerðin er virkjuð getur notandinn aðeins skoðað upplýsingar fyrir Alicia og Ahmed, vegna þess að þau eru einnig starfandi í USMF lögaðilanum.

Upplýsingarnar sem eru sýndar eru mismunandi eftir því hvaða forriti þú ert að nota.

## <a name="dynamics-365-human-resources-stand-alone"></a>Dynamics 365 Human Resources sjálfstætt

Ef aðgerðin til að takmarka aðgang að starfsmannaupplýsingum er virkjuð, mun takmarkaði notandinn sjá autt gildi í sumum listum sem innihalda nafn starfsmannsins.

Til dæmis mun notandi sem hefur aðeins aðgang að USMF lögaðilanum upplifa eftirfarandi hegðun:

- Í **Virkar stöður** lista, the **Vinnumaður** dálkurinn verður auður fyrir stöðu Arons vegna þess að notandinn hefur ekki aðgang að starfsmönnum USSI lögaðilans.
- Ef notandinn kafar niður á nafn starfsmannsins, autt **Vinnumaður** síða mun birtast.

## <a name="dynamics-365-human-resources-on-finance-infrastructure"></a>Dynamics 365 Human Resources um innviði fjármála

Ef aðgerðin til að takmarka aðgang að starfsmannaupplýsingum er virkur, mun takmarkaði notandinn sjá nafn starfsmannsins á sumum listum.

Til dæmis mun notandi sem hefur aðeins aðgang að USMF lögaðilanum upplifa eftirfarandi hegðun:

- Í **Virkar stöður** lista, the **Vinnumaður** dálkurinn mun sýna nafn Arons. Ef notandinn sveimar yfir nafni starfsmannsins mun aðeins nafnið og titillinn birtast.
- Ef notandinn kafar niður á nafn starfsmannsins, autt **Vinnumaður** síða mun birtast.

> [!TIP]
> Ef þú ert að nota Dynamics 365 Human Resources á Finance innviðum og vilt að takmarkaðir notendur sjái auð gildi fyrir starfsmannanöfn, geturðu bætt við **Takmarka aðgang starfsmanna** öryggisréttindi til notendahlutverkanna á **Öryggisstillingar** síðu.

Eftir að þú hefur virkjað eiginleikann verður þú að ljúka nokkrum aukaskrefum til að stilla heimildir fyrir hvern notanda sem þarf að takmarka útsýni.

1. Á síðunni **Notendur** skal velja notanda.
2. Veljið hlutverk fyrir notandann. Boðið verður upp á valkostinn **Úthluta fyrirtækjum**.
3. Veljið **Úthluta fyrirtækjum**.
4. Á nýju síðunni skaltu velja **Veita ákveðnum fyrirtækjum aðgang hverju fyrir sig** og veldu síðan fyrirtækin sem notandinn á að hafa aðgang að.
5. Endurtakið skref 2 til 4 fyrir öll hin hlutverkin sem notandinn hefur, þar með talið hlutverk notanda í kerfinu.

> [!NOTE]
> Lögaðilarnir sem notandi hefur aðgang að verða að passa yfir öll hlutverk notandans.
