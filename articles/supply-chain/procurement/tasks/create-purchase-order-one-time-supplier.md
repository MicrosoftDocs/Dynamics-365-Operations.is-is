---
title: Stofna innkaupapöntun fyrir einskiptisbirgi
description: Þessi verklýsing sýnir hvernig á að stofna innkaupapöntun fyrir eins-skiptis birgi.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 76915772809d736cac9e8a9439d9e693a4490eec
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204908"
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

