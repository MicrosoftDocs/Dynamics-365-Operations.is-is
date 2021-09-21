---
title: Hámarksfjöldi aukastafa fyrir birgðahaldseininguna er 0
description: 'Þegar reynt er að bóka birgðafærslu eða birgðafrátekningu kemur upp villa: „Hámarksfjöldi aukastafa fyrir birgðahaldseininguna er 0.“'
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9dec198e2d77efd2253c80e14d15791cc37f88e1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476699"
---
# <a name="maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Hámarksfjöldi aukastafa fyrir birgðahaldseininguna er 0


## <a name="symptoms"></a>Einkenni

Þegar reynt er að bóka birgðafærslu eða birgðafrátekningu koma upp eftirfarandi villuboð:

> Hámarksfjöldi aukastafa fyrir birgðahaldseininguna er 0.

Þetta vandamál kemur upp þegar magn birgðafærslunnar er tilgreint sem gildi í aukastöfum sem er undir nákvæmnismörkunum sem reiturinn styður. Til dæmis *hefur magn 0,5* verið tilgreint fyrir birgðafærsluna en aðeins heiltölumagn er stutt. Þess vegna ætti gildið að vera *1* í stað *0,5*.

## <a name="resolution"></a>Lausn

1. Keyrið eftirfarandi forskrift í tilviki SQL Server til að slétta magn í birgðafærslum. Þessi forskrift mun leiðrétta gildi í töflunni **inventTrans** .

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Keyra skal samræmisathugun á birgðum þar sem kveikt er á valkostinum **Leiðrétta villu**. Þessi athugun mun leiðrétta gildi í tölfunni **inventSum**.

> [!IMPORTANT]
> Sérstaklega er mælt með því að fara gætilega þegar forskriftinni er breytt samkvæmt þörfum umhverfisins, prófið hana í prófunarumhverfi og athugið síðan niðurstöðurnar áður en forskriftin er keyrð í framleiðsluumhverfi.
