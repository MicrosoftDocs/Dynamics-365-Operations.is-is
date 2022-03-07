---
title: Ekki er hægt að stilla magn þjónustuvöru á sölutilboðslínu
description: Á meðan unnið er með sölutilboð er ekki hægt að velja sölumagn fyrir afurðir sem eru þjónustuvörur vegna þess að engar efnislegar vörur eru til staðar til að telja.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea0f8f246e95f90b6ac5e78ee63950c9ca836a0e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476701"
---
# <a name="cant-change-the-sales-quantity-of-a-service-item-on-a-sales-quotation-line"></a>Ekki er hægt að breyta sölumagni þjónustuvöru í sölutilboðslínu

## <a name="symptoms"></a>Einkenni

Ef reynt er að stilla sölumagn (reiturinn **SalesQty**) fyrir vöru af gerðinni *Þjónusta* í sölutilboðslínu, birtast eftirfarandi skilaboð:

> Uppfærsla er ekki leyfð í reitnum „Magn“.

## <a name="cause"></a>Orsök

Þetta á að vera svona. Ekki er hægt að velja sölumagn fyrir afurðir sem eru þjónustuvörur. Ef til dæmis boðið er upp á þjónustu til að setja upp vöru, er engin ástæða til þess að skrá magn því að það er engin efnisleg vara til staðar til að telja. Aðeins er um að ræða þjónustu.
