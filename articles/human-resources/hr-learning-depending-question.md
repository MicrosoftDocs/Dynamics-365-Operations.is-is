---
title: Búa til spurningu sem er háð svari við fyrri spurningu
description: Skilyrtar spurningar gera kleift að tilgreina hvaða eftirfylgni spurninguar eru boðnar svarendum, byggt á svarinu í fyrri spurningu.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11787aa0b32c0d7493e4528b00304e51f01a655f
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728907"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Búa til spurningu sem er háð svari við fyrri spurningu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Skilyrtar spurningar gera kleift að tilgreina hvaða eftirfylgni spurninguar eru boðnar svarendum, byggt á svarinu í fyrri spurningu. Til dæmis, ef spyrja „Finnst þér betra kaffi eða te", röklegt eftirfylgni spurningu getur verið ákvörðuð eftir því hvort svarandi velur kaffi eða te sem svar sitt. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="find-the-existing-questionnaire"></a>Finna fyrirliggjandi spurningalista
1. Fara til **Spurningalisti** > **Hönnun** > **Spurningalistar**.
2. Velja spurningalistann WorkFH á listanum.

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>Bæta við spurningum og undirspurningar við Spurningalista
1. Smellur **Spurningar**.
2. Smellt er á **Nýtt**.
3. Í **Spurning** reit, veldu spurningu númer 00016.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Smelltu á **Vista**.
7. Lokið síðunni.

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>Stilla Röð Spurningalista á Skilyrt og gera spurninguna háða viðeigandi spurningu
1. Smellið á **Breyta**.
2. Útvíkkaðu kaflann **Uppsetning**.
3. Í **Spurninga röð** reit, veldu 'skilyrt'.
4. Smellur **Skilyrt** spurningu.
5. Veljið ‚Spurningar\útskýra hvers vegna þú svaraðir fyrri spurningu eins og þú gerðir?', í trénu.
6. Í **Aðalspurning** reit, veldu spurningu 00009.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Í **Svaraðu** reit, sláðu inn auðkenni svarraðar svarmöguleikans sem þú vilt gera spurninguna háða. Settu Til dæmis inn 1 fyrir fyrsta svarvalkost.
9. Smelltu á **Vista**.
10. Í trénu, velja ‚Spurningar\ Ég fæ sanngjörn laun fyrir mína vinnu.'.
    * Athugið að spurningatréð var uppfært til að sýna háðar kringumstæður.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
