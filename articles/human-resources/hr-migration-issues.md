---
title: Dynamics 365 Human Resources innviðir sameina þekkt mál
description: Þessi grein sýnir vandamál sem geta komið upp meðan á Microsoft stendur Dynamics 365 Human Resources sameining innviða.
author: twheeloc
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 28c2c10a9293d00e26dfcc80ab08b89a122a6135
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2022
ms.locfileid: "9732772"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-known-issues"></a>Dynamics 365 Human Resources innviðir sameina þekkt mál

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="shared-dataverse-environments"></a>Deilt Dataverse umhverfi

Dual Write ramminn styður ekki að tengja tvö fjármála- og rekstrarforritsumhverfi við það sama Dataverse umhverfi. Ef þú ert með a Dataverse umhverfi sem er deilt með báðum eftirfarandi hlutum, verður þú annað hvort að afrita Dataverse umhverfi eða skiptu því:

- Fjármála- og rekstrarapp
- Núverandi mannauðsumhverfi

## <a name="environment-type-requirements"></a>Kröfur um gerð umhverfis

Eftirfarandi umhverfisgerðir eru nauðsynlegar áður en þú getur gert flutninginn:

- Ef þú ert ekki með neitt sjálfstætt sandkassaumhverfi, verður þú að búa til eitt til að staðfesta flutninginn.
- Ef þú ert með mörg sjálfstæð framleiðsluumhverfi er hægt að flytja eitt þeirra. Hafðu samband við þjónustudeild Microsoft til að merkja önnur umhverfi sem sandkassa.

## <a name="teams-integration"></a>Samþætting teyma

Núverandi mannauðsappið í Teams er nú fært yfir í a Microsoft Power Platform lausn. Frekari upplýsingar er að finna í [Forrit Human Resources í Teams](hr-admin-teams-leave-app.md).

## <a name="licensing"></a>Leyfisveiting

Engar breytingar eru á leyfisveitingum fyrir Dynamics 365 Human Resources á eftirfarandi sviðum: 

- **Lágmarksfjöldi kröfu um leyfiskaup**
- **Leyfi fyrir framleiðsluumhverfi og sandkassaumhverfi** – Ef þú ert með fyrirliggjandi sjálfstæð mannauðsleyfi sem innihalda eitt framleiðsluumhverfi og eitt sandkassaumhverfi, verður sami fjöldi leyfa tiltækur á fjármála- og rekstrarinnviðum.
- **Viðbótarsandkassaleyfi** – Ef þú hefur keypt viðbótarsandkassaleyfi fyrir sjálfstæða mannauðsforritið, verður sami fjöldi leyfa tiltækur fyrir sandkassaumhverfi á fjármála- og rekstrarinnviðum. 
