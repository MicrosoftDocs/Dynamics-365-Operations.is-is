---
title: Stofna notkunarskýrslur
description: Þetta efni útskýrir hvernig á að stofna notkunarskýrslur í eignastjórnun.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d28acbccc35b3f59f9cca7236dd721a1d9bdead8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430449"
---
# <a name="create-consumption-reports"></a>Stofna notkunarskýrslur

[!include [banner](../../includes/banner.md)]

 

Þegar þú hefur búið til og sent notkunarskráningar í verkbeiðnum í eignastýringu eru tvær skýrslur tiltækar til að birta notkunarupplýsingar.


## <a name="asset-consumption-report"></a>Eignanotkunarskýrsla

Þegar þú hefur bókað notkun á verkbeiðnir geturðu prentað eignanotkunarskýrslu. Skýrslan sýnir klukkustundir, tímakostnað, vörukostnað og útgjöld sem er bókaður á eignir.

1. Smelltu á **Eignastýringu** > **Skýrslur** > **Eignir** > **Eignanotkun**.

2. Í glugganum **Eignanotkun** velurðu færibreytu- og upplýsingastig sem þú vilt sjá með því að velja **Já** á viðeigandi skiptihnöppum og setja inn virkt staðsetningarstig í kaflanum **Sýna**.
    - Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að eignalínur séu varðandi virkar staðsetningar. 
    
        Til dæmis, ef þú setur inn töluna „1“ í reitinn, og þú ert með fjölþrepa skipulag virkra staðsetninga, verða allar eignir fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að bæta línu við af virkum staðsetningum sem eru staðsettar á lægra stigi. 
        
        Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar eignalínur á öllum virkum staðsetningarstigum sem þær tengjast. 
        
    - Veldu **Já** á skiptihnappnum **Summa á öllum undireignum** til að sjá fjárhæðir fyrir hverja undireign í skýrslunni.

3. Veldu dagsetningartíma í kaflanum **Dagsetningar**.

4. Á flýtiflipanum **Áfangastaður** skaltu velja hvort þú vilt birta skýrsluna á skjánum, prenta hana eða vista hana sem skrá eða tölvupóst.

5. Ef þess er krafist geturðu valið sérstakar eignir sem birtast í skýrslunni. Á flýtiflipanum **Færslur til að hafa með** smellirðu á **Sía** og bætir við eignunum sem þú vilt hafa með í skýrslunni.

6. Smellið á **Í lagi** til að stofna skýrsluna.


## <a name="work-order-consumption-report"></a>Notkunarskýrsla verkbeiðni

Þegar þú hefur bókað notkun á verkbeiðnir geturðu prentað notkunarskýrslu verkbeiðni. Skýrslan sýnir klukkustundir, tímakostnað, vörukostnað og útgjöld sem er bókaður á verkbeiðnir.

1. Smelltu á **Eignastýring** > **Skýrslur** > **Verkbeiðnir** > **Notkun verkbeiðni**.

2. Í glugganum **Notkun verkbeiðni** velurðu þær færibreytur sem þú vilt láta fylgja með í skýrslunni með því að velja **Já** á viðeigandi skiptihnöppum í kaflanum **Sýna**.

3. Veldu dagsetningartíma í kaflanum **Dagsetningar**.

4. Á flýtiflipanum **Áfangastaður** skaltu velja hvort þú vilt birta skýrsluna á skjánum, prenta hana eða vista hana sem skrá eða tölvupóst.

5. Ef þess er krafist geturðu valið sérstakar verkbeiðnir sem birtast í skýrslunni. Á flýtiflipanum **Færslur til að hafa með** smellirðu á **Sía** og bætir við verkbeiðnunum sem þú vilt hafa með í skýrslunni.

6. Smellið á **Í lagi** til að stofna skýrsluna.


>[!NOTE]
>Þú getur líka búið til [verkbeiðnaskýrslu](../work-orders/work-order-report.md), sem inniheldur fleiri upplýsingar um verkbeiðni.

