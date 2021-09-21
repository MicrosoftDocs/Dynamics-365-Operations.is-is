---
title: Síusvæðið á listasíðu lagerstöðu virkar ekki sem skyldi
description: Síurnar á síusvæðinu á síðunni „Lagerlisti“ sía ekki niðurstöður eins og þú gerir ráð fyrir.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: df11b1c1e7de36fa0458cd931d4be7f84a15d143
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476689"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Síusvæðið á listasíðu lagerstöðu virkar ekki sem skyldi

## <a name="symptoms"></a>Einkenni

Síurnar á síusvæðinu á **Listasíða lagers** síðunni sía ekki niðurstöður eins og þú gerir ráð fyrir.

## <a name="resolution"></a>Lausn

Síðan  **Lagerlisti**  er sett saman úr ítarlegri töflu yfir lagerbirgðir sem inniheldur allar tiltækar víddir. Listinn á þessari síðu er hins vegar samantekt. Hann gæti þar af leiðandi sameinað línur úr upprunatöflunni með því að leggja saman gildi samkvæmt víddunum sem eru sýndar.

Síur sem eru settar upp á síusvæðinu eiga við upprunatöfluna, ekki uppsafnaðan lista. Þessi hegðun getur stundum leitt til óvæntrar niðurstöðu eins og lýst er í [þessum dæmum](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples).

 [Síurnar sem gefnar eru upp í hnitanetinu](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters)  *eiga*  hinsvegar við samanlagða listann. Þessar síur fela í sér bæði QuickFilter efst í hnitanetinu og síuna fyrir hvern dálkahaus.
