---
title: Stigveldi verslunar
description: Þessi grein lýsir stigveldi í Dynamics 365 Commerce.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.industry: Retail
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
ms.openlocfilehash: ce196acc8c4bced865b983b12d72f8bc6e4d02a0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271878"
---
# <a name="commerce-hierarchies"></a>Stigveldi verslunar

[!include [banner](includes/banner.md)]

Þessi grein lýsir stigveldi í Dynamics 365 Commerce.

Hægt er að stofna tegundastigveldi til að skipuleggja afurðirnar sem seldar eru í gegnum rásir. Hægt er að nota stigveldi afurðar til að flokka eða flokka afurðir. Síðan er hægt að nota þessar afurðir til að stofna afurðaúrval og vildarkerfi viðskiptavina. Einnig er hægt úthluta afurðareigindum og eiginleikum, úthluta uppbyggingu verðlagningar, taka með afurðir í kynningartilboð afurða og nota afurðir fyrir skýrslugerð. Hægt er að stofna eitt tegundastigveldi til að tákna allar afurðirnir og tegundir í fyrirtækjasamstæðunni, og nota síðan tegundastigveldi fyrir marga. Einnig er hægt að stofna mörg tegundastigveldi í sérstökum tilgangi, t. d. til kynningar á afurð. Þegar stofnað er stigveldi afurða verður að úthluta tegundastigveldisgerð til að auðkenna tilgang tegundastigveldisins. Til dæmis er aðeins vísað í afurðastigveldi sem er úthlutað á **Yfirlitsstigveldi Commerce** þegar flett er í afurðum eftir tegund á netinu eða á sölustað (POS).

## <a name="hierarchy-types"></a>Gerðir stigveldis

Eftirfarandi tafla sýnir þær gerðir tegundastigvelda sem eru tiltækar og almennan tilgang hverrar gerðar.

| Gerð tegundastigveldis       | Málefni |
|-------------------------------|---------|
| Afurðarstigveldi      | Veljið þessa stigveldisgerð til að skilgreina aðalstigveldi smásöluafurða fyrir fyrirtækið. Hægt er að nota þessa gerð stigveldis fyrir smásölu, verðlagningu og kynningartilboð, skýrslugerð og skipulagningu úrvals. Aðeins er hægt að úthluta einu stigveldi afurða þessu stigveldi. |
| Viðbótarstigveldi | Notið þessa gerð stigveldis fyrir allar frekari tegundir stigveldis sem á að stofna. Til dæmis á vorin þarf kynningartilboð fyrir sundföt. Þess vegna hefurðu sundfataafurðirnar í aðskildu tegundastigveldi og beita verðlagningu kynningartilboðs á mismunandi tegundir afurða. |
| Valmyndarstigveldi   | Notið þessa gerð stigveldis til að flokka og raða afurðum í tegundum svo að hægt sé að skoða afurðir á netinu eða á söllustað. |

Með tegundastigveldi til að skipuleggja vörur er hægt að setja upp og viðhalda afurðareigindum og eiginleikum tegundastigs. Þessi eigindir og eiginleikar hafa stillingar fyrir afurðavíddir og stillingar á Sölustað. Allar afurðir sem er úthlutað á tegundirnar erfa sjálfkrafa þær eigindir og eiginleika sem eru skilgreindir. Einnig er hægt að afrita stillingar eiginleika fyrir afurðir í margar afurðir í valinni tegund á sama tíma.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
