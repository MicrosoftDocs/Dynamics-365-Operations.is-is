---
title: Setja upp flutningsskorður fyrir vöru
description: Þetta ferli setur upp flutningsstjórnunarskorðu til að koma í veg fyrir að valin vara sé flutt í gegnum valda stöð.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSConstraint, InventLocationIdLookup, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2ff8458a9821e1aa2ae8d2dc93cc89cfc318d70
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233560"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="bfc32-103">Setja upp flutningsskorður fyrir vöru</span><span class="sxs-lookup"><span data-stu-id="bfc32-103">Set up transportation constraints for an item</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bfc32-104">Þetta ferli setur upp flutningsstjórnunarskorðu til að koma í veg fyrir að valin vara sé flutt í gegnum valda stöð.</span><span class="sxs-lookup"><span data-stu-id="bfc32-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="bfc32-105">Þetta verk myndi venjulega vera framkvæmt af samræmingaraðila flutninga.</span><span class="sxs-lookup"><span data-stu-id="bfc32-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="bfc32-106">Hægt er að nota þetta ferli í sýnigögn fyrirtækisins USMF eða þín eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="bfc32-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="bfc32-107">Stofna vöruskorðu</span><span class="sxs-lookup"><span data-stu-id="bfc32-107">Create an item constaint</span></span>
1. <span data-ttu-id="bfc32-108">Fara í skorður.</span><span class="sxs-lookup"><span data-stu-id="bfc32-108">Go to Constraints.</span></span>
2. <span data-ttu-id="bfc32-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="bfc32-109">Click New.</span></span>
3. <span data-ttu-id="bfc32-110">Í reitinn vöruskorða skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="bfc32-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="bfc32-111">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="bfc32-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="bfc32-112">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="bfc32-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="bfc32-113">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="bfc32-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="bfc32-114">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="bfc32-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="bfc32-115">Sláið inn eða veldu gildi í reitnum stöð.</span><span class="sxs-lookup"><span data-stu-id="bfc32-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="bfc32-116">Í reitnum skorðuaðgerð skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="bfc32-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="bfc32-117">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="bfc32-117">Click Save.</span></span>
11. <span data-ttu-id="bfc32-118">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="bfc32-118">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]