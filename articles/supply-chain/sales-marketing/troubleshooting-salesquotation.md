---
title: Villuleita sölutilboð
description: Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með sölutilboð.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 67610a833be132399b2d47ae8c6b27119be9ce95
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430288"
---
# <a name="troubleshoot-sales-quotations"></a>Villuleita sölutilboð

Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með sölutilboð.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>Ég get ekki sölumagni sölutilboðs fyrir þjónustuvöru.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Ef reynt er að stilla sölumagn (reiturinn **SalesQty**) fyrir vöru af gerðinni *Þjónusta* í sölutilboðslínu, birtast eftirfarandi skilaboð: „Uppfærsla er ekki leyfð fyrir reitinn Magn.“

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Ekki er hægt að velja sölumagn fyrir afurðir sem eru þjónustuvörur. Ef til dæmis boðið er upp á þjónustu til að setja upp vöru, er engin ástæða til þess að skrá magn því að það er engin efnisleg vara til staðar. Aðeins er um að ræða þjónustu.

