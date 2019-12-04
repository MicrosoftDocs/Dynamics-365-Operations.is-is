---
title: Innfella Power Apps-forrit í Dynamics 365 - Core HR
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
ms.openlocfilehash: 6d1b7f1dd71e6bcbf10c4d91fe33e9494b041a2c
ms.sourcegitcommit: ae0efac749ab34d423fac44d00a597801c143fbb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/22/2019
ms.locfileid: "2830210"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="1bde4-103">Innfella Power Apps-forrit í Dynamics 365 - Core HR</span><span class="sxs-lookup"><span data-stu-id="1bde4-103">Embed Power Apps apps in Dynamics 365 - Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1bde4-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="1bde4-104">**Issue**</span></span>

<span data-ttu-id="1bde4-105">Valmyndaratriði **Power Apps** hefur horfið úr einingu **Kerfisstjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="1bde4-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="1bde4-106">**Orsök**</span><span class="sxs-lookup"><span data-stu-id="1bde4-106">**Cause**</span></span>

<span data-ttu-id="1bde4-107">Hönnun notandaviðmótsins hefur verið breytt og Microsoft Power Apps er nú hluti af staðlaða sérsniðna líkaninu.</span><span class="sxs-lookup"><span data-stu-id="1bde4-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="1bde4-108">**Upplausn**</span><span class="sxs-lookup"><span data-stu-id="1bde4-108">**Resolution**</span></span>

<span data-ttu-id="1bde4-109">Aðferðin við innfellingu Power Apps hefur verið breytt.</span><span class="sxs-lookup"><span data-stu-id="1bde4-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="1bde4-110">Power Apps er nú bætt við í gegnum sérsniðna líkanið.</span><span class="sxs-lookup"><span data-stu-id="1bde4-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="1bde4-111">Hægt er að bæta Power Apps við nánast allar síður í Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="1bde4-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="1bde4-112">Upplýsingar um það hvernig á að innfella Power Apps í Talent er að finna í [Innfella Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="1bde4-112">For information about how to embed Power Apps in Talent, see [Embed Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="1bde4-113">Allir viðskiptamenn Power Apps sem felldu inn forrit fyrir breytinguna ættu að hafa verið uppfærðir í nýja líkaninu.</span><span class="sxs-lookup"><span data-stu-id="1bde4-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="1bde4-114">Hnappurinn **Power Apps** er efst í hægra horninu á nánast öllum síðum í Talent.</span><span class="sxs-lookup"><span data-stu-id="1bde4-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="1bde4-115">Hægt er að nota þennan hnapp til að setja inn Power Apps.</span><span class="sxs-lookup"><span data-stu-id="1bde4-115">You can use this button to insert Power Apps.</span></span>

<span data-ttu-id="1bde4-116">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="1bde4-116">Here is an example.</span></span>

1. <span data-ttu-id="1bde4-117">Opnið **Starfsmannastjórnun \> Tenglar \> Starfskraftar \> Starfsmenn**.</span><span class="sxs-lookup"><span data-stu-id="1bde4-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="1bde4-118">Veljið hnappinn **Power Apps** og síðan **Setja inn PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="1bde4-118">Select the **Power Apps** button, and then select **Insert a PowerApp**.</span></span>

    ![Power Apps-hnappur](media/png.png)

3. <span data-ttu-id="1bde4-120">Ljúkið við svæðin í svarglugganum **Setja inn PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="1bde4-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Svarglugginn „Setja inn PowerApp“](media/insert-powerapp.png)

<span data-ttu-id="1bde4-122">Önnur leið er að fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="1bde4-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="1bde4-123">Á aðgerðasvæði síðunnar, á flipanum **Valkostir** í flokknum **Sérsníða**, skal velja **Sérsníða þessa skjámynd**.</span><span class="sxs-lookup"><span data-stu-id="1bde4-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Sérsníða flokk á flipanum „Valkostir“](media/options.png)

    <span data-ttu-id="1bde4-125">Tækjastika sérstillinga birtist.</span><span class="sxs-lookup"><span data-stu-id="1bde4-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="1bde4-126">Á tækjastikunni skal velja **Setja inn \> PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="1bde4-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Setja inn Power Apps-forrit með tækjastiku sérstillinga](media/powerapp-bar.png)
