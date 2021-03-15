---
title: Stofna innkaupapöntun fyrir einskiptisbirgi
description: Þessi verklýsing sýnir hvernig á að stofna innkaupapöntun fyrir eins-skiptis birgi.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c4885547cdf2f8496446761e27ce39e67e670f15
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016403"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Stofna innkaupapöntun fyrir einskiptisbirgi

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að stofna innkaupapöntun fyrir eins-skiptis birgi. Birgirinn er stofnuð sjálfkrafa með innkaupapöntun, frekar en að þurfa að stofna lánardrottnalykil handvirkt. Innkaupapöntun eru yfirleitt stofnaðar af innkaupastjórar. Dæmi sem eru sýnd í þessari handbók er hægt að nota sýnigögn USMF-fyrirtækisins. Það er skilyrði að eins skiptis lánardrottinn hefur verið sett upp á síðunni færibreytum viðskiptaskulda.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Stofna innkaupapöntun fyrir einskiptisbirgi
1. Fara í innkaup og aðföng > innkaupapöntun > allar innkaupapantanir.
2. Smellið á „Nýtt“.
3. Velja Já í svæðið eins-skiptis lánardrottinn.
    * Lykill lánardrottins er sjálfkrafa stofnuð og úthlutað á innkaupapöntun. Lánardrottnalykill er stofnuð byggt á sniðmátinu sem er tilgreind á flipanum Almennt í síðunni færibreytum viðskiptaskulda.  
4. Færið inn heiti fyrir lánardrottinn í svæðið Heiti.
5. Smellið á „Í lagi“.
    * Innkaupapöntun má nú ljúka og unnin eins og hver önnur pöntun. Það eru engar sérstakar einkenni tengdar því hvernig þetta er gert. Reikningur reikningsfærir færslu á gjalddaga á lánardrottnalykil sem stofnaður var með pöntun og þá verður greiðslan unnin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]