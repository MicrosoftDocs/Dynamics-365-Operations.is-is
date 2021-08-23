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
ms.openlocfilehash: d4e76f3b6231b6f307173fa176360daf775c8a7950bc4ab2f2162c768102c369
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717415"
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

![Runuvinnslur.](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]