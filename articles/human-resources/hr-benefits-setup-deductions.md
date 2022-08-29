---
title: Grunnstilla frádrætti
description: Notaðu frádrátt í Microsoft Dynamics 365 Human Resources til að ákvarða hve mikið, ef einhver er, til að draga frá launaávísun starfsmanns fyrir hverja bætur.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 46a37aebf99751d16952d3d7c07c538713377a67
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324874"
---
# <a name="configure-deductions"></a>Grunnstilla frádrætti


Notaðu frádrátt í Microsoft Dynamics 365 Human Resources til að ákvarða hve mikið, ef einhver er, til að draga frá launaávísun starfsmanns fyrir hverja bætur. Frádráttur er gildandi frá dagsetningunni, svo þú getur haldið sögulega skrá yfir frádráttarupplýsingar. 

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Frádráttur**.

2. Veljið **Nýtt**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Frádráttur** | Sérstakt auðkenni sem er notað til að bera kennsl á fríðindafrádráttinn. |
   | **Lýsing** | Lýsing á frádrætti. |
   | **Virkt** | Upphafsdagsetningin. Sjálfgefið gildi er núverandi kerfisdagsetning. |
   | **Lok gildistíma** | Lokadagsetningin. Sjálfgefið gildi er 12/31/2154, sem táknar aldrei. |
   | **Fyrirsögn** | Fyrirsagnarkóði frá launakerfi sem þessi frádráttur mun nota fyrir starfsmannahluta frádráttarins við vinnslu bóta á launaskrá. Þetta er notað þegar þú notar þriðja aðila launaskrá. |
   | **Tilvísun starfsmanns í launafrádrátt** | Kóðinn úr launakerfinu sem frádrátturinn notar fyrir hluta starfsmannsins eða atvinnuveitandans af frádrættinum þegar fríðindi eru reiknuð út miðað við laun. |
   | **Fyrirsögn upphæðar** | Fyrirsagnarkóði frá launakerfi sem þessi frádráttarupphæð mun nota fyrir starfsmannahluta frádráttarins við vinnslu bóta á launaskrá. Þetta er venjulega notað þegar þú notar þriðja aðila launaskrá. |
   | **Má eyða** | Tilgreinir hvort útflutt gildi úr Dynamics 365 Finance geti valdið því að gildinu sé eytt í launakerfinu. |
   | **Paraðir dálkar** | Tilgreinir hvort flytja eigi fyrirsögn og frádráttarupphæð í pöruðum aðliggjandi dálkum til launakerfisins. |
   | **Breyta gildisdegi** | Dagsetningin þegar frádráttarbreyting fríðinda verður virk. Á þessari dagsetningu breytist frádráttur fríðinda og allar fríðindaáætlanir sem tengjast þessum frádrætti eru uppfærðar svo lengi sem úrvinnslan **Uppfærsla frádráttarbreytingar** er keyrð. |
   | **Lokið er við að gera breytingar á frádrætti** | Gátreiturinn **Frádráttarbreytingum lokið** verður sjálfkrafa valinn þegar breytingum á frádrætti bótagreiðslna hefur verið lokið með frávinnslu breytinga á frádrátti. |
   
4. Veldu til að fylgjast með og viðhalda breytingum á uppbótarhlutfalli **Aðgerðir** og veldu síðan **Viðhalda útgáfum**.

5. Veljið **Vista**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

