---
title: Stigveldi fyrirtækis í Common Data Service
description: Þetta efni lýsir samþættingu stigveldisgagna milli forrita Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9a12ab249129dce24cdca5e29d737fa9f68c0eac
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572450"
---
# <a name="organization-hierarchy-in-common-data-service"></a>Stigveldi fyrirtækis í Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Vegna þess að Dynamics 365 Finance er fjármálakerfi er *fyrirtæki* kjarnahugtak og kerfisuppsetning byrjar með stillingu fyrirtækisstigveldis. Síðan er hægt að rekja fjárhag fyrirtækja á fyrirtækjastigi og einnig á hvaða stigi sem er í fyrirtækjastigveldinu.

Þó að Common Data Service sé ekki með hugtak fyrirtækjastigveldis er það með nokkur laus hugtök, svo sem heildarsölutekjur. Sem hluti af samþættingu Common Data Service er gagnaskipulag stigveldis fyrirtækis er bætt við Common Data Service.

## <a name="data-flow"></a>Gagnaflæði

Vistkerfi fyrirtækja sem samanstendur af forritum Finance and Operations og Common Data Service mun halda áfram að hafa stigveldi fyrirtækis. Þetta stigveldi fyrirtækis er byggt á forritum Finance and Operations, en það er útsett í Common Data Service í upplýsinga- og stækkunarlegum tilgangi. Eftirfarandi mynd sýnir upplýsingar um stigveldi fyrirtækis sem birtast í Common Data Service sem einstefnugagnaflæði úr forritum Finance and Operations til Common Data Service.

![Skipulagsmynd](media/dual-write-data-flow.png)

## <a name="templates"></a>Sniðmát

Einingakort yfir stigveldi fyrirtækis eru tiltæk fyrir samstillingu á einstefnu gagna úr forritum Finance and Operations til Common Data Service.

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a>Innri tilgangur í stigveldi fyrirtækja

Þetta sniðmát veitir aðra leiðina til samstillingar á tilgangseiningu fyrirtækjaskipulags úr Finance and Operations til annarra forrita Dynamics 365.

<!-- ![architecture image](media/dual-write-purpose.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
HIERARCHYTYPE | \> | msdyn\_hierarchypurposetypename
HIERARCHYTYPE | \> | msdyn\_hierarchytype.msdyn\_name
HIERARCHYPURPOSE | \>\> | msdyn\_hierarchypurpose
IMMUTABLE | \>\> | msdyn\_immutable
SETASDEFAULT | \>\> | msdyn\_setasdefault

## <a name="internal-organization-hierarchy-type"></a>Innri gerð fyrirtækisstigveldis

Þetta sniðmát veitir aðra leiðina til samstillingar á tilgangseiningu fyrirtækjaskipulags úr Finance and Operations til annarra forrita Dynamics 365.

<!-- ![architecture image](media/dual-write-type.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
HEITI | \> | msdyn\_name

## <a name="internal-organization-hierarchy"></a>Innra fyrirtækisstigveldi

Þetta sniðmát veitir aðra leiðina til samstillingar á birtri einingu fyrirtækjaskipulags úr Finance and Operations til annarra forrita Dynamics 365.

<!-- ![architecture image](media/dual-write-organization.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
VALIDTO | \> | msdyn\_validto
VALIDFROM | \> | msdyn\_validfrom
HIERARCHYTYPE | \> | msdyn\_hierarchytypename
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentpartyid
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childpartyid
HIERARCHYTYPE | \> | msdyn\_hierarchytypeid.msdyn\_name
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childid.msdyn\_partynumber
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentid.msdyn\_partynumber

## <a name="internal-organization"></a>Innra fyrirtæki

Upplýsingar um innra skipulag í Common Data Service koma úr tveimur einingum, **rekstrareiningu** og **lögaðilum**.

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a>Rekstrareining

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
LANGUAGEID | \> | msdyn\_languageid
NAMEALIAS | \> | msdyn\_namealias
HEITI | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
OPERATINGUNITTYPE | \>\> | msdyn\_type

### <a name="legal-entity"></a>Lögaðili

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
NAMEALIAS | \> | msdyn\_namealias
LANGUAGEID | \> | msdyn\_languageid
HEITI | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
none | \>\> | msdyn\_type
LEGALENTITYID | \> | msdyn\_companycode

## <a name="company"></a>Fyrirt.

Veitir tvíátta samstillingu upplýsinga um lögaðila (fyrirtæki) milli Finance and Operations og annarra forrita Dynamics 365.

<!-- ![architecture image](media/dual-write-company.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
HEITI | = | cdm\_name
LEGALENTITYID | = | cdm\_companycode
