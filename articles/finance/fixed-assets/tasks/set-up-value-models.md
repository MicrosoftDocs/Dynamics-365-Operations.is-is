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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727062"
---
# <a name="set-up-value-models"></a>Setja upp virðislíkön

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

Þessi ferli sýnir hvernig á að stofna nýtt eignabók og tengja hana við eignaflokk.

## <a name="create-a-book"></a>Búa til bók
1. Fara til **Fastafjármunir \> Uppsetning \> Bækur**.
2. Veljið **Nýtt**.
3. Í **Bók** reit, sláðu inn gildi.
4. Sláið inn gildi í reitnum **Lýsing**.
5. Stilltu **Reiknaðu afskriftir** valmöguleika til **Já**.

    Ef **Reiknaðu afskriftir** er valkostur er stilltur á **Já**, verður tilheyrandi eignabók innifalin í afskriftatillögum. Ef það er stillt á **Nei**, eignabókin verður ekki sjálfkrafa afskrifuð.

6. Í **Afskriftasnið** reit, sláðu inn eða veldu gildi.

    * Önnur afskriftarregla er einnig þekkt sem umskiptingaraðferð afskriftar. Afskriftatillögu verður skipta yfir í þessa forstillingu þegar önnur forstilling reiknar afskriftarupphæð sem er jöfn eða meiri en sjálfgefinn afskriftareglu.
    * Óregluleg afskriftaregla er notuð fyrir aukalega afskrift af eign við óvenjulegar aðstæður. Til dæmis er hægt að nota þetta til að skrá niðurstöður úr náttúruhamfarir afskrift.
    * Ef þú velur **Stofna afskriftaleiðréttingar með grunnleiðréttingum**, verða leiðréttingar á afskriftum sjálfkrafa búnar til þegar verðmæti eignarinnar er uppfært. Að öðrum kosti mun uppfært eignavirði aðeins hafa áhrif á framtíðarafskriftaútreikninga.

7. Stilltu **Stofna afskriftaleiðréttingar með grunnleiðréttingum** valmöguleika til **Já**.

    * Sjálfgefið er að eignabókarfærslur eru bókaðar í fjárhag. Hins vegar geturðu slökkt á bókun í aðalbók fyrir bókina með því að stilla á **Bóka í aðalbók** valmöguleika til **Nei**. Bækur sem eru ekki bókaðar í fjárhag eru venjulega notaðar til skattskýrslu. Þessi valkostur veitir þér meiri sveigjanleika til að eyða sögulegum færslum fyrir eignabókina, vegna þess að færslurnar hafa ekki verið skuldbundnar í fjárhag.
    * Sjálfgefið er **Færslulag** reiturinn er stilltur á **Núverandi lag** ef bókin er færð í aðalbók og **Enginn** ef bókin er ekki færð í aðalbók. Uppfærðu verðmæti **Færslulag** reit ef færslur fyrir þessa bók ættu að vera bókaðar í annað lag.

8. Reiknaðu jákvæðar afskriftir.

    * Sjálfgefið er **Reiknaðu jákvæðar afskriftir** valkostur er stilltur á **Nei**. Þessi stilling gefur til kynna að afskriftir muni lána valinni eignabók. Að auki er **Leyfa hreint bókfært virði hærra en kaupverð** og **Leyfa neikvætt nettó bókfært virði** valkostir eru báðir stilltir á **Nei**, og stillingunum er hægt að breyta sjálfstætt. 
    * Til að reikna út jákvæðar afskriftir skaltu stilla **Reiknaðu jákvæðar afskriftir** valmöguleika til **Já**. Þessi stilling gefur til kynna að afskriftir munu skuldfæra eignabókina. Þegar **Reiknaðu jákvæðar afskriftir** valkostur er stilltur á **Já**, hinn **Leyfa hreint bókfært virði hærra en kaupverð** og **Leyfa neikvætt nettó bókfært virði** valkostir verða sjálfkrafa stilltir á **Já**, og þeim verður læst. Þessi læsing hjálpar til við að tryggja að jákvæðar afskriftir verði aðeins notaðar á fastafjármuni sem voru keyptir með neikvæðu bókfærðu virði (inneign). 

10. Í **Dagatal** reit, sláðu inn eða veldu gildi.

    Afleiddar afskriftabækur munu bóka færslur á mismunandi bækur í einu. Færslur eru stofnaðar með aðalbókinni og á meðan á bókun stendur, er nákvæmt afrit færslunnar bókað í afleiddu bókina. Ekki eru framkvæmdir endurreikningar með færslum afleiddrar bókar, svo ekki ætti að nota hana fyrir afskriftarfærslur.

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Tengið bók við eignaflokk

1. Veldu **Rekstrarfjármunahópar**.
2. Í reitnum **Eignaflokkur** skal færa inn eða velja gildi.
3. Í **Þjónustulíf** reit, sláðu inn númer.

    * Afskriftarímabil eru reiknuð eftir að líftími eignarinnar er færður inn.
    * Hægt er að stilla þessa afskrifarvenju eins og þarf af skattalegum ástæðum.
    * Fyrir fastafjármuni sem tengjast leigusamningum er verðmæti **Þjónustulíf** reiturinn verður hnekkt af því sem er styttra af leigutímanum í eignabók og nýtingartíma eigna. Ef **Eignaskipti** valkostur er stilltur á **Já** fyrir leigubók, verðmæti á **Þjónustulíf** reit mun alltaf vera nýtingartími eignarinnar.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
