---
title: Innfella PowerApps-forrit í Core HR
description: Þetta efnisatriði útskýrir hvernig á að leysa vandamál þar sem valmyndaratriði PowerApps hefur horfið úr kerfisstjórnunareiningunni.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 197b553f0b202ee29ad42274e2c0e03446ec782c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "304871"
---
# <a name="embed-powerapps-apps-in-core-hr"></a><span data-ttu-id="97222-103">Innfella PowerApps-forrit í Core HR</span><span class="sxs-lookup"><span data-stu-id="97222-103">Embed PowerApps apps in Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="97222-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="97222-104">**Issue**</span></span>

<span data-ttu-id="97222-105">Valmyndaratriði **PowerApps** hefur horfið úr einingu **Kerfisstjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="97222-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="97222-106">**Orsök**</span><span class="sxs-lookup"><span data-stu-id="97222-106">**Cause**</span></span>

<span data-ttu-id="97222-107">Hönnun notandaviðmótsins hefur verið breytt og Microsoft PowerApps er nú hluti af staðlaða sérsniðna líkaninu.</span><span class="sxs-lookup"><span data-stu-id="97222-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="97222-108">**Upplausn**</span><span class="sxs-lookup"><span data-stu-id="97222-108">**Resolution**</span></span>

<span data-ttu-id="97222-109">Aðferðin við innfellingu PowerApps-forrita hefur verið breytt.</span><span class="sxs-lookup"><span data-stu-id="97222-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="97222-110">PowerApps-forritum er nú bætt við í gegnum sérsniðna líkanið.</span><span class="sxs-lookup"><span data-stu-id="97222-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="97222-111">Hægt er að bæta PowerApps-forritum við nánast allar síður í Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="97222-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 for Talent.</span></span>

<span data-ttu-id="97222-112">Upplýsingar um það hvernig á að innfella PowerApps-forrit í Talent er að finna í [Innfella PowerApps-forrit](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="97222-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="97222-113">Allir viðskiptamenn PowerApps sem felldu inn forrit fyrir breytinguna ættu að hafa verið uppfærðir í nýja líkaninu.</span><span class="sxs-lookup"><span data-stu-id="97222-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="97222-114">Hnappurinn **PowerApps** er efst í hægra horninu á nánast öllum síðum í Talent.</span><span class="sxs-lookup"><span data-stu-id="97222-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="97222-115">Hægt er að nota þennan hnapp til að setja inn PowerApps-forrit.</span><span class="sxs-lookup"><span data-stu-id="97222-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="97222-116">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="97222-116">Here is an example.</span></span>

1. <span data-ttu-id="97222-117">Opnið **Starfsmannastjórnun \> Tenglar \> Starfskraftar \> Starfsmenn**.</span><span class="sxs-lookup"><span data-stu-id="97222-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="97222-118">Veljið hnappinn **PowerApps** og síðan **Setja inn PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="97222-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![PowerApps-hnappur](media/png.png)

3. <span data-ttu-id="97222-120">Ljúkið við svæðin í svarglugganum **Setja inn PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="97222-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Svarglugginn „Setja inn PowerApp“](media/insert-powerapp.png)

<span data-ttu-id="97222-122">Önnur leið er að fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="97222-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="97222-123">Á aðgerðasvæði síðunnar, á flipanum **Valkostir** í flokknum **Sérsníða**, skal velja **Sérsníða þessa skjámynd**.</span><span class="sxs-lookup"><span data-stu-id="97222-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Sérsníða flokk á flipanum „Valkostir“](media/options.png)

    <span data-ttu-id="97222-125">Tækjastika sérstillinga birtist.</span><span class="sxs-lookup"><span data-stu-id="97222-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="97222-126">Á tækjastikunni skal velja **Setja inn \> PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="97222-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Setja inn PowerApps-forrit með tækjastiku sérstillinga](media/powerapp-bar.png)
