---
title: "Aðaláætlanagerð fyrir svæðistryggingu, vöruhús áskilið"
description: "Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði sem þakningarvídd er áætluð. Vöruhúsavíddin er skyldug."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 39f105bd1c6a6da4b73ae2a9c5657b15c6794ec0
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>Aðaláætlanagerð fyrir svæðistryggingu, vöruhús áskilið

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði sem þakningarvídd er áætluð. Vöruhúsavíddin er skyldug.

Eftirfarandi aðstæður eru í þessu dæmi um aðaláætlunargerð:

-   Svæðavídd er stillt á áskilið og verður að færa inn á eftirspurnarfærslu. Ekki er hægt að breyta þessari stillingu.
-   Vöruhúsavíddin er skyldug og hana þarf að færa inn í færslu eftirspurnar.
-   Svæðisvíddin er stillt á þekjuáætlun. Aðrar víddir gætu einnig verið stilltar á þekjuáætlanir. Fjölsvæðiseiginleikinn hefur aftur á móti ekki áhrif á þær.
-   Vöruhúsavíddin er ekki stillt á þekjuáætlanagerð. Þessvegna, framboð og eftirspurn safnast upp á staðsetningu, og hugsanlega, á öðrum víddum sem eru með tryggingaráætlun.

Eftirfarandi myndræn framsetning sýnir hvernig aðaláætlanagerð fer fram. Færibreyturnar sem vísað er í á myndinni og staðsetningar þeirra eru sem hér segir:
-   Vöruþekja er skilgreind fyrir vöruna. Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**. Veljið vöruna og smellið síðan á **Áætla &gt; Vöruþekja**.
-   Áfyllingarvensl eru skilgreind fyrir vöruhúsið. Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**. Á flýtiflipanum **Aðaláætlanagerð** skal sjá reitinn **Aðalvöruhús**.
-   Sjálfgefin pöntunargerð er stillt á Framleiðslu, Innkaupapöntun eða Kanban. Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**. Veldu vöruna og smelltu síðan á **Áætla &gt; Sjálfgefnar pöntunarstillingar**. Í á **Sjálfgefnar pöntunarstillingar** skjámynd sjá **Sjálfgefin pöntunargerð**.

![Eftirspurn fyrir þekju svæðis, vöruhús skyldugt](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a>Frekari upplýsingar
--------

[Áætlanagerð og fjölsvæðiseiginleikinn](master-plan-multisite-functionality.md)

[Aðaláætlanagerð - trygging svæðis og vöruhúss, vöruhús lögbundið](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Aðaláætlanagerð - trygging svæðis, vöruhús lögbundið](master-plan-site-coverage-warehouse-mandatory.md)

[Aðaláætlanagerð - trygging svæðis og vöruhúss, vöruhús ekki lögbundið](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Aðaláætlanagerð - Hvernig uppskriftaútgáfan er ákvörðuð](master-plan-bom-version-determined.md)




