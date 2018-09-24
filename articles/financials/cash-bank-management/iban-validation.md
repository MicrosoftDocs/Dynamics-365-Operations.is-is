---
title: "Stjórna villuleit á reikningi með alþjóðlegt bankareikningsnúmer (IBAN)"
description: "Þetta efnisatriði útskýrir hvernig á að stjórna villuleit á reikningi með alþjóðlegt bankareikningsnúmer (IBAN)."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: is-is
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a>Stjórna villuleit á reikningi með alþjóðlegt bankareikningsnúmer (IBAN)

[!include [banner](../includes/banner.md)]

Villuleit á reikningi með alþjóðlegt bankareikningsnúmer (IBAN) eykur fjölda villuleita sem gerðar eru þegar þú bætir IBAN við bankareikning.

Skipulag IBAN er geymt í Microsoft Dynamics 365 for Finance and Operation og er sjálfkrafa hlaðið upp þegar þú notar IBAN í fyrsta skipti fyrir bankareikning. Bankareikningsnúmerið er hluti af skipulagi sem er skilgreint fyrir IBAN númer. Byggt á því skipulagi, ef staða og lengd reikningsnúmersins í IBAN passar ekki við stöðuna sem er skilgreind í skipulaginu fyrir hvert land eða hvert svæði, færðu viðvörunarboð.

## <a name="set-up-iban-structures"></a>Setja upp IBAN-skipulag

1. Farðu í **Reiðufjár- og bankastjórnun \> Uppsetning \> IBAN-skipulag**.
2. Takið eftir að IBAN-skipulagið fyrir hvert land eða hvert svæði hefur verið sett upp sjálfkrafa.
3. Ef þú verður að sérstilla skipulagið fyrir tiltekið land eða svæði, getur þú breytt því.
4. Skilgreiningar skipulags verða hluti af öllum nýjum útgáfum. Þú getur notað valmyndina **Endurstilla skipulag** til að hlaða niður nýjustu skilgreiningunum eftir hverja uppfærslu.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Villuleita IBAN-skipulag á bankareikningi

1. Farið í **Reiðufjár- og bankastjórnun \> Bankareikningar \> Bankareikningar**.
2. Stofna bankareikning.
3. Í flýtiflipanum **Viðbótarupplýsingar** skal slá inn IBAN-númeri.

    Ef staða og lengd reikningsnúmersins í IBAN passar ekki við stöðuna sem er skilgreind í skipulaginu fyrir hvert land eða hvert svæði, færðu viðvörunarboð. Þú getur ekki haldið áfram ef lengd IBAN-númers passar ekki við lengdina í IBAN-skipulaginu.

    Villuleitin staðfestir einnig að bankareikningsnúmerið samsvarar þeim hluta IBAN-númersins sem táknar bankareikningsnúmerið. Ef bankareikningsnúmerið passar ekki, færðu viðvörunarboð. Þessi skilaboð eru aðeins viðvörun. Þú getur haldið áfram, jafnvel þótt bankareikningsnúmerið passi ekki.

