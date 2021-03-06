---
title: Villuleita greiningarskýrslur
description: Þessi grein útskýrir hvað eigi gera ef gagnabreytingar viðskiptamanns birtast ekki í neinum vinnusvæðum hans.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8dab12213e9730e72aede70c5b5d1368ef77664e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053540"
---
# <a name="troubleshoot-analytic-reports"></a>Villuleita greiningarskýrslur

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Úthreyfing**

Gagnabreytingar viðskiptamanns birtast ekki á flipunum **Greiningar** í einhverjum vinnusvæða hans.

**Orsök**

Skýrslur Microsoft Power BI eru endurnýjaðar á fjögurra klukkustunda fresta samkvæmt áætlun runuvinnslu fyrir framkvæmd mælingar.

**Upplausn**

Þetta mál snýst hugsanlega bara um tímasetningu. Fylgið eftirfarandi skrefum til að hefja runuvinnslu og uppfæra greiningarvinnusvæði.

1. Opnið síðuna **Runuvinnslur** í **Kerfisstjórnun \> Tenglar \> Runuvinnslur \> Runuvinnslur**. Önnur leið er að nota leitina og slá inn **Runuvinnslur**.
1. Finnið verkið **Framkvæma mælingu** í listanum.
1. Veljið **Breyta** efst á síðunni og stillið áætlaðan upphafsdag/tíma á gildi sem endurnýjar greiningarnar nær núgildandi tíma.

![Runuvinnslur](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]