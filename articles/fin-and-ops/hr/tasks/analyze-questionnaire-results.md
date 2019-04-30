---
title: Greina niðurstöður spurningalista
description: Hægt er að nota talnagögn spurningalista til að reikna út meðaltöl, samtölur og prósentur samkvæmt lýðfræðilegum gögn.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d8f9c2fcf0be117f8fcde5113c0d42f11786679
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/19/2019
ms.locfileid: "858584"
---
# <a name="analyzing-questionnaire-results"></a>Greina niðurstöður spurningalista

[!include [task guide banner](../../includes/task-guide-banner.md)]

Hægt er að nota talnagögn spurningalista til að reikna út meðaltöl, samtölur og prósentur samkvæmt lýðfræðilegum gögn. Til að hefja ferlið, farið í Spurningalist > Skoða og greina niðurstöður > Talnagögn spurningalista. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="create-a-questionnaire-statistics-record"></a>Stofna færslu fyrir talnagögn Spurningalista
1. Fara á talnagögn spurningalista
2. Smellið á „Nýtt“.
3. Í listanum skal merkja valda línu.
4. Í reitnum talnagögn skal færa inn gildi.
5. Í reitinn Lýsing skal slá inn gildi.
6. Í reitnum Spurningalisti skal smella á fellilistahnappinn til að opna leitina.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Smellið á flipann „Almennt“.
    * Veljið ef óskað er að taka með niðurstöður fyrir ónafngreinda eða niðurstöður úr starfsmönnum, tengiliði og umsækjendur.  
9. Veldu eða hreinsaðu gátreitinn starfsmaður.
    * Ef þú verður að skoða niðurstöður eftir aldur eða starfsaldur, tilgreina bil sem óskað er að nota til að flokka niðurstöðurnar.  
    * Innfærsla á 5 fyrir aldursbilið mun flokka niðurstöðurnar samkvæmt fimm ár aldursbila.  
10. Í reitinn aldur skal slá inn númer.
    * Veljið ef óskað er að keyra útreikning gagnvart öllum spurningalistanum, fyrir hvern niðurstöðuflokk, fyrir hverja spurningu, eða fyrir hvern spurningaröð.  
    * Velja hvernig óskað er að flokka niðurstöðurnar.  
    * Til dæmis, ef meðaltal punkta fyrir hverja spurningu er reiknað, viltu e.t.v. sjá spurningar flokkuð eftir niðurstöðuflokki.  
    * Velja gögn til að byggja útreikning á.  
    * Til dæmis, ef óskað er að sjá meðaltalsprósent sem fékkst úr í spurningalista á meðal starfsmenn þinna eða meðaltal stigafjölda sem var náð á meðal starfsmanna þinna.  
11. Smellt er á flipann Svið.
    * Notið afmarkanir til að takmarka niðurstöðum við einungis þá sem uppfylla skilyrði afmörkunar.  
12. Smellið á flipann Flokkun .
    * Flokkanir er notuð til að ákvarða hvernig á að birta niðurstöður.  
    * Til dæmis flokka niðurstöðurnar fyrst eftir kyni, síðan eftir aldri.  
13. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Flytja í flokkanir inn á valda hlið og setja þær í viðeigandi röð.  

## <a name="execute-the-statistics-calculation"></a>Framkvæma útreikningur talnagagna
1. Smelltu á Keyra.
    * Velja hvaða aðgerð útreiknings sem óskað er að framkvæma á niðurstöður.  
    * Til dæmis er hægt að reikna meðaltal prósentur milli spurningalista fyrir valdar flokkanir eða samtala punkta yfir niðurstöðuflokka fyrir valdar flokkanir.  
2. Veljið eða hreinsið gátreit Eyða fyrri leit.
3. Smellið á „Í lagi“.

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a>Skoða niðurstöður keyrslu talnagögn spurningalista.
1. Smelltu á Niðurstöður.
2. Smelltu á Niðurstöður.
3. Lokið síðunni.

