---
title: "Bæta fjárhagsvíddum við CFO vinnusvæðið"
description: "Þetta efnisatriði útskýrir hvernig skal bæta fjárhagsvíddum við CFO vinnusvæðið, svo hægt sé að nota þær fyrir fjárhags- og fjárhagáætlunarskýrslurnar."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9e674948f642ab7525f96092a9a1f3adaae66974
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>Bæta fjárhagsvíddum við CFO vinnusvæðið

[!include[banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig skal bæta fjárhagsvíddum við Fjármálastjóra (CFO) vinnusvæðið, svo hægt sé að nota þær fyrir fjárhags- og fjárhagáætlunarskýrslurnar. CFO vinnusvæðið er með **Yfirlit** flipa og **Fjármála** flipa. Skýrslurnar á þessum tveimur flipum eru studdar með tveimur mælingum: LedgerActivityMeasure and BudgetActivityMeasure. Í júlí 2017 uppfærslunni af Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition er tenging á milli þessara tveggja mælinga og DimensionCombinationEntity einingarinnar. Þar af leiðandi geturðu valið víddir.

1. Í Finance and Operations, á **Eining verslun** síðunni skal uppfæra **LedgerActivityMeasure** og **BudgetActivityMeasure** mælingarnar.
2. Í Microsoft Visual Studio skal opna Application Explorer og leita að **LedgerCFO**.
3. Undir **Forði** skal opna **LedgerCFOWorkspacePBIX**.
4. Þegar forðinn opnast í Microsoft Power BI skjáborð, skal velja **Sækja gögn**, velja **SQL Server gagnagrunnur**, og velja svo **Tengja**.
5. Færa inn heiti þjóns og færa inn **AxDW** sem gagnagrunninn. Velja skal **DirectQuery** og svo **Í lagi**.
6. Leita að og velja **LedgerActivityMeasure\_DimensionCombination** og velja svo **Hlaða**.

    > [!TIP]
    > Í listanum **Reitir** skal endurnefna töfluna **Fjármálavíddir** svo það sé auðvelt að finna hana.

7. Smellið á **Stjórna venslum** og veljið síðan **Nýtt**.
8. Í fyrsta reitnum skal velja **Fjárhagsvirkni** og velja svo **Fjárhagsvídd**.
9. Í öðrum reitnum skal velja **LedgerActivityMeasure\_DimensionCombination** (eða **Fjármálavíddir** ef þú endurnefndir töfluna). Velja **DimensionCombinationRECID** hausinn.
10. Í reitnum **Línufjöldi** skal velja **Margar til ein**.
11. Breyta **Þverlæg afmörkun leið** gildinu í **Stakur**.
12. Velja bæði **Virkja þessi vensl** og **Gera ráð fyrir tilvísandi áreiðanleika**, veljið **Í lagi** og veljið síðan **Loka**.

    [![Stofna vensl](./media/Create-relationship.png)](./media/Create-relationship.png)

13. Í listanum **Reitir** ættirðu að sjá töfluna og tiltækar fjármálavíddir. Dragðu fjárhagsvíddirnar sem þú vilt yfir í skýrsla-stig afmarkanirnar.
14. Vista breytingarnar.
15. Í Hugbúnaðarhlutatrénu (AOT) skal hægri-smella á þitt verkefni og velja síðan **Samstilla**.
16. Smíðaðu þitt verkefni og opnaðu svo forritið til að skoða niðurstöðurnar.

    [![Vinnusvæði lokið](./media/workspace.png)](./media/workspace.png)
