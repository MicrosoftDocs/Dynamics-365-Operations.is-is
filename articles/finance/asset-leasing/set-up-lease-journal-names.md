---
title: Sett upp leigubókanöfn
description: Þetta efnisatriði útskýrir hvernig á að skilgreina heiti leigubóka. Heiti leigubóka tilgreina færslubækur sem færslur sem eru með eignaleigu eru bókaðar í.
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
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 89c5fc768aafe9e5de9adcde32e7b4d0a084941b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990918"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="be258-104">Sett upp leigubókanöfn</span><span class="sxs-lookup"><span data-stu-id="be258-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be258-105">Heiti leigubóka tilgreina færslubækur sem Færslur Eignarleigu eru bókaðar í.</span><span class="sxs-lookup"><span data-stu-id="be258-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="be258-106">Aðeins færslubókarnöfn sem er úthlutað á færslubókargerðina **Eignarleiga** birtast í **Upphafleg skráning** og **Heiti mánaðarlegrar færslubókar** reitir á síðunni **Færibreytur eignarleigu**.</span><span class="sxs-lookup"><span data-stu-id="be258-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="be258-107">Aðeins er hægt að úthluta færslubókargerðinni **skráning á reikningi lánardrottins** í reitinn **Heiti reikningabókar**.</span><span class="sxs-lookup"><span data-stu-id="be258-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="be258-108">Til að skilgreina heiti leigubóka skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="be258-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="be258-109">Opnið **Eignarleiga \> Uppsetning \> Færibreytur fyrir eignarleigu**.</span><span class="sxs-lookup"><span data-stu-id="be258-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="be258-110">Á flipanum **Almennt** í reitnum **Færslubókarheiti upphaflegrar skráningar** skal velja færslubók.</span><span class="sxs-lookup"><span data-stu-id="be258-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="be258-111">Allar upphaflegar færslubókarskráningar verða bókaðar á þetta færslubókarheiti.</span><span class="sxs-lookup"><span data-stu-id="be258-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="be258-112">Velja færslubók í svæðinu **Heiti reikningabókar**.</span><span class="sxs-lookup"><span data-stu-id="be258-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="be258-113">Ef valkosturinn **Greiða lánardrottni** er stilltur á **Já** fyrir leigubókina verða reikningar leigu og kostnaðar bókaðir á þetta færslubókarheiti.</span><span class="sxs-lookup"><span data-stu-id="be258-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="be258-114">Velja færslubók í svæðinu **Heiti leigubókar**.</span><span class="sxs-lookup"><span data-stu-id="be258-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="be258-115">Allar afskriftir, vextir og endurflokkunarfærslur fyrir skammtíma verða bókaðar á þetta færslubókarheiti.</span><span class="sxs-lookup"><span data-stu-id="be258-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="be258-116">Ef valkosturinn **Greiða lánardrottni** er stilltur á **Nei** fyrir leigubókina verða leigugreiðslur og kostnaðarfærslur einnig bókaðar á þetta færslubókarheiti.</span><span class="sxs-lookup"><span data-stu-id="be258-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>
