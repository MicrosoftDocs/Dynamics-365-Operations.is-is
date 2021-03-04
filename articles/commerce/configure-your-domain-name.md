---
title: Skilgreina lénsheiti
description: Þetta efni útskýrir hvernig á að stilla lén fyrir Microsoft Dynamics 365 netverslunarsíðu.
author: psimolin
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ac1b0c8baaddd6ca62cc49657fff364df21c14f2
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517124"
---
# <a name="configure-your-domain-name"></a>Skilgreina lénsheiti


[!include [banner](includes/banner.md)]

Þetta efni útskýrir hvernig á að stilla lén fyrir Microsoft Dynamics 365 netverslunarsíðu. 

## <a name="add-domains-during-e-commerce-initialization"></a>Bæta lénum við frumstillingu á e-Commerce

Til að tengja lén við Dynamics 365 Commerce rafrænt viðskiptaumhverfi skal ræsa e-Commerce eins og lýst er í [Uppsetning á nýjum leigjanda rafrænna viðskipta](deploy-ecommerce-site.md). Í frumstillingu er beðið um upplýsingar sem verða notaðar til að úthluta rafræna viðskiptaumhverfinu. Í reitnum **Studd hýsilnöfn** bætirðu við öllum lénum sem þú ætlar að nota með þessu umhverfi. Margfeldi lén ætti að aðgreina með semi-kommu. Á þennan hátt eru lén skilgreind í öllum nauðsynlegum Commerce-íhlutum og þau eru tilbúin til notkunar þegar umferð er færð frá afhendingarneti notanda (CDN) eða vefþjóni og beint í framenda rafrænna e-Commerce.

## <a name="add-domains-after-e-commerce-initialization"></a>Bæta við lénum eftir frumstillingu e-Commerce

Þú verður að leggja fram þjónustubeiðni til að tengja ný lén við rafrænt viðskiptaumhverfi eftir ræsingu e-Commerce

## <a name="additional-resources"></a>Frekari upplýsingar

[Uppsetning á nýjum leigjanda rafrænna viðskipta](deploy-ecommerce-site.md)

[Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md)

[Tengja svæði Dynamics 365 Commerce við netrás](associate-site-online-store.md)

[Vinna með skrárnar robots.txt](manage-robots-txt-files.md)

[Hlaða upp mörgum URL-framsendingum í einu](upload-bulk-redirects.md)

[Setja upp B2C-leigjanda í Commerce](set-up-B2C-tenant.md)

[Setja upp sérsniðnar síður fyrir innskráningu notenda](custom-pages-user-logins.md)

[Stilla marga B2C leigjendur í viðskiptaumhverfi](configure-multi-B2C-tenants.md)

[Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md)

[Virkja greiningu á verslun eftir staðsetningu](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]