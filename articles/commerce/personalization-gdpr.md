---
title: Afþakka sérsniðnar tillögur
description: Þetta efni útskýrir hvernig þú getur látið viðskiptavini afþakka að fá persónulegar ráðleggingar í Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6a64b45e1326673dd84c3c705491c9c100cdd069
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413131"
---
# <a name="opt-out-of-personalized-recommendations"></a>Afþakka sérsniðnar tillögur

[!include [banner](includes/banner.md)]

Þetta efni útskýrir hvernig þú getur látið viðskiptavini afþakka að fá persónulegar ráðleggingar í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Við stofnun reiknings eru nýir viðskiptavinir sjálfkrafa settir upp til að fá persónulega ráðleggingar. Hins vegar Dynamics 365 Commerce veitir smásöluaðilum ýmsar leiðir til að láta notendur afþakka að fá þessar ráðleggingar og takmarka vinnslu persónuupplýsinga sinna. Sannvottir notendur sem afþakka að fá persónulegar ráðleggingar hætta strax að sjá persónulega lista. Að auki verða öll persónuleg gögn sem safnað er til að sérsníða verða fjarlægð úr persónulegum ráðleggingalíkönum.

Nánari upplýsingar um persónulegar afurðaráðleggingar, sjá [Virkja persónulegar ráðleggingar](personalized-recommendations.md).

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a>Leiðir fyrir smásala til að innleiða afþakkunarupplifun

Smásalar hafa þrjár leiðir til að innleiða afökkunarupplifun.

### <a name="opting-out-on-behalf-of-users"></a>Að afþakka fyrir hönd notenda

Í reikningsstjórnun í bakvinnslu Commerce geta smásalar afþakkað fyrir hönd notenda.

1. Leitaðu að á heimasíðu bakvinnslu **allir viðskiptavinir**.
1. Leitaðu að og veldu viðskiptavin og veldu síðan flýtiflipann **Retail**.

    ![Flýtireiturinn Retail](./media/Disablepersonalizationpart1.png)

1. Undir **Persónuvernd**, stilltu **Slökkva á sérstillingu** kostur á **Já**.

    ![Öryggisstillingar](./media/Disablepersonalizationpart2.png)

1. Veljið **Vista** og lokið skjámyndinni.

### <a name="module-based-opt-out-experience"></a>Eining byggð á afþakkunarreynslu

Söluaðilar geta látið staðfesta notendur afþakka sérsniðnar ráðleggingar. Til að bjóða upp á þessa afþakkunarupplifun skaltu bæta við afþakkunareiningunni fyrir notendur á prófílsíðum viðskiptavinarreiknings.

### <a name="custom-extensions"></a>Sérsniðnar viðbætur

Söluaðilar geta búið til sínar eigin viðbætur til að stjórna afþreyingarupplifun fyrir notendur. Fyrir frekari upplýsingar, sjá [Hringdu í smáforritaskil smásölumiðlara](e-commerce-extensibility/call-retail-server-apis.md) og [Stækkanleiki á netinu](e-commerce-extensibility/overview.md).

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a>Fáðu stafrænt afrit af persónulegum ráðleggingagögnum fyrir hönd staðfestra notanda

Viðskiptavinir gætu viljað fá stafrænt afrit af persónulegum gögnum sínum og einnig séð útflutt mynd af niðurstöðum ráðlegginga. Ef viðskiptavinur óskar eftir þessum upplýsingum verður smásalinn að búa til sérsniðna viðbyggingu sem kallar forritunarviðmót smáforritsþjónustunnar (API) og fyrirspurnir fyrir fullan árangur frá **Velur fyrir þig** listi, byggður á auðkenni viðskiptavinarins. Síðan er hægt að flytja niðurstöðurnar með kommu-aðgreindu gildi (CSV) og deila með viðskiptavininum.

Eftirfarandi dæmi sýnir hvernig smásala getur sinnt þessu verkefni.

1. Söluaðilinn býr til sérsniðna viðbót til að draga persónulegar ráðleggingargögn fyrir hönd notandans. Nánari upplýsingar um hvernig á að búa til einingar, klóna núverandi einingar, hringja í API fyrir smásala netþjóns og aðgerðir til að hringja í gögn, sjá [Stækkanleiki á netinu](e-commerce-extensibility/overview.md).
2. Sérsniðna viðbótin hringir í **fá tilmæli** kjarna gagnaaðgerð og miðlar nauðsynlegum upplýsingum til þeirra, byggðar á kröfum listans. Í tilviki **Velur fyrir þig** listanum verður viðbótin að gefa réttan listaheiti og kenni viðskiptavina yfir í gagnaaðgerðina.

    Ein leið til að búa til sérsniðna viðbót er að klóna núverandi vöruöflunareining sem er notuð til að skila niðurstöðum meðmæla. Með því að klóna þessa núverandi einingu getur smásali breytt núverandi kóða og bætt við nýjum hnappi sem flytur niðurstöður ráðlegginganna yfir í CSV skjal. Frekari upplýsingar er að finna í [Klóna einingar einingasafns](e-commerce-extensibility/clone-starter-module.md) og [Afurðasafnseiningar](product-collection-module-overview.md).

    Sjá heildarskoðun á API-bókasafni smásöluþjónsins [API og viðskiptavinir smásölumiðstöðva og neytenda](dev-itpro/retail-server-customer-consumer-api.md).

3. Eftir að sérsniðna viðbótin er búin til getur smásalinn flutt út CSV-skrá yfir allar niðurstöður meðmæla, byggðar á sérstöku viðskiptavinaauðkenni auðkennds notanda.
4. Söluaðilinn getur deilt útfluttu CSV-skjalinu sem inniheldur fullan persónulega lista yfir ráðlagðar vörur með staðfestum notanda.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir afurðarráðleggingar](product-recommendations.md)

[Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi](enable-adls-environment.md)

[Virkja ráðleggingar um afurðir](enable-product-recommendations.md)

[Kveikja á sérsniðnum tillögum](personalized-recommendations.md)

[Virkja tillögur um að kaupa svipaða vöru](shop-similar-looks.md)

[Bæta við afurðatillögum á sölustað](product.md)

[Bæta tillögum við færsluskjáinn](add-recommendations-control-pos-screen.md)

[Aðlagaðu niðurstöður AI-ML](modify-product-recommendation-results.md)

[Búðu til handvirkt myndaðar ráðleggingar](create-editorial-recommendation-lists.md)

[Búðu til tillögur með kynningargögnum](product-recommendations-demo-data.md)

[Algengar spurningar um afurðaráðleggingar](faq-recommendations.md)
