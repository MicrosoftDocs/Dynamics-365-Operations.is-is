---
title: "Nota ytri vörulista fyrir PunchOut eProcurement"
description: "Þetta efnisatriði útskýrir hvernig hægt er að nota ytri vörulista til að stofna og senda innkaupabeiðnir."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c345f1f8d1aaa93dbe02f1f8c53df63bf3488a9e
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="use-external-catalogs-for-punchout-eprocurement"></a><span data-ttu-id="9faf9-103">Nota ytri vörulista fyrir PunchOut eProcurement</span><span class="sxs-lookup"><span data-stu-id="9faf9-103">Use external catalogs for PunchOut eProcurement</span></span>
<span data-ttu-id="9faf9-104">Með því að nota ytri vörulistar PunchOut e-innkaup, ekki þarf að halda utan um upplýsingar um vörum í eigin aðalgögn við lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="9faf9-104">By using external catalogs for PunchOut e-procurement, you don't have to maintain information about your vendors' products in your own master data.</span></span> <span data-ttu-id="9faf9-105">Þess í stað innkaupakörfu á vefsvæði lánardrottins breytt innkaupabeiðni sem hefur verið rétt afurðarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="9faf9-105">Instead, the shopping cart on a vendor's website is converted to requisition lines that have the correct product information.</span></span> 

<span data-ttu-id="9faf9-106">Ætti að forðast umsjón með lýsingum og verð í lánardrottnar vörum í eigin aðalgögnum vöru.</span><span class="sxs-lookup"><span data-stu-id="9faf9-106">You should avoid maintaining the descriptions and prices of your vendors’ products in your own product master data.</span></span> <span data-ttu-id="9faf9-107">Þess í stað skaltu nota ytri vörulista fyrir PunchOut eProcurement.</span><span class="sxs-lookup"><span data-stu-id="9faf9-107">Instead, use external catalogs for PunchOut e-procurement.</span></span> <span data-ttu-id="9faf9-108">Síðan, þegar starfsmönnum er að stofna innkaupabeiðnir, þær geta "punch" lánardrottins vörulista ytra setur (með öðrum orðum þær skilja kerfið og fara sem lánardrottinn setur).</span><span class="sxs-lookup"><span data-stu-id="9faf9-108">Then, when employees create requisitions, they can “punch out” to a vendor’s external catalog site (in other words, they leave your system and go to the vendor’s site).</span></span> <span data-ttu-id="9faf9-109">Vörurnar sem bætt er í innkaupakörfuna á vefsvæði lánardrottins getur síðan breytt til línur innkaupabeiðni.</span><span class="sxs-lookup"><span data-stu-id="9faf9-109">The products that are added to the shopping cart on the vendor’s website can then be converted to requisition lines.</span></span> <span data-ttu-id="9faf9-110">Þar af leiðandi fæst rétt afurðarupplýsingar: framleiðslulíkans Kenni, nafn, verð og o.s.frv.</span><span class="sxs-lookup"><span data-stu-id="9faf9-110">Therefore, you get the correct product information: product ID, name, price, and so on.</span></span>

<span data-ttu-id="9faf9-111">Nota ytri vörulistar sem starfsmaður verður að stofna beiðni á við **innkaupabeiðnir Mínar** síðu.</span><span class="sxs-lookup"><span data-stu-id="9faf9-111">To use external catalogs, an employee must create a requisition on the **My purchase requisitions** page.</span></span>

<span data-ttu-id="9faf9-112">Starfsmaðurinn sem stofnar beiðni kallast útskráningarferli beiðninnar.</span><span class="sxs-lookup"><span data-stu-id="9faf9-112">The employee who creates a requisition is referred to as the preparer of the requisition.</span></span> <span data-ttu-id="9faf9-113">Útskráningarferli, sem hægt er að ljúka eftirfarandi verkum.</span><span class="sxs-lookup"><span data-stu-id="9faf9-113">As a preparer, you can complete the following tasks.</span></span>

<span data-ttu-id="9faf9-114">Notkun á **Ytri vörulistar** línu aðgerð til að opna síðuna sem inniheldur öll ytri vörulistar sem eru í boði fyrir tiltekna requester kaupa lögaðili og móttaka rekstrarfærslna einingu.</span><span class="sxs-lookup"><span data-stu-id="9faf9-114">Use the **External catalogs** line action to open a page that includes all external catalogs that are available for the specified requester, buying legal entity, and receiving operating unit.</span></span>

