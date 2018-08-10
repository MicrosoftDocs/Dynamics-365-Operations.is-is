---
title: "Leiðrétting textareiknings"
description: "Þessi grein útskýrir hvernig á að leiðrétta reikningur með frjálsum texta sem hefur verið bókaður og endurútgefa hann sem leiðréttan reikning."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cbae4c444db29a8dc7f3040aa78e45c0da092efd
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="correct-a-free-text-invoice"></a>Leiðrétting textareiknings

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að leiðrétta reikningur með frjálsum texta sem hefur verið bókaður og endurútgefa hann sem leiðréttan reikning.

Til að leiðrétta textareikning sem þegar hefur verið bókaður, skal opna bókaðan textareikning. Á síðunni **Reikningur** skal velja **Hætta við**, og veljið síðan **Leiðrétta reikning**. Velja ástæðukóða, bæta við athugasemd og veljið°dagsetningu fyrir nýjan leiðréttan reikning. Hægt er að breyta leiðrétta reikningnum og bóka hann. 

Þegar leiðrétti reikningurinn er bókaður, er afturköllunarreikningur stofnaður fyrir kredit-upphæð sem er jöfn upphaflegri upphæð reikningsins. Þess vegna er samanlögð staða upprunalega reikningsins og afturköllunarreikningsins 0 (núll). Afturköllunarreikningurinn er jafnaður á móti upprunalega reikningnum. 

Eftir að leiðrétti reikningurinn er bókaður, verða þrír reikningar:

-   **Upprunalegi reikningurinn** – reikningurinn sem inniheldur upplýsingarnar sem verið er að leiðrétta.
-   **Afturköllunarreikningur** – kerfismyndaður kreditreikningur sem var stofnaður til að hætta við reikninginn sem var síðast leiðréttur.
-   **Leiðréttur reikningur** – reikningurinn sem inniheldur leiðréttar reikningsupplýsingar.

Hægt er að þekkja afturköllunarreikninga og leiðrétta reikninga á tvo vegu:

-   Síðan **Allir reikningar með frjálsum texta** inniheldur **Leiðrétting** dálk,°þar sem hægt er að sjá hvaða reikningar eru afturköllunarreikningar og leiðréttir reikningar.
-   Haus textareikningsins sýnir stöðuna **Afturköllunarreikningur ‚\[reikningsnúmer\]'** eða **Leiðréttur reikningur '\[reikningsnúmer\]'**.

> [!NOTE]
> Þessi aðgerð er bara tiltæk ef **Leiðrétting á textareikningi** skilgreiningarlykill er valinn.




