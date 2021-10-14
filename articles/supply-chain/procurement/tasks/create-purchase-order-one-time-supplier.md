---
title: Stofna innkaupapöntun fyrir einskiptisbirgi
description: Þessi verklýsing sýnir hvernig á að stofna innkaupapöntun fyrir eins-skiptis birgi.
author: Henrikan
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e89a9d1b382efa3b90b8d70e84777321e9595f4a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579545"
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