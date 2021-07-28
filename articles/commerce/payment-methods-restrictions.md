---
title: Takmarka greiðslumáta fyrir skil án kvittunar
description: Þetta efnisatriði lýsir því hvernig hægt er að takmarka ákveðnar greiðslugerðir ef endurgreiðslurnar er gerðar án kvittunar.
author: rapraj
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 4d4f2ee97db52c055136912b237412b1148c26bd
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352349"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Takmarka greiðslumáta fyrir skil án kvittunar


[!include [banner](includes/banner.md)]

Það þarf að skilgreina hverja greiðslugerð sem smásali samþykkir þegar kerfið er uppsett. Þetta efnisatriði lýsir því hvernig hægt er að takmarka ákveðnar greiðslugerðir ef endurgreiðslurnar er gerðar án kvittunar.

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