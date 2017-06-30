---
title: "Aðaláætlanagerð fyrir svæðis og vöruhúsatryggingu, vöruhús ekki áskilið"
description: "Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði og vöruhús sem þakningarvíddir er áætluð. Vöruhúsavíddin er ekki skyldug."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ec5150abd297a7c00ac180db581adb30bef65b3f
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>Aðaláætlanagerð fyrir svæðis og vöruhúsatryggingu, vöruhús ekki áskilið

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði og vöruhús sem þakningarvíddir er áætluð. Vöruhúsavíddin er ekki skyldug.

Eftirfarandi aðstæður eru í þessu dæmi um aðaláætlunargerð:

-   Svæðavídd er stillt á áskilið og verður að færa inn á eftirspurnarfærslu. Ekki er hægt að breyta þessari stillingu.
-   Vöruhúsavíddin er ekki stillt sem skyldug. Vöruhúsið gæti verið þekkt en er ekki notað í útreikningi aðaláætlanagerðar.
-   Víddir svæða og vöruhúsa eru stilltar á þekjuáætlun. Aðrar víddir gætu einnig verið stilltar á þekjuáætlanir. Fjölsvæðiseiginleikinn hefur aftur á móti ekki áhrif á þær.

Eftirfarandi myndræn framsetning sýnir hvernig aðaláætlanagerð fer fram. Færibreyturnar sem vísað er í á myndinni og staðsetningar þeirra eru sem hér segir:
-   Vöruhúsið er stillt á Handvirkt. Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**. Á við **aðaláætlanagerð** flýtiflipa, sjá á **Handvirkt** svæði.
-   Vöruþekja er skilgreind fyrir vöruna. Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**. Veljið vöruna og svo á aðgerðarrúðu á flipanum **Áætlun** er smellt á **Vöruþekja**.
-   Áfyllingarvensl eru skilgreind fyrir vöruhúsið. Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**. Á flýtiflipanum **Aðaláætlanagerð** skal sjá reitahópur  **Aðalvöruhús**.
-   Sjálfgefin pöntunargerð er stillt á Framleiðslu, Innkaupapöntun eða Kanban. Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**. Veljið vöruna og svo á Aðgerðarrúða á flipa **Áætlun** er smellt á **Sjálfgefnar pöntunarstillingar** Í á **Sjálfgefnar pöntunarstillingar** skjámynd sjá **Sjálfgefin pöntunargerð**.

![Eftirspurn fyrir þekju svæðis og vöruhúss, vöruhús ekki skyldugt](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)

 
-



<a name="see-also"></a>Sjá einnig
--------

[Áætlanagerð og fjölsvæðiseiginleikinn](master-plan-multisite-functionality.md)

[Aðaláætlanagerð - trygging svæðis og vöruhúss, vöruhús lögbundið](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Aðaláætlanagerð - trygging svæðis, vöruhús lögbundið](master-plan-site-coverage-warehouse-mandatory.md)

[Aðaláætlanagerð- trygging svæðis,  vöruhús ekki lögbundið](master-plan-site-coverage-warehouse-not-mandatory.md)

[Aðaláætlanagerð - Hvernig uppskriftaútgáfan er ákvörðuð](master-plan-bom-version-determined.md)




