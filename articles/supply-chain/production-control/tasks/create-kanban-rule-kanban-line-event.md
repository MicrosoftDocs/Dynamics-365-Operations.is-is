--- 
title: "Stofna kanban-reglu með kanban-línutilviki"
description: "Þetta ferli stofnar kanban-reglu með því að nota stillinguna línutilvik kanbans til að virkja sækja úr ferlisverkþætti."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9ef7b8e920d22cbc4f96676e68a263f2da7f232c
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a>Stofna kanban-reglu með kanban-línutilviki

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli stofnar kanban-reglu með því að nota stillinguna línutilvik kanbans til að virkja sækja úr ferlisverkþætti. Kanban-reglu virkjast af kanban ferlisverkþætti, með magnið það sama eða hærri en 25 hvert. Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF. Þetta verkefni er ætlað fyrir Ferlishönnuð eða Virðisstraumsstjóra, þar sem þau undirbúa framleiðslu nýja eða breytta afurðar í lean-umhverfi.


## <a name="create-a-kanban-rule"></a>Stofna kanban-reglu
1. Farið í upplýsingar um afurðarstjórnun > Lean-framleiðsla > Kanban-reglur.
2. Smellið á „Nýtt“.
3. Velja 'Tilvik' í reitnum Áfyllingaráætlun.
    * Þetta myndar kanban beint úr eftirspurn. Hann er notaður til að setja upp reglur sem skilgreina framleiða eftir pöntun-aðstæður.  
4. Færa inn eða velja gildi í reitnum Fyrsta áætlun verkþáttarins.
    * Sláið inn eða Veljið SpeakerAssemblyAndPolish. Fyrsti verkþáttur kanban-reglu framleiðslu er ferlisverkþáttur í framleiðsluflæðinu. Þegar þú velur aðgerð, eru gildisdagsetningar verkþáttar afrituð í gildisdagsetningar kanban-reglu.  
5. Útvíkka hlutann Upplýsingar.
6. Í reitinn afurð skal færa inn ‚L0001‘.
7. Útvíkka hlutann Tilvik.
8. Í reitnum línutilvik kanbans skal velja ‚Sjálfvirkt‘.
    * Þetta myndar tilvikskanban eftir þörfum.  Þessi reitur er notuð til að stilla kanban-reglur sem fylla efni á sem krafist er fyrir úrvinnsluaðgerð. Þegar Sjálfvirk er valið, eru tilvikskanbön stofnaðar með eftirspurn. Mælt er með þessari stillingu ef búist er við að keyra framleiðslu sama dag.  
9. Stilla lágmarksmagn tilviks á ‚25‘.
    * Tilvikskanban eru myndaðar þegar eftirspurnarmagn er jafnt eða meira en þetta svæði. Þetta er hentugt ef á að framleiða pöntunarmagn sem er minna en þetta svæði á einni vél og meira en þetta svæði á annarri vél.  
10. Smellið á „Vista“.

## <a name="create-sales-order-and-trigger-kanban-chain"></a>Stofna sölupöntun og virkja kanban keðju
1. Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir
2. Smellið á „Nýtt“.
3. Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.
    * Veljið viðskiptavinalykill US-003 Forest Wholesales.  
4. Smellið á „Í lagi“.
5. Sláið inn „L0001“ á svæðinu „Vörunúmer“.
    * L0001 er varan sem kanban-regla er stofnuð fyrir.  
6. Stillið magn á „27“.
    * Þar sem 27 er hærri en lágmarksmagnið 25 á kanban-reglu, mun þetta virkja tilvikskanban.  
7. Ritað er ‚1‘ í reitnum Svæði.
8. Sláðu inn eða veldu gildi í reitnum Vöruhús.
    * Velja vöruhús 13.  
9. Smellið á „Vista“.

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a>Skoða kanban sem var myndað af kanban-reglu
1. Farið í upplýsingar um afurðarstjórnun > Lean-framleiðsla > Kanban-reglur.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Útvíkkar kanban-hlutann.
    * Athugið að kanban fyrir 27 var stofnað til að vinna verkþátt á grunni stofnaðrar kanban-reglu.  
    * Þetta er síðasta skrefið  


