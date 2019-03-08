---
title: Flytja eign
description: Þessi verkefnaleiðbeiningar fyrir verk flytja fjárhagsupplýsingar fyrir eignabók úr einni fjárhagsvíddasamstæða í nýja fjárhagsvíddasamstæða.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb8a5b94d9a0bb510daa2a698524e0c380597991
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "357198"
---
# <a name="transfer-a-fixed-asset"></a>Flytja eign

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verkefnaleiðbeiningar fyrir verk flytja fjárhagsupplýsingar fyrir eignabók úr einni fjárhagsvíddasamstæða í nýja fjárhagsvíddasamstæða.  Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.

1. Fara í Eignir > Eignir > Eignir.
2. Finna og velja eign sem á að flytja, á listanum.
3. Á Aðgerðasvæðinu skal smellt á eign.
4. Smellt er á Flytja eignir.
5. Dagsetning er rituð í reitinn Dagsetning millifærslu.
6. Færa inn athugasemdir til að lýsa flutninginn.
    * Þessi listi sýnir allar bækur fyrir eignina.  
7. Merkja bækur sem á að flytja í nýtt fjárhagsvíddasamstæða.
    * Listinn sýnir núverandi gildi fjárhagsvídda fyrir valda bók.  
    * Velja fjárhagsvídd til að uppfæra fyrir valda eignabók.  
8. Í reitnum fjárhagsvídd skal smella á fellilistahnappinn til að opna leitina.
    * Stilla aðra fjárhagsvíddargildi sem viðeigandi.  
    * Öllum fjárhagsvíddargildum breyta þegar flutningur fer fram, hvort sem hefur verið fært inn gildi eða skilið eftir autt. Til dæmis, ef fært er inn gildi fyrir BusinessUnit (fyrirtækjaeining) og hafðir CostCenter (kostnaðarstað) fjárhagslegar víddir autt. Ef reikningsskipulagið leyfði auð gildi fyrir CostCenter og Deild, myndi flutningurinn leiða til þess að hvert virðislíkan hefur nýtt gildi fyrir BusinessUnit (fyrirtækjaeining) og tómt gildi fyrir CostCenter og deild.  
9. Smelltu á Uppfæra.
    * Það verður tækifæri til að forskoða breytingar áður en ljúka flutningi.  
    * Skoða niðurstöður áður en eignabækur fluttar.  
10. Smelltu á Flutningur.

