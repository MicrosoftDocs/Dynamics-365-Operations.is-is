---
title: Leiðrétting textareiknings
description: Þessi grein útskýrir hvernig á að leiðrétta reikningur með frjálsum texta sem hefur verið bókaður og endurútgefa hann sem leiðréttan reikning.
author: abruer
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3cc07a1f0ba444250eddcf892681e2ca63e9c1a
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780260"
---
# <a name="correct-a-free-text-invoice"></a>Leiðrétting textareiknings

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að leiðrétta reikningur með frjálsum texta sem hefur verið bókaður og endurútgefa hann sem leiðréttan reikning.

Til að leiðrétta ókeypis textareikning sem þegar hefur verið bókaður: 
1. Opnaðu birta reikninginn með frjálsum texta. 
2. Á síðunni **Reikningur** skal velja **Hætta við**, og veljið síðan **Leiðrétta reikning**. 
3. Velja ástæðukóða, bæta við athugasemd og veljið°dagsetningu fyrir nýjan leiðréttan reikning.
4. Hægt er að breyta leiðrétta reikningnum og bóka hann. 

Þegar leiðrétti reikningurinn er bókaður, er afturköllunarreikningur stofnaður fyrir kredit-upphæð sem er jöfn upphaflegri upphæð reikningsins. Þess vegna er samanlögð staða upprunalega reikningsins og afturköllunarreikningsins 0 (núll). Afturköllunarreikningurinn er jafnaður á móti upprunalega reikningnum. 

Eftir að leiðrétti reikningurinn er bókaður, verða þrír reikningar:

-   **Upprunalegi reikningurinn** – reikningurinn sem inniheldur upplýsingarnar sem verið er að leiðrétta.
-   **Afturköllunarreikningur** – kerfismyndaður kreditreikningur sem var stofnaður til að hætta við reikninginn sem var síðast leiðréttur.
-   **Leiðréttur reikningur** – reikningurinn sem inniheldur leiðréttar reikningsupplýsingar.

Hægt er að þekkja afturköllunarreikninga og leiðrétta reikninga á tvo vegu:

-   Síðan **Allir reikningar með frjálsum texta** inniheldur **Leiðrétting** dálk,°þar sem hægt er að sjá hvaða reikningar eru afturköllunarreikningar og leiðréttir reikningar.
-   Haus textareikningsins sýnir stöðuna **Afturköllunarreikningur ‚\[reikningsnúmer\]'** eða **Leiðréttur reikningur '\[reikningsnúmer\]'**.

> [!NOTE]
> Þessi aðgerð er bara tiltæk ef **Leiðrétting á textareikningi** skilgreiningarlykill er valinn. Frekari upplýsingar um hvernig á að virkja stillingarlykla er að finna í hlutanum Virkja (eða slökkva) stillingarlykla í [Viðhaldsstilling](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) grein. 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
