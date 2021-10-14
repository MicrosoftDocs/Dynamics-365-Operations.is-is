---
title: Yfirlit yfir umsjón hönnunarbreytinga
description: Í þessu efnisatriði er að finna yfirlit yfir umsjón hönnunarbreytinga, sem hjálpar til við að skipuleggja og vinna með afurðarútgáfum, og stjórna lífferlum og hönnunarbreytingum.
author: t-benebo
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 89a3eb584275e52910726ca5a9ed53f744f10b8d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574690"
---
# <a name="engineering-change-management-overview"></a>Yfirlit yfir umsjón hönnunarbreytinga

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Samantekt eiginleika

Framleiðendur í dag krefjast öflugrar afurðagagnastjórnunar, útgáfustjórnunar og umsjón hönnunarbreytinga til að ná árangri í heimi með stöðugt minnkandi líftíma, auknum kröfum um gæði og áreiðanleika og aukna áherslu á vöruöryggi.

Umsjón hönnunarbreytinga færir skipulag og aga í ferli vörugagnastjórnunar og gerir skilgreiningu, losun og endurskoðun vara mögulegan á stjórnanlegan hátt sem er studdur af verkflæði.Í gegnum afurðarútgáfu og breytingastjórnun hönnunar er hægt að skrá, meta áhrif og nota breytingar á hönnun í gegnum allt líftímakerfi afurðar.

Umsjón hönnunarbreytinga sem hjálpar til við að skipuleggja og vinna með afurðarútgáfur, og stjórna lífferlum og hönnunarbreytingum. Hér er listi yfir helstu eiginleikana:

- Útgáfa vöru
- Aukin virkni afurðarlosunar sem gerir þér kleift að viðhalda aðalgögnum afurðar í einum lögaðila (hönnunarfyrirtækinu) og gefa út fullskilgreinda útgefna afurð til annarra lögaðila
- Reglur fyrir staðfestingu á því að nauðsynlegar upplýsingar séu slegnar inn áður en afurðarútgáfa er virkjuð (undirbúningsathugun)
- Bætt líftímastjórnun með ítarlegum stýringum fyrir það hvenær er hægt að nota útgefna afurð í tilteknum viðskiptaferlum
- Breytingarbeiðnir hönnunar sem eru studdar af verkflæði
- Breytingarpantanir hönnunar sem eru studdar af verkflæði

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

