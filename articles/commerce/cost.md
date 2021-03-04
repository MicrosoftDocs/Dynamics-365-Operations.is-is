---
title: Skilgreining kostnaðar fyrir dreifingarstjórnun pöntunar (DOM)
description: Þetta efnisatriði lýsir skilgreiningu kostnaðar fyrir virkni dreifingarstjórnunar pöntunar (DOM) í Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b96780745e8dd8a6e2b46a3286bf4a6a307d886c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001050"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a>Skilgreining kostnaðar fyrir dreifingarstjórnun pöntunar (DOM)

[!include [banner](../includes/banner.md)]

Fyrirtæki íhuga marga kostnaðaríhluti til að ákvarða bestu staðsetninguna til að uppfylla pöntun frá. Sumir þessara kostnaðaríhluta eru sendingarkostnaður, úrvinnslukostnaður og pökkunarkostnaður. Samsetning þessa kostnaðar er reiknaður til að ákvarða uppfyllingarstaðsetningu.

Þegar fyrsta ítrekun úthlutaðrar pantanastjórnunar (DOM) í Dynamics 365 Commerce fínstillti úthlutun pantana á uppfyllingarstaðsetningar var eingöngu vegalengd tekin með í reikninginn. Vegalengd er ekki það sama og kostnaður þótt hægt sé að gera ráð fyrir henni í kostnaði. Til dæmis kostar sendingarmáti að næturlagi meira en þriggja daga sending eða sjö daga sending sem felur í sér sömu vegalengdina.

Eiginleiki kostnaðarskilgreiningar gerir söluaðilum kleift að skilgreina og grunnstilla aukalega kostnaðaríhluti sem verða reiknaðir og hafðir með til að ákvarða bestu staðsetninguna til að uppfylla pöntunarlínur frá.

Þegar kostnaðaríhlutir eru skilgreindir notar DOM-leysarinn eingöngu þessar kostnaðarskilgreiningar til að ákvarða bestu staðsetninguna til að uppfylla pöntun. Hann tekur ekki vegalengd inn sem kostnað. Ef hins vegar engir kostnaðaríhlutir eru skilgreindir notar DOM-leysarinn vegalengd sem kostnað til að ákvarða bestu staðsetninguna til að uppfylla pöntun.

## <a name="set-up-cost-components"></a>Uppsetning kostnaðaríhluta

Hægt er að skilgreina tvær megingerðir kostnaðaríhluta í kerfinu: **Sending** og **Annað**.

Báðar gerðir kostnaðaríhluta styðja marga útreikningsgrunna eins og sýnt er í eftirfarandi töflu.

<table>
<thead>
<tr>
<th>Gerð kostnaðaríhlutar</th>
<th>Grunnur útreikninga</th>
</tr>
</thead>
<tbody>
<tr>
<td>Sending</td>
<td>
<ul>
<li>Einfalt</li>
<li>Lagskipt</li>
</ul>
</td>
</tr>
<tr>
<td>Annað</td>
<td>
<ul>
<li>Sölupöntun</li>
<li>Sölulínur</li>
<li>Staðsetning</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a>Gerð íhlutar fyrir sendingarkostnað

Þessi hluti útskýrir hvernig á að setja upp hverja samsetningu fyrir sig fyrir kostnaðaríhlut af gerðinni **Sending** og útreikningsgrunn fyrir sendingarkostnað. Þar er einnig útskýrt hvernig DOM-leysarinn notar hverja samsetningu.

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a>Gerð kostnaðaríhlutar = sending og útreikningsgrunnur = einfaldur

Ef samsetning kostnaðaríhlutar af gerðinni **Sending** og útreikningsgrunnurinn **Einfaldur** er notuð byggist sendingarkostnaður fyrir afhendingarmáta annaðhvort á flötum kostnaði eða vegalengd.

Setja verður upp eftirfarandi reiti fyrir þessa samsetningu:

