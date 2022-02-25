---
title: Yfirlit yfir verkfræðibreytingastjórnun (inniheldur myndband)
description: Í þessu efnisatriði er að finna yfirlit yfir umsjón hönnunarbreytinga, sem hjálpar til við að skipuleggja og vinna með afurðarútgáfum, og stjórna lífferlum og hönnunarbreytingum.
author: t-benebo
ms.date: 01/11/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 54d91d009d70194dfc91c8c855e0088f9de01718
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103814"
---
# <a name="engineering-change-management-overview"></a>Yfirlit yfir umsjón hönnunarbreytinga

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Samantekt eiginleika

Framleiðendur nútímans krefjast öflugrar vörugagnastjórnunar, útgáfustýringar og verkfræðilegrar breytingastjórnunar til að ná árangri í heimi sífellt minnkandi vörulífs, aukinna gæða- og áreiðanleikakrafna og aukinnar áherslu á vöruöryggi.

Verkfræðileg breytingastjórnun færir uppbyggingu og aga inn í vörugagnastjórnunarferlið og gerir kleift að skilgreina, gefa út og endurskoða vörur á stýrðan hátt sem er studd af verkflæði. Með vöruútgáfum og verkfræðilegri breytingastjórnun geturðu skjalfest, metið áhrif og beitt verkfræðilegum breytingum í gegnum allan líftíma vöru.

Umsjón hönnunarbreytinga sem hjálpar til við að skipuleggja og vinna með afurðarútgáfur, og stjórna lífferlum og hönnunarbreytingum. Hér er listi yfir helstu eiginleikana:

- Útgáfa vöru
- Aukin virkni afurðarlosunar sem gerir þér kleift að viðhalda aðalgögnum afurðar í einum lögaðila (hönnunarfyrirtækinu) og gefa út fullskilgreinda útgefna afurð til annarra lögaðila
- Reglur fyrir staðfestingu á því að nauðsynlegar upplýsingar séu slegnar inn áður en afurðarútgáfa er virkjuð (undirbúningsathugun)
- Bætt líftímastjórnun með ítarlegum stýringum fyrir það hvenær er hægt að nota útgefna afurð í tilteknum viðskiptaferlum
- Breytingarbeiðnir hönnunar sem eru studdar af verkflæði
- Breytingarpantanir hönnunar sem eru studdar af verkflæði

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4HE6B]

