---
title: Setja upp þróunarumhverfi rafrænna viðskipta til að kemba lag 1 af sýndarvél Retail Server
description: Þessi grein útskýrir hvernig á að setja upp þróunarumhverfi fyrir rafræn viðskipti til að villuleita gegn sýndarvél á Tier 1 Retail Server (VM).
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7cc6c936c67bc82da1a237341ac07fb69d4ac233
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855703"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a>Setja upp þróunarumhverfi rafrænna viðskipta til að kemba lag 1 af sýndarvél Retail Server

[!include [banner](../../includes/banner.md)]

Þessi grein útskýrir hvernig á að setja upp þróunarumhverfi fyrir rafræn viðskipti til að villuleita gegn sýndarvél á Tier 1 Retail Server (VM).

## <a name="description"></a>lýsing

Lag 1 umhverfi Microsoft Dynamics 365 Commerce eru yfirleitt notuð fyrir Commerce Runtime (CRT) og þróun á viðbót sölustaðar (POS). Þetta eru sjálfstæð umhverfi. Vegna þess að hönnunin er af eðli SaaS-þjónustu inniheldur hún ekki þætti rafrænna viðskipta.

Í sumum aðstæðum gæti verið sniðugt að prófa köll á viðbætur á umhverfislag 1 svo hægt sé að kemba viðbætur úr þáttum rafrænna viðskipta. Almennar leiðbeiningar er að finna í [Kemba með hliðsjón af þróunarumhverfislag 1 í Commerce](../e-commerce-extensibility/debug-tier-1.md).

Þegar umhverfislag 1 er kembt, vegna þess að svæðið kallar nú á annað Retail Server, gætu köll milli þjóna valdið ýmsum villum sem tengjast öryggisreglu efnisins.

Eftirfarandi mynd sýnir dæmi um villu sem gæti komið upp þegar afbrigði er valið á upplýsingasíðu afurðar.

![Villa þegar afbrigði er valið á upplýsingasíðu afurðar.](media/unhandled-rejection-error.jpg)

Eftirfarandi mynd sýnir dæmi um svipaða villu í verkfærum kembiforrits í vafra (F12 forritunarverkfæri). Villuboðin minnast á brot á öryggisleiðbeiningu efnisins.

![Villa í verkfærum kembiforrits.](media/debugger-tools-error.JPG)

## <a name="resolution"></a>Lausn

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a>Gera öryggisreglu efnis óvirka fyrir svæðið í vefsmið Commerce

1. Veljið svæðið sem unnið er á.
1. Veljið **Stillingar** og veljið síðan **Viðbætur**.
1. Í flipanum **Öryggisregla efnis** skal velja **Gera öryggisreglu efnis óvirka**.
1. Veljið **Vista og birta**.

> [!NOTE]
> B2C-innskráning virkar ekki í staðbundnu þróunarumhverfi. Hins vegar er hægt að nota greiðsluferli gesta eða smíða gervisíður til að hvetja til innskráningar notanda eins og þörf er á.

## <a name="additional-resources"></a>Frekari upplýsingar

[Hafist handa með stækkunarhæfni rafrænna viðskipta á netinu](../e-commerce-extensibility/sdk-getting-started.md)

[Stjórna öryggisreglu fyrir efni (CSP) á svæði fyrir rafræn viðskipti](../manage-csp.md)
