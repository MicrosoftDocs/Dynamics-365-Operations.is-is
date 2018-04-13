--- 
title: "Loka fjárhagsári"
description: "Þetta ferli fara í gegnum árslokaferli sem flytja stöður yfir á nýtt fjárhagsár."
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4f2f1f1206f3cb3534ef93923d4945bb63814514
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="close-the-fiscal-year"></a>Loka fjárhagsári

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli fara í gegnum árslokaferli sem flytja stöður yfir á nýtt fjárhagsár.


## <a name="validate-year-end-close-parameters"></a>Villuleita færibreytur árslokalokunar
1. Fara í Fjárhagur > Fjárhagsuppsetning > Færibreytur fyrir fjárhag.
2. Víkka út hlutann lokun fjárhagsárs.
3. Veldu Já eða nei fyrir valkostinn Eyða lokunarfærslum árs í millifærslu
    * Ef fjárhagsári hefur verið lokað og lokun ársloka er keyrt aftur, er þessa stillingu mikilvæg. Ef stillt á Já, verður fylgiskjali fyrir lok fyrra árs eytt, og nýtt fylgiskjali verða stofnaðar fyrir allar upphafsstöður lykla. Ef stillt á Nei, helst fyrri fylgiskjal og nýju fylgiskjali aðeins verður stofnuð til að leiðrétta færslur sem voru bókaðar eftir síðustu lokun ársloka.  
4. Veldu já eða nei um hvort eigi að Stofna lokunarfærslur í millifærslu
    * Ef setja á Já tvær færslur eru stofnaðar. Eitt fylgiskjal er stofnað í fjárhagsárinu sem verið er að loka til að færa stöður í P&L fjárhagslykla niður í núll og önnur fylgiskjal eru stofnuð á næsta fjárhagsári fyrir upphafsstöður. Ef stillt á Nei, eitt fylgiskjal er stofnuð á næsta fjárhagsári fyrir upphafsstöður.  
5. Veldu Já eða nei um hvort eigi að Stilla stöðu fjárhagsárs á lokað fyrir fullt og allt
    * Ef stillt á Já verður staða fjárhagsárs stillt á Endanlega lokað.  Þar sem ekki er hægt að enduropna varanlega lokað ár, væri bestu venju að þessi valkostur er stilltur á nei.  
6. Veldu Já eða nei um hvort Rita þarf fylgiskjalsnúmer á meðan á lokun árs stendur.
    * Ef stillt á Já, verður að færa inn númer fylgiskjals handvirkt í árslokaferlinu. Númeraröð er ekki notuð til að mynda þetta fylgiskjalsnúmer. Bestu starfsvenjur er að setja þetta á Já.  
7. Lokið síðunni.
8. Fara í Fjárhag > Loka tímabili > Árslok.
9. Smellið á Nýtt til að stofna sniðmát árslokalokunar.
    * Hægt er ða stofna sniðmát fyrir hóp lögaðila sem á að keyra árslokalokun fyrir. Hægt er að endurnota þetta sniðmát ár eftir ár.  
10. Færið inn heiti sniðmáts árslokalokunar í reitinn heiti flokks.
11. Velja fjárhagsár sem sniðmátið verður stofnuð fyrir.
    * Aðeins er hægt að flokka lögaðila sem nota sama fjárhagsárið saman í sniðmáti árslokalokunar . Þetta er vegna þess að árslokalokun er gerð með því að velja fjárhagsár, en ekki dagsetningu.  
12. Nota má flýtileiðina til að vista færslu.
13. Smella á bæta Við til að velja lögaðila fyrir sniðmátið.
    * Hægt er að bæta lögaðilar við með því að velja annað hvort lögaðila eða með því að velja stigveldi fyrirtækis.  Aðeins verður bætt við lögaðilum sem eru með stigveldi fyrirtækis með sama fjárhagsdagatal valið.  
14. Velja annaðhvort lögaðila eða stigveldisskipan.
15. Smellið á „Í lagi“.
16. Velja hvort fjárhagsvíddir verpa fluttar á næsta fjárhagsár.
    * Bestu starfsvenjur er að setja þetta valkost á Já fyrir efnahagslykla.  Þetta viðheldur fjárhagsvíddum á bókaðar færslur þegar stofnaðir eru upphafsstöður fyrir efnahagslykla.  Fyrir rekstrarlykla, er hægt að velja að vinna með fjárhagsvíddir (Loka öllum) þegar stöður eru fluttar yfir á óráðstafað eigið fé eða þú getur valið að hafa fjárhagsvíddir skipt út fyrir annað víddargildi (Loka einum). Ef þú velur Loka einum, geturðu skilgreint tiltekið víddargildi fyrir hverja vídd eða jafnvel valið að skilja eftir autt.  
17. Smellið á „Vista“.
18. Hefja árslokalokun með því að velja keyra fjárhagslokun á Aðgerðarúðunni.
    * Árslokalokun verður keyrt fyrir valið sniðmát.  
19. Veldu allt eða hlutmengi lögaðila úr sniðmátinu úr hverju á að keyra árslokalokunina.
    * Þegar fyrst er keyrt árslokalokun, þá gætu flest fyrirtæki valið að keyra árslokalokun fyrir alla lögaðila innan þess sniðmáts til að fá upphafsstöður. Ef leiðréttingarfærslur eru gerðar eftir það, geturðu valið að keyra árslokalokun fyrir aðeins þeirra lögaðila sem hafa leiðréttingar.  
20. Smellið á „Í lagi“.
21. Velja fjárhagsár sem árslokalokun verður keyrð fyrir.
22. Í reitinn fylgiskjal skal slá inn gildi.
    * Bestu starfsvenjur er að hafa fjárhagsár í fylgiskjalsnúmerinu, til að auðvelda að finna fylgiskjal árslokalokunar sem er stofnaður.  
23. Árslokalokunin er sjálfgefið keyrt í runu.
    * Það eru bestu starfsvenjur fyrir langtímaferli til að keyra í runuhætti. Þetta er yfirleitt eitt af þessum ferlum, og er það ástæðan fyrir því að sjálfgefið er að nota runuhátt.  
24. Smellið á „Í lagi“.


