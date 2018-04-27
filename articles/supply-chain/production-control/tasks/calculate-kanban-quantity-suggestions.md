--- 
title: "Reikna út tillögur um kanban-magn"
description: "Þetta ferli leggur áherslu á besta kanban-stærð og magn fyrir tiltekna kanban-reglu með því að nota útreikning kanban-magns."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a817dbc02890d863f68c5bf2a6cc11b9a5328060
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="calculate-kanban-quantity-suggestions"></a>Reikna út tillögur um kanban-magn

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli leggur áherslu á besta kanban-stærð og magn fyrir tiltekna kanban-reglu með því að nota útreikning kanban-magns. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta ferli er ætlað fyrir virðisstraumsstjóra. Það er frumskilyrði að þú hafir lokið ferli Bæta nýja útreikningsstefnu kanban-magns á kanban-reglu.


## <a name="create-a-kanban-quantity-calculation"></a>Stofna útreikning fyrir kanban-magn
1. Fara í Framleiðslustýringar > Reglubundin verkefni > Útreikningur kanban-magns > Útreikningsreglur kanban-magns.
2. Smellið á „Nýtt“.
3. Í svæðið Heiti, færðu inn 'Speaker2016'.
4. Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.
    * Veljið regluna sem þú hefur stofnað í ferlinu Bæta til nýja útreikningsstefnu kanban-magns á kanban-reglu. Til dæmis Speaker2016.  
5. Í listanum skal smella á tengilinn í valinni línu.
6. Í svæðið Regla virk frá og með dagsetningu, setja dagsetningu og tíma í '2012-12-17T08:00:00'.
    * Þessi dagsetning virkar sem grundvöllur fyrir því að ákvarða hvaða fasta kanban-reglur eru hafðar með í útreikningur kanban-magns.  
7. Í upphafsdagsetningarsvæðið Uppfyllt eftirspurn tímabils, setja dagsetningu og tíma í ' 2012-11-17T09:00:00'.
    * Frá og með þessari dagsetningu eru liðnar eftirspurnarfærslur hafðar með í útreikningi kanban-magns.  
8. Í lokadagsetningarsvæðið Uppfyllt eftirspurn tímabils, setja dagsetningu og tíma í ' 2012-12-17T07:59:59'.
    * Til og með þessari dagsetningu eru liðnar eftirspurnarfærslur hafðar með í útreikningi kanban-magns.  
9. Í upphafsdagsetningarsvæðið eftirspurnartímabil, setja dagsetningu og tíma í ' 2012-12-17T08:00:00'.
    * Frá og með þessari dagsetningu eru núgildandi eftirspurnarfærslur hafðar með í útreikningi kanban-magns.  
10. Í lokadagsetningarsvæðið eftirspurnartímabil, setja dagsetningu og tíma í ' 2013-01-16T07:59:59'.
    * Til og með þessari dagsetningu eru núgildandi eftirspurnarfærslur hafðar með í útreikningi kanban-magns.  

## <a name="generate-kanban-quantity-proposal"></a>Stofna Tillaga um kanban-magn.
1. Smellið á „Vista“.
2. Smellt er á Mynda.
    * Þetta myndar tillögulína kanban-magns fyrir kanban-reglu 000020.  

## <a name="run-kanban-quantity-calculation"></a>Keyra útreikning fyrir kanban-magn
1. Smellt er á að reikna Út.
    * þetta reiknar Tillaga um kanban-magn.  
2. Smellið á „Í lagi“.
3. Í listanum skal merkja valda línu.
    * Athugið ráðlagt kanban-magn er 2.  

## <a name="change-product-quantity-and-calculate-again"></a>Breyta magni afurðar og reikna aftur
1. Setja afurðarmagn á "5".
2. Smellt er á að reikna Út.
3. Smellið á „Í lagi“.
    * Athugið með kanban-magn 5 er tillaga breytt í kanban-magn 4.  
    * Þetta er vegna þeirrar staðreyndar að með lægra magn afurðar þurfum við fleiri kanban til að uppfylla eftirspurnina.  

## <a name="update-kanban-rule"></a>Uppfæra kanban-reglu
1. Í reitnum dagsetning regluvirkni skal færa inn dagsetningu og tíma.
    * Stilltu ‚Regla er virk frá og með dagsetningu' á dagsetningu í framtíðinni. Til dæmis í dag + eitt ár.  
2. Smelltu á Uppfæra.
3. Smellið á „Í lagi“.
4. Lokið síðunni.

## <a name="validate-change-on-kanban-rule"></a>Villuleita breytingu á kanban-reglu
1. Farið í upplýsingar um afurðarstjórnun > Lean-framleiðsla > Kanban-reglur.
2. Í listanum skal smella á tengilinn í valinni línu.
    * Velja kanban-reglu sem var stofnuð í fyrri undirverki. Þetta ætti að vera fyrsta kanban-reglu af listanum er raðað eftir númeri.  
3. Víxla útvíkkun á liðnum upplýsingar.
    * Athugið gildisdagsetning, sem þýðir að þessi regla er ekki virk til þessarar dagsetningar.  
4. Víxla útvíkkun á liðnum magn.
    * Athugið að þetta er sjálfgefið magn sem fært var inn í útreikningi kanban-magns.  
    * Athugið að þetta er fast kanban-magn 4 úr útreikningi kanban-magns.  
5. Smellt er á flipann ListPanel.


