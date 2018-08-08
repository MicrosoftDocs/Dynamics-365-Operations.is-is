--- 
title: "Stofna valmyndaratriði fartækis fyrir samstæðu númeraplatna"
description: "Þessi verklýsing sýnir hvernig á að stofna valmyndaratriði fartækis fyrir vinnu við samstæðu númeraplötu."
author: ShylaThompson
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: a05efffcd393329000394027a1ef26d1b019e7ae
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="4cc3d-103">Stofna valmyndaratriði fartækis fyrir samstæðu númeraplatna</span><span class="sxs-lookup"><span data-stu-id="4cc3d-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4cc3d-104">Þessi verklýsing sýnir hvernig á að stofna valmyndaratriði fartækis fyrir vinnu við samstæðu númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="4cc3d-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="4cc3d-105">Þetta gerir starfsmanna vöruhússins mögulegt að gera hluti samstæða á einni númeraplötu með hluti sem eru á annarri númeraplötu á sömu staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="4cc3d-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="4cc3d-106">Til dæmis gætu þeir notað þetta ef síðari sviðsetningarskref væru þau sömu á báðum vinnupöntununum, þannig að vinnu þarf aðeins að framkvæma einu sinni fyrir sameinaðar vörur.</span><span class="sxs-lookup"><span data-stu-id="4cc3d-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="4cc3d-107">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="4cc3d-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="4cc3d-108">Verkefnið myndu yfirleitt vera framkvæmd af yfirmanni vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="4cc3d-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="4cc3d-109">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="4cc3d-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="4cc3d-110">Fara í vöruhúsakerfi > Uppsetning > fartækis > Valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="4cc3d-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="4cc3d-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="4cc3d-111">Click New.</span></span>
3. <span data-ttu-id="4cc3d-112">Í svæðið heiti valmyndaratriðis, færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="4cc3d-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="4cc3d-113">Í reitinn Titill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="4cc3d-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="4cc3d-114">Í reitnum Stilling velurðu „óbeint“.</span><span class="sxs-lookup"><span data-stu-id="4cc3d-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="4cc3d-115">Velja 'Sameina númeraplötur' í reitnum verkþáttakóði</span><span class="sxs-lookup"><span data-stu-id="4cc3d-115">In the Activity code field, select 'Consolidate license plates'.</span></span>


