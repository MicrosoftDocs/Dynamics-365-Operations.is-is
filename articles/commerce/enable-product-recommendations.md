---
title: Virkja ráðleggingar um afurðir
description: Þetta efni útskýrir hvernig hægt er að gera tillögur um vörur sem byggjast á námi gervigreindarvélar (AI-ML) í boði fyrir viðskiptavini Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770140"
---
# <a name="enable-product-recommendations"></a>Virkja ráðleggingar um afurðir

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni útskýrir hvernig hægt er að gera tillögur um vörur sem byggjast á námi gervigreindarvélar (AI-ML) í boði fyrir viðskiptavini Microsoft Dynamics 365 Commerce. Nánari upplýsingar um afurðatillögur er að finna í [yfirliti yfir afurðatillögur í POS-skjölum](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Ráðleggingar fyrir skoðun
Áður en það er gert kleift, vinsamlegast hafðu í huga að afurðatillögur eru aðeins studdar fyrir viðskiptavini F&O sem styðja smíði 10.0.6 og hafa flutt geymslu sína með BDL. 

Að auki skal tryggja að RetailSale mælingar hafi verið gerðar virkar. Til að læra meira um þetta uppsetningarferli skaltu fara [hingað.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>Kveikja á tillögum

Til að kveikja á afurðatillögum skal fylgja þessum skrefum.

1. Farðu í **Retail** &gt; **Afurðatillögur** &gt; **Tillögufæribreytur**.
1. Á listanum yfir sameiginlegar færibreytur velurðu **Tillögulistar**.
1. Stillið valkostinn **Virkja tillögur** á **Já**.

![virkja afurðatillögur](./media/enableproductrecommendations.png)

> [!NOTE]
> Þetta ferli hefur ferlið við að mynda afurðatillögulista. Allt að nokkrar klukkustundir gætu verið nauðsynlegar áður en listarnir eru tiltækir og sjást á sölustað (POS) eða í Dynamics 365 for Commerce.

## <a name="configure-recommendation-list-parameters"></a>Stilla færibreytur tillögulista
Sjálfgefið er að AI-ML-byggðir afurðatillögulistar veiti leiðbeinandi gildi. Þú getur breytt sjálfgefnum gildum svo að þau henti flæði fyrirtækisins. Til að læra meira um hvernig eigi að breyta sjálfgefnum færibreytum skaltu fara í [Stjórna AI-ML-byggðum niðurstöðum afurðatillagna](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Sýna tillögur um POS tæki
Eftir að hafa gert tillögur í bakvinnslunni virkar verður að bæta tillöguglugganum við á POS skjánum með skipulagstólinu. Til að læra meira um þetta ferli skaltu fara [hingað.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir afurðarráðleggingar](product-recommendations.md)

[Bæta við listum með afurðartillögum við síður](add-reco-list-to-page.md)

[Bæta tillöguglugga við POS tæki](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


