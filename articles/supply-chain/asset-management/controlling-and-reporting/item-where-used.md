---
title: Notkunarstaður vöru
description: Þetta efni útskýrir hvernig á að fá yfirlit yfir hvar hlutur er notaður í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 476b01a4bae34a271203f34481ff18042783d4df
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811264"
---
# <a name="item-where-used"></a><span data-ttu-id="6a62f-103">Notkunarstaður vöru</span><span class="sxs-lookup"><span data-stu-id="6a62f-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6a62f-104">Þú getur gert útreikning fyrir tiltekinn hlut til að fá yfirlit yfir hvar í eignastjórnun hluturinn hefur verið notaður.</span><span class="sxs-lookup"><span data-stu-id="6a62f-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="6a62f-105">Niðurstöðurnar sýna samhengið sem hluturinn hefur verið notaður á meðan á líftíma hans stóð.</span><span class="sxs-lookup"><span data-stu-id="6a62f-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="6a62f-106">Síðuna **Notkunarstaður vöru** er hægt að opna í aðalvalmyndinni fyrir eignastjórnun og einnig er hægt að nálgast hana af eftirfarandi síðum:</span><span class="sxs-lookup"><span data-stu-id="6a62f-106">The **Item where used** page can be opened from the main Asset Management menu, and it can also be accessed from the following pages:</span></span>

- [<span data-ttu-id="6a62f-107">Eignauppskriftir</span><span class="sxs-lookup"><span data-stu-id="6a62f-107">Asset BOMs</span></span>](../objects/object-BOM.md)

- [<span data-ttu-id="6a62f-108">Varahlutir í sjálfgefinni tegund eigna</span><span class="sxs-lookup"><span data-stu-id="6a62f-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [<span data-ttu-id="6a62f-109">Flokkar viðhaldsverkgerðar og viðhaldsverkgerðir, afbrigði viðhaldsverkgerðar, viðskipti viðhaldsvinnslu og viðhaldsgátlistar</span><span class="sxs-lookup"><span data-stu-id="6a62f-109">Maintenance job type categories and maintenance job types, maintenance job type variants, maintenance job trades, and maintenance checklists</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [<span data-ttu-id="6a62f-110">Viðhaldsspá</span><span class="sxs-lookup"><span data-stu-id="6a62f-110">Maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

- [<span data-ttu-id="6a62f-111">Innkaup</span><span class="sxs-lookup"><span data-stu-id="6a62f-111">Procurement</span></span>](../work-orders/procurement.md)

- [<span data-ttu-id="6a62f-112">Innkaup verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="6a62f-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="6a62f-113">Gerðu útreikning notkunarstað vöru</span><span class="sxs-lookup"><span data-stu-id="6a62f-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="6a62f-114">Smelltu á **Eignastjórnun** > **Fyrirspurnir** > **Notkunarstaður vöru** eða veldu hnappinn **Notkunarstaður vöru** á einni af síðunum sem nefndar eru hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="6a62f-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="6a62f-115">Í glugganum **Notkunarstaður vöru** skaltu velja hlutinn sem þú vilt gera útreikning fyrir í reitnum **Vörunúmer**.</span><span class="sxs-lookup"><span data-stu-id="6a62f-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="6a62f-116">Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að vörulínur séu varðandi virkar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="6a62f-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="6a62f-117">Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa virkt staðsetningarskipulag, verða allar vörulínur fyrir virka staðsetningu sýndar á efsta þrepi.</span><span class="sxs-lookup"><span data-stu-id="6a62f-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="6a62f-118">Þess vegna er hægt að bæta tengslum/magni á línu frá virkum staðsetningum sem eru staðsettar á lægra stigi.</span><span class="sxs-lookup"><span data-stu-id="6a62f-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="6a62f-119">Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar vörulínur á öllum virkum staðsetningarstigum sem þær tengjast.</span><span class="sxs-lookup"><span data-stu-id="6a62f-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="6a62f-120">Í hlutanum **Hafa með** velurðu „Já“ á skiptihnöppunum sem þú vilt hafa með í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="6a62f-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="6a62f-121">Smellið á **Í lagi** til að byrja að reikna.</span><span class="sxs-lookup"><span data-stu-id="6a62f-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="6a62f-122">Á flipanum **Notkunarstaður vöru** velurðu hnappana **Flokka eftir** til að sýna nauðsynleg smáatriði við útreikninginn.</span><span class="sxs-lookup"><span data-stu-id="6a62f-122">On the **Item where used** tab, select the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="6a62f-123">Valdir hnappar **Flokka eftir** eru auðkenndir.</span><span class="sxs-lookup"><span data-stu-id="6a62f-123">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="6a62f-124">Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.</span><span class="sxs-lookup"><span data-stu-id="6a62f-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="6a62f-125">Ef þú vilt sýna mál sem tengjast vörunni skaltu smella á **Sýna víddir** og velja víddirnar sem á að sýna.</span><span class="sxs-lookup"><span data-stu-id="6a62f-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

## <a name="example"></a><span data-ttu-id="6a62f-126">Dæmi</span><span class="sxs-lookup"><span data-stu-id="6a62f-126">Example</span></span>

<span data-ttu-id="6a62f-127">Á skjámyndinni hér að neðan sérðu dæmi um útreikning á vöru þar sem notað er vörunúmerið "1000".</span><span class="sxs-lookup"><span data-stu-id="6a62f-127">In the screenshot below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![Dæmi um útreikning á notkunarstað vöru](media/12-controlling-and-reporting.png)

