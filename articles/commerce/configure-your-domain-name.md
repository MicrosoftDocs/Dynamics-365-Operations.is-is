---
title: Skilgreina lénsheiti
description: Þetta efni útskýrir hvernig á að stilla lén fyrir Microsoft Dynamics 365 netverslunarsíðu.
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
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
ms.openlocfilehash: 4db774783dba4b1cea9552da3cff29a9528bd496
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002175"
---
# <a name="configure-your-domain-name"></a>Skilgreina lénsheiti


[!include [banner](includes/banner.md)]

Þetta efni útskýrir hvernig á að stilla lén fyrir Microsoft Dynamics 365 netverslunarsíðu. 

## <a name="add-domains-during-e-commerce-initialization"></a>Bættu við lénum við frumstillingu netverslunar

Til að tengja lén við netverslunarumhverfi þitt skaltu frumstilla netverslun eins og lýst er í [Uppsetning á nýju vefsvæði fyrir netverslun](deploy-ecommerce-site.md). Við frumstilling er beðið um að upplýsingar séu látnar í té sem notaðar verða til að bjóða upp á netverslunarumhverfi þitt. Í reitnum **Studd hýsilnöfn** bætirðu við öllum lénum sem þú ætlar að nota með þessu umhverfi. Margfeldi lén ætti að aðgreina með semi-kommu. Með þessum hætti eru lénin skilgreind í öllum nauðsynlegum íhlutum netverslunar og þau eru tilbún til notkunar þegar þú skiptir úr umferð frá efnisbirtingarnetinu (CDN) eða netþjóninum og beinir henni á framvinnslu netverslunar.

## <a name="add-domains-after-e-commerce-initialization"></a>Bættu við lénum eftir frumstillingu netverslunar

Til að tengja ný lén við netverslunarumhverfi þitt eftir frumstillingu á netverslun verður þú að leggja fram þjónustubeiðni.

## <a name="additional-resources"></a>Frekari upplýsingar

[Uppsetning á nýju vefsvæði fyrir rafræn viðskipti](deploy-ecommerce-site.md)

[Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md)

[Tengja netsvæði við rás](associate-site-online-store.md)

[Stjórna robots.txt-skrám](manage-robots-txt-files.md)

[Setja upp sérsniðnar síður fyrir innskráningu notenda](custom-pages-user-logins.md)

[Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md)

[Virkja greiningu á verslun eftir staðsetningu](enable-store-detection.md)
