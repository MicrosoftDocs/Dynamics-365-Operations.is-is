---
title: Aðgengiseiginleikar og -geta
description: Þetta efnisatriði veitir upplýsingar um aðgengiseiginleika og -getu í Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e667f89ffbc5496cc93f83fd3e7b29ba6ffa979
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946029"
---
# <a name="accessibility-features-and-capabilities"></a>Aðgengiseiginleikar og -geta

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um aðgengiseiginleika og -getu í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Aðgengiseiginleikar og -geta veita öllum notendum hagnýta leið til að fá aðgang að og framkvæma aðgerðir svo þeir geti náð markmiðum sínum. Þessi breiði hópur notenda gæti þurft hjálpartæki fyrir heyrn, sjón, hreyfigetu eða vegna taugafræðilegs fjölbreytileika.

Ýmsir þættir í Dynamics 365 Commerce gera þér kleift að byggja upp vefsvæðið svo að það innihaldi hjálpartæki. Þegar þú hannar vefsvæðið ættir þú að huga að þeim aðgengisaðgerðum sem nefndar eru á [Aðgengismiðstöð Microsoft](https://www.microsoft.com/accessibility). 

Þetta efni lýsir nokkrum viðbótarsviðum aðgengisvirkni sem þú ættir að hafa í huga þegar þú notar Dynamics 365 Commerce.

## <a name="image-alt-text"></a>Annar myndtexti

Dynamics 365 Commerce er með innbyggt stafrænt eignastýringarkerfi til að rekja mynd- og myndbandaeignir sem notaðar eru á vefsvæðinu. Hægt er að bæta við myndatexta, lýsingum og öðrum texta í eiginleikaglugg fyrir mynd þegar hún er valin eða hlaðið inn.

## <a name="video-accessibility"></a>Myndskeiðsaðgengi

Stafræna eignastýringakerfið Dynamics 365 Commerce styður ýmsa aðgengiseiginleika fyrir myndefni. Eftirfarandi tafla telur upp nokkur dæmi.

| Myndskeiðseiginleiki               | Lýsing |
|-----------------------------|-------------|
| Lokaður skjátexti (CC)      | Texti sem hægt er að sýna fyrir hljóð og lýsandi þætti myndskeiðs til að hjálpa notendum sem eru heyrnarskertir |
| Skjátextar                   | Myndtextaskrár sem sýna texta fyrir vísbendingar samhengis eða spjall á skjánum |
| Hljóðritun           | Hljóðritun á textaformi af töluðum orðum sem er mynduð úr hljóði myndskeiðseigna |
| Hljóðlýsingar           | Aukahljóðrás sem lýsir innihaldi eða samhengi sem er að gerast á skjánum |
| Lágmarksaldurshlið            | Eiginleiki sem getur geymt lágmarksaldur sem áhorfandi verður að vera á til að skoða myndskeið (lýsigögn aðeins) |

### <a name="configure-video-accessibility-elements"></a>Stilla aðgangsþætti myndskeiðs

Í Dynamics 365 Commerce, í kaflanum **Eignir** fyrir vefsvæðið, geturðu hlaðið upp myndskeiðseignum sem eru með aðskildar skrár fyrir lokaða myndatexta, venjulegt hljóð og lýsandi hljóð. Einnig er hægt að mynda lokaða myndatexta sjálfkrafa þegar myndskeiðseign er hlaðið upp.

#### <a name="generate-or-upload-closed-caption-files-during-video-asset-upload"></a>Myndaðu eða flyttu upp myndatexta við upphleðslu myndskeiðseigna

Fylgdu þessu skrefi til að láta myndatexta myndast sjálfkrafa þegar þú hleður upp myndskeiði.

- Í glugganum **Uppflutningur eigna** velurðu **Mynda lokaða myndatexta sjálfvirkt**. Ef þú ert að búa til lokaða myndatexta, verður skráarveljarann fyrir lokaða myndatexta ekki tiltækur í glugganum.

Fylgdu þessu skrefi til að hlaða myndatexta handvirkt upp þegar þú hleður upp myndskeiði.

- Í glugganum **Uppflutningur eigna** hreinsarðu **Mynda lokaða myndatexta sjálfvirkt**.

Til að hlaða upp venjulegum eða lýsandi hljóðskrám fyrir myndskeiðið skaltu nota skráaveljarann í glugganum **Uppflutningur eigna**.

> [!NOTE]
> Einnig er hægt að bæta við lokuðum myndatexta, venjulegu hljóði og lýsandi hljóðeignum eftir að myndskeiðseign hefur verið hlaðið upp. Farðu í **Eignir**, veldu myndskeiðseignina og sæktu hana. Síðan skaltu hlaða upp viðbótareignunum í eiginleikaglugganum fyrir myndskeiðseignina.

#### <a name="edit-cc-and-audio-transcript-files"></a>Breyta CC og hljóðritunarskrám

Hægt er að breyta CC og hljóðritunarskrám beint í höfundatólinu. Spilun myndskeiðs er tiltæk meðan á klippingu stendur.

Fylgdu þessum skrefum til að breyta CC og hljóðritunarskrám.

1. Farðu í **Eignir**, veldu myndskeiðseignina og veldu síðan **Breyta CC/hljóðriti**. Ritill lokaðs myndatexta og hljóðritunar birtist.
1. Velja **Skrá út**.
1. Breyttu lokuðum myndatexta eða hljóðritunartexta.
1. Þegar því er lokið skaltu velja **Vista** og velja síðan **Skrá inn**.
1. Þegar þú ert tilbúin/n að birta skaltu velja **Birta**.

#### <a name="set-the-minimum-age-attribute"></a>Stilltu eigindina Lágmarksaldur

Hægt er að tengja lýsigagnaeigndina **Lágmarksaldur** við myndskeiðseignir.

Til að stilla eigindina **Lágmarksaldur** fyrir myndskeiðseign skaltu fylgja þessum skrefum.

1. Farðu í **Eignir** og veldu myndskeiðseignina.
1. Velja **Skrá út**.
1. Í eiginleikaglugganum fyrir myndskeiðseignina skaltu stilla eigindina **Lágmarksaldur**.

> [!NOTE]
> Eiginleikaglugginn er aðeins notaður til að stilla og geyma eigindagildi lýsigagna. Það verður að búa til sérsniðnar einingar til að nota þessa eigind fyrir endurspilun.

## <a name="additional-resources"></a>Frekari upplýsingar

[Aðgengi í skjámyndum, afurðum og stýringum](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/user-interface/enable-accessibility)

[Aðgengismiðstöð Microsoft](https://www.microsoft.com/accessibility)

[Aðgengismiðstöð Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/accessibility/index)

[Yfirlit yfir samræmi](compliance-overview.md)

[Kökusamræmi](cookie-compliance.md)

[Bæt við síðu persónuverndarstefnu](add-privacy-page.md)
