---
title: Unnið er úr beint afleiddum staðfestum pöntunum með verkflæði endurskoðunar
description: Beint afleiddar staðfestar pantanir eru unnar með vinnuflæði sem hefur stöðuna Í endurskoðun.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026617"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a><span data-ttu-id="4a3eb-103">Unnið er úr beint afleiddum staðfestum pöntunum með verkflæði endurskoðunar</span><span class="sxs-lookup"><span data-stu-id="4a3eb-103">Directly derived firmed orders are processed by an in-review workflow</span></span>

<span data-ttu-id="4a3eb-104">KB númer: 4612450</span><span class="sxs-lookup"><span data-stu-id="4a3eb-104">KB number: 4612450</span></span>

## <a name="symptoms"></a><span data-ttu-id="4a3eb-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="4a3eb-105">Symptoms</span></span>

<span data-ttu-id="4a3eb-106">Beint afleiddar staðfestar pantanir eru unnar með vinnuflæði sem hefur stöðuna *Í endurskoðun*.</span><span class="sxs-lookup"><span data-stu-id="4a3eb-106">Directly derived firmed orders are processed by a workflow that has a status of *In-review*.</span></span>

## <a name="resolution"></a><span data-ttu-id="4a3eb-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="4a3eb-107">Resolution</span></span>

<span data-ttu-id="4a3eb-108">Þegar kveikt er á breytingarrakningu er staðan *Í endurskoðun* úthlutuð á staðferstar afleiddar pantanir (innkaupapantanir undirverktaka).</span><span class="sxs-lookup"><span data-stu-id="4a3eb-108">When change tracking is enabled, a status of *In-review* is assigned to firmed derived orders (subcontract purchase orders).</span></span> <span data-ttu-id="4a3eb-109">Ef innkaupapöntun er afleidd (innkaupapöntun undirverktaka) er hún því aðeins send í vinnuflæði.</span><span class="sxs-lookup"><span data-stu-id="4a3eb-109">Therefore, if a purchase order is derived (a subcontract purchase order), it's only submitted to a workflow.</span></span> <span data-ttu-id="4a3eb-110">Ef innkaupapöntun er staðfest innkaupatillaga er hún sjálfkrafa samþykkt til að tryggja að áætlunarvélin stofni ekki nýjar áætlaðar pantanir á meðan innkaupapöntunin er enn í stöðunni *Drög*.</span><span class="sxs-lookup"><span data-stu-id="4a3eb-110">If a purchase order is a firmed planned purchase order, it's automatically approved to ensure that the planning engine doesn't create new planned orders while the purchase order is still in *Draft* status.</span></span>
