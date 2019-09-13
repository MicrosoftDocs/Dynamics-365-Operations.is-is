---
title: Stofna og viðhalda á birgðalæsing
description: Þessi verklýsing sýnir hvernig á að koma í veg fyrir að efnislegar lagerbirgðir séu frátekinn af önnur upprunaskjöl á útleið með því að nota lokun birgða.
author: perlynne
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2485eaf31226b11106895074ae0ad95e561777b
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916600"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Stofna og viðhalda á birgðalæsing

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að koma í veg fyrir að efnislegar lagerbirgðir séu frátekinn af önnur upprunaskjöl á útleið með því að nota lokun birgða. Hægt er að keyra ferlið sýnigögn fyrirtækisins USMF með dæmagildum sem eru sýndar. Þú þarft að hafa vöru á lager raunbirgðum tiltækt áður en byrjað er að þetta ferli.


## <a name="create-an-inventory-blocking"></a>Stofna birgðalæsing
1. Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Birgðastýring > Reglubundin verk > Birgðalæsing**.
2. Smellt er á **Nýtt**.
3. Í reitnum **Vörunúmer** skal smella á fellilistahnappinn til að opna leitina.
4. Veljið vöruna sem á að velja af listanum. Veljið vörunúmer með efnislegar lagerbirgðir sem á að loka. Ef verið er að nota USMF er hægt að velja vöru M9201.  
5. Í reitnum **Magn** slærðu inn tölu. Ef verið er að nota vöru M9201, þarf að velja minna en 200.
6. Útvíkkaðu flýtiflipann **Birgðavíddir**.
7. Í reitnum **Vöruhús** skal smella á fellilistahnappinn til að opna leitina.
8. Í listanum skal finna og velja þá skráningu sem óskað er eftir. Ef verið er að nota M9201 vöru er hægt að velja vöruhús 51.  
9. Smellt er á **Vista**.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Uppfæra skilyrðum fyrir birgðalæsing
1. Á flýtiflipanum **Almennt**, í reitnum **Magn** skal slá inn tölu. Uppfæra magnsvæði birgða til að endurspegla magn til að loka.  
2. Í reitnum **Væntanleg dagsetning** skal færa inn dagsetningu. Þú vilt kannski tilgreina þegar búist er við að læstar birgðir verða tiltækar til frátektar með því að úthluta væntanleg dagsetning.. Ef Áætlað innhreyfingar valkostur er valinn fyrir við birgðalæsing, eins og hann er sjálfgefinn þegar handvirkt við er stofnuð lokun, þessi dagsetning birtist á áætlaðrar færslu.  
3. Smellt er á **Vista**.

## <a name="remove-the-inventory-blocking"></a>Fjarlægja birgðalæsingu
1. Í **Aðgerðasvæðinu** skal smella á **Eyða**.
2. Smellið á **Já**.
3. Lokið síðunni.

