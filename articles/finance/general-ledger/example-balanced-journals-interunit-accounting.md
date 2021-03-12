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
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f189d1ed5b0917c9975587accc2275556ceb8143
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968755"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="bd06b-103">Jafnaðar færslubækur fyrir millieiningabókhald</span><span class="sxs-lookup"><span data-stu-id="bd06b-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd06b-104">Þessi grein sýnir hvernig færslubók er jöfnuð sjálfkrafa þegar jöfnunarfjárhagsvídd er valin á síðunni Fjárhagur.</span><span class="sxs-lookup"><span data-stu-id="bd06b-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="bd06b-105">Ef bókhaldsfærslur eru ekki jafnaðar á stigi fjárhagsvíddargilda, eru sjálfkrafa stofnaðar lykilfærslur til að jafna við færslubókina.</span><span class="sxs-lookup"><span data-stu-id="bd06b-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="bd06b-106">Þessar lykilfærslur nota **Millieining - debet** og **Millieining - kredit** bókunargerðir á síðunni **Fjárhagslyklar fyrir sjálfvirkar færslur** til að ákvarða aðallykilinn.</span><span class="sxs-lookup"><span data-stu-id="bd06b-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="bd06b-107">Til dæmis er Fyrirtækiseining, sem er anna hluti fjárhagslykils, valið sem jöfnunarfjárhagsvídd og eftirfarandi bókhaldsfærslur verða síðan stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="bd06b-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="bd06b-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="bd06b-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="bd06b-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="bd06b-109">100.00 DR</span></span> |
| <span data-ttu-id="bd06b-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="bd06b-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="bd06b-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="bd06b-111">100.00 DR</span></span> |
| <span data-ttu-id="bd06b-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="bd06b-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="bd06b-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="bd06b-113">200.00 CR</span></span> |

<span data-ttu-id="bd06b-114">Í þessu tilfelli eru eftirfarandi stöður ákvarðaðar:</span><span class="sxs-lookup"><span data-stu-id="bd06b-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="bd06b-115">Fyrir fyrirtækiseiningu MSP = 100.00 CR</span><span class="sxs-lookup"><span data-stu-id="bd06b-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="bd06b-116">Fyrir fyrirtækiseiningu NY = 100.00 DR</span><span class="sxs-lookup"><span data-stu-id="bd06b-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="bd06b-117">Þessvegna eru°eftirfarandi bókhaldsfærslur stofnaðar sjálfkrafa til að jafna færslubókina á stigi fjárhagsvíddargilda.</span><span class="sxs-lookup"><span data-stu-id="bd06b-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="bd06b-118">(Debet millieininga) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="bd06b-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="bd06b-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="bd06b-119">100.00 DR</span></span> |
| <span data-ttu-id="bd06b-120">(Kredit millieininga) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="bd06b-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="bd06b-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="bd06b-121">100.00 CR</span></span> |