<span data-ttu-id="9faf9-115">Breyta requester kaupa lögaðili og móttaka rekstrarfærslna einingu eftir heimildum þínum.</span><span class="sxs-lookup"><span data-stu-id="9faf9-115">Depending on your permissions, change the requester, buying legal entity, and receiving operating unit.</span></span> <span data-ttu-id="9faf9-116">Breytingar á þessum gildum breyst lista yfir ytri vörulistar eru tiltæk í requester.</span><span class="sxs-lookup"><span data-stu-id="9faf9-116">A change in those values might change the list of external catalogs that are available to a requester.</span></span> <span data-ttu-id="9faf9-117">Ytri vörulistar sem eru tiltækar fara eftir núverandi virka innkaup reglurnar fyrir veitta lögaðili eða móttöku rekstrarfærslna eininguna.</span><span class="sxs-lookup"><span data-stu-id="9faf9-117">The external catalogs that are available depend on the current active purchasing policies for the buying legal entity or the receiving operating unit.</span></span> <span data-ttu-id="9faf9-118">Þessar reglur má gera eða torvelda aðgang að tilteknum innkaupaflokkana.</span><span class="sxs-lookup"><span data-stu-id="9faf9-118">These policies can allow or prevent access to specific procurement categories.</span></span> <span data-ttu-id="9faf9-119">Þar af leiðandi lista yfir ytri vörulistar sem tengt er þessum innkaupaflokkana getur fyrir áhrifum.</span><span class="sxs-lookup"><span data-stu-id="9faf9-119">Therefore, the list of external catalogs that are mapped to these procurement categories can be affected.</span></span>

<span data-ttu-id="9faf9-120">Frekari upplýsingar um hvernig reglur eru settir upp eru í [Innkaupastefnum](../procurement/purchase-policies.md).</span><span class="sxs-lookup"><span data-stu-id="9faf9-120">For more information about policies, see [Purchasing policies](../procurement/purchase-policies.md).</span></span>

- <span data-ttu-id="9faf9-121">Finna ytri vörulistar fyrir tiltekna innkaupaflokkana, færa inn texta í leitarsvæðið vörulista.</span><span class="sxs-lookup"><span data-stu-id="9faf9-121">To find external catalogs for specific procurement categories, enter text in the catalog search field.</span></span>
- <span data-ttu-id="9faf9-122">Til að bæta vörum úr vörulista lánardrottins ytri á vefsvæði lánardrottins, smellt er á utanaðkomandi vörulistann.</span><span class="sxs-lookup"><span data-stu-id="9faf9-122">To add products from a vendor’s external catalog on the vendor’s website, click the external catalog.</span></span> <span data-ttu-id="9faf9-123">Bætið svo afurðum við innkaupakörfuna og ljúkið við kaupin. Innkaupakörfulínurnar verða fluttar í Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9faf9-123">Then add products to the shopping cart, and check out. The shopping cart lines will be transferred to Microsoft Dynamics 365.</span></span>

<span data-ttu-id="9faf9-124">Ef það eru margir valkostir innkaupaflokkana velja rétta innkaupaflokkurinn áður en línum er bætt við við innkaupabeiðnina.</span><span class="sxs-lookup"><span data-stu-id="9faf9-124">If there are multiple options for procurement categories, select the correct procurement category before you add the lines to the requisition.</span></span>
<span data-ttu-id="9faf9-125">Eftir að línum hefur verið bætt við innkaupabeiðni er hægt að bæta viðbótarlínum án þess að nota ytri vörulistar.</span><span class="sxs-lookup"><span data-stu-id="9faf9-125">After lines have been added to a requisition, you can add more lines without using external catalogs.</span></span> <span data-ttu-id="9faf9-126">Einnig er hægt er að áfram ytri vörulistar er notuð til að bæta við línu.</span><span class="sxs-lookup"><span data-stu-id="9faf9-126">Alternatively, you can continue to use external catalogs to add lines.</span></span>

<span data-ttu-id="9faf9-127">Þegar beiðnin er tilbúin fyrir **Verkflæði** > **Senda** aðgerð til að senda hana til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="9faf9-127">When the requisition is ready, use the **Workflow** > **Submit** action to submit it for approval.</span></span>

