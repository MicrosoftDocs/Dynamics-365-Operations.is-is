---
title: Flytja inn og vinna með kreditkortafærslur
description: Í þessu efnisatriði er útskýrt hvernig á að flytja inn og viðhalda kostnaðartengdum kreditkortafærslum. Hægt er að setja upp þessar færslur þannig að þær séu fluttar inn sjálfkrafa á endurteknum tíma, og einnig er hægt að flytja þær inn handvirkt eftir þörfum.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4484ea6fa446c73b8854e7822237bb3c6b9f9023
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187568"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="cb12a-104">Flytja inn og vinna með kreditkortafærslur</span><span class="sxs-lookup"><span data-stu-id="cb12a-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb12a-105">Kostnaðartengdar kreditkortafærslur er hægt að setja upp þannig að þær séu fluttar inn sjálfkrafa á endurteknum tíma.</span><span class="sxs-lookup"><span data-stu-id="cb12a-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="cb12a-106">Einnig er hægt að flytja viðskiptin inn handvirkt eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="cb12a-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="cb12a-107">Kreditkortafærslurnar eru fluttar inn gagnaeiningunni Kreditkortafærslur.</span><span class="sxs-lookup"><span data-stu-id="cb12a-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="cb12a-108">Frekari upplýsingar um gagnaeiningar er að finna í [Gagnaeiningar](../../dev-itpro/data-entities/data-entities.md).</span><span class="sxs-lookup"><span data-stu-id="cb12a-108">For more information about data entities, see [Data entities](../../dev-itpro/data-entities/data-entities.md).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="cb12a-109">Flytja inn kreditkortafærslur</span><span class="sxs-lookup"><span data-stu-id="cb12a-109">Import credit card transactions</span></span>

1. <span data-ttu-id="cb12a-110">Á síðunni **Kreditkortafærslur** skal velja **Flytja inn færslur**.</span><span class="sxs-lookup"><span data-stu-id="cb12a-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="cb12a-111">Ef þú opnar gagnastjórnun í fyrsta skipti verður kerfið að uppfæra lista yfir gagnaeiningar áður en hægt er að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="cb12a-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="cb12a-112">Í reitnum **Heiti** skal slá inn einkvæma lýsingu innflutningsverksins.</span><span class="sxs-lookup"><span data-stu-id="cb12a-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="cb12a-113">Í **Snið upprunagagna** reitnum skal velja snið skárinnar sem inniheldur kreditkortafærslurnar til innflutnings.</span><span class="sxs-lookup"><span data-stu-id="cb12a-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="cb12a-114">Smellið á **Flytja inn** og veljið síðan skrána til að flytja inn.</span><span class="sxs-lookup"><span data-stu-id="cb12a-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="cb12a-115">Eftir að skránni hefur verið hlaðið upp skal staðfesta vörpun kreditkortafærslunnar og dálka gagnaeiningar kreditkortafærslunnar með því að velja **Skoða kort** tengilinn á reitnum.</span><span class="sxs-lookup"><span data-stu-id="cb12a-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="cb12a-116">Ef um er að ræða vörpunarvillur, eða ef nauðsynlegt er að breyta vörpuninni skal gera breytingar á vörpuninni í flipanum **Vörpunarbirting** eða **Vörpunarupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="cb12a-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="cb12a-117">Til að gera kreditkortafærslur sjálfvirkar skal velja **Stofna endurtekna gagnavinnslu**.</span><span class="sxs-lookup"><span data-stu-id="cb12a-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="cb12a-118">Svo er hægt að velja endurtekningar sem skilgreina hversu oft kreditkortafærslurskuli fluttar inn.</span><span class="sxs-lookup"><span data-stu-id="cb12a-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="cb12a-119">Þegar þú hefur lokið þessu skaltu velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cb12a-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="cb12a-120">Til að flytja inn völdu skrána strax skaltu velja **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="cb12a-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="cb12a-121">Ef villur eiga sér stað við innflutning er hægt að skoða keyrsluskrána eða sviðsetningargögn til að sjá villurnar sem verður að laga til að tryggja að innflutningur heppnist.</span><span class="sxs-lookup"><span data-stu-id="cb12a-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="cb12a-122">Ef nauðsynlegt er að flytja inn fleiri en eitt skjalasnið þarf að búa til aðskilin innflutningsverk fyrir hverja skjalagerð.</span><span class="sxs-lookup"><span data-stu-id="cb12a-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="cb12a-123">Endurúthluta kreditkortafærslum fyrir starfsmenn sem hafa lokið störfum</span><span class="sxs-lookup"><span data-stu-id="cb12a-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="cb12a-124">Þegar samningi starfsmanns er sagt upp er AD DS (Active Directory Domain Services) reikningur hans er gerður óvirkur.</span><span class="sxs-lookup"><span data-stu-id="cb12a-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="cb12a-125">Hins vegar gætu verið virkar kreditkortafærslur sem þarf samt að gjaldfæra og endurgreiða.</span><span class="sxs-lookup"><span data-stu-id="cb12a-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="cb12a-126">Á síðunni **Kreditkortafærslur** er hægt að endurúthluta starfsmanni á allar kreditkortafærslur þar sem tengdum starfsmanni hefur verið sagt upp störfum.</span><span class="sxs-lookup"><span data-stu-id="cb12a-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="cb12a-127">Veldu eina eða fleiri kreditkortafærslur og svo **Endurúthluta færslu**.</span><span class="sxs-lookup"><span data-stu-id="cb12a-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="cb12a-128">Þú getur síðan valið annan starfsmann til að úthluta kreditkortafærslunum á.</span><span class="sxs-lookup"><span data-stu-id="cb12a-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="cb12a-129">Eftir endurúthlutun kreditkortafærsluna er hægt að velja þær fyrir kostnaðarskýrslu og greiða hana með reglulegu ferli fyrir endurgreiðslu kostnaðarskýrslu.</span><span class="sxs-lookup"><span data-stu-id="cb12a-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
