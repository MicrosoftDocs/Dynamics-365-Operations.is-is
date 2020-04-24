---
title: Virkja ráðleggingar um afurðir
description: Þetta efni útskýrir hvernig hægt er að gera tillögur um vörur sem byggjast á námi gervigreindarvélar (AI-ML) í boði fyrir viðskiptavini Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
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
ms.openlocfilehash: d38d7b0e98d84e23d7a51c5d8ee65df4a3b9e4a7
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259795"
---
# <a name="enable-product-recommendations"></a>Virkja ráðleggingar um afurðir

[!include [banner](includes/banner.md)]

Þetta efni útskýrir hvernig hægt er að gera tillögur um vörur sem byggjast á námi gervigreindarvélar (AI-ML) í boði fyrir viðskiptavini Microsoft Dynamics 365 Commerce. Nánari upplýsingar um afurðatillögur er að finna í [yfirliti yfir afurðatillögur í POS-skjölum](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Ráðleggingar fyrir skoðun

Áður en virkjun er gerð skal hafa í huga að afurðatillögur eru aðeins studdar fyrir viðskiptavini Commerce sem hafa flutt geymslu sína með Azure Data Lake Storage (ADLS). 

Eftirfarandi stillingar verða að vera gerðar virkar í bakvinnslunni áður en ráðleggingar eru virkjaðar:

1. Ganga úr skugga um að ADLS hafi verið keypt og staðfest með góðum árangri í umhverfinu. Nánari upplýsingar er að finna í [Ganga úr skugga um að ADLS hafi verið keypt og staðfest með góðum árangri í umhverfinu](enable-ADLS-environment.md).
2. Ganga úr skugga um að endurnýjun einingaverslunarinnar hafi verið gerð sjálfvirk. Fyrir frekari upplýsingar, sjá [Ganga úr skugga um að endurnýjun einingaverslunarinnar hafi verið sjálfvirk](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
3. Staðfestu að Azure AD auðkennisstilling innihaldi færslu fyrir tillögur. Nánari upplýsingar um framkvæmd þessarar aðgerðar eru hér að neðan.

Að auki skal tryggja að RetailSale mælingar hafi verið gerðar virkar. Til að læra meira um þetta uppsetningarferli, sjá [Vinna með mælingar](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).

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

1. Farðu í **Retail og Commerce &gt; Afurðatillögur &gt; Færibreytur tillögulista**.
1. Á listanum yfir sameiginlegar færibreytur velurðu **Tillögulistar**.
1. Stillið valkostinn **Virkja tillögur** á **Já**.

![Kveikt á tillögum](./media/enablepersonalization.png)

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

[Virkja ADLS í Dynamics 365 Commerce umhverfi](enable-adls-environment.md)

[Kveikja á sérsniðnum tillögum](personalized-recommendations.md)

[Afþakka sérsniðnar tillögur](personalization-gdpr.md)

[Bæta afurðaráðleggingum við sölustað](product.md)

[Bæta við tillögum á færsluskjáinn](add-recommendations-control-pos-screen.md)

[Aðlagaðu niðurstöður AI-ML](modify-product-recommendation-results.md)

[Búðu til handvirkt myndaðar ráðleggingar](create-editorial-recommendation-lists.md)

[Búðu til tillögur með kynningargögnum](product-recommendations-demo-data.md)

[Algengar spurningar um afurðaráðleggingar](faq-recommendations.md)

