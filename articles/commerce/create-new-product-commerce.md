---
title: Stofna nýja afurð í Commerce
description: Þessi grein lýsir því hvernig á að búa til nýja vöru í Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 654ba19b0bc96ab40c8c27106fd819faa85a4ce8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270182"
---
# <a name="create-a-new-product-in-commerce"></a>Stofna nýja afurð í Commerce


[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að búa til nýja vöru í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Afurð er fyrst og fremst skilgreind af afurðarnúmeri, heiti og lýsingu. Hins vegar þarf fleiri upplýsingar til að hægt sé að lýsa afurð eða þjónustu:

## <a name="create-a-new-product"></a>Stofna nýja afurð

1. Í Skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Afurðir og flokkar \> Afurðir eftir flokki**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í fellilistanum **Gerð afurðar** velurðu annaðhvort **Vara** eða **Þjónusta**.
1. Í fellilistanum **Undirgerð afurðar** velurðu annaðhvort **Afurð** (ef afurðin hefur engin afbrigði) eða **Afurðasniðmát** (ef afurðin verður með afbrigði).
1. Í reitinn **Afurðanúmer** slærðu inn afurðarnúmer ef slíkt hefur ekki þegar verið sett inn.
1. Í reitinn **Heiti afurðar** slærðu inn afurðarheiti.
1. Í reitinn **Leitarheiti** slærðu inn leitarheiti.
1. Í fellilistanum **Smásöluflokkur** velurðu viðeigandi flokk.
1. Ef afurðin er sett velurðu **Já** fyrir **Afurðasett**.
1. Ef undirtegund afurðarinnar er afurðarsniðmát skaltu stilla **Afurðavíddaflokkur** til að innihalda studd afbrigði. Valkostirnir eru meðal annars **Litur**, **Stærð**, **Stíll** og **Stilling**. Þú gætir þurft að búa til fleiri afurðavíddaflokka ef þörf krefur.
1. Í fellilistanum **Afbrigðistækni** velurðu viðeigandi valkost.
1. Veljið **Í lagi**.

Eftirfarandi mynd sýnir dæmi um afurð sem er bætt við.

![Stofna afurð.](media/create-new-product.png)

Þegar afurð er bætt við er hægt að stilla viðbótargögn fyrir hana, svo sem **Afurðarlýsing**, **Afbrigðaflokkar**, **Víddarflokkar**, **Afurðaeigindir** og **Skyldar afurðir**.

Eftirfarandi mynd sýnir viðbótarupplýsingar afurðar.

![Upplýsingar um afurð.](media/create-new-product-2.png)

### <a name="create-product-variants"></a>Stofna afurðarafbrigði

Ef undirtegund afurðarinnar er **Afurðarsniðmát** verður að búa til sérstök afbrigði. 

Til að stofna afurðarafbrigði skal fylgja eftirfarandi skrefum.

1. Í aðgerðasvæðinu velurðu **Afurðarafbrigði**.
1. Ef afbrigðishópar hafa verið valdir á aðgerðarglugganum, veldu **Tillögur um afbrigði*.
1. Veldu afbrigði sem þú vilt styðja fyrir afurðina.
1. Velja **Stofna**.

## <a name="release-a-product"></a>Losaðu afurð

Til að selja afurð verður hún fyrst að verða gefin út til lögaðila.

1. Af afurðasíðunni velurðu **Losa afurðir**.

    ![Losa afurð.](media/create-new-product-3.png)

1. Veldu afurðina til að losa og veldu síðan **Næst**.

    ![Veldu afurð til að losa.](media/create-new-product-4.png)

1. Veldu flokk afurðarafbrigða til að losa og veldu síðan **Næst**.

    ![Veldu afbrigði til að losa.](media/create-new-product-5.png)

1. Veldu lögaðilann og veldu síðan **Næst**.

    ![Veldu lögaðila.](media/create-new-product-6.png)

1. Veljið **Ljúka**.

    ![Ljúktu losun afurðar.](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a>Samskipaðu losaða afurð

Þegar afurð er losuð þarf hún síðan frekari stillingar sem fela í sér að bæta við verði við afurðina.

1. Í Skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Afurðir og flokkar \> Losaðar afurðir eftir flokki**.
1. Veldu afurðaflokkshnút fyrir afurðina sem var losuð og veldu síðan afurðina af afurðalistanum.
1. Í aðgerðaglugganum velurðu **Breyta**.
1. Í kaflanum **Kaupa** stillirðu alla nauðsynlega eiginleika, þ.m.t. **Eining**, **Verð** og **Magn**.
1. Í aðgerðarglugganum velurðu **Staðfesta** til að tryggja að engar villur hafi verið tilkynntar vegna reita sem vantar.
1. Í aðgerðaglugganum velurðu **Vista.**

Eftirfarandi mynd sýnir dæmi um stillingu á losaðri afurð.

![Skilgreina losaða afurð.](media/create-new-product-8.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Stofna lögaðila](channels-legal-entities.md)

[Búa til afbrigðaflokk](create-variant-group.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
