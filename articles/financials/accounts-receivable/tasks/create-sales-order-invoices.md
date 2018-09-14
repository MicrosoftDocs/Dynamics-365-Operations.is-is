--- 
title: "Stofna sölupantanareikninga"
description: "Þessi leiðarvísi fyrir verk lýsir reikningsfærslu sölupöntunar, þar á meðal sameiningu reikninga og runuvinnslu."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4b72d5b283f9401d358ee68f4650c486ebb2fd7d
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-sales-order-invoices"></a>Stofna sölupantanareikninga

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi leiðarvísi fyrir verk lýsir reikningsfærslu sölupöntunar, þar á meðal sameiningu reikninga og runuvinnslu. Þessi aðferð notar sýnigögn USMF fyrirtækisins.


## <a name="create-an-invoice-from-a-sales-order"></a>Stofna reikning úr sölupöntun
1. Farið í Viðskiptakröfur > Pantanir > Sendar sölupantanir sem ekki er búið að reikningsfæra.
2. Veljið sölupöntun af listanum. 
3. Smellið á „Reikningur“ á aðgerðarúðunni.
4. Smellið á „Reikningur“.
    * Athugið að þessi sölupöntun hefur margir fylgiseðlar tengjast. Það mun einungis sýna orðið <multiple> í stað númer fylgiseðils.  
5. Víkkið út færibreytuhlutann.
    * Bókun verður að vera stillt á Já til að bóka reikninginn. Einnig er hægt að slökkva á bókun og prenta bara reikning. Hins vegar hægt að gera sömu niðurstöðu með því að stofna bráðabirgðareikninginn í stað reiknings.  
    * Þessi valkostur er notaður fyrir runuvinnslu. Fyrirspurnin er keyrð þegar runuvinnsla er keyrð.    
6. Prenta svæði, velja 'Eftir'.
7. Velja skal Já til að Prenta reikninginn.
    * Prentstýring er hægt að prenta mörg afrit af reikningi og senda einnig reikninginn með tölvupósti sem pdf-skrá.  
8. Veljið ‚taka saman' í svæði Prenta gjöld.
9. Í Athuga lánamarkasvæðið skal velja "Staða".
10. Smellið á Hætta við.

## <a name="combine-orders-into-a-single-invoice"></a>Sameina pantanir í einn reikning
1. Farið í Viðskiptakröfur > Pantanir > Allar sölupantanir.
2. Finna viðskiptavin sem hefur opna marga reikninga.
3. Velja þarf opna sölupöntun.
4. Veljið aðra opin sölupöntun fyrir sama viðskiptavininn.
5. Smellið á „Reikningur“ á aðgerðarúðunni.
6. Smellt er á Reikningnum.
7. Víkkið út færibreytuhlutann.
8. Veljið „Allt“ á svæðinu „Magn“.
    * Athugið að eru tvo reikninga eru skráðir í hlutanum yfirlit. Látum okkur nú sameina þau í einn reikning.  
9. í svæðið safnuppfærslu fyrir, Veljið 'Lykilnúmer Reiknings'.
10. Smellt er á Skipulag til að sameina sölupantanir í einn reikning.
    * Tvær sölupantanir eru nú sameinaðar einn reikning.   
11. Smellið á Hætta við.
12. Smella á Já.

## <a name="post-invoices-in-a-batch"></a>Bóka reikninga í runu
1. Fara í Viðskiptakröfur > Reikningar > Runa reikningsfærsla > Reikningur.
2. Smellið á Velja.
3. Smellið á „Í lagi“.
4. Smellt er á Runu.
5. Smellt er á Já til að kveikja á runuvinnslu.
6. Smellið á Endurtekning.
7. Velja daga
8. Smellið á „Í lagi“.
9. Smellið á „Í lagi“.
10. Smellið á Hætta við.
11. Smella á Já.


