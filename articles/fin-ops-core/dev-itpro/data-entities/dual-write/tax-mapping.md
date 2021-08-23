---
title: Samþættur skattur
description: Þetta efni lýsir samþættingu skattaupplýsinga milli Finance and Operations og Dataverse.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: c7e76294944196670ed4b02ebf785c1bed7b5106f73d4b66a15a19c9a4235cbf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738553"
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
