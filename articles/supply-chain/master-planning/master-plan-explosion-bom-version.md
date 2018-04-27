---
title: "Niðurbrot uppskriftarútgáfu"
description: "Þessi grein útskýrir aðstæður aðaláætlanagerðar sem felur í sér niðurbrot uppskriftarútgáfu."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0f852c8d100c91d055e58c4594106aedf6fe5afb
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="explosion-of-a-bom-version"></a>Niðurbrot uppskriftarútgáfu

[!INCLUDE [banner](../includes/banner.md)]

Þessi grein útskýrir aðstæður aðaláætlanagerðar sem felur í sér niðurbrot uppskriftarútgáfu.

Niðurbrot eftirspurnar í uppskriftarútgáfunni býr til eftirspurn fyrir hverja uppskriftarlínuvöru við tiltekið svæði og mögulega við tiltekið vöruhús. Uppskrift sem á við um°tiltekið setur gæti haft tiltekið vöruhús skilgreint fyrir hverja uppskriftarlínu. Einnig ákvarða víddarstillingar vörunnar hvort vöruhúsið sé nauðsynlegt fyrir hverja uppskriftarlínu. Þessi eftirspurn sem eftir er fyrir hverja uppskriftarlínuvöru verður svo°að upphafspunkti fyrir aukaniðurbrot eftirspurnar. Eftirfarandi aðstæður eru í þessu dæmi um aðaláætlunargerð:

-   Svæðisvíddin er skylda og hana þarf að færa inn í færslu eftirspurnar.
-   Svæðisvíddin er samræmd. Þess vegna er svæðið fyrir neðra-stigs eftirspurn hið sama og svæðið í upprunalegu eftirspurnarfærslunni.

Eftirfarandi mynd sýnir framvindu niðurbrots eftirspurnar í aðaláætlunargerð. ![Niðurbrot eftirspurnar með útgáfu uppskriftar](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="see-also"></a>Sjá einnig
--------

[Aðaláætlanagerð - Hvernig uppskriftaútgáfan er ákvörðuð](master-plan-bom-version-determined.md)

[Áætlanagerð og fjölsvæðiseiginleikinn](master-plan-multisite-functionality.md)




