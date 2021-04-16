---
title: Samþættur skattur
description: Þetta efni lýsir samþættingu skattaupplýsinga milli Finance and Operations og Dataverse.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a7992520b57b4c19b6dc8e13bd8e9ffc87b40f5a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750643"
---
# <a name="integrated-tax"></a>Samþættur skattur

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Skattuppsetningargögn skilgreina uppsetningu bæði á óbeinum sköttum (VSK, GST, virðisaukaskattur) og staðgreiðslu. Það lýsir skattaútreikningsreglu, skatthlutfalli, skattabókhaldi, uppgjöri og öðrum hugtökum.

## <a name="templates"></a>Sniðmát

Skattagögn innihalda safn af töflukortum sem vinna saman í gagnasamskiptum, eins og sýnt er í eftirfarandi töflu.

Finance and Operations-smáforrit | Líkanadrifin forrit í Dynamics 365 | lýsing |
-------------------------|---------------------------------|----|
VSK-flokkur vöru | msdyn_taxitemgroups |
Skattayfirvöld | msdyn_taxauthorities |
Eining undanþágukóða virðisaukaskatts fyrir CDS | msdyn_taxexemptcodes |
VSK-flokkar | msdyn_taxgroups |
Fjárhagsbókunarflokkar virðisaukaskatts V2 | msdyn_taxpostinggroups |
Staðgreiðsluskattskóðar | msdyn_withholdingtaxcodes |
Staðgreiðsluskattsflokkar | msdyn_withholdingtaxgroups | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]