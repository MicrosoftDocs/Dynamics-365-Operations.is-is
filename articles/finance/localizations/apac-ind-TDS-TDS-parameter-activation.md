---
title: Stilla TDS færibreytur
description: Þetta efnisatriði útskýrir hvernig á að stilla færibreytur til að virkja virkni skattur sem dreginn er frá í uppruna (TDS) í tilgreindum færslum. Þetta er nauðsynlegt skref til að nota eiginleikann skattur sem dreginn er frá í uppruna, TDS.
author: kailiang
ms.date: 02/12/2021
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
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023326"
---
# <a name="set-the-tds-parameters"></a><span data-ttu-id="65a42-104">Stilla TDS færibreytur</span><span class="sxs-lookup"><span data-stu-id="65a42-104">Set the TDS parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65a42-105">Þetta efnisatriði útskýrir hvernig á að stilla færibreytur til að virkja virkni skattur sem dreginn er frá í uppruna (TDS) í tilgreindum færslum.</span><span class="sxs-lookup"><span data-stu-id="65a42-105">This topic explains how to set parameters to activate Tax Deducted at Source (TDS) functionality in specified transactions.</span></span> <span data-ttu-id="65a42-106">Þetta er nauðsynlegt skref til að nota eiginleikann skattur sem dreginn er frá í uppruna, TDS.</span><span class="sxs-lookup"><span data-stu-id="65a42-106">This is a necessary step to use the Tax Deducted at Source TDS feature.</span></span>

1. <span data-ttu-id="65a42-107">Farðu í **Fjárhag \> Fjárhagsuppsetning \> Fjárhagsfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="65a42-107">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="65a42-108">Á flipanum **Beinir skattar** í hlutanum **Skattur sem dreginn er frá í uppruna** skal stilla valkostinn **Virkja TDS** á **Já** til að virkja TDS virknina og síður og reiti sem eru notaðir fyrir það.</span><span class="sxs-lookup"><span data-stu-id="65a42-108">On the **Direct taxes** tab, in the **Tax Deducted at Source** section, set the **Activate TDS** option to **Yes** to activate the TDS functionality, and the pages and fields that are used for it.</span></span>
3. <span data-ttu-id="65a42-109">Stilltu valkostinn **Reikningur** á **Já** til að virkja reitina sem eru notaðir til að reikna út og draga TDS á reikningsstigi.</span><span class="sxs-lookup"><span data-stu-id="65a42-109">Set the **Invoice** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the invoice level.</span></span>
4. <span data-ttu-id="65a42-110">Veldu valkostinn **Greiðsla** á **Já** til að virkja reitina sem eru notaðir til að reikna út og draga TDS frá greiðslustiginu.</span><span class="sxs-lookup"><span data-stu-id="65a42-110">Set the **Payment** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the payment level.</span></span>

    <span data-ttu-id="65a42-111">[![Flipi beinna skatta](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span><span class="sxs-lookup"><span data-stu-id="65a42-111">[![Direct taxes tab](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span></span>

5. <span data-ttu-id="65a42-112">Á flipanum **Númeraraðir** finnur þú röðina þar sem reiturinn **Tilvísun** er stilltur á **Greiðsla staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="65a42-112">On the **Number sequences** tab, find the row where the **Reference** field is set to **Withholding tax payment**.</span></span> <span data-ttu-id="65a42-113">Í línunni **Kóði númeraraðar** fyrir línuna er kóði númeraraðarinnar valinn.</span><span class="sxs-lookup"><span data-stu-id="65a42-113">In the **Number sequence code** field for the row, select the number sequence code.</span></span> <span data-ttu-id="65a42-114">Kóði númeraraðar er notaður til að mynda númer fylgiskjals fyrir reglulegt TDS-uppgjörsferli.</span><span class="sxs-lookup"><span data-stu-id="65a42-114">The number sequence code is used to generate voucher numbers for the periodic TDS settlement process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="65a42-115">Til að keyra reglubundna TDC-jöfnun farið í **Skattur \> Skattskýrslur \> Staðgreiðsluskattur \> Greiðsla staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="65a42-115">To run the periodic TDS settlement process, go to **Tax \> Declarations \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="65a42-116">[![Flipinn Númeraraðir](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span><span class="sxs-lookup"><span data-stu-id="65a42-116">[![Number sequences tab](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span></span>

6. <span data-ttu-id="65a42-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="65a42-117">Close the page.</span></span>
