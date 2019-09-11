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
ms.openlocfilehash: 84ab803aedf5b803b6c5f39ff1907726335cb45d
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918327"
---
# <a name="item-where-used"></a><span data-ttu-id="141b0-103">Notkunarstaður vöru</span><span class="sxs-lookup"><span data-stu-id="141b0-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="141b0-104">Þú getur gert útreikning fyrir tiltekinn hlut til að fá yfirlit yfir hvar í eignastjórnun hluturinn hefur verið notaður.</span><span class="sxs-lookup"><span data-stu-id="141b0-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="141b0-105">Niðurstöðurnar sýna samhengið sem hluturinn hefur verið notaður á meðan á líftíma hans stóð.</span><span class="sxs-lookup"><span data-stu-id="141b0-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="141b0-106">Síðuna **Notkunarstaður vöru** er hægt að opna í aðalvalmyndinni fyrir eignastjórnun og einnig er hægt að nálgast hana af eftirfarandi síðum:</span><span class="sxs-lookup"><span data-stu-id="141b0-106">The **Item where used** page can be opened from the main Asset management menu, and it can also be accessed from the following pages:</span></span>

[<span data-ttu-id="141b0-107">Uppskrift eignar</span><span class="sxs-lookup"><span data-stu-id="141b0-107">Asset BOM</span></span>](../objects/object-BOM.md)

[<span data-ttu-id="141b0-108">Varahlutir í sjálfgefinni tegund eigna</span><span class="sxs-lookup"><span data-stu-id="141b0-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md)

[<span data-ttu-id="141b0-109">Vöruspá í sjálfgefinni spá um gerð viðhaldsstarfa</span><span class="sxs-lookup"><span data-stu-id="141b0-109">Item forecast on Maintenance job type defaults forecast</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

[<span data-ttu-id="141b0-110">Viðhaldsspá verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="141b0-110">Work order maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

[<span data-ttu-id="141b0-111">Innkaupabeiðni verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="141b0-111">Work order purchase requisition</span></span>](../work-orders/procurement.md)

[<span data-ttu-id="141b0-112">Innkaup verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="141b0-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="141b0-113">Gerðu útreikning notkunarstað vöru</span><span class="sxs-lookup"><span data-stu-id="141b0-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="141b0-114">Smelltu á **Eignastjórnun** > **Fyrirspurnir** > **Notkunarstaður vöru** eða veldu hnappinn **Notkunarstaður vöru** á einni af síðunum sem nefndar eru hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="141b0-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="141b0-115">Í glugganum **Notkunarstaður vöru** skaltu velja hlutinn sem þú vilt gera útreikning fyrir í reitnum **Vörunúmer**.</span><span class="sxs-lookup"><span data-stu-id="141b0-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="141b0-116">Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að vörulínur séu varðandi virkar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="141b0-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> <span data-ttu-id="141b0-117">Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa virkt staðsetningarskipulag, verða allar vörulínur fyrir virka staðsetningu sýndar á efsta þrepi.</span><span class="sxs-lookup"><span data-stu-id="141b0-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="141b0-118">Þess vegna er hægt að bæta tengslum/magni á línu frá virkum staðsetningum sem eru staðsettar á lægra stigi.</span><span class="sxs-lookup"><span data-stu-id="141b0-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="141b0-119">Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar vörulínur á öllum virkum staðsetningarstigum sem þær tengjast.</span><span class="sxs-lookup"><span data-stu-id="141b0-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="141b0-120">Í hlutanum **Hafa með** velurðu „Já“ á skiptihnöppunum sem þú vilt hafa með í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="141b0-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="141b0-121">Smellið á **Í lagi** til að byrja að reikna.</span><span class="sxs-lookup"><span data-stu-id="141b0-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="141b0-122">Á flipanum **Notkunarstaður vöru** > aðgerðarrúðahópunum **Flokka eftir...** velurðu viðeigandi hnappa til að sýna nauðsynleg smáatriði við útreikninginn.</span><span class="sxs-lookup"><span data-stu-id="141b0-122">On the **Item where used** tab > **Group by...** action pane groups, select the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="141b0-123">Valdir aðgerðarrúðahnappar eru auðkenndir.</span><span class="sxs-lookup"><span data-stu-id="141b0-123">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="141b0-124">Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.</span><span class="sxs-lookup"><span data-stu-id="141b0-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="141b0-125">Ef þú vilt sýna mál sem tengjast vörunni skaltu smella á **Sýna víddir** og velja víddirnar sem á að sýna.</span><span class="sxs-lookup"><span data-stu-id="141b0-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

<span data-ttu-id="141b0-126">Á myndinni hér að neðan sérðu dæmi um útreikning á vöru þar sem notaður er vörunúmerið "1000".</span><span class="sxs-lookup"><span data-stu-id="141b0-126">In the figure below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![Mynd 1](media/12-controlling-and-reporting.png)

