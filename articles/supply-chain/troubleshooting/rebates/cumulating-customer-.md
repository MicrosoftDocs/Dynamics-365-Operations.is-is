---
title: Uppsöfnun viðskiptavinaafsláttar mistókst þegar flokkar vöruafsláttar eru notaðir
description: Þegar þú notar samninga um afslátt viðskiptavina ásamt vöruafsláttarhópum er afsláttur reiknaður út en uppsöfnun mistekst.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fc3381dab77cf80c0fd65f3bc27c11b814e72368631bd0e2145aac0be4f4fba4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760371"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Uppsöfnun viðskiptavinaafsláttar mistókst þegar flokkar vöruafsláttar eru notaðir

KB númer: 4611372

## <a name="symptoms"></a>Einkenni

Þegar þú notar samninga um afslátt viðskiptavina (af gerðinni *upphæð*) ásamt vöruafsláttarhópum er afsláttur reiknaður út en uppsöfnun mistekst.

## <a name="resolution"></a>Upplausn

Kerfið hagar sér eins og það er hannað. Vöruflokkar flokka aðeins vörur með sama þröskuldsskilyrði. Afsláttarskilyrðið (þröskuldur) er sett á móti upphæðinni fyrir hvern hlut, ekki á móti uppsafnaðri upphæð fyrir hvern hlut í vöruflokknum.
