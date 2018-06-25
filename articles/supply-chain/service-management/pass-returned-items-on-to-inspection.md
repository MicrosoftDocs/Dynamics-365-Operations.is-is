---
title: "Sending skilaðra vara í skoðun"
description: "Þegar skilavara er skráð skal ákvarða að senda eigi vöru í eftirlit áður en henni er skilað í birgðir eða hún losuð á einhvern annan hátt."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4a60e6635e3bb1723ced7aba1a71135116b53272
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---


# <a name="pass-returned-items-on-to-inspection"></a><span data-ttu-id="3cf5a-103">Sending skilaðra vara í skoðun</span><span class="sxs-lookup"><span data-stu-id="3cf5a-103">Pass returned items on to inspection</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3cf5a-104">Þegar skilavara er skráð er hægt að ákvarða að senda eigi vöru í eftirlit áður en henni er skilað í birgðir eða hún losuð á einhvern annan hátt.</span><span class="sxs-lookup"><span data-stu-id="3cf5a-104">When registering a returned item, you may determine that an item should be sent for inspection before it is returned to inventory or disposed of in some other way.</span></span>

1.  <span data-ttu-id="3cf5a-105">Smelltu á **Birgðastjórnun** \> **Færslubækur** \> **Vörumóttaka** \> **Vörumóttaka**.</span><span class="sxs-lookup"><span data-stu-id="3cf5a-105">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>
    
    <span data-ttu-id="3cf5a-106">\-eða-</span><span class="sxs-lookup"><span data-stu-id="3cf5a-106">\-or-</span></span>
    
    <span data-ttu-id="3cf5a-107">Smelltu á **Birgðastjórnun** \> **Færslubækur** \> **Vörumóttaka** \> **Framleiðsluinntak**.</span><span class="sxs-lookup"><span data-stu-id="3cf5a-107">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Production input**.</span></span>

2.  <span data-ttu-id="3cf5a-108">Skráðu kvittun hlutar eins og venjulega í skjámyndinni **Staðsetningarfærslubók**.</span><span class="sxs-lookup"><span data-stu-id="3cf5a-108">On the **Location journal** form, register the receipt of an item as usual.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="3cf5a-109">Til að fá upplýsingar um skráningu kvittunar á skilavörum skal sjá <A href="register-the-receipt-of-returned-items.md">Skrá kvittun á skilavörum</A></span><span class="sxs-lookup"><span data-stu-id="3cf5a-109">For information about registering the receipt of returned items, see <A href="register-the-receipt-of-returned-items.md">Register the receipt of returned items</A></span></span></P>



3.  <span data-ttu-id="3cf5a-110">Á flipanum **Sjálfgefin gildi** á svæðinu **Afgreiðslumáti** skal velja reitinn **Stjórnun biðgeymslu**.</span><span class="sxs-lookup"><span data-stu-id="3cf5a-110">On the **Default values** tab, in the **Mode of handling** area, select the **Quarantine management** box.</span></span>

<span data-ttu-id="3cf5a-111">Þetta biður kerfið um að stofna birgðageymslupöntun og einstaklingurinn eða deildin sem framkvæmir eftirlitið svarar þessari pöntun með skjámyndinni **Stjórnun biðgeymslu**.</span><span class="sxs-lookup"><span data-stu-id="3cf5a-111">This will prompt the system to create a quarantine order, and the person or department that performs inspections will respond to this order using the **Quarantine order** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="3cf5a-112">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="3cf5a-112">See also</span></span>

[<span data-ttu-id="3cf5a-113">Setja skilaðar vörur í skoðun</span><span class="sxs-lookup"><span data-stu-id="3cf5a-113">Take returned items through inspection</span></span>](take-returned-items-through-inspection.md)

[<span data-ttu-id="3cf5a-114">Tilgreint hvernig losa eigi skilaðar vörur</span><span class="sxs-lookup"><span data-stu-id="3cf5a-114">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

