---
title: Nota skjástillingar fyrir afurðavíddir
description: Í þessu efnisatriði er fjallað um skjástillingar fyrir afurðarvíddir og útskýrt hvernig á að nota þær í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d6854c11822e07ff06426b7a35eac86cdc0e9b06
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356903"
---
# <a name="apply-display-settings-for-product-dimensions"></a>Nota skjástillingar fyrir afurðavíddir

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Í þessu efnisatriði er fjallað um skjástillingar fyrir afurðarvíddir og útskýrt hvernig á að nota þær í Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce styður stærð, stíl og litvíddir til að greina afurðarafbrigði. Stærðir eru yfirleitt sýndar sem textagildi, t.d. „Lítið“, „Miðlungs“ og „Stórt“ fyrir stærðir og „Svart“ og „Brúnt“ fyrir liti. Ef afurð styður hinsvegar mörg afbrigði getur reynst erfitt að leita í afurðarafbrigðum vegna þess að margs konar val er nauðsynlegt til að skoða myndina fyrir hvert afbrigði. Til að gera það auðveldara að skoða afurðarafbrigði getur útgáfa 10.0.20 af Commerce notað myndir og sextándakerfiskóða til að sýna víddir sem sýnishorn.

Í vefsmið Commerce eru víddastillingar skilgreindar á **Stillingar svæðis \> Viðbætur \> Stillingar víddar**. Eftirfarandi skýringarmynd sýnir dæmi um víddastillingar í vefsmið.

![Dæmi um svæðisstillingar í vefsmið Commerce.](./dev-itpro/media/swatch_site_settings.PNG)

Tvær víddarsamstæður eru tiltækar:

- **Víddir sem á að birta sem mynd** – Tilgreinið hvaða víddir ættu að birtast sem sýnishorn á svæðum rafrænna viðskipta á borð við upplýsingasíður afurða og listasíður leitarniðurstaða. Hægt er að sýna hvaða samsetningu sem er af lita-, stærðar- og stílvíddum. Ef vídd er valin til birtingar sem sýnishorn mun myndþýðingareining Commerce leita að tiltækri skilgreiningu á sýnishorni sextándakerfiskóða. Ef enginn sextándakerfiskóði er stilltur leita kerfisrök að stillingu á sýnishorni myndaslóðar. Ef hvorki sextándakerfiskóði né myndaslóð er skilgreind verður texti sýndur.

    Eftirfarandi mynd sýnir dæmi þar sem upplýsingasíða afurðar á svæði fyrir rafræn viðskipti inniheldur sýnishorn lita og stærða. Í þessu dæmi er sextándakerfiskóði skilgreindur fyrir litavíddina. Því eru sýnishorn sýnd sem litir. Hinsvegar er hvorki sextándakerfiskóði né myndaslóð stillt fyrir stærðarvíddina. Því er texti sýndur.

    ![Dæmi um litavíddina sem sýnd er sem sýnishorn á upplýsingasíðu afurðar á rafrænu svæði viðskipta.](./dev-itpro/media/swatch_pdp.png)

- **Víddir til að birta í afurðarspjaldi** – Tilgreinið hvaða víddir eigi að birtast á afurðarspjöldum sem eru sýnd í listum og á listasíðum. Áður en vídd getur birst á afurðarspjaldi þarf að virkja þessa stillingu fyrir þá vídd. Stillingin **Víddir til að birta sem mynd** ætti einnig að vera virk. Hegðun sýnishornavals á afurðarspjöldum er fínstillt fyrir litavíddina. Fyrir aðrar víddir gæti skoðunarviðbót verið nauðsynleg til að sérstilla hegðun sýnishornavals.

    Eftirfarandi mynd sýnir dæmi þar sem listasíða á svæði rafrænna viðskipta inniheldur afurðarspjöld sem eru með litaspjöld.

    ![Dæmi um litavíddina sem sýnd er sem litaspjald á listasíðu svæðis fyrir rafræn viðskipti.](./dev-itpro/media/swatch_searchresults.PNG)

Upplýsingar um hvernig á að stilla víddir afurða þannig að þau eru birt sem sýnishorn á vefsíðum er að finna í [Stilla afurðarvíddargildi þannig að þau birtist sem sýnishorn](./dev-itpro/dimensions-swatch.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Leitarniðurstöðueining](search-result-module.md)

[Kaupgluggaeining](add-buy-box.md)

[Stilla afurðarvíddargildi þannig að þau birtist sem sýnishorn](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
