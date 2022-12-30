---
title: Yfirlit yfir umsjón hönnunarbreytinga (inniheldur myndband)
description: Í þessari grein er að finna yfirlit yfir breytingastjórnun hönnunar, sem hjálpar til við að skipuleggja og vinna með afurðarútgáfum, og stjórna lífferlum og hönnunarbreytingum.
author: t-benebo
ms.date: 08/09/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a01dfd72428c75d1bb24f32c73c9c799a6c5017e
ms.sourcegitcommit: b3579ac62e1ea15664a114abcc2409cad76d4f19
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/14/2022
ms.locfileid: "9682507"
---
# <a name="engineering-change-management-overview"></a>Yfirlit yfir umsjón hönnunarbreytinga

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Samantekt eiginleika

Framleiðendur í dag krefjast öflugrar afurðagagnastjórnunar, útgáfustjórnunar og breytingastjórnun hönnunar til að ná árangri í heimi með stöðugt minnkandi líftíma, auknum kröfum um gæði og áreiðanleika og aukna áherslu á vöruöryggi.

Breytingastjórnun hönnunar færir skipulag og aga í ferli vörugagnastjórnunar og gerir skilgreiningu, losun og endurskoðun vara mögulegan á stjórnanlegan hátt sem er studdur af verkflæði. Með vöruútgáfum og umsjón hönnunarbreytinga er hægt að skjalfesta, meta áhrif af og nota hönnunarbreytingar í gegnum allan líftíma vöru.

Umsjón hönnunarbreytinga sem hjálpar til við að skipuleggja og vinna með afurðarútgáfur, og stjórna lífferlum og hönnunarbreytingum. Hér er listi yfir helstu eiginleikana:

- Útgáfa vöru
- Aukin virkni afurðarlosunar sem gerir þér kleift að viðhalda aðalgögnum afurðar í einum lögaðila (hönnunarfyrirtækinu) og gefa út fullskilgreinda útgefna afurð til annarra lögaðila
- Reglur fyrir staðfestingu á því að nauðsynlegar upplýsingar séu slegnar inn áður en afurðarútgáfa er virkjuð (undirbúningsathugun)
- Bætt líftímastjórnun með ítarlegum stýringum fyrir það hvenær er hægt að nota útgefna afurð í tilteknum viðskiptaferlum
- Breytingarbeiðnir hönnunar sem eru studdar af verkflæði
- Breytingarpantanir hönnunar sem eru studdar af verkflæði

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4HE6B]

