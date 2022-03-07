---
title: Stigveldi fyrirtækis í Dataverse
description: Þetta efni lýsir samþættingu stigveldisgagna milli forrita Finance and Operations og Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: afc1b5996667835c460f467526493380aa2d6403
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062087"
---
# <a name="organization-hierarchy-in-dataverse"></a>Stigveldi fyrirtækis í Dataverse

[!include [banner](../../includes/banner.md)]



Vegna þess að Dynamics 365 Finance er fjármálakerfi er *fyrirtæki* kjarnahugtak og kerfisuppsetning byrjar með stillingu fyrirtækisstigveldis. Síðan er hægt að rekja fjárhag fyrirtækja á fyrirtækjastigi og einnig á hvaða stigi sem er í fyrirtækjastigveldinu.

Þó að Dataverse sé ekki með hugtak fyrirtækjastigveldis er það með nokkur laus hugtök, svo sem heildarsölutekjur. Sem hluti af samþættingu Dataverse er gagnaskipulag stigveldis fyrirtækis er bætt við Dataverse.

## <a name="data-flow"></a>Gagnaflæði

Vistkerfi fyrirtækja sem samanstendur af forritum Finance and Operations og Dataverse mun halda áfram að hafa stigveldi fyrirtækis. Þetta stigveldi fyrirtækis er byggt á forritum Finance and Operations, en það er útsett í Dataverse í upplýsinga- og stækkunarlegum tilgangi. Eftirfarandi mynd sýnir upplýsingar um stigveldi fyrirtækis sem birtast í Dataverse sem einstefnugagnaflæði úr forritum Finance and Operations til Dataverse.

![Skipulagsmynd.](media/dual-write-data-flow.png)

Skipulagsstigveldistöflukort eru fáanleg fyrir einstefnusamstillingu gagna frá Finance and Operations forritum til Dataverse.

## <a name="templates"></a>Sniðmát

Afurðarupplýsingar innihalda allar upplýsingar sem tengjast vörunni og skilgreiningu hennar, svo sem afurðarvíddir eða mælingar og geymsluvíddir. Eins og eftirfarandi tafla sýnir er búið að stofna safn af töflukortum til að samstilla afurðir og tengdar upplýsingar.

Forrit fyrir Finance and Operations | Forrit viðskiptavinatengsla     | lýsing
-----------------------|--------------------------------|---
[Lögaðilar](mapping-reference.md#102) | cdm_companies | Veitir tvíátta samstillingu upplýsinga um lögaðila (fyrirtæki).
[Lögaðilar](mapping-reference.md#142) | msdyn_internalorganizations |
[Rekstrareining](mapping-reference.md#143) | msdyn_internalorganizations |
[Stigveldi fyrirtækis - birt](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | Þetta sniðmát veitir samstillingu í eina átt í töflunni Stigveldi fyrirtækis - birt.
[Tilgangur fyrir stigveldi fyrirtækis](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | Þetta sniðmát veitir samstillingu í eina átt á töflunni Tilgangur fyrir stigveldi fyrirtækis.
[Gerð fyrirtækisstigveldis](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | Þetta sniðmát veitir samstillingu í eina átt í töflunni Gerð fyrirtækisstigveldis.

## <a name="internal-organization"></a>Innra fyrirtæki

Upplýsingar um samstæðufyrirtæki í Dataverse koma úr tveimur töflum: **Rekstrareiningu** og **Lögaðilum**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
