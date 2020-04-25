---
title: Stigveldi fyrirtækis í Common Data Service
description: Þetta efni lýsir samþættingu fyrirtækjaupplýsinga milli forrita Finance and Operations og Common Data Service.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: fc5db8d04a2860df0c917816e2910c6fbda941ff
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173155"
---
# <a name="organization-hierarchy-in-common-data-service"></a>Stigveldi fyrirtækis í Common Data Service

[!include [banner](../../includes/banner.md)]



Vegna þess að Dynamics 365 Finance er fjármálakerfi er *fyrirtæki* kjarnahugtak og kerfisuppsetning byrjar með stillingu fyrirtækisstigveldis. Síðan er hægt að rekja fjárhag fyrirtækja á fyrirtækjastigi og einnig á hvaða stigi sem er í fyrirtækjastigveldinu.

Þó að Common Data Service sé ekki með hugtak fyrirtækjastigveldis er það með nokkur laus hugtök, svo sem heildarsölutekjur. Sem hluti af samþættingu Common Data Service er gagnaskipulag stigveldis fyrirtækis er bætt við Common Data Service.

## <a name="data-flow"></a>Gagnaflæði

Vistkerfi fyrirtækja sem samanstendur af forritum Finance and Operations og Common Data Service mun halda áfram að hafa stigveldi fyrirtækis. Þetta stigveldi fyrirtækis er byggt á forritum Finance and Operations, en það er útsett í Common Data Service í upplýsinga- og stækkunarlegum tilgangi. Eftirfarandi mynd sýnir upplýsingar um stigveldi fyrirtækis sem birtast í Common Data Service sem einstefnugagnaflæði úr forritum Finance and Operations til Common Data Service.

![Skipulagsmynd](media/dual-write-data-flow.png)

## <a name="templates"></a>Sniðmát

Einingakort yfir stigveldi fyrirtækis eru tiltæk fyrir samstillingu á einstefnu gagna úr forritum Finance and Operations til Common Data Service.

## <a name="templates"></a>Sniðmát

Afurðarupplýsingar innihalda allar upplýsingar sem tengjast vörunni og skilgreiningu hennar, svo sem afurðarvíddir eða mælingar og geymsluvíddir. Eins og meðfylgjandi tafla sýnir, er safn af einingakortum búið til til að samstilla vörur og tengdar upplýsingar.

Finance and Operations-smáforrit | Önnur Dynamics 365 forrit | lýsing
-----------------------|--------------------------------|---
Tilgangur fyrir stigveldi fyrirtækis | msdyn_internalorganizationhierarchypurposes | Þetta sniðmát veitir samstillingu í eina átt á einingunni tilgangi fyrirtækjaskipulags.
Gerð fyrirtækisstigveldis | msdyn_internalorganizationhierarchytypes | Þetta sniðmát veitir samstillingu í eina átt á einingunni Gerð fyrirtækjaskipulags.
Stigveldi fyrirtækis - útgefið | msdyn_internalorganizationhierarchies | Þetta sniðmát veitir samstillingu í eina átt á einingunni Útgefið fyrirtækjaskipulag.
Rekstrareining | msdyn_internalorganizations | 
Lögaðilar | msdyn_internalorganizations | 
Lögaðilar | cdm_companies | Veitir tvíátta samstillingu upplýsinga um lögaðila (fyrirtæki).


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>Innra fyrirtæki

Upplýsingar um innra skipulag í Common Data Service koma úr tveimur einingum, **rekstrareiningu** og **lögaðilum**.

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]

