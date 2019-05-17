---
title: Vöruskil á mörgum pöntunum viðskiptavinar og reikningum
description: Þetta efnisatriði lýsir því hvernig hægt er að skila vörum á mörgum pöntunum viðskiptavinar og reikningum í Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: d410fde2cd127f8d644e6a385937b6bc98d74576
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517091"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Vöruskil á mörgum pöntunum viðskiptavinar og reikningum

[!include [banner](includes/banner.md)]


Í Dynamics 365 for Finance and Operations útgáfu 10.0 er hægt að skila vörum á mörgum pöntunum og reikningum, en í fyrri útgáfum var aðeins hægt að vinna úr vöruskilum í gegnum einn reikning í einu. 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>Skilgreina Retail til að styðja vöruskil á mörgum pöntunum viðskiptavinar og reikningum

1. Opnið **Retail-færibreytur \> Pantanir viðskiptavinar**.
1. Gerið færibreytuna **Virkja skil fyrir margar pantanir** virka. 

## <a name="process-returns"></a>Vinna úr vöruskilum

Þegar búið er að virkja færibreytuna og breytingarnar hafa verið samstilltar við verslanirnar getur gjaldkeri í versluninni valið margar sölupantanir fyrir viðskiptavin til að skila.

Þegar pantanir er valdar birtist listi yfir allar skilavörur sem eru á öllum reikningunum fyrir pantanirnar. Gjaldkerinn getur þá valið vörurnar sem á að skila. Ein skilapöntun verður stofnuð fyrir allar völdu vörurnar.
