---
title: Samræmd númeraröð fyrir vinnslukenni
description: Þessi eiginleiki býður upp á eina samræmda númeraröð sem býr til vinnslukenni fyrir einingar framleiðslustýringar, framkvæmdar framleiðslu og tíma og viðveru.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8ff8fae0bb20b11b15c7520fbb14727ff0372ca0255adc82599c6680a64671af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748716"
---
# <a name="unified-number-sequence-for-job-ids"></a>Samræmd númeraröð fyrir vinnslukenni

[!include [banner](../includes/banner.md)]

Þessi eiginleiki býður upp á eina samræmda númeraröð sem býr til vinnslukenni fyrir einingar framleiðslustýringar, framkvæmdar framleiðslu og tíma og viðveru. Áður var hægt að velja mismunandi númeraröð fyrir hverja einingu fyrir sig, sem gat leitt til vinnslukenna sem stönguðust á ef tvær eða fleiri þessara raða notuðu eins snið. Slíkur árekstur getur skemmt gögn.

## <a name="turn-on-this-feature-for-your-system"></a>Kveikja á þessum eiginleika fyrir kerfið

Ef kerfið inniheldur ekki eiginleikana sem lýst er í þessu efnisatriði skal fara í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eiginleikanum *Samræmd númeraröð fyrir vinnslukenni*.

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a>Setja upp samræmda númeraröð fyrir vinnslukenni

Þegar þessi eiginleiki hefur verið virkjaður, verða fyrirliggjandi númeraraðastillingar fyrir **Auðkenningu vinnslu**, sem staðsettar eru á færibreytusíðum fyrir einingar framleiðslustýringar, framkvæmdar framleiðslu og tíma og viðveru úreldar og nýjum reit **Samræmds vinnslukennis** verður bætt við. Allar þrjár einingarnar samnýta gildið fyrir **Samræmt vinnslukenni** sem fyrir vikið tryggir að allar einingarnar vísi í sömu númeraröðina. Vinnslukenni verða þar af leiðand einkvæm yfir allar þrjár einingarnar og árekstrar því úr sögunni.

Til að setja upp samræmda númeraröð fyrir vinnslukenni:

1. Kveikið á eiginleikanum eins og lýst er í fyrri hlutanum.
1. Annaðhvort skal benda á númeraröðina sem á að nota fyrir samræmd vinnslukenni eða stofna nýja. Frekari upplýsingar er að finna í [Yfirlit númeraraða](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).
1. Farið á síðuna **Færibreytur framleiðslustýringar**, **Færibreytur framleiðsluframkvæmdar** eða **Færibreytur tíma og viðveru**. Það skiptir ekki máli hvað er valið þegar þessi stilling er gerð á einhverri af þessum síðum þar sem allar aðrar síður uppfærast sjálfkrafa.
1. Opnið **Númeraraðir** flipann á valinni færibreytusíðu.
1. Úthlutið **Númeraraðarkóðanum** sem gerð var grein fyrir áður í línunni **Samræmd vinnslukenni** í hnitanetinu.
