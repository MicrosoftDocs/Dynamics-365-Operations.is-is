---
title: Aðaláætlanagerð fyrir svæðistryggingu, vöruhús áskilið
description: Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði sem þakningarvídd er áætluð. Vöruhúsavíddin er skyldug.
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
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72240e7db8ec914220cb8f8f1185a91a304ff66b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977964"
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

[Yfirlit yfir aðaláætlanir og virkni á mörgum svæðum](master-plan-multisite-functionality.md)

[Aðaláætlanagerð fyrir þekju svæðis og vöruhúss, vöruhús áskilið](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Aðaláætlanagerð fyrir þekju svæðis, vöruhús áskilið](master-plan-site-coverage-warehouse-mandatory.md)

[Aðaláætlanagerð fyrir þekju svæðis og vöruhúss, vöruhús ekki áskilið](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Uppskriftarútgáfa ákvörðuð](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]