Fyrra myndbandið ([Breyta stjórnunargetu í Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) er innifalið í [Spilunarlisti fyrir fjármál og rekstur](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) í boði á YouTube.

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>Kveikja á eiginleikum fyrir umsjón hönnunarbreytinga fyrir kerfið

Áður en hægt er að nota umsjón hönnunarbreytinga þarf að virkja bæði eiginleikann *Umsjón hönnunarbreytinga* og skilgreiningarlykil hans. Ef einnig á að rekja útgáfuvídd afurðanna í færslum (valfrjálst) þarf einnig að virkja bæði eiginleikann *Vídd afurðarútgáfu* og skilgreiningarlykil hans. Eftir að þessi skilyrði hafa verið sett upp eins og þörf er á verður hægt að nota aðra valfrjálsa eiginleika til stjórnun hönnunarbreytinga.

### <a name="turn-the-basic-engineering-change-management-features-on-or-off"></a>Kveiktu eða slökktu á grunneiginleikum verkfræðibreytingastjórnunar

Til að kveikja eða slökkva á grunneiginleikum verkfræðibreytingastjórnunar skaltu fylgja þessum skrefum. Frá og með Supply Chain Management útgáfu 10.0.25 er *Verkfræðibreytingastjórnun* kveikt er á eiginleikum sjálfgefið.

1. Farðu í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnusvæðið.
1. Athuga með uppfærslur.
1. Snúðu eiginleikanum sem heitir *Verkfræðibreytingastjórnun* kveikt eða slökkt, eftir þörfum.
1. Ef þú vilt fylgjast með útgáfuvídd afurða í færslum (valfrjálst) skaltu kveikja á eiginleikanum sem er nefndur *Vöruvíddarútgáfa*.

### <a name="turn-the-required-configuration-keys-on-or-off"></a>Kveiktu eða slökktu á nauðsynlegum stillingarlyklum

Næst skal kveikja á skilgreiningarlyklunum með því að fylgja þessum skrefum. Þetta er ekki sjálfgefið kveikt.

1. Setjið kerfið í viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Opnið **Kerfisstjórnun \> Setja upp \> Skilgreining leyfis**.
1. Víkkið út hnútinn **Viðskipti**
1. Virkjaðu eða slökktu á stillingarlykli fyrir aðaleiginleikann með því að nota **Verkfræðibreytingastjórnun** gátreit.
1. Stækkaðu hnútinn **Umsjón hönnunarbreytinga** og veldu eða hreinsaðu eftirfarandi gátreiti eftir þörfum (eftir því hvaða eiginleika á að nota):

    - **Leit að eigind** – Veldu þennan gátreit til að virkja [leitareiginleika eigindar](engineering-attributes-and-search.md). Við mælum með því að þessi eiginleiki sé virkur en hægt er að hreinsa þennan gátreit ef ekki á að nota hann.
    - **Breytingastjórnun fyrir framleiðsluferli** – Veldu þennan gátreit ef þú vilt nota eiginleika fyrir umsjón hönnunarbreytinga til að stjórna breytingum í formúlum fyrir framleiðsluferli. Ef þú þarft ekki að stjórna formúlum geturðu hreinsað þennan gátreit. Frekari upplýsingar eru í [Stjórna breytingum á formúlum og innihaldsefnum þeirra](manage-formula-changes.md)

1. Ef einnig á að nota vídd útgáfunnar skal velja gátreitinn **Afurðarvídd - Útgáfa**. (Þessi gátreitur er neðar á listanum, ekki hreiður undir **Verkfræðibreytingastjórnun** hnút.) Þú getur hreinsað þennan gátreit ef þú þarft ekki þennan eiginleika.
1. Slökkvið á viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Gagnagrunnurinn verður að vera samstilltur til að tryggja að stillingarlyklar séu rétt uppfærðir til að endurspegla breytingar þínar. Gerðu eitt af eftirfarandi skrefum, eftir því hvers konar umhverfi þú ert að vinna við:
    - **Fyrir Tier 1 (þróunar) umhverfi** : Opnaðu verkefnið þitt í Microsoft Visual Studio og veldu síðan **Dynamics 365 \> Samstilla gagnagrunn \> Samstilla**.
    - **Fyrir Tier 2 (og hærra) umhverfi** : Gagnagrunnurinn samstillist sjálfkrafa eftir að þú setur umhverfið í og úr viðhaldsham, svo þú getur sleppt þessu skrefi.

### <a name="turn-on-additional-engineering-change-management-features"></a>Kveikja á eiginleikum fyrir umsjón frekari hönnunarbreytinga

Eftir að þú kveikir á eiginleikum fyrir umsjón grunnhönnunarbreytinga og virkjar skilgreiningarlykla þeirra, er nokkrum eiginleikum fyrir umsjón frekari hönnunarbreytinga bætt við eiginleikastjórnun. Hver þessara eiginleika er sýndur undir einingunni **Umsjón hönnunarbreytinga**. Eftirfarandi tafla lýsir hverjum valfrjálsum eiginleika og veitir tengla fyrir frekari upplýsingar. Frá og með Supply Chain Management útgáfu 10.0.25 er sjálfgefið kveikt á öllum þessum eiginleikum, en þú getur samt valið að slökkva á þeim.

| Eiginleikaheiti í eiginleikastjórnun | Lýsing | Staða eiginleika |
|---|---|---|
| Virkja breytingastjórnun á fyrirliggjandi afurðum | <p>Þessi eiginleiki gerir þér kleift að umbreyta núverandi afurðum í hönnunarafurðir svo að þú getir haft umsjón með þeim í gegnum stjórnun hönnunarbreytinga.</p><p>Frekari upplýsingar eru í [Virkja breytingastjórnun á fyrirliggjandi afurðum](change-management-existing-products.md).</p> |
| Hönnunartilkynningar fyrir framleiðslu | <p>Þegar afurð er breytt í hönnun getur verið mikilvægt að tilkynna framleiðslu um þessar breytingar. Á þann hátt geta starfsmenn framleiðslu gripið til viðeigandi ráðstafana, t.d. skipta út íhlut, skipta um uppskriftir eða leið. Þessi eiginleiki gerir þér kleift að tilkynna framleiðslu um breytingar á afurðum sem verið er að framleiða.</p><p>Frekari upplýsingar eru í [Umsjón hönnunarbreytinga](engineering-change-management.md).</p> |
| Bætt erfðaeigind fyrir umsjón hönnunarbreytinga | <p>Þessi eiginleiki einfaldar stjórnun eiginda fyrir fullunnar vörur eða millivörur. Þegar kveikt er á þessum eiginleika er auðveldara að auðkenna allar eigindirnar sem tilheyra vöru og hægt er að velja eigindirnar sem á að dreifa úr þeirri vöru til yfirvöru hennar. Þessi eiginleiki er gagnlegur þegar til dæmis einn þáttur í fullunninni vöru er viðkvæmur, eitraður eða eldfimur vegna þess að þú getur auðveldlega borið kennsl á viðkvæma, eitraða eða eldfima eigindina og dreift henni í fullunna vöru.</p><p>Frekari upplýsingar er að finna í [Hönnunareigindir og leit að hönnunareigind](engineering-attributes-and-search.md).</p> |
| Undirbúningsathuganir afurðar | <p>Þessi eiginleiki gerir þér kleift að setja upp undirbúningsathuganir fyrir staðlaðar (ekki hannaðar) afurðir. Notaðu undirbúningsathuganir afurðar til að ganga úr skugga um að hver afurð sé skilgreind að fullu og að allar reglur séu stilltar áður en boðið verður upp á afurðina og hún notuð í færslum. Ef þessi eiginleiki er gerður óvirkur eftir að hann hefur verið notaður verða öllum fyrirliggjandi undirbúningsathugunum fyrir staðlaðar afurðir eytt.</p><p>Frekari upplýsingar er að finna í [Undirbúningur afurðar](product-readiness.md).</p> |
| Stjórna breytingum á formúlum og innihaldsefnum þeirra | <p>Þessi eiginleiki gerir kleift að fylgjast með breytingum á innihaldsefnum formúlu, aukaafurðum og hliðarafurðum.</p><p>Frekari upplýsingar eru í [Stjórna breytingum á formúlum og innihaldsefnum þeirra](manage-formula-changes.md)</p> |
| Afbrigði útbúið fyrir hönnunarafurðir | <p>Þessi eiginleiki gerir kleift að búa til afbrigði fyrir hönnunarafurðir sem byggja á tiltækum víddargildum.</p><p>Frekari upplýsingar er að finna í [Búa til afbrigði fyrir hönnunarafurðir](engineering-variants.md).</p> |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
