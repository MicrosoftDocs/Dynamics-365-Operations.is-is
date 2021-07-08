---
title: Kóði lánardrottins er ekki heimilaður fyrir tiltekna afurð og dagsetningu
description: Þegar reynt er að staðfesta áætlaða pöntun eða bæta línu við innkaupapöntun berast villuboð þar sem kemur fram að kóði lánardrottins sé ekki heimilaður fyrir afurð og dagsetningu.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294104"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a><span data-ttu-id="d358c-103">Kóði lánardrottins er ekki heimilaður fyrir tiltekna afurð og dagsetningu</span><span class="sxs-lookup"><span data-stu-id="d358c-103">Vendor code isn't authorized for a specific product and date</span></span>

<span data-ttu-id="d358c-104">Villukóði SYP4881415</span><span class="sxs-lookup"><span data-stu-id="d358c-104">Error code: SYP4881415</span></span>

## <a name="symptoms"></a><span data-ttu-id="d358c-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="d358c-105">Symptoms</span></span>

<span data-ttu-id="d358c-106">Þegar reynt er að fastsetja áætlaða pöntun eða bæta línu við innkaupapöntun koma upp eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="d358c-106">When you try to firm a planned order or add a line to a purchase order, you receive the following error message:</span></span>

> <span data-ttu-id="d358c-107">Kóði lánardrottins %1 er ekki heimilaður fyrir %2 á %3.</span><span class="sxs-lookup"><span data-stu-id="d358c-107">Vendor code %1 is not authorized for %2 on %3.</span></span>

## <a name="cause"></a><span data-ttu-id="d358c-108">Orsök</span><span class="sxs-lookup"><span data-stu-id="d358c-108">Cause</span></span>

<span data-ttu-id="d358c-109">Villa kemur upp vegna þess að reiturinn **Samþykkt prófunaraðferð lánadrottins** er stilltur á *Aðeins viðvörun* eða *Ekki leyfð* fyrir tilgreinda afurð og lánardrottinn hefur ekki leyfi til að útvega þessa afurð sem stendur.</span><span class="sxs-lookup"><span data-stu-id="d358c-109">The error occurs because the **Approved vendor check method** field is set to *Warning only* or *Not allowed* for the specified product, and the vendor isn't currently authorized to supply that product.</span></span>

## <a name="resolution"></a><span data-ttu-id="d358c-110">Lausn</span><span class="sxs-lookup"><span data-stu-id="d358c-110">Resolution</span></span>

<span data-ttu-id="d358c-111">Til að laga þetta vandamál skal annaðhvort slökkva á athugun lánardrottins fyrir viðeigandi afurð eða samþykkja lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="d358c-111">To fix this issue, either disable the vendor check for the relevant product or approve the vendor.</span></span>

<span data-ttu-id="d358c-112">Til að slökkva á athugun lánardrottins fyrir afurð skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="d358c-112">To disable the vendor check for a product, follow these steps.</span></span>

1. <span data-ttu-id="d358c-113">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="d358c-113">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="d358c-114">Viðeigandi vara er opnuð.</span><span class="sxs-lookup"><span data-stu-id="d358c-114">Open the relevant product.</span></span>
1. <span data-ttu-id="d358c-115">Í flýtiflipanum **Innkaup** skal stilla reitinn **Samþykkt prófunaraðferð lánadrottins** á annað gildi en *Aðeins viðvörun* eða *Ekki leyfð*.</span><span class="sxs-lookup"><span data-stu-id="d358c-115">On the **Purchase** FastTab, set the **Approved vendor check method** field to a value other than *Warning only* or *Not allowed*.</span></span>

<span data-ttu-id="d358c-116">Til að samþykkja lánardrottinn fyrir vöru skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="d358c-116">To approve a vendor for a product, follow these steps.</span></span>

1. <span data-ttu-id="d358c-117">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="d358c-117">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="d358c-118">Opnið viðeigandi vöru.</span><span class="sxs-lookup"><span data-stu-id="d358c-118">Open the relevant item.</span></span>
1. <span data-ttu-id="d358c-119">Á aðgerðasvæðinu, í flipanum **Innkaup**, í flokknum **Samþykktur lánardrottinn**, skal velja **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="d358c-119">On the Action Pane, on the **Purchase** tab, in the **Approved vendor** group, select **Setup**.</span></span>
1. <span data-ttu-id="d358c-120">Á listasíðunni **Samþykktur lánardrottinn** skal bæta línu við hnitanetið og stilla eftirfarandi gildi fyrir hana:</span><span class="sxs-lookup"><span data-stu-id="d358c-120">On the **Approved vendor** list page, add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="d358c-121">**Lánardrottinn** – Veljið lánardrottin til að samþykkja fyrir núverandi afurð.</span><span class="sxs-lookup"><span data-stu-id="d358c-121">**Vendor** – Select the vendor to approve for the current product.</span></span>
    - <span data-ttu-id="d358c-122">**Gildisdagsetning** – Veljið fyrstu dagsetninguna sem lánardrottinn er samþykktur fyrir.</span><span class="sxs-lookup"><span data-stu-id="d358c-122">**Effective date** – Select the first date that the vendor is approved for.</span></span>
    - <span data-ttu-id="d358c-123">**Lokadagsetning** – Veljið síðustu dagsetninguna sem lánardrottinn er samþykktur fyrir.</span><span class="sxs-lookup"><span data-stu-id="d358c-123">**Expiration date** – Select the last date that the vendor is approved for.</span></span>

<span data-ttu-id="d358c-124">Frekari upplýsingar er að finna í [Samþykkja lánardrottna fyrir tilteknar afurðir](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span><span class="sxs-lookup"><span data-stu-id="d358c-124">For more information, see [Approve vendors for specific products](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span></span>
