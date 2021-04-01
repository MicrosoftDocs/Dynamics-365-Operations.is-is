---
title: Loka fjárhagsári
description: Þetta ferli fara í gegnum árslokaferli sem flytja stöður yfir á nýtt fjárhagsár.
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6299325bb8d77cad3977ae3c20790122574b47f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235814"
---
# <a name="close-the-fiscal-year"></a>Loka fjárhagsári

[!include [banner](../../includes/banner.md)]

Þetta ferli fara í gegnum árslokaferli sem flytja stöður yfir á nýtt fjárhagsár.


## <a name="validate-year-end-close-parameters"></a>Villuleita færibreytur árslokalokunar
1. Farðu í **Skoðunarrúðu > Kerfi > Fjárhagur > Fjárhagsuppsetning > Fjárhagsfæribreytur**.
2. Víkkaðu út hlutann **Lokun fjárhagsárs**.
3. Veldu „Já“ eða „Nei“ fyrir valkostinn **Eyða lokunarfærslum árs í millifærslu**.
    
    Ef fjárhagsári hefur verið lokað og lokun ársloka er keyrt aftur, er þessa stillingu mikilvæg. Ef stillt á Já, verður fylgiskjali fyrir lok fyrra árs eytt, og nýtt fylgiskjali verða stofnaðar fyrir allar upphafsstöður lykla. Ef stillt á Nei, helst fyrri fylgiskjal og nýju fylgiskjali aðeins verður stofnuð til að leiðrétta færslur sem voru bókaðar eftir síðustu lokun ársloka.

4. Veldu „Já“ eða „Nei“ fyrir valkostinn **Stofna lokunarfærslur í millifærslu**.

    Ef setja á Já tvær færslur eru stofnaðar. Eitt fylgiskjal er stofnað í fjárhagsárinu sem verið er að loka til að færa stöður í P&L fjárhagslykla niður í núll og önnur fylgiskjal eru stofnuð á næsta fjárhagsári fyrir upphafsstöður. Ef stillt á Nei, eitt fylgiskjal er stofnuð á næsta fjárhagsári fyrir upphafsstöður.  

5. Veldu „Já“ eða „Nei“ fyrir valkostinn **Stilla stöðu fjárhagsárs á lokað fyrir fullt og allt**.

    Ef stillt á Já verður staða fjárhagsárs stillt á Endanlega lokað.  Þar sem ekki er hægt að enduropna varanlega lokað ár, væri bestu venju að þessi valkostur er stilltur á nei.  

6. Veldu „Já“ eða „Nei“ fyrir valkostinn **Rita þarf fylgiskjalsnúmer á meðan á lokun árs stendur**.

    Ef stillt á Já, verður að færa inn númer fylgiskjals handvirkt í árslokaferlinu. Númeraröð er ekki notuð til að mynda þetta fylgiskjalsnúmer. Bestu starfsvenjur er að setja þetta á Já.  

7. Lokið síðunni.
8. Farðu í **Fjárhagur > Tímabil er lokað > Árslokalokun**.
9. Smelltu á **Nýtt** til að stofna sniðmát árslokalokunar.

    Hægt er ða stofna sniðmát fyrir hóp lögaðila sem á að keyra árslokalokun fyrir. Hægt er að endurnota þetta sniðmát ár eftir ár.  

10. Í reitnum **Heiti hóps** færirðu inn sniðmátsheiti árslokalokunar.
11. Í reitnum **Fjárhagsdagatal** velurðu fjárhagsárið sem sniðmátið verður stofnað fyrir.

    Aðeins er hægt að flokka lögaðila sem nota sama fjárhagsárið saman í sniðmáti árslokalokunar . Þetta er vegna þess að árslokalokun er gerð með því að velja fjárhagsár, en ekki dagsetningu.  

12. Í **Aðgerðasvæðinu** smellirðu á **Vista**.
13. Í hlutanum **Lögaðilar** smellirðu á **Bæta við** til að velja lögaðila fyrir þetta sniðmát.
    
    Hægt er að bæta lögaðilar við með því að velja annað hvort lögaðila eða með því að velja stigveldi fyrirtækis.  Aðeins verður bætt við lögaðilum sem eru með stigveldi fyrirtækis með sama fjárhagsdagatal valið.  

14. Velja annaðhvort lögaðila eða stigveldisskipan.
15. Smellt er á **OK**.
16. Veldu „Já“ eða „Nei“ í **Flytja víddir efnahagsreiknings**.

    Bestu starfsvenjur eru að stilla þennan valkost á Já fyrir efnahagslykla. Þetta viðheldur fjárhagsvíddum á bókaðar færslur þegar stofnaðir eru upphafsstöður fyrir efnahagslykla. Fyrir rekstrarlykla, er hægt að velja að vinna með fjárhagsvíddir (Loka öllum) þegar stöður eru fluttar yfir á óráðstafað eigið fé eða þú getur valið að hafa fjárhagsvíddir skipt út fyrir annað víddargildi (Loka einum). Ef þú velur Loka einum, geturðu skilgreint tiltekið víddargildi fyrir hverja vídd eða jafnvel valið að skilja eftir autt.  

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