---
title: Stigveldi fyrirtækis í Dataverse
description: Þessi grein lýsir samþættingu skipulagsgagna milli fjármála- og rekstrarappa og Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 48533dd104f62080d0ebd47389a4a829c772db13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289047"
---
# <a name="organization-hierarchy-in-dataverse"></a>Stigveldi fyrirtækis í Dataverse

[!include [banner](../../includes/banner.md)]



Vegna þess að Dynamics 365 Finance er fjármálakerfi, *skipulag* er kjarnahugtak og kerfisuppsetning byrjar með uppsetningu á stigveldi fyrirtækis. Síðan er hægt að rekja fjárhag fyrirtækja á fyrirtækjastigi og einnig á hvaða stigi sem er í fyrirtækjastigveldinu.

Þó að Dataverse sé ekki með hugtak fyrirtækjastigveldis er það með nokkur laus hugtök, svo sem heildarsölutekjur. Sem hluti af samþættingu Dataverse er gagnaskipulag stigveldis fyrirtækis er bætt við Dataverse.

## <a name="data-flow"></a>Gagnaflæði

Vistkerfi fyrirtækja sem samanstendur af fjármála- og rekstraröppum og Dataverse verður áfram með stigveldi skipulagsheilda. Þetta stigveldi stofnunarinnar er byggt á fjármála- og rekstrarforritum, en það er afhjúpað í Dataverse í upplýsinga- og stækkunarskyni. Eftirfarandi mynd sýnir stigveldisupplýsingar fyrirtækisins sem eru afhjúpaðar í Dataverse sem einhliða gagnaflæði frá fjármála- og rekstraröppum til Dataverse.

![Skipulagsmynd.](media/dual-write-data-flow.png)

Skipulagsstigveldistöflukort eru fáanleg fyrir einhliða samstillingu gagna úr fjármála- og rekstraröppum til Dataverse.

## <a name="templates"></a>Sniðmát

Fyrirtæki er hópur af fólki sem eru að vinna saman að því að framkvæma viðskiptaferli eða ná markmiði. Stigveldi fyrirtækis standa fyrir vensl á milli fyrirtækja sem þú ert með saman í rekstri. Hægt er að skilgreina eftirfarandi gerðir samstæðufyrirtæki: lögaðila, rekstrareiningar, og hópa. Eins og eftirfarandi tafla sýnir er safn af töflukortum búið til til að samstilla lögaðila, rekstrareiningu, s og tengdar skipulagsstigveldisupplýsingar.

Forrit fyrir Finance and Operations | Forrit viðskiptavinatengsla     | Lýsing
-----------------------|--------------------------------|---
[Lögaðilar](mapping-reference.md#102) | cdm_companies | 
[Lögaðilar](mapping-reference.md#142) | msdyn_internalorganizations |
[Rekstrareining](mapping-reference.md#143) | msdyn_internalorganizations |
[Stigveldi fyrirtækis - birt](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | Þetta sniðmát veitir samstillingu í eina átt í töflunni Stigveldi fyrirtækis - birt.
[Tilgangur fyrir stigveldi fyrirtækis](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | Þetta sniðmát veitir samstillingu í eina átt á töflunni Tilgangur fyrir stigveldi fyrirtækis.
[Gerð fyrirtækisstigveldis](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | Þetta sniðmát veitir samstillingu í eina átt í töflunni Gerð fyrirtækisstigveldis.

## <a name="internal-organization"></a>Innra fyrirtæki

Upplýsingar um samstæðufyrirtæki í Dataverse koma úr tveimur töflum: **Rekstrareiningu** og **Lögaðilum**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

