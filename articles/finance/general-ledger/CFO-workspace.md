---
title: Bæta fjárhagsvíddum við CFO vinnusvæðið
description: Þessi grein útskýrir hvernig skal bæta fjárhagsvíddum við CFO vinnusvæðið, svo hægt sé að nota þær fyrir fjárhags- og fjárhagáætlunarskýrslurnar.
author: aprilolson
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ea453eed826dec2e97371ec559e91b94933bdce6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853381"
---
# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>Bæta fjárhagsvíddum við CFO vinnusvæðið

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig skal bæta fjárhagsvíddum við Fjármálastjóra (CFO) vinnusvæðið, svo hægt sé að nota þær fyrir fjárhags- og fjárhagáætlunarskýrslurnar. CFO vinnusvæðið er með **Yfirlit** flipa og **Fjármála** flipa. Skýrslurnar á þessum tveimur flipum eru studdar með tveimur mælingum: LedgerActivityMeasure and BudgetActivityMeasure. Það er tenging á milli þessara tveggja mælinga og DimensionCombinationEntity einingarinnar. Þar af leiðandi geturðu valið víddir.

1. Í Finance, á síðunni **Einingaverslun** skal uppfæra **LedgerActivityMeasure** og **BudgetActivityMeasure** mælingarnar.
2. Í Microsoft Visual Studio skal opna Application Explorer og leita að **FjárhagurCFO**.
3. Undir **Forði** skal opna **LedgerCFOWorkspacePBIX**.
4. Þegar forðinn opnast í Microsoft Power BI Desktop, skal velja **Sækja gögn**, velja **SQL þjónn gagnagrunnur**, og velja svo **Tengja**.
5. Færa inn heiti þjóns og færa inn **AxDW** sem gagnagrunninn. Velja skal **DirectQuery** og svo **Í lagi**.
6. Leita að og velja **LedgerActivityMeasure\_DimensionCombination** og velja svo **Hlaða**.

    > [!TIP]
    > Í listanum **Reitir** skal endurnefna töfluna **Fjármálavíddir** svo það sé auðvelt að finna hana.

7. Smellið á **Stjórna venslum** og veljið síðan **Nýtt**.
8. Í fyrsta reitnum skal velja **Fjárhagsvirkni** og velja svo **Fjárhagsvídd**.
9. Í öðrum reitnum skal velja **LedgerActivityMeasure\_DimensionCombination** (eða **Fjármálavíddir** ef þú endurnefndir töfluna). Veldu hausinn  **DimensionCombinationRECID**.
10. Í reitnum **Línufjöldi** skal velja **Margar til ein**.
11. Breyta **Þverlæg afmörkun leið** gildinu í **Stakur**.
12. Velja bæði **Virkja þessi vensl** og **Gera ráð fyrir tilvísandi áreiðanleika**, veljið **Í lagi** og veljið síðan **Loka**.

    [![Stofna vensl.](./media/Create-relationship.png)](./media/Create-relationship.png)

13. Í listanum **Reitir** ættirðu að sjá töfluna og tiltækar fjármálavíddir. Dragðu fjárhagsvíddirnar sem þú vilt yfir í skýrsla-stig afmarkanirnar.
14. Vista breytingarnar.
15. Í Hugbúnaðarhlutatrénu (AOT) skal hægri-smella á þitt verkefni og velja síðan **Samstilla**.
16. Smíðaðu þitt verkefni og opnaðu svo forritið til að skoða niðurstöðurnar.

    [![Vinnusvæði lokið.](./media/workspace.png)](./media/workspace.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