Fyrra myndskeið ([Eiginleikar breytingastjórnunar í Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) er tekin með í [Finance and Operations spilunarlista](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) sem er í boði á YouTube.

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>Kveikja á eiginleikum fyrir umsjón hönnunarbreytinga fyrir kerfið

Áður en hægt er að nota umsjón hönnunarbreytinga þarf að virkja bæði eiginleikann *Umsjón hönnunarbreytinga* og skilgreiningarlykil hans. Ef einnig á að rekja útgáfuvídd afurðanna í færslum (valfrjálst) þarf einnig að virkja bæði eiginleikann *Vídd afurðarútgáfu* og skilgreiningarlykil hans. Eftir að þessi skilyrði hafa verið sett upp eins og þörf er á verður hægt að nota aðra valfrjálsa eiginleika til stjórnun hönnunarbreytinga.

### <a name="turn-on-the-basic-engineering-change-management-features"></a>Kveikja á eiginleikum fyrir umsjón grunnhönnunarbreytinga

Fyrst skal kveikja á eiginleikunum með því að fylgja þessum skrefum.

1. Farðu í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnusvæðið.
1. Athuga með uppfærslur.
1. Kveikið á eiginleikanum sem kallast *Umsjón hönnunarbreytinga*.
1. Ef nota á þetta skal einnig kveikja á eiginleikanum sem kallast *Útgáfa afurðarvíddar*.

### <a name="turn-on-the-required-configuration-keys"></a>Kveiktu á nauðsynlegum stillingalyklum

Næst skal kveikja á skilgreiningarlyklunum með því að fylgja þessum skrefum.

1. Setjið kerfið í viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Opnið **Kerfisstjórnun \> Setja upp \> Skilgreining leyfis**.
1. Víkkið út hnútinn **Viðskipti**
1. Virkið skilgreiningarlykilinn fyrir aðaleiginleikann með því að velja gátreitinn **Stjórnun hönnunarbreytingar**.
1. Stækkaðu hnútinn **Umsjón hönnunarbreytinga** og veldu eða hreinsaðu eftirfarandi gátreiti eftir þörfum (eftir því hvaða eiginleika á að nota):

    - **Leit að eigind** – Veldu þennan gátreit til að virkja [leitareiginleika eigindar](engineering-attributes-and-search.md). Við mælum með því að þessi eiginleiki sé virkur en hægt er að hreinsa þennan gátreit ef ekki á að nota hann.
    - **Breytingastjórnun fyrir framleiðsluferli** – Veldu þennan gátreit ef þú vilt nota eiginleika fyrir umsjón hönnunarbreytinga til að stjórna breytingum í formúlum fyrir framleiðsluferli. Ef þú þarft ekki að stjórna formúlum geturðu hreinsað þennan gátreit. Frekari upplýsingar eru í [Stjórna breytingum á formúlum og innihaldsefnum þeirra](manage-formula-changes.md)

1. Ef einnig á að nota vídd útgáfunnar skal velja gátreitinn **Afurðarvídd - Útgáfa**. (Þessi gátreitur er neðar á listanum, ekki faldaður undir hnútnum **Stjórnun hönnunarbreytinga**.)
1. Slökkvið á viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

> [!IMPORTANT]
> Frá og með apríl 2022 verða leyfislyklarnir fyrir bæði **Stjórnun hönnunarbreytinga** og **Afurðarvídd - Útgáfa** virkjaðir að sjálfgefnu fyrir allar nýja uppsetningar, en þú munt enn geta slökkt á þeim ef á þarf að halda.

### <a name="turn-on-additional-engineering-change-management-features"></a>Kveikja á eiginleikum fyrir umsjón frekari hönnunarbreytinga

Eftir að þú kveikir á eiginleikum fyrir umsjón grunnhönnunarbreytinga og virkjar skilgreiningarlykla þeirra, er nokkrum eiginleikum fyrir umsjón frekari hönnunarbreytinga bætt við eiginleikastjórnun. Hver þessara eiginleika er sýndur undir einingunni **Umsjón hönnunarbreytinga**. Eftirfarandi tafla lýsir hverjum valfrjálsum eiginleika og veitir tengla fyrir frekari upplýsingar.

| Eiginleikaheiti í eiginleikastjórnun | lýsing |
|---|---|
| Virkja breytingastjórnun á fyrirliggjandi afurðum | <p>Þessi eiginleiki gerir þér kleift að umbreyta núverandi afurðum í hönnunarafurðir svo að þú getir haft umsjón með þeim í gegnum stjórnun hönnunarbreytinga.</p><p>Frekari upplýsingar eru í [Virkja breytingastjórnun á fyrirliggjandi afurðum](change-management-existing-products.md).</p> |
| Hönnunartilkynningar fyrir framleiðslu | <p>Þegar afurð er breytt í hönnun getur verið mikilvægt að tilkynna framleiðslu um þessar breytingar. Á þann hátt geta starfsmenn framleiðslu gripið til viðeigandi ráðstafana, t.d. skipta út íhlut, skipta um uppskriftir eða leið. Þessi eiginleiki gerir þér kleift að tilkynna framleiðslu um breytingar á afurðum sem verið er að framleiða.</p><p>Frekari upplýsingar eru í [Umsjón hönnunarbreytinga](engineering-change-management.md).</p> |
| Bætt erfðaeigind fyrir umsjón hönnunarbreytinga | <p>Þessi eiginleiki einfaldar stjórnun eiginda fyrir fullunnar vörur eða millivörur. Þegar kveikt er á þessum eiginleika er auðveldara að auðkenna allar eigindirnar sem tilheyra vöru og hægt er að velja eigindirnar sem á að dreifa úr þeirri vöru til yfirvöru hennar. Þessi eiginleiki er gagnlegur þegar til dæmis einn þáttur í fullunninni vöru er viðkvæmur, eitraður eða eldfimur vegna þess að þú getur auðveldlega borið kennsl á viðkvæma, eitraða eða eldfima eigindina og dreift henni í fullunna vöru.</p><p>Frekari upplýsingar er að finna í [Hönnunareigindir og leit að hönnunareigind](engineering-attributes-and-search.md).</p> |
| Undirbúningsathuganir afurðar | <p>Þessi eiginleiki gerir þér kleift að setja upp undirbúningsathuganir fyrir staðlaðar (ekki hannaðar) afurðir. Notaðu undirbúningsathuganir afurðar til að ganga úr skugga um að hver afurð sé skilgreind að fullu og að allar reglur séu stilltar áður en boðið verður upp á afurðina og hún notuð í færslum. Ef þessi eiginleiki er gerður óvirkur eftir að hann hefur verið notaður verða öllum fyrirliggjandi undirbúningsathugunum fyrir staðlaðar afurðir eytt.</p><p>Frekari upplýsingar er að finna í [Undirbúningur afurðar](product-readiness.md).</p> |
| Stjórna breytingum á formúlum og innihaldsefnum þeirra | <p>Þessi eiginleiki gerir kleift að fylgjast með breytingum á innihaldsefnum formúlu, aukaafurðum og hliðarafurðum.</p><p>Frekari upplýsingar eru í [Stjórna breytingum á formúlum og innihaldsefnum þeirra](manage-formula-changes.md)</p> |
| Afbrigði útbúið fyrir hönnunarafurðir | <p>Þessi eiginleiki gerir kleift að búa til afbrigði fyrir hönnunarafurðir sem byggja á tiltækum víddargildum.</p><p>Frekari upplýsingar er að finna í [Búa til afbrigði fyrir hönnunarafurðir](engineering-variants.md).</p> |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
