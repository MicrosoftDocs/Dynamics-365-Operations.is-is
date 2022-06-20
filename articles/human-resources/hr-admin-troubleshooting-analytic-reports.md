---
title: Villuleita greiningarskýrslur
description: Þessi grein útskýrir hvernig á að leysa og greina vandamál ef gagnabreytingar viðskiptavinar birtast ekki á neinu af vinnusvæðum viðskiptavinarins.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1e6ae8931679feb2103172eb1a21649734acd995
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902228"
---
# <a name="troubleshoot-analytic-reports"></a>Villuleita greiningarskýrslur


[!INCLUDE [PEAP](../includes/peap-2.md)]

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
