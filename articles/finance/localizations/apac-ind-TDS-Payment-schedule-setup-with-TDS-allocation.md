---
title: Setja upp greiðsluáætlanir með TDS-úthlutun
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp greiðsluáætlanir fyrir skattaúthlutanir sem er dreginn frá upprunalegri greiðslu (TDS).
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
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023336"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a><span data-ttu-id="916b7-103">Setja upp greiðsluáætlanir með TDS-úthlutun</span><span class="sxs-lookup"><span data-stu-id="916b7-103">Set up payment schedules with TDS allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="916b7-104">Í þessu efnisatriði er útskýrt hvernig á að setja upp greiðsluáætlanir fyrir skattaúthlutanir sem er dreginn frá upprunalegri greiðslu (TDS).</span><span class="sxs-lookup"><span data-stu-id="916b7-104">This topic explains how to set up payment schedules with Tax Deducted at Source (TDS) allocation.</span></span>

1. <span data-ttu-id="916b7-105">Farið í **Viðskiptaskuldir \> Greiðsluuppsetning \> Greiðsluáætlanir**.</span><span class="sxs-lookup"><span data-stu-id="916b7-105">Go to **Accounts payable \> Payment setup \> Payment schedules**.</span></span>

    <span data-ttu-id="916b7-106">[![Síða greiðsluáætlunar](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span><span class="sxs-lookup"><span data-stu-id="916b7-106">[![Payment schedules page](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span></span>

2. <span data-ttu-id="916b7-107">Á aðgerðasvæðinu skal velja **Nýr** til að búa til greiðsluáætlun og færa inn nauðsynlegar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="916b7-107">On the Action Pane, select **New** to create a payment schedule, and enter the required details.</span></span>
3. <span data-ttu-id="916b7-108">Í svæðinu **Úthlutun** skal velja aðferðina sem á að nota til að úthluta greiðslunni fyrir greiðsluáætlunina:</span><span class="sxs-lookup"><span data-stu-id="916b7-108">In the **Allocation** field, select the method to use to allocate the payment for the payment schedule:</span></span>

    - <span data-ttu-id="916b7-109">Alls</span><span class="sxs-lookup"><span data-stu-id="916b7-109">Total</span></span>
    - <span data-ttu-id="916b7-110">Föst upphæð</span><span class="sxs-lookup"><span data-stu-id="916b7-110">Fixed amount</span></span>
    - <span data-ttu-id="916b7-111">Fast magn</span><span class="sxs-lookup"><span data-stu-id="916b7-111">Fixed quantity</span></span>
    - <span data-ttu-id="916b7-112">Tilgreint</span><span class="sxs-lookup"><span data-stu-id="916b7-112">Specified</span></span>

    <span data-ttu-id="916b7-113">Reiturinn **Úthlutun staðgreiðsluskatts** sýnir TDS-úthlutunaraðferðina fyrir greiðsluáætlunina.</span><span class="sxs-lookup"><span data-stu-id="916b7-113">The **Withholding tax allocation** field shows the TDS allocation method for the payment schedule.</span></span> <span data-ttu-id="916b7-114">Ef þú velur **Alls** í reitnum **Úthlutun** er reiturinn **Úthlutun staðgreiðsluskatts** sjálfkrafa stilltur á **Alls**.</span><span class="sxs-lookup"><span data-stu-id="916b7-114">If you select **Total** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Total**.</span></span> <span data-ttu-id="916b7-115">Ef þú velur **Föst upphæð**, **Fast magn** eða **Tilgreint** í reitnum **Úthlutun** er reiturinn **Úthlutun staðgreiðsluskatts** sjálfkrafa stilltur á **Hlutfallslega**.</span><span class="sxs-lookup"><span data-stu-id="916b7-115">If you select **Fixed amount**, **Fixed quantity**, or **Specified** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Proportionally**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="916b7-116">Ef svæðið **Úthlutun staðgreiðsluskatts** er stillt á **Samtals** eru afborganirnar reiknaðar á grundvelli brúttóupphæðarinnar, sem inniheldur TDS-upphæðina.</span><span class="sxs-lookup"><span data-stu-id="916b7-116">If the **Withholding tax allocation** field is set to **Total**, the payment installments are calculated based on the gross amount, which includes the TDS amount.</span></span> <span data-ttu-id="916b7-117">Ef svæðið **Úthlutun staðgreiðsluskatts** er stillt á **Hlutfallslega** eru afborganirnar reiknaðar á grundvelli nettó reikningsupphæðar eftir að TDS-upphæðin er dregin frá.</span><span class="sxs-lookup"><span data-stu-id="916b7-117">If the **Withholding tax allocation** field is set to **Proportionally**, the payment installments are calculated based on the net invoice amount after the TDS amount is deducted.</span></span>

4. <span data-ttu-id="916b7-118">Færið inn aðrar áskildar upplýsingar og lokið svo síðunni.</span><span class="sxs-lookup"><span data-stu-id="916b7-118">Enter the other required details, and then close the page.</span></span>
