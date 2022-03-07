---
title: Villa í útreikningi bakfærslukostnaðaraðferðar við birgðalokun
description: Í eldri útgáfum gætir þú hafa fengið villu í útreikningi bakfærslukostnaðaraðferðar við birgðalokun. Leyst hefur verið úr vandamálinu.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ae92b7121998d6b1ba2f08ea5736c55637867fbf
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476645"
---
# <a name="backflush-costing-calculation-error-during-inventory-closing"></a>Villa í útreikningi bakfærslukostnaðaraðferðar við birgðalokun

## <a name="symptoms"></a>Einkenni

Við notkun útgáfa sem eru eldri en útgáfa 10.0.13 og þú notar ekki kostnaðarflæði í Lean-framleiðslu færðu eftirfarandi viðvörunarboð að ósekju við birgðalokun:

> Þú ert að fara að framkvæma birgðalokun með dagsetningu %1. Engin keyrsla á bakfærslukostnaðaraðferð útreiknings með dagsetningu %1 sem samsvarar tímabilslokum hefur verið skráð. Munið að keyra bakfærslukostnaðaraðferðar með dagsetningu á %1 sem samsvarar lokun tímabilsins. Mat á birgðum, kostnaði seldra vara og frávikum er mögulega ekki rétt í undirbók eða fjárhag fyrr en þetta hefur verið keyrt.

## <a name="resolution"></a>Lausn

Leyst hefur verið úr vandamálinu í útgáfu 10.0.13 og nýrri. Frekari upplýsingar er að finna í [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).
