---
title: Uppsetning á TDS-flokki, PAN- og TAN-upplýsingum fyrir lánardrottna og viðskiptavini
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp upplýsingar um flokkinn fyrir skatt sem er dreginn frá í upphafi (TDS), varanlegt lykilnúmer (PAN) og skattlykilnúmer (TAN) fyrir lánardrottna og viðskiptavini.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: fd33b1775afefed798f1e9bb7601f4112222c430
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023329"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a><span data-ttu-id="01651-103">Uppsetning á TDS-flokki, PAN- og TAN-upplýsingum fyrir lánardrottna og viðskiptavini</span><span class="sxs-lookup"><span data-stu-id="01651-103">TDS group, PAN, and TAN information setup for vendors and customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01651-104">Í þessu efnisatriði er útskýrt hvernig á að setja upp upplýsingar um flokkinn fyrir skatt sem er dreginn frá í upphafi (TDS), varanlegt lykilnúmer (PAN) og skattlykilnúmer (TAN) fyrir lánardrottna og viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="01651-104">This topic explains how to set up information about the Tax Deducted at Source (TDS) group, permanent account number (PAN), and tax account number (TAN) for vendors and customers.</span></span>

1. <span data-ttu-id="01651-105">Farið í **Viðskiptaskuldir \> Lánardrottnar \> Allir lánardrottnar** eða **Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="01651-105">Go to **Accounts payable \> Vendors \> All vendors** or **Accounts receivable \> Customers \> All customers**.</span></span>

    <span data-ttu-id="01651-106">[![Síða allra lánardrottna](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span><span class="sxs-lookup"><span data-stu-id="01651-106">[![All vendors page](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span></span>

2. <span data-ttu-id="01651-107">Á aðgerðasvæðinu skal velja **Nýr** til að búa til lánardrottin eða viðskiptavin og færa inn nauðsynlegar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="01651-107">On the Action Pane, select **New** to create a vendor or customer, and enter the required details.</span></span> <span data-ttu-id="01651-108">Einnig er hægt að velja núverandi lánardrottin eða viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="01651-108">Alternatively, select an existing vendor or customer.</span></span>
3. <span data-ttu-id="01651-109">Í flýtiflipanum **Reikningur og afhending**, í hlutanum **Staðgreiðsluskattur**, skal stilla valkostinn **Reikna staðgreiðsluskatt** á **Já** til að reikna staðgreiðsluskatt, TDS eða skatt dreginn frá upprunalegri færslu (TCS) fyrir lánardrottin eða viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="01651-109">On the **Invoice and delivery** FastTab, in the **Withholding tax** section, set the **Calculate withholding tax** option to **Yes** to calculate withholding tax, TDS, or Tax Collected at Source (TCS) for the vendor or customer.</span></span>
4. <span data-ttu-id="01651-110">TDS fyrir innkaupareikning er reiknað út frá sjálfgefnum TDS-flokki sem er skilgreindur fyrir lánardrottin eða viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="01651-110">TDS for a purchase invoice is calculated based on the default TDS group that is defined for the vendor or customer.</span></span> <span data-ttu-id="01651-111">Í reitnum **TDS-flokkur** skal velja sjálfgefinn TDS-flokk.</span><span class="sxs-lookup"><span data-stu-id="01651-111">In the **TDS group** field, select the default TDS group.</span></span>

    > [!NOTE]
    > <span data-ttu-id="01651-112">Þegar TDS-flokkur er valinn í reitnum **TDS-flokkur** verða reitirnir **Staðgreiðsluskattsflokkur** og **TCS-flokkur** ekki í boði.</span><span class="sxs-lookup"><span data-stu-id="01651-112">When you select a TDS group in the **TDS group** field, the **Withholding tax group** and **TCS group** fields become unavailable.</span></span>

5. <span data-ttu-id="01651-113">Í flýtiflipanum **Skattaupplýsingar**, í hlutanum **Upplýsingar um PAN**, í reitnum **Staða**, skal velja stöðu varanlegs reikningsnúmers fyrir lánardrottin eða viðskiptavin:</span><span class="sxs-lookup"><span data-stu-id="01651-113">On the **Tax information** FastTab, in the **PAN information** section, in the **Status** field, select the status of the permanent account number for the vendor or customer:</span></span>

    - <span data-ttu-id="01651-114">**Ekki fyrir hendi** – Lánardrottinn eða viðskiptavinur er ekki með PAN.</span><span class="sxs-lookup"><span data-stu-id="01651-114">**Not available** – The vendor or customer doesn't have a PAN.</span></span>
    - <span data-ttu-id="01651-115">**Móttekið** – Lánardrottinn eða viðskiptavinur er með PAN.</span><span class="sxs-lookup"><span data-stu-id="01651-115">**Received** – The vendor or customer has a PAN.</span></span>
    - <span data-ttu-id="01651-116">**Sótt um** – Lánardrottinn eða viðskiptavinur hefur sótt um PAN.</span><span class="sxs-lookup"><span data-stu-id="01651-116">**Applied** – The vendor or customer has applied for a PAN.</span></span>
    - <span data-ttu-id="01651-117">**Ógilt** – Lánardrottinn eða viðskiptavinur er með PAN en það er ekki gilt.</span><span class="sxs-lookup"><span data-stu-id="01651-117">**Invalid** – The vendor or customer has a PAN, but it isn't valid.</span></span>

6. <span data-ttu-id="01651-118">Ef **Móttekið** var valið í reitnum **Staða** til að gefa til kynna að lánardrottin eða viðskiptavinur sé með PAN skal færa inn PAN í reitinn **Númer**.</span><span class="sxs-lookup"><span data-stu-id="01651-118">If you selected **Received** in the **Status** field to indicate that the vendor or customer has a PAN, enter the PAN in the **Number** field.</span></span> <span data-ttu-id="01651-119">PAN verður að samanstanda af fimm bókstöfum, síðan fjórum tölustöfum og síðan einum bókstaf.</span><span class="sxs-lookup"><span data-stu-id="01651-119">The PAN must consist of five alphabetic characters, then four numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="01651-120">Eftirfarandi er dæmi: **ABCDE1260A**.</span><span class="sxs-lookup"><span data-stu-id="01651-120">Here is an example: **ABCDE1260A**.</span></span>
7. <span data-ttu-id="01651-121">Ef **Sótt um** var valið í reitnum **Staða** til að gefa til kynna að lánardrottin eða viðskiptavinur hafi sótt um PAN skal færa inn tilvísunarnúmerið í reitinn **Tilvísunarnúmer**.</span><span class="sxs-lookup"><span data-stu-id="01651-121">If you selected **Applied** in the **Status** field to indicate that the vendor or customer has applied for PAN, enter the reference number in the **Reference number** field.</span></span>
8. <span data-ttu-id="01651-122">Í reitnum **Eðli skattgreiðanda** skal velja eðli skattgreiðendaflokks sem lánardrottinn eða viðskiptavinur tilheyrir:</span><span class="sxs-lookup"><span data-stu-id="01651-122">In the **Nature of assessee** field, select the nature of assessee category that the vendor or customer belongs to:</span></span>

    - <span data-ttu-id="01651-123">Fyrirt.  </span><span class="sxs-lookup"><span data-stu-id="01651-123">Company</span></span>
    - <span data-ttu-id="01651-124">HUF</span><span class="sxs-lookup"><span data-stu-id="01651-124">HUF</span></span>
    - <span data-ttu-id="01651-125">Staðfesta</span><span class="sxs-lookup"><span data-stu-id="01651-125">Firm</span></span>
    - <span data-ttu-id="01651-126">Sérstakt</span><span class="sxs-lookup"><span data-stu-id="01651-126">Individual</span></span>
    - <span data-ttu-id="01651-127">AOP</span><span class="sxs-lookup"><span data-stu-id="01651-127">AOP</span></span>
    - <span data-ttu-id="01651-128">BOI</span><span class="sxs-lookup"><span data-stu-id="01651-128">BOI</span></span>
    - <span data-ttu-id="01651-129">Staðaryfirvald</span><span class="sxs-lookup"><span data-stu-id="01651-129">Local authority</span></span>
    - <span data-ttu-id="01651-130">Aðrir</span><span class="sxs-lookup"><span data-stu-id="01651-130">Others</span></span>

    <span data-ttu-id="01651-131">[![Flýtiflipi skattaupplýsinga](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span><span class="sxs-lookup"><span data-stu-id="01651-131">[![Tax information FastTab](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span></span>

9. <span data-ttu-id="01651-132">Á aðgerðasvæðinu, í flipanum **Lánardrottinn**, í flokknum **Skráning**, skal velja **Skráningarkenni** til að opna síðuna **Stjórna aðsetrum**.</span><span class="sxs-lookup"><span data-stu-id="01651-132">On the Action Pane, on the **Vendor** tab, in the **Registration** group, select **Registration IDs** to open the **Manage addresses** page.</span></span>
10. <span data-ttu-id="01651-133">Á síðunni **Stjórna aðsetrum**, í flýtiflipanum **Skattaupplýsingar**, skal velja **Bæta við** eða **Breyta** til að opna síðuna **Stjórna skattaupplýsingum** þar sem hægt er að vinna með færslu skattskráningar.</span><span class="sxs-lookup"><span data-stu-id="01651-133">On the **Manage addresses** page, on the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>
11. <span data-ttu-id="01651-134">Á síðuna **Stjórna skattaupplýsingum**, í flýtiflipann **Staðgreiðsluskattur**, í reitinn **Skattlykilnúmer (TAN)** skal færa inn TAN.</span><span class="sxs-lookup"><span data-stu-id="01651-134">On the **Manage tax information** page, on the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the TAN.</span></span> <span data-ttu-id="01651-135">TAN verður að samanstanda af fjórum bókstöfum, síðan fimm tölustöfum og síðan einum bókstaf.</span><span class="sxs-lookup"><span data-stu-id="01651-135">The TAN must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="01651-136">Eftirfarandi er dæmi: **AFGH54821T**.</span><span class="sxs-lookup"><span data-stu-id="01651-136">Here is an example: **AFGH54821T**.</span></span>
12. <span data-ttu-id="01651-137">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="01651-137">Close the page.</span></span>
