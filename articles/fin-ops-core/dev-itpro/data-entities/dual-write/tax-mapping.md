---
title: Samþættur skattur
description: Þessi grein lýsir samþættingu skattagagna milli Finance and Operations og Dataverse.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8864a9567d57739aa72fa1859f5cfce6df33e8f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864544"
---
# <a name="integrated-tax"></a>Samþættur skattur

[!include [banner](../../includes/banner.md)]



Skattuppsetningargögn skilgreina uppsetningu bæði á óbeinum sköttum (VSK, GST, virðisaukaskattur) og staðgreiðslu. Það lýsir skattaútreikningsreglu, skatthlutfalli, skattabókhaldi, uppgjöri og öðrum hugtökum.

## <a name="templates"></a>Sniðmát

Skattagögn innihalda safn af töflukortum sem vinna saman í gagnasamskiptum, eins og sýnt er í eftirfarandi töflu.

| Forrit Finance and Operations | Forrit viðskiptavinatengsla | Lýsing |
|-----------------------------|-----------------------------------|-------------|
[VSK-flokkur vöru](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Skattayfirvöld](mapping-reference.md#193) | msdyn_taxauthorities | |
[Eining undanþágukóða virðisaukaskatts fyrir CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[VSK-flokkar](mapping-reference.md#195) | msdyn_taxgroups | |
[Fjárhagsbókunarflokkar virðisaukaskatts V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Staðgreiðsluskattskóðar](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Staðgreiðsluskattsflokkar](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
