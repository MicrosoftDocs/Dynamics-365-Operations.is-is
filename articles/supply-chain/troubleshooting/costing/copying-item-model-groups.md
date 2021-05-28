---
title: Vantar reitarstillingar þegar vörulíkanaflokkareru afritaðir á annan lögaðila
description: Reitarstillingar vantar þegar vörulíkanaflokkareru afritaðir á annan lögaðila
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f6fdfef0bc377418ed8a9c8830e74526a0b95eb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026604"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a><span data-ttu-id="27481-103">Vantar reitarstillingar þegar vörulíkanaflokkareru afritaðir á annan lögaðila</span><span class="sxs-lookup"><span data-stu-id="27481-103">Missing field settings when item model groups are copied to another legal entity</span></span>

<span data-ttu-id="27481-104">KB númer: 4612800</span><span class="sxs-lookup"><span data-stu-id="27481-104">KB number: 4612800</span></span>

## <a name="symptoms"></a><span data-ttu-id="27481-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="27481-105">Symptoms</span></span>

<span data-ttu-id="27481-106">Þegar þú afritar vörulíkanahópa til annars lögaðila (fyrirtækis) með eininguna *Birgðareglur vörulíkanaflokks* vantar sumar reitastillingar (til dæmis birgðalíkanið og lýsingin) í nýja líkanahópinn í lögaðilann.</span><span class="sxs-lookup"><span data-stu-id="27481-106">When you copy item model groups to another legal entity (company) by using the *Item model group inventory policies* entity, some field settings (for example, the inventory model and description) are missing in the new model group in the destination legal entity.</span></span>

## <a name="resolution"></a><span data-ttu-id="27481-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="27481-107">Resolution</span></span>

<span data-ttu-id="27481-108">Til að búa til heildarafrit af vörulíkanaflokki á annan lögaðila verður einnig að velja bæði birgðareglur vörulíkanaflokks (`InventInventoryPolicyEntity`) og áætlunarreglur kostnaðarflæðis (`InventCostFlowAssumptionPolicyEntity`) sem eru tengdar vörulíkanaflokknum.</span><span class="sxs-lookup"><span data-stu-id="27481-108">To create a complete copy of an item model group to another legal entity, you must also select both the item model group inventory policies (`InventInventoryPolicyEntity`) and the cost flow assumption policies (`InventCostFlowAssumptionPolicyEntity`) that are associated with the item model group.</span></span>
