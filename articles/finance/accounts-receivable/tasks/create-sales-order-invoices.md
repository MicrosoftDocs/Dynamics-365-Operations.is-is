---
title: Stofna sölupantanareikninga
description: Þessi grein lýsir því hvernig á að reikningsfæra sölupöntun, þar á meðal sameiningu reikninga og runuvinnslu.
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ff76eac54da6621d999d9b629fac920ba8de294
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778385"
---
# <a name="create-sales-order-invoices"></a>Stofna sölupantanareikninga

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir því hvernig á að reikningsfæra sölupöntun, þar á meðal sameiningu reikninga og runuvinnslu. Þessi aðferð notar sýnigögn USMF fyrirtækisins.


## <a name="create-an-invoice-from-a-sales-order"></a>Stofna reikning úr sölupöntun
1. Farðu í **Sloðunarrúða > Kerfiseiningar > viðskiptakröfur > Pantanir > Sendar en óreikningsfærðar sölupantanir**.
2. Veljið sölupöntun af listanum. 
3. Í **aðgerðasvæðinu** er smellt á **Reikningur > Mynda > Reikningur**. Athugið að þessi sölupöntun hefur margir fylgiseðlar tengjast. Það mun einungis sýna orðið *mörg* í stað númer fylgiseðils.  
4. Útvíkkaðu hlutann **Færibreytur**.
    - Birting verður að vera stillt á **Já** til að bóka reikninginn. Einnig er hægt að slökkva á bókun og prenta bara reikning. Hins vegar hægt að gera sömu niðurstöðu með því að stofna bráðabirgðareikninginn í stað reiknings.  
    - Þessi valkostur er notaður fyrir runuvinnslu. Fyrirspurnin er keyrð þegar runuvinnsla er keyrð.
5. Í **Prenta** reit, veldu **Eftir**.
6. Velja skal **Já** til að **Prenta reikninginn**. Prentstjórnun getur prentað mörg eintök af reikningnum og einnig sent reikninginn með tölvupósti sem PDF skjal.  
7. Í **Prentunargjöld** reit, veldu **Tekið saman**.
8. Í **Athugaðu lánshæfismat** reit, veldu **Jafnvægi**.
9. Smelltu á **Hætta við**.

## <a name="combine-orders-into-a-single-invoice"></a>Sameina pantanir í einn reikning
1. Farðu í **Sloðunarrúða > Kerfiseiningar > viðskiptakröfur > Pantanir > Allar sölupantanir**.
2. Finna viðskiptavin sem hefur opna marga reikninga.
3. Veldu margar opnar sölupantanir frá sama viðskiptavini.
4. Í **aðgerðasvæðinu** er smellt á **Reikningur > Mynda > Reikningur**.
5. Útvíkkaðu hlutann **Færibreytur**.
6. Í reitnum **Magn** velurðu **Allt**. Athugið að eru tvo reikninga eru skráðir í hlutanum yfirlit. Látum okkur nú sameina þau í einn reikning.  
7. Í **Yfirlitsuppfærsla fyrir** reit, veldu **Reikningsreikningur**.
8. Smelltu á **Raða** til að sameina sölupantanir í einn reikning. Tvær sölupantanir eru nú sameinaðar einn reikning.   
9. Smelltu á **Hætta við**.
10. Smellið á **Já**.

## <a name="post-invoices-in-a-batch"></a>Bóka reikninga í runu
1. Farðu í **Skoðunarrúðu > Einingar > Viðskiptakröfur > Reikningar > Runureikningsfærsla > Reikningur**.
2. Smellið á **Velja**.
3. Smellt er á **OK**.
4. Smelltu á **Runa**.
5. Veldu **Já** í **Runuvinnslu**.
6. Smelltu á **Endurtekning**.
7. Veldu **Dagar**.
8. Smellt er á **OK**.
9. Smellt er á **OK**.
10. Smelltu á **Hætta við**.
11. Smellið á **Já**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
