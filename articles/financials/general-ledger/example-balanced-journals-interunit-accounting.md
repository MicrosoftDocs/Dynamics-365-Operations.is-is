---
title: Jafnaðar færslubækur fyrir millieiningabókhald
description: Þessi grein sýnir hvernig færslubók er jöfnuð sjálfkrafa þegar jöfnunarfjárhagsvídd er valin á síðunni Fjárhagur.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e84d96b5467b38e07a9ed31f142c27b638289284
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839354"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="076b8-103">Jafnaðar færslubækur fyrir millieiningabókhald</span><span class="sxs-lookup"><span data-stu-id="076b8-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="076b8-104">Þessi grein sýnir hvernig færslubók er jöfnuð sjálfkrafa þegar jöfnunarfjárhagsvídd er valin á síðunni Fjárhagur.</span><span class="sxs-lookup"><span data-stu-id="076b8-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="076b8-105">Ef bókhaldsfærslur eru ekki jafnaðar á stigi fjárhagsvíddargilda, eru sjálfkrafa stofnaðar lykilfærslur til að jafna við færslubókina.</span><span class="sxs-lookup"><span data-stu-id="076b8-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="076b8-106">Þessar lykilfærslur nota **Millieining - debet** og **Millieining - kredit** bókunargerðir á síðunni **Fjárhagslyklar fyrir sjálfvirkar færslur** til að ákvarða aðallykilinn.</span><span class="sxs-lookup"><span data-stu-id="076b8-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="076b8-107">Til dæmis er Fyrirtækiseining, sem er anna hluti fjárhagslykils, valið sem jöfnunarfjárhagsvídd og eftirfarandi bókhaldsfærslur verða síðan stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="076b8-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="076b8-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="076b8-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="076b8-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="076b8-109">100.00 DR</span></span> |
| <span data-ttu-id="076b8-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="076b8-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="076b8-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="076b8-111">100.00 DR</span></span> |
| <span data-ttu-id="076b8-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="076b8-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="076b8-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="076b8-113">200.00 CR</span></span> |

<span data-ttu-id="076b8-114">Í þessu tilfelli eru eftirfarandi stöður ákvarðaðar:</span><span class="sxs-lookup"><span data-stu-id="076b8-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="076b8-115">Fyrir fyrirtækiseiningu MSP = 100.00 CR</span><span class="sxs-lookup"><span data-stu-id="076b8-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="076b8-116">Fyrir fyrirtækiseiningu NY = 100.00 DR</span><span class="sxs-lookup"><span data-stu-id="076b8-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="076b8-117">Þessvegna eru°eftirfarandi bókhaldsfærslur stofnaðar sjálfkrafa til að jafna færslubókina á stigi fjárhagsvíddargilda.</span><span class="sxs-lookup"><span data-stu-id="076b8-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="076b8-118">(Debet millieininga) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="076b8-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="076b8-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="076b8-119">100.00 DR</span></span> |
| <span data-ttu-id="076b8-120">(Kredit millieininga) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="076b8-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="076b8-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="076b8-121">100.00 CR</span></span> |





