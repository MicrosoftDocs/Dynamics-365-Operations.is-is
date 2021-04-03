---
title: Búa til spurningu sem er háð svari við fyrri spurningu
description: Skilyrtar spurningar gera kleift að tilgreina hvaða eftirfylgni spurninguar eru boðnar svarendum, byggt á svarinu í fyrri spurningu.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a76220647417b6ff69e2f0ab5b2fa5297db5c49
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467844"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Búa til spurningu sem er háð svari við fyrri spurningu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



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



[!INCLUDE[footer-include](../includes/footer-banner.md)]