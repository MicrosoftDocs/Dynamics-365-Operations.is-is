---
title: Engin frá-dagsetning er í flipa virkra verða á síðu vöruverðs.
description: Engin frá-dagsetning er í flipa virkra verða á síðu vöruverðs.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: dc0071bc508fc1b2fcfa5071f0756434641b7e6f872308ed4febb0cb34d37840
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730131"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a>Engin frá-dagsetning er í flipa virkra verða á síðu vöruverðs.

KB númer: 4613548

## <a name="symptoms"></a>Einkenni

Ekkert **Frá-dagsetning** gildi er í flipa **Virkra verða** á síðu **Vöruverðs**.

## <a name="resolution"></a>Upplausn

Gildið **Frá dagsetningu** (gildistími) sem er stillt á biðverðinu færist ekki yfir á virka verðið.

Þegar kostnaðarfærsla vöru er upphaflega færð inn hefur hún stöðuna *Í biðstöðu* og ætlaða upphafsdagsetningu. Þegar kostnaðarfærsla vöru er virkjuð uppfærist staðan í *Virk* og gildisdagsetningin er uppfærð í virkjunardagsetningu. Því er virkjunardagsetning virks verðs alltaf raundagsetning virkjunarinnar.

Frekari upplýsingar eru í [Yfirlit kostnaðarútgáfa](../../cost-management/costing-versions.md).