Fyrra myndskeið ([Eiginleikar breytingastjórnunar í Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) er tekin með í [spilunarlista fjármála- og reksturs](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) sem er í boði á YouTube.

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>Kveikja á eiginleikum fyrir umsjón hönnunarbreytinga fyrir kerfið

Áður en hægt er að nota umsjón hönnunarbreytinga þarf að virkja bæði eiginleikann *Umsjón hönnunarbreytinga* og skilgreiningarlykil hans. Ef einnig á að rekja útgáfuvídd afurðanna í færslum (valfrjálst) þarf einnig að virkja bæði eiginleikann *Vídd afurðarútgáfu* og skilgreiningarlykil hans. Eftir að þessi skilyrði hafa verið sett upp eins og þörf er á verður hægt að nota aðra valfrjálsa eiginleika til stjórnun hönnunarbreytinga.

### <a name="turn-the-basic-engineering-change-management-features-on-or-off"></a>Kveikja eða slökkva á eiginleikum fyrir umsjón grunnhönnunarbreytinga

Til að kveikja eða slökkva á eiginleikum fyrir umsjón grunnhönnunarbreytinga skal fylgja þessum skrefum. Sem hluti af Supply Chain Management, útgáfa 10.0.25, er sjálfgefið kveikt á eiginleikanum *Umsjón hönnunarbreytinga*.

1. Farðu í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnusvæðið.
1. Athuga með uppfærslur.
1. Kveiktu eða slökktu á eiginleikanum *Umsjón hönnunarbreytinga* eftir þörfum.
1. Ef rekja á útgáfuvídd vara í færslum (valfrjálst) skal kveikja á eiginleikanum sem heitir *Útgáfa afurðarvíddar*.

### <a name="turn-the-required-configuration-keys-on-or-off"></a>Kveikja eða slökkva á nauðsynlegum skilgreiningarlyklum

Næst skal kveikja á skilgreiningarlyklunum með því að fylgja þessum skrefum. Það er ekki sjálfgefið að kveikt sé á þeim.

1. Setjið kerfið í viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Opnið **Kerfisstjórnun \> Setja upp \> Skilgreining leyfis**.
1. Víkkið út hnútinn **Viðskipti**
1. Gerið skilgreiningarlykilinn fyrir aðaleiginleikann virkan eða óvirkan með því að velja gátreitinn **Umsjón hönnunarbreytingaa**.
1. Stækkaðu hnútinn **Umsjón hönnunarbreytinga** og veldu eða hreinsaðu eftirfarandi gátreiti eftir þörfum (eftir því hvaða eiginleika á að nota):

    - **Leit að eigind** – Veldu þennan gátreit til að virkja [leitareiginleika eigindar](engineering-attributes-and-search.md). Við mælum með því að þessi eiginleiki sé virkur en hægt er að hreinsa þennan gátreit ef ekki á að nota hann.
    - **Breytingastjórnun fyrir framleiðsluferli** – Veldu þennan gátreit ef þú vilt nota eiginleika fyrir umsjón hönnunarbreytinga til að stjórna breytingum í formúlum fyrir framleiðsluferli. Ef þú þarft ekki að stjórna formúlum geturðu hreinsað þennan gátreit. Frekari upplýsingar eru í [Stjórna breytingum á formúlum og innihaldsefnum þeirra](manage-formula-changes.md)

1. Ef einnig á að nota vídd útgáfunnar skal velja gátreitinn **Afurðarvídd - Útgáfa**. (Þessi gátreitur er neðar á listanum, ekki faldaður undir hnútnum **Umsjón hönnunarbreytinga**.) Hægt er að hreinsa gátreitinn ef ekki er þörf á þessum eiginleika.
1. Slökkvið á viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Samstilla þarf gagnagrunninn til að tryggja að stillilyklarnir séu uppfærðir í samræmi við breytingar þínar. Framkvæmdu eitt af eftirfarandi skrefum, eftir því hvaða tegund af umhverfi er verið að vinna með:
    - **Fyrir Tier 1 (þróunarumhverfi)**: Opnaðu verkið þitt í Microsoft Office Visual Studio og veldu svo **Dynamics 365 \> Samstilla gagnagrunn \> Samstilla**.
    - **Fyrir lag 2 (og hærra) umhverfi**: Gagnagrunnurinn samstillist sjálfkrafa eftir að sett er á umhverfið og viðhaldsstillingin, þannig að hægt er sleppa þessu skrefi.

> [!NOTE]
> Til að nota umsjón hönnunarbreytinga þarf að stilla bæði númeraröð uppskriftar og númeraröð formúlu (ef þú ert að nota formúlur) á *Sjálfvirkt* á síðunni **Númeraraðir**.

### <a name="turn-on-additional-engineering-change-management-features"></a>Kveikja á eiginleikum fyrir umsjón frekari hönnunarbreytinga

Eftir að þú kveikir á eiginleikum fyrir umsjón grunnhönnunarbreytinga og virkjar skilgreiningarlykla þeirra, er nokkrum eiginleikum fyrir umsjón frekari hönnunarbreytinga bætt við eiginleikastjórnun. Hver þessara eiginleika er sýndur undir einingunni **Umsjón hönnunarbreytinga**. Eftirfarandi tafla lýsir hverjum valfrjálsum eiginleika og veitir tengla fyrir frekari upplýsingar.

| Eiginleikaheiti í eiginleikastjórnun | Lýsing | Staða eiginleika |
|---|---|---|
| Virkja breytingastjórnun á fyrirliggjandi afurðum | <p>Þessi eiginleiki gerir þér kleift að umbreyta núverandi afurðum í hönnunarafurðir svo að þú getir haft umsjón með þeim í gegnum stjórnun hönnunarbreytinga.</p><p>Frekari upplýsingar eru í [Virkja breytingastjórnun á fyrirliggjandi afurðum](change-management-existing-products.md).</p> | Tiltækt frá og með útgáfu 10.0.25 |
| Hönnunartilkynningar fyrir framleiðslu | <p>Þegar afurð er breytt í hönnun getur verið mikilvægt að tilkynna framleiðslu um þessar breytingar. Á þann hátt geta starfsmenn framleiðslu gripið til viðeigandi ráðstafana, t.d. skipta út íhlut, skipta um uppskriftir eða leið. Þessi eiginleiki gerir þér kleift að tilkynna framleiðslu um breytingar á afurðum sem verið er að framleiða.</p><p>Frekari upplýsingar eru í [Umsjón hönnunarbreytinga](engineering-change-management.md).</p> |  Tiltækt frá og með útgáfu 10.0.25 |
| Bætt erfðaeigind fyrir umsjón hönnunarbreytinga | <p>Þessi eiginleiki einfaldar stjórnun eiginda fyrir fullunnar vörur eða millivörur. Þegar kveikt er á þessum eiginleika er auðveldara að auðkenna allar eigindirnar sem tilheyra vöru og hægt er að velja eigindirnar sem á að dreifa úr þeirri vöru til yfirvöru hennar. Þessi eiginleiki er gagnlegur þegar til dæmis einn þáttur í fullunninni vöru er viðkvæmur, eitraður eða eldfimur vegna þess að þú getur auðveldlega borið kennsl á viðkvæma, eitraða eða eldfima eigindina og dreift henni í fullunna vöru.</p><p>Frekari upplýsingar er að finna í [Hönnunareigindir og leit að hönnunareigind](engineering-attributes-and-search.md).</p> |  Tiltækt frá og með útgáfu 10.0.25 |
| Undirbúningsathuganir afurðar | <p>Þessi eiginleiki gerir þér kleift að setja upp undirbúningsathuganir fyrir staðlaðar (ekki hannaðar) afurðir. Notaðu undirbúningsathuganir afurðar til að ganga úr skugga um að hver afurð sé skilgreind að fullu og að allar reglur séu stilltar áður en boðið verður upp á afurðina og hún notuð í færslum. Ef þessi eiginleiki er gerður óvirkur eftir að hann hefur verið notaður verða öllum fyrirliggjandi undirbúningsathugunum fyrir staðlaðar afurðir eytt.</p><p>Frekari upplýsingar er að finna í [Undirbúningur afurðar](product-readiness.md).</p> |  Tiltækt frá og með útgáfu 10.0.25 |
| Stjórna breytingum á formúlum og innihaldsefnum þeirra | <p>Þessi eiginleiki gerir kleift að fylgjast með breytingum á innihaldsefnum formúlu, aukaafurðum og hliðarafurðum.</p><p>Frekari upplýsingar eru í [Stjórna breytingum á formúlum og innihaldsefnum þeirra](manage-formula-changes.md)</p> |  Tiltækt frá og með útgáfu 10.0.25 |
| Afbrigði útbúið fyrir hönnunarafurðir | <p>Þessi eiginleiki gerir kleift að búa til afbrigði fyrir hönnunarafurðir sem byggja á tiltækum víddargildum.</p><p>Frekari upplýsingar er að finna í [Búa til afbrigði fyrir hönnunarafurðir](engineering-variants.md).</p> |  Tiltækt frá og með útgáfu 10.0.25 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

