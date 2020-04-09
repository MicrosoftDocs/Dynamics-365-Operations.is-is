---
title: Samþættur skattur
description: Þetta efni lýsir samþættingu skattaupplýsinga milli Finance and Operations og Common Data Service.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a4da37d45698290b40f6c72148f1500bef72127a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173086"
---
# <a name="integrated-tax"></a>Samþættur skattur

[!include [banner](../../includes/banner.md)]



Skattuppsetningargögn skilgreina uppsetningu bæði á óbeinum sköttum (VSK, GST, virðisaukaskattur) og staðgreiðslu. Það lýsir skattaútreikningsreglu, skatthlutfalli, skattabókhaldi, uppgjöri og öðrum hugtökum.

## <a name="templates"></a>Sniðmát

Skattaupplýsingar innihalda safn af einingaspjöldum sem virka saman á meðan samskipti við lánardrottna eru í gangi, eins og sýnt er í eftirfarandi töflu.

| Finance and Operations-smáforrit | Líkanadrifin forrit í Dynamics 365 | lýsing |
-------------------------|---------------------------------
Skattkóðar                   | msdyn\_taxcodes.md | 
Skattflokkar                 | msdyn\_taxgroups.md | 
Vöruskattflokkar             | msdyn\_taxitemgroups.md | 
Skattaundanþágur             | msdyn\_taxexemptcodes.md | 
Skattayfirvöld             | msdyn\_taxauthorities.md | 
Staðgreiðsluskattskóðar       | msdyn\_withholdingtaxcodes.md | 
Staðgreiðsluskattsflokkar     | msdyn\_withholdingtaxgroups.md | 
Fjárhagslykilshópur fyrir skatt | msdyn\_taxpostinggroups     | 

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

