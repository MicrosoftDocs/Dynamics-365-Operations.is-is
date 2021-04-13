---
title: Vöruskil á mörgum pöntunum viðskiptavinar og reikningum
description: Þetta efnisatriði lýsir því hvernig hægt er að skila vörum á mörgum pöntunum viðskiptavinar og reikningum í Dynamics 365 Commerce.
author: josaw1
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
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
ms.openlocfilehash: 4a64794a0e04516441fab628d441640e4d154b8d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796895"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="a1908-103">Vöruskil á mörgum pöntunum viðskiptavinar og reikningum</span><span class="sxs-lookup"><span data-stu-id="a1908-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="a1908-104">Í þessari grein er lýst tveimur eiginleikum sem fínstilla skil pöntunar viðskiptavinar á mörgum reikningum.</span><span class="sxs-lookup"><span data-stu-id="a1908-104">This article describes two features that optimize customer order returns over multiple invoices.</span></span> 

## <a name="enable-refunds-over-multiple-captures"></a><span data-ttu-id="a1908-105">Virkja endurgreiðslur á mörgum úthlutunum</span><span class="sxs-lookup"><span data-stu-id="a1908-105">Enable refunds over multiple captures</span></span>

<span data-ttu-id="a1908-106">Þessi eiginleiki virkjar margar tengdar endurgreiðslur fyrir sömu pöntun viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="a1908-106">This feature enables multiple linked refunds against the same customer order.</span></span> 

1. <span data-ttu-id="a1908-107">Farðu á vinnusvæðið **Eiginleikastjórnun** og leitaðu að **Virkja endurgreiðslur á mörgum úthlutunum**.</span><span class="sxs-lookup"><span data-stu-id="a1908-107">Go to the **Feature management** workspace and search for **Enable refunds over multiple captures**.</span></span>
2. <span data-ttu-id="a1908-108">Veldu **Virkja endurgreiðslur á mörgum pöntunum** og smelltu á **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="a1908-108">Select **Enable refunds over multiple orders** and then click **Enable**.</span></span> 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a><span data-ttu-id="a1908-109">Virkja viðeigandi skattaútreikning fyrir skil á hluta af magni</span><span class="sxs-lookup"><span data-stu-id="a1908-109">Enable proper tax calculation for returns with partial quantity</span></span>

<span data-ttu-id="a1908-110">Þessi eiginleiki tryggir að þegar pöntun er skilað með því að nota marga reikninga verði skattar að lokum jafnir þeirri skattupphæð sem var upprunalega innheimt.</span><span class="sxs-lookup"><span data-stu-id="a1908-110">This feature ensures that when an order is returned using multiple invoices, the taxes will ultimately be equal to the tax amount originally charged.</span></span> 

1. <span data-ttu-id="a1908-111">Farðu á vinnusvæðið **Eiginleikastjórnun** og leitaðu að **Virkja viðeigandi skattaútreikning fyrir skil á hluta af magni**.</span><span class="sxs-lookup"><span data-stu-id="a1908-111">Go to the **Feature management** workspace and search for **Enable proper tax calculation for returns with partial quantity**.</span></span>
2. <span data-ttu-id="a1908-112">Veldu **Virkja viðeigandi skattaútreikning fyrir skil á hluta af magni** og smelltu á **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="a1908-112">Select **Enable proper tax calculation for returns with partial quantity** and then click **Enable**.</span></span> 


## <a name="process-returns"></a><span data-ttu-id="a1908-113">Vinna úr vöruskilum</span><span class="sxs-lookup"><span data-stu-id="a1908-113">Process returns</span></span>

<span data-ttu-id="a1908-114">Þegar búið er að virkja þessa eiginleika og breytingarnar hafa verið samstilltar við verslanirnar getur gjaldkeri í versluninni valið margar sölupantanir fyrir viðskiptavin til að skila.</span><span class="sxs-lookup"><span data-stu-id="a1908-114">After these features are turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="a1908-115">Þegar pantanir er valdar birtist listi yfir allar skilavörur sem eru á öllum reikningunum fyrir pantanirnar.</span><span class="sxs-lookup"><span data-stu-id="a1908-115">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="a1908-116">Gjaldkerinn getur þá valið vörurnar sem á að skila.</span><span class="sxs-lookup"><span data-stu-id="a1908-116">The cashier can then select the products to return.</span></span> <span data-ttu-id="a1908-117">Ein skilapöntun verður stofnuð fyrir allar völdu vörurnar.</span><span class="sxs-lookup"><span data-stu-id="a1908-117">A single return order will be created for all the selected products.</span></span>

<span data-ttu-id="a1908-118">Ef pöntuninni var skilað að fullu verður skattupphæðin sem skilað er til viðskiptavinarins jöfn skattupphæðinni sem var upphaflega innheimt.</span><span class="sxs-lookup"><span data-stu-id="a1908-118">If the order is fully returned, the amount of taxes returned to the customer will be equal to the amount of tax originally charged.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]