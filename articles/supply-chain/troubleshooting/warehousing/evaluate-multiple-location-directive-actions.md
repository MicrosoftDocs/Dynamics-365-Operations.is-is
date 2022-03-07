---
title: Meta allar aðgerðir fyrir staðsetningarleiðbeiningar margra birgðahaldseininga
description: Nýjum eiginleika hefur verið bætt við til að meta allar aðgerðir fyrir margar staðsetningarleiðbeiningar birgðahaldseininga. Þessi síða sýnir þér upplýsingar um hvernig á að kveikja á honum.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 45995ed6f051cdf6be2b2985ff0e2cb1decf4cf0
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476643"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Valkostur margra birgðahaldseininga metur ekki margar aðgerðir staðsetningarleiðbeininga

## <a name="symptoms"></a>Einkenni

Staðsetningarleiðbeiningar af vinnutegundinni *Sölupantanir* og *Frágangur* ekki meta margar aðgerðir staðsetningarleiðbeininga þegar valkosturinn **Margar birgðahaldseiningar** er valinn. Aðeins fyrsta aðgerð fyrir staðsetningarleiðbeiningar er metin.

## <a name="resolution"></a>Lausn

Nýr eiginleiki, *Meta allar aðgerðir fyrir staðsetningarleiðbeiningar margra birgðahaldseininga*, hefur verið bætt við útgáfu 10.0.15 (sjá [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Þessi eiginleiki metur allar aðgerðir fyrir staðsetningarleiðbeiningar margra birgðahaldseininga. Ef þessi eiginleiki er nauðsynlegur skal nota [Eiginleikastjórnun](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) til að kveikja á honum.
