---
title: Fella Power Apps-forrit inn í Dynamics 365 Human Resources
description: Þetta efnisatriði útskýrir hvernig á að leysa vandamál þar sem valmyndaratriði Microsoft Power Apps hefur horfið úr kerfisstjórnunareiningunni.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461478"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a><span data-ttu-id="311c2-103">Fella Power Apps-forrit inn í Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="311c2-103">Embed Power Apps apps in Dynamics 365 Human Resources</span></span>

<span data-ttu-id="311c2-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="311c2-104">**Issue**</span></span>

<span data-ttu-id="311c2-105">Valmyndaratriði **Power Apps** hefur horfið úr einingu **Kerfisstjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="311c2-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="311c2-106">**Orsök**</span><span class="sxs-lookup"><span data-stu-id="311c2-106">**Cause**</span></span>

<span data-ttu-id="311c2-107">Hönnun notandaviðmótsins hefur verið breytt og Microsoft Power Apps er nú hluti af staðlaða sérsniðna líkaninu.</span><span class="sxs-lookup"><span data-stu-id="311c2-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="311c2-108">**Upplausn**</span><span class="sxs-lookup"><span data-stu-id="311c2-108">**Resolution**</span></span>

<span data-ttu-id="311c2-109">Aðferðin við innfellingu Power Apps hefur verið breytt.</span><span class="sxs-lookup"><span data-stu-id="311c2-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="311c2-110">Power Apps er nú bætt við í gegnum sérsniðna líkanið.</span><span class="sxs-lookup"><span data-stu-id="311c2-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="311c2-111">Hægt er að bæta Power Apps við nánast allar síður í Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="311c2-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="311c2-112">Upplýsingar um það hvernig á að innfella Power Apps í Talent er að finna í [Innfella Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="311c2-112">For information about how to embed Power Apps in Talent, see [Embed Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="311c2-113">Allir viðskiptamenn Power Apps sem felldu inn forrit fyrir breytinguna ættu að hafa verið uppfærðir í nýja líkaninu.</span><span class="sxs-lookup"><span data-stu-id="311c2-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="311c2-114">Hnappurinn **Power Apps** er efst í hægra horninu á nánast öllum síðum í Talent.</span><span class="sxs-lookup"><span data-stu-id="311c2-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="311c2-115">Hægt er að nota þennan hnapp til að setja inn forrit.</span><span class="sxs-lookup"><span data-stu-id="311c2-115">You can use this button to insert apps.</span></span>

<span data-ttu-id="311c2-116">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="311c2-116">Here is an example.</span></span>

1. <span data-ttu-id="311c2-117">Opnið **Starfsmannastjórnun \> Tenglar \> Starfskraftar \> Starfsmenn**.</span><span class="sxs-lookup"><span data-stu-id="311c2-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="311c2-118">Veldu hnappinn **Power Apps** og veldu síðan **Bæta við forriti frá Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="311c2-118">Select the **Power Apps** button, and then select **Add an app from Power Apps**.</span></span>

    ![Power Apps-hnappur](media/png.png)

3. <span data-ttu-id="311c2-120">Ljúktu við reitina í valmyndinni **Bæta við forriti frá Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="311c2-120">Complete the fields in the **Add an app from Power Apps** dialog box.</span></span>

    ![Bæta við forriti úr valmynd Power Apps](media/insert-powerapp.png)

<span data-ttu-id="311c2-122">Önnur leið er að fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="311c2-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="311c2-123">Á aðgerðasvæði síðunnar, á flipanum **Valkostir** í flokknum **Sérsníða**, skal velja **Sérsníða þessa síðu**.</span><span class="sxs-lookup"><span data-stu-id="311c2-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this page**.</span></span>

    ![Sérsníða flokk á flipanum „Valkostir“](media/options.png)

    <span data-ttu-id="311c2-125">Tækjastika sérstillinga birtist.</span><span class="sxs-lookup"><span data-stu-id="311c2-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="311c2-126">Á tækjastikunni velurðu **Bæta við forriti úr Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="311c2-126">On the toolbar, select **Add an app from Power Apps**.</span></span>

    ![Bæta við forriti úr Power Apps með tækjastiku sérstillinga](media/powerapp-bar.png)
