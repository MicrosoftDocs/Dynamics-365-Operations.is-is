---
title: Flytja fjárhagsáætlanir verks við lok fjárhagsárs
description: Þessi grein veitir upplýsingar um hvernig á að flytja fjárhæðir sem eftir eru til komandi ára og búa til upplýsingar um fjárhagsáætlunarskrá.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172331"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Flytja fjárhagsáætlanir verks við lok fjárhagsárs

[!include [banner](../includes/banner.md)]

Þegar þú vinnur að fjögurra ára verkefni gætirðu haft eftir fjárhagsáætlun í lok reikningsársins. Þú getur flutt eftirstandandi fjárhagsáætlanaupphæðir á ókomið ár og stofnað upplýsingar fjárhagsáætlunarskráar fyrir upphæðir í tengdum fjárhagslyklum. Áður en þú yfirfærir upphæðirnar skaltu fara yfir og greina eftirstandandi upphæðir fjárhagsáætlunar.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Yfirfarið og greinið eftirstandandi fjárhagsáætlunarupphæðir

Ljúkið eftirfarandi skrefum til að fara yfir áætlunarupphæðir ársloka fyrir verk en ekki yfirfæra upphæðirnar.

1. Farðu í **Verkefnisstjórnun og bókhald** > **Reglubundin** > **Fjárhagsáætlanir** > **Fjárhagsáætlanir frá fyrra tímabili**. 
2. Á síðunni **Yfirfærsluferli verkáætlunar**, á flipanum **Valkostir í árslok**, staðfestirðu að **Yfirfæra eftirstöðvar á upphæð áætlunarverks** sé ekki virkt.
3. Á flipanum **Færibreytur**, í reitnum **Fjárhagsáætlunar verks**, velurðu fjárhagsárið sem þú vilt skoða eftirstandandi upphæð fjárhagsáætlunar fyrir. 
4. Í reitnum **Opnunarfjárhagsár** skal velja upphaf fjárhagsárs þar sem skoða á eftirstandandi fjárhagsáætlanaupphæð. 
5. Í reitnum **Frá spálíkani** velurðu **Eftirstöðvar fjárhagsáætlunar**. 
6. Til að fela í sér verk sem uppfylla valin skilyrði og hafa enga eftirstandandi fjárhagsáætlun, velurðu **Birta eftirstöðvar sem núll**.  
7. Á flipanum **Velja fjárhagsáætlanir** velurðu **Sæktu allar fjárhagsáætlanir** til að hlaða öllum fjárhagsáætlunum sem samsvara völdum forsendum og veldu síðan **Ferli**. 
8. Til að hanna fyrirspurn gagnagrunns sem hleður tilteknu safni fjárhagsáætlana í gluggann velurðu **Sækja valdar fjárhagsáætlanir**.

Fyrir frekari upplýsingar um tiltekna línu á glugganum velurðu línuna og síðan **Skoða upplýsingar um fjárhagsáætlun** eða **Skoða reikninga**.

## <a name="carry-forward-remaining-budget-amounts"></a>Yfirfæra eftirstöðvar upphæðar fjárhagsáætlunar 

