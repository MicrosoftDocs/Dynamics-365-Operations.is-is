---
title: Skilgreina lénsheiti
description: Þessi grein útskýrir hvernig á að stilla lén fyrir a Microsoft Dynamics 365 netverslunarsíða.
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 00c75581ba08979dfbc784f949c30b9bf78d44c9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892132"
---
# <a name="configure-your-domain-name"></a>Skilgreina lénsheiti


[!include [banner](includes/banner.md)]

Þessi grein útskýrir hvernig á að stilla lén fyrir a Microsoft Dynamics 365 netverslunarsíða. 

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