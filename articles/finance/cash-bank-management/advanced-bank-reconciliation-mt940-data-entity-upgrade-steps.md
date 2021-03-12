---
title: Innflutningur ítarlegrar bankaafstemmingar MT940 – Uppfærsla samsettrar gagnaeiningar
description: Raðnúmeri þarf að bæta við einingunni innflutningur bankayfirlits til að styðja MT940 sniði.
author: panolte
manager: AnnBe
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4d3bd54f0f2329c8c0602171a7f3c1ca444672b3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985412"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="4da1a-103">Innflutningur ítarlegrar bankaafstemmingar MT940 – Uppfærsla samsettrar gagnaeiningar</span><span class="sxs-lookup"><span data-stu-id="4da1a-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4da1a-104">Raðnúmeri þarf að bæta við einingunni innflutningur bankayfirlits til að styðja MT940 sniði.</span><span class="sxs-lookup"><span data-stu-id="4da1a-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="4da1a-105">Fylgið eftirfarandi skrefum til að bæta einingunni innflutningur bankayfirlits til að styðja MT940 sniði.</span><span class="sxs-lookup"><span data-stu-id="4da1a-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="4da1a-106">Taka saman og samstilla eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="4da1a-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="4da1a-107">Samsett eining\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="4da1a-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="4da1a-108">Eining\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="4da1a-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="4da1a-109">Eining\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="4da1a-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="4da1a-110">Eining\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="4da1a-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="4da1a-111">Entity\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="4da1a-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="4da1a-112">Töfbles\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="4da1a-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="4da1a-113">Gagnastjórnun\\gagnaverk.</span><span class="sxs-lookup"><span data-stu-id="4da1a-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="4da1a-114">Hlaða MT940 innflutningsverk</span><span class="sxs-lookup"><span data-stu-id="4da1a-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="4da1a-115">Breyta XSLT.</span><span class="sxs-lookup"><span data-stu-id="4da1a-115">Change XSLT.</span></span>
            -   <span data-ttu-id="4da1a-116">Smellið á **Skoða kort**.</span><span class="sxs-lookup"><span data-stu-id="4da1a-116">Click **View map**.</span></span>
            -   <span data-ttu-id="4da1a-117">Smellt er á **Skoða kort** á skjal bankayfirlits.</span><span class="sxs-lookup"><span data-stu-id="4da1a-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="4da1a-118">Smelltu á **Umbreytingar**</span><span class="sxs-lookup"><span data-stu-id="4da1a-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="4da1a-119">Eyða skrá BankReconiliation-to-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="4da1a-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="4da1a-120">Bætið nýja útgáfu af BankReconiliation-to-Composite.xsl.</span><span class="sxs-lookup"><span data-stu-id="4da1a-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="4da1a-121">Sýna **Raðnúmer** á **Upprunagögn** útlit.</span><span class="sxs-lookup"><span data-stu-id="4da1a-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="4da1a-122">Snið upprunagagna = XML-Element.</span><span class="sxs-lookup"><span data-stu-id="4da1a-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="4da1a-123">Nafn einingar = bankayfirlit.</span><span class="sxs-lookup"><span data-stu-id="4da1a-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="4da1a-124">Hlaða upp gagnaskrá = ný útgáfa SampleBankCompositeEntity.xml.</span><span class="sxs-lookup"><span data-stu-id="4da1a-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="4da1a-125">Smellið á **„Já“** til að skrifa yfir núgildandi skrá.</span><span class="sxs-lookup"><span data-stu-id="4da1a-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="4da1a-126">Smellið á **Já** til að mynda nýja vörpun.</span><span class="sxs-lookup"><span data-stu-id="4da1a-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="4da1a-127">Staðfestið að S **equenceNumber** er varpað.</span><span class="sxs-lookup"><span data-stu-id="4da1a-127">Verify that S **equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="4da1a-128">Smellt er á **Skoða kort** á yfirlitseiningunni.</span><span class="sxs-lookup"><span data-stu-id="4da1a-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="4da1a-129">Staðfestið að **SequenceNumber** er varpað úr uppruna í sviðsetningu.</span><span class="sxs-lookup"><span data-stu-id="4da1a-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="4da1a-130">Flytja inn nýtt uppgjör.</span><span class="sxs-lookup"><span data-stu-id="4da1a-130">Import the new statement.</span></span>




