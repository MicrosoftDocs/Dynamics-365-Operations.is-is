---
title: Takmarka greiðslumáta fyrir skil án kvittunar
description: Þessi grein lýsir því hvernig hægt er að takmarka ákveðnar greiðslutegundir fyrir endurgreiðslu ef skil eru gerðar án kvittunar.
author: josaw1
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.industry: Retail
ms.search.form: RetailTenderTypeTable
ms.openlocfilehash: 9b14d7d8f6a2d9209ad6a12cd53bce4a9b50178d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281397"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Takmarka greiðslumáta fyrir skil án kvittunar


[!include [banner](includes/banner.md)]

Það þarf að skilgreina hverja greiðslugerð sem smásali samþykkir þegar kerfið er uppsett. Þessi grein lýsir því hvernig hægt er að takmarka ákveðnar greiðslutegundir fyrir endurgreiðslu ef skil eru gerðar án kvittunar.

## <a name="set-up-payment-methods"></a>Setja upp greiðsluhætti

Til að setja upp greiðslumáta verður eftirfarandi verkefnum að vera lokið.
1. Búa til greiðslumáta sem eru samþykktir af öllu fyrirtækinu.
2. Stofna kortategundir og kortanúmer fyrir fyrirtækið í heild sinni. Ef taka á við kredit- eða debetkortum þarf að búa til einn greiðslumáta fyrir kort og búa síðan til kortategundir og kortanúmer fyrir fyrirtækið allt.
3. Setja upp greiðsluhætti verslunar. Tengið greiðslumáta við hverja verslun og færið síðan inn stillingar fyrir einstakar verslanir fyrir hvern greiðslumáta verslunar.
4. Setja upp kortagreiðsluhætti fyrir verslanir. Ljúkið kortauppsetningu fyrir alla greiðsluhætti korts sem verslunin tekur á móti.

![Uppsetning verslunar.](media/NoReceiptReturns1.png "Uppsetning smásöluverslunar") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Takmarka greiðslumáta fyrir skil án kvittunar

Fyrir hvern greiðsluhátt verslunar, á síðunni **Stjórnun verslunar**, undir **Skil án kvittunar**, skal stilla **Takmarka endurgreiðslur án kvittunar** á **Já**. 

Sjálfgefið gildi á valkostinum er **Nei**, sem tryggir að greiðslumátinn sé leyfður fyrir endurgreiðslur. 

Þegar **Takmarka endurgreiðslur án kvittunar** er stillt á **Já** verður valinn greiðslumáti ekki leyfður fyrir endurgreiðslur. 

![Greiðslumáti í verslun.](media/NoReceiptReturns3.png "Greiðslumáti viðskiptakrafna") 

> [!NOTE]
> Þegar gjaldkeri velur greiðslumáta sem takmarkar endurgreiðslu án kvittunar birtist skilaboð til að staðfesta viðeigandi greiðslumáta.

![Viðunandi greiðslumátar.](media/NoReceiptReturns4.png "Viðunandi greiðslumátar") 

Ef færsla er bæði með endurgreiðslu með kvittun og án kvittunar, verður ekki farið eftir skilmálum takmörkunar vegna þess að færslan verður verkflæði endurgreiðslu með kvittun. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
