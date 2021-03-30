---
title: Aðgengiseiginleikar og -geta
description: Þetta efnisatriði inniheldur upplýsingar um aðgengiseiginleikana og möguleika í Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 094ad8d34e13051ce7596be462070ead4cbc4f14
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206656"
---
# <a name="accessibility-features-and-capabilities"></a>Aðgengiseiginleikar og -geta


[!include [banner](includes/banner.md)]

Þetta efnisatriði inniheldur upplýsingar um aðgengiseiginleikana og möguleika í Microsoft Dynamics 365 Commerce.

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
| Lokaður skjátexti (CC)      | Texti sem hægt er að birta fyrir hljóð og lýsa hljóðeiginleikum myndbands til að hjálpa notendum sem eru heyrnarlausir eða heyrnarskertir |
| Skjátextar                   | Myndtextaskrár sem sýna texta fyrir vísbendingar samhengis eða spjall á skjánum |
| Hljóðritun           | Hljóðritun á textaformi af töluðum orðum sem er mynduð úr hljóði myndskeiðseigna |
| Hljóðlýsingar           | Aukahljóðrás sem lýsir innihaldi eða samhengi sem er að gerast á skjánum |
| Lágmarksaldurshlið            | Eiginleiki sem getur geymt lágmarksaldur sem áhorfandi verður að vera á til að skoða myndskeið (lýsigögn aðeins) |

### <a name="configure-video-accessibility-elements"></a>Stilla aðgangsþætti myndskeiðs

Í hlutanum Commerce **Miðlasafn** fyrir vefsvæðið þitt geturðu hlaðið upp myndbandseignum sem eru með aðskildar skrár fyrir skjátexta, venjulegt hljóð og hljóðlýsingar. Einnig er hægt að mynda lokaða myndatexta sjálfkrafa þegar myndskeiðseign er hlaðið upp.

#### <a name="generate-or-upload-closed-caption-files-during-video-asset-upload"></a>Myndaðu eða flyttu upp myndatexta við upphleðslu myndskeiðseigna

Fylgdu þessu skrefi til að láta myndatexta myndast sjálfkrafa þegar þú hleður upp myndskeiði.

- Í glugganum **Uppflutningur eigna** velurðu **Mynda lokaða myndatexta sjálfvirkt**. Ef þú ert að búa til lokaða myndatexta, verður skráarveljarann fyrir lokaða myndatexta ekki tiltækur í glugganum.

Fylgdu þessu skrefi til að hlaða myndatexta handvirkt upp þegar þú hleður upp myndskeiði.

- Í glugganum **Uppflutningur eigna** hreinsarðu **Mynda lokaða myndatexta sjálfvirkt**.

Til að hlaða upp venjulegum eða lýsandi hljóðskrám fyrir myndskeiðið skaltu nota skráaveljarann í glugganum **Uppflutningur eigna**.

> [!NOTE]
> Einnig er hægt að bæta við lokuðum myndatexta, venjulegu hljóði og lýsandi hljóðeignum eftir að myndskeiðseign hefur verið hlaðið upp. Opnaðu **Miðlasafnið**, veldu myndbandseignina og smelltu á **Breyta** til að athuga það. Settu síðan viðbótareignirnar upp í eiginleikaglugganum fyrir myndbandseignina og hladdu upp viðbótareignunum.

#### <a name="edit-cc-and-audio-transcript-files"></a>Breyta CC og hljóðritunarskrám

Hægt er að breyta CC og hljóðritunarskrám beint í höfundatólinu. Spilun myndskeiðs er tiltæk meðan á klippingu stendur.

Fylgdu þessum skrefum til að breyta CC og hljóðritunarskrám.

1. Opnaðu **Miðlasafnið** og veldu skráarheiti myndbandseignarinnar. Ritill lokaðs myndatexta og hljóðritunar birtist.
1. Veljið **Breyta**.
1. Breyttu lokuðum myndatexta eða hljóðritunartexta.
1. Þegar því er lokið skaltu smella á **Vista** og smella á **Ljúka við breytingar**.
1. Þegar þú ert tilbúin/n að birta skaltu velja **Birta**.

#### <a name="set-the-minimum-age-attribute"></a>Stilltu eigindina Lágmarksaldur

Hægt er að tengja lýsigagnaeigndina **Lágmarksaldur** við myndskeiðseignir.

Til að stilla eigindina **Lágmarksaldur** fyrir myndskeiðseign skaltu fylgja þessum skrefum.

1. Opnaðu **Miðlasafnið** og veldu myndbandseignina.
1. Veljið **Breyta**.
1. Í eiginleikaglugganum fyrir myndskeiðseignina skaltu stilla eigindina **Lágmarksaldur**.

> [!NOTE]
> Eiginleikaglugginn er aðeins notaður til að stilla og geyma eigindagildi lýsigagna. Það verður að búa til sérsniðnar einingar til að nota þessa eigind fyrir endurspilun.

## <a name="additional-resources"></a>Frekari upplýsingar

[Aðgengi í skjámyndum, afurðum og stýringum](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/user-interface/enable-accessibility)

[Aðgengismiðstöð Microsoft](https://www.microsoft.com/accessibility)

[Aðgengismiðstöð Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/accessibility/index)

[Yfirlit yfir reglufylgni](compliance-overview.md)

[Reglufylgni köku](cookie-compliance.md)

[Bæta við persónuverndarstefnusíðu](add-privacy-page.md)

[Skipta um notandakenni sem tengjast röktum efnisbreytingum](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]