---
title: Uppfæra samsetta einingu færslubókar banka
description: Eftirfarandi skrefum þarf til að bæta við aukalegum reitnum BankTransactionType við samsetta BankJournalEntity.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7e265915cf3f53a8243788b50a9374d521efbbae
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819604"
---
# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="4d108-103">Uppfæra samsetta einingu færslubókar banka</span><span class="sxs-lookup"><span data-stu-id="4d108-103">Update the bank journal composite entity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d108-104">Eftirfarandi skrefum þarf til að bæta við aukalegum reitnum BankTransactionType við samsetta BankJournalEntity.</span><span class="sxs-lookup"><span data-stu-id="4d108-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="4d108-105">Fylgið eftirfarandi skrefum til að bæta reitnum BankTransactionType við samsetta BankJournalEntity.</span><span class="sxs-lookup"><span data-stu-id="4d108-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="4d108-106">Tala sa,am og samstilla eftirfarandi samsettar einingar færslubókar banka, einingar og sviðsetningartöflur:</span><span class="sxs-lookup"><span data-stu-id="4d108-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="4d108-107">Samsett eining\\BankJournalEntity</span><span class="sxs-lookup"><span data-stu-id="4d108-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="4d108-108">Eining\\BankJournalHeaderEntity</span><span class="sxs-lookup"><span data-stu-id="4d108-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="4d108-109">Eining\\BankJournalLineEntity</span><span class="sxs-lookup"><span data-stu-id="4d108-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="4d108-110">Tafla\\BankJournalHeaderStaging</span><span class="sxs-lookup"><span data-stu-id="4d108-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="4d108-111">Tafla\\BankJournalLineStaging</span><span class="sxs-lookup"><span data-stu-id="4d108-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="4d108-112">Gagnastjórnun\\gagnaverk</span><span class="sxs-lookup"><span data-stu-id="4d108-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="4d108-113">Sýna **Bankafærslu** gerð á **Upprunagögn** útlit.</span><span class="sxs-lookup"><span data-stu-id="4d108-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="4d108-114">Snið upprunagagna = XML-Element.</span><span class="sxs-lookup"><span data-stu-id="4d108-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="4d108-115">Nafn einingar = færslubók banka</span><span class="sxs-lookup"><span data-stu-id="4d108-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="4d108-116">Hlaða upp gagnaskrá = ný útgáfa SampleBankJournalCompositeEntity.xml</span><span class="sxs-lookup"><span data-stu-id="4d108-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="4d108-117">Smellið á **„Já“** til að skrifa yfir núgildandi skrá.</span><span class="sxs-lookup"><span data-stu-id="4d108-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="4d108-118">Smellið á **Já** til að mynda vörpun frá byrjun.</span><span class="sxs-lookup"><span data-stu-id="4d108-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="4d108-119">Staðfestið að Bankafærslugerð er varpað.</span><span class="sxs-lookup"><span data-stu-id="4d108-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="4d108-120">Smellið á **Skoða vörpun** á Línueiningar.</span><span class="sxs-lookup"><span data-stu-id="4d108-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="4d108-121">Staðfestið að bankafærslugerð er varpað úr uppruna í sviðsetningu.</span><span class="sxs-lookup"><span data-stu-id="4d108-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="4d108-122">Flytja inn nýtt uppgjör.</span><span class="sxs-lookup"><span data-stu-id="4d108-122">Import the new statement.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]