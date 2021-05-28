---
title: Uppsöfnun viðskiptavinaafsláttar mistókst þegar flokkar vöruafsláttar eru notaðir
description: Þegar þú notar samninga um afslátt viðskiptavina ásamt vöruafsláttarhópum er afsláttur reiknaður út en uppsöfnun mistekst.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026599"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a><span data-ttu-id="7b61b-103">Uppsöfnun viðskiptavinaafsláttar mistókst þegar flokkar vöruafsláttar eru notaðir</span><span class="sxs-lookup"><span data-stu-id="7b61b-103">Cumulation of customer rebates fails when item rebate groups are used</span></span>

<span data-ttu-id="7b61b-104">KB númer: 4611372</span><span class="sxs-lookup"><span data-stu-id="7b61b-104">KB number: 4611372</span></span>

## <a name="symptoms"></a><span data-ttu-id="7b61b-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="7b61b-105">Symptoms</span></span>

<span data-ttu-id="7b61b-106">Þegar þú notar samninga um afslátt viðskiptavina (af gerðinni *upphæð*) ásamt vöruafsláttarhópum er afsláttur reiknaður út en uppsöfnun mistekst.</span><span class="sxs-lookup"><span data-stu-id="7b61b-106">When you use customer rebate agreements (of the *amount* type) in combination with item rebate groups, rebates are calculated, but cumulation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="7b61b-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="7b61b-107">Resolution</span></span>

<span data-ttu-id="7b61b-108">Kerfið hagar sér eins og það er hannað.</span><span class="sxs-lookup"><span data-stu-id="7b61b-108">The system is behaving as designed.</span></span> <span data-ttu-id="7b61b-109">Vöruflokkar flokka aðeins vörur með sama þröskuldsskilyrði.</span><span class="sxs-lookup"><span data-stu-id="7b61b-109">Item groups group only items that have the same threshold condition.</span></span> <span data-ttu-id="7b61b-110">Afsláttarskilyrðið (þröskuldur) er sett á móti upphæðinni fyrir hvern hlut, ekki á móti uppsafnaðri upphæð fyrir hvern hlut í vöruflokknum.</span><span class="sxs-lookup"><span data-stu-id="7b61b-110">The rebate condition (threshold) is set against the amount for each item, not against the cumulated amount for any item in the item group.</span></span>
