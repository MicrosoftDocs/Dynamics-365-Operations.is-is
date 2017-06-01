---
title: "Greiðsluhættir í símaveri"
description: "Þetta efnisatriði fjallar um mismunandi greiðslumáta sem hægt er að nota í símaveri í Smásölu og viðskipti."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 930264f9c22cbde102b59237e432df7d7e4836c8
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="payment-methods-in-a-call-center"></a>Greiðsluhættir í símaveri

[!include[banner](includes/banner.md)]


Þetta efnisatriði fjallar um mismunandi greiðslumáta sem hægt er að nota í símaveri í Smásölu og viðskipti.

Greiðsluháttunum sem notaðir eru í öðrum rása í smásala og viðskipti í Microsoft Dynamics AX, eins og reiðufé ávísanir, kreditkort og gjafakort, einnig er hægt að nota í símaverum. Eftir að þú hefur sett upp greiðslumáta fyrir símaver, birtist það sem einn af valkostunum í hlutanum **greiðslur** í **sölupöntun** síðunni fyrir notendur símavers. Þú getur að auki sett upp á afsláttarmiða til bjóða afslátt til viðskiptavina sem setja inn pöntun hjá símaþjónustuver fyrirtækis þíns. Afsláttarmiðar getur verið föst upphæð afsláttar eða prósentu vöruverð eða heildarupphæð pöntunar. Til dæmis upphæð afsláttarmiða gæti verið að bjóða viðskiptavinum 75.00 afslátt þegar viðskiptavinurinn eyðir 750.00 eða meiru. Hægt að stofna mismunandi gerðir af afsláttarmiða, setja upp móðurfyrirtækis/útibús afsláttarmiða, og afrita eða ógilda afsláttarmiða. Notið valkostina í eftirfarandi töflu til að stofna afsláttarmiða.

|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Eigind**             | Í **innlausnartaxti** svæðinu, færið inn gildi áætlaða innlausnartaxti fyrir afsláttarmiða sem prósentu, og veljið hvort afsláttarmiðinn er einnota, verður sjálfkrafa endurútgefinn eða á við tiltekinn viðskiptavin.                                                                                                                                                                                                                                                                                                                                                                                       |
| **Gilt**                 | Í **Upphafsdagsetning** og **lokadagsetning** reitir skal færa inn dagsetningar fyrir fyrsta og síðasta daga sem afsláttarmiðinn gildir.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Innifela/útiloka reglur** | Í **vörulisti** og**vörur** svæðunum, skal velja hvort allar vörulista eða vörum er tekin með eða skilinn eftir í afsláttarmiðann. Ef valið er **Taka með** eða **Útiloka**, smellið á **Setja upp**, veljið **taka Með/útiloka vörulista** eða **taka Með/útiloka afurðir**, og færa inn upplýsingar um vörulista eða vöru. Ef **ekkert** er valið í þessum svæðum, allir vörulistar eða vörur eru teknar með í afsláttarmiðann.                                                                                                                                                                                                                          |
| **Ýmislegt**         | Ef ekki er hægt að nota þennan afsláttarmiða með öðrum afslætti, veljið þá **Sértækt** gátreitinn. Síðan, í **Uppruna** svæðinu, veljið þar sem hægt er að nota afsláttarmiðann. Ef þetta er afsláttarmiði framleiðanda, velja **Afsláttarmiði framleiðanda**  gátreitinn.                                                                                                                                                                                                                                                                                                                                                                |
| **Framtíðarafsláttarmiðar**         | Ef þessi afsláttarmiða verður tengt við aðra afsláttarmiða sem yfireining, veljið **Yfireining afsláttarmiði** gátreitinn. Ef þessi afsláttarmiði ætti að vera tengd sem undirstig afsláttarmiða með fyrirliggjandi afsláttarmiða, veljið **kenni yfirafsláttarmiði**  svæði. Til dæmis viltu stofna afsláttarmiða fyrir vörulistann næsta vors. Öll önnur afsláttarmiða sem þú stofnar fyrir vorvörulistann yrðu undireiningar afsláttarmiða í vorvörulistanum. Undirafsláttarmiða geta innihaldið 20 prósent afslátt fyrir nýjar pantanir viðskiptavinar, afslátt 10 prósent af nýlega útgefnar vöru eða 95,00 af pantanir upp á 1.000,00 eða meira. |

Ef leggja á fram kreditkortagreiðslu úr **sölupöntun** síða og færð boð sem tilgreinir að kreditkorti fékk ekki heimild er hægt að annast heimild handvirkt. Hægt er að heimila, hafna eða endursenda kreditkortafærslu með því að nota **stjórnun heimilda** síðu. Síðu færibreytum símavers er notuð til að skilgreina viðbótarupplýsingar greiðsluvinnslu valkosti:

-   Ávísanabið láta fjármálastarfsfólk vinna pantanir sem hafa verið sett í bið þar sem ávísun var notuð sem greiðslumáti og ávísunin bið farið var yfir þröskuldsupphæð. Bið hægt að losa handvirkt eða sjálfvirkt eða það rennur út í lok skilgreindu tímabili.
-   Hægt er að setja þröskulda, fyrir ofan þá þurfa ávísanir og kreditkort að fá handvirka samþykkt vegna endurgreiðslna. Endurgreiðsla sem fer yfir þröskuldsgildi upphæð er bætt við samþykki biðröð. Eftir að þú samþykkja endurgreiðslu er hægt að reikningsfæra skilasölupöntunina.





