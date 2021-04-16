---
title: Altækur staðgreiðsluskattur
description: Þetta efnisatriði veitir upplýsingar um virkni altæks staðgreiðsluskatts og hvernig á að setja hana upp. Virkni altæks staðgreiðsluskatts er bætt fyrir færslur lánardrottins og viðskiptavinar þannig að staðgreiðsluskattur er reiknaður á vörustigi.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 9a73d34fb4fbf007cbb5a996cfa6e9719532869c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826667"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="33c94-104">Altækur staðgreiðsluskattur</span><span class="sxs-lookup"><span data-stu-id="33c94-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33c94-105">Þetta efnisatriði veitir upplýsingar um virkni altæks staðgreiðsluskatts og útskýrir hvernig á að setja hana upp.</span><span class="sxs-lookup"><span data-stu-id="33c94-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="33c94-106">Nýja virknin er í boði í útgáfu 10.0.17 og nýrri.</span><span class="sxs-lookup"><span data-stu-id="33c94-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="33c94-107">Virkni altæks staðgreiðsluskatts er bætt fyrir færslur lánardrottins og viðskiptavinar þannig að staðgreiðsluskattur er reiknaður á vörustigi.</span><span class="sxs-lookup"><span data-stu-id="33c94-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="33c94-108">Staðan í staðgreiðsluskattslykli frá innkaupafærslum er hægt að jafna með því að keyra greiðsluvinnslu staðgreiðsluskatts á móti jöfnunarlykli staðgreiðsluskatts.</span><span class="sxs-lookup"><span data-stu-id="33c94-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="33c94-109">Altækur staðgreiðsluskattur styður ekki virknina **Vinna með gjöld** á síðum innkaupapöntunar, lánardrottnareikningis og sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="33c94-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="33c94-110">Kveikja á altækum staðgreiðsluskatti</span><span class="sxs-lookup"><span data-stu-id="33c94-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="33c94-111">Á vinnusvæðinu **Eiginleikastjórnun** skal velja **Altækur staðgreiðsluskattur** og síðan velja **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="33c94-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="33c94-112">Farið í **Skattur \> Uppsetning \> Færibreytur \> Færibreytur fjárhags** og síðan í flipanum **Staðgreiðsluskattur** skal stilla valkostinn **Virkja altækan staðgreiðsluskatt** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="33c94-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="33c94-113">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="33c94-113">Select **Save**.</span></span>
4. <span data-ttu-id="33c94-114">Uppfærið síðuna í vafranum.</span><span class="sxs-lookup"><span data-stu-id="33c94-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="33c94-115">Ekki er hægt að kveikja á virkni altæks staðgreiðsluskatts fyrir lönd/svæði þar sem staðbundnar lausnir staðgreiðsluskatts eru þegar til staðar.</span><span class="sxs-lookup"><span data-stu-id="33c94-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="33c94-116">Þessi lönd eru m.a. Indland, Brasilía, Taíland, Sádi-Arabía, Írland, Stóra-Bretland og Bandaríkin.</span><span class="sxs-lookup"><span data-stu-id="33c94-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]