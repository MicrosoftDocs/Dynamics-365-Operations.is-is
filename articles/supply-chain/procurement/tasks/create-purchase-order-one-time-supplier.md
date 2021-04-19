---
title: Stofna innkaupapöntun fyrir einskiptisbirgi
description: Þessi verklýsing sýnir hvernig á að stofna innkaupapöntun fyrir eins-skiptis birgi.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fe76a3d481c3bc8dd3a3d45eda031df61ece4aa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812374"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="6f1d1-103">Stofna innkaupapöntun fyrir einskiptisbirgi</span><span class="sxs-lookup"><span data-stu-id="6f1d1-103">Create a purchase order for a one-time supplier</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f1d1-104">Þessi verklýsing sýnir hvernig á að stofna innkaupapöntun fyrir eins-skiptis birgi.</span><span class="sxs-lookup"><span data-stu-id="6f1d1-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="6f1d1-105">Birgirinn er stofnuð sjálfkrafa með innkaupapöntun, frekar en að þurfa að stofna lánardrottnalykil handvirkt.</span><span class="sxs-lookup"><span data-stu-id="6f1d1-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="6f1d1-106">Innkaupapöntun eru yfirleitt stofnaðar af innkaupastjórar.</span><span class="sxs-lookup"><span data-stu-id="6f1d1-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="6f1d1-107">Dæmi sem eru sýnd í þessari handbók er hægt að nota sýnigögn USMF-fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="6f1d1-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="6f1d1-108">Það er skilyrði að eins skiptis lánardrottinn hefur verið sett upp á síðunni færibreytum viðskiptaskulda.</span><span class="sxs-lookup"><span data-stu-id="6f1d1-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="6f1d1-109">Stofna innkaupapöntun fyrir einskiptisbirgi</span><span class="sxs-lookup"><span data-stu-id="6f1d1-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="6f1d1-110">Fara í innkaup og aðföng > innkaupapöntun > allar innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="6f1d1-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="6f1d1-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="6f1d1-111">Click New.</span></span>
3. <span data-ttu-id="6f1d1-112">Velja Já í svæðið eins-skiptis lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="6f1d1-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="6f1d1-113">Lykill lánardrottins er sjálfkrafa stofnuð og úthlutað á innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="6f1d1-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="6f1d1-114">Lánardrottnalykill er stofnuð byggt á sniðmátinu sem er tilgreind á flipanum Almennt í síðunni færibreytum viðskiptaskulda.</span><span class="sxs-lookup"><span data-stu-id="6f1d1-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="6f1d1-115">Færið inn heiti fyrir lánardrottinn í svæðið Heiti.</span><span class="sxs-lookup"><span data-stu-id="6f1d1-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="6f1d1-116">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6f1d1-116">Click OK.</span></span>
    * <span data-ttu-id="6f1d1-117">Innkaupapöntun má nú ljúka og unnin eins og hver önnur pöntun.</span><span class="sxs-lookup"><span data-stu-id="6f1d1-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="6f1d1-118">Það eru engar sérstakar einkenni tengdar því hvernig þetta er gert.</span><span class="sxs-lookup"><span data-stu-id="6f1d1-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="6f1d1-119">Reikningur reikningsfærir færslu á gjalddaga á lánardrottnalykil sem stofnaður var með pöntun og þá verður greiðslan unnin.</span><span class="sxs-lookup"><span data-stu-id="6f1d1-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]