---
title: Búðu til handvirkt myndaðar ráðleggingar
description: Þetta efni útskýrir hvernig söluaðilar geta búið til og stjórnað handbókum vörulista fyrir viðskiptavini Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e9ce8887f3cd7da0e250d3b0ffe96b222953de44
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965354"
---
# <a name="manually-create-curated-recommendations"></a>Búðu til handvirkt myndaðar ráðleggingar

[!include [banner](includes/banner.md)]

Þetta efni útskýrir hvernig söluaðilar geta búið til og stjórnað ráðleggingalista afurða fyrir viðskiptavini Microsoft Dynamics 365 Commerce.

Sérvaldir listar eru safn af einstöku efni sem fólk hefur búið til og sérvalið.  

## <a name="create-a-new-list"></a>Stofnið nýjan lista.

Til að stofna lista með sérvöldum afurðatillögum skal fylgja þessum skrefum.

1. Farðu í **Retail og Commerce &gt; Afurðatillögur &gt; Tillögulistar**.
1. Veljið **Nýtt**.
1. Í reitinn **Listakenni** skal slá inn gildi.
1. Í reitinn **Listaheiti** skal slá inn gildi.
    - **Listaheiti** er titill listans sem mun birtast í samanburðarlistanum í einingunni **Vörusafn**.
1. Til að bæta afurðum við listann skaltu velja **Bæta við afurðum**.
1. Til að breyta röð á vörum á listanum, sláðu inn gildi í dálkinum **Sýna röðun**.
    - Ef tvær vörur hafa sama gildi skjáraðar, þá getur endanleg röð þessara tveggja niðurstaðna verið frábrugðin bakforritinu.
1. Veldu **Vista** til að vista listann.

## <a name="example-list"></a>Dæmalisti

![Dæmi sérvalinn listi í bakforriti](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir afurðarráðleggingar](product-recommendations.md)

[Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi](enable-adls-environment.md)

[Virkja ráðleggingar um afurðir](enable-product-recommendations.md)

[Kveikja á sérsniðnum tillögum](personalized-recommendations.md)

[Afþakka sérsniðnar tillögur](personalization-gdpr.md)

[Virkja tillögur um að kaupa svipaða vöru](shop-similar-looks.md)

[Bæta við afurðatillögum á sölustað](product.md)

[Bæta tillögum við færsluskjáinn](add-recommendations-control-pos-screen.md)

[Aðlagaðu niðurstöður AI-ML](modify-product-recommendation-results.md)

[Búðu til tillögur með kynningargögnum](product-recommendations-demo-data.md)

[Algengar spurningar um afurðaráðleggingar](faq-recommendations.md)
