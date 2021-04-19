---
title: Villuleita sölutilboð
description: Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með sölutilboð.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 09529ba729170be7281e2ae04008d3ba4a58e060
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824751"
---
# <a name="troubleshoot-sales-quotations"></a>Villuleita sölutilboð

Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með sölutilboð.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>Ég get ekki sölumagni sölutilboðs fyrir þjónustuvöru.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Ef reynt er að stilla sölumagn (reiturinn **SalesQty**) fyrir vöru af gerðinni *Þjónusta* í sölutilboðslínu, birtast eftirfarandi skilaboð: „Uppfærsla er ekki leyfð fyrir reitinn Magn.“

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Ekki er hægt að velja sölumagn fyrir afurðir sem eru þjónustuvörur. Ef til dæmis boðið er upp á þjónustu til að setja upp vöru, er engin ástæða til þess að skrá magn því að það er engin efnisleg vara til staðar. Aðeins er um að ræða þjónustu.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]