---
title: "Vörulistar símavers"
description: "Þessi grein lýsir virkni sem er sértæk fyrir símaver fyrir vörulista í Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7be87496ceaea2d1d5f97a5cc17e50dcddbaf33d
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="call-center-catalogs"></a><span data-ttu-id="d9b48-103">Vörulistar símavers</span><span class="sxs-lookup"><span data-stu-id="d9b48-103">Call center catalogs</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="d9b48-104">Þessi grein lýsir virkni sem er sértæk fyrir símaver fyrir vörulista í Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="d9b48-104">This article describes the call center–specific functionality for catalogs in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="d9b48-105">Í  símaver, er hægt að nota vörulista til að auðkenna afurðirnar sem óskað er eftir að bjóða uppá í verslunum.</span><span class="sxs-lookup"><span data-stu-id="d9b48-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="d9b48-106">Símaver nota yfirleitt prentaða vörulista.</span><span class="sxs-lookup"><span data-stu-id="d9b48-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="d9b48-107">Hönnun og framleiðsla prentaðra vörulista er meðhöndluð utan Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="d9b48-107">The design and production of a printed catalog is handled outside Dynamics 365 for Retail.</span></span> <span data-ttu-id="d9b48-108">Hins vegar er hægt að stofna og geyma stafræna skjámynd vörulista með því að nota sömu síðurnar og eru notaðar til að setja upp smásöluvörulista á netinu.</span><span class="sxs-lookup"><span data-stu-id="d9b48-108">However, you can create and store a digital form of a catalog by using the same pages that you use to set up online retail catalogs.</span></span> <span data-ttu-id="d9b48-109">Áður en hægt er að stofna vörulista verður að setja upp afurðaúrvali og úthluta þjónustumiðstöð í úrvali.</span><span class="sxs-lookup"><span data-stu-id="d9b48-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="d9b48-110">Að bæta afurðir vörulista með því að velja vörur úr þessum úrvali.</span><span class="sxs-lookup"><span data-stu-id="d9b48-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="d9b48-111">Eftir að afurðir hefur verið bætt við vörulista og vörulistinn er lokið, verður að villuleita vörulista til að staðfesta gögn.</span><span class="sxs-lookup"><span data-stu-id="d9b48-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="d9b48-112">Vörulisti er því næst sendar til yfirferðar og samþykktar.</span><span class="sxs-lookup"><span data-stu-id="d9b48-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="d9b48-113">Eftir að vörulisti er samþykktur er hægt að birta hann.</span><span class="sxs-lookup"><span data-stu-id="d9b48-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="d9b48-114">Þegar vörulista símavers vinnustöð er stofnuð mögulegar skyndimynd af gögn vörulista á þeim tíma sem vörulistinn er birtur.</span><span class="sxs-lookup"><span data-stu-id="d9b48-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time that the catalog is published.</span></span> <span data-ttu-id="d9b48-115">Þessi virkni skyndimynd gerir kleift að fá aðgang að tiltekinni útgáfu vörulista, jafnvel þótt vörulistinn er síðar breytt og uppfært.</span><span class="sxs-lookup"><span data-stu-id="d9b48-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="d9b48-116">Einnig er hægt að setja vörulista símavers upp til að taka með valfrjálsum eftirfarandi aðgerðum:</span><span class="sxs-lookup"><span data-stu-id="d9b48-116">Call center catalogs can also be set up to include the following optional features:</span></span>

-   <span data-ttu-id="d9b48-117">**Frumkóðar** - Frumkóðar eru notaðir til að fylgjast með viðbrögðum viðskiptavina við tilteknum póstum verslun.</span><span class="sxs-lookup"><span data-stu-id="d9b48-117">**Source codes** – Source codes are used to track the customer response to specific catalog mailings.</span></span>
-   <span data-ttu-id="d9b48-118">**Ókeypis vörur** – Vörur sem hægt er að bæta við pöntun viðskiptavinar án viðbótargjalda.</span><span class="sxs-lookup"><span data-stu-id="d9b48-118">**Free products** – Products can be included in a customer's order at no additional charge.</span></span> <span data-ttu-id="d9b48-119">Þessum vörum er sjálfkrafa bætt við pöntun þegar frumkóði fyrir vörulistann er færður inn í pöntun.</span><span class="sxs-lookup"><span data-stu-id="d9b48-119">These products are automatically added to an order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="d9b48-120">**Forskriftir** – Forskriftir eru texti sem starfsmaður í símaveri les fyrir viðskiptavini þegar sölupöntun er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="d9b48-120">**Scripts** – Scripts are texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="d9b48-121">Forskriftir geta innihaldið kveðjur eða innkaupapöntun tillögur.</span><span class="sxs-lookup"><span data-stu-id="d9b48-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="d9b48-122">**Útlit síðu** – Útlit síðu fangar síðustöðu afurða í prentuðum vörulista.</span><span class="sxs-lookup"><span data-stu-id="d9b48-122">**Page layout** – A page layout captures the page position of products in the printed catalog.</span></span> <span data-ttu-id="d9b48-123">Þessar upplýsingar eru notaðar fyrir greiningarskýrslu vörulistasvæðis.</span><span class="sxs-lookup"><span data-stu-id="d9b48-123">This information is used for the catalog area analysis report.</span></span>





