---
title: Innflutningur ítarlegrar bankaafstemmingar MT940 – Uppfærsla samsettrar gagnaeiningar
description: Raðnúmeri þarf að bæta við einingunni innflutningur bankayfirlits til að styðja MT940 sniði.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 88eb5b3c408d36620ab550b29d2e5a3278d25d8a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842666"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="6a9f1-103">Innflutningur ítarlegrar bankaafstemmingar MT940 – Uppfærsla samsettrar gagnaeiningar</span><span class="sxs-lookup"><span data-stu-id="6a9f1-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a9f1-104">Raðnúmeri þarf að bæta við einingunni innflutningur bankayfirlits til að styðja MT940 sniði.</span><span class="sxs-lookup"><span data-stu-id="6a9f1-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="6a9f1-105">Fylgið eftirfarandi skrefum til að bæta einingunni innflutningur bankayfirlits til að styðja MT940 sniði.</span><span class="sxs-lookup"><span data-stu-id="6a9f1-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="6a9f1-106">Taka saman og samstilla eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="6a9f1-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="6a9f1-107">Samsett eining\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="6a9f1-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="6a9f1-108">Eining\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="6a9f1-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="6a9f1-109">Eining\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="6a9f1-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="6a9f1-110">Eining\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="6a9f1-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="6a9f1-111">Entity\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="6a9f1-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="6a9f1-112">Töfbles\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="6a9f1-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="6a9f1-113">Gagnastjórnun\\gagnaverk.</span><span class="sxs-lookup"><span data-stu-id="6a9f1-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="6a9f1-114">Hlaða MT940 innflutningsverk</span><span class="sxs-lookup"><span data-stu-id="6a9f1-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="6a9f1-115">Breyta XSLT.</span><span class="sxs-lookup"><span data-stu-id="6a9f1-115">Change XSLT.</span></span>
            -   <span data-ttu-id="6a9f1-116">Smellið á **Skoða kort**.</span><span class="sxs-lookup"><span data-stu-id="6a9f1-116">Click **View map**.</span></span>
            -   <span data-ttu-id="6a9f1-117">Smellt er á **Skoða kort** á skjal bankayfirlits.</span><span class="sxs-lookup"><span data-stu-id="6a9f1-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="6a9f1-118">Smelltu á **Umbreytingar**</span><span class="sxs-lookup"><span data-stu-id="6a9f1-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="6a9f1-119">Eyða skrá BankReconiliation-to-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="6a9f1-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="6a9f1-120">Bætið nýja útgáfu af BankReconiliation-to-Composite.xsl.</span><span class="sxs-lookup"><span data-stu-id="6a9f1-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="6a9f1-121">Sýna **Raðnúmer** á **Upprunagögn** útlit.</span><span class="sxs-lookup"><span data-stu-id="6a9f1-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="6a9f1-122">Snið upprunagagna = XML-Element.</span><span class="sxs-lookup"><span data-stu-id="6a9f1-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="6a9f1-123">Nafn einingar = bankayfirlit.</span><span class="sxs-lookup"><span data-stu-id="6a9f1-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="6a9f1-124">Hlaða upp gagnaskrá = ný útgáfa SampleBankCompositeEntity.xml.</span><span class="sxs-lookup"><span data-stu-id="6a9f1-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="6a9f1-125">Smellið á **„Já“** til að skrifa yfir núgildandi skrá.</span><span class="sxs-lookup"><span data-stu-id="6a9f1-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="6a9f1-126">Smellið á **Já** til að mynda nýja vörpun.</span><span class="sxs-lookup"><span data-stu-id="6a9f1-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="6a9f1-127">Staðfestið að S**equenceNumber** er varpað.</span><span class="sxs-lookup"><span data-stu-id="6a9f1-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="6a9f1-128">Smellt er á **Skoða kort** á yfirlitseiningunni.</span><span class="sxs-lookup"><span data-stu-id="6a9f1-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="6a9f1-129">Staðfestið að **SequenceNumber** er varpað úr uppruna í sviðsetningu.</span><span class="sxs-lookup"><span data-stu-id="6a9f1-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="6a9f1-130">Flytja inn nýtt uppgjör.</span><span class="sxs-lookup"><span data-stu-id="6a9f1-130">Import the new statement.</span></span>




