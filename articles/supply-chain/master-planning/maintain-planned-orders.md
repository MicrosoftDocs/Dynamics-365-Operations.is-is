---
title: Vinna með áætlaðar pantanir
description: Þetta efnisatriði gefur upplýsingar um hvernig á að stjórna áætluðum pöntunum. Hún lýsir því hvernig hægt er að uppfæra stöðu áætlaðra pantana, staðfesta þær og sía fyrir áætluðum pöntunum sem hafa sömu stöðu og valin áætluð pöntun.
author: roxanadiaconu
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ddf2c7b4c67bec6c29387c78d1fdb021d85d702
ms.sourcegitcommit: 620e15555d176eec3905b48d5001af1c50107ce6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2019
ms.locfileid: "1993441"
---
# <a name="maintain-planned-orders"></a>Vinna með áætlaðar pantanir

[!include [banner](../includes/banner.md)]

Þetta efnisatriði gefur upplýsingar um hvernig á að stjórna áætluðum pöntunum. Hún lýsir því hvernig hægt er að uppfæra stöðu áætlaðra pantana, staðfesta þær og sía fyrir áætluðum pöntunum sem hafa sömu stöðu og valin áætluð pöntun.

Hægt er að stjórna áætluðum pöntunum úr vinnusvæðinu **Aðaláætlanagerð**, úr listanum **Áætluð pöntun** eða listunum **Áætlaðar framleiðslupantanir**, **Áætlaðar innkaupapantanir**, og **Flutningsáætlanir**. 

## <a name="planned-order-status"></a>Staða tillögu
Hægt er að nota svæðið **Staða** til að aðstoða við að rekja framgang. Eftirtalin gildi eru notuð:

-   Þegar aðaláætlunagerð°myndar áætlaðar pantanir, hafa áætlaðar pantanir stöðuna **Óunnið**.
-   Þegar valið er að staðfesta ekki áætlaða pöntun getur hún fengið stöðuna **Lokið**.
-   Ef þú vilt festa skipulagða pöntun geturðu breytt stöðunni í **Samþykkt**. Skipulögð pantanir með stöðuna **Samþykkt** er virt með aðalskipulagningu, svo þeim er ekki breytt eða þeim eytt. 

## <a name="firming-planned-orders"></a>Staðfesting á tillögum 
Með því að staðfesta tillögur eru raunverulegar pantanir búnar til. Þetta eru líka þekkt sem *losaðar* eða *opnar pantanir*. Þegar áætluð pöntun er staðfest er hún færð í pöntunarhluta í viðeigandi einingu.

Þú getur valið tvo staðfestingarvalkosti af síðunni **Tillögur**:

-   **Staðfesta** - Þetta mun staðfesta eina eða margar valdar tillögur.
-   **Staðfesta allt** - Þetta staðfestir allar tillögur í síunni. Með því að nota **Staðfesta allt** þarftu ekki að velja tillöguna, allar tillögur innan síunnar verða staðfestar. Þessi valkostur getur verið gagnlegur ef þú ert að styrkja mikinn fjölda tillagna.

> [!NOTE]
> Þú getur fylgst með fyrirhugaðri pöntun sem var stytt frá **Staðfestingarsaga** undir **Skjámyndinni Tillögur > Skoða > Staðfestingasaga**.

## <a name="parallelize-firming"></a>Samhliða staðfesting
Ef þú ætlar að vinna margar pantanir í einu getur samhliða keyrsla bætt keyrslutímann eða frammistöðu. Þessi valkostur er tiltækur við staðfestingu á mörgum tillögum með annaðhvort **Staðfesta** eða **Staðfesta allt**. Eftirfarandi færibreytur eru tiltækar:

-   **Samhliða staðfesting** - Ef **Já** verður staðfestingarferlið gert samhliða með fjölda þráða sem skilgreindir eru í **Fjöldi þráða**.
-   **Fjöldi þráða** - Stýrir fjölda þráða sem notaðir eru til að gera staðfestingarferlið samhliða. Færiubreytan er aðeins sýnd þegar **Samhliða staðfesting** er stillt á **Já**.


<a name="additional-resources"></a>Frekari upplýsingar
--------

[Aðaláætlanir](master-plans.md)



