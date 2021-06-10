---
title: Ekki er hægt að sía aðalskipulagsatriði eftir gildum viðkomandi þekjuflokks
description: Ekki er hægt að sía aðalskipulagsatriði eftir gildum viðkomandi þekjuflokks.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049473"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a>Ekki er hægt að sía aðalskipulagsatriði eftir gildum viðkomandi þekjuflokks

KB númer: 4612572

## <a name="symptoms"></a>Einkenni

Þú vilt sía vörurnar sem verða hafðar með í runuvinnslu aðaláætlanagerðar samkvæmt gildunum á tengdum færslum úr töflu vöruþekju. (Þú vilt til dæmis sía vörur eftir gildinu fyrir **Lánardrottin** og/eða **Þekjuflokk**). Uppsetning síðunnar fyrir runuvinnslu gerir þér kleift að búa til tengingu frá töflunni **Vörur** við töfluna **Vöruþekja** og síðan tilgreina reitargildi úr vöruþekjutöflunni í fyrirspurninni þinni. Hinsvegar eftir að þú lýkur við þessa uppsetningu býr kerfið samt sem áður til áætlaðar pantanir fyrir alla vöruþekjuna, ekki bara fyrir vörurnar sem passa við tiltekin reitargildi úr töflu vöruþekjunnar.

## <a name="resolution"></a>Lausn

Sían fyrir runuvinnslu getur aðeins síað atriði. Þótt þú getir bætt tengingu við töfluna **Vöruþekja**, munu síustillingar sem gerðar eru gagnvart þeirri töflu ekki hafa áhrif á úttak fyrirspurnarinnar. Á keyrslutíma keyrir kerfið áætlun fyrir alla þekjuflokka og öll afbrigði sem síuðu atriðin hafa. Þegar vara hefur verið höfð með í keyrslunni munu þekjuflokkar sem hafðir eru með í vörusíunni ekki hafa áhrif á úttak áætlanagerðar.
