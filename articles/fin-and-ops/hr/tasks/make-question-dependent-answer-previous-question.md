--- 
title: "Búa til spurningu sem er háð svari við fyrri spurningu"
description: "Skilyrtar spurningar gera kleift að tilgreina hvaða eftirfylgni spurninguar eru boðnar svarendum, byggt á svarinu í fyrri spurningu."
author: twheeloc
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 05f7af94813934c1d77d6a509587280395f0e8bd
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Búa til spurningu sem er háð svari við fyrri spurningu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Skilyrtar spurningar gera kleift að tilgreina hvaða eftirfylgni spurninguar eru boðnar svarendum, byggt á svarinu í fyrri spurningu. Til dæmis, ef spyrja „Finnst þér betra kaffi eða te", röklegt eftirfylgni spurningu getur verið ákvörðuð eftir því hvort svarandi velur kaffi eða te sem svar sitt. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="find-the-existing-questionnaire"></a>Finna fyrirliggjandi spurningalista
1. Fara í Spurningalisti > Hönnun > Spurningalistar.
2. Velja spurningalistann WorkFH á listanum.

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>Bæta við spurningum og undirspurningar við Spurningalista
1. Smellt er á Spurningar.
2. Smellið á „Nýtt“.
3. Veljið númer spurningu 00016 í svæðinu Spurningu.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Smellið á „Vista“.
7. Lokið síðunni.

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>Stilla Röð Spurningalista á Skilyrt og gera spurninguna háða viðeigandi spurningu
1. Smellið á „Breyta“.
2. Víkka út hlutann Uppsetning.
3. Veljið 'Skilyrt' í svæðinu röðun Spurninga.
4. Smellt er á Skilyrðisbundin spurning
5. Veljið ‚Spurningar\útskýra hvers vegna þú svaraðir fyrri spurningu eins og þú gerðir?', í trénu.
6. Velja spurninguna 00009 í svæðinu aðalspurning
7. Í listanum skal smella á tengilinn í valinni línu.
8. Í svarreitnum, Færa inn Kenni svarraðar fyrir svarvalkost sem gera á spurningu háða. Settu Til dæmis inn 1 fyrir fyrsta svarvalkost.
9. Smelltu á Vista.
10. Í trénu, velja ‚Spurningar\ Ég fæ sanngjörn laun fyrir mína vinnu.'.
    * Athugið að spurningatréð var uppfært til að sýna háðar kringumstæður.  


