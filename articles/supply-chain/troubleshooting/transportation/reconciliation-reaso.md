---
title: Aðeins er hægt að bæta aðallyklinum við sem kreditlykli vegna afstemmingar
description: Þegar afstemmingarástæða er sett upp í flutningsstjórnun er aðeins hægt að bæta aðalreikningnum við sem inneignarreikningi.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c4ba48c5b6e3476c203eed2fddf053ce8af873dd6a7665df54560c8894f8c2d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750883"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a>Aðeins er hægt að bæta aðallyklinum við sem kreditlykli vegna afstemmingar

KB númer: 4603538

## <a name="symptoms"></a>Einkenni

Þegar afstemmingarástæða er sett upp í flutningsstjórnun er aðeins hægt að bæta aðalreikningnum við sem inneignarreikningi. Þú getur ekki bætt við kostnaðarstað eða neinum öðrum víddum sem kreditreikninginn. En debetreikningurinn gerir þér kleift að velja aðrar víddir.

## <a name="resolution"></a>Upplausn

Ef afstemmingin er ekki gerð til að greiða lánardrottinum heldur til að lána tilteknum aðalreikningi leyfir kerfið þér ekki að velja fjárhagsvídd lánareikningsins þegar ástæðan fyrir afstemmingunni er sett upp.

Ef lykilskipulagið krefst tiltekins fjárhagsvíddargildis fyrir aðalreikninginn inneignar er ekki hægt að færa sjálfkrafa inn færslubók lánardrottins þar sem fjárhagsvíddargildið vantar. Því verður fyrst að tilgreina kreditreikninginn handvirkt með því að nota síðuna **Reikningabók**.

Ekki er hægt að bóka reikningsbók lánardrottins sjálfkrafa vegna þess að víddargildi er nauðsynlegt fyrir lánareikninginn. Þú verður að bóka þetta handvirkt eftir að þú hefur bætt víddargildinu handvirkt við aðalreikning fyrir lánalínuna.
