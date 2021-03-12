---
title: Vinnusvæði fyrir reikningsfærslur fyrir samstarf lánardrottna
description: Í þessu efnisatriði er útskýrt hvernig á að skoða reikninga lánardrottins og senda reikninga frá úr vinnusvæði fyrir reikningsfærslu fyrir samstarf lánardrottna.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 30e9012845838a4d1df5f1308740b356a64433e9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993164"
---
# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="d0110-103">Vinnusvæði fyrir reikningsfærslur fyrir samstarf lánardrottna</span><span class="sxs-lookup"><span data-stu-id="d0110-103">Vendor collaboration invoicing workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0110-104">Í þessu efnisatriði er útskýrt hvernig á að skoða reikninga lánardrottins og senda reikninga frá úr vinnusvæði fyrir reikningsfærslu fyrir samstarf lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="d0110-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="d0110-105">Vinnusvæðið **Reikningsfærslur fyrir samstarf lánardrottna** er hægt að nota til að skoða upplýsingar um reikning lánardrottins og senda reikninga í kerfið með því að nota getu verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="d0110-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to the system using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="d0110-106">Vinnusvæði fyrir reikningsfærslur fyrir samstarf lánardrottna</span><span class="sxs-lookup"><span data-stu-id="d0110-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="d0110-107">Samantektarreitir</span><span class="sxs-lookup"><span data-stu-id="d0110-107">Summary tiles</span></span>

<span data-ttu-id="d0110-108">**Samantekt** reitir veita yfirlit yfir reikninga fyrir valinn lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="d0110-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="d0110-109">Hægt er að skoða reikninga eftir stöðu þeirra.</span><span class="sxs-lookup"><span data-stu-id="d0110-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="d0110-110">Reikningsdrög hafa ekki verið send í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="d0110-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="d0110-111">Sendir, en ekki samþykktir reikningar eru þá reikningar sem lánardrottinn hefur sent en hafa ekki verið bókaðir í forritið.</span><span class="sxs-lookup"><span data-stu-id="d0110-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in the application.</span></span>
-   <span data-ttu-id="d0110-112">Samþykktir, en ekki greiddir reikninga eru þeir sem hafa verið bókaðir en hafa ekki enn verið að fullu greiddir.</span><span class="sxs-lookup"><span data-stu-id="d0110-112">Approved, not paid invoices are those that have been posted, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="d0110-113">Greiddir reikningar eru þeir sem hafa verið greiddir að fullu í forritinu.</span><span class="sxs-lookup"><span data-stu-id="d0110-113">Paid invoices are those that have been fully paid in the application.</span></span>

<span data-ttu-id="d0110-114">Smella á reit á opnar síað yfirlit fyrir **lista yfir Reikninga** síðuna.</span><span class="sxs-lookup"><span data-stu-id="d0110-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>

### <a name="tabular-lists"></a><span data-ttu-id="d0110-115">Töflulisti</span><span class="sxs-lookup"><span data-stu-id="d0110-115">Tabular lists</span></span>

<span data-ttu-id="d0110-116">Í **Töflulista** hlutanum er stöðu reikningsfærslu brotin niður á svipaðan hátt og samantektarreitir: Drög og Sent, en ekki samþykktir listar.</span><span class="sxs-lookup"><span data-stu-id="d0110-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="d0110-117">Þegar í stöðunni drög, er hægt að senda reikning í verkflæði eða eyða honum.</span><span class="sxs-lookup"><span data-stu-id="d0110-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="d0110-118">Síðasti töflulistinn er valkostur til að finna reikninga.</span><span class="sxs-lookup"><span data-stu-id="d0110-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="d0110-119">Hægt er að sía á meðan er leitað, til að leyfa hraðari leit.</span><span class="sxs-lookup"><span data-stu-id="d0110-119">You can filter as you search, to allow for faster searches.</span></span>

### <a name="all-vendor-invoices-list-page"></a><span data-ttu-id="d0110-120">Listasíðu fyrir alla reikninga lánardrottins</span><span class="sxs-lookup"><span data-stu-id="d0110-120">All vendor invoices list page</span></span>

<span data-ttu-id="d0110-121">Hægt er að skoða allar bókaðar og óbókaðar lánardrottnareikninga á listasíðunni **Reikningar lánardrottna í samstarfi** listasíðu.</span><span class="sxs-lookup"><span data-stu-id="d0110-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="d0110-122">Hægt er að nota þessa listasíðu til að skoða greiðslustöðu reikninganna.</span><span class="sxs-lookup"><span data-stu-id="d0110-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="d0110-123">Greiðslustöðurnar innifela óbókað, ógreiddur, greiddur að hluta, og greiddur að fullu.</span><span class="sxs-lookup"><span data-stu-id="d0110-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="d0110-124">Búa til nýr reikningur úr innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="d0110-124">Creating a new invoice from a purchase order</span></span>

<span data-ttu-id="d0110-125">Hægt er að stofna nýjan reikning lánardrottins með því að velja **Nýtt** aðgerð á **reikningsfærsla fyrir samstarf lánardrottna** vinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="d0110-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="d0110-126">Númer innkaupapöntunar og reikningsnúmer verður að gefa upp af lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="d0110-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="d0110-127">Að sjálfgefnu birtast allar línur úr innkaupapöntun lánardrottins á nýjan reikning.</span><span class="sxs-lookup"><span data-stu-id="d0110-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="d0110-128">Hægt er að breyta upplýsingum um magni og kostnað áður en senda reikning lánardrottins til verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="d0110-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="d0110-129">Tengja má skrárnar, athugasemdir, myndir og Vefslóðir við reikning áður en hún er send.</span><span class="sxs-lookup"><span data-stu-id="d0110-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>

<span data-ttu-id="d0110-130">Nánari upplýsingar er að finna í [Samstarf lánardrottna við utanaðkomandi lánardrottna](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="d0110-130">For more information, see [Vendor collaboration with external vendors](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span></span>



