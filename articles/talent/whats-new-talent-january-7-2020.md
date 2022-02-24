---
title: Nýjungar eða breytingar í Dynamics 365 Talent (7. janúar 2020)
description: Þessi grein lýsir nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461526"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a>Nýjungar eða breytingar í Dynamics 365 Talent (7. janúar 2020)

Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Breytingar í Onboard

Þessi útgáfa inniheldur minniháttar villuleiðréttingar fyrir Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Breytingar í Core HR

Breytingum sem lýst er í þessum kafla gilda um byggingarnúmer 8.1.2697. Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Microsoft Dynamics Lifecycle Services (LCS).

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a>Get ekki eytt starfsmönnum sem eru ekki með atvinnuskrá - (386157)

Þessi breyting bætir við eyðingarvalkosti í **Starfsmenn án atvinnu** form. Starfsmenn birtast á þessu formi þegar engin framtíð, virk eða söguleg ráðning er fyrir hendi fyrir starfsmanninn. Í þessari útgáfu er eyða aðeins virkt fyrir kerfisstjóra. Í útgáfu næstu viku verður öryggi hins vegar uppfært svo að allir notendur sem hafa aðstoðarmannahlutverk HR geti fjarlægt starfsmenn án atvinnu. Þú getur einnig gert þessar breytingar handvirkt með því að fylgja eftirfarandi skrefum.

1. Farðu í **Öryggisskilgreining**.
2. Á flipanum **Réttindi** síaðu listann **Réttindi** á **Viðhalda starfsmönnum**.
3. Í dálkinum **Tilvísanir** veldu **Birta valmyndaratriðin**.
4. Í **Yfirlitsvalmyndaratriði** velurðu **HcmWOrkersWithoutEmployment**.
5. Stilltu **Eyða** leyfi til að veita.
6. Veldu flipann **Óbirtir hlutir**.
7. Velja **Birta allt**.
