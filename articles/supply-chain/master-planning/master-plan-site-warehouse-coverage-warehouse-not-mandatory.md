---
title: Aðaláætlanagerð fyrir svæðis og vöruhúsatryggingu, vöruhús ekki áskilið
description: Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði og vöruhús sem þakningarvíddir er áætluð. Vöruhúsavíddin er ekki skyldug.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e47531c75e54b23054464a5e1b1841eb2d82e093
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430073"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>Aðaláætlanagerð fyrir svæðis og vöruhúsatryggingu, vöruhús ekki áskilið

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði og vöruhús sem þakningarvíddir er áætluð. Vöruhúsavíddin er ekki skyldug.

Eftirfarandi aðstæður eru í þessu dæmi um aðaláætlunargerð:

-   Svæðavídd er stillt á áskilið og verður að færa inn á eftirspurnarfærslu. Ekki er hægt að breyta þessari stillingu.
-   Vöruhúsavíddin er ekki stillt sem skyldug. Vöruhúsið gæti verið þekkt en er ekki notað í útreikningi aðaláætlanagerðar.
-   Víddir svæða og vöruhúsa eru stilltar á þekjuáætlun. Aðrar víddir gætu einnig verið stilltar á þekjuáætlanir. Fjölsvæðiseiginleikinn hefur aftur á móti ekki áhrif á þær.

Eftirfarandi myndræn framsetning sýnir hvernig aðaláætlanagerð fer fram. Færibreyturnar sem vísað er í á myndinni og staðsetningar þeirra eru sem hér segir:
-   Vöruhúsið er stillt á Handvirkt. Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**. Á við **aðaláætlanagerð** flýtiflipa, sjá á **Handvirkt** svæði.
-   Vöruþekja er skilgreind fyrir vöruna. Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**. Veljið vöruna og svo á aðgerðarrúðu á flipanum **Áætlun** er smellt á **Vöruþekja**.
-   Áfyllingarvensl eru skilgreind fyrir vöruhúsið. Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**. Á flýtiflipanum **Aðaláætlanagerð** skal sjá reitahópur  **Aðalvöruhús**.
-   Sjálfgefin pöntunargerð er stillt á Framleiðslu, Innkaupapöntun eða Kanban. Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**. Veljið vöruna og svo á aðgerðarrúðu á flipanum **Áætlun** er smellt á **Sjálfgefnar pöntunarstillingar**. Í á **Sjálfgefnar pöntunarstillingar** skjámynd sjá **Sjálfgefin pöntunargerð**.

![Eftirspurn fyrir þekju svæðis og vöruhúss, vöruhús ekki skyldugt](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a>Frekari upplýsingar
--------

[Yfirlit yfir aðaláætlanir og virkni á mörgum svæðum](master-plan-multisite-functionality.md)

[Aðaláætlanagerð fyrir þekju svæðis, vöruhús áskilið](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Aðaláætlanagerð fyrir þekju svæðis og vöruhúss, vöruhús áskilið](master-plan-site-coverage-warehouse-mandatory.md)

[Aðaláætlanagerð fyrir þekju svæðis og vöruhúss, vöruhús ekki áskilið](master-plan-site-coverage-warehouse-not-mandatory.md)

[Uppskriftarútgáfa ákvörðuð](master-plan-bom-version-determined.md)



