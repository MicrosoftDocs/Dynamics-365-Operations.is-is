---
title: "Grunnstilla hliðstæður verkþátt í verkflæði"
description: "Til að skilgreina samhliða verkþátt, Ljúka eftirfarandi aðgerðum í verkflæðisritill."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ec1c1d8abc49deb8ef16322370c59d40b01d344c
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="configure-a-parallel-activity-in-a-workflow"></a><span data-ttu-id="4f05c-103">Grunnstilla hliðstæður verkþátt í verkflæði</span><span class="sxs-lookup"><span data-stu-id="4f05c-103">Configure a parallel activity in a workflow</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="4f05c-104">Til að skilgreina samhliða verkþátt, Ljúka eftirfarandi aðgerðum í verkflæðisritill.</span><span class="sxs-lookup"><span data-stu-id="4f05c-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="4f05c-105">Samhliða verkþáttur samanstendur úr verkflæðisgreinar sem eru keyrðar á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="4f05c-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="4f05c-106">Nefna Hliðstæður verkþáttur</span><span class="sxs-lookup"><span data-stu-id="4f05c-106">Name a parallel activity</span></span>
<span data-ttu-id="4f05c-107">Fylgið þessum skrefum til að færa inn heiti á samhliða aðgerð.</span><span class="sxs-lookup"><span data-stu-id="4f05c-107">Follow these steps to enter a name for a parallel activity.</span></span>
1.  <span data-ttu-id="4f05c-108">Hægrismellt á hliðstæður verkþáttur og smellið síðan á **Eiginleika** til að opna í **Eiginleika** skjámynd.</span><span class="sxs-lookup"><span data-stu-id="4f05c-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2.  <span data-ttu-id="4f05c-109">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="4f05c-109">In the left pane, click **Basic Settings**.</span></span>
3.  <span data-ttu-id="4f05c-110">Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir hliðstæður verkþáttur</span><span class="sxs-lookup"><span data-stu-id="4f05c-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4.  <span data-ttu-id="4f05c-111">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="4f05c-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="4f05c-112">Skilgreina greinar Hliðstæður verkþáttur</span><span class="sxs-lookup"><span data-stu-id="4f05c-112">Configure the branches of a parallel activity</span></span>
<span data-ttu-id="4f05c-113">Fylgdu eftirfarandi skrefum til að bæta við og skilgreina greinar þessa hliðstæður verkþáttur.</span><span class="sxs-lookup"><span data-stu-id="4f05c-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>
1. <span data-ttu-id="4f05c-114">Tvísmellið á samhliða verkþáttar til að birta greinar hins samhliða verkþáttar.</span><span class="sxs-lookup"><span data-stu-id="4f05c-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="4f05c-115">Til að bæta við grein, dragið á **Grein** einingu úr á **verkflæðiseiningar** svæði á innskotsstaður í striga.</span><span class="sxs-lookup"><span data-stu-id="4f05c-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="4f05c-116">Eftirfarandi tala sýnir innskotsstaði. ![innskotsstaður](./media/workflow_insertionpoint.gif)</span><span class="sxs-lookup"><span data-stu-id="4f05c-116">The following figure shows an insertion point.![Insertion point](./media/workflow_insertionpoint.gif)</span></span>

   |                                              <span data-ttu-id="4f05c-117"><strong>Ábending</strong></span><span class="sxs-lookup"><span data-stu-id="4f05c-117"><strong>Note</strong></span></span>                                               |
   |------------------------------------------------------------------------------------------------------------------|
   | <span data-ttu-id="4f05c-118">Röðun greina er ekki mikilvæg þar sem allar greinar samhliða verkþáttar keyra á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="4f05c-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span> |


3. <span data-ttu-id="4f05c-119">Til þess að skilgreina hver grein, sjá [Skilgreina samhliða grein](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="4f05c-119">To configure each branch, see [Configure a parallel branch](configure-parallel-branch-workflow.md).</span></span>






