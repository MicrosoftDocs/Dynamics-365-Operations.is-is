---
title: Skilgreina afmarkaða tilfangaflokka framleiðslu
description: tilfangaflokk er safn rekstrartilföng sem samsvara yfirleitt efnislegt fyrirtæki vinnuflokkana, skilgreind eru með gulum línur í vinnslusal framleiðslu.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eaccb566c04d6d4b91ea8cb046931e750a4c6eed
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430037"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="6c08a-103">Skilgreina afmarkaða tilfangaflokka framleiðslu</span><span class="sxs-lookup"><span data-stu-id="6c08a-103">Define discrete manufacturing resource group</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6c08a-104">tilfangaflokk er safn rekstrartilföng sem samsvara yfirleitt efnislegt fyrirtæki vinnuflokkana, skilgreind eru með gulum línur í vinnslusal framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="6c08a-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="6c08a-105">Þessi verklýsing sýnir hvernig skilgreina skal tilfangaflokk til að nota í afmarkaða framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="6c08a-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="6c08a-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="6c08a-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="6c08a-107">Fara á tilfangaflokkur</span><span class="sxs-lookup"><span data-stu-id="6c08a-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="6c08a-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="6c08a-108">Click New.</span></span>
3. <span data-ttu-id="6c08a-109">Færa inn gildi í svæðið tilfangaflokkur.</span><span class="sxs-lookup"><span data-stu-id="6c08a-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="6c08a-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="6c08a-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6c08a-111">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="6c08a-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="6c08a-112">Færa inn eða veljið gildi í reitinn eining Framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="6c08a-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="6c08a-113">Skilgreina sjálfgefnar færibreytur aðgerðar</span><span class="sxs-lookup"><span data-stu-id="6c08a-113">Define default operational parameters</span></span>
1. <span data-ttu-id="6c08a-114">Stækka hlutann aðgerð.</span><span class="sxs-lookup"><span data-stu-id="6c08a-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="6c08a-115">Færið inn tölu í reitinn úrkastsprósenta.</span><span class="sxs-lookup"><span data-stu-id="6c08a-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="6c08a-116">Sláið inn eða veldu gildi í reitnum Setja upp flokkur.</span><span class="sxs-lookup"><span data-stu-id="6c08a-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="6c08a-117">Færa inn eða veljið gildi í reitinn flokkur keyrslutíma</span><span class="sxs-lookup"><span data-stu-id="6c08a-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="6c08a-118">Færið inn tölu í Aðgerðaröðun prósentusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="6c08a-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="6c08a-119">Skilgreina afgreiðslutíma</span><span class="sxs-lookup"><span data-stu-id="6c08a-119">Define operating hours</span></span>
1. <span data-ttu-id="6c08a-120">Stækka Dagatals hluta.</span><span class="sxs-lookup"><span data-stu-id="6c08a-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="6c08a-121">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="6c08a-121">Click Add.</span></span>
3. <span data-ttu-id="6c08a-122">Sláið inn eða veldu gildi í reitnum dagatal.</span><span class="sxs-lookup"><span data-stu-id="6c08a-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="6c08a-123">Bæta tilföngum aðgerða við</span><span class="sxs-lookup"><span data-stu-id="6c08a-123">Add operations resources</span></span>
1. <span data-ttu-id="6c08a-124">Stækka Tilföng hlutann.</span><span class="sxs-lookup"><span data-stu-id="6c08a-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="6c08a-125">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="6c08a-125">Click Add.</span></span>
3. <span data-ttu-id="6c08a-126">Sláið inn eða veldu gildi í reitnum tilföng.</span><span class="sxs-lookup"><span data-stu-id="6c08a-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="6c08a-127">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="6c08a-127">Click Add.</span></span>
5. <span data-ttu-id="6c08a-128">Sláið inn eða veldu gildi í reitnum tilföng.</span><span class="sxs-lookup"><span data-stu-id="6c08a-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="6c08a-129">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="6c08a-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="6c08a-130">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="6c08a-130">In the list, click the link in the selected row.</span></span>

