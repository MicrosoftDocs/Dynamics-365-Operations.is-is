---
title: Uppfæra verktakamiða lánardrottna og búa til skýrslu
description: Þetta ferli fer í gegnum bókun á reikningi lánardrottins með meðfylgjandi upplýsingar um verktakamiða og myndun skýrslu um verktakamiða.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: kfend
ms.search.region: Iceland
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 567ef30384337fb93b498371ec3f991d40aa90e5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982056"
---
# <a name="update-vendor-invoice-declarations-and-generate-the-report"></a><span data-ttu-id="334fa-103">Uppfæra verktakamiða lánardrottna og búa til skýrslu</span><span class="sxs-lookup"><span data-stu-id="334fa-103">Update vendor invoice declarations and generate the report</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="334fa-104">Þetta ferli fer í gegnum bókun á reikningi lánardrottins með meðfylgjandi upplýsingar um verktakamiða og myndun skýrslu um verktakamiða.</span><span class="sxs-lookup"><span data-stu-id="334fa-104">This procedure walks you through posting a vendor invoice with invoice declaration information attached and generating an invoice declaration report.</span></span> <span data-ttu-id="334fa-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF með land aðalaðsetur lögaðila uppfært í Ísland.</span><span class="sxs-lookup"><span data-stu-id="334fa-105">The demo data company used to create this procedure is DEMF with the country of legal entity primary address updated to Iceland.</span></span>


## <a name="post-a-vendor-invoice"></a><span data-ttu-id="334fa-106">Bóka reikning lánardrottins</span><span class="sxs-lookup"><span data-stu-id="334fa-106">Post a vendor invoice</span></span>
1. <span data-ttu-id="334fa-107">Fara í Viðskiptaskuldir > Reikningar > Reikningabók.</span><span class="sxs-lookup"><span data-stu-id="334fa-107">Go to Accounts payable > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="334fa-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="334fa-108">Click New.</span></span>
3. <span data-ttu-id="334fa-109">Í reitnum Heiti velurðu ‚APInvoice‘.</span><span class="sxs-lookup"><span data-stu-id="334fa-109">In the Name field, In the Name field, select 'APInvoice'.</span></span>
4. <span data-ttu-id="334fa-110">Smellið á Línur.</span><span class="sxs-lookup"><span data-stu-id="334fa-110">Click Lines.</span></span>
5. <span data-ttu-id="334fa-111">Í reitinn Lykill skal færa inn gildin 'IS-001'.</span><span class="sxs-lookup"><span data-stu-id="334fa-111">In the Account field, specify the values 'IS-001'.</span></span>
6. <span data-ttu-id="334fa-112">Í reitinn Reikningur skal færa inn "IS-001-01".</span><span class="sxs-lookup"><span data-stu-id="334fa-112">In the Invoice field, type 'IS-001-01'.</span></span>
7. <span data-ttu-id="334fa-113">Í reitnum Kredit skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="334fa-113">In the Credit field, enter a number.</span></span>
8. <span data-ttu-id="334fa-114">Í reitinn Mótlykill skal tilgreina gildin '200130--'.</span><span class="sxs-lookup"><span data-stu-id="334fa-114">In the Offset account field, specify the values '200130--'.</span></span>
9. <span data-ttu-id="334fa-115">Smellið á flipann Reikningur.</span><span class="sxs-lookup"><span data-stu-id="334fa-115">Click the Invoice tab.</span></span>
10. <span data-ttu-id="334fa-116">Í reitinn Skjal skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="334fa-116">In the Document field, type a value.</span></span>
11. <span data-ttu-id="334fa-117">Í reitnum Reikningsdagsetning er dagsetning í dag rituð.</span><span class="sxs-lookup"><span data-stu-id="334fa-117">In the Invoice date field, enter today's date.</span></span>
12. <span data-ttu-id="334fa-118">Í reitnum Verktakamiðar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="334fa-118">In the Invoice declaration field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="334fa-119">Í listanum velurðu flokkinn Verktakamiðar.</span><span class="sxs-lookup"><span data-stu-id="334fa-119">In the list, select the Invoice declaration category.</span></span>
14. <span data-ttu-id="334fa-120">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="334fa-120">Click Post.</span></span>

## <a name="generate-an-invoice-declaration"></a><span data-ttu-id="334fa-121">Mynda verktakamiða</span><span class="sxs-lookup"><span data-stu-id="334fa-121">Generate an invoice declaration</span></span>
1. <span data-ttu-id="334fa-122">Fara í Viðskiptaskuldir > Fyrirspurnir og skýrslur > Reikningur > Skýrsla um verktakamiða lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="334fa-122">Go to Accounts payable > Inquiries and reports > Invoice > Vendor invoice declaration report.</span></span>
2. <span data-ttu-id="334fa-123">Í reitnum Yfirvöld skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="334fa-123">In the Authority field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="334fa-124">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="334fa-124">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="334fa-125">Dagsetning er rituð í reitinn Frá dags.</span><span class="sxs-lookup"><span data-stu-id="334fa-125">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="334fa-126">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="334fa-126">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="334fa-127">Merkið við gátreitinn Stofna skýrsluskrá.</span><span class="sxs-lookup"><span data-stu-id="334fa-127">Check the Create report file checkbox.</span></span>
7. <span data-ttu-id="334fa-128">Í reitinn Heiti skal slá inn ‚Skýrsla um verktakamiða lánardrottins (IS)‘.</span><span class="sxs-lookup"><span data-stu-id="334fa-128">In the Name field, select 'Vendor invoice declaration report (IS)'..</span></span>
8. <span data-ttu-id="334fa-129">Merkið við gátreitinn Stofna textaskrá.</span><span class="sxs-lookup"><span data-stu-id="334fa-129">Check the Create text file checkbox.</span></span>
9. <span data-ttu-id="334fa-130">Í reitinn Heiti skal slá inn ‚Skýrsla um verktakamiða lánardrottins yfirlýsing (IS)‘.</span><span class="sxs-lookup"><span data-stu-id="334fa-130">In the Name field, select 'Vendor invoice declaration (IS)'.</span></span>
10. <span data-ttu-id="334fa-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="334fa-131">Click OK.</span></span>

