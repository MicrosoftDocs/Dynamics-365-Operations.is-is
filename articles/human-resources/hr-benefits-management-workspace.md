---
title: Vinnusvæði fríðindastjórnunar
description: Þetta efnisatriði lýsir Fríðindastjórnun vinnusvæðinu í Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e6cc1432e108c74706dea124a62024272e65b6c1
ms.sourcegitcommit: 47a3ad71210c7ac84d0c25e913c440b5ba205282
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2021
ms.locfileid: "7512475"
---
# <a name="benefits-management-workspace"></a>Vinnusvæði fríðindastjórnunar

[!include [applies to](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

Þetta efnisatriði lýsir **Fríðindastjórnun** vinnusvæðinu í Dynamics 365 Human Resources.

> [!NOTE]
> Til að skoða **Fríðindastjórnun** vinnusvæðið verður fyrst að virkja eiginleikann **(Forskoðun) Vinnusvæði fríðindastjórnunar** í eiginleikastjórnun. Frekari upplýsingar um hvernig forskoðunareiginleikar eru virkjaðir er að finna í [Vinna með eiginleika](hr-admin-manage-features.md).<br><br>![Virkja vinnusvæði fríðindastjórnunar.](./media/hr-benefits-management-workspace-enable.png)

Vinnusvæðið **Fríðindastjórnun** veitir yfirlit yfir fríðindaatriði sem þú þarft að skoða. Á þessari síðu er hægt að sjá:

- Samtölur fyrir vörur sem bíða aðgerðar
- Starfskraftar með óstaðfest val
- Starfsmenn sem skráðu sig nýlega fyrir fríðindum
- Starfskraftar með viðburði í framtíðinni
- Nýjar ráðningar sem ekki hafa verið skráðar
- Starfskraftar með virka viðburði
- Starfsmenn með opnar skráningar sem hafa ekki enn skráð sig fyrir neinum áætlunum

![Vinnusvæði fríðindastjórnunar.](./media/hr-benefits-management-workspace.png)

## <a name="view-action-items"></a>Skoða aðgerðaatriði

Hægt er að skoða aðgerðaatriðin með því að velja reit eða flipa. Ef flipi er valinn er hægt að skoða og velja starfsmenn á síðu vinnusvæðisins.

![Aðgerðaratriði.](./media/hr-benefits-management-workspace-action-items.png)

Ef þú velur spjald ferðu á síðuna fyrir það svæði. Til dæmis ef einhver af þessum reitum sem birtast á síðunni **Fríðindaáætlun starfsmanna** eru valdir, síaðir fyrir starfsmenn, þarf að grípa til aðgerða:

- **Óstaðfest val**
- **Opna skráningar með engum skráðum áætlunum**
- **Skráður í fríðindi**
- **Nýr starfsmaður ekki skráður**

![Fríðindaáætlanir starfskrafts.](./media/hr-benefits-management-workspace-plans.png)

Ef **Virkir viðburðir** eða **Viðburðir í framtíðinni** er valið verður farið yfir á lista yfir virka viðburði og viðburði í framtíðinni.

![Viðburðir.](./media/hr-benefits-management-workspace-life-events.png)

## <a name="processing"></a>Í vinnslu

Til að vinna úr hæfi skráningar, viðburðum eða uppfærslur á taxtabreytingum skal velja viðeigandi atriði á yfirlitsstikunni.

![Í vinnslu.](./media/hr-benefits-management-workspace-processing.png)

Til að skoða vinnu niðurstaðna skal velja **Vinna niðurstöður** á síðunni.

![Vinna úr niðurstöðum.](./media/hr-benefits-management-workspace-process-results.png)

Frekari upplýsingar um meðhöndlun fríðinda eru í:

- [Vinna úr fríðindahæfni](hr-benefits-process-enrollment-eligibility.md)
- [Vinna úr breytingum á viðburðum](hr-benefits-process-life-event-changes.md)
- [Vinna úr hæfni viðburðar](hr-benefits-process-life-event-eligibility.md)
- [Vinna úr viðburðum](hr-benefits-process-life-events.md)
- [Vinna úr breytingum á hlutfalli](hr-benefits-process-rate-changes.md)

## <a name="change-period"></a>Breyta tímabili

Til að skoða annað fríðindatímabil skal velja það úr fellilistanum **Tímabil**.

![Breyta tímabili.](./media/hr-benefits-management-workspace-period.png)


## <a name="open-enrollment-tab"></a>Opna skráningarflipa

Hægt er að skoða aðgerðaatriðin með því að velja reit eða flipa. Ef flipi er valinn er hægt að skoða og velja starfsmenn á síðu vinnusvæðisins.
Í flipanum **Opin skráning** eru lykilmælikvarðar fyrir opna skráningarferlið. 

Upplýsingar um opna skráningu birtast 30 dögum fyrir **Upphafsdag skráningar**. Þetta er skilgreint í uppsetningu **Tímabila** í **Fríðindastjórnun** > **Tenglar** > **Tímabil** í reitnum **Upphafsdagur skráningar**.  Til að breyta þessari stillingu skal fara í **Samnýttar færibreytur fyrir mannauð** > **Fríðindastjórnun** > **Valkostir opinnar skráningar** og uppfæra reitinn **Fjöldi af**.  

Eftirfarandi upplýsingar eru tiltækar í flipanum **Opin skráning**:
 - Starfsmenn sem hafa ekki hafið opna skráningarferlið
 - Starfsfólk sem er að kjósa
 - Starfsfólk sem hefur lokið við að kjósa
 - Óstaðfest val

**Samantektarreitir**

- **Ekki hafið** – Reiturinn **Ekki hafið** sýnir fjölda starfsmanna sem hafa ekki hafið skráningarferlið. Reiturinn **Ekki hafið** er síaður listi sem sýnir aðeins starfsmenn sem eru ekki með neinar áætlanir valdar, felldar niður eða útskráðar fyrir tímabil opinnar skráningaráætlunar. Áskildar áætlanir eru hunsaðar og ekki hafðar með vegna þess að þær eru sjálfgefið valdar fyrir starfsmanninn.  Þú getur rakið þig til baka í þennan reit til að sjá lista yfir starfsmenn sem hafa ekki hafið opið skráningarferli á síðunni **Fríðindaáætlun starfsmanns**.

  > [!NOTE]
  > Ef þú vilt ekki fylgjast með framgangi opinnar skráningar fyrir **Áætlunargerð** getur þú útilokað hana með því að fara í **Fríðindastjórnun** > **Tenglar** > **Færibreytur sjálfsafgreiðslu starfsmanns** > **Uppsetning reita fyrir fríðindaáætlanir** og uppfæra reitinn **Rekja framgang opinnar skráningar**.  Þú gætir til dæmis hafa búið til áætlanir þar sem er **Áætlunargerð** = **Önnur**. Þessar áætlanir gætu verið valfrjálsar áætlanir sem þú vilt ekki fylgjast með framgangi skráningar. Ef þú velur ekki þessa áætlunargerð verða áætlanir af þessari gerð hunsaðar þegar rakin er framvinda eða lok skráningar í flipanum **Opin skráning**. Þessi stilling á við um áætlunargerðina sem er valin fyrir öll tímabil og lögaðila.

- **Í vinnslu** – Reiturinn **Í vinnslu** gefur upp fjölda starfsmanna sem eru með val í vinnslu. Reiturinn **Í vinnslu** er síaður listi sem sýnir aðeins starfsmenn sem eru með a.m.k. eina niðurfellda eða valda áætlun. Áskildar áætlanir eru hunsaðar og ekki hafðar með vegna þess að þær eru sjálfgefið valdar fyrir starfsmanninn. Þú getur rakið þig til baka úr þessum reit til að sjá valdar og niðurfelldar áætlanir á síðunni **Magnuppfærsla fríðindaáætlana starfskrafts**.

- **Skráður í fríðindi** – Reiturinn **Skráður í fríðindi** gefur upp fjölda starfsmanna sem eru að fullu skráðir í fríðindi. Reiturinn **Skráður í fríðindi** er síaður listi sem sýnir starfsmenn sem hafa annaðhvort valið eða fellt niður allar áætlanir. Fyrirspurnin mun útiloka áætlanir þar sem opin skráning er ekki rakin á síðunni **Færibreytur sjálfsafgreiðslu starfsmanns**. Þú getur rakið þig til baka úr þessum reit til að sjá lista yfir starfsmenn á síðunni **Fríðindaáætlanir starfskrafts**.

- **Óstaðfest val** – Reiturinn **Óstaðfest val** sýnir fjölda starfsmanna sem eru með áætlanir sem eru valdar eða niðurfelldar og þurfa staðfestingu. Þú getur rakið þig til baka úr þessum reit til að sýna síðuna **Magnuppfærsla fríðindaáætlana starfskrafts**.

**Aðgerð**

- **Ekki hafið** - Flipinn **Ekki hafið** sýnir lista yfir starfsmenn sem hafa ekki hafið skráningarferlið. Reiturinn **Ekki hafið** er síaður listi sem sýnir starfsmenn sem eru ekki með neinar áætlanir valdar, felldar niður eða útskráðar fyrir tímabil opinnar skráningaráætlunar. Áskildar áætlanir eru hunsaðar og ekki hafðar með vegna þess að þær eru sjálfgefið valdar fyrir starfsmanninn. Þú getur rakið þig til baka á starfsmanninn til að sýna síðuna **Upplýsingar um fríðindaáætlanir starfskrafts**.

- **Val í vinnslu** - Flipinn **Val í vinnslu** sýnir lista yfir starfsmenn sem eru með val í vinnslu. Reiturinn **Val í vinnslu** er síaður listi sem sýnir starfsmenn sem eru með a.m.k. eina niðurfellda eða valda áætlun. Áskildar áætlanir eru hunsaðar og ekki hafðar með vegna þess að þær eru sjálfgefið valdar fyrir starfsmanninn. Þú getur rakið þig til baka á starfsmanninn til að sýna síðuna **Upplýsingar um fríðindaáætlanir starfskrafts**.

## <a name="view-more-options"></a>Skoða fleiri valkosti

Til að sjá frekari upplýsingar og/eða frekari aðgerðir skal velja **Tenglar**.

![Tenglar.](./media/hr-benefits-management-workspace-links.png)

## <a name="see-also"></a>Sjá einnig

[Yfirlit fríðindastjórnunar](hr-benefits-management-overview.md)
