---
title: Afskriftir eigna
description: Þetta efnisatriði veitir yfirlit yfir afskriftir eigna.
author: ShylaThompson
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ec8544b885485781b0b9c0a59ec47f90fdceb6b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826883"
---
# <a name="fixed-asset-depreciation"></a>Afskriftir eigna

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir yfirlit yfir afskriftir eigna.

Afskriftir eru tímabilsfærsla sem vanalega minnkar virði eigna í efnahagslykli og er gjaldfærð á rekstrarlykla sem útgjöld. Þess vegna er aðallykil yfirleitt notaður til að kreditfæra reglubundnar afskriftir í efnahagslykli. Mótlykill er lykill í hagnaðar- og taphluta bókhaldslykilsins.

## <a name="depreciation-adjustment"></a>Leiðrétting afskriftar
Yfirleitt er einungis leiðrétting á bókaðri afskriftafærslu bókuð sem afskriftaleiðrétting. Þess vegna eru bæði aðallykill og mótlykill settir upp á sama hátt og lyklar afskrifta. Leiðrétting afskriftar getur annaðhvort verið jákvæð upphæð eða neikvæð upphæð en aðgerðir aðallykils (sem efnahagslykill) og virkni mótlykils (yfirleitt sem rekstrarlykill) eru enn þær sömu.

## <a name="extraordinary-depreciation"></a>Óreglulegar afskriftir
Óreglulegar afskriftir virkar eins og grunnafskriftinni. Það þýðir að aðallykill er notaður til að kreditfæra afskriftaupphæðina á efnahagslykilinn og minnka virði eignar. Mótlykill er lykill hagnaðar og taps, þar sem afskrift sem er reiknuð fyrir fjárhagstímabil er gjaldfærð sem útgjöld. 

Óreglulegar afskriftir virkar sjálfstætt fyrir grunnafskriftinni. Með því að hafa óreglulegar afskriftir sem aðskilda færslugerð er hægt að bóka og tilkynna óreglulegu afskriftirnar óháð venjulegu grunnafskriftunum.

## <a name="special-depreciation-allowance"></a>Sérstök heimild til afskriftar
Hægt er að nota sérstök heimild til afskriftar til að gera aukalegar afskriftaupphæðir fyrsta árið sem eign er í þjónustu og afskrifuð. Sérstök heimild til afskriftar verður gerð á undan öðrum afskriftaútreikningum. Þar sem sérstakar heimildir til afskrifta eru oft óþekkt fyrr en síðar í líftíma eignar, er best að nota þessa gerð afskriftar með bók sem ekki bókar í fjárhag. Hægt er að nota Eyða færslum sem eru ekki bókaðar í fjárhag valkost til að eyða færsluferli fyrir þessar bækur. Svo er hægt að eyða afskriftarsögu fyrir eignabókina, bóka sérstök heimild til afskriftar þegar hún er þekkt, og bóka svo eftirstandandi afskriftarfærslum fyrir árið. 

Hægt er að stofna ótakmarkaðan fjölda af sérstök heimild til afskriftar. Eftir að þessum færslum hefur verið úthlutað á eignaflokka eru þær notaðar í eignabók. 

Sérstök heimild til afskriftar eru færðar inn sem prósenta eða föst upphæð. Þegar þú bókar afskriftartillögur eru bókaðar afskriftafærslur sérstakrar heimildar í bókina sem aðskildar færslur frá afskriftarfærslum.

## <a name="depreciation-calendars"></a>Afskriftardagatöl
Hver bók hefur dagatalið sem notað er við afskriftir eigna. Bókin notar fjárhagsdagatal sjálfgefið ef þú tiltekur ekki dagatal. Einnig þarf að velja fjárhagsdagatal fyrir bók þegar tengd afskriftarregla bókar notar fjárhagslegt afskriftaár. 

Hægt er að stofna samnýtt dagatöl með síðunni **Fjárhagsdagatöl** í fjárhag.

Frekari upplýsingar eru í [Afskriftaaðferðir og hefðir](depreciation-methods-conventions.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]