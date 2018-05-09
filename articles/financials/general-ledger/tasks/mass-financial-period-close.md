--- 
title: "Fjöldalokun fjárhagstímabils"
description: "Þessi verklýsing fer í gegnum hvernig setja skal tímabil á bið eða loka varanlega tímabili eða meira en einn lögaðila í einu."
author: aprilolson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e329cb0f842232a66f74879c498db22c0ee7d768
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="mass-financial-period-close"></a><span data-ttu-id="8460e-103">Fjöldalokun fjárhagstímabils</span><span class="sxs-lookup"><span data-stu-id="8460e-103">Mass financial period close</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8460e-104">Þessi verklýsing fer í gegnum hvernig setja skal tímabil á bið eða loka varanlega tímabili eða meira en einn lögaðila í einu.</span><span class="sxs-lookup"><span data-stu-id="8460e-104">This procedure shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="8460e-105">Þar að auki sýnir verkið hvernig á að takmarka bókun notandaflokks í ákveðnar kerfiseiningar.</span><span class="sxs-lookup"><span data-stu-id="8460e-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="8460e-106">Fara í Fjárhag > Loka tímabili > Dagatal fjárhags.</span><span class="sxs-lookup"><span data-stu-id="8460e-106">Go to General ledger > Period close > Ledger calendars.</span></span>
    * <span data-ttu-id="8460e-107">Athugið að lista yfir lögaðila sem birt er háð fjárhagsdagatalinu sem var valin á síðunni.</span><span class="sxs-lookup"><span data-stu-id="8460e-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="8460e-108">Aðeins lögaðila sem nota valið fjárhagsdagatal birtast.</span><span class="sxs-lookup"><span data-stu-id="8460e-108">Only legal entities using the selected fiscal calendar will display.</span></span>  
2. <span data-ttu-id="8460e-109">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="8460e-109">Click Edit.</span></span>
3. <span data-ttu-id="8460e-110">Velja tímabil sem ætlunin er að breyta stöðu fyrir.</span><span class="sxs-lookup"><span data-stu-id="8460e-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="8460e-111">Velja lögaðilar sem ætlunin er að Uppfæra stöðu fyrir.</span><span class="sxs-lookup"><span data-stu-id="8460e-111">Select the legal entities for which you want to update the status.</span></span>
    * <span data-ttu-id="8460e-112">Hægt er að velja alla lögaðila fljótt með því að velja gátmerki efri vinstra megin á hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="8460e-112">You can quickly select all legal entities  by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="8460e-113">Velja uppfæra kerfiseiningu til að skilgreina bókunaraðgang að valinni einingu.</span><span class="sxs-lookup"><span data-stu-id="8460e-113">Select Update module access to define the posting access to a selected module.</span></span>
    * <span data-ttu-id="8460e-114">Stöðu kerfiseiningar má einnig uppfæra eina í einu með því að breyta færslum í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="8460e-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="8460e-115">Hnappurinn er gagnleg þegar á að uppfæra margar færslur lögaðila á skjótan hátt.</span><span class="sxs-lookup"><span data-stu-id="8460e-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="8460e-116">Veldu einingu sem þú vilt að uppfæri stöðuna í einungu forrits.</span><span class="sxs-lookup"><span data-stu-id="8460e-116">In the Application module, select the module that you want to update the status.</span></span> <span data-ttu-id="8460e-117">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="8460e-117">Click Select.</span></span>
7. <span data-ttu-id="8460e-118">Í Aðgangsstig skal velja Allt, Ekkert eða tiltekinn notendaflokkinn.</span><span class="sxs-lookup"><span data-stu-id="8460e-118">In the Access level, select All, None, or a specific user group.</span></span> <span data-ttu-id="8460e-119">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="8460e-119">Click Select.</span></span>
    * <span data-ttu-id="8460e-120">Allar tilgreinir að allir notendur með breytingaaðgang að kerfið geti bókað ef tímabilið er opið.</span><span class="sxs-lookup"><span data-stu-id="8460e-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="8460e-121">Ekkert tilgreinir að notendur geta ekki bókað í kerfinu ef tímabilið er opið.</span><span class="sxs-lookup"><span data-stu-id="8460e-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="8460e-122">Ákveðinn notendaflokkur gefur til kynna að aðeins notendur í flokknum geti bókað í kerfiseininguna ef tímabilið er opið.</span><span class="sxs-lookup"><span data-stu-id="8460e-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="8460e-123">Smelltu á Uppfæra.</span><span class="sxs-lookup"><span data-stu-id="8460e-123">Click Update.</span></span>
9. <span data-ttu-id="8460e-124">Veljið annað tímabil til að uppfæra stöðu.</span><span class="sxs-lookup"><span data-stu-id="8460e-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="8460e-125">Velja lögaðilar sem ætlunin er að Uppfæra stöðu tímabils fyrir.</span><span class="sxs-lookup"><span data-stu-id="8460e-125">Select the legal entities for which you want to update the period status.</span></span>
11. <span data-ttu-id="8460e-126">Veldu að uppfæra stöðu tímabils og stilltu stöðuna Á bið, eða Endanlega lokað.</span><span class="sxs-lookup"><span data-stu-id="8460e-126">Select Update period status and set the status of On hold, Open, or Permanently closed.</span></span>
    * <span data-ttu-id="8460e-127">Opna tilgreinir að hægt er að bóka á tímabilið, að því tilskildu að notandi hafi aðgang.</span><span class="sxs-lookup"><span data-stu-id="8460e-127">Open indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="8460e-128">Á bið þýðir að ekki er hægt að bóka á tímabilið en hægt er að enduropna tímabilið.</span><span class="sxs-lookup"><span data-stu-id="8460e-128">On hold means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="8460e-129">Endanlega lokað þýðir að tímabilið er lokað og að aldrei er hægt að opna það aftur.</span><span class="sxs-lookup"><span data-stu-id="8460e-129">Permanently closed means the period is closed and can never be opened.</span></span> <span data-ttu-id="8460e-130">Ekki er hægt að bóka í leiðrétting.</span><span class="sxs-lookup"><span data-stu-id="8460e-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="8460e-131">Ekki er ráðlagt að stilla tímabil sem varanlega lokað fyrr en öllum leiðréttingum og endurskoðunum er lokið.</span><span class="sxs-lookup"><span data-stu-id="8460e-131">We do not recommend setting a period to Permanently closed until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="8460e-132">Smelltu á Uppfæra.</span><span class="sxs-lookup"><span data-stu-id="8460e-132">Click Update.</span></span>


