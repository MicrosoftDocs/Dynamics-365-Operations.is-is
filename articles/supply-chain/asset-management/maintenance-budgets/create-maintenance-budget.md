---
title: Stofna fjárhagsáætlanir viðhalds
description: Þetta efni útskýrir hvernig á að stofna fjárhagsáætlun viðhalds í eignastjórnun.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a375eb7c208479615b2d5e7cf78168ffd7ac8b16c52c85a7ef5a41aa69c947d5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776945"
---
# <a name="create-maintenance-budgets"></a>Stofna fjárhagsáætlanir viðhalds

[!include [banner](../../includes/banner.md)]

 



Fjárhagsáætlanir viðhalds eru notaðar til að veita yfirsýn yfir væntanlegan kostnað vegna fyrirbyggjandi viðhalds. Fjárhagsáætlunarlínur eru reiknaðar út frá viðhaldsáætlunarlínum sem hafa áætlaðan upphafsdag á fjárhagsáætlunartímabilinu.

Fjárhagsáætlanir viðhalds eru byggðar á kostnaðargerðum sem notaðar eru í eignastýringu: **Fyrirbyggjandi**, **Leiðréttandi** og **Fjárfesting**. Fjárhagsáætlunarkostnaður vegna viðhalds fjárfestinga er innifalinn fyrir virkar eignir sem eiga sér endurnýjunardagsetningu á fjárhagsáætlunartímabilinu og tilheyrandi endurnýjunargildi. Kostnaður áætlunar vegna viðgerða er innifalinn ef fyrri leiðréttingardagur er innifalinn í útreikningi fjárhagsáætlunar. Í því tilfelli er leiðréttingarkostnaður frá fyrra tímabili reiknaður fyrir sama framtíðartímabil og þú reiknar út viðhaldsáætlun fyrir.

## <a name="create-a-maintenance-budget"></a>Stofna fjárhagsáætlun viðhalds

1. Veldu **Eignastýring** \> **Fyrirspurnir** \> **Viðhaldsáætlun** \> **Fjárhagsáætlun**.
2. Veldu **Stofna fjárhagsáætlun**.
3. Í reitinn **Viðhaldsáætlun** skal slá inn kenni fjárhagsáætlunar.
4. Í reitnum **Lýsing** skal færa inn lýsingu.
4. Á flýtiflipanum **Tímabil**, í reitunum **Frá dagsetningu** og **Til dagsetningar**, skal slá inn upphafs- og lokadagsetningar fjárhagsáætlunartímabilsins.
5. Til að fela í sér leiðréttandi kostnað við fjárhagsáætlun sem er reiknaður út á grundvelli raunkostnaðar frá fyrra tímabili skal slá inn upphafsdagsetningu tímabilsins sem þessi kostnaður ætti að vera með frá í reitinn **Leiðrétting frá dagsetningu**.
6. Eftir því hvaða upplýsingastigs er krafist í fjárhagsáætluninni skal stilla viðeigandi valkosti á hinum fimm flýtiflipum **Flokka eftir**.
7. Veljið **Í lagi**.
8. Veldu **Fjárhagsáætlunarlínur** til að opna síðuna **Fjárhagsáætlunarlínur viðhalds** þar sem þú getur skoðað allar fjárhagsáætlunarlínur sem hafa verið búnar til á tímabilinu.
9. Til að samþykkja fjárhagsáætlunina skaltu velja hana á síðunni **Fjárhagsáætlanir viðhalds** og velja síðan **Samþykkja**. Síðan, í valmyndinni **Samþykkja fjárhagsáætlun** skaltu velja **Í lagi**. Nafn þitt er slegið inn í reitinn **Samþykkt af** á síðunni **Fjárhagsáætlanir viðhalds**.

    > [!NOTE]
    > Þegar þú hefur samþykkt fjárhagsáætlun viðhalds geturðu ekki endurútreiknað eða aðlagað tengdar línur á síðunni **Fjárhagsáætlunarlínur viðhalds** nema að þú fjarlægir samþykkið fyrst. Til að fjarlægja samþykki á fjárhagsáætlun viðhalds skaltu velja hana á síðunni **Fjárhagsáætlanir viðhalds** og velja síðan **Samþykkja**. Síðan, í valmyndinni **Samþykkja fjárhagsáætlun** skaltu velja **Í lagi**.

![Fjárhagsáætlanir viðhalds.](media/01-maintenance-budgets.png)

Einnig er hægt að stofna nýja fjárhagsáætlun viðhalds með því að afrita fyrirliggjandi fjárhagsáætlun. Á síðunni **Fjárhagsáætlanir viðhalds** velurðu fjárhagsáætlun til að afrita og síðan **Afrita**. Þessi aðferð er gagnleg ef þú hefur til dæmis búið til fjárhagsáætlun í einn mánuð og vilt afrita hana á aðra mánuði.

> [!NOTE]
> Viðhaldsfjárhagsáætlunin reiknar aðeins kostnaðaráætlun fjárhagsáætlunar út frá fjárhagsáætlunarlínum viðhalds. Til að reikna út raunkostnað fyrir sama tímabil er hægt að gera þann útreikning á síðunni **Stýring eignakostnaðar**. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]