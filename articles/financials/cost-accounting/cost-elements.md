---
title: "Víddir kostnaðareiningar"
description: "Sem ein grunnstólpi kostnaðarbókhalds, eru víddir kostnaðareiningar notaðar til að flokka og rekja hvert kostnaður streymir."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 00a09120116183785d96ed1e18c577d5430fa16b
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="cost-element-dimensions"></a>Víddir kostnaðareiningar

[!include[banner](../includes/banner.md)]


Sem ein grunnstólpi kostnaðarbókhalds, eru víddir kostnaðareiningar notaðar til að flokka og rekja hvert kostnaður streymir. 

Kostnaðareiningu samsvarar afurð sem tengist kostnaði í bókhaldslykum. Nokkurn vegin, getur það verið hvaða gerð einingar á lægsta stigi í fyrirtæki þangað sem kostnaður getur streymt. Kostnaðareiningar sem hugtak nær frá fjárhagslyklum til allra tilfanga sem tengjast kostnaði. Núna, kostnaðarbókhald styður fjárhagslykla.

## <a name="two-types-of-cost-elements"></a>Tveimur gerðum kostnaðareiningar
Til eru tvær gerðir kostnaðareiningar: Aðal kostnaðareining og auka kostnaðareining. Eftirfarandi tafla útskýrir mismuninn á milli tveggja gerða.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Aðal Kostnaðareiningar</strong></td>
<td><strong>Aukakostnaðareining</strong></td>
</tr>
<tr class="even">
<td>Aðal kostnaðareiningar tákna flæði kostnaðar frá fjárhagsbókhald í kostnaðarbókhald. Skipulag kostnaðareiningar samsvarar skipulagi rekstrarreiknings í fjárhagi, þar sem kostnaðareining samsvarar aðallykill. Ekki öll aðallykla þurfa endilega að koma fram sem kostnaðareining samkvæmt þörfum fyrirtækis. Dæmi um aðal kostnaðareiningar innifela:
<ul>
<li>Kostnaður seldra vara</li>
<li>Taka með óbeinan kostnað</li>
<li>Starfsmannakostnaður</li>
<li>Orkukostnaður</li>
</ul></td>
<td>Auka kostnaðareiningar tákna flæði innri kostnaðar þar sem þessi kostnaður er stofnaður og notaður í kostnaðarbókhaldi. Þeir eru notaðir til að tryggja hægt sé að rekja uppruna kostnaðar. Þessar kostnaðareiningar eru notaðir í úthlutun kostnaðar og óbeinn útreikninga. Dæmi um auka kostnaðareiningu innifelur:
<ul>
<li>Framleiðslukostnaður</li>
<li>Framleiðsla, hráefni og kostnaður vegna markaðsstarfs</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a>Víddir kostnaðareiningar og víddarstök kostnaðareiningar.
Kostnaðareiningar eru vísað til sem *víddir kostnaðareiningar* . Einstaka víddargildi kallast *víddarstök kostnaðareiningar*. Til dæmis, þú ert með skipulag fyrir bókhaldslykill US (COA) sem er grunnur fyrir þinni lögboðnu skýrslugerð. Þessi COA er notað sem vídd kostnaðareiningar. Lyklar sem eru aðal kostnaðareiningar, eru sýndar sem víddarstök kostnaðareiningar í kostnaðarbókhaldi. Eftirfarandi skjámyndir sýna dæmi um Aðallykla sem vídd kostnaðareiningar með hennar raunverulegu aðallykla sem víddarstök kostnaðareiningar. 

[![cost-element-dimensions](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)

## <a name="import-cost-element-dimension-members-through-data-connectors"></a>Flytja inn víddarstök kostnaðareiningar með gagnatengjum.
Til að auðvelda uppsetningu víddarstök kostnaðareiningar í kostnaðarbókhald geturðu notað gagnatengi sem eru annað hvort for-innbyggð eða sérstaklega innbygð af þér til að sækja aðal kostnaðareiningar úr einu eða fleiru upprunakerfi.

## <a name="implementation-considerations"></a>Umhugsunarefni fyrir innleiðingu
Þar sem kostnaðareiningar tákna lægsta stigið upplýsingar um kostnað, ættirðu að ganga úr skugga um að allar kostnaðareiningar sem krafist er að geri stjórnunarskýrslugerðina séu hafðar með þegar þú framkvæmir skipulag kostnaðareiningar. Það er áskorun að finna viðeigandi fjölda kostnaðareininga fyrir kostnaðarstýringu. Hafandi þúsundum kostnaðareiningar getur gert það erfitt að stýra hverja kostnaðareiningu. Til vara geturðu flokka kostnaðareiningar og hafa umsjón með kostnaðarstýring á samanlögðum stigum.




