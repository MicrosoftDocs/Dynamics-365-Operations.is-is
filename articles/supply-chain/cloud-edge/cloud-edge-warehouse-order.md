---
title: Vöruhúsapantanir fyrir einingakvarða skýja og jaðra
description: Í þessu efnisatriði er að finna upplýsingar um getu vöruhúsapöntunar sem er notuð sem hluti vinnuálags einingarkvarða í vöruhúsi.
author: perlynne
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f2401102ab44f5c24f5cd6f545f30438db0a36cf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836687"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="b790e-103">Vöruhúsapantanir fyrir einingakvarða skýja og jaðra</span><span class="sxs-lookup"><span data-stu-id="b790e-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="b790e-104">Ekki eru allar viðskiptaaðgerðir studdar að fullu í opinni forútgáfu þegar vinnuálag einingarkvarða er notað.</span><span class="sxs-lookup"><span data-stu-id="b790e-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="b790e-105">Ef einingarkvarðar eru notaðir skal gæta þess að nota aðeins þau ferli sem þetta efnisatriði lýsir sérstaklega sem studd ferli.</span><span class="sxs-lookup"><span data-stu-id="b790e-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="b790e-106">Hvað eru vöruhúsapantanir?</span><span class="sxs-lookup"><span data-stu-id="b790e-106">What are warehouse orders?</span></span>

<span data-ttu-id="b790e-107">*Vöruhúsapantanir* eru gerð pöntunar sem var stofnuð til að styðja uppsetningar á vöruhúsum miðstöðvar og einingarkvarða.</span><span class="sxs-lookup"><span data-stu-id="b790e-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="b790e-108">Þær gera kleift að taka á móti birgðum þegar vinnuálag vöruhúss er keyrt í einingarkvarða.</span><span class="sxs-lookup"><span data-stu-id="b790e-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="b790e-109">Þær eru aðeins notaðar með innkaupapöntunum.</span><span class="sxs-lookup"><span data-stu-id="b790e-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="b790e-110">Vöruhúsapantanir eru notaðar sem hluti af vinnslu vöruhúsakerfis, t.d. þegar farsímaforrit vöruhúsakerfis er notað til að skrá efnislegar lagerbirgðir við vinnslu á innkaupapöntun á innleið.</span><span class="sxs-lookup"><span data-stu-id="b790e-110">Warehouse orders are used as part of warehouse management processing, such as when the Warehouse Management mobile app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="b790e-111">Vöruhúsapantanir eru stofnaðar sem hluti af ferlinu *Losa í vöruhús* sem er í boði fyrir innkaupapantanir sem tilgreina vöruhús einingarkvarða og vörur sem gert er kleift að nota vöruhúsakerfisferli.</span><span class="sxs-lookup"><span data-stu-id="b790e-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b790e-112">Vöruhúsapantanir eru aðeins í boði í uppsetningum sem nota [Vinnuálag vöruhúsakerfis fyrir einingakvarða skýja og jaðra](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="b790e-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="b790e-113">Stofna vöruhúsapöntun</span><span class="sxs-lookup"><span data-stu-id="b790e-113">Create a warehouse order</span></span>

<span data-ttu-id="b790e-114">Til að stofna vöruhúsapöntun, skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="b790e-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="b790e-115">Skráðu þig inn í tilvikið af Microsoft Dynamics 365 Supply Chain Management sem keyrir á miðstöðinni.</span><span class="sxs-lookup"><span data-stu-id="b790e-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="b790e-116">(Nauðsynlegt er að hefja ferlið *Losa í vöruhús* meðan notandi er innskráður í miðstöðina.)</span><span class="sxs-lookup"><span data-stu-id="b790e-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="b790e-117">Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.</span><span class="sxs-lookup"><span data-stu-id="b790e-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="b790e-118">Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Aðgerðir**, velurðu **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="b790e-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="b790e-119">Til að skoða tengdar línur vöruhúsapöntunar skal opna viðeigandi innkaupapöntun, velja línu í hlutanum **Innkaupapöntunarlínur** og síðan á tækjastikunni skal velja **Vöruhús \> Línur vöruhúsapöntunar**.</span><span class="sxs-lookup"><span data-stu-id="b790e-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="b790e-120">Til að skoða allar línur skal fara í **Vöruhúsakerfi \> Fyrirspurnir og skýrslur \> Línur vöruhúsapöntunar**.</span><span class="sxs-lookup"><span data-stu-id="b790e-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

