---
title: Greiningarskýrslur eru ekki uppfærðar
description: Þetta efnisatriði útskýrir hvað eigi gera ef gagnabreytingar viðskiptamanns birtast ekki í neinum vinnusvæðum hans.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fc2e6259a8f9d17dc0f7652f207acfa53da76a8d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898574"
---
# <a name="analytic-reports-are-not-updated"></a>Greiningarskýrslur eru ekki uppfærðar

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
