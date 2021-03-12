---
title: Uppfæra staðalkostnað í framleiðsluumhverfis
description: Þessi skrá veitir leiðbeiningar um uppfærslu á stöðluðum kostnaði í framleiðsluumhverfi.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7bc203176967fbe6c20f4f687fe36fdcf3157b20
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983826"
---
# <a name="update-standard-costs-in-a-manufacturing-environment"></a>Uppfæra staðalkostnað í framleiðsluumhverfis

[!include [banner](../includes/banner.md)]

Þessi skrá veitir leiðbeiningar um uppfærslu á stöðluðum kostnaði í framleiðsluumhverfi. 

Uppfærslur geta endurspeglað nýjar vörur, kostnaðartegundir eða óbeinar formúlur kostnaðarútreiknings. Þeir geta einnig endurspeglað leiðréttingar og breytingar á kostnaði. Uppfærslugerðin mun hafa áhrif á þau skref sem eru nauðsynleg til að uppfæra staðalkostnað eins og sýnt er í eftirfarandi tilfellum.

-   Færið inn þær staðalkostnaðarbreytingar sem búist er við fyrir keyptar vörur og breytið svo stöðu kostnaðarfærslu vörunnar **í virkt** á viðeigandi dagsetningu. En ekki endurreikna samt kostnað framleiddra vara sem nota keyptu vörurnar.
-   Færið inn staðalkostnað fyrir nýja keypta vöru en ekki endurreikna kostnað framleiddra vara með uppskriftarútgáfu sem inniheldur keyptu vöruna sem þátt.
-   Leiðréttið eða breytið kostnaði keyptu vörunnar eða breytið kostnaðarflokknum sem er úthlutaður keyptu vörunni og reiknið út kostnað allra framleiddra vara með víxilsútgáfu sem inniheldur keyptu vöruna sem þátt.
-   Breytið kostnaði kostnaðartegundar og reiknið út kostnað allra framleiddra vara með leiðarútgáfu sem inniheldur leiðaraðgerðir sem nota kostnaðartegundina.
-   Breytið kostnaðartegundunum sem eru úthlutaðar leiðaraðgerðum eða kostnaðarflokknum sem er úthlutaður kostnaðartegundum. Reiknið síðan út kostnað allra framleiddra vara með leiðarútgáfu sem inniheldur leiðaraðgerðir sem nota kostnaðartegundina.
-   Breytið óbeinni jöfnu kostnaðarútreiknings og reiknið út kostnaðinn fyrir allar framleiddar vörur sem verða fyrir áhrifum vegna breytingarinnar.
-   Breytið eða bætið við framleiðslustað fyrir framleidda vöru og reiknið út framleiðslukostnað vörunnar fyrir staðinn.
-   Reiknið út (eða endurreiknið) kostnaðinn við framleidda vörur og endurreiknið kostnaðinn við allar framleiddar vörur með víxilútgáfu sem inniheldur framleiddu vöruna sem þátt.
-   Reiknið út kostnað við nýja framleidda vöru á grundvelli skilgreindra, samþykktra og virkra víxils- og leiðarupplýsinga.

Hvert tilfelli krefst ítarlegrar umhugsunar um það hvernig eigi að uppfæra staðalkostnað.



