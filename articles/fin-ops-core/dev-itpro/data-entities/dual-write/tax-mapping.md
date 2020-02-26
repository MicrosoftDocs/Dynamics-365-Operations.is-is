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
ms.openlocfilehash: 0d32a5f7859f0200da823a73d94b9a6b2a9c8e7d
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019836"
---
# <a name="integrated-tax"></a>Samþættur skattur

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Skattuppsetningargögn skilgreina uppsetningu bæði á óbeinum sköttum (VSK, GST, virðisaukaskattur) og staðgreiðslu. Það lýsir skattaútreikningsreglu, skatthlutfalli, skattabókhaldi, uppgjöri og öðrum hugtökum.

## <a name="templates"></a>Sniðmát

Skattaupplýsingar innihalda safn af einingaspjöldum sem virka saman á meðan samskipti við lánardrottna eru í gangi, eins og sýnt er í eftirfarandi töflu.

Finance and Operations   | Önnur Dynamics 365 forrit
-------------------------|---------------------------------
Skattkóðar                  | msdyn\_taxcodes.md
Skattflokkar               | msdyn\_taxgroups.md
Vöruskattflokkar          | msdyn\_taxitemgroups.md
Skattaundanþágur           | msdyn\_taxexemptcodes.md
Skattayfirvöld          | msdyn\_taxauthorities.md
Staðgreiðsluskattskóðar      | msdyn\_withholdingtaxcodes.md
Staðgreiðsluskattsflokkar   | msdyn\_withholdingtaxgroups.md
Fjárhagslykilshópur fyrir skatt | msdyn\_taxpostinggroups  

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

