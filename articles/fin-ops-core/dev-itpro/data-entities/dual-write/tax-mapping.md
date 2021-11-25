---
title: Samþættur skattur
description: Þetta efni lýsir samþættingu skattaupplýsinga milli Finance and Operations og Dataverse.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: d1e74bbbeba019ca48dd823b58251643e96edd0c
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782211"
---
# <a name="integrated-tax"></a>Samþættur skattur

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Skattuppsetningargögn skilgreina uppsetningu bæði á óbeinum sköttum (VSK, GST, virðisaukaskattur) og staðgreiðslu. Það lýsir skattaútreikningsreglu, skatthlutfalli, skattabókhaldi, uppgjöri og öðrum hugtökum.

## <a name="templates"></a>Sniðmát

Skattagögn innihalda safn af töflukortum sem vinna saman í gagnasamskiptum, eins og sýnt er í eftirfarandi töflu.

| Finance and Operations-smáforrit | Forrit viðskiptavinatengsla | lýsing |
|-----------------------------|-----------------------------------|-------------|
[VSK-flokkur vöru](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Skattayfirvöld](mapping-reference.md#193) | msdyn_taxauthorities | |
[Eining undanþágukóða virðisaukaskatts fyrir CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[VSK-flokkar](mapping-reference.md#195) | msdyn_taxgroups | |
[Fjárhagsbókunarflokkar virðisaukaskatts V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Staðgreiðsluskattskóðar](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Staðgreiðsluskattsflokkar](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
