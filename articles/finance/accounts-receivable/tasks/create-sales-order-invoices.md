---
title: Stofna sölupantanareikninga
description: Þetta efnisatriði lýsir því hvernig á að reikningsfæra sölupöntun, þ.m.t. sameina reikninga og runuvinnslu.
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b6712779ca64f5934edd37730597541679b86e43
ms.sourcegitcommit: 03f53980a4bc67b73ac2be76a3b3e7331d0db705
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/18/2021
ms.locfileid: "7394611"
---
# <a name="create-sales-order-invoices"></a>Stofna sölupantanareikninga

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að reikningsfæra sölupöntun, þ.m.t. sameina reikninga og runuvinnslu. Þessi aðferð notar sýnigögn USMF fyrirtækisins.


## <a name="create-an-invoice-from-a-sales-order"></a>Stofna reikning úr sölupöntun
1. Farðu í **Sloðunarrúða > Kerfiseiningar > viðskiptakröfur > Pantanir > Sendar en óreikningsfærðar sölupantanir**.
2. Veljið sölupöntun af listanum. 
3. Í **aðgerðasvæðinu** er smellt á **Reikningur > Mynda > Reikningur**. Athugið að þessi sölupöntun hefur margir fylgiseðlar tengjast. Það mun einungis sýna orðið *mörg* í stað númer fylgiseðils.  
4. Útvíkkaðu hlutann **Færibreytur**.
    - Bókun verður að vera stillt á Já til að bóka reikninginn. Einnig er hægt að slökkva á bókun og prenta bara reikning. Hins vegar hægt að gera sömu niðurstöðu með því að stofna bráðabirgðareikninginn í stað reiknings.  
    - Þessi valkostur er notaður fyrir runuvinnslu. Fyrirspurnin er keyrð þegar runuvinnsla er keyrð.
5. Í reitnum **Prenta** skal velja 'Eftir'.
6. Velja skal **Já** til að **Prenta reikninginn**. Prentstýring er hægt að prenta mörg afrit af reikningi og senda einnig reikninginn með tölvupósti sem pdf-skrá.  
7. Í reitnum **Prenta gjöld** skaltu velja Taka saman.
8. Í reitnum **Athuga lánamark** skal velja Staða.
9. Smelltu á **Hætta við**.

## <a name="combine-orders-into-a-single-invoice"></a>Sameina pantanir í einn reikning
1. Farðu í **Sloðunarrúða > Kerfiseiningar > viðskiptakröfur > Pantanir > Allar sölupantanir**.
2. Finna viðskiptavin sem hefur opna marga reikninga.
3. Veldu margar opnar sölupantanir frá sama viðskiptavini.
4. Í **aðgerðasvæðinu** er smellt á **Reikningur > Mynda > Reikningur**.
5. Útvíkkaðu hlutann **Færibreytur**.
6. Í reitnum **Magn** velurðu Allt. Athugið að eru tvo reikninga eru skráðir í hlutanum yfirlit. Látum okkur nú sameina þau í einn reikning.  
7. í reitnum **Safnuppfærsla fyrir** skal velja Lykilnúmer Reiknings.
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
