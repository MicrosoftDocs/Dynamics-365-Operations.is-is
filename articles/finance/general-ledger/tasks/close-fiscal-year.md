---
title: Loka fjárhagsári
description: Þetta ferli fara í gegnum árslokaferli sem flytja stöður yfir á nýtt fjárhagsár.
author: aprilolson
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8eb36cb856d191d64561060e7de4a1f9fd947882
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717475"
---
# <a name="close-the-fiscal-year"></a>Loka fjárhagsári

[!include [banner](../../includes/banner.md)]

Þetta ferli fara í gegnum árslokaferli sem flytja stöður yfir á nýtt fjárhagsár.


## <a name="validate-year-end-close-parameters"></a>Villuleita færibreytur árslokalokunar
1. Farðu í **Skoðunarrúðu > Kerfi > Fjárhagur > Fjárhagsuppsetning > Fjárhagsfæribreytur**.
2. Víkkaðu út hlutann **Lokun fjárhagsárs**.
3. Veldu **Já** eða **Nei** fyrir **Eyða lok árs viðskiptum við flutning** valmöguleika.
    
Ef fjárhagsári hefur verið lokað og lokun ársloka er keyrt aftur, er þessa stillingu mikilvæg. Ef stillt er á **Já**, skírteini fyrir síðustu áramót verður eytt og nýtt skírteini verður búið til fyrir alla reikninga upphafsstöðu. Ef stillt er á **Nei**, fyrri skírteinið verður áfram og nýtt skírteini verður aðeins búið til til að leiðrétta færslur sem voru bókaðar eftir síðustu áramót.

4. Veldu **Já** eða **Nei** fyrir **Búðu til lokafærslur meðan á flutningi stendur** valmöguleika.

Ef stillt er á **Já**, tvær færslur eru búnar til. Eitt fylgiskjal er búið til á því fjárhagsári sem verið er að loka til að færa stöður allra fjárhagsreikninga niður í núll og annað fylgiskjal er búið til á næsta fjárhagsári fyrir upphafsinnstæður. Ef stillt er á **Nei**, eitt fylgiskjal er búið til á næsta reikningsári fyrir upphafsstöður.  

5. Veldu **Já** eða **Nei** fyrir **Stilltu stöðu fjárhagsárs á varanlega lokað** valmöguleika.

Ef stillt er á **Já**, verður reikningsársstaðan stillt á Lokað varanlega. Vegna þess að ekki er hægt að opna varanlega lokað ár aftur, væri best að setja þennan valkost á **Nei**.  

6. Veldu **Já** eða **Nei** fyrir **Skráningarnúmer þarf að fylla út í lok árs** valmöguleika.

Ef stillt er á **Já**, verður að slá inn fylgiskjalsnúmer handvirkt í lok ársloka. Númeraröð er ekki notuð til að mynda þetta fylgiskjalsnúmer. Það er best að stilla þetta á **Já**.  

7. Lokið síðunni.
8. Farðu í **Fjárhagur > Tímabil er lokað > Árslokalokun**.
9. Smelltu á **Nýtt** til að stofna sniðmát árslokalokunar.

Hægt er ða stofna sniðmát fyrir hóp lögaðila sem á að keyra árslokalokun fyrir. Hægt er að endurnota þetta sniðmát ár eftir ár.  

10. Í **Nafn hóps** reit, sláðu inn heiti fyrir lok ársloka.
11. Í reitnum **Fjárhagsdagatal** velurðu fjárhagsárið sem sniðmátið verður stofnað fyrir.

Aðeins er hægt að flokka lögaðila sem nota sama fjárhagsárið saman í sniðmáti árslokalokunar . Þetta er vegna þess að árslokalokun er gerð með því að velja fjárhagsár, en ekki dagsetningu.  

12. Í **Aðgerðasvæðinu** smellirðu á **Vista**.
13. Í hlutanum **Lögaðilar** smellirðu á **Bæta við** til að velja lögaðila fyrir þetta sniðmát.
    
Hægt er að bæta lögaðilar við með því að velja annað hvort lögaðila eða með því að velja stigveldi fyrirtækis. Aðeins verður bætt við lögaðilum sem eru með stigveldi fyrirtækis með sama fjárhagsdagatal valið.  

14. Velja annaðhvort lögaðila eða stigveldisskipan.
15. Smellt er á **OK**.
16. Veldu **Já** eða **Nei** í **Flutningur efnahagsreikningsvídd**.

Það er best að stilla þennan valkost á **Já** fyrir efnahagsreikninga. Þetta viðheldur fjárhagsvíddum á bókaðar færslur þegar stofnaðir eru upphafsstöður fyrir efnahagslykla. Fyrir rekstrarreikninga geturðu valið að viðhalda fjárhagsvíddum (**Lokaðu öllu**) þegar innstæður eru færðar í Óráðstafað hagnað eða þú getur valið að láta fjárhagsvíddir skipt út fyrir annað víddargildi (**Loka smáskífur**). Ef þú velur **Loka smáskífur**, þú getur skilgreint tiltekið víddargildi fyrir hverja vídd eða jafnvel valið að skilja það eftir autt.  

17. Smellt er á **Vista**.
18. Hefja árslokalokun með því að velja **Keyra fjárhagslokun** á **Aðgerðarúðunni**. Árslokalokun verður keyrt fyrir valið sniðmát.  
19. Veldu allt eða hlutmengi lögaðila úr sniðmátinu úr hverju á að keyra árslokalokunina.

Þegar fyrst er keyrt árslokalokun, þá gætu flest fyrirtæki valið að keyra árslokalokun fyrir alla lögaðila innan þess sniðmáts til að fá upphafsstöður. Ef leiðréttingarfærslur eru gerðar eftir það, geturðu valið að keyra árslokalokun fyrir aðeins þeirra lögaðila sem hafa leiðréttingar.  

20. Smellt er á **OK**.
21. Velja fjárhagsár sem árslokalokun verður keyrð fyrir.
22. Í reitinn **Fylgiskjal** skal slá inn gildi. Bestu starfsvenjur eru að hafa fjárhagsár í fylgiskjalsnúmerinu, til að auðvelda að finna fylgiskjal árslokalokunar sem er stofnaður.  
23. Árslokalokunin er sjálfgefið keyrt í runu. Það eru bestu starfsvenjur fyrir langtímaferli til að keyra í runuhætti. Þetta er yfirleitt eitt af þessum ferlum, og er það ástæðan fyrir því að sjálfgefið er að nota runuhátt.  
24. Smellt er á **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
