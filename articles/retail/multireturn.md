---
title: Vöruskil á mörgum pöntunum viðskiptavinar og reikningum
description: Þetta efnisatriði lýsir því hvernig hægt er að skila vörum á mörgum pöntunum viðskiptavinar og reikningum í Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 1/08/2019
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
ms.openlocfilehash: d2cf6f92e90ef196827abb599c65c732615ec7bb
ms.sourcegitcommit: e72eae546d48d41d4b07ff78cfc0242c32b793e7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2019
ms.locfileid: "373069"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="5a0dd-103">Vöruskil á mörgum pöntunum viðskiptavinar og reikningum</span><span class="sxs-lookup"><span data-stu-id="5a0dd-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="5a0dd-104">Í Dynamics 365 for Finance and Operations útgáfu 10.0 er hægt að skila vörum á mörgum pöntunum og reikningum, en í fyrri útgáfum var aðeins hægt að vinna úr vöruskilum í gegnum einn reikning í einu.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-104">In Dynamics 365 for Finance and Operations version 10.0, returns can be made across multiple orders and invoices, whereas in releases prior to 10.0, returns could only be processed by a single invoice at a time.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="5a0dd-105">Skilgreina Retail til að styðja vöruskil á mörgum pöntunum viðskiptavinar og reikningum</span><span class="sxs-lookup"><span data-stu-id="5a0dd-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="5a0dd-106">Opnið **Retail-færibreytur \> Pantanir viðskiptavinar**.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="5a0dd-107">Gerið færibreytuna **Virkja skil fyrir margar pantanir** virka.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="5a0dd-108">Vinna úr vöruskilum</span><span class="sxs-lookup"><span data-stu-id="5a0dd-108">Process returns</span></span>

<span data-ttu-id="5a0dd-109">Þegar búið er að virkja færibreytuna og breytingarnar hafa verið samstilltar við verslanirnar getur gjaldkeri í versluninni valið margar sölupantanir fyrir viðskiptavin til að skila.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="5a0dd-110">Þegar pantanir er valdar birtist listi yfir allar skilavörur sem eru á öllum reikningunum fyrir pantanirnar.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="5a0dd-111">Gjaldkerinn getur þá valið vörurnar sem á að skila.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="5a0dd-112">Ein skilapöntun verður stofnuð fyrir allar völdu vörurnar.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-112">A single return order will be created for all the selected products.</span></span>
