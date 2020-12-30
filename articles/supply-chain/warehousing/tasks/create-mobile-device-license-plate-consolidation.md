---
title: Stofna valmyndaratriði fartækis fyrir samstæðu númeraplatna
description: Þessi verklýsing sýnir hvernig á að stofna valmyndaratriði fartækis fyrir vinnu við samstæðu númeraplötu.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7dc52284473f3e3275675b608386641c8570218b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430196"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="5bbf6-103">Stofna valmyndaratriði fartækis fyrir samstæðu númeraplatna</span><span class="sxs-lookup"><span data-stu-id="5bbf6-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5bbf6-104">Þessi verklýsing sýnir hvernig á að stofna valmyndaratriði fartækis fyrir vinnu við samstæðu númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="5bbf6-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="5bbf6-105">Þetta gerir starfsmanna vöruhússins mögulegt að gera hluti samstæða á einni númeraplötu með hluti sem eru á annarri númeraplötu á sömu staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="5bbf6-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="5bbf6-106">Til dæmis gætu þeir notað þetta ef síðari sviðsetningarskref væru þau sömu á báðum vinnupöntununum, þannig að vinnu þarf aðeins að framkvæma einu sinni fyrir sameinaðar vörur.</span><span class="sxs-lookup"><span data-stu-id="5bbf6-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="5bbf6-107">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="5bbf6-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="5bbf6-108">Verkefnið myndu yfirleitt vera framkvæmd af yfirmanni vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="5bbf6-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="5bbf6-109">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="5bbf6-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="5bbf6-110">Fara í vöruhúsakerfi > Uppsetning > fartækis > Valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="5bbf6-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="5bbf6-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5bbf6-111">Click New.</span></span>
3. <span data-ttu-id="5bbf6-112">Í svæðið heiti valmyndaratriðis, færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5bbf6-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="5bbf6-113">Í reitinn Titill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5bbf6-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="5bbf6-114">Í reitnum Stilling velurðu „óbeint“.</span><span class="sxs-lookup"><span data-stu-id="5bbf6-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="5bbf6-115">Velja 'Sameina númeraplötur' í reitnum verkþáttakóði</span><span class="sxs-lookup"><span data-stu-id="5bbf6-115">In the Activity code field, select 'Consolidate license plates'.</span></span>