- **Kostnaðarstuðull** – Færið inn einkvæmt kennimerki fyrir kostnaðarstuðul.
- **Lýsing** – Færið inn heiti og lýsingu á kostnaðarstuðli.
- **Upphafsdagur** og **Lokadagur** – Hægt er að nota þessa reiti til að takmarka kostnaðarstuðul fyrir tiltekið tímabil. Ef þessir reitir eru skildir eftir auðir gildir kostnaðarstuðullinn um óákveðinn tíma.
- **Virkur** – Segið til um hvort kostnaðarstuðull sé virkur. DOM tekur aðeins virka kostnaðarstuðla til greina sem tengjast uppfyllingarsniði.
- **Fyrirtæki** – Tilgreinið lögaðila sem kostnaðarstuðull er skilgreindur fyrir. Allar línur útreikningsskilyrðis verður að vera fyrir sama lögaðilann.
- **Afhendingarmátar** – Tilgreinið afhendingarmáta sem kostnaður er skilgreindur fyrir.
- **Gerð útreiknings** – Tilgreinið hvernig reikna eigi kostnað fyrir tiltekinn afhendingarmáta. Tvær gerðir útreiknings eru studdar:

    - **Fastur** – Flatur kostnaður er notaður fyrir afhendingarmáta. Ef þessi útreikningsgerð er valin skilgreinir reiturinn **Kostnaður** flatan kostnað.
    - **Á hverja fjarlægðareiningu** – Kostnaður fyrir afhendingarmáta er reiknaður sem kostnaðarvirðið sem er skilgreint í reitnum **Kostnaður** margfaldað með vegalengdinni milli afhendingaraðseturs og staðsetningar.

- **Kostnaður** – Tilgreinið kostnaðarvirði sem er notað í tengslum við reitinn **Gerð útreiknings** til að reikna út kostnað á afhendingarmáta.

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a>Gerð kostnaðaríhlutar = sending og útreikningsgrunnur = lagskiptur

Ef samsetning kostnaðaríhlutar af gerðinni **Sending** og útreikningsgrunnurinn **Lagskiptur** er notuð byggist sendingarkostnaður fyrir afhendingarmáta annaðhvort á flötum kostnaði eða vegalengd. Í þessari samsetningu byggist vegalengdin hins vegar á lagskiptu fjarlægðarbili.

Setja verður upp eftirfarandi reiti fyrir þessa samsetningu:

- **Kostnaðarstuðull** – Færið inn einkvæmt kennimerki fyrir kostnaðarstuðul.
- **Lýsing** – Færið inn heiti og lýsingu á kostnaðarstuðli.
- **Sjálfgefinn kostnaður** – Tilgreinið kostnað sem á að nota fyrir afhendingarmáta ef vegalengdin milli afhendingaraðseturs og staðsetningar fellur ekki undir neina af lagskiptu vegalengdunum fyrir afhendingarmáta.
- **Upphafsdagur** og **Lokadagur** – Hægt er að nota þessa reiti til að takmarka kostnaðarstuðul fyrir tiltekið tímabil. Ef þessir reitir eru skildir eftir auðir gildir kostnaðarstuðullinn um óákveðinn tíma.
- **Virkur** – Segið til um hvort kostnaðarstuðull sé virkur. DOM tekur aðeins virka kostnaðarstuðla til greina sem tengjast uppfyllingarsniði.
- **Fyrirtæki** – Tilgreinið lögaðila sem kostnaðarstuðull er skilgreindur fyrir. Allar línur útreikningsskilyrðis verður að vera fyrir sama lögaðilann.
- **Afhendingarmátar** – Tilgreinið afhendingarmáta sem kostnaður er skilgreindur fyrir.
- **Tegund vegalengdar** – Tilgreinið hvort skilgreining á lagskiptri vegalengd sé fyrir flug eða akstur.
- **Fjarlægðareiningar** – Tilgreinið einingu sem lagskipt vegalengd er mæld í.
- **Fjarlægð frá** – Tilgreinið upphafsbil fyrir lagskipta vegalengd.
- **Fjarlægð til** – Tilgreinið lokabil fyrir lagskipta vegalengd.
- **Gerð útreiknings** – Tilgreinið hvernig reikna eigi kostnað fyrir tiltekinn afhendingarmáta og lagskipta vegalengd. Tvær gerðir útreiknings eru studdar:

    - **Fastur** – Flatur kostnaður er notaður fyrir afhendingarmáta. Ef þessi útreikningsgerð er valin skilgreinir reiturinn **Kostnaður** flatan kostnað.
    - **Á hverja fjarlægðareiningu** – Kostnaður fyrir afhendingarmáta og lagskipta vegalengd er reiknaður sem kostnaðarvirðið sem er skilgreint í reitnum **Kostnaður** margfaldað með vegalengdinni milli afhendingaraðseturs og staðsetningar.

- **Kostnaður** – Tilgreinið kostnaðarvirði sem er notað í tengslum við reitinn **Gerð útreiknings** til að reikna út kostnað á afhendingarmáta.

> [!NOTE]
> - Þegar lagskiptar vegalengdir eru skilgreindar sannprófar kerfið hvort vegalengdir vanti eða þær skarist á.
> - Tegund vegalengdar sem er notuð fyrir afhendingarmáta verður að vera sú sama fyrir allar lagskiptu vegalengdirnar.

### <a name="other-cost-component-type"></a>Önnur gerð kostnaðaríhlutar

