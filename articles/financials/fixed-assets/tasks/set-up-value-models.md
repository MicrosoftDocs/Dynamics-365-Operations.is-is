---
title: Setja upp virðislíkön
description: Þessi ferli sýnir hvernig á að stofna nýtt eignabók og tengja hana við eignaflokk.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e067173b27488422fd05ad45f37528f00f04a2bd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571651"
---
# <a name="set-up-value-models"></a>Setja upp virðislíkön

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi ferli sýnir hvernig á að stofna nýtt eignabók og tengja hana við eignaflokk. Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.


## <a name="create-a-book"></a>Búa til bók
1. Fara í Eignir > Uppsetning > Bækur.
2. Smellið á „Nýtt“.
3. Í reitinn Bók skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
    * Þegar Reikna afskrift er valin verða tengdar bækur eigna teknar með í afskriftartillögur. Ef hann er ekki valinn verða bókin ekki sjálfkrafa afskrifa.  
5. Velja skal Já í Reikna út afskriftir reitnum.
6. Sláið inn eða veldu gildi í reitnum Afskriftarregla.
    * Önnur afskriftarregla er einnig þekkt sem umskiptingaraðferð afskriftar. Afskriftatillögu verður skipta yfir í þessa forstillingu þegar önnur forstilling reiknar afskriftarupphæð sem er jöfn eða meiri en sjálfgefinn afskriftareglu.  
    * Óregluleg afskriftaregla er notuð fyrir aukalega afskrift af eign við óvenjulegar aðstæður. Til dæmis er hægt að nota þetta til að skrá niðurstöður úr náttúruhamfarir afskrift.  
    * Ef Stofna afskriftaleiðréttingar með grunnleiðréttingum er valinn, afskriftaleiðréttingar sjálfkrafa stofnuð þegar virði eignar er uppfærður. Ef það er ekki valinn er mun uppfært virði eignarinnar aðeins hafa áhrif á afskriftaútreikninga fram á við.  
7. Veldu Já í reitnum Stofna afskriftaleiðréttingar með grunnleiðréttingum
    * Að sjálfgefnu eru færslur eignabókar bókaðar í fjárhag. Hægt er að gera bókun í fjárhag fyrir bók óvirka með því að stilla reitinn Bóka í fjárhag á nei. Bækur sem bóka ekki í fjárhag eru vanalega notaðar fyrir skattskýrslugerð. Þetta gefur viðbótar sveigjanleika til að eyða sögulegum færslum fyrir eignabók þar sem þær hafa ekki verið bundnar í fjárhag.  
    * Sjálfgefið bókunarlag fer á Núverandi lag ef bókin er bókuð í fjárhag, en Ekkert ef það er ekki bókað í fjárhag. Uppfæra bókunarlag ef nauðsynlegt er fyrir þetta bók til að bóka í öðru lagi.  
8. Sláið inn eða veldu gildi í reitnum dagatal.
    * Afleiddar afskriftabækur munu bóka færslur á mismunandi bækur í einu. Færslur eru stofnaðar með aðalbókinni og á meðan á bókun stendur, er nákvæmt afrit færslunnar bókað í afleiddu bókina. Ekki eru framkvæmdir endurreikningar með færslum afleiddrar bókar, svo ekki ætti að nota hana fyrir afskriftarfærslur.  

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Tengið bók við eignaflokk
1. Smella á eignaflokkar.
2. Færa inn eða veljið gildi í svæðinu eignaflokkur.
3. Í reitinn líftími skal slá inn númer.
    * Athugaðu að afskriftartímabils er reiknað eftir uppsetningu líftíma.  
    * Er hægt að setja afskriftarreglan eins og krafist er hvað varðar skatta.  

