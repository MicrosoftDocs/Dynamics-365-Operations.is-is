---
title: Stofna lögaðila
description: Þessi grein lýsir því hvernig á að stofna lögaðila í Microsoft Dynamics 365 Commerce, sem þarf að búa til og stilla áður en rásir eru búnar til.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: e99536d3706c842d69060136f23508208b16b461
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276320"
---
# <a name="create-legal-entities"></a>Stofna lögaðila

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að stofna lögaðila í Microsoft Dynamics 365 Commerce, sem þarf að búa til og stilla áður en rásir eru búnar til.

Lögaðili er fyrirtæki sem hefur skráð ögfest lagalega uppbyggingu. Lögaðila er hægt að færa inn í samninga og eru þeir krafnir um að útbúa yfirlit sem segir til um frammistöðu þeirra.

Fyrirtæki er lögaðila. Eins og stendur eru fyrirtæki aðeins ein tegund af lögaðila sem þú getur búið til, og sérhver lögaðili tengist auðkenni fyrirtækisins. Þessi tenging er til staðar þar sem sum virk svæði í forritinu nota fyrirtækjakenni eða *DataAreaId* í gagnalíkönum sínum. Í þessum virku svæðum eru fyrirtæki notuð sem mörk fyrir öryggi gagna. Notendur geta nálgast gögn aðeins fyrir fyrirtæki sem eru skráðir inn í. 

Þegar þú stofnar rás verður þú að tilgreina hvaða lögaðila þessi rás tilheyrir.

## <a name="create-a-new-legal-entity"></a>Stofna nýjan lögaðila

Til að stofna nýjan lögaðila í Dynamics 365 Commerce  skal fylgja þessum skrefum.

1. Í yfirlitsglugganum ferðu í **Einingar \> Uppsetning höfuðstöðva \> Lögaðilar**.
1. Í aðgerðaglugganum velurðu **Nýtt**. Glugginn **Nýr lögaðili** birtist til hægri.
1. Í reitinn **Heiti** skal slá inn gildi.
1. Í reitinn **Fyrirtæki** skal slá inn gildi.
1. Í reitinn **Land/svæði** skal slá inn eða velja gildi.
1. Veldu **Í lagi**. 

   ![Stofnun lögaðila.](media/legal-entities.png)

1. Í kaflanum **Almennt** gefurðu upp eftirfarandi almennar upplýsingar um lögaðilann: 
   1. Færa skal inn leitarheiti, ef krafist er leitarheitis. Leitarheiti er annað nafn sem hægt er að nota til að leita að þessum lögaðila. 
   1. Veljið hvort þessi lögaðili er notaður sem samstæðufyrirtæki.
   1. Veljið hvort þessi lögaðili er notaður sem losunarfyrirtæki. 
   1. Veldu **sjálfgefið tungumál** fyrir eininguna. 
   1. Veljið **tímabelti** fyrir eininguna.
1. Í hlutanum **Aðsetur** velurðu **Breyta** til að færa inn upplýsingar um aðsetur, til dæmis götunafn og götunúmer, póstnúmer og borg.
1. Í hlutanum **Tengslaupplýsingar** skal færa inn upplýsingar um aðferðir samskipta, svo sem tölvupósta, vefslóðir og símanúmer.
1. Í hlutanum **Lögboðin skýrslugerð** skal færa inn skráningarnúmerin sem eru notuð fyrir lögboðna skýrslugerð.
1. Í hlutanum **Skráningarnúmer** skaltu slá inn allar upplýsingar sem lögaðilinn krefst.
1. Í hlutanum **Bankareikningsupplýsingar** skal slá inn bankareikninga og leiðarnúmer fyrir lögaðilann.
1. Í hlutanum **Erlend viðskipti og vörustjórnun** skaltu færa sendingarupplýsingar inn fyrir lögaðilann.
1. Í hlutanum **Númeraröð** er hægt að skoða númeraraðirnar sem tengjast lögaðilanum. Til að byrja með verður þetta tómt.
1. Í hlutanum **Yfirlitsmynd** skaltu skoða eða breyta merki og yfirlitsmynd sem tengjast lögaðilanum.
1. Í hlutanum **Skattskráning** skal færa inn skráningarnúmerin sem eru notuð til að senda skýrslu til skattyfirvalda.
1. Í hlutanum **Skattur 1099** skal færa inn 1099 upplýsingar fyrir lögaðilann.
1. Í **Skattaupplýsingar** kafla, sláðu inn skattaupplýsingar fyrir lögaðilann.
1. Veljið **Vista**.

Eftirfarandi mynd sýnir upplýsingar um dæmi um lögaðila.

![Almennur hluti lögaðila.](media/legal-entities-general.png)
   
## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir fyrirtæki og fyrirtækjastigveldi](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Skipuleggja fyrirtækjastigveldi](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Stigveldi fyrirtækis](channels-org-hierarchies.md)

[Yfirlit yfir rásir](channels-overview.md)

[Skilyrði fyrir rásauppsetningu](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
