---
title: Aðgengiseiginleikar og -geta
description: Þessi grein veitir upplýsingar um aðgengiseiginleika og möguleika í Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: a797b94d8101100574169cdcecfe8df2b5954c15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278152"
---
# <a name="accessibility-features-and-capabilities"></a>Aðgengiseiginleikar og -geta

[!include [banner](includes/banner.md)]

Þessi grein veitir upplýsingar um aðgengiseiginleika og möguleika í Microsoft Dynamics 365 Commerce.

Aðgengiseiginleikar og -geta veita öllum notendum hagnýta leið til að fá aðgang að og framkvæma aðgerðir svo þeir geti náð markmiðum sínum. Þessi breiði hópur notenda gæti þurft hjálpartæki fyrir heyrn, sjón, hreyfigetu eða vegna taugafræðilegs fjölbreytileika.

Ýmsir þættir í Dynamics 365 Commerce gera þér kleift að byggja upp vefsvæðið svo að það innihaldi hjálpartæki. Þegar þú hannar vefsvæðið ættir þú að huga að þeim aðgengisaðgerðum sem nefndar eru á [Aðgengismiðstöð Microsoft](https://www.microsoft.com/accessibility). 

Þessi grein lýsir nokkrum viðbótarsviðum aðgengisvirkni sem þú ættir að hafa í huga þegar þú notar Dynamics 365 Commerce.

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

[Aðgengi í skjámyndum, afurðum og stýringum](/dynamics365/unified-operations/dev-itpro/user-interface/enable-accessibility)

[Aðgengismiðstöð Microsoft](https://www.microsoft.com/accessibility)

[Aðgengismiðstöð Dynamics 365](/dynamics365/get-started/accessibility/index)

[Yfirlit yfir reglufylgni](compliance-overview.md)

[Reglufylgni köku](cookie-compliance.md)

[Bæta við persónuverndarstefnusíðu](add-privacy-page.md)

[Skipta um notandakenni sem tengjast röktum efnisbreytingum](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
