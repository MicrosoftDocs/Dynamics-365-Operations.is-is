---
title: "Nýlega bætt breyta aðgerðir í verkskráningu"
description: "Ef að verkskráning er notuð til að stofna leiðbeiningar fyrir verk er hægt að breyta skal skrár fleiri hagkvæman hátt með því að nota aðgerðir sem lýst er í þessa wiki."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core
ms.custom: 266464
ms.assetid: b4640e67-4b92-4855-8041-1bfc71aadc47
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: c4f9ac515eab6ed8b194fc8985f6d3fae40ced38
ms.lasthandoff: 03/31/2017


---

# <a name="recently-added-editing-features-in-task-recorder"></a>Nýlega bætt breyta aðgerðir í verkskráningu

Ef að verkskráning er notuð til að stofna leiðbeiningar fyrir verk er hægt að breyta skal skrár fleiri hagkvæman hátt með því að nota aðgerðir sem lýst er í þessa wiki.

Þessar aðgerðir eru tiltækar í á **Stillingar &gt;verkskráning &gt;Breyta skráningu** valmynd.

-   Setja inn skref án þess að skrá allt skrána aftur.
-   Flytja skref undir að undirverki án þess að skrá allt skrána aftur.
-   Fella svæði Skráningu heiti og lýsingu.

## <a name="insert-steps-without-rerecording-the-entire-file"></a>Setja inn skref án rerecording allt skrá
Þú getur nú bætt skref alls staðar í leiðarvísi fyrir verk án þess að spila aftur eða skrá allt skrána aftur.

1.  Veljið skref eftir á í nýja skref til að setja inn. Gangið úr skugga um að skrefið er auðkenndur.

Í röð fyrir verkskráningu til að setja inn skref þarf rétta opna síðuna. Rétt síðan er nýja skref gerist síðuna. Verkskráning er ferli sem ákvarðar hvað virka síðu er og verður að gera virkni ef rétt síðu er ekki opin. 

[![tg1](./media/tg1.png)](./media/tg1.png) 


Þegar varan er á rétta síðu **setja Inn skref** verður tiltækur.

[![tg2](./media/tg2-231x300.png)](./media/tg2.png)

2. Smellið á **setja Inn skref**.

Þegar smellt er á **setja Inn skref**, skiptir verkskráning til að skrá ham. Hvaða aðgerð í Notendaviðmóti núna verða að vera skráð og bætt við í stað skrefa.

3. Smellið á **Stöðva**.

Endurtaka má ferli er bætt við eins mörgum skref eða flutt til eins margar undiríhluti verk eftir þörfum (sjá fyrir neðan fyrir undiríhluti verkefni).

4. Þegar það er gert breytingar á leiðarvísi fyrir verk, smellið á **breytingum Lokið**, og veljið síðan einn af kostum til að vista eða birta leiðarvísi fyrir verk.

## <a name="move-steps-under-a-subtask-without-rerecording-the-entire-file"></a>Flytja skref undir undirverk fyrir runuhaus án rerecording allt skrá
Hægt er að færa skref undir að undirverki án þess að spila aftur eða skrá allt skrána aftur. Hægt einnig að flytja skref undirverki eða lok skrefinu undirverki ef óskað er að flokka í fyrirliggjandi loka skref.

1.  Veljið skref eða undirverki skref sem á að flytja. Gangið úr skugga um að skrefið er auðkenndur.
2.  Smellið á sporöskjulaga, og smella síðan á **skref Fara eftir**.

[![tg3](./media/tg3.png)](./media/tg3.png)

3. Veljið skref eða undirverki skref sem á að færa skrefið eða undirverki skrefið eftir. Verkskráning verður að færa skrefið.

4. Til að færa lok skrefinu undirverki skal velja hana, smella á í sporöskjulaga, **skref Fara eftir**, og veljið síðan skref eftir sem óskað er eftir lok skrefinu undirverki að.

Ef óskað er eftir að fyrsta skrefið í leiðarvísi fyrir verk innan undirverki til að stofna þrep undirverki sem önnur skrefið og færa fyrsta skrefið í það. Hægt er að bæta við eða færa eins mörg þrep eða undiríhluti verk eftir þörfum.

5. Þegar það er gert breytingar á leiðarvísi fyrir verk, smellið á **breytingum Lokið**, og veljið síðan einn af kostum til að vista eða birta leiðarvísi fyrir verk.

## <a name="collapse-recording-name-and-description"></a>Fella Skráningu heiti og lýsingu
Hægt er að útvíkka og draga saman við **heiti Skráningar** og **Skráningu lýsing** svæði. Þegar þessi svæði eru dregin saman verður fleiri skref sýnilegir í rúðunni breytingum verkskráning. 

[![tg4](./media/tg4-300x252.png)](./media/tg4.png)  

<a name="see-also"></a>Sjá einnig
--------

[Stofna fylgiskjölum eða þjálfun með verkskráningu](/dynamics365/operations/dev-itpro/user-interface/task-recorder)

[Verk flýtitilvísun verkskráningar](/dynamics365/operations/dev-itpro/user-interface/task-recorder-quick-reference)


