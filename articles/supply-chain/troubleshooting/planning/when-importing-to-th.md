---
title: Beðið er um að vista vöruþekjustillingar þrátt fyrir að þú hafir ekki gert neinar breytingar
description: Beðið er um vista vöruþekjustillingar þrátt fyrir að þú hafir ekki gert neinar breytingar.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 29ee23164430f219ff3d0c94216a8be43f480ce309f6cdac3dac6ed5b6d030af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730083"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a>Beðið er um að vista vöruþekjustillingar þrátt fyrir að þú hafir ekki gert neinar breytingar

KB númer: 4615588

## <a name="symptoms"></a>Einkenni

Í sumum tilvikum gætir þú fengið eftirfarandi skilaboð þegar þú opnar síðuna **Vöruþekja** eftir að hafa flutt inn vörur í gegnum eininguna *Vöruþekja V2*:

> Á að vista breytingarnar áður en lokað er?

Þú færð þessi skilaboð jafnvel þótt þú hafir ekki gert neinar breytingar.

## <a name="resolution"></a>Lausn

Síðan **Vöruþekja** inniheldur flókna sjálfgefna reglu sem gæti valdið því að skilaboðin birtist eftir að beinar breytingar hafa nýlega verið gerðar í gagnagrunninum, t.d. í gegnum innflutning einingar. Til dæmis er reitur `AREGENERALSETTINGSOVERRIDDEN` einingar stilltur á *Nei* en þú flytur inn skrá sem gefur upp ný eða breytt gildi fyrir reiti á borð við `PRODUCTCOVERAGEGROUPID` og/eða `VENDORACCOUNTNUMBER`. Í þessu tilfelli, vegna þess að reiturinn `AREGENERALSETTINGSOVERRIDDEN` er stilltur á *Nei*, eru gildin sjálfkrafa hreinsuð úr reitunum þegar þú opnar síðuna **Vöruþekja** í fyrsta skipti eftir innflutninginn. Ef þú vistar breytingarnar þegar skilaboðaglugginn biður um það, eru þær geymdar í gagnagrunninum. Annars færðu sömu skilaboðin næst þegar þú opnar síðuna.

Til að koma í veg fyrir þessa hegðun en einnig hafa með gildi fyrir reiti eins og `PRODUCTCOVERAGEGROUPID` í gegnum innflutning á einingu skal stilla `AREGENERALSETTINGSOVERRIDDEN` á *Já* þegar þú flytur inn.
