--- 
title: Keyra kanban-vinnsluverk
description: "Þetta ferli leggur áherslu á framkvæmd kanban-ferlisvinnslu."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 50b5048a5f9277c47444fa69d2c8cc8e36ba7dcd
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="execute-kanban-process-jobs"></a>Keyra kanban-vinnsluverk

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli leggur áherslu á framkvæmd kanban-ferlisvinnslu. Fyrsta vinnslan er lokið með áætlað magn og hefur engar villur. Annari vinnslu er lokið með villum. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta ferli er ætluð fyrir á starfsmaður á vél.


## <a name="select-a-kanban-job"></a>Veljið kanban-vinnslu.
1. Fara í Framleiðslustýring > Kanban > Kanban-spjald fyrir ferlisvinnslur.
2. Í reitnum vinnuflokkur skal smella á fellilistahnappinn til að opna leitina.
3. Smellt er á línuna með 1250 tilfangaflokki. Þetta síar vinnslu til að birta aðeins vinnslur fyrir vinnuflokk 1250.
    * Merkja línuna sem hefur stöðuna Áætluð vinnslu.  

## <a name="complete-a-job-with-expected-quantity"></a>Ljúka vinnslu með áætlað magn
1. Stækka eða fella saman hlutann Upplýsingar.
    * Þessi hluti sýnir mikilvægar upplýsingar um kortanúmer, vörunúmer, pantað magn, og aðgerðaheiti.  
2. Útvíkka eða draga saman hlutann leiðbeiningar fyrir framleiðslu.
    * Þessi hluti sýnir leiðbeiningar fyrir framleiðslu fyrir aðgerðina. Leiðbeiningarnar má vera texta, myndir, teikningar og önnur skjöl.  
3. Smellið á „Byrja“.
    * Velja vinnsla sem ekki er kláruð. Nota stöðutákn í svæðinu staða vinnslu til að skoða stöðu vinnslunnar.      
4. Smelltu á Ljúka.
    * Vinnslu er lokið með áætlaða gæði.  

## <a name="complete-a-job-with-errors"></a>Ljúka vinnslu með villum
1. Smellið á „Byrja“.
    * Þegar vinnslu er lokið er næstu vinnslu á listanum sjálfkrafa valið. Þess vegna þarf ekki vinnsla vera valin áður en smellt er á Ræsa.  
2. Í aðgerðasvæðinu er smellt á framleiðsla
3. Smella á Lokið (upplýsingar)
4. Í listanum skal merkja valda línu.
5. Í reitnum gallað magn, skal slá inn númer.
6. Í reitnum gallalaust magn skal slá inn númer.
7. Smellið á „Í lagi“.


