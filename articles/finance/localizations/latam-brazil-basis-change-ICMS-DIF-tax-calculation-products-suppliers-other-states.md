---
title: Grunnbreyting á ICMS-DIF skattaútreikningum fyrir vörur frá birgjum í öðrum ríkjum
description: Þetta efnisatriði lýsir uppsetningu fyrir útreikninga á skattategundinni ICMS-DIF þegar skattskjal er móttekið í Brasilíska fylkinu Rio Grande do Sul (RS) eða São Paulo (SP).
author: Kai-Cloud
ms.date: 1/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 16f78b85567e6d08c588e621119513ff070bf618
ms.sourcegitcommit: 68655c5673aef9892063e5913ffee6bfc3817387
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/21/2022
ms.locfileid: "8016146"
---
# <a name="basis-change-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Grunnbreyting á ICMS-DIF skattaútreikningum fyrir vörur frá birgjum í öðrum ríkjum

Þetta efni lýsir uppsetningu fyrir útreikninga á **ICMS-DIF** skattategund þegar skattskjal er móttekið í brasilíska fylkinu Rio Grande do Sul (RS) eða São Paulo (SP).

Samkvæmt skilgreiningunni í ríkislögunum verður Imposto sobre Circulação de Mercadorias e Serviços (ICMS) sem safnað er að fylgja þessari reglu:

*ICMS til að safna* = ([(*Aðgerðarupphæð* –*ICMS frá uppruna*) ÷ (1 –*ICMS % innri*)] ×*ICMS % innri*) -*ICMS upphæð frá uppruna*

## <a name="example"></a>Dæmi

Brasilískt fyrirtæki í RS-ríkinu fær fjárhagsskjal fyrir kaup frá söluaðila í SP-ríkinu. Fyrirtækið verður að innheimta prósentumismun ICMS milli RS-ríkis (18 prósent) og SP-ríkis (12 prósent). Hins vegar ber að reikna grunninn samkvæmt fyrri reglu.

- **Upphæð aðgerða:** 1.000,00 brasilískir raunir (1.000,00 R$)
- **ICMS milliríki:** R$ 120.00
- **ICMS hlutfall í RS ríkinu:** 18 prósent
- **ICMS til að safna í RS ríkinu:** (\[ (1.000 – 120) ÷ (1 – 0,18)\] × 0,18) – 120 = R$ 73,17 

## <a name="resolution"></a>Upplausn

Til að reikna út mismunadrifið ICMS (ICMS-DIF) samkvæmt reglum RS-ríkisins, verður þú að setja upp VSK-kóða og VSK-flokk á eftirfarandi hátt:

1. Búðu til söluskattskóða til að fá 12 prósenta ICMS (fyrir hitt ríkið). Þessi kóði er notaður til að skrá skattkröfur frá seljanda.
2. Búðu til söluskattskóða til að safna ICMS-DIF. Þessi söluskattskóði ætti að hafa prósentuupphæð 18 prósent (fyrir þitt eigið ríki) til að skilgreina muninn á milli 18 prósent og 12 prósent. Stilltu skatttegundina á **ICMS-DIF**. Þessi virðisaukaskattskóði verður að vera skilgreindur á eftirfarandi hátt í útreikningsbreytum:

    - Í **Uppruni** reit, veldu **Hlutfall af brúttófjárhæð**.
    - Í **Jaðargrunnur** reit, veldu **Nettóupphæð á línu** eða **Nettóupphæð reikningsstöðu**.
    - Skilgreindu skattlagningarkóðann þannig að hann hafi fjárhagslegt gildi sem **3**. Á þennan hátt verður leiðréttingarfærslan sjálfkrafa búin til þegar **Fjárhagsbækur** eining er virkjuð.
    - Í uppsetningu söluskattshópsins, veldu **Notaðu skatt** valkostur fyrir **ICMS-DIF** söluskattskóða.
