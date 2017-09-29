---
title: "Vinnusvæði fyrir reikningsfærslur fyrir samstarf lánardrottna"
description: "Í þessu efnisatriði er útskýrt hvernig á að skoða reikninga lánardrottins og senda reikninga frá úr vinnusvæði fyrir reikningsfærslu fyrir samstarf lánardrottna."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3f9b8cc1ee7f8c8bed79bac3ca6a6856d9101aad
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---

# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="22f69-103">Vinnusvæði fyrir reikningsfærslur fyrir samstarf lánardrottna</span><span class="sxs-lookup"><span data-stu-id="22f69-103">Vendor collaboration invoicing workspace</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="22f69-104">Í þessu efnisatriði er útskýrt hvernig á að skoða reikninga lánardrottins og senda reikninga frá úr vinnusvæði fyrir reikningsfærslu fyrir samstarf lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="22f69-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="22f69-105">**Vinnusvæði fyrir reikningsfærslur fyrir samstarf lánardrottna** er hægt að nota til að skoða upplýsingar um reikning lánardrottins og senda reikninga til að Microsoft Dynamics 365 Finance and Operations, Enterprise edition með því að nota getu verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="22f69-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="22f69-106">Vinnusvæði fyrir reikningsfærslur fyrir samstarf lánardrottna</span><span class="sxs-lookup"><span data-stu-id="22f69-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="22f69-107">Samantektarreitir</span><span class="sxs-lookup"><span data-stu-id="22f69-107">Summary tiles</span></span>

<span data-ttu-id="22f69-108">**Samantekt** reitir veita yfirlit yfir reikninga fyrir valinn lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="22f69-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="22f69-109">Hægt er að skoða reikninga eftir stöðu þeirra.</span><span class="sxs-lookup"><span data-stu-id="22f69-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="22f69-110">Reikningsdrög hafa ekki verið send í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="22f69-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="22f69-111">Sendir, en ekki samþykktir reikningar eru þá reikningar sem lánardrottinn hefur sent en hafa ekki verið bókaðir í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="22f69-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in Finance and Operations.</span></span>
-   <span data-ttu-id="22f69-112">Samþykktir, en ekki greiddir reikninga eru þeir sem hafa verið bókaðir í Finance and Operations en hafa ekki enn verið að fullu greiddir.</span><span class="sxs-lookup"><span data-stu-id="22f69-112">Approved, not paid invoices are those that have been posted in Finance and Operations, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="22f69-113">Greiddir reikningar eru þeir sem hafa verið greiddir að fullu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="22f69-113">Paid invoices are those that have been fully paid in Finance and Operations.</span></span>

<span data-ttu-id="22f69-114">Smella á reit á opnar síað yfirlit fyrir **lista yfir Reikninga** síðuna.</span><span class="sxs-lookup"><span data-stu-id="22f69-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>
### <a name="tabular-lists"></a><span data-ttu-id="22f69-115">Töflulisti</span><span class="sxs-lookup"><span data-stu-id="22f69-115">Tabular lists</span></span>

<span data-ttu-id="22f69-116">Í **Töflulista** hlutanum er stöðu reikningsfærslu brotin niður á svipaðan hátt og samantektarreitir: Drög og Sent, en ekki samþykktir listar.</span><span class="sxs-lookup"><span data-stu-id="22f69-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="22f69-117">Þegar í stöðunni drög, er hægt að senda reikning í verkflæði eða eyða honum.</span><span class="sxs-lookup"><span data-stu-id="22f69-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="22f69-118">Síðasti töflulistinn er valkostur til að finna reikninga.</span><span class="sxs-lookup"><span data-stu-id="22f69-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="22f69-119">Hægt er að sía á meðan er leitað, til að leyfa hraðari leit.</span><span class="sxs-lookup"><span data-stu-id="22f69-119">You can filter as you search, to allow for faster searches.</span></span>
<span data-ttu-id="22f69-120">Listasíðu fyrir alla reikninga lánardrottins</span><span class="sxs-lookup"><span data-stu-id="22f69-120">All vendor invoices list page</span></span>
-----------------------------

<span data-ttu-id="22f69-121">Hægt er að skoða allar bókaðar og óbókaðar lánardrottnareikninga á listasíðunni **Reikningar lánardrottna í samstarfi** listasíðu.</span><span class="sxs-lookup"><span data-stu-id="22f69-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="22f69-122">Hægt er að nota þessa listasíðu til að skoða greiðslustöðu reikninganna.</span><span class="sxs-lookup"><span data-stu-id="22f69-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="22f69-123">Greiðslustöðurnar innifela óbókað, ógreiddur, greiddur að hluta, og greiddur að fullu.</span><span class="sxs-lookup"><span data-stu-id="22f69-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="22f69-124">Búa til nýr reikningur úr innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="22f69-124">Creating a new invoice from a purchase order</span></span>
--------------------------------------------

<span data-ttu-id="22f69-125">Hægt er að stofna nýjan reikning lánardrottins með því að velja **Nýtt** aðgerð á **reikningsfærsla fyrir samstarf lánardrottna** vinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="22f69-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="22f69-126">Númer innkaupapöntunar og reikningsnúmer verður að gefa upp af lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="22f69-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="22f69-127">Að sjálfgefnu birtast allar línur úr innkaupapöntun lánardrottins á nýjan reikning.</span><span class="sxs-lookup"><span data-stu-id="22f69-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="22f69-128">Hægt er að breyta upplýsingum um magni og kostnað áður en senda reikning lánardrottins til verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="22f69-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="22f69-129">Tengja má skrárnar, athugasemdir, myndir og Vefslóðir við reikning áður en hún er send.</span><span class="sxs-lookup"><span data-stu-id="22f69-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>



<span data-ttu-id="22f69-130">Nánari upplýsingar má finna í [Samstarf við lánardrottna með því að nota Gátt Lánardrottins](/dynamics365/unified-operations/supply-chain/procurement/collaborate-vendors-vendor-portal)</span><span class="sxs-lookup"><span data-stu-id="22f69-130">For more information, see [Collaborating with vendors by using the Vendor portal](/dynamics365/unified-operations/supply-chain/procurement/collaborate-vendors-vendor-portal)</span></span>




