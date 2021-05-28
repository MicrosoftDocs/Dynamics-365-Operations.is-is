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
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026599"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Uppsöfnun viðskiptavinaafsláttar mistókst þegar flokkar vöruafsláttar eru notaðir

KB númer: 4611372

## <a name="symptoms"></a>Einkenni

Þegar þú notar samninga um afslátt viðskiptavina (af gerðinni *upphæð*) ásamt vöruafsláttarhópum er afsláttur reiknaður út en uppsöfnun mistekst.

## <a name="resolution"></a>Upplausn

Kerfið hagar sér eins og það er hannað. Vöruflokkar flokka aðeins vörur með sama þröskuldsskilyrði. Afsláttarskilyrðið (þröskuldur) er sett á móti upphæðinni fyrir hvern hlut, ekki á móti uppsafnaðri upphæð fyrir hvern hlut í vöruflokknum.
