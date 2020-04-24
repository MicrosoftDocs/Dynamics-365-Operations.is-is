---
title: Endurnota afurðarafbrigði
description: Hægt er að tilgreina að sjálfkrafa eigi að nota aftur fyrirliggjandi afbrigði fyrir vöru. Síðan, þegar notandi hefur lokið skilgreinarlotu athugar kerfið hvort skilgreining sem samsvarar vali notanda er þegar til. Ef samsvarandi skilgreiningu finnst er auðkenni Skilgreiningar, samsvarandi uppskrift (BOM), og leið endurnotuð.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f72d93600db3d9bf0a44ac1fe84111527bb31d0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209403"
---
# <a name="reuse-product-configurations"></a>Endurnota afurðarafbrigði

[!include [banner](../includes/banner.md)]

Hægt er að tilgreina að sjálfkrafa eigi að nota aftur fyrirliggjandi afbrigði fyrir vöru. Síðan, þegar notandi hefur lokið skilgreinarlotu athugar kerfið hvort skilgreining sem samsvarar vali notanda er þegar til. Ef samsvarandi skilgreiningu finnst er auðkenni Skilgreiningar, samsvarandi uppskrift (BOM), og leið endurnotuð.

<a name="requirements-for-reusing-configurations"></a>Skilyrði til að geta endurnotað afbrigði
---------------------------------------

Til að geta látið endurnota afurður, verður að tilgreina eftirfarandi upplýsingar um íhluti og eigindir í síðunni **upplýsingar um afbrigðalíkan afurðar** :

-   **Íhlutir og undiríhlutir** - á flipanum **almennt** í reitnum **endurnota afbrigði**, veldu **já**.
-   **Eigind** – Á **Eigind** flýtiflipi, veldu **Hafa með í endurnotkun** valkost. Þessi valkostur er aðeins tiltækur þegar tengdur íhlutur er virkjaður fyrir endurnotkun. Ef þú velur engin eigindi til endurnotkunar, er afbrigðið alltaf endurnotað, óháð vali notandans á meðan verið var að skilgreina. Eigindagildi á fyrirliggjandi skilgreiningu verða passa við vali notanda. Til dæmis, ef notandinn velur **blár** sem lit á meðan á skilgreiningu stendur, athugar kerfið hvort fyrirliggjandi afbrigði íhlutar hafi litinn bláan.

## <a name="resetting-configuration-reuse"></a>Endurstilling endurnotkun skilgreiningar
Þegar þú endurstillir endurnotkun skilgreiningar, er ekki lengur tekið tillit til áður stofnaðra skilgreininga. Þú gætir viðjal endurstilla endurnotkun skilgreiningar ef uppskriftin eða leiðin var breytt, en ekki var breytt tengdar eigindir. Þú endurstillir endurnotkun skilgreiningar á flipanum **Almennt** fyrir íhlut.



