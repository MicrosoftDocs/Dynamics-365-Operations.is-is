---
title: Setja upp virðislíkön
description: Þessi ferli sýnir hvernig á að stofna nýtt eignabók og tengja hana við eignaflokk.
author: moaamer
ms.date: 12/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71d256b600956a4e525cde626c958713f6258f5a
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727062"
---
# <a name="set-up-value-models"></a>Setja upp virðislíkön

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

Þessi ferli sýnir hvernig á að stofna nýtt eignabók og tengja hana við eignaflokk.

## <a name="create-a-book"></a>Búa til bók
1. Farið í **Eignir \> Uppsetning \> Bækur**.
2. Veljið **Nýtt**.
3. Í reitinn **Bók** skal færa inn gildi.
4. Sláið inn gildi í reitnum **Lýsing**.
5. Stillið valkostinn **Reikna afskrift** á **Já**.

    Ef valkosturinn **Reikna út afskriftir** er stilltur á **Já** verður tengd eignabók höfð með í afskriftartillögum. Ef hann er stilltur á **Nei** verður eignabókin ekki sjálfkrafa afskrifuð.

6. Sláið inn eða veldu gildi í reitnum **Afskriftarregla**.

    * Önnur afskriftarregla er einnig þekkt sem umskiptingaraðferð afskriftar. Afskriftatillögu verður skipta yfir í þessa forstillingu þegar önnur forstilling reiknar afskriftarupphæð sem er jöfn eða meiri en sjálfgefinn afskriftareglu.
    * Óregluleg afskriftaregla er notuð fyrir aukalega afskrift af eign við óvenjulegar aðstæður. Til dæmis er hægt að nota þetta til að skrá niðurstöður úr náttúruhamfarir afskrift.
    * Ef valið er **Stofna afskriftaleiðréttingar með grunnleiðréttingum** verða afskriftarleiðréttingar sjálfkrafa búnar til þegar gildi eignarinnar er uppfært. Annars hefur uppfært eignavirði aðeins áhrif á útreikninga á afskriftum í framtíðinni.

7. Stilltu valkostinn **Stofna afskriftaleiðréttingar með grunnleiðréttingum** á **Já**.

    * Að sjálfgefnu verða færslur eignabókar bókaðar í fjárhag. Hins vegar er hægt að gera bókun í fjárhag fyrir bókina óvirka með því að stilla reitinn **Bóka í fjárhag** á **Nei**. Bækur sem eru ekki bókaðar í fjárhag eru yfirleitt notaðar fyrir skattaskýrslugerð. Þessi valkostur veitir þér meiri sveigjanleika til að eyða sögulegum færslum fyrir eignabókina því að færslurnar hafa ekki verið skráðar í fjárhaginn.
    * Reiturinn **Bókunarlag** er sjálfgefið stilltur á **Núverandi lag** ef bókin er bókuð í fjárhaginn og **Ekkert** ef bókin er ekki bókuð í fjárhaginn. Uppfærðu gildið í reitnum **Bókunarlag** ef færslur fyrir þessa bók eiga að vera bókuð á annað lag.

8. Reikna jákvæða afskrift.

    * Valkosturinn **Reikna jákvæða afskrift** er stilltur á **Nei**. Þessi stilling gefur til kynna að afskriftir muni færast í valda eignabók. Þar að auki eru valkostirnir **Leyfa bókað nettóvirði hærra en kaupverð** og **Leyfa neikvætt bókað nettóvirði** báðir stilltir á **Nei** og hægt er að breyta hvorri stillingu fyrir sig. 
    * Til að reikna jákvæðar afskriftir skal stilla valkostinn **Reikna jákvæðar afskriftir** á **Já**. Þessi stilling gefur til kynna að afskriftin muni skuldfærst í eignabókina. Þegar valkosturinn **Reikna jákvæðar afskriftir** er stilltur á **Já** munu valkostirnir **Leyfa bókað nettóvirði hærra en kaupverð** og **Leyfa neikvætt bókað nettóvirði** vera sjálfkrafa stilltir á **Já** og þeim verður læst. Þessi læsing hjálpar til við að tryggja að jákvæðar afskriftir verði aðeins gerðar á eignum sem voru yfirteknir með neikvæðu bókfærðu virði (kredit). 

10. Sláið inn eða veldu gildi í reitnum **Dagatal**.

    Afleiddar afskriftabækur munu bóka færslur á mismunandi bækur í einu. Færslur eru stofnaðar með aðalbókinni og á meðan á bókun stendur, er nákvæmt afrit færslunnar bókað í afleiddu bókina. Ekki eru framkvæmdir endurreikningar með færslum afleiddrar bókar, svo ekki ætti að nota hana fyrir afskriftarfærslur.

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Tengið bók við eignaflokk

1. Veldu **Eignaflokkar**.
2. Í reitnum **Eignaflokkur** skal færa inn eða velja gildi.
3. Í reitinn **Líftími** skal slá inn númer.

    * Afskriftarímabil eru reiknuð eftir að líftími eignarinnar er færður inn.
    * Hægt er að stilla þessa afskrifarvenju eins og þarf af skattalegum ástæðum.
    * Fyrir eignir sem tengjast leigusamningum verður gildið í reitnum **Líftími** hnekkt af leigutímanum í eignabókinni og nýtingartíma eignar. Ef valkosturinn **Eignarhald flutt** er stilltur á **Já** fyrir leigubókina mun gildið í reitnum **Líftími** alltaf vera nýtingartími eignarinnar.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
