---
title: Grunnstilla frádrætti
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009432"
---
# <a name="configure-deductions"></a>Grunnstilla frádrætti

[!include [banner](includes/preview-feature.md)]

Notaðu frádrátt í Microsoft Dynamics 365 Human Resources til að ákvarða hve mikið, ef einhver er, til að draga frá launaávísun starfsmanns fyrir hverja bætur. Frádráttur er gildandi frá dagsetningunni, svo þú getur haldið sögulega skrá yfir frádráttarupplýsingar. 

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Frádráttur**.

2. Veljið **Nýtt**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | Frádráttur | Sérstakt auðkenni sem er notað til að bera kennsl á fríðindafrádráttinn. |
   | Lýsing | Lýsing á frádrætti. |
   | Virkt | Upphafsdagsetningin. Sjálfgefið gildi er núverandi kerfisdagsetning. |
   | Lok gildistíma | Lokadagsetningin. Sjálfgefið gildi er 12/31/2154, sem táknar aldrei. |
   | Fyrirsögn | Fyrirsagnarkóði frá launakerfi sem þessi frádráttur mun nota fyrir starfsmannahluta frádráttarins við vinnslu bóta á launaskrá. Þetta er notað þegar þú notar þriðja aðila launaskrá. |
   | Tilvísun starfsmanns í launafrádrátt | Kóðinn úr launakerfinu sem frádrátturinn notar fyrir hluta starfsmannsins eða atvinnuveitandans af frádrættinum þegar fríðindi eru reiknuð út miðað við laun. |
   | Fyrirsögn upphæðar | Fyrirsagnarkóði frá launakerfi sem þessi frádráttarupphæð mun nota fyrir starfsmannahluta frádráttarins við vinnslu bóta á launaskrá. Þetta er venjulega notað þegar þú notar þriðja aðila launaskrá. |
   | Má eyða | Tilgreinir hvort flutt gildi frá Dynamics 365 for Finance and Operations getur valdið því að gildinu er eytt í launakerfinu. |
   | Paraðir dálkar | Tilgreinir hvort flytja eigi fyrirsögn og frádráttarupphæð í pöruðum aðliggjandi dálkum til launakerfisins. |
   | Breyta gildisdegi | Dagsetningin þegar frádráttarbreyting fríðinda verður virk. Á þessum degi mun kerfið sjálfkrafa breyta frítekjumarkinu og uppfæra allar fríðindaáætlanir sem fylgja þessu frádrætti, svo framarlega sem þú keyrir vinnslu frádráttaruppfærsluskipta. |
   | Lokið er við að gera breytingar á frádrætti | Gátreiturinn frá frádráttarbreytingum lokið verður sjálfkrafa valinn þegar breytingum á frádrætti bótagreiðslna hefur verið lokið með frávinnslu breytinga á frádrátti. |
   
4. Veldu til að fylgjast með og viðhalda breytingum á uppbótarhlutfalli **Aðgerðir** og veldu síðan **Viðhalda útgáfum**.

5. Veljið **Vista**. 
