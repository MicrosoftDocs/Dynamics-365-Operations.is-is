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
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1930999604fb2605a88bad9a5972afd3579976a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975111"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="135e9-103">Skilgreina afmarkaða tilfangaflokka framleiðslu</span><span class="sxs-lookup"><span data-stu-id="135e9-103">Define discrete manufacturing resource group</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="135e9-104">tilfangaflokk er safn rekstrartilföng sem samsvara yfirleitt efnislegt fyrirtæki vinnuflokkana, skilgreind eru með gulum línur í vinnslusal framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="135e9-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="135e9-105">Þessi verklýsing sýnir hvernig skilgreina skal tilfangaflokk til að nota í afmarkaða framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="135e9-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="135e9-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="135e9-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="135e9-107">Fara á tilfangaflokkur</span><span class="sxs-lookup"><span data-stu-id="135e9-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="135e9-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="135e9-108">Click New.</span></span>
3. <span data-ttu-id="135e9-109">Færa inn gildi í svæðið tilfangaflokkur.</span><span class="sxs-lookup"><span data-stu-id="135e9-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="135e9-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="135e9-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="135e9-111">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="135e9-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="135e9-112">Færa inn eða veljið gildi í reitinn eining Framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="135e9-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="135e9-113">Skilgreina sjálfgefnar færibreytur aðgerðar</span><span class="sxs-lookup"><span data-stu-id="135e9-113">Define default operational parameters</span></span>
1. <span data-ttu-id="135e9-114">Stækka hlutann aðgerð.</span><span class="sxs-lookup"><span data-stu-id="135e9-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="135e9-115">Færið inn tölu í reitinn úrkastsprósenta.</span><span class="sxs-lookup"><span data-stu-id="135e9-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="135e9-116">Sláið inn eða veldu gildi í reitnum Setja upp flokkur.</span><span class="sxs-lookup"><span data-stu-id="135e9-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="135e9-117">Færa inn eða veljið gildi í reitinn flokkur keyrslutíma</span><span class="sxs-lookup"><span data-stu-id="135e9-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="135e9-118">Færið inn tölu í Aðgerðaröðun prósentusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="135e9-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="135e9-119">Skilgreina afgreiðslutíma</span><span class="sxs-lookup"><span data-stu-id="135e9-119">Define operating hours</span></span>
1. <span data-ttu-id="135e9-120">Stækka Dagatals hluta.</span><span class="sxs-lookup"><span data-stu-id="135e9-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="135e9-121">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="135e9-121">Click Add.</span></span>
3. <span data-ttu-id="135e9-122">Sláið inn eða veldu gildi í reitnum dagatal.</span><span class="sxs-lookup"><span data-stu-id="135e9-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="135e9-123">Bæta tilföngum aðgerða við</span><span class="sxs-lookup"><span data-stu-id="135e9-123">Add operations resources</span></span>
1. <span data-ttu-id="135e9-124">Stækka Tilföng hlutann.</span><span class="sxs-lookup"><span data-stu-id="135e9-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="135e9-125">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="135e9-125">Click Add.</span></span>
3. <span data-ttu-id="135e9-126">Sláið inn eða veldu gildi í reitnum tilföng.</span><span class="sxs-lookup"><span data-stu-id="135e9-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="135e9-127">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="135e9-127">Click Add.</span></span>
5. <span data-ttu-id="135e9-128">Sláið inn eða veldu gildi í reitnum tilföng.</span><span class="sxs-lookup"><span data-stu-id="135e9-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="135e9-129">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="135e9-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="135e9-130">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="135e9-130">In the list, click the link in the selected row.</span></span>

