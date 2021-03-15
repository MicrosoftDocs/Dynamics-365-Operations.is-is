---
title: Flytja eign
description: Þessi verkefnaleiðbeiningar fyrir verk flytja fjárhagsupplýsingar fyrir eignabók úr einni fjárhagsvíddasamstæða í nýja fjárhagsvíddasamstæða.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0770011a76b1e4cc8b4d13e54fab2d0fba43f8a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975917"
---
# <a name="transfer-a-fixed-asset"></a>Flytja eign

[!include [banner](../../includes/banner.md)]

Þessi verkefnaleiðbeiningar fyrir verk flytja fjárhagsupplýsingar fyrir eignabók úr einni fjárhagsvíddasamstæða í nýja fjárhagsvíddasamstæða.  Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.

1. Í skoðunarrúðnni ferðu í **Kerfseiningar > Fastafjármunir > Fastafjármunir > Fastafjármunir**.
2. Finna og velja eign sem á að flytja, á listanum.
3. Á aðgerðasvæðinu skal smellt á **Fastafjármuni**.
4. Smellt er á **Flytja eignir**.
5. Dagsetning er rituð í reitinn **Dagsetning millifærslu**.
6. Færa inn athugasemdir til að lýsa flutninginn.
    
    Þessi listi sýnir allar bækur fyrir eignina.  
7. Merkja bækur sem á að flytja í nýtt fjárhagsvíddasamstæða.
    * Listinn sýnir núverandi gildi fjárhagsvídda fyrir valda bók.  
    * Velja fjárhagsvídd til að uppfæra fyrir valda eignabók.  
8. Í reitnum **fjárhagsvídd** skal smella á fellilistahnappinn til að opna leitina.
    * Stilla aðra fjárhagsvíddargildi sem viðeigandi.  
    * Öllum fjárhagsvíddargildum breyta þegar flutningur fer fram, hvort sem hefur verið fært inn gildi eða skilið eftir autt. Til dæmis, ef fært er inn gildi fyrir BusinessUnit (fyrirtækjaeining) og hafðir CostCenter (kostnaðarstað) fjárhagslegar víddir autt. Ef reikningsskipulagið leyfði auð gildi fyrir CostCenter og Deild, myndi flutningurinn leiða til þess að hvert virðislíkan hefur nýtt gildi fyrir BusinessUnit (fyrirtækjaeining) og tómt gildi fyrir CostCenter og deild.  
9. Smelltu á **Uppfæra**.
    * Það verður tækifæri til að forskoða breytingar áður en ljúka flutningi.  
    * Skoða niðurstöður áður en eignabækur fluttar.  
10. Smelltu á **Flutningur**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]