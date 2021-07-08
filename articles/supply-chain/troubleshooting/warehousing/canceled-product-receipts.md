---
title: Innhreyfingarskjöl afurða sem hætt var við uppfæra ekki færslustöðu í skráð
description: Eftir að hætt er við innhreyfingarskjöl afurða í hleðslu á innleið uppfærir kerfið sjálfkrafa stöðu birgðafærslunnar úr móttekið í pantað.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294099"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a>Innhreyfingarskjöl afurða sem hætt var við uppfæra ekki færslustöðu í skráð

## <a name="symptoms"></a>Einkenni

Þegar aðgerðin **Hætta við innhreyfingarskjöl afurða** hefur verið keyrð uppfærir kerfið sjálfkrafa stöðu birgðafærslna úr *Móttekið* í *Pantað*.

## <a name="resolution"></a>Lausn

Þegar hætt er við fylgiseðla fyrir hleðslur á útleið helst staða birgðafærslna óbreytt í *Tekið til*. Hinsvegar þegar hætt er við innhreyfingarskjöl afurða úr hleðslu á innleið er staða birgðafærslna ekki endurheimt í *Skráð*. Þar af leiðandi, eftir að hætt er við innhreyfingarskjal afurðar úr hleðslu á innleið, verður starfsmaður í vöruhúsi að endurskrá vörumagnið fyrir hleðslurnar.

Frekari upplýsingar er að finna í [Skrá vörumagn sem kemur með hleðslu á innleið](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).
