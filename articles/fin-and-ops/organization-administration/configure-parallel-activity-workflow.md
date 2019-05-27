---
title: Skilgreina hliðstæða verkþætti í verkflæði
description: Til að skilgreina samhliða verkþátt, Ljúka eftirfarandi aðgerðum í verkflæðisritill.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01c1fa876dd66ba6f0e1cdcecff56f424e117bd9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563320"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="b06b7-103">Skilgreina hliðstæða verkþætti í verkflæði</span><span class="sxs-lookup"><span data-stu-id="b06b7-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b06b7-104">Til að skilgreina samhliða verkþátt, Ljúka eftirfarandi aðgerðum í verkflæðisritill.</span><span class="sxs-lookup"><span data-stu-id="b06b7-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="b06b7-105">Samhliða verkþáttur samanstendur úr verkflæðisgreinar sem eru keyrðar á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="b06b7-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="b06b7-106">Nefna Hliðstæður verkþáttur</span><span class="sxs-lookup"><span data-stu-id="b06b7-106">Name a parallel activity</span></span>

<span data-ttu-id="b06b7-107">Fylgið þessum skrefum til að færa inn heiti á samhliða aðgerð.</span><span class="sxs-lookup"><span data-stu-id="b06b7-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="b06b7-108">Hægrismellt á hliðstæður verkþáttur og smellið síðan á **Eiginleika** til að opna í **Eiginleika** skjámynd.</span><span class="sxs-lookup"><span data-stu-id="b06b7-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="b06b7-109">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="b06b7-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="b06b7-110">Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir hliðstæður verkþáttur</span><span class="sxs-lookup"><span data-stu-id="b06b7-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="b06b7-111">Smellið á **Loka**.</span><span class="sxs-lookup"><span data-stu-id="b06b7-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="b06b7-112">Skilgreina greinar Hliðstæður verkþáttur</span><span class="sxs-lookup"><span data-stu-id="b06b7-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="b06b7-113">Fylgdu eftirfarandi skrefum til að bæta við og skilgreina greinar þessa hliðstæður verkþáttur.</span><span class="sxs-lookup"><span data-stu-id="b06b7-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="b06b7-114">Tvísmellið á samhliða verkþáttar til að birta greinar hins samhliða verkþáttar.</span><span class="sxs-lookup"><span data-stu-id="b06b7-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="b06b7-115">Til að bæta við grein, dragið á **Grein** einingu úr á **verkflæðiseiningar** svæði á innskotsstaður í striga.</span><span class="sxs-lookup"><span data-stu-id="b06b7-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="b06b7-116">Eftirfarandi tala sýnir innskotsstað.</span><span class="sxs-lookup"><span data-stu-id="b06b7-116">The following figure shows an insertion point.</span></span>

    ![Innskotsstaður](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="b06b7-118">Röðun greina er ekki mikilvæg þar sem allar greinar samhliða verkþáttar keyra á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="b06b7-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="b06b7-119">Til þess að skilgreina hver grein, sjá [Skilgreina samhliða grein](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="b06b7-119">To configure each branch, see [Configure a parallel branch](configure-parallel-branch-workflow.md).</span></span>
