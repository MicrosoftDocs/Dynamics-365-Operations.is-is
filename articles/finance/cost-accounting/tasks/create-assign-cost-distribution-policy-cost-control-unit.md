---
title: Stofna og úthluta kostnaðardreifingarreglu fyrir kostnaðarstýringareiningu
description: Kostnaðardreifingarreglur eru notaðar til að dreifa kostnaði sem hefur verið fjárhagslega talinn á sameiginlegum kostnaðarstað.
author: kfend
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.search.form: CAMCostDistributionRule
ms.openlocfilehash: 23adea279cad3fcf69cc6926d6f8dee485150221
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272399"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a>Stofna og úthluta kostnaðardreifingarreglu fyrir kostnaðarstýringareiningu

[!include [banner](../../includes/banner.md)]

Kostnaðardreifingarreglur eru notaðar til að dreifa kostnaði sem hefur verið fjárhagslega talinn á sameiginlegum kostnaðarstað. Endurskoðandi kostnaðar gengur úr skugga um að kostnaði sé dreift til kostnaðarstaða, út frá völdum úthlutunargrunni. Stefna og samsvarandi reglur er úthlutað til kostnaðarstýringareiningar. Þessar verkefnaleiðbeiningar nota dæmi til að sýna hvernig skal stofna kostnaðardreifingarstefnu og samsvarandi reglur.


## <a name="create-a-policy"></a>Stofna Stefnu
1. Fara í Kostnaðarbókhald > Stefnur > Stefnur fyrir kostnaðardreifingu.
2. Smellið á „Nýtt“.
3. Sláið inn gildi í reitinn Stefnuheiti.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðarhlutar.
    * Velja Fyrirtæki  
6. Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðareiningar.
    * Velja CDS P/L.  
7. Sláið inn eða veljið gildi í reitnum Tölfræðileg vídd.
    * Velja skal Tölfræðilegar einingar.  
8. Smellið á „Vista“.

## <a name="create-rules-for-the-policy"></a>Stofna reglur fyrir stefnuna
1. Smellið á „Nýtt“.
2. Í listanum skal merkja valda línu.
3. Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.
    * Útvíkka stigveldið til að velja 094.  
4. Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðareiningar.
    * Velja Annar rekstrarkostnaður og veljið síðan 605110 Hreinsun.  
5. Veljið valkost í svæðinu Kostnaðarhegðun.
    * Velja Fastur kostnaður.  
6. Sláið inn eða veldu gildi í Úthlutunargrunnur reitnum.
7. Smellið á „Nýtt“.
8. Í listanum skal merkja valda línu.
9. Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.
    * Útvíkka stigveldið til að velja 094.  
10. Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðareiningar.
    * Velja Annar rekstrarkostnaður og veljið síðan 605150 Leiga.  
11. Veljið valkost í svæðinu Kostnaðarhegðun.
    * Velja Fastur kostnaður.  
12. Sláið inn eða veldu gildi í Úthlutunargrunnur reitnum.
13. Smellið á „Vista“.

## <a name="assign-rules-to-a-cost-control-unit"></a>Úthluta reglum til kostnaðarstýringareiningar
1. Smella á Regluúthlutanir fyrir kostnaðarstýringareiningu.
2. Smellið á „Nýtt“.
3. Í listanum skal merkja valda línu.
4. Færa skal inn dagsetningu í reitinn Gildir frá dagsetningu reikningsskila.
    * Velja 1. september í gildu fjárhagsárinu.  
5. Í reitinn Kostnaðarstýringareining skal slá inn eða velja gildi.
6. Smellið á „Vista“.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
