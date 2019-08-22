---
title: Stjórna villuleit á reikningi með alþjóðlegt bankareikningsnúmer (IBAN)
description: Þetta efnisatriði útskýrir hvernig á að stjórna villuleit á reikningi með alþjóðlegt bankareikningsnúmer (IBAN).
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 70c497ec575ffcaa6f2fdc3fe77bae7b41dc02fb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842426"
---
# <a name="manage-international-bank-account-number-iban-validation"></a>Stjórna villuleit á alþjóðlegu bankareikningsnúmerinu (IBAN)

[!include [banner](../includes/banner.md)]

Villuleit með alþjóðlegu bankareikningsnúmeri (IBAN) eykur fjölda villuleita sem gerðar eru þegar þú bætir IBAN við bankareikning.

Upplýsingar um skipulag IBAN er geymd í Microsoft Dynamics 365 for Finance and Operations. Þessar upplýsingar eru sjálfkrafa hlaðnir þegar þú notar IBAN fyrst á bankareikningum. Það inniheldur lengd IBAN, upphafsstöðu bankareikningsrnúmers og leiðarrnúmer og lengd bankareikningsnúmersins og leiðarrnúmersins.

## <a name="set-up-iban-structures"></a>Setja upp IBAN-skipulag

1. Farðu í **Reiðufjár- og bankastjórnun \> Uppsetning \> IBAN-skipulag**.
2. Takið eftir að IBAN-skipulagið fyrir hvert land eða hvert svæði hefur verið sett upp sjálfkrafa.
3. Ef þú vilt aðlaga skipulagið að tiltekið land eða svæði, getur þú breytt þeim.
4. Skilgreiningar skipulags verða hluti af öllum nýjum útgáfum. Þú getur notað valmyndina **Endurstilla skipulag** til að hlaða niður nýjustu skilgreiningunum eftir hverja uppfærslu.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Villuleita IBAN-skipulag á bankareikningi

1. Farið í **Reiðufjár- og bankastjórnun \> Bankareikningar \> Bankareikningar**.
2. Stofna bankareikning.
3. Í flýtiflipanum **Viðbótarupplýsingar** skal slá inn IBAN-númeri.

    Ef lengd IBAN er ekki í samræmi við lengd sem er skilgreind fyrir hvert land eða svæði, færðu viðvörunarskilaboð. Þú getur ekki haldið áfram ef lengd IBAN passar ekki lengdina sem tilgreind er í IBAN uppbyggingu.

    Villuleitin staðfestir einnig að bankareikningsnúmerið samsvarar þeim hluta IBAN-númersins sem táknar bankareikningsnúmerið. Ef bankareikningsrnúmerið passar ekki, færðu viðvörunarskilaboð. Þessi skilaboð eru aðeins viðvörun. Þú getur haldið áfram, jafnvel þótt bankareikningsnúmerið passi ekki.

    Villuleitin staðfestir einnig að leiðarnúmer bankans samsvari þeim hluta IBAN sem táknar leiðarnúmer bankans. Leiðarnúmerið inniheldur bankanúmer og oft viðbótarútibú bankans. Ef leiðarnúmer bankans passar ekki, færðu viðvörunarskilaboð. Þessi skilaboð eru aðeins viðvörun. Þú getur haldið áfram, jafnvel þótt leiðarnúmer bankans passi ekki saman.
