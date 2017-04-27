---
title: "Nýlega viðbættar breytingaaðgerðir í verkskráningu"
description: "Ef verkskráning er notuð til að stofna leiðbeiningar fyrir verk er hægt að breyta skrám á skilvirkari hátt með því að nota aðgerðir sem lýst er í þessu wiki."
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

# <a name="recently-added-editing-features-in-task-recorder"></a>Nýlega viðbættar breytingaaðgerðir í verkskráningu

Ef verkskráning er notuð til að stofna leiðbeiningar fyrir verk er hægt að breyta skrám á skilvirkari hátt með því að nota aðgerðir sem lýst er í þessu wiki.

Þessir eiginleikar eru í boði í valmyndinni **Stillingar &gt;Verkskráning &gt;Breyta skráningu**.

-   Setja inn skref án þess að skrá alla skrána aftur.
-   Flytja skref undir undirverkefni án þess að skrá alla skrána aftur.
-   Fella saman reiti fyrir heiti og lýsingu skráningar.

## <a name="insert-steps-without-rerecording-the-entire-file"></a>Setja inn skref án þess að skrá alla skrána aftur
Þú getur nú bætt inn skrefum alls staðar í verkefnaleiðbeiningum án þess að spila aftur eða skrá alla skrána aftur.

1.  Veldu skrefið sem setja á nýtt skref inn á eftir. Gangið úr skugga um að skrefið sé auðkennt.

Til að verkskráning geti sett inn skref þarf að hafa rétta síðu opna. Rétta síðan er síðan þar sem nýja skrefið birtist. Verkskráning er gangverk sem ákvarðar hvað virka síðan er og mun afvirkja virknina ef rétt síða er ekki opin. 

[![tg1](./media/tg1.png)](./media/tg1.png) 


Þegar þú ert á réttri síðu verður **Setja inn skref** tiltækt.

[![tg2](./media/tg2-231x300.png)](./media/tg2.png)

2. Smellt er á **Setja inn**.

Þegar smellt er á **Setja inn skref** skiptir verkskráning yfir í skráningarham. Allar aðgerðir í Notendaviðmóti verða núna skráðar og bætt við sem skref.

3. Smellið á **Stöðva**.

Hægt er að endurtaka ferlið, bæta við eins mörgum skrefum eða flytja til eins mörg undirverk og þarf (sjá fyrir neðan fyrir undirverk).

4. Þegar búið er að gera breytingar á verkefnaleiðbeiningum skal smella á **Breytingum lokið** og velja síðan einn af kostunum til að vista eða birta verkefnaleiðbeiningarnar.

## <a name="move-steps-under-a-subtask-without-rerecording-the-entire-file"></a>Flytja skref undir undirverk án þess að skrá alla skrána aftur.
Hægt er að flytja skref undir undirverkefni án þess að endurspila eða skrá alla skrána aftur. Einnig er hægt að flytja skref undirverks eða lokaskref undirverks ef óskað er að flokka fyrirliggjandi skrefablokk.

1.  Veljið skrefið eða skref undirverks sem á að flytja. Gangið úr skugga um að skrefið sé auðkennt.
2.  Smellið á úrfellingarmerkið og smellið síðan á **Flytja skref á eftir**.

[![tg3](./media/tg3.png)](./media/tg3.png)

3. Veljið skrefið eða skref undirverks sem á að flytja skrefið eða undirverkið eftir. Verkskráning mun færa skrefið.

4. Til að færa lokaskref undirverks skal velja það, smella á úrfellingarmerkið, smella á **Flytja skref á eftir**, og velja síðan skrefið sem lokaskref undirverks á að vera á eftir.

Ef óskað er eftir að fyrsta skrefið í verkefnaleiðbeiningum sé innan undirverks þarf að stofna skref undirverks sem annað skref og færa fyrsta skrefið síðan í það. Hægt er að bæta við eins mörgum skrefum og undirverkum og þarf.

5. Þegar búið er að gera breytingar á verkefnaleiðbeiningum skal smella á **Breytingum lokið** og velja síðan einn af kostunum til að vista eða birta verkefnaleiðbeiningarnar.

## <a name="collapse-recording-name-and-description"></a>Fella saman heiti og lýsingu skráningar
Hægt er að útvíkka og draga saman reitina **Heiti skráningar** og **Lýsing skráningar**. Þegar þessi svæði eru dregin saman verða fleiri skref sýnileg í breytingarúðu Verkskráningar. 

[![tg4](./media/tg4-300x252.png)](./media/tg4.png)  

<a name="see-also"></a>Sjá einnig
--------

[Stofna fylgiskjölum eða þjálfun með verkskráningu](/dynamics365/operations/dev-itpro/user-interface/task-recorder)

[Flýtitilvísun verkskráningar](/dynamics365/operations/dev-itpro/user-interface/task-recorder-quick-reference)


