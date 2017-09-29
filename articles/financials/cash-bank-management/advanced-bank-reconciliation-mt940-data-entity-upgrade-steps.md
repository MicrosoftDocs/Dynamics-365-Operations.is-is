---
title: "Innflutningur ítarlegrar bankaafstemmingar MT940 – Uppfærsla samsettrar gagnaeiningar"
description: "Raðnúmeri þarf að bæta við einingunni innflutningur bankayfirlits til að styðja MT940 sniði."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0fb86cd4264d5420c479e14f7eed41e480c88b63
ms.contentlocale: is-is
ms.lasthandoff: 07/18/2017

---

# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="c1f03-103">Innflutningur ítarlegrar bankaafstemmingar MT940 – Uppfærsla samsettrar gagnaeiningar</span><span class="sxs-lookup"><span data-stu-id="c1f03-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c1f03-104">Raðnúmeri þarf að bæta við einingunni innflutningur bankayfirlits til að styðja MT940 sniði.</span><span class="sxs-lookup"><span data-stu-id="c1f03-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="c1f03-105">Fylgið eftirfarandi skrefum til að bæta einingunni innflutningur bankayfirlits til að styðja MT940 sniði.</span><span class="sxs-lookup"><span data-stu-id="c1f03-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="c1f03-106">Taka saman og samstilla eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="c1f03-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="c1f03-107">Samsett eining\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="c1f03-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="c1f03-108">Eining\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="c1f03-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="c1f03-109">Eining\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="c1f03-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="c1f03-110">Eining\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="c1f03-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="c1f03-111">Entity\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="c1f03-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="c1f03-112">Töfbles\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="c1f03-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="c1f03-113">Gagnastjórnun\\gagnaverk.</span><span class="sxs-lookup"><span data-stu-id="c1f03-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="c1f03-114">Hlaða MT940 innflutningsverk</span><span class="sxs-lookup"><span data-stu-id="c1f03-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="c1f03-115">Breyta XSLT.</span><span class="sxs-lookup"><span data-stu-id="c1f03-115">Change XSLT.</span></span>
            -   <span data-ttu-id="c1f03-116">Smellið á **Skoða kort**.</span><span class="sxs-lookup"><span data-stu-id="c1f03-116">Click **View map**.</span></span>
            -   <span data-ttu-id="c1f03-117">Smellt er á **Skoða kort** á skjal bankayfirlits.</span><span class="sxs-lookup"><span data-stu-id="c1f03-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="c1f03-118">Smelltu á **Umbreytingar**</span><span class="sxs-lookup"><span data-stu-id="c1f03-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="c1f03-119">Eyða skrá BankReconiliation-to-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="c1f03-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="c1f03-120">Bætið nýja útgáfu af BankReconiliation-to-Composite.xsl.</span><span class="sxs-lookup"><span data-stu-id="c1f03-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="c1f03-121">Sýna **Raðnúmer** á **Upprunagögn** útlit.</span><span class="sxs-lookup"><span data-stu-id="c1f03-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="c1f03-122">Snið upprunagagna = XML-Element.</span><span class="sxs-lookup"><span data-stu-id="c1f03-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="c1f03-123">Nafn einingar = bankayfirlit.</span><span class="sxs-lookup"><span data-stu-id="c1f03-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="c1f03-124">Hlaða upp gagnaskrá = ný útgáfa SampleBankCompositeEntity.xml.</span><span class="sxs-lookup"><span data-stu-id="c1f03-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="c1f03-125">Smellið á **„Já“** til að skrifa yfir núgildandi skrá.</span><span class="sxs-lookup"><span data-stu-id="c1f03-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="c1f03-126">Smellið á **Já** til að mynda nýja vörpun.</span><span class="sxs-lookup"><span data-stu-id="c1f03-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="c1f03-127">Staðfestið að S**equenceNumber** er varpað.</span><span class="sxs-lookup"><span data-stu-id="c1f03-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="c1f03-128">Smellt er á **Skoða kort** á yfirlitseiningunni.</span><span class="sxs-lookup"><span data-stu-id="c1f03-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="c1f03-129">Staðfestið að **SequenceNumber** er varpað úr uppruna í sviðsetningu.</span><span class="sxs-lookup"><span data-stu-id="c1f03-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="c1f03-130">Flytja inn nýtt uppgjör.</span><span class="sxs-lookup"><span data-stu-id="c1f03-130">Import the new statement.</span></span>





