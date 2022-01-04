---
title: Síusvæðið á listasíðu lagerstöðu virkar ekki sem skyldi
description: Síurnar í síurúðunni á síðunni „Vinnlisti“ sía ekki niðurstöður eins og þú bjóst við.
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
ms.openlocfilehash: 2b2b233e22378c8710a63dce83d168bfd89eba7f
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920499"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Síusvæðið á listasíðu lagerstöðu virkar ekki sem skyldi

## <a name="symptoms"></a>Einkenni

Síurnar í síurúðunni á **Á lager listi** síða ekki sía niðurstöður eins og þú býst við.

## <a name="resolution"></a>Lausn

Síðan **Lagerlisti** er sett saman úr ítarlegri töflu yfir lagerbirgðir sem inniheldur allar tiltækar víddir. Listinn á þessari síðu er hins vegar samantekt. Hann gæti þar af leiðandi sameinað línur úr upprunatöflunni með því að leggja saman gildi samkvæmt víddunum sem eru sýndar.

Síur sem eru settar upp í síurúðunni eiga við upprunatöfluna, ekki uppsafnaða listann. Þessi hegðun getur stundum leitt til óvæntrar niðurstöðu eins og lýst er í [þessum dæmum](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples).

[Síurnar sem gefnar eru upp í hnitanetinu](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters) *eiga* hinsvegar við samanlagða listann. Þessar síur fela í sér bæði QuickFilter efst í hnitanetinu og síuna fyrir hvern dálkahaus.
