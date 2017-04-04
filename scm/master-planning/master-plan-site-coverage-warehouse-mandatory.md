---
title: "Áætlanagerð fyrir þekju svæðis, vöruhús skyldugt"
description: "Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði sem þakningarvídd er áætluð. Vöruhúsavíddin er skyldug."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4c595aa9809e37ba752b76f559ef909c071eb303
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>Áætlanagerð fyrir þekju svæðis, vöruhús skyldugt

Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði sem þakningarvídd er áætluð. Vöruhúsavíddin er skyldug.

Eftirfarandi aðstæður eru í þessu dæmi um aðaláætlunargerð:

-   Svæðavídd er stillt á áskilið og verður að færa inn á eftirspurnarfærslu. Ekki er hægt að breyta þessari stillingu.
-   Vöruhúsavíddin er skyldug og hana þarf að færa inn í færslu eftirspurnar.
-   Svæðisvíddin er stillt á þekjuáætlun. Aðrar víddir gætu einnig verið stilltar á þekjuáætlanir. Fjölsvæðiseiginleikinn hefur aftur á móti ekki áhrif á þær.
-   Vöruhúsavíddin er ekki stillt á þekjuáætlanagerð. Þessvegna, framboð og eftirspurn safnast upp á staðsetningu, og hugsanlega, á öðrum víddum sem eru með tryggingaráætlun.

Eftirfarandi myndræn framsetning sýnir hvernig aðaláætlanagerð fer fram. Færibreyturnar sem vísað er í á myndinni og staðsetningar þeirra eru sem hér segir:
-   Vöruþekja er skilgreind fyrir vöruna. Smellið á **upplýsingar afurðastjórnun &gt;Afurðir&gt; Útgefnum afurðum**. Veljið vöruna og smellið síðan á **Áætlun &gt;Vöruþekja**.
-   Áfyllingarvensl eru skilgreind fyrir vöruhúsið. Smellt er á **Birgðastjórnun &gt;Uppsetningu &gt;niðurbrot &gt;Vöruhús**. Á flýtiflipanum **Aðaláætlanagerð** skal sjá reitinn **Aðalvöruhús**.
-   Sjálfgefin pöntunargerð er stillt á Framleiðslu, Innkaupapöntun eða Kanban. Smellið á **upplýsingar afurðastjórnun &gt;Afurðir&gt; Útgefnum afurðum**. Veljið vöruna og smellið síðan á **Áætlun &gt;Sjálfgefnar pöntunarstillingar**. Í á **Sjálfgefnar pöntunarstillingar** skjámynd sjá **Sjálfgefin pöntunargerð**.

![Eftirspurn fyrir þekju svæðis, vöruhús skyldugt](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="see-also"></a>Sjá einnig
--------

[Master planning and multisite functionality](master-plan-multisite-functionality.md)

[Aðaláætlanagerð - trygging svæðis og vöruhúss, vöruhús lögbundið](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Sniðmát fjárhagsáætlunargerðar - þekjuflokks setrið. vöruhús skyldugt](master-plan-site-coverage-warehouse-mandatory.md)

[Aðaláætlanagerð - trygging svæðis og vöruhúss, vöruhús ekki lögbundið](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Aðaláætlanagerð - Hvernig uppskriftaútgáfan er ákvörðuð](master-plan-bom-version-determined.md)


