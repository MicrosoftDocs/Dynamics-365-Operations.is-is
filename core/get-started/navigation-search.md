---
title: Flettingaleit
description: "Þessi grein útskýrir hvernig skuli nota leitaraðgerðina og fletta í síður í Microsoft Dynamics 365 for Operations."
author: aneesmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 87fed576f8cf358520d94f5cd5b326ff9801913a
ms.lasthandoff: 03/31/2017


---

# <a name="navigation-search"></a>Flettingaleit

[!include[banner](../includes/banner.md)]


Þessi grein útskýrir hvernig skuli nota leitaraðgerðina og fletta í síður í Microsoft Dynamics 365 for Operations.

Dynamics 365 for Operations veitir eiginleika fyrir breitt svið iðnaðar og framleiðslu. Forritið felur í sér fjölda svæða og síður til að hjálpa þér að framkvæma ýmis verk. Til að finna fljótt þær síður sem þú þarft að ljúka verkefni, nota eiginleikann flettingaleit. Til að Nota þessa aðgerð þarf að smella á í **Leit** teiknið til að birta **Leit** gátreiturinn. Síðan er hægt að slá eitt eða fleiri orð í reitnum. Kerfið leitar strax að viðeigandi síðum í forritinu sem passa orð sem þú slóst inn. Til dæmis gætir þú slærð inn "reikningur lánardrottins" sem inntak, og þá birtir kerfið niðurstöður sem passa við inntak. **Ábending:** **Leit** gátreiturinn hjálpar til við að leita og fletta að síðum. Það ekki gagnast við að finna ákveðna gögn eða aðgerðir. 

[![leitarreitur](./media/search-box.png)](./media/search-box.png) Flettingaleitareiginleikinn þjónar einnig sem frábær leið fyrir þig til að fletta fljótt á ákveðna síðu. Til dæmis, ef þú ert starfsmaður viðskiptaskulda sem oft notar síðuna **Greiðslubók**, gætirðu slegið inn "greiðslubók" í leitarreitinn. Þar sem inntak er nákvæm samsvörun fyrir blaðsíðutitil, er síðan skráð á toppi af leitarniðurstöðum, og þú getur fljótt flett á það. 

[![leit í greiðslubók](./media/searching-for-payment-journal.png)](./media/searching-for-payment-journal.png) 

Leitarniðurstöðulistinn sýnir síðutitilinn auk flettingarleiðar. Þetta hjálpar þér að gera þér grein fyrir staðsetningu síðunnar í forritinu. Það hjálpar einnig til að aðgreina á milli tveggja eða fleiri svipuð síður í niðurstöðum. Þegar þú leitar að síðu, er inntak þitt er borin saman við síðutitli, auk flettingarleiðar. Ef til dæmis er fært er inn "kröfur" í ** **leitarreitnum sjást niðurstöður fyrir síður sem tiltæk er í svæðinu Viðskiptakröfur--jafnvel þótt titlar síðu innihalda ekki orðið "kröfur." 

[![leit í kröfum](./media/search-for-the-word-receivable.png)](./media/search-for-the-word-receivable.png) 

Vegna stjórnunar og öryggissjónarmiða sýnir flettingaleitareiginleikinn aðeins:

-   Síður sem eru virkjaðir í gildandi skilgreiningu (með skilgreiningarlykla).
-   Síður sem notandi hefur aðgang að byggt á hlutverki notanda

Lista yfir leitarniðurstöður takmarkast við 10 vörur. Ef þú finnur ekki það sem þú ert að leita að í niðurstöðum, ættir þú að reyna fínstillingu eða uppfæra inntak. Frá þróunarsjónarhóli er flettingaleitarvirkni mjög auðvelt að til að finna jafnvægi, þar er nánast engin töf milli uppsetningar valmyndaratriða og getu þeirra til að birtast í leitarniðurstöðum. Svo lengi sem tengt er í valmyndaratriðin annað hvort úr skoðunarrúðunni eða á yfirlitinu, verða þær sjálfkrafa finnanlegar. Flettingaleitarvirkni er einnig með mikið umbeðna aðgerð fyrir lengra komna: getu til fljótt fletta á síðu á grundvelli heitis á tæknilegri skjámynd. Margir notendur eru svo kunnugir kerfinu, að þeir vita nákvæmlega nöfn skjámyndar sem þeir vinna með. Ef þú ert einn af þessum notendum má færa inn **skjámynd: (form:)** og í kjölfarið kemur heiti skjámyndarinnar sem er leitað eftir. Til dæmis, ef fært er inn **form: vendinvoice**,sýna leitarniðurstöður allar síður þar sem heiti skjámyndar byrjar **vendinvoice**. 

[![leit fyrir vendinvoice sniðmát](./media/search-for-form-vendinvoice.png)](./media/search-for-form-vendinvoice.png)




