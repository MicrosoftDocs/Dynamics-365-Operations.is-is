---
title: Yfirlit yfir umsjón hönnunarbreytinga
description: Í þessu efnisatriði er að finna yfirlit yfir umsjón hönnunarbreytinga, sem hjálpar til við að skipuleggja og vinna með afurðarútgáfum, og stjórna lífferlum og hönnunarbreytingum.
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d7c0839ffbea80904ca12d1cba7ba9880f721cdd
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947521"
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

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a>Kveikja á eiginleikum fyrir umsjón hönnunarbreytinga og útgáfuvíddir fyrir kerfið

Áður en hægt er að nota umsjón hönnunarbreytinga þarf að virkja bæði eiginleikann *Umsjón hönnunarbreytinga* og skilgreiningarlykil hans. Ef einnig á að rekja útgáfuvídd afurðanna í færslum (valfrjálst) þarf einnig að virkja eiginleikann *Vídd afurðarútgáfu* og skilgreiningarlykil hans.

Fyrst skal kveikja á eiginleikunum með því að fylgja þessum skrefum.

1. Farðu í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnusvæðið.
1. Athuga með uppfærslur.
1. Kveikið á eiginleikanum sem kallast **Umsjón hönnunarbreytinga**.
1. Ef nota á þetta skal einnig kveikja á eiginleikanum sem kallast **Útgáfa afurðarvíddar**.

Næst skal kveikja á skilgreiningarlyklunum með því að fylgja þessum skrefum.

1. Setjið kerfið í viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Opnið **Kerfisstjórnun \> Setja upp \> Skilgreining leyfis**.
1. Víkkið út hnútinn **Viðskipti**
1. Virkið skilgreiningarlykilinn fyrir aðaleiginleikann með því að velja gátreitinn **Stjórnun hönnunarbreytingar**. (Ekki er nauðsynlegt að stækka hnútinn nema ef einnig á að slökkva á einum eða báðum undireiginleikum hans.)
1. Ef einnig á að nota vídd útgáfunnar skal þá velja gátreitinn **Afurðarvídd - Útgáfa**. (Þessi gátreitur er neðar á listanum, ekki faldaður undir hnútnum **Stjórnun hönnunarbreytinga**.)
1. Slökkvið á viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

> [!IMPORTANT]
> Frá og með apríl 2022 verða leyfislyklarnir fyrir bæði **Stjórnun hönnunarbreytinga** og **Afurðarvídd - Útgáfa** virkjaðir að sjálfgefnu fyrir allar nýja uppsetningar, en þú munt enn geta slökkt á þeim ef á þarf að halda.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