<span data-ttu-id="b790e-121">Einnig er hægt að kveikja á ferlinu *Losa í vöruhús* úr runuvinnslu með því að fara í **Vöruhúsakerfi > Losa í vöruhús > Sjálfvirk losun innkaupapantana**.</span><span class="sxs-lookup"><span data-stu-id="b790e-121">You can also trigger the *Release to warehouse* process from a batch job by going to **Warehouse management > Release to warehouse > Automatic release of purchase orders**.</span></span> <span data-ttu-id="b790e-122">Við uppsetningu runuvinnslunnar er hægt að velja tilteknar innkaupapöntunarlínur sem byggja á fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="b790e-122">When setting up the batch job, you can select specific purchase order lines based on a query.</span></span> <span data-ttu-id="b790e-123">Dæmigerð atburðarás væri að setja upp endurtekna runuvinnslu sem losar allar staðfestar innkaupapöntunarlínur sem búist er við að berist næsta dag.</span><span class="sxs-lookup"><span data-stu-id="b790e-123">A typical scenario would be to set up a recurrent batch job that releases all the confirmed purchase order lines expected to arrive the next day.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="b790e-124">Hætta við vöruhúsapöntun</span><span class="sxs-lookup"><span data-stu-id="b790e-124">Cancel a warehouse order</span></span>

<span data-ttu-id="b790e-125">Sem hluti af ferlinu *Losa í vöruhús*, eru birgðafærslur innkaupapöntunar tengdar við vöruhúsapantanir og læstar fyrir uppfærslum miðstöðvarinnar.</span><span class="sxs-lookup"><span data-stu-id="b790e-125">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="b790e-126">Ef losað var í vöruhúsið fyrir mistök eða önnur ástæða er fyrir því að afturkalla stofnun á línum vöruhúsapöntunar, er hægt að óska eftir því að hætta við línur vöruhúsapöntunar.</span><span class="sxs-lookup"><span data-stu-id="b790e-126">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="b790e-127">Til að hætta við línur vöruhúsapöntunar skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="b790e-127">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="b790e-128">Skráið ykkur inn í tilvik Supply Chain Management sem er keyrt í miðstöðinni.</span><span class="sxs-lookup"><span data-stu-id="b790e-128">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="b790e-129">Farið í **Vöruhúsakerfi \> Fyrirpurnir og skýrslur \> Línur vöruhúsapöntunar**.</span><span class="sxs-lookup"><span data-stu-id="b790e-129">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="b790e-130">Velja skal viðeigandi línu.</span><span class="sxs-lookup"><span data-stu-id="b790e-130">Select the relevant line.</span></span>
1. <span data-ttu-id="b790e-131">Í aðgerðarúðunni skal velja **Hætta við vöruhúsapöntunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="b790e-131">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="b790e-132">Beiðninni um að hætta við línur verður hafnað fyrir línur sem annaðhvort bíða afturköllunar eða sem verið að vinna úr í vöruhúsi þar sem vinnuálagið er keyrt í kvörðunareiningu.</span><span class="sxs-lookup"><span data-stu-id="b790e-132">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="b790e-133">Fylgjast með vöruhúsapöntun</span><span class="sxs-lookup"><span data-stu-id="b790e-133">Monitor a warehouse order</span></span>

<span data-ttu-id="b790e-134">Í yfirlitinu **Línur vöruhúsapöntunar** er hægt að fylgjast með framvindu móttöku á innleið með því að fara yfir gildin í dálkinum **Magn sem er eftir til móttöku**.</span><span class="sxs-lookup"><span data-stu-id="b790e-134">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="b790e-135">Til að skoða upplýsingar sem tengjast vinnu sem gerð er með farsímaforriti vöruhúsakerfis skal fylgja einu af þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="b790e-135">To view details that are related to work that is done by using the Warehouse Management mobile app, follow one of these steps.</span></span>

- <span data-ttu-id="b790e-136">Farið í **Vöruhúsakerfi \> Fyrirpurnir og skýrslur \> Línur vöruhúsapöntunar** og notið síuna til að finna línurnar sem leitað er að.</span><span class="sxs-lookup"><span data-stu-id="b790e-136">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="b790e-137">Opnið **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir** og opnið viðeigandi innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="b790e-137">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="b790e-138">Í hlutanum **Innkaupapöntunarlínur** skal velja eina eða fleiri línur og síðan á tækjastikunni skal velja **Vöruhús \> Færslur vöruhúsamóttöku**.</span><span class="sxs-lookup"><span data-stu-id="b790e-138">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]