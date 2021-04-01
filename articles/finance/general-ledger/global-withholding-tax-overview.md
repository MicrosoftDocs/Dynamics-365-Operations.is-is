---
title: Altækur staðgreiðsluskattur
description: Þetta efnisatriði veitir upplýsingar um virkni altæks staðgreiðsluskatts og hvernig á að setja hana upp. Virkni altæks staðgreiðsluskatts er bætt fyrir færslur lánardrottins og viðskiptavinar þannig að staðgreiðsluskattur er reiknaður á vörustigi.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 25fc503d6145872b8e9f28b8d9a4d7b9c1ba53a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249168"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="c3e50-104">Altækur staðgreiðsluskattur</span><span class="sxs-lookup"><span data-stu-id="c3e50-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3e50-105">Þetta efnisatriði veitir upplýsingar um virkni altæks staðgreiðsluskatts og útskýrir hvernig á að setja hana upp.</span><span class="sxs-lookup"><span data-stu-id="c3e50-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="c3e50-106">Nýja virknin er í boði í útgáfu 10.0.17 og nýrri.</span><span class="sxs-lookup"><span data-stu-id="c3e50-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="c3e50-107">Virkni altæks staðgreiðsluskatts er bætt fyrir færslur lánardrottins og viðskiptavinar þannig að staðgreiðsluskattur er reiknaður á vörustigi.</span><span class="sxs-lookup"><span data-stu-id="c3e50-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="c3e50-108">Staðan í staðgreiðsluskattslykli frá innkaupafærslum er hægt að jafna með því að keyra greiðsluvinnslu staðgreiðsluskatts á móti jöfnunarlykli staðgreiðsluskatts.</span><span class="sxs-lookup"><span data-stu-id="c3e50-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="c3e50-109">Altækur staðgreiðsluskattur styður ekki virknina **Vinna með gjöld** á síðum innkaupapöntunar, lánardrottnareikningis og sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="c3e50-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="c3e50-110">Kveikja á altækum staðgreiðsluskatti</span><span class="sxs-lookup"><span data-stu-id="c3e50-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="c3e50-111">Á vinnusvæðinu **Eiginleikastjórnun** skal velja **Altækur staðgreiðsluskattur** og síðan velja **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="c3e50-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="c3e50-112">Farið í **Skattur \> Uppsetning \> Færibreytur \> Færibreytur fjárhags** og síðan í flipanum **Staðgreiðsluskattur** skal stilla valkostinn **Virkja altækan staðgreiðsluskatt** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="c3e50-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="c3e50-113">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="c3e50-113">Select **Save**.</span></span>
4. <span data-ttu-id="c3e50-114">Uppfærið síðuna í vafranum.</span><span class="sxs-lookup"><span data-stu-id="c3e50-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="c3e50-115">Ekki er hægt að kveikja á virkni altæks staðgreiðsluskatts fyrir lönd/svæði þar sem staðbundnar lausnir staðgreiðsluskatts eru þegar til staðar.</span><span class="sxs-lookup"><span data-stu-id="c3e50-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="c3e50-116">Þessi lönd eru m.a. Indland, Brasilía, Taíland, Sádi-Arabía, Írland, Stóra-Bretland og Bandaríkin.</span><span class="sxs-lookup"><span data-stu-id="c3e50-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]