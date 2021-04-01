---
title: Fylgjast með vörusendingabirgðum með samstarfi lánardrottna
description: Þessi verklýsing sýnir hvernig á að nota Lánardrottnar í samstarfi til að sjá upplýsingar um birgðamagn sem hafa verið settar í vörusendingu hjá viðskiptavini.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1c75db4ef5d07e4ae396401a851389b7ecb9242
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244376"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="dcf8a-103">Fylgjast með vörusendingabirgðum með samstarfi lánardrottna</span><span class="sxs-lookup"><span data-stu-id="dcf8a-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dcf8a-104">Þessi verklýsing sýnir hvernig á að nota Lánardrottnar í samstarfi til að sjá upplýsingar um birgðamagn sem hafa verið settar í vörusendingu hjá viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="dcf8a-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="dcf8a-105">Einnig er hæt að fylgjast með notkun birgða þegar viðskiptavinurinn tekur eignarhald á birgðum.</span><span class="sxs-lookup"><span data-stu-id="dcf8a-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="dcf8a-106">Hægt er að nota þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="dcf8a-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="dcf8a-107">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="dcf8a-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="dcf8a-108">Skoða notaðar birgðir</span><span class="sxs-lookup"><span data-stu-id="dcf8a-108">View consumed inventory</span></span>
1. <span data-ttu-id="dcf8a-109">Fara í Lánardrottnar í samstarfi > vörusendingabirgðir > Afurðir mótteknar úr vörusendingabirgðum.</span><span class="sxs-lookup"><span data-stu-id="dcf8a-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="dcf8a-110">Listinn sýnir innhreyfingarskjalslínur sem voru mynduð þegar eignarhaldi á vörusendingabirgðum var breytt úr lánardrottni í viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="dcf8a-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="dcf8a-111">Það gæti þurft að skruna til hægri til að sjá magn og aðrar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="dcf8a-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="dcf8a-112">Hægt er að nota upplýsingarnar í þessum lista til að mynda reikninga fyrir viðskiptavini þína.</span><span class="sxs-lookup"><span data-stu-id="dcf8a-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="dcf8a-113">Einnig er hægt að flytja út gögn í Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="dcf8a-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="dcf8a-114">Smelltu á Skoða innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="dcf8a-114">Click View purchase order.</span></span>
3. <span data-ttu-id="dcf8a-115">Víkkið út hlutann „Upplýsingar um línu“.</span><span class="sxs-lookup"><span data-stu-id="dcf8a-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="dcf8a-116">Línan er merkt sem Vörusending, og hausinn sýnir að innkaupapöntun er með stöðuna Móttekið.</span><span class="sxs-lookup"><span data-stu-id="dcf8a-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="dcf8a-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="dcf8a-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="dcf8a-118">Skoða lagerbirgðir</span><span class="sxs-lookup"><span data-stu-id="dcf8a-118">View on-hand inventory</span></span>
1. <span data-ttu-id="dcf8a-119">Fara í Lánardrottnar í samstarfi > vörusendingabirgðir > vörusendingabirgðum á lager.</span><span class="sxs-lookup"><span data-stu-id="dcf8a-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="dcf8a-120">Síðan vörusendingabirgðir á lager sýnir birgðir sem þú átt í vöruhúsi viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="dcf8a-120">The On-hand consignment inventory page shows the stock that you own at the customer's warehouse.</span></span> <span data-ttu-id="dcf8a-121">Hægt er að birta aðrar víddir, eins og svæði og vöruhús, með því að smella á flipann Birta víddir.</span><span class="sxs-lookup"><span data-stu-id="dcf8a-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]