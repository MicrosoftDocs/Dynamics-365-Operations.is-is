---
title: "Stofna og vinna með birgðalæsingu"
description: "Þessi verklýsing sýnir hvernig á að koma í veg fyrir að efnislegar lagerbirgðir séu frátekinn af önnur upprunaskjöl á útleið með því að nota lokun birgða."
author: perlynne
manager: AnnBe
ms.date: 12/02/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7272349cf16b9459823a752b8d3df915f42606ef
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-maintain-inventory-blocking"></a>Stofna og vinna með birgðalæsingu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að koma í veg fyrir að efnislegar lagerbirgðir séu frátekinn af önnur upprunaskjöl á útleið með því að nota lokun birgða. Hægt er að keyra ferlið sýnigögn fyrirtækisins USMF með dæmagildum sem eru sýndar. Þú þarft að hafa vöru á lager raunbirgðum tiltækt áður en byrjað er að þetta ferli.


## <a name="create-an-inventory-blocking"></a>Stofna birgðalæsing
1. Fara í birgðastjórnun > Reglubundin verkefni >birgðalæsing.
2. Smellið á „Nýtt“.
3. Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.
4. Veljið vöruna sem á að velja af listanum.
    * Veljið vörunúmer með efnislegar lagerbirgðir sem á að loka. Ef verið er að nota USMF er hægt að velja vöru M9201.  
5. Færið inn númer í reitnum „Magn“.
    * Ef verið er að nota vöru M9201, þarf að velja minna en 200.  
6. Víxla útvíkkun á hlutanum birgðavíddir.
7. Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.
8. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Ef verið er að nota M9201 vöru er hægt að velja vöruhús 51.  
9. Smellið á „Vista“.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Uppfæra skilyrðum fyrir birgðalæsing
1. Færið inn númer í reitnum „Magn“.
    * Uppfæra magnsvæði birgða til að endurspegla magn til að loka.  
2. Færa inn dagsetningu í svæðinu áætluð dagsetning.
    * Þú vilt kannski tilgreina þegar búist er við að læstar birgðir verða tiltækar til frátektar með því að úthluta væntanleg dagsetning.. Ef Áætlað innhreyfingar valkostur er valinn fyrir við birgðalæsing, eins og hann er sjálfgefinn þegar handvirkt við er stofnuð lokun, þessi dagsetning birtist á áætlaðrar færslu.  
3. Smellið á „Vista“.

## <a name="remove-the-inventory-blocking"></a>Fjarlægja birgðalæsingu
1. Smellið á Eyða.
2. Smella á Já.
3. Lokið síðunni.

