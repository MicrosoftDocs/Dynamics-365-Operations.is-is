---
title: "Flokkar samstæðulykla og viðbótar samstæðulyklar"
description: "Þetta efnisatriði veitir upplýsingar um flokka samstæðulykla og viðbótarsamstæðulykla og útskýrir hvernig þeir eru notaðir í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4fcdaa26eb2f15bbf6f7d80bd59a54899f637a2c
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="bd40b-103">Flokkar samstæðulykla og viðbótar samstæðulyklar</span><span class="sxs-lookup"><span data-stu-id="bd40b-103">Consolidation account groups and additional consolidation accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bd40b-104">Þetta efnisatriði veitir upplýsingar um flokka samstæðulykla og viðbótarsamstæðulykla og útskýrir hvernig þeir eru notaðir í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="bd40b-104">This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<a name="consolidation-account-groups"></a><span data-ttu-id="bd40b-105">Flokkar samstæðulykla</span><span class="sxs-lookup"><span data-stu-id="bd40b-105">Consolidation account groups</span></span>
----------------------------

<span data-ttu-id="bd40b-106">Flokkar samstæðulykla gera þér kleift að stofna flokk þeirra lykla sem þú vilt nota til að sameina gögn.</span><span class="sxs-lookup"><span data-stu-id="bd40b-106">Consolidation account groups let you create groups of the accounts that you want to use to consolidate data.</span></span> <span data-ttu-id="bd40b-107">Oftast stendur flokkur samstæðulykla fyrir stjórnvaldatilskipaðan bókhaldslykil eða varpar lyklum á flokka sem eru skilgreindir eftir höfuðstöðvum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="bd40b-107">Most often, a consolidation account group represents a government-mandated chart of accounts or maps accounts to a group that is defined by the company's headquarters.</span></span> <span data-ttu-id="bd40b-108">Hægt er að finna flokka samstæðulykla í svæðinu **Setja upp** í einingunni **Samstæður**.</span><span class="sxs-lookup"><span data-stu-id="bd40b-108">You can find consolidation account groups in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="bd40b-109">Þegar nýjum flokki er bætt við skal færa inn einkvæmt kenni fyrir lyklaflokkinn og heiti.</span><span class="sxs-lookup"><span data-stu-id="bd40b-109">When you add a new group, you enter a unique identifier for the account group and a name.</span></span>

## <a name="additional-consolidation-accounts"></a><span data-ttu-id="bd40b-110">Fleiri samstæðulyklar</span><span class="sxs-lookup"><span data-stu-id="bd40b-110">Additional consolidation accounts</span></span>
<span data-ttu-id="bd40b-111">Fleiri samstæðulyklar gera þér kleift að úthluta lykli úr fyrirliggjandi bókhaldslykill til samstæðulykill flokkur.</span><span class="sxs-lookup"><span data-stu-id="bd40b-111">Additional consolidation accounts let you assign an account from an existing chart of accounts to a consolidation account group.</span></span> <span data-ttu-id="bd40b-112">Síðan er hægt að tilgreina samstæðulykill gildi og heiti.</span><span class="sxs-lookup"><span data-stu-id="bd40b-112">You can then specify a consolidation account value and name.</span></span> 

<span data-ttu-id="bd40b-113">Hægt er að finna viðbótar samstæðulykla í svæðinu **Setja upp** í einingunni **Samstæður**.</span><span class="sxs-lookup"><span data-stu-id="bd40b-113">You can find additional consolidation accounts in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="bd40b-114">Þegar nýr samstæðulykill er stofnaður verður að tilgreina gerð eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="bd40b-114">When you create a new consolidation account, you must specify the following information:</span></span>

-   <span data-ttu-id="bd40b-115">**Aðallykill** – Þessi reitur er uppfletting sem sýnir alla aðallykla sem eru á grunni bókhaldslykill sem var valinn á síðunni.</span><span class="sxs-lookup"><span data-stu-id="bd40b-115">**Main account** – This field is a lookup that shows all the main accounts that are based on the chart of accounts that you selected on the page.</span></span> <span data-ttu-id="bd40b-116">Þegar þú velur lykil er heiti hans sjálfvirkt skráð í svæðið **Heiti reiknings**.</span><span class="sxs-lookup"><span data-stu-id="bd40b-116">When you select an account, the name is automatically entered in the **Main account name** field.</span></span>
-   <span data-ttu-id="bd40b-117">**Flokkur samstæðulykla** – Notaðu þetta svæði til að tilgreina flokk til að úthluta lykill í.</span><span class="sxs-lookup"><span data-stu-id="bd40b-117">**Consolidation account group** – Use this field to specify the group to assign the account to.</span></span> <span data-ttu-id="bd40b-118">Ef þú sameinar á tvo mismunandi vegu verður að bæta við sama lykli í alla fjóra flokka samstæðulykla.</span><span class="sxs-lookup"><span data-stu-id="bd40b-118">If you consolidate in two different ways, you must add the same account to all four consolidation account groups.</span></span>
-   <span data-ttu-id="bd40b-119">**Samstæðulykill** – Skráðu gildi samstæðulykilsins.</span><span class="sxs-lookup"><span data-stu-id="bd40b-119">**Consolidation account** – Enter the value of the consolidation account.</span></span> <span data-ttu-id="bd40b-120">Þetta gildi þarf ekki að vera lykill úr bókhaldslykill.</span><span class="sxs-lookup"><span data-stu-id="bd40b-120">This value doesn't have to be an account from a chart of accounts.</span></span> <span data-ttu-id="bd40b-121">Það getur verið hvaða gildi sem þú vilt.</span><span class="sxs-lookup"><span data-stu-id="bd40b-121">It can be any value that you require.</span></span>
-   <span data-ttu-id="bd40b-122">**Heiti samstæðulykils** – Skráðu heiti reikningsins eins og það á að birtast á fyrirspurnum og skýrslum.</span><span class="sxs-lookup"><span data-stu-id="bd40b-122">**Consolidation account name** – Enter the name of account as you want it to appear on inquiries and reports.</span></span>
-   <span data-ttu-id="bd40b-123">**SAT stig** – Þessi reitur er notaður til að tilkynna lyklayfirlit til mexíkanskra skattayfirvalda.</span><span class="sxs-lookup"><span data-stu-id="bd40b-123">**SAT level** – This field is used to report account statements to the Mexican tax authorities.</span></span> 

<span data-ttu-id="bd40b-124">Þegar þú hefur lokið stofnun á flokkum samstæðulykla og viðbótar samstæðulykla er hægt að velja flokkinn í ferlinu Sameina á netinu.</span><span class="sxs-lookup"><span data-stu-id="bd40b-124">When you've finished creating your consolidation account groups and additional consolidation accounts, you can select the group in the Consolidate online process.</span></span>


<span data-ttu-id="bd40b-125">Nánari upplýsingar er að finna í [Stofna samstæðuhópa og fleiri samstæðulykla](../general-ledger/tasks/create-consolidation-groups.md)</span><span class="sxs-lookup"><span data-stu-id="bd40b-125">For more information, see [Create consolidation groups and additional consolidation accounts](../general-ledger/tasks/create-consolidation-groups.md).</span></span> 




