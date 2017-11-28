---
title: "Smásölustigveldi"
description: "Þessi grein lýsir smásölustigveldi í Microsoft Dynamics 365 for Retail."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e94b59540c9ef188a07e2e24ef4a04829b9d37f8
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="retail-hierarchies"></a>Smásölustigveldi

[!include[banner](includes/banner.md)]


Þessi grein lýsir smásölustigveldi í Microsoft Dynamics 365 for Retail.

Hægt er að stofna smásöluflokkastigveldi til að skipuleggja afurðirnar sem seldar eru í gegnum smásölurásir. Hægt er að nota smásölustigveldi afurðar til að flokka eða flokka afurðir. Síðan er hægt að nota þessar afurðir til að stofna afurðaúrval og vildarkerfi viðskiptavina. Einnig er hægt úthluta afurðareigindum og eiginleikum, úthluta uppbyggingu verðlagningar, taka með afurðir í kynningartilboð afurða og nota afurðir fyrir skýrslugerð. Hægt er að stofna eitt tegundastigveldi til að tákna allar afurðir og tegundir í fyrirtækjasamstæðunni, og nota síðan tegundastigveldi fyrir margan tilgang. Einnig er hægt að stofna mörg tegundastigveldi í sérstökum tilgangi, t. d. til kynningar á afurð. Þegar stofnað er stigveldi smásöluafurða verður að úthluta tegundastigveldisgerð til að auðkenna tilgang tegundastigveldisins. Til dæmis er aðeins vísað í afurðastigveldi sem er úthlutað á **Yfirlitsstigveldi smásölu** þegar flett er í afurðum eftir tegund á netinu eða á sölustað (POS).

## <a name="retail-hierarchy-types"></a>Gerðir smásölustigvelda
Eftirfarandi tafla sýnir þær gerðir tegundastigvelda sem eru tiltækar og almennan tilgang hverrar gerðar.

| Gerð tegundastigveldis       | Tilgangur                                                                                                                                                                                                                                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stigveldi smásöluafurða      | Veljið þessa stigveldisgerð til að skilgreina aðalstigveldi smásöluafurða fyrir fyrirtækið. Hægt er að nota þessa gerð stigveldis fyrir smásölu, verðlagningu og kynningartilboð, skýrslugerð og skipulagningu úrvals. Aðeins er hægt að úthluta einu stigveldi smásöluafurða þessu stigveldi.                                       |
| Viðbótarstigveldi smásölu | Notið þessa gerð stigveldis fyrir allar frekari tegundir smásölustigveldis sem á að stofna. Til dæmis á vorin þarf kynningartilboð fyrir sundföt. Þess vegna hefurðu sundfataafurðirnar í aðskildu tegundastigveldi og beita verðlagningu kynningartilboðs á mismunandi tegundir afurða. |
| Skoðunarstigveldi smásölu   | Notið þessa gerð stigveldis til að flokka og raða afurðum í tegundum svo að hægt sé að skoða afurðir á netinu eða á söllustað.                                                                                                                                                                                       |

Með tegundastigveldi smásölu til að skipuleggja vörur er hægt að setja upp og viðhalda afurðareigindum og eiginleikum tegundastigs. Þessi eigindir og eiginleikar hafa stillingar fyrir afurðavíddir og stillingar á Sölustað. Allar afurðir sem er úthlutað á tegundirnar erfa sjálfkrafa þær eigindir og eiginleika sem eru skilgreindir. Einnig er hægt að afrita stillingar eiginleika fyrir afurðir í margar afurðir í valinni tegund á sama tíma.