Þessi hluti útskýrir hvernig á að setja upp hverja samsetningu fyrir sig fyrir kostnaðaríhlut af gerðinni **Annar** og aðra kostnaðargerð fyrir kostnað án sendingar. Þar er einnig útskýrt hvernig DOM-leysarinn notar hverja samsetningu.

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a>Gerð kostnaðaríhlutar = annar og önnur kostnaðargerð = sölupöntun

Samsetning fyrir kostnaðaríhlut af gerðinni **Annar** og annan kostnað af gerðinni **Sölupöntun** er notuð til að skilgreina kostnað án sendingar á stigi sölupöntunar.

Setja verður upp eftirfarandi reiti fyrir þessa samsetningu:

- **Kostnaðarstuðull** – Færið inn einkvæmt kennimerki fyrir kostnaðarstuðul.
- **Lýsing** – Færið inn heiti og lýsingu á kostnaðarstuðli.
- **Upphafsdagur** og **Lokadagur** – Hægt er að nota þessa reiti til að takmarka kostnaðarstuðul fyrir tiltekið tímabil. Ef þessir reitir eru skildir eftir auðir gildir kostnaðarstuðullinn um óákveðinn tíma.
- **Virkur** – Segið til um hvort kostnaðarstuðull sé virkur. DOM tekur aðeins virka kostnaðarstuðla til greina sem tengjast uppfyllingarsniði.
- **Kostnaður** – Tilgreinið kostnaðarvirði fyrir kostnað án sendingar á stigi sölupöntunar.

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a>Gerð kostnaðaríhlutar = annar og önnur kostnaðargerð = sölulína

Samsetning fyrir kostnaðaríhlut af gerðinni **Annar** og annan kostnað af gerðinni **Sölulína** er notuð til að skilgreina kostnað án sendingar á stigi sölulínu.

Setja verður upp eftirfarandi reiti fyrir þessa samsetningu:

- **Kostnaðarstuðull** – Færið inn einkvæmt kennimerki fyrir kostnaðarstuðul.
- **Lýsing** – Færið inn heiti og lýsingu á kostnaðarstuðli.
- **Upphafsdagur** og **Lokadagur** – Hægt er að nota þessa reiti til að takmarka kostnaðarstuðul fyrir tiltekið tímabil. Ef þessir reitir eru skildir eftir auðir gildir kostnaðarstuðullinn um óákveðinn tíma.
- **Virkur** – Segið til um hvort kostnaðarstuðull sé virkur. DOM tekur aðeins virka kostnaðarstuðla til greina sem tengjast uppfyllingarsniði.
- **Kostnaður** – Tilgreinið kostnaðarvirði fyrir kostnað án sendingar á stigi sölupöntunarlínu.

#### <a name="cost-component-type--other-and-other-cost-type--location"></a>Gerð kostnaðaríhlutar = annar og önnur kostnaðargerð = staðsetning

Samsetning fyrir kostnaðaríhlut af gerðinni **Annar** og annan kostnað af gerðinni **Staðsetning** er notuð til að skilgreina kostnað án sendingar fyrir flokk staðsetninga eða eina staðsetningu.

Setja verður upp eftirfarandi reiti fyrir þessa samsetningu:

- **Kostnaðarstuðull** – Færið inn einkvæmt kennimerki fyrir kostnaðarstuðul.
- **Lýsing** – Færið inn heiti og lýsingu á kostnaðarstuðli.
- **Upphafsdagur** og **Lokadagur** – Hægt er að nota þessa reiti til að takmarka kostnaðarstuðul fyrir tiltekið tímabil. Ef þessir reitir eru skildir eftir auðir gildir kostnaðarstuðullinn um óákveðinn tíma.
- **Virkur** – Segið til um hvort kostnaðarstuðull sé virkur. DOM tekur aðeins virka kostnaðarstuðla til greina sem tengjast uppfyllingarsniði.
- **Uppfyllingarflokkur** – Tilgreinið flokk staðsetninga sem kostnaður án sendingar er skilgreindur fyrir.
- **Uppfyllingarflokkur** – Tilgreinið staðsetningu sem kostnaður án sendingar er skilgreindur fyrir.

    > [!NOTE]
    > Ekki er hægt að tilgreina uppfyllingarflokk og uppfyllingarstaðsetningu í sömu línunni fyrir útreikningsskilyrði sem byggir á staðsetningu.

- **Kostnaður** – Tilgreinið kostnaðarvirði fyrir kostnað án sendingar á stigi uppfyllingarflokks eða uppfyllingarstaðsetningar.

> [!IMPORTANT]
> Til að DOM taki þennan kostnað til greina þegar hann er keyrður þarf að bæta kostnaðarstuðli við viðeigandi uppfyllingarsnið.
