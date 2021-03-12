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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: b206dbda56acd4fcd4aa98be4b5e0d6c839f0354
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976417"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>Stjórna villuleit á reikningi með alþjóðlegt bankareikningsnúmer (IBAN)

[!include [banner](../includes/banner.md)]

Villuleit með alþjóðlegu bankareikningsnúmeri (IBAN) eykur fjölda villuleita sem gerðar eru þegar þú bætir IBAN við bankareikning.

Upplýsingar um skipulag IBAN er geymd í Microsoft Dynamics 365 Finance. Þessar upplýsingar eru sjálfkrafa hlaðnir þegar þú notar IBAN fyrst á bankareikningum. Það inniheldur lengd IBAN, upphafsstöðu bankareikningsrnúmers og leiðarrnúmer og lengd bankareikningsnúmersins og leiðarrnúmersins.

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
