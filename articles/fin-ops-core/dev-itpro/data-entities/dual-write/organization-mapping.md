---
title: Stigveldi fyrirtækis í Dataverse
description: Þessi grein lýsir samþættingu fyrirtækjaupplýsinga milli forrita fjármála- og reksturs og Dataverse.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289047"
---
# <a name="organization-hierarchy-in-dataverse"></a>Stigveldi fyrirtækis í Dataverse

[!include [banner](../../includes/banner.md)]



Vegna þess að Dynamics 365 Finance er fjármálakerfi er *fyrirtæki* kjarnahugtak og kerfisuppsetning byrjar með stillingu fyrirtækisstigveldis. Síðan er hægt að rekja fjárhag fyrirtækja á fyrirtækjastigi og einnig á hvaða stigi sem er í fyrirtækjastigveldinu.

Þó að Dataverse sé ekki með hugtak fyrirtækjastigveldis er það með nokkur laus hugtök, svo sem heildarsölutekjur. Sem hluti af samþættingu Dataverse er gagnaskipulag stigveldis fyrirtækis er bætt við Dataverse.

## <a name="data-flow"></a>Gagnaflæði

Vistkerfi fyrirtækja sem samanstendur af forritum fjármála- og reksturs og Dataverse mun halda áfram að hafa stigveldi fyrirtækis. Þetta stigveldi fyrirtækis er byggt á forritum fjármála- og reksturs, en það er útsett í Dataverse í upplýsinga- og stækkunarlegum tilgangi. Eftirfarandi mynd sýnir upplýsingar um stigveldi fyrirtækis sem birtast í Dataverse sem einstefnugagnaflæði úr forritum fjármála- og reksturs til Dataverse.

![Skipulagsmynd.](media/dual-write-data-flow.png)

Töflukort fyrirtækjastigveldis eru tiltæk fyrir einstefnusamstillingu gagna frá forritum fjármála- og reksturs til Dataverse.

## <a name="templates"></a>Sniðmát

Fyrirtæki er hópur af fólki sem eru að vinna saman að því að framkvæma viðskiptaferli eða ná markmiði. Stigveldi fyrirtækis standa fyrir vensl á milli fyrirtækja sem þú ert með saman í rekstri. Hægt er að skilgreina eftirfarandi gerðir samstæðufyrirtæki: lögaðila, rekstrareiningar, og hópa. Eins og eftirfarandi tafla sýnir er búið að stofna safn af töflukortum til að samstilla lögaðila, rekstrareiningar og upplýsingar tengdar upplýsingar stigveldi stofnunar/fyrirtækis.

Forrit fyrir fjármál- og rekstur | Forrit viðskiptavinatengsla     | Lýsing
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

