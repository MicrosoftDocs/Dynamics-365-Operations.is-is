---
title: Aðaláætlanagerð fyrir svæðistryggingu, vöruhús ekki áskilið
description: Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði sem þakningarvídd er áætluð.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e94deffb928704ff96491174a7bf31a823c7a38d
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357072"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Aðaláætlanagerð fyrir svæðistryggingu, vöruhús ekki áskilið

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig vöru sem hefur svæði sem þakningarvídd er áætluð.

Eftirfarandi aðstæður eru í þessu dæmi um aðaláætlunargerð:

-   Svæðavídd er stillt á áskilið og verður að færa inn á eftirspurnarfærslu.
-   Vöruhúsavíddin er ekki stillt sem skyldug. Vöruhúsið gæti verið þekkt en er ekki notað í útreikningi aðaláætlanagerðar.
-   Svæðisvíddin er stillt á þekjuáætlun.
-   Vöruhúsavíddin er ekki stillt á þekjuáætlanagerð. Þessvegna, framboð og eftirspurn safnast upp á staðsetningu, og hugsanlega, á öðrum víddum sem eru með tryggingaráætlun.

Eftirfarandi myndræn framsetning sýnir hvernig aðaláætlanagerð fer fram. Færibreyturnar sem vísað er í á myndinni og staðsetningar þeirra eru sem hér segir:
-   Vöruþekja er skilgreind fyrir vöruna. Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**. Veljið vöruna og smellið síðan á **Áætla &gt; Vöruþekja**.
-   Áfyllingarvensl eru skilgreind fyrir vöruhúsið. Smellið á **Birgðastjórnun &gt; Uppsetning &gt; Niðurbrot birgða &gt; Vöruhús**. Á flýtiflipanum **Aðaláætlanagerð** skal sjá reitinn **Aðalvöruhús**.
-   Sjálfgefin pöntunargerð er stillt á Framleiðslu, Innkaupapöntun eða Kanban. Smellið á **Upplýsingastjórnun afurða &gt; Afurðir&gt; Losaðar afurðir**. Veldu vöruna og smelltu síðan á **Áætla &gt; Sjálfgefnar pöntunarstillingar**. Í skjámyndinni **Sjálfgefnar pöntunarstillingar** er að finna reitinn **Sjálfgefin pöntunargerð**.

![Eftirspurn eftir þekju svæðis, vöruhús ekki skyldugt.](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir aðaláætlanir og virkni á mörgum svæðum](master-plan-multisite-functionality.md)

[Aðaláætlanagerð fyrir þekju svæðis og vöruhúss, vöruhús áskilið](master-plan-site-coverage-warehouse-mandatory.md)

[Aðaláætlanagerð fyrir þekju svæðis, vöruhús áskilið](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Aðaláætlanagerð fyrir þekju svæðis, vöruhús ekki áskilið](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Uppskriftarútgáfa ákvörðuð](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]