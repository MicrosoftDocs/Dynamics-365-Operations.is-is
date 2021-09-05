---
title: Setja upp virðislíkön
description: Þessi ferli sýnir hvernig á að stofna nýtt eignabók og tengja hana við eignaflokk.
author: moaamer
ms.date: 08/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46c26e5fad3c5c60d87c2fea2b29043c69b82b5d
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344659"
---
# <a name="set-up-value-models"></a>Setja upp virðislíkön

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]


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

  - Afskriftarímabil eru reiknuð eftir að líftími eignarinnar er færður inn.  
  - Hægt er að stilla þessa afskrifarvenju eins og þarf af skattalegum ástæðum.
  - Fyrir eignir sem tengjast leigusamningum verður gildið í reitnum **Líftími** hnekkt af annaðhvort leigutímanum í eignabókinni eða nýtingartíma eignarinnar eftir því hvort er styttra. Ef reiturinn **Eignarhald flutt** er stilltur á **Já** fyrir leigubókina mun gildið í reitnum **Líftími** alltaf vera nýtingartími eignarinnar.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
