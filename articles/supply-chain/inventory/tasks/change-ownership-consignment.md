---
title: Breyta eiganda vörusendingabirgða samkvæmt eftirspurn eftir framleiðslu
description: Þessi verklýsing sýnir hvernig á að breyta eiganda vörusendingabirgða úr lánardrottni í þinn lögaðila þegar eftirspurn er til staðar fyrir birgðirnar í framleiðslu.
author: perlynne
manager: tfehr
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c50affa05b8df53d31660854f4d1ead6aeff820
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430603"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="9ae13-103">Breyta eiganda vörusendingabirgða samkvæmt eftirspurn eftir framleiðslu</span><span class="sxs-lookup"><span data-stu-id="9ae13-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9ae13-104">Þessi verklýsing sýnir hvernig á að breyta eiganda vörusendingabirgða úr lánardrottni í þinn lögaðila þegar eftirspurn er til staðar fyrir birgðirnar í framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="9ae13-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="9ae13-105">Þessi breyting á eignarhaldi er gert með því að stofna og bóka birgðabók eignarhaldsbreytingar.</span><span class="sxs-lookup"><span data-stu-id="9ae13-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="9ae13-106">Hægt er að stofna Færslubókarlínur eignarhaldsbreytingar handvirkt eða, eins og sést í þessari skráningu, byggt á fyrirliggjandi framleiðslueftirspurn.</span><span class="sxs-lookup"><span data-stu-id="9ae13-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="9ae13-107">Yfirleitt, getur yfirmaður í vinnusal framkvæmt verkið.</span><span class="sxs-lookup"><span data-stu-id="9ae13-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="9ae13-108">Hægt er að nota þetta ferli í sýnigögn fyrirtækisins USMF eða þín eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="9ae13-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="9ae13-109">Ef verið er að nota eigin gögn, skal ganga úr skugga um að vera með eftirfarandi forsendur: heiti birgðabókar sem hefur verið sett upp fyrir breytingu á eignarhaldi birgða, efnislega skráð vara á lager í eigu lánardrottins og ein eða fleiri framleiðslupöntunarlínur fyrir efni.</span><span class="sxs-lookup"><span data-stu-id="9ae13-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="9ae13-110">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="9ae13-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

> [!NOTE]
> <span data-ttu-id="9ae13-111">Vörusendingarferli á útleið eru ekki studd út-úr-kassanum og sjálfvirk vinnsla færslubókar eignarhalds er ekki studd.</span><span class="sxs-lookup"><span data-stu-id="9ae13-111">Outbound consignment processes are not supported out-of-the-box and automatic ownership journal processing is not supported.</span></span>

## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="9ae13-112">Stofna færslubóka fyrir eignarhald birgða.</span><span class="sxs-lookup"><span data-stu-id="9ae13-112">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="9ae13-113">Fara í Birgðastjórnun > Færslubókarfærslur > Vörur > Eignarhaldsleiðrétting birgða.</span><span class="sxs-lookup"><span data-stu-id="9ae13-113">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="9ae13-114">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="9ae13-114">Click New.</span></span>
    * <span data-ttu-id="9ae13-115">Birgðafærslubók fyrir breytingu á eignarhaldi er notuð til að breyta eiganda vörusendingabirgða úr lánardrottni í núverandi lögaðila.</span><span class="sxs-lookup"><span data-stu-id="9ae13-115">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="9ae13-116">Þessari breytingu á eignarhaldi er gert með því að losa lagerbirgðir sem er í eigu lánardrottins og taka á móti þessum birgðum í núverandi lögaðila.</span><span class="sxs-lookup"><span data-stu-id="9ae13-116">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="9ae13-117">Sláið inn eða veldu gildi í reitnum heiti.</span><span class="sxs-lookup"><span data-stu-id="9ae13-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="9ae13-118">Aðeins er hægt að velja heiti birgðabóka sem eru með færslubókargerðina eignarhaldsbreyting.</span><span class="sxs-lookup"><span data-stu-id="9ae13-118">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="9ae13-119">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9ae13-119">Click OK.</span></span>
5. <span data-ttu-id="9ae13-120">Smellið á Aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="9ae13-120">Click Functions.</span></span>
6. <span data-ttu-id="9ae13-121">Smelltu á Stofna færslubókarlínur úr framleiðslupöntunum</span><span class="sxs-lookup"><span data-stu-id="9ae13-121">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="9ae13-122">Hægt er að hefja ferlið við breytingu á eignarhaldi með því að spyrjast fyrir um allar framleiðslulínur sem eru með eftirspurn eftir notkun á hráefni.</span><span class="sxs-lookup"><span data-stu-id="9ae13-122">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="9ae13-123">Veljið valkost í reitnum stöður birgðaúthreyfinga sem taka á með.</span><span class="sxs-lookup"><span data-stu-id="9ae13-123">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="9ae13-124">Þessi valkostur gerir þér kleift að sía eftir úthreyfingarstöðu birgðafærslna.</span><span class="sxs-lookup"><span data-stu-id="9ae13-124">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="9ae13-125">Til dæmis er hægt að stofna færslubókarlínur fyrir birgðir hefur tekið efnislegar stöður Tekið til og frátekið.</span><span class="sxs-lookup"><span data-stu-id="9ae13-125">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="9ae13-126">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="9ae13-126">Expand the Records to include section.</span></span>
    * <span data-ttu-id="9ae13-127">Í þessum hluta er hægt að beita frekari síun.</span><span class="sxs-lookup"><span data-stu-id="9ae13-127">This section lets you apply additional filtering.</span></span> <span data-ttu-id="9ae13-128">Til dæmis er hægt að velja ákveðna hráefnisdagsetningu.</span><span class="sxs-lookup"><span data-stu-id="9ae13-128">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="9ae13-129">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9ae13-129">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="9ae13-130">Bóka birgðabók eignarhaldsbreytingar.</span><span class="sxs-lookup"><span data-stu-id="9ae13-130">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="9ae13-131">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="9ae13-131">Click Post.</span></span>
    * <span data-ttu-id="9ae13-132">Þegar færslubókin er bókuð, eru birgðir í eigu lánardrottins losaðar með "Breytingu á Eignarhaldi" tilvísun.</span><span class="sxs-lookup"><span data-stu-id="9ae13-132">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="9ae13-133">Birgðum er síðan móttekin sem Á lager með því að nota birgðafærslu sem er uppfærð með innhreyfingarskjali afurðar fyrir innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="9ae13-133">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="9ae13-134">Athugið að aðeins eru stofnaðar færslur sem tengjast bókaðri færslubók.</span><span class="sxs-lookup"><span data-stu-id="9ae13-134">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="9ae13-135">Ekki eru stofnaðar neinar væntanlegar birgðafærslur.</span><span class="sxs-lookup"><span data-stu-id="9ae13-135">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="9ae13-136">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9ae13-136">Click OK.</span></span>
3. <span data-ttu-id="9ae13-137">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9ae13-137">Close the page.</span></span>

