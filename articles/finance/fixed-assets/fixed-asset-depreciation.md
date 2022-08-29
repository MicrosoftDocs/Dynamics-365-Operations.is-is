---
title: Afskriftir eigna
description: Þessi grein veitir yfirlit yfir afskriftir í fastafjármunum.
author: moaamer
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.form: AssetBonus, AssetBookTable
ms.openlocfilehash: 9761fc9846324d1c165274b72033e195bf4ea3e0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275296"
---
# <a name="fixed-asset-depreciation"></a>Afskriftir eigna

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þessi grein veitir yfirlit yfir afskriftir í fastafjármunum.

Afskriftir eru tímabilsfærsla sem vanalega minnkar virði eigna í efnahagslykli og er gjaldfærð á rekstrarlykla sem útgjöld. Þess vegna er aðallykil yfirleitt notaður til að kreditfæra reglubundnar afskriftir í efnahagslykli. Mótlykill er lykill í hagnaðar- og taphluta bókhaldslykilsins.

Frá og með útgáfu 10.0.24 er **Reiknaðu jákvæðar afskriftir** stillingarvalkostur eignabókar á **Bækur** síða gerir afskriftir kleift að skuldfæra fasta eign sem er keypt með neikvæðu bókfærðu virði (inneign).

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
