---
title: Flettingaleit
description: "Þessi skrá er útskýrt hvernig notið leitaraðgerðina til að fletta á síður í Microsoft Dynamics 365 fyrir Aðgerðir."
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

Þessi skrá er útskýrt hvernig notið leitaraðgerðina til að fletta á síður í Microsoft Dynamics 365 fyrir Aðgerðir.

Dynamics 365 fyrir Aðgerðir sem veitir fyrir breið fylki industries og verticals. Forritið felur í sér fjölda svæða og síður til að aðstoða við að framkvæma ýmsar aðgerðir. Nota aðgerðina leit skoðunarrúðunni til að finna síður sem þú þarft að ljúka við verkefni. Til að Nota þessa aðgerð þarf að smella á í **Leit** teiknið til að birta **Leit** gátreiturinn. Síðan er hægt að slá eitt eða fleiri orð í reitnum. Kerfið leitar strax að viðeigandi síðum í forritinu sem passa orð sem þú slóst inn. Til dæmis gætir þú slærð inn "reikningur lánardrottins" sem inntak, og þá birtir kerfið niðurstöður sem passa við inntak. **Ábending:** **Leit** gátreiturinn hjálpar til við að leita og fletta að síðum. Það ekki gagnast við að finna ákveðna gögn eða aðgerðir. 

[![leit gátreiturinn](./media/search-box.png)](./media/search-box.png) yfirlitstegundar search eiginleiki þjónar einnig sem línanna er meiri leið til að fara í ákveðna síðu. Til dæmis, ef þú ert með viðskiptaskuldum afgreiðslumaður sem oft notar á **greiðslubók** síðu væri að færa inn "greiðslubók" í reit leit. Þar á inntak er nákvæm samsvörun fyrir titill síðunnar síðan sé skráður efst á leitarniðurstöðum og er hægt að fara í hana. 

[![leit-fyrir--greiðslubók](./media/searching-for-payment-journal.png)](./media/searching-for-payment-journal.png) 

Í leitarniðurstöðulisti birtir titill síðunnar auk slóð yfirlitstegundar. Þetta hjálpar þér að gera þér grein fyrir staðsetningu síðunnar í forritinu. Það hjálpar einnig til að aðgreina á milli tveggja eða fleiri svipuð síður í niðurstöðum. Þegar þú leitar að síðu, er inntak þitt er borin saman við síðutitli, auk flettingarleiðar. Til dæmis, ef fært er inn "viðskiptavina" í á ** ** leit reitnum sjást niðurstöður fyrir síður sem tiltæk er í svæðinu Viðskiptakröfur--jafnvel þótt titla síðu innihalda orðið "viðskiptavini." 

[![leit-fyrir-í-word-viðskiptavinir](./media/search-for-the-word-receivable.png)](./media/search-for-the-word-receivable.png) 

Stjórnun og öryggi, skoðun leita einungis surfaces virkni:

-   Síður sem eru virkjaðir í gildandi skilgreiningu (með skilgreiningarlykla).
-   Síður sem notandi hefur aðgang að byggt á hlutverki notanda

Lista yfir leitarniðurstöður takmarkast við 10 vörur. Ef þú finnur ekki það sem þú ert að leita að í niðurstöðum, ættir þú að reyna fínstillingu eða uppfæra inntak. Frá þróunarsjónarhóli er flettingaleitarvirkni mjög auðvelt að til að finna jafnvægi, þar er nánast engin töf milli uppsetningar valmyndaratriða og getu þeirra til að birtast í leitarniðurstöðum. Svo lengi sem tengt er í valmyndaratriðin annað hvort úr skoðunarrúðunni eða á yfirlitinu, verða þær sjálfkrafa finnanlegar. Flettingaleitarvirkni er einnig með mikið umbeðna aðgerð fyrir lengra komna: getu til fljótt fletta á síðu á grundvelli heitis á tæknilegri skjámynd. Margir notendur eru svo kunnugir kerfinu, að þeir vita nákvæmlega nöfn skjámyndar sem þeir vinna með. Ef þú ert einn af þessum notendum má færa inn **skjámynd: (form:)** og í kjölfarið kemur heiti skjámyndarinnar sem er leitað eftir. Til dæmis, ef fært er inn **form: vendinvoice**,sýna leitarniðurstöður allar síður þar sem heiti skjámyndar byrjar **vendinvoice**. 

[![leit-fyrir-skjámynd-vendinvoice](./media/search-for-form-vendinvoice.png)](./media/search-for-form-vendinvoice.png)


