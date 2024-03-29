---
title: Virkja ráðleggingar um afurðir
description: Þessi grein útskýrir hvernig á að gera ráðleggingar um vörur sem byggjast á gervigreind-vélanámi (AI-ML) aðgengilegar fyrir Microsoft Dynamics 365 Commerce viðskiptavinum.
author: bebeale
ms.date: 09/08/2022
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
ms.openlocfilehash: fc1b43fa70e6652d38b1141e2d93cf323f70a756
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460022"
---
# <a name="enable-product-recommendations"></a>Virkja ráðleggingar um afurðir

[!include [banner](includes/banner.md)]

Þessi grein útskýrir hvernig á að gera ráðleggingar um vörur sem byggjast á gervigreind-vélanámi (AI-ML) aðgengilegar fyrir Microsoft Dynamics 365 Commerce viðskiptavinum. Nánari upplýsingar um afurðatillögur er að finna í [yfirliti yfir afurðatillögur í POS-skjölum](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Ráðleggingar fyrir skoðun

1. Gakktu úr skugga um að þú sért með gilt leyfi fyrir Dynamics 365 Commerce tillögur.
1. Gakktu úr skugga um að einingaverslunin sé tengd við Azure Data Lake Storage Gen2 reikning í eigu viðskiptavinar. Frekari upplýsingar er að finna í [Gakktu úr skugga um að Azure Data Lake Storage hafi verið keypt og staðfest í umhverfinu](enable-ADLS-environment.md).
1. Staðfestu að Azure AD auðkennisstilling innihaldi færslu fyrir tillögur. Nánari upplýsingar um framkvæmd þessarar aðgerðar eru hér að neðan.
1. Gakktu úr skugga um að dagleg uppfærsla einingaverslunar í Azure Data Lake Storage Gen2 hafi verið tímasett. Fyrir frekari upplýsingar, sjá [Ganga úr skugga um að endurnýjun einingaverslunarinnar hafi verið sjálfvirk](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
1. Virkja mælingar RetailSale fyrir einingaverslun. Frekari upplýsingar um uppsetningu þessa ferlis er að finna í [Vinna með mælingar](/dynamics365/ai/customer-insights/pm-measures).
1. Gakktu úr skugga um að umhverfið þitt hafi stillt framreiðslu- og eldunarsvæðin á þeim svæðum sem nú eru studd, eins og hér segir:

    - **Stuðstuð eldunarsvæði:** ESB/US/CA/AU.
    - **Stuðningssvæði fyrir þjónustu:** BNA/CA/AU. Ef afgreiðslusvæðið passar ekki við eitt af núverandi studdu svæðum, mun meðmælaþjónustan velja næst studda afgreiðslusvæðið.

Að loknum ofangreindum skrefum er allt til reiðu til að virkja tillögur.

> [!NOTE]
> Það er þekkt vandamál þar sem ráðleggingar birtast ekki eftir að eftirfarandi skrefum er lokið. Þetta vandamál stafar af vandamálum í gagnaflæði í umhverfinu. Ef umhverfið þitt sýnir ekki niðurstöður tilmæla skaltu stilla önnur gögn fyrir meðmælaþjónustuna með því að fylgja skrefunum í [Settu upp annað gagnaflæði fyrir tillögur](set-up-alternate-data-flow.md). Þú verður að hafa Azure stjórnandaheimildir til að ljúka þessum skrefum. Ef þú þarft aðstoð, hafðu samband við FastTrack fulltrúa þinn.

## <a name="azure-ad-identity-configuration"></a>Azure AD auðkennisskilgreining

Þetta skref er aðeins nauðsynlegt fyrir viðskiptavini sem keyra innviði sem þjónustu (IaaS) uppsetningu. Azure AD auðkennisstilling er sjálfvirk fyrir viðskiptavini sem keyra á Azure Service Fabric, en við mælum með að þú staðfestir að stillingin sé stillt eins og búist var við.

### <a name="setup"></a>Uppsetning

1. Í Commerce Headquarters skal leita að síðunni **Azure Active Directory forrit**.
1. Athugaðu hvort færsla sé fyrir hendi fyrir **RecommendationSystemApplication-1**. Ef færsla er ekki til skaltu búa til eina með því að nota eftirfarandi upplýsingar:

    - **Auðkenni biðlara**: d37b07e8-dd1c-4514-835d-8b918e6f9727
    - **Heiti**: RecommendationSystemApplication-1
    - **Notandakenni**: RetailServiceAccount

1. Vistið og lokið síðunni. 

## <a name="turn-on-recommendations"></a>Kveikja á tillögum

Til að kveikja á afurðatillögum skal fylgja þessum skrefum.

1. Í Commerce Headquarters skal leita að **Eiginleikastjórnun**.
1. Veljið **Allir** til að sjá lista yfir tiltæka eiginleika. 
1. Í leitarreitnum skal slá inn **Ráðleggingar**.
1. Veljið eiginleikann **Afurðaráðleggingar**.
1. Á eiginleikasvæðinu **Afurðaráðleggingar** skal velja **Virkja núna**.

![Kveikt á tillögum.](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> - Ferlið að ofan byrjar ferlið við að mynda afurðatillögulista. Það getur tekið nokkrar klukkustundir áður en listarnir verða tiltækir og sjást á sölustað (POS) eða í Dynamics 365 Commerce.
> - Þessi stilling virkjar ekki alla eiginleika tillagna. Ítarlegri eiginleikum eins og sérsniðnum tillögum, „versla svipað útlit“ og „versla svipaða lýsingu“ er stjórnað af sérstökum færslum eiginleikastjórnunar. Upplýsingar um að hvernig á að virkja þessa eiginleika í Commerce Headquarters er að finna í [Virkja sérsniðnar tillögur](personalized-recommendations.md), [Virkja tillögur um „versla svipaða lýsingu](shop-similar-looks.md) og [Virkja tillögur um „versla svipaða lýsingu“](shop-similar-description.md).

## <a name="configure-recommendation-list-parameters"></a>Stilla færibreytur tillögulista

Sjálfgefið er að AI-ML-byggðir afurðatillögulistar veiti leiðbeinandi gildi. Þú getur breytt sjálfgefnum gildum svo að þau henti flæði fyrirtækisins. Til að læra meira um hvernig eigi að breyta sjálfgefnum færibreytum skaltu fara í [Stjórna AI-ML-byggðum niðurstöðum afurðatillagna](modify-product-recommendation-results.md).

## <a name="include-recommendations-in-e-commerce-experiences"></a>Hafa tillögur með í upplifun rafrænna viðskipta

Eftir að hafa virkjað tillögur í Commerce Headquarters sýndu Commerce-einingar venjulega niðurstöður tillagna fyrir upplifun rafrænna viðskipta sem voru tilbúnar til að vera skilgreindar. Frekari upplýsingar er að finna í [Einingar afurðasafns](product-collection-module-overview.md).

## <a name="show-recommendations-on-pos-devices"></a>Sýna tillögur um POS tæki

Eftir að hafa gert tillögur í Commerce-höfuðstöðvar virkar verður að bæta tillöguglugganum við á POS skjánum með skipulagstólinu. Til að fræðast um þetta ferli, sjá [Bættu ráðleggingastjórnun við viðskiptaskjáinn á POS tækjum](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Kveikja á sérsniðnum tillögum

Í Dynamics 365 Commerce geta smásalar gert persónulegar ráðleggingar um vörur (einnig þekktar sem persónugervingar) tiltækar. Þannig er hægt að fella persónulegar ráðleggingar inn í upplifun viðskiptavina á netinu og á sölustað. Þegar kveikt er á sérstillingaraðgerðinni getur kerfið tengt kaup notanda og vöruupplýsingar til að búa til sérsniðnar ráðleggingar um vöru.

Til að læra meira um persónulegar ráðleggingar, sjá [Virkja persónulegar ráðleggingar](personalized-recommendations.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir afurðarráðleggingar](product-recommendations.md)

[Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi](enable-adls-environment.md)

[Settu upp annað gagnaflæði fyrir tillögur](set-up-alternate-data-flow.md)

[Virkja sérsniðnar ráðleggingar](personalized-recommendations.md)

[Virkja tillögur um að kaupa svipaða vöru](shop-similar-looks.md)

[Afþakka sérsniðnar tillögur](personalization-gdpr.md)

[Bæta afurðaráðleggingum við sölustað](product.md)

[Bæta við tillögum á færsluskjáinn](add-recommendations-control-pos-screen.md)

[Aðlagaðu niðurstöður AI-ML](modify-product-recommendation-results.md)

[Búðu til handvirkt myndaðar ráðleggingar](create-editorial-recommendation-lists.md)

[Búðu til tillögur með kynningargögnum](product-recommendations-demo-data.md)

[Algengar spurningar um afurðaráðleggingar](faq-recommendations.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
