---
title: Keyra kanban-vinnsluverk
description: Þetta ferli leggur áherslu á framkvæmd kanban-ferlisvinnslu.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b6b74ea84ec403790c257ecfe8147a116cd97e9ff5a21b2cd7f649202771d07d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711760"
---
# <a name="execute-kanban-process-jobs"></a>Keyra kanban-vinnsluverk

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]