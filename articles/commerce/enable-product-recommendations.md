---
title: Virkja ráðleggingar um afurðir
description: Þetta efnisatriði útskýrir hvernig á að gera afurðatillögur sem byggja á vélnám gervigreindar (AI-ML) í boði fyrir Microsoft Dynamics 365 Commerce viðskiptavini.
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
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
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bfecc53a17eb44c5726103b4df738d6c6b0311aec07ad8eab55fa9c94787957a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752484"
---
# <a name="enable-product-recommendations"></a>Virkja ráðleggingar um afurðir

[!include [banner](includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að gera afurðatillögur sem byggja á vélnám gervigreindar (AI-ML) í boði fyrir Microsoft Dynamics 365 Commerce viðskiptavini. Nánari upplýsingar um afurðatillögur er að finna í [yfirliti yfir afurðatillögur í POS-skjölum](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Ráðleggingar fyrir skoðun

Áður en er virkjað skal hafa í huga að afurðartillögur eru aðeins studdar fyrir Commerce-viðskiptavini sem hafa flutt geymsluna sína til að nota Azure Data Lake Storage. 

Eftirfarandi stillingar verða að vera gerðar virkar í bakvinnslunni áður en ráðleggingar eru virkjaðar:

1. Gakktu úr skugga um að Azure Data Lake Storage hafi verið keypt og staðfest í umhverfinu. Frekari upplýsingar er að finna í [Gakktu úr skugga um að Azure Data Lake Storage hafi verið keypt og staðfest í umhverfinu](enable-ADLS-environment.md).
2. Ganga úr skugga um að endurnýjun einingaverslunarinnar hafi verið gerð sjálfvirk. Fyrir frekari upplýsingar, sjá [Ganga úr skugga um að endurnýjun einingaverslunarinnar hafi verið sjálfvirk](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
3. Staðfestu að Azure AD auðkennisstilling innihaldi færslu fyrir tillögur. Nánari upplýsingar um framkvæmd þessarar aðgerðar eru hér að neðan.

Að auki skal tryggja að RetailSale mælingar hafi verið gerðar virkar. Til að læra meira um þetta uppsetningarferli, sjá [Vinna með mælingar](/dynamics365/ai/customer-insights/pm-measures).

## <a name="azure-ad-identity-configuration"></a>Azure AD auðkennisskilgreining

Þetta skref er nauðsynlegt fyrir alla viðskiptavini sem reka innra skipulag sem þjónustustillingu (IaaS). Fyrir viðskiptavini sem keyra á Service Fabric (SF) ætti þetta skref að vera sjálfvirkt og við mælum með að staðfesta að stillingin sé stillt eins og vænst er.

### <a name="setup"></a>Setja upp

1. Úr bakvinnslunni leitarðu að síðunni **Azure Active Directory forrit**.
2. Staðfestu hvort færsla sé fyrir hendi fyrir „RecommendationSystemApplication-1“.

Ef færslan er ekki til skaltu bæta við nýrri færslu með eftirfarandi upplýsingum:

- **Biðlarakenni** - d37b07e8-dd1c-4514-835d-8b918e6f9727
- **Heiti** - RecommendationSystemApplication-1
- **Notandakenni** - RetailServiceAccount

Vistið og lokið síðunni. 

## <a name="turn-on-recommendations"></a>Kveikja á tillögum

Til að kveikja á afurðatillögum skal fylgja þessum skrefum.

1. Í Commerce Headquarters skal leita að **Eiginleikastjórnun**.
1. Veljið **Allir** til að sjá lista yfir tiltæka eiginleika. 
1. Í leitarreitnum skal slá inn **Ráðleggingar**.
1. Veljið eiginleikann **Afurðaráðleggingar**.
1. Á eiginleikasvæðinu **Afurðaráðleggingar** skal velja **Virkja núna**.

![Kveikt á tillögum.](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> Þetta ferli hefur ferlið við að mynda afurðatillögulista. Það getur tekið nokkrar klukkustundir áður en listarnir verða tiltækir og sjást á sölustað (POS) eða í Dynamics 365 Commerce.

## <a name="configure-recommendation-list-parameters"></a>Stilla færibreytur tillögulista

Sjálfgefið er að AI-ML-byggðir afurðatillögulistar veiti leiðbeinandi gildi. Þú getur breytt sjálfgefnum gildum svo að þau henti flæði fyrirtækisins. Til að læra meira um hvernig eigi að breyta sjálfgefnum færibreytum skaltu fara í [Stjórna AI-ML-byggðum niðurstöðum afurðatillagna](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Sýna tillögur um POS tæki

Eftir að hafa gert tillögur í bakvinnslu Commerce virkar verður að bæta tillöguglugganum við á POS skjánum með skipulagstólinu. Til að fræðast um þetta ferli, sjá [Bættu ráðleggingastjórnun við viðskiptaskjáinn á POS tækjum](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Kveikja á sérsniðnum tillögum

Í Dynamics 365 Commerce geta smásalar gert persónulegar ráðleggingar um vörur (einnig þekktar sem persónugervingar) tiltækar. Þannig er hægt að fella persónulegar ráðleggingar inn í upplifun viðskiptavina á netinu og á sölustað. Þegar kveikt er á sérstillingaraðgerðinni getur kerfið tengt kaup notanda og vöruupplýsingar til að búa til sérsniðnar ráðleggingar um vöru.

Til að læra meira um persónulegar ráðleggingar, sjá [Virkja persónulegar ráðleggingar](personalized-recommendations.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir afurðarráðleggingar](product-recommendations.md)

[Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi](enable-adls-environment.md)

[Kveikja á sérsniðnum tillögum](personalized-recommendations.md)

[Virkja tillögur um að kaupa svipaða vöru](shop-similar-looks.md)

[Afþakka sérsniðnar tillögur](personalization-gdpr.md)

[Bæta afurðaráðleggingum við sölustað](product.md)

[Bæta við tillögum á færsluskjáinn](add-recommendations-control-pos-screen.md)

[Aðlagaðu niðurstöður AI-ML](modify-product-recommendation-results.md)

[Búðu til handvirkt myndaðar ráðleggingar](create-editorial-recommendation-lists.md)

[Búðu til tillögur með kynningargögnum](product-recommendations-demo-data.md)

[Algengar spurningar um afurðaráðleggingar](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]