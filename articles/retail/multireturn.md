---
title: Vöruskil á mörgum pöntunum viðskiptavinar og reikningum
description: Þetta efnisatriði lýsir því hvernig hægt er að skila vörum á mörgum pöntunum viðskiptavinar og reikningum í Dynamics 365 Retail.
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
ms.openlocfilehash: 25a1081e5f903076e23089c41dda7437f8a70124
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017990"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="b59ac-103">Vöruskil á mörgum pöntunum viðskiptavinar og reikningum</span><span class="sxs-lookup"><span data-stu-id="b59ac-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="b59ac-104">Hægt er að framkvæma vöruskil fyrir margar pantanir og reikninga.</span><span class="sxs-lookup"><span data-stu-id="b59ac-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="b59ac-105">Skilgreina Retail til að styðja vöruskil á mörgum pöntunum viðskiptavinar og reikningum</span><span class="sxs-lookup"><span data-stu-id="b59ac-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="b59ac-106">Opnið **Retail-færibreytur \> Pantanir viðskiptavinar**.</span><span class="sxs-lookup"><span data-stu-id="b59ac-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="b59ac-107">Gerið færibreytuna **Virkja skil fyrir margar pantanir** virka.</span><span class="sxs-lookup"><span data-stu-id="b59ac-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="b59ac-108">Vinna úr vöruskilum</span><span class="sxs-lookup"><span data-stu-id="b59ac-108">Process returns</span></span>

<span data-ttu-id="b59ac-109">Þegar búið er að virkja færibreytuna og breytingarnar hafa verið samstilltar við verslanirnar getur gjaldkeri í versluninni valið margar sölupantanir fyrir viðskiptavin til að skila.</span><span class="sxs-lookup"><span data-stu-id="b59ac-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="b59ac-110">Þegar pantanir er valdar birtist listi yfir allar skilavörur sem eru á öllum reikningunum fyrir pantanirnar.</span><span class="sxs-lookup"><span data-stu-id="b59ac-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="b59ac-111">Gjaldkerinn getur þá valið vörurnar sem á að skila.</span><span class="sxs-lookup"><span data-stu-id="b59ac-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="b59ac-112">Ein skilapöntun verður stofnuð fyrir allar völdu vörurnar.</span><span class="sxs-lookup"><span data-stu-id="b59ac-112">A single return order will be created for all the selected products.</span></span>
