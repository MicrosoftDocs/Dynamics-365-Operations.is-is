---
title: "Breyta eiganda vörusendingabirgða samkvæmt eftirspurn eftir framleiðslu"
description: "Þessi verklýsing sýnir hvernig á að breyta eiganda vörusendingabirgða úr lánardrottni í þinn lögaðila þegar eftirspurn er til staðar fyrir birgðirnar í framleiðslu."
author: perlynne
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 89e1926b070beab6b30d82be2f52a75a68544e27
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="8a15c-103">Breyta eiganda vörusendingabirgða samkvæmt eftirspurn eftir framleiðslu</span><span class="sxs-lookup"><span data-stu-id="8a15c-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8a15c-104">Þessi verklýsing sýnir hvernig á að breyta eiganda vörusendingabirgða úr lánardrottni í þinn lögaðila þegar eftirspurn er til staðar fyrir birgðirnar í framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="8a15c-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="8a15c-105">Þessari breytingu á eignarhaldi er gert með því að stofna og bóka birgðabók eignarhaldsbreytingar.</span><span class="sxs-lookup"><span data-stu-id="8a15c-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="8a15c-106">Hægt er að stofna Færslubókarlínur eignarhaldsbreytingar handvirkt eða, eins og sést í þessari skráningu, byggt á fyrirliggjandi framleiðslueftirspurn.</span><span class="sxs-lookup"><span data-stu-id="8a15c-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="8a15c-107">Yfirleitt, getur yfirmaður í vinnusal framkvæmt verkið.</span><span class="sxs-lookup"><span data-stu-id="8a15c-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="8a15c-108">Hægt er að nota þetta ferli í sýnigögn fyrirtækisins USMF eða þín eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="8a15c-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="8a15c-109">Ef verið er að nota eigin gögn, skal ganga úr skugga um að vera með eftirfarandi forsendur: heiti birgðabókar sem hefur verið sett upp fyrir breytingu á eignarhaldi birgða, efnislega skráð vara á lager í eigu lánardrottins og ein eða fleiri framleiðslupöntunarlínur fyrir efni.</span><span class="sxs-lookup"><span data-stu-id="8a15c-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="8a15c-110">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="8a15c-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="8a15c-111">Stofna færslubóka fyrir eignarhald birgða.</span><span class="sxs-lookup"><span data-stu-id="8a15c-111">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="8a15c-112">Fara í Birgðastjórnun > Færslubókarfærslur > Vörur > Eignarhaldsleiðrétting birgða.</span><span class="sxs-lookup"><span data-stu-id="8a15c-112">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="8a15c-113">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8a15c-113">Click New.</span></span>
    * <span data-ttu-id="8a15c-114">Birgðafærslubók fyrir breytingu á eignarhaldi er notuð til að breyta eiganda vörusendingabirgða úr lánardrottni í núverandi lögaðila.</span><span class="sxs-lookup"><span data-stu-id="8a15c-114">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="8a15c-115">Þessari breytingu á eignarhaldi er gert með því að losa lagerbirgðir sem er í eigu lánardrottins og taka á móti þessum birgðum í núverandi lögaðila.</span><span class="sxs-lookup"><span data-stu-id="8a15c-115">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="8a15c-116">Sláið inn eða veldu gildi í reitnum heiti.</span><span class="sxs-lookup"><span data-stu-id="8a15c-116">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="8a15c-117">Aðeins er hægt að velja heiti birgðabóka sem eru með færslubókargerðina eignarhaldsbreyting.</span><span class="sxs-lookup"><span data-stu-id="8a15c-117">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="8a15c-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8a15c-118">Click OK.</span></span>
5. <span data-ttu-id="8a15c-119">Smellið á Aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="8a15c-119">Click Functions.</span></span>
6. <span data-ttu-id="8a15c-120">Smelltu á Stofna færslubókarlínur úr framleiðslupöntunum</span><span class="sxs-lookup"><span data-stu-id="8a15c-120">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="8a15c-121">Hægt er að hefja ferlið við breytingu á eignarhaldi með því að spyrjast fyrir um allar framleiðslulínur sem eru með eftirspurn eftir notkun á hráefni.</span><span class="sxs-lookup"><span data-stu-id="8a15c-121">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="8a15c-122">Veljið valkost í reitnum stöður birgðaúthreyfinga sem taka á með.</span><span class="sxs-lookup"><span data-stu-id="8a15c-122">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="8a15c-123">Þessi valkostur gerir þér kleift að sía eftir úthreyfingarstöðu birgðafærslna.</span><span class="sxs-lookup"><span data-stu-id="8a15c-123">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="8a15c-124">Til dæmis er hægt að stofna færslubókarlínur fyrir birgðir hefur tekið efnislegar stöður Tekið til og frátekið.</span><span class="sxs-lookup"><span data-stu-id="8a15c-124">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="8a15c-125">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="8a15c-125">Expand the Records to include section.</span></span>
    * <span data-ttu-id="8a15c-126">Í þessum hluta er hægt að beita frekari síun.</span><span class="sxs-lookup"><span data-stu-id="8a15c-126">This section lets you apply additional filtering.</span></span> <span data-ttu-id="8a15c-127">Til dæmis er hægt að velja ákveðna hráefnisdagsetningu.</span><span class="sxs-lookup"><span data-stu-id="8a15c-127">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="8a15c-128">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8a15c-128">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="8a15c-129">Bóka birgðabók eignarhaldsbreytingar.</span><span class="sxs-lookup"><span data-stu-id="8a15c-129">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="8a15c-130">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="8a15c-130">Click Post.</span></span>
    * <span data-ttu-id="8a15c-131">Þegar færslubókin er bókuð, eru birgðir í eigu lánardrottins losaðar með "Breytingu á Eignarhaldi" tilvísun.</span><span class="sxs-lookup"><span data-stu-id="8a15c-131">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="8a15c-132">Birgðum er síðan móttekin sem Á lager með því að nota birgðafærslu sem er uppfærð með innhreyfingarskjali afurðar fyrir innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="8a15c-132">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="8a15c-133">Athugið að aðeins eru stofnaðar færslur sem tengjast bókaðri færslubók.</span><span class="sxs-lookup"><span data-stu-id="8a15c-133">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="8a15c-134">Ekki eru stofnaðar neinar væntanlegar birgðafærslur.</span><span class="sxs-lookup"><span data-stu-id="8a15c-134">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="8a15c-135">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8a15c-135">Click OK.</span></span>
3. <span data-ttu-id="8a15c-136">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8a15c-136">Close the page.</span></span>

