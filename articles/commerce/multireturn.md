---
title: Vöruskil á mörgum pöntunum viðskiptavinar og reikningum
description: Þetta efnisatriði lýsir því hvernig hægt er að skila vörum á mörgum pöntunum viðskiptavinar og reikningum í Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: ee4c863e617b9351e55e1fc652ea8905f17c8346
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976664"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Vöruskil á mörgum pöntunum viðskiptavinar og reikningum

[!include [banner](includes/banner.md)]


Í þessari grein er lýst tveimur eiginleikum sem fínstilla skil pöntunar viðskiptavinar á mörgum reikningum. 

## <a name="enable-refunds-over-multiple-captures"></a>Virkja endurgreiðslur á mörgum úthlutunum

Þessi eiginleiki virkjar margar tengdar endurgreiðslur fyrir sömu pöntun viðskiptavinar. 

1. Farðu á vinnusvæðið **Eiginleikastjórnun** og leitaðu að **Virkja endurgreiðslur á mörgum úthlutunum**.
2. Veldu **Virkja endurgreiðslur á mörgum pöntunum** og smelltu á **Virkja**. 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Virkja viðeigandi skattaútreikning fyrir skil á hluta af magni

Þessi eiginleiki tryggir að þegar pöntun er skilað með því að nota marga reikninga verði skattar að lokum jafnir þeirri skattupphæð sem var upprunalega innheimt. 

1. Farðu á vinnusvæðið **Eiginleikastjórnun** og leitaðu að **Virkja viðeigandi skattaútreikning fyrir skil á hluta af magni**.
2. Veldu **Virkja viðeigandi skattaútreikning fyrir skil á hluta af magni** og smelltu á **Virkja**. 


## <a name="process-returns"></a>Vinna úr vöruskilum

Þegar búið er að virkja þessa eiginleika og breytingarnar hafa verið samstilltar við verslanirnar getur gjaldkeri í versluninni valið margar sölupantanir fyrir viðskiptavin til að skila.

Þegar pantanir er valdar birtist listi yfir allar skilavörur sem eru á öllum reikningunum fyrir pantanirnar. Gjaldkerinn getur þá valið vörurnar sem á að skila. Ein skilapöntun verður stofnuð fyrir allar völdu vörurnar.

Ef pöntuninni var skilað að fullu verður skattupphæðin sem skilað er til viðskiptavinarins jöfn skattupphæðinni sem var upphaflega innheimt.



[!INCLUDE[footer-include](../includes/footer-banner.md)]