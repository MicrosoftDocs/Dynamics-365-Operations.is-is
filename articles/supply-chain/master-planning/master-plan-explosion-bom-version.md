---
title: Niðurbrot uppskriftarútgáfu
description: Þessi grein útskýrir aðstæður aðaláætlanagerðar sem felur í sér niðurbrot uppskriftarútgáfu.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 482c036294f525be5db1dc6efefe76a9ba5b3ce5
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983696"
---
# <a name="explosion-of-a-bom-version"></a>Niðurbrot uppskriftarútgáfu

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir aðstæður aðaláætlanagerðar sem felur í sér niðurbrot uppskriftarútgáfu.

Niðurbrot eftirspurnar í uppskriftarútgáfunni býr til eftirspurn fyrir hverja uppskriftarlínuvöru við tiltekið svæði og mögulega við tiltekið vöruhús. Uppskrift sem á við um°tiltekið setur gæti haft tiltekið vöruhús skilgreint fyrir hverja uppskriftarlínu. Einnig ákvarða víddarstillingar vörunnar hvort vöruhúsið sé nauðsynlegt fyrir hverja uppskriftarlínu. Þessi eftirspurn sem eftir er fyrir hverja uppskriftarlínuvöru verður svo°að upphafspunkti fyrir aukaniðurbrot eftirspurnar. Eftirfarandi aðstæður eru í þessu dæmi um aðaláætlunargerð:

-   Svæðisvíddin er skylda og hana þarf að færa inn í færslu eftirspurnar.
-   Svæðisvíddin er samræmd. Þess vegna er svæðið fyrir neðra-stigs eftirspurn hið sama og svæðið í upprunalegu eftirspurnarfærslunni.

Eftirfarandi mynd sýnir framvindu niðurbrots eftirspurnar í aðaláætlunargerð. ![Niðurbrot eftirspurnar með útgáfu uppskriftar](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Uppskriftarútgáfa ákvörðuð](master-plan-bom-version-determined.md)

[Yfirlit yfir aðaláætlanir og virkni á mörgum svæðum](master-plan-multisite-functionality.md)



