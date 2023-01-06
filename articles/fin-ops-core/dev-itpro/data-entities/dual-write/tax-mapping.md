---
title: Samþættur skattur
description: Þessi grein lýsir samþættingu skattagagna milli fjármála og rekstrar og Dataverse.
author: josaw
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8f148b710e2294edf1e402b9b8b22cb24e60a1f2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288795"
---
# <a name="integrated-tax"></a>Samþættur skattur

[!include [banner](../../includes/banner.md)]



Skattuppsetningargögn skilgreina uppsetningu bæði á óbeinum sköttum (VSK, GST, virðisaukaskattur) og staðgreiðslu. Það lýsir skattaútreikningsreglu, skatthlutfalli, skattabókhaldi, uppgjöri og öðrum hugtökum.

## <a name="templates"></a>Sniðmát

Skattagögn innihalda safn af töflukortum sem vinna saman í gagnasamskiptum, eins og sýnt er í eftirfarandi töflu.

| Forrit fyrir fjármál- og rekstur | Forrit viðskiptavinatengsla | Lýsing |
|-----------------------------|-----------------------------------|-------------|
[VSK-flokkur vöru](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Skattayfirvöld](mapping-reference.md#193) | msdyn_taxauthorities | |
[Eining undanþágukóða virðisaukaskatts fyrir CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[VSK-flokkar](mapping-reference.md#195) | msdyn_taxgroups | |
[Fjárhagsbókunarflokkar virðisaukaskatts V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Staðgreiðsluskattskóðar](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Staðgreiðsluskattsflokkar](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

