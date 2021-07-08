---
title: Afurð er í bið fyrir færslur
description: Þegar áætlaðar pantanir eru festar koma upp villuboð sem gefa til kynna að vara er í bið fyrir færslur.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301280"
---
# <a name="product-is-on-hold-for-transactions"></a><span data-ttu-id="6556d-103">Afurð er í bið fyrir færslur</span><span class="sxs-lookup"><span data-stu-id="6556d-103">Product is on hold for transactions</span></span>

<span data-ttu-id="6556d-104">Villukóði SYS13295</span><span class="sxs-lookup"><span data-stu-id="6556d-104">Error code: SYS13295</span></span>

## <a name="symptoms"></a><span data-ttu-id="6556d-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="6556d-105">Symptoms</span></span>

<span data-ttu-id="6556d-106">Þegar áætlaðar pantanir eru festar koma upp eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="6556d-106">After you firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="6556d-107">Varan %1 er lokuð vegna færslna í %2.</span><span class="sxs-lookup"><span data-stu-id="6556d-107">Item %1 is on hold for transactions in %2.</span></span>

## <a name="cause"></a><span data-ttu-id="6556d-108">Orsök</span><span class="sxs-lookup"><span data-stu-id="6556d-108">Cause</span></span>

<span data-ttu-id="6556d-109">Þegar útilokuðum vörum er lýst notar kerfið hugtökin *útilokað*, *stöðvað* og *í bið* sitt á hvað.</span><span class="sxs-lookup"><span data-stu-id="6556d-109">When describing blocked items, system uses the terms *blocked*, *stopped*, and *on hold* interchangeably.</span></span> <span data-ttu-id="6556d-110">Þessi villa þýðir að varan er stillt sem **Stöðvuð** í sjálfgefnum pöntunarstillingum.</span><span class="sxs-lookup"><span data-stu-id="6556d-110">This error means that the item is set as **Stopped** in its default order settings.</span></span>

<span data-ttu-id="6556d-111">Ef vara er útilokuð og henni er bætt við innkaupapöntunarlínu eða sölupöntunarlínu koma upp viðvörunarboð.</span><span class="sxs-lookup"><span data-stu-id="6556d-111">If an item is blocked, and you add it to a purchase order or sales order line, you receive a warning message.</span></span> <span data-ttu-id="6556d-112">Þegar vara er útilokuð er ekki hægt að breyta birgðafærslum sem tengjast innkaupapöntunarlínunni eða sölupöntunarlínunni (til dæmis þegar fylgiseðill eða reikningur er bókaður).</span><span class="sxs-lookup"><span data-stu-id="6556d-112">When an item is blocked, inventory transactions that are related to the purchase order or sales order line can't be modified (for example, when you post a packing slip or an invoice).</span></span> <span data-ttu-id="6556d-113">Hægt er að útiloka keypta vöru og selja vöru á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="6556d-113">You can block a purchased item, and, at the same time, sell the item.</span></span> <span data-ttu-id="6556d-114">Í þessu tilfelli er gátreiturinn **Stöðvað** valinn í innkaupapöntun, en varan er ekki útilokuð í birgðum eða í sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="6556d-114">In this case, the **Stopped** check box is selected on a purchase order, but the item isn't blocked in inventory or on a sales order.</span></span>

<span data-ttu-id="6556d-115">Hér eru nokkur skilyrði sem geta orðið til þess að lokað verði á sölu á vörunúmeri:</span><span class="sxs-lookup"><span data-stu-id="6556d-115">Here are some of the conditions that can cause an item number to be blocked from being sold:</span></span>

- <span data-ttu-id="6556d-116">Vara er enn í þróun eða framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="6556d-116">The item is still under development or manufacture.</span></span> <span data-ttu-id="6556d-117">Þess vegna viltu ekki að hún sé seld eða tekin frá.</span><span class="sxs-lookup"><span data-stu-id="6556d-117">Therefore, you don't want it to be sold or reserved.</span></span>
- <span data-ttu-id="6556d-118">Þú hefur móttekið margar gallaðar vörur og laga verður gallana áður en hægt er að selja vöruna.</span><span class="sxs-lookup"><span data-stu-id="6556d-118">You've received many defective items, and the defects must be corrected before the item can be sold.</span></span>

<span data-ttu-id="6556d-119">Í tilvikum af þessu tagi er hægt að loka á vöruna þar til leyst hefur verið úr vandamálinu.</span><span class="sxs-lookup"><span data-stu-id="6556d-119">In cases of this type, you can block the item until the issue is resolved.</span></span>

<span data-ttu-id="6556d-120">Ef lokað er á vöru og skilapöntunarlína er stofnuð birtast skilaboð.</span><span class="sxs-lookup"><span data-stu-id="6556d-120">If an item is blocked, and you create a return order line, you receive a message.</span></span> <span data-ttu-id="6556d-121">Ekki er hægt að loka á röð eða lotu vöru.</span><span class="sxs-lookup"><span data-stu-id="6556d-121">You can't block a series or a lot of an item.</span></span> <span data-ttu-id="6556d-122">Ef loka þarf hluta vöru er það hægt með því að flytja birgðir eða með því að loka á heildarbirgðir vörunnar yfir það tímabil.</span><span class="sxs-lookup"><span data-stu-id="6556d-122">If parts of an item must be blocked, you can block them by moving inventory or by blocking the full stock of the item for that period.</span></span>

## <a name="resolution"></a><span data-ttu-id="6556d-123">Lausn</span><span class="sxs-lookup"><span data-stu-id="6556d-123">Resolution</span></span>

- <span data-ttu-id="6556d-124">Opnið síðuna **Sjálfgefnar pöntunarstillingar** fyrir vöruna og hreinsið gátreitinn **Stöðvað**.</span><span class="sxs-lookup"><span data-stu-id="6556d-124">Open the **Default order settings** page for the item, and clear the **Stopped** checkbox.</span></span>
