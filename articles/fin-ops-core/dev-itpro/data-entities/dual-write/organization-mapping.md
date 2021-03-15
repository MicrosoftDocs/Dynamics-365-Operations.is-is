---
title: Stigveldi fyrirtækis í Dataverse
description: Þetta efni lýsir samþættingu fyrirtækjaupplýsinga milli forrita Finance and Operations og Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 5132fd85fdf2c08ccded9db590328c394a2f984e
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744694"
---
# <a name="organization-hierarchy-in-dataverse"></a>Stigveldi fyrirtækis í Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Vegna þess að Dynamics 365 Finance er fjármálakerfi er *fyrirtæki* kjarnahugtak og kerfisuppsetning byrjar með stillingu fyrirtækisstigveldis. Síðan er hægt að rekja fjárhag fyrirtækja á fyrirtækjastigi og einnig á hvaða stigi sem er í fyrirtækjastigveldinu.

Þó að Dataverse sé ekki með hugtak fyrirtækjastigveldis er það með nokkur laus hugtök, svo sem heildarsölutekjur. Sem hluti af samþættingu Dataverse er gagnaskipulag stigveldis fyrirtækis er bætt við Dataverse.

## <a name="data-flow"></a>Gagnaflæði

Vistkerfi fyrirtækja sem samanstendur af forritum Finance and Operations og Dataverse mun halda áfram að hafa stigveldi fyrirtækis. Þetta stigveldi fyrirtækis er byggt á forritum Finance and Operations, en það er útsett í Dataverse í upplýsinga- og stækkunarlegum tilgangi. Eftirfarandi mynd sýnir upplýsingar um stigveldi fyrirtækis sem birtast í Dataverse sem einstefnugagnaflæði úr forritum Finance and Operations til Dataverse.

![Skipulagsmynd](media/dual-write-data-flow.png)

Töflukort fyrirtækjastigveldis eru tiltæk fyrir einstefnusamstillingu gagna frá Finance and Operations -forritum til Dataverse.

## <a name="templates"></a>Sniðmát

Afurðarupplýsingar innihalda allar upplýsingar sem tengjast vörunni og skilgreiningu hennar, svo sem afurðarvíddir eða mælingar og geymsluvíddir. Eins og eftirfarandi tafla sýnir er búið að stofna safn af töflukortum til að samstilla afurðir og tengdar upplýsingar.

Finance and Operations-smáforrit | Önnur Dynamics 365 forrit | lýsing
-----------------------|--------------------------------|---
Tilgangur fyrir stigveldi fyrirtækis | msdyn_internalorganizationhierarchypurposes | Þetta sniðmát veitir samstillingu í eina átt á töflunni Tilgangur fyrir stigveldi fyrirtækis.
Gerð fyrirtækisstigveldis | msdyn_internalorganizationhierarchytypes | Þetta sniðmát veitir samstillingu í eina átt í töflunni Gerð fyrirtækisstigveldis.
Stigveldi fyrirtækis - birt | msdyn_internalorganizationhierarchies | Þetta sniðmát veitir samstillingu í eina átt í töflunni Stigveldi fyrirtækis - birt.
Rekstrareining | msdyn_internalorganizations |
Lögaðilar | msdyn_internalorganizations |
Lögaðilar | cdm_companies | Veitir tvíátta samstillingu upplýsinga um lögaðila (fyrirtæki).

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>Innra fyrirtæki

Upplýsingar um samstæðufyrirtæki í Dataverse koma úr tveimur töflum, **rekstrareiningu** og **lögaðilum**.

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]