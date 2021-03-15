---
title: Virkja ráðleggingar um „versla svipaða lýsingu“
description: Þetta efnisatriði lýsir því hvernig á að virkja vörutillögurnar fyrir „versla vörur með svipaðri lýsingu“ í Microsoft Dynamics 365 Commerce.
author: bsokolov
manager: AnnBe
ms.date: 01/13/2021
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
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b3b7abf47a3bdacaa4b91ae32b68a809a84b0b1d
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098632"
---
# <a name="enable-shop-similar-description-recommendations"></a>Virkja ráðleggingar um „versla svipaða lýsingu“

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að virkja vörutillögurnar fyrir „versla vörur með svipaðri lýsingu“ í Microsoft Dynamics 365 Commerce.

Eiginleikinn fyrir tillögu um „versla vörur með svipaðri lýsingu“ í Dynamics 365 Commerce notar gervigreind og vélnám til að koma með tillögur að vörum sem eru með svipaðar lýsingar og það sem viðskiptavinurinn er að skoða. Með því að bjóða upp á tillögur fyrir „versla vörur með svipaðri lýsingu“ fyrir allar smásölurásir í Commerce, geta smásalar auðveldað viðskiptavinum að finna það sem þeir vilja.

Virknin fyrir tillögur um „versla vörur með svipaðri lýsingu“ notar vöruheiti og lýsingu á grunnvöru til að finna og mæla með svipuðum vörum í vörulista smásöluaðilans.

Tillögur fyrir „versla vörur með svipaðri lýsingu“ er í boði bæði á sölustað og í rafrænni viðskiptaupplifun.

## <a name="example-scenarios"></a>Dæmi um aðstæður

Eftirfarandi dæmi um aðstæður sýnir tillögugerðir sem virknin „versla vörur með svipaðri lýsingu“ getur boðið upp á:

- Viðskiptavinur skoðar gamaldags hornspangagleraugu og fær nokkrar tillögur að öðrum gleraugum sem eru með svipaða hönnun innan sviðs smásöluaðilans.
- Viðskiptavinur notar tillögur að „versla vörur með svipaða lýsingu“ til að uppgötva kaffitegundir sem eru með svipað bragð og hann keypti áður hjá smásöluaðilanum.

## <a name="set-up-shop-similar-description-recommendations"></a>Setja upp tilllögur að „versla vörur með svipaðri lýsingu“

Vöruráðleggingar eru aðeins studdar fyrir notendur Commerce sem hafa flutt geymsluna sína til Azure Data Lake Storage Gen2.

### <a name="prerequisites"></a>Forkröfur

Áður en hægt er að sýna viðskiptavinum ráðleggingar um „versla vörur með svipaðri lýsingu“ þarf að ljúka eftirfarandi skilyrðum:

- [Virkja ráðleggingar um afurðir](enable-product-recommendations.md) í Commerce Headquarters.
- Staðfestið að miðlaþjónninn styðji HTTP-köll.

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a>Kveikja á eiginleika fyrir ráðleggingar um „versla vörur með svipaðri lýsingu“

Til að kveikja á eiginleika fyrir ráðleggingar um „versla vörur með svipaðri lýsingu“ í Commerce Headquarters skal fylgja þessum skrefum.

1. Á vinnusvæðinu **Eiginleikastjórnun**, í lista yfir tiltæka eiginleika, skal leita að og velja **Versla vörur með svipaða lýsingu**.
1. Í glugganum hægra megin skal velja **Virkja**.

> [!NOTE]
> Þegar kveikt er á eiginleikanum byrjar kerfið að búa til tillögulista yfir vörur. Það getur tekið allt að einn dag áður en listarnir verða aðgengilegir og sýnilegir á netinu og í afgreiðslukössum.
>
> Ef slökkt er á eiginleikanum mun það ekki hafa áhrif á aðrar gerðir af vörutillögum. Frekari upplýsingar um vörutillögur er að finna í [Yfirlit yfir vöruráðleggingar](product-recommendations.md).

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a>Bæta hnappi fyrir versla vörur með svipaða lýsingu á síður vöruupplýsinga

Þegar kveikt hefur verið á eiginleikanum fyrir tillögur að „versla vörur með svipaða lýsingu“ í Commerce Headquarters er hægt að bæta hnappnum **Versla vörur með svipaða lýsingu** við kaupglugga hvaða vöruupplýsingasíðu sem er. Viðskiptavinur sem velur þennan hnapp er vísað á viðeigandi síðu **Versla vörur með svipaða lýsingu** sem sýnir vörur sem eru svipaðar útlits. Viðskiptavinurinn getur síðan notað val til að afmarka vörurnar enn frekar.

Til að bæta hnappnum **Versla vörur með svipaða lýsingu** við upplýsingasíðu afurðar með því að nota Commerce Site Builder, skal fylgja þessum skrefum.

1. Opnið fyrirliggjandi síðu svæðishönnunar sem inniheldur kaupgluggaeiningu.
1. Á vinstra yfirlitssvæðinu skal velja kaupgluggaeininguna.
1. Á hægra yfirlitssvæðinu skal velja gátreitinn **Virkja tengil til að kaupa vörur með svipaða lýsingu**.
1. Veljið **Vista**.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana. Þegar síðan hefur verið birt mun upplýsingasíða afurðar innihalda hnappinn **Versla vörur með svipaða lýsingu**.

Eftirfarandi mynd sýnir gátreitinn **Virkja tengil til að versla vörur með svipaða lýsingu** og hnappinn **Versla vörur með svipaða lýsingu** í dæmi um upplýsingasíðu afurðar í svæðishönnuði.

![Gátreiturinn „Virkja tengil til að versla vörur með svipaða lýsingu“ og hnappurinn „Versla vörur með svipaða lýsingu“ á upplýsingasíðu afurðar í svæðishönnuði](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir afurðarráðleggingar](product-recommendations.md)

[Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi](enable-adls-environment.md)

[Virkja ráðleggingar um afurðir](enable-product-recommendations.md)

[Virkja tillögur um að kaupa svipaða vöru](shop-similar-looks.md)

[Aðlagaðu niðurstöður AI-ML](modify-product-recommendation-results.md)

[Búðu til handvirkt myndaðar ráðleggingar](create-editorial-recommendation-lists.md)

[Algengar spurningar um afurðaráðleggingar](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]