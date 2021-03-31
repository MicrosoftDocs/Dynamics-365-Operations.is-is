---
title: Algengar spurningar um afurðaráðleggingar
description: Þetta efni veitir upplýsingar um ferla og verkfæri sem þú getur notað til að leysa vandamál sem tengjast afurðatillögum eða niðurstöðum þeirra.
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
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f0140f798e000ca66c67afa00f788abc560c8a07
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216700"
---
# <a name="product-recommendations-faq"></a>Algengar spurningar um afurðaráðleggingar


[!include [banner](includes/banner.md)]

Þetta efni veitir upplýsingar um ferla og verkfæri sem þú getur notað til að leysa vandamál sem tengjast [afurðatillögum](product-recommendations.md) eða niðurstöðum þeirra.

## <a name="best-practices"></a>Bestu starfsvenjur
Það er mjög mikilvægt að nýta hugtakið afurðarsniðmát og afbrigði. Skynsamleg flokkun afbrigða í yfirafurðarsniðmát hjálpar listum reiknirita og þjónustu við að búa til betri líkön. Að auki getur þjónustan þjónað aðeins einu afurðatilviki í stað þess að setja öll náskyld afbrigði á lista. Þegar öll náskyld afbrigði eru sett á lista geta rangar eða afritaðar niðurstöður komið fram.

## <a name="why-are-products-missing-from-my-recommendation-lists"></a>Af hverju vantar vörur í tillögulistunum mínum?

Venjulega, ef vöru vantar í afurðatillögulista, gæti verið um uppstillingarvandamál að ræða. Til dæmis gæti verið um ranga upphafsdagsetningu eða lokadagsetningu að ræða, vídd gæti verið rangt stillt eða varan gæti ekki verið í réttu rásarsamsetningu, o.s.frv.

Ef vöru vantar í tillögulista sem er byggður á námi gervigreindar-véla (AI-ML) gæti varan hugsanlega ekki passað við viðmiðanir tillögulistans, eða það gæti verið að það hafi ekki verið nægjanlegar innkaupafærslur til að tillögulistinn geti sýnt það.

Við mælum með að þú athugir þessi skref:
1. **Gakktu úr skugga um að afurðatillögur hafi verið gerðar virkar í HQ**. Nánari upplýsingar um hvernig hægt er að virkja þessa þjónustu er að finna í [Virkja afurðatillögur](enable-product-recommendations.md).
1. **Gakktu úr skugga um að helstu afurðaeiginleikar séu stilltir.** Til dæmis verður að stilla vöruúrval á **Láta fylgja með**.
1. **Fyrir nýjar valdar vörur getur tekið allt að 3 klukkustundir áður en varan byrjar að birtast á nýja listanum.**
1. **Ef vara er enn ekki að birtast í Vinsælt, Mest selt, Fólki líkar líka eða Oft keypt saman, þá gæti verið að sú vara hafi ekki nægar færslur.** Í þessu tilfelli geturðu annaðhvort beðið eftir að fleiri færslur eigi sér stað, uppfært sjálfgefna færibreytur tillögulistans eða notað handvirkar íhlutanir til að breyta tillöguniðurstöðum afurðalista. Fyrir frekari upplýsingar um breytur ráðlegginga, sjá [Stjórna AI-ML byggðum afurðum meðmæla](modify-product-recommendation-results.md).
1. **Gakktu úr skugga um að varan uppfylli tillöguviðmið fyrir listann.** Fyrir frekari upplýsingar um tillögufæribreytur afurða, sjá [Stjórna AI-ML-byggðum niðurstöðum afurðatillagna](modify-product-recommendation-results.md).

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a>Hvernig get ég komið í veg fyrir að slæmum tillögum sé skilað?

Tillögulistar þurfa mikið magn færslna til að skila niðurstöðum. Þess vegna er mikilvægt að notendur leggi fram öll söguleg færslugögn.

Að auki eru afurðir sem hafa engar færslur eða fáar færslur yfirleitt ekki með niðurstöðurnar **Fólki líkar líka** eða **Oft keypt saman** og birtast ekki á tillögulistanum **Vinsælt** eða **Mest selt**. Þessar aðstæður geta oft komið upp fyrir mjög nýjar vörur, eða fyrir gamlar vörur sem eru með lítinn fjölda kaupa. Vinsælir nýir hlutir munu auðveldlega komast yfir þetta mál.

Við mælum með að þú fylgir þessum skrefum:
1. **Gakktu úr skugga um að varan uppfylli tillöguviðmið fyrir listann.** Fyrir frekari upplýsingar um tillögufæribreytur afurða, sjá Breyta AI-ML-byggðum niðurstöðum afurðatillagna.
1. **Ef varan er ný skaltu íhuga að breyta meðmælalistanum þar til varan er komin með fleiri færslur.** Fyrir frekari upplýsingar um hvernig eigi að breyta niðurstöðum tillögulista, sjá [Stjórna AI-ML-byggðum niðurstöðum afurðatillagna](modify-product-recommendation-results.md).


- **Gakktu úr skugga um að varan uppfylli tillöguviðmið fyrir listann.** Fyrir frekari upplýsingar um tillögufæribreytur afurða, sjá [Stjórna AI-ML-byggðum niðurstöðum afurðatillagna](modify-product-recommendation-results.md).
- **Ef varan er ný skaltu íhuga að breyta meðmælalistanum þar til varan er komin með fleiri færslur**. Fyrir frekari upplýsingar um hvernig eigi að breyta niðurstöðum tillögulista, sjá [Stjórna AI-ML-byggðum niðurstöðum afurðatillagna](modify-product-recommendation-results.md).

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a>Get ég fjarlægt vöru en samt séð hana í versluninni?

Þú getur aðlagað lista sem eru búnir til á reiknirit ef viðskiptaþörf kemur upp. Hins vegar, ef vara er fjarlægð af tillögulistanum, verður varan áfram sýnileg í versluninni. Fyrir frekari upplýsingar um hvernig eigi að breyta niðurstöðum afurðatillagna, sjá [Stjórna AI-ML-byggðum niðurstöðum afurðatillagna](modify-product-recommendation-results.md).

Ef þú verður að hindra að hlutur verði uppgötvaður í versluninni, verður þú að breyta gildinu **Vöruúrval** í **Útiloka**.

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a>Hvernig bæti ég lista við netverslunarsíðu?

Nánari upplýsingar um hvernig á að bæta við afurðatillögusíðum við vefverslunina þína, sjá [Bæta afurðatillögulistum við síður](add-reco-list-to-page.md).

## <a name="how-do-i-enable-recommendations-on-pos"></a>Hvernig get ég virkjað tillögur fyrir POS?

Eftir að hafa gert afurðatillögur virkar þarftu að bæta við tillöguborðinu á POS skjánum. Nánari upplýsingar er að finna í [Bæta við tillögustýringu á færsluskjá tækja á sölustað](add-recommendations-control-pos-screen.md).

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

[Búðu til handvirkt myndaðar ráðleggingar](create-editorial-recommendation-lists.md)

[Búðu til tillögur með kynningargögnum](product-recommendations-demo-data.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]