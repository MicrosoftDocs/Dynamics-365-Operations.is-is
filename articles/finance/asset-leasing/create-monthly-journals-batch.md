---
title: Stofna mánaðarlegar færslubókarfærslur í runu
description: Þetta efnisatriði útskýrir hvernig á að stofna færslubókarfærslur í runu til að auka skilvirkni þegar mánaðarleg útgjöld eru skráð.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a2293f6bd3ce66832996652c3bfca0fc4bc73782
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4444578"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="624c9-103">Stofna mánaðarlegar færslubókarfærslur í runu</span><span class="sxs-lookup"><span data-stu-id="624c9-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="624c9-104">Þetta efnisatriði útskýrir hvernig á að stofna færslubókarfærslur í runu til að auka skilvirkni þegar mánaðarleg útgjöld eru skráð.</span><span class="sxs-lookup"><span data-stu-id="624c9-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="624c9-105">Hægt er að nota runuvinnslur til að stofna bókarfærslur úr mörgum áætlunum.</span><span class="sxs-lookup"><span data-stu-id="624c9-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="624c9-106">Þessar bókarfærslur geta falið í sér leigugreiðslur, skaðabætur, afskriftir, afskriftir afnotaréttar á eign og rekstrarkostnað.</span><span class="sxs-lookup"><span data-stu-id="624c9-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="624c9-107">Einnig er hægt að nota runuvinnslu til að gera fyrstu viðurkenningu margra leigusamninga samtímis eða búa til skiptileiðréttingar fyrir marga leigusamninga samtímis.</span><span class="sxs-lookup"><span data-stu-id="624c9-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="624c9-108">Til að setja upp runuvinnslu, eða til að vinna með greiðslureikninga, afskriftir eða vexti fyrir marga leigusamninga, ferðu í **Eignarleiga \> Reglubundið \> Runubókarstofnun**.</span><span class="sxs-lookup"><span data-stu-id="624c9-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="624c9-109">Í svarglugganum sem birtist er hægt að velja áætlunina sem stofna á færslubókarfærslur úr.</span><span class="sxs-lookup"><span data-stu-id="624c9-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="624c9-110">Einnig er hægt að tilgreina hvort keyra eigi runuvinnsluna fyrir tilteknar einingar, leigusamningsflokka eða leigubækur.</span><span class="sxs-lookup"><span data-stu-id="624c9-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="624c9-111">Síðari færslur, svo sem afskriftaráætlanir skulda, greiðslur, afskriftir og kostnaður, verða aðeins bókaðar eftir að upphafleg viðurkenning fyrir samsvarandi leigusamninga er bókuð.</span><span class="sxs-lookup"><span data-stu-id="624c9-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="624c9-112">Færslubókarfærslur eru stofnaðar en þær verða ekki bókaðar fyrr en **Keyra** skipunin er valin.</span><span class="sxs-lookup"><span data-stu-id="624c9-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>
