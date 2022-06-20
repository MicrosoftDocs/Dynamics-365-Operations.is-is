---
title: Virkja tillögur um að kaupa svipaða vöru
description: Þessi grein lýsir því hvernig á að virkja vöruráðleggingar um „verslaðu svipað útlit“ í Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 3024e832de5e6a60b49c5b0c8bfbe36b2c416379
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884578"
---
# <a name="enable-shop-similar-looks-recommendations"></a>Virkja tillögur um að kaupa svipaða vöru

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að virkja vöruráðleggingar um „verslaðu svipað útlit“ í Microsoft Dynamics 365 Commerce.

Eiginleikinn fyrir ráðleggingar um „versla svipaða vöru“ í Dynamics 365 Commerce notar gervigreind og vélnám til að sýna viðskiptavinum afurðir sem líta svipað út. Með því að bjóða upp á tillögur fyrir „versla svipaða vöru“ fyrir allar smásölurásir í Commerce, geta smásalar aukið ánægja viðskiptavina með því að hjálpa viðskiptavinum að finna á auðveldan hátt það sem þeir vilja.

Virknin fyrir tillögur um að „versla svipaða vöru“ notar afurðarmyndir af grunnafbrigði afurðar til að finna og mæla með svipað útlítandi afurðum í vörulista smásala. 

Tillögur um að „versla svipaða vöru“ eru í boði í bæði umhverfi sölustaðar og rafrænna viðskipta.

### <a name="example-scenarios"></a>Dæmi um aðstæður

- Viðskiptavinur skoðar peysu með svörtum röndum og fær tillögu um svipaða peysu í rauðum lit. Viðskiptavinurinn velur ráðlögðu vöruna í staðinn fyrir þá sem var skoðuð fyrst og fær síðan tillögur um svipaðar afurðir og þá rauðu. 
- Viðskiptavinur notar „versla svipaða vöru“ tillögurnar til að finna eyrnalokka sem passa við hring sem viðskiptavinurinn hefur áhuga á að kaupa.

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a>Virkja tillögur um að kaupa svipaða vöru í Commerce Headquarters

Vöruráðleggingar eru aðeins studdar fyrir notendur Commerce sem hafa flutt geymsluna sína til Azure Data Lake Gen2.

### <a name="prerequisites"></a>Forkröfur

Áður en smásalar geta byrjað að sýna viðskiptavinum ráðleggingar um „versla svipaða vöru“, eru tvö undirbúningsskref:

- [Virkja ráðleggingar um afurðir](enable-product-recommendations.md) í Commerce Headquarters.
- Staðfestið að miðlaþjónninn styðji HTTP-köll.

Til að tillöguvélin geti fengið aðgang að afurðarmyndum, verða smásalar að búa til vefslóðir afurða. Til að búa til vefslóðir afurða í Commerce Headquarters skal fylgja þessum skrefum.

1. Opnið **Myndir afurða**.
1. Á aðgerðasvæðinu skal velja **Skilgreina sniðmát fyrir miðla**.
1. Á eiginleikasvæðinu **Skilgreina sniðmát fyrir miðla**, undir **Vefslóðir miðla**, skal velja **Búa til vefslóðir**.

> [!NOTE]
> Þegar kveikt er á tillögueiginleikanum fyrir „versla svipaða vöru“, hefst ferlið við að búa til tillögulista afurða. Allt að einn dagur getur liðið áður en þessir listar verða í boði og sýnilegir á netinu og í afgreiðslukössum.

Til að virkja tillögueiginleikann „versla svipaða vöru“ í Commerce Headquarters skal fylgja þessum skrefum.

1. Opnið **Eiginleikastjórnun**.
1. Í lista yfir tiltæka eiginleika skal leita að og velja **Versla svipaðar vörur**.
1. Í glugganum hægra megin skal velja **Virkja** til að kveikja á þjónustunni.

Eftirfarandi mynd sýnir eiginleikann **Versla svipaðar vörur** á síðunni **Eiginleikastjórnun** í Commerce Headquarters.

![Eiginleikinn „versla svipaðar vörur“ á síðu eiginleikastjórnunar í Commerce Headquarters.](./media/enableshopsimilarlooks.png)

Eftir að undanfarandi verkum hefur verið lokið eru afgreiðslukassar sjálfkrafa stækkaðir með samhengissvæði **Versla svipaðar vörur**. Með því að velja **Skoða meira** getur notendum afgreiðslukassa verið vísað á síðu „versla svipaðar vörur“ sem hægt er að sía enn frekar.

> [!NOTE]
> Ef slökkt er á tillögueiginleikanum „versla svipaðar vörur“, verða engar aðrar gerðir af vöruráðleggingum fyrir áhrifum. Frekari upplýsingar um vörutillögur er að finna í [Yfirlit yfir vöruráðleggingar](product-recommendations.md).

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a>Bæta hnappnum „Versla svipaðar vörur“ við upplýsingasíður afurða með því að nota svæðishönnuð Commerce

Þegar búið er að virkja ráðleggingareiginleikann „versla svipaðar vörur“ í Commerce Headquarters, býður valkostur í svæðishönnuði Commerce upp á að smásalar bæti hnappnum **Versla svipaðar vörur** við kaupglugga hvaða upplýsingasíðu afurðar sem er. Viðskiptavinur sem velur þennan hnapp er vísað á viðeigandi síðu fyrir „versla svipaðar vörur“ sem skilar vörum með svipuðu útliti. Þar getur viðskiptavinurinn notað val til að sía frekar afurðirnar.

Til að bæta hnappnum **Versla svipaðar vörur** við upplýsingasíðu afurðar með því að nota svæðishönnuð Commerce, skal fylgja þessum skrefum.

1. Opnið fyrirliggjandi síðu svæðishönnunar sem inniheldur kaupgluggaeiningu.
1. Á vinstra yfirlitssvæðinu skal velja kaupgluggaeininguna.
1. Á hægri yfirlitssvæðinu skal velja gátreitinn **Virkja tengil til að kaupa svipaða vöru**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana. Þegar síðan hefur verið birt mun upplýsingasíða afurðar innihalda hnappinn **Versla svipaðar vörur**.

Eftirfarandi mynd sýnir gátreitinn **Virkja tengil til að kaupa svipaða vöru** og hnappinn **Versla svipaðar vörur** á dæmi um upplýsingasíðu afurðar í svæðishönnuði.

![Gátreiturinn „Virkja tengil til að kaupa svipaða vöru“ og hnappurinn „Versla svipaðar vörur“ á upplýsingasíðu afurðar í svæðishönnuði.](./media/SSLecomtooling.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir afurðarráðleggingar](product-recommendations.md)

[Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi](enable-adls-environment.md)

[Virkja ráðleggingar um afurðir](enable-product-recommendations.md)

[Afþakka sérsniðnar tillögur](personalization-gdpr.md)

[Bæta afurðaráðleggingum við sölustað](product.md)

[Bæta við tillögum á færsluskjáinn](add-recommendations-control-pos-screen.md)

[Aðlagaðu niðurstöður AI-ML](modify-product-recommendation-results.md)

[Búðu til handvirkt myndaðar ráðleggingar](create-editorial-recommendation-lists.md)

[Búðu til tillögur með kynningargögnum](product-recommendations-demo-data.md)

[Algengar spurningar um afurðaráðleggingar](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