Þegar unnið er með eftirstandandi áætlunarupphæðir er hægt að stofna færslur í fjárhag fyrir upphæðir sem á að yfirfæra. Til að stofna fjárhagsfærslur skal ljúka skrefunum í hlutanum [Yfirfæra fjárhagsáætlunarfjárhæðir og stofna fjárhagsfærslur](#carry-forward). 

> [!NOTE]
> Fjárhagsáætlunarupphæðir sem eru yfirfærðar eru fluttar á spárlíkanið sem er valið á síðunni **Spárlíkön** sem spárlíkan yfirfærslu.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Yfirfæra fjárhagsáætlunarupphæðir og stofna fjárhagsfærslur

1.  Veldu **Verkefnisstjórnun og bókhald** > **Reglubundin** > **Fjárhagsáætlanir** > **Fjárhagsáætlanir frá fyrra tímabili**. 
2. Á síðunni **Framlag til verkefnaáætlunar** velurðu **Árslok** og virkjar síðan **Yfirfæra eftirstöðvar á upphæð áætlunarverks** og **Stofna færslur fjárhagsáætlunarskrár í fjárhag**. 
3. Á flipanum **Færibreytur**, í reitahópnum **Færibreytur verks** velurðu eftirfarandi:

   - **Fjárhagsáætlunarár verks**: Veldu upphaf fjárhagsárs þar sem skoða á eftirstandandi fjárhagsáætlanaupphæðir. 
   - **Hagnaður og tap**: Stofnaðu hagnaðar - og tapsfærslurnar í fjárhag skal velja gátreitinn. 
   -  **WIP**: Stofna færslur verka í vinnslu (WIP) í fjárhagnum.
   -  **Launaskrá**: Stofna launaskiptingarfærslur í fjárhag skal velja gátreitinn . 

5. Í reitahópnum **Fjárhagur** gefurðu upp eftirfarandi upplýsingar: 

   - Í svæðinu **Opnunarfjárhagsár** skal velja fjárhagsárið sem á að yfirfæra eftirstandandi fjárhagsáætlanaupphæðir á fyrir þessi verk. Sjálfgefið gildi er eitt ár á eftir gildi í reitnum **Fjárhagsáætlunarár verks**.
   -  Í reitnum **Yfirfærslutímabil** er valið tímabilið sem stofna á sundurliðun fjárhagsáætlunarskrár fyrir í fjárhag. Þetta er yfirleitt í fyrsta tímabili opnunarfjárhagsárs.

6. Í reitahópnum **Afrita úr/í** gefurðu upp eftirfarandi upplýsingar:

   - Í reitnum **Úr spárlíkani** skal velja spárlíkan fjárhagsáætlunar verksins sem tengist eftirstandandi fjárhagsáætlanaupphæðum sem á að yfirfæra fyrir verkin. 
   - Í reitnum **Til fjárhagsáætlunarlíkans fjárhags** skal velja fjárhagsáætlunarlíkan verksins sem tengist eftirstandandi fjárhagsáætlanaupphæðum sem á að yfirfæra í fjárhag. 
   -  Veldu **Flytja sölugjaldmiðil** til að nota sölugjaldmiðil verksins fyrir fjárhagsfærslurnar sem eru stofnaðar með því að flytja fjárhagsáætlunarupphæðir fyrir verk skal velja gátreitinn . Þegar valkosturinn er ekki valinn nota færslurnar bókhaldsgjaldmiðilinn. 
   -  Veldu **Birta eftirstöðvar sem núll** til að hafa með verk sem hafa engar eftirstandandi áætlunarupphæðir, en sem uppfylla önnur skilyrði sem valin voru í verkunum sem eru sýndar í neðsta glugganum.

7. Á flipanum **Velja fjárhagsáætlanir** velurðu **Sækja allar fjárhagsáætlanir** til að hlaða öllum fjárhagsáætlunum sem samsvara völdum forsendum. Ef þú vilt frekar hanna fyrirspurn gagnagrunns sem hleður tilteknu safni fjárhagsáætlana verks í gluggann velurðu **Sækja valdar fjárhagsáætlanir**.
8. Fyrir hvert verk sem á að vinna með skal velja valkostinn í upphafi línunnar fyrir verkið.

    > [!TIP]
    > Til að velja öll eða flest verk velurðu hakið efst í efra vinstra horninu. Til að útiloka vinnslu á einhverju verki hreinsarðu gátreitinn fyrir það verk.

9. Til að flytja eftirstandandi fjárhagsáætlanaupphæðir fyrir valin verk á valið fjárhagsár og stofna sundurliðun fjárhagsáætlunarskrár í fjárhag velurðu **Ferli**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Yfirfæra fjárhagsáætlunarupphæðir án þess að stofna fjárhagsfærslur

1. Farðu í **Verkefnisstjórnun og bókhald** > **Reglubundin** > **Fjárhagsáætlanir** > **Fjárhagsáætlanir frá fyrra tímabili**.
2. Á síðunni **Yfirfærsluferli verkáætlunar**, í reitnum **Valkostir í árslok**, velurðu **Yfirfæra eftirstöðvar á upphæð áætlunarverks**.
3. Í hópnum **Færibreytur**, í reitnum **Fjárhagsáætlunar verks**, velurðu fjárhagsárið sem þú vilt skoða eftirstandandi upphæðir fjárhagsáætlunar fyrir.
4. Í hópnum **Afrita úr/í** gefurðu upp eftirfarandi upplýsingar:

   - Í reitnum **Úr spárlíkani** skal velja spárlíkan fjárhagsáætlunar verksins sem tengist eftirstandandi fjárhagsáætlanaupphæðum sem á að yfirfæra fyrir verkin. 
   - Veldu **Birta eftirstöðvar sem núll** til að fela í sér verk sem hafa engar eftirstandandi upphæðir fjárhagsáætlunar sem uppfylla hin skilyrðin sem þú valdir.
   - Í hópnum **Velja fjárhagsáætlanir** velurðu **Sækja allar fjárhagsáætlanir** til að hlaða öllum fjárhagsáætlunum sem samsvara völdum forsendum. Til að hanna fyrirspurn gagnagrunns sem hleður tilteknu safni fjárhagsáætlana verks í gluggann velurðu **Sækja valdar fjárhagsáætlanir**.

5. Fyrir hvert verk sem á að vinna með skal velja valkostinn í upphafi línunnar fyrir verkið. 
6. Veldu **Ferli** til að flytja eftirstandandi fjárhagsáætlanaupphæðir fyrir valin verk á valið fjárhagsár.

