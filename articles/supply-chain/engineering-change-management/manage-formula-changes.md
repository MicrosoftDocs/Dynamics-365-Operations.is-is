---
title: Stjórna breytingum á formúlum og innihaldsefnum þeirra
description: Í þessu efnisatriði er lýst hvernig eigi að stjórna formúlum og stjórna breytingum á aðalgögnum framleiðsluferlis.
author: t-benebo
ms.date: 05/19/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 825cc5b9355695a648c857e5197b5b93a21fdb43
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115194"
---
# <a name="manage-changes-in-formulas-and-their-ingredients"></a>Stjórna breytingum á formúlum og innihaldsefnum þeirra

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Ef notaðir eru möguleikar framleiðsluferlis hjá Microsoft Dynamics 365 Supply Chain Management er einnig hægt að nota tengda möguleika formúlustjórnunar til að hafa umsjón með eftirfarandi breytingum:

- **Vöruformúla og áætlanagerð:** Hafa umsjón með breytingum á innihaldsefnum formúlu og aukaafurðum og hliðarafurðum þeirra.
- **Aukaafurðir og hliðarafurðir:** Breyta magni og öðrum upplýsingum um aukaafurðir og hliðarafurðir í formúlu.
- **Vörur með framleiðsluþyngd:** Hafa umsjón með breytingum á vörum með framleiðsluþyngd.

## <a name="turn-on-this-feature-in-your-system"></a>Kveikja á þessum eiginleika í kerfinu

Til að nota þennan eiginleika verður að ljúka eftirfarandi verkum:

1. Virkjið eiginleikann fyrir *umsjón hönnunarbreytinga* og skilgreiningarlykla hans eins og lýst er í [Yfirlit yfir umsjón hönnunarbreytinga](product-engineering-overview.md). Eins og minnst er á í þessu efnisatriði skal einnig ganga úr skugga um að virkja leyfislykilinn **Breytingastjórnun fyrir framleiðsluferli** sem er faldaður fyrir neðan leyfislykilinn **Umsjón hönnunarbreytinga**.
1. Kveikið að *Stjórna breytingum á formúlum og innihaldsefnum þeirra* eiginleikanum í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="feature-naming-conventions"></a>Eiginleiki nafngiftavenja

Í notandaviðmóti og fylgiskjölum Supply Chain Management er yfirleitt vísað í virkni breytingastjórnunar sem *umsjón hönnunarbreytinga* og yfirleitt er vísað í stýrðar afurðir sem *hönnunarafurðir*. Þótt þessi hugtök séu yfirleitt ekki tengd við stjórnun formúla fyrir framleiðsluferli ætti einfaldlega að líta á breytingastjórnun hönnunar sem breytingastjórnun og líta á hönnunarafurðir sem afurðir með útgáfu.

## <a name="work-with-formula-change-management-features"></a>Vinna með eiginleika formúlubreytingastjórnunar

Eftirfarandi listi tekur saman hvernig eiginleikar hönnunarbreytingastjórnunar eiga við um formúlustjórnun. Hann veitir einnig tengla í frekari upplýsingar. Þar sem breytingastjórnun formúlu nýtir sér eiginleika hönnunarbreytingastjórnunar er sniðugt að kynna sér hvernig breytingastjórnun hönnunar virkar almennt þannig að hægt sé að nota hana til að stjórna formúlum og innihaldsefnum þeirra.

- **Miðlæg gagnastjórnun afurðar** – Setjið upp fyrirtæki sem í gegnum stýrt útgáfuferli tryggir að nákvæm og viðeigandi afurðargögn séu í boði fyrir notendur í fyrirtækinu. Frekari upplýsingar er að finna í [Hönnunarfyrirtæki og reglur um eignarétt gagna](engineering-org-data-ownership-rules.md).
- **Útgáfa afurðar** – Rekið breytingar á afurðum í gegnum afurðarútgáfur og stjórnið afurðinni í gegnum öll stig aðfangakeðjunnar. Á þennan hátt er hægt að rekja breytingarnar í samsetningunni. Frekari upplýsingar eru í [Hönnunarútgáfur og flokkar hönnunarafurðar](engineering-versions-product-category.md).
- **Líftímastjórnun afurðar** – Stjórnið sýnileika afurðargagna í gegnum fyrirtækið og stjórnið framboði á útgáfum afurðar á hverju stigi aðfangakeðjunnar. Þú hefur ítarlega stjórn á því hvenær hægt er að nota útgáfu afurðar í tilteknum viðskiptaferlum og þú getur búið til þínar eigin líftímastöður sem henta viðskiptaþörfum þínum. Frekari upplýsingar er að finna í [Líftímastöður afurðar og færslur](product-lifecycle-state-transactions.md).
- **Breytingastjórnun formúlu** – Notendur í gegnum fyrirtækið geta óskað eftir breytingum á formúlum. Notið breytingaraðir til að meta og skrá áhrif framlagðra breytinga. Bætið við verkflæðum til að stjórna breytingaferlinu og útgáfu nýrra útgáfa afurðarinnar og formúlum hennar. Frekari upplýsingar eru í [Umsjón hönnunarbreytinga](engineering-change-management.md).
- **Undirbúningsstjórnun** – Notið kerfisathugunir og leiðarvísa (spurningalista og gátlista) til að ganga úr skugga um að öll nauðsynleg afurðargögn séu færð inn að fullu áður en afurðin er gefin út. Frekari upplýsingar er að finna í [Undirbúningur afurðar](product-readiness.md).
- **Aukin virkni afurðarlosunar** – Losið fullskilgreindar útgáfur afurðar og formúlu hennar úr fyrirtæki (lögaðila) yfir í aðra lögaðila. Það er meira að segja hægt að ákveða hvort þurfi að fara yfir eða breyta afurðarupplýsingunum fyrir útgáfu. Frekari upplýsingar er að finna í [Skipulag afurðarútgáfu](release-product-structure.md).

Athugið að flest efnisatriðin sem tengt er við í fyrri lista gefa upp dæmi sem byggja á uppskriftum. Formúlur virka þó á svipaðan hátt. Hér eru nokkur viðbótarhugtök sem gagnlegt er að vita þegar breytingastjórnun er notuð (eða eingöngu breytingastjórnun formúlu) til að stjórna formúlum og uppskriftum:

- Fyrir hvern [flokk hönnunarafurðar](engineering-versions-product-category.md) er hægt að tilgreina framleiðslugerðina (uppskrift, formúlu eða áætlunarvöru). Einnig er hægt að tilgreina hvort þörf sé á stuðningi við framleiðsluþyngd fyrir afurðir sem nota þann flokk.
- Aukaafurðir og hliðarafurðir eru ekki hönnunarafurðir. Þær fá þar af leiðandi ekki útgáfur. Ef þarf að breyta þeim skal einfaldlega stofna nýja afurð. Þessi nálgun auðveldar utanumhald.
- Hægt er að stjórna endanlegum vörum sem eru uppskriftir og eru með undireiningar formúluvöru. Virknin virkar fyrir allar samsetningar á uppskriftum sem innihalda formúlur og/eða formúlur sem innihalda uppskriftir.
