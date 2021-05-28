---
title: Uppfæra númer og dagsetningar vottorða fyrir TDS-færslur
description: Í þessu efnisatriði er útskýrt hvernig á að uppfæra endurheimtanleg vottorðanúmer og dagsetningar sem voru skráðar fyrir lánardrottin, viðskiptavin og fjárhagslykil fyrir skatt sem dreginn er frá í upphafi (TDS).
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
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023324"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a><span data-ttu-id="52949-103">Uppfæra númer og dagsetningar vottorða fyrir TDS-færslur</span><span class="sxs-lookup"><span data-stu-id="52949-103">Update certificate numbers and dates for TDS transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52949-104">Í þessu efnisatriði er útskýrt hvernig á að uppfæra endurheimtanleg vottorðanúmer og dagsetningar sem voru skráðar fyrir lánardrottin, viðskiptavin og fjárhagslykil fyrir skatt sem dreginn er frá í upphafi (TDS).</span><span class="sxs-lookup"><span data-stu-id="52949-104">This topic explains how to update the recoverable certificate numbers and dates that were recorded for vendor, customer, and ledger accounts for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="52949-105">Hægt er að skoða vottorðin fyrir TDS-færslur á síðunni **Endurheimtanleg vottorð**.</span><span class="sxs-lookup"><span data-stu-id="52949-105">You can view the certificates for TDS transactions on the **Recoverable certificates** page.</span></span> <span data-ttu-id="52949-106">Hægt er að uppfæra vottorðin með því að nota síðuna **Uppfæra vottorð**.</span><span class="sxs-lookup"><span data-stu-id="52949-106">You can update the certificates by using the **Update Certificates** page.</span></span>

<span data-ttu-id="52949-107">Fylgið þessum skrefum til að uppfæra vottorðanúmerin og dagsetningarnar fyrir TDS-færslur.</span><span class="sxs-lookup"><span data-stu-id="52949-107">Follow these steps to update certificate numbers and dates for TDS transactions.</span></span>

1. <span data-ttu-id="52949-108">Farið í **Skattur \> Skattskýrslur \> Staðgreiðsluskattur \> Uppfæra vottorð**.</span><span class="sxs-lookup"><span data-stu-id="52949-108">Go to **Tax \> Declarations \> Withholding tax \> Update certificate**.</span></span>

    <span data-ttu-id="52949-109">[![Síða vottorðauppfærslu](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span><span class="sxs-lookup"><span data-stu-id="52949-109">[![Update certificate page](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span></span>

2. <span data-ttu-id="52949-110">Á síðunni **Uppfæra vottorð**, í hlutanum **Velja**, í reitnum **Skattgerð**, skal velja **TDS**.</span><span class="sxs-lookup"><span data-stu-id="52949-110">On the **Update certificate** page, in the **Select** section, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="52949-111">Í reitnum **Vottorðanúmer** skal velja TDS-vottorðanúmer viðskiptavinar eða lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="52949-111">In the **Certificate number** field, select the customer's or vendor's TDS certificate number.</span></span>

    > [!NOTE]
    > <span data-ttu-id="52949-112">Reiturinn **Númer vottorðs** sýnir aðeins TDS-vottorðanúmer sem gátreiturinn **Lokað** er hreinsaður fyrir á síðunni **Endurheimtanleg vottorð**.</span><span class="sxs-lookup"><span data-stu-id="52949-112">The **Certificate number** field lists only TDS certificate numbers that the **Closed** check box is cleared for on the **Recoverable certificates** page.</span></span>

    <span data-ttu-id="52949-113">Reiturinn **Dagsetning vottorðs** sýnir dagsetningu vottorðsins.</span><span class="sxs-lookup"><span data-stu-id="52949-113">The **Certificate date** field shows the certificate date.</span></span> <span data-ttu-id="52949-114">Reiturinn **Gerð lykils** sýnir gerð lykilsins sem TDS-vottorðanúmerið er móttekið fyrir and reiturinn **Heiti** sýnir heiti lykilsins.</span><span class="sxs-lookup"><span data-stu-id="52949-114">The **Account type** field shows the type of account that the TDS certificate number is received for, and the **Name** field shows the name of the account.</span></span>

5. <span data-ttu-id="52949-115">Í reitunum **Frá dagsetningu** og **Til dagsetningar** skal velja upphafs- og lokadagsetningar tímabilsins til að sýna TDS-færslur fyrir.</span><span class="sxs-lookup"><span data-stu-id="52949-115">In the **From date** and **To date** fields, select the start and end dates of the period to show the TDS transactions for.</span></span>
6. <span data-ttu-id="52949-116">Veljið **Sýna gögn** til að skoða TDS-færslur sem voru bókaðar á völdu tímabili.</span><span class="sxs-lookup"><span data-stu-id="52949-116">Select **Show data** to view the TDS transactions that were posted during the selected period.</span></span>

    <span data-ttu-id="52949-117">Í flipanum **Yfirlit** sýnir hnitanetið í efri rúðunni eftirfarandi upplýsingar um hverja TDS-færslu sem var bókuð fyrir lánardrottin eða viðskiptavin á völdu tímabili:</span><span class="sxs-lookup"><span data-stu-id="52949-117">On the **Overview** tab, the grid in the upper pane shows the following information about each TDS transaction that was posted for the vendor or customer during the selected period:</span></span>

    - <span data-ttu-id="52949-118">**Fylgiskjal** – Fylgiskjalsnúmer TDS-færslunnar.</span><span class="sxs-lookup"><span data-stu-id="52949-118">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="52949-119">**Dagsetning** – Dagsetning TDS-færslunnar.</span><span class="sxs-lookup"><span data-stu-id="52949-119">**Date** – The date of the TDS transaction.</span></span>
    - <span data-ttu-id="52949-120">**Upphæð** – Upphæð reiknings sem TDS var reiknað fyrir.</span><span class="sxs-lookup"><span data-stu-id="52949-120">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="52949-121">**Skattupphæð** – TDS-skattupphæð sem reiknuð var fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="52949-121">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>

7. <span data-ttu-id="52949-122">Til að færa tilteknar TDS-færslur úr efra hnitanetinu og yfir í neðra hnitanetið skal velja færslurnar og síðan velja **Hafa með**.</span><span class="sxs-lookup"><span data-stu-id="52949-122">To move specific TDS transactions from the upper grid to the lower grid, select the transactions, and then select **Include**.</span></span> <span data-ttu-id="52949-123">Að öðrum kosti skal velja **Taka allt með** til að færa allar TDS-færslur úr efra hnitanetinu og yfir í neðra hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="52949-123">Alternatively, select **Include all** to move all TDS transactions from the upper grid to the lower grid.</span></span>

    <span data-ttu-id="52949-124">Til að færa tilteknar TDS-færslur eða allar TDS-færslur úr neðra hnitanetinu og yfir í efra hnitanetið skal nota hnappinn **Útiloka** eða **Útiloka allt**.</span><span class="sxs-lookup"><span data-stu-id="52949-124">To move specific TDS transactions or all TDS transactions from the lower grid to the upper grid, use the **Exclude** or **Exclude all** button.</span></span>

8. <span data-ttu-id="52949-125">Veljið **Uppfæra** til að uppfæra reitina **Númer vottorðs** og **Dagsetning vottorðs** fyrir TDS-færslur í neðra hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="52949-125">Select **Update** to update the **Certificate number** and **Certificate date** fields for TDS transactions in the lower grid.</span></span>
10. <span data-ttu-id="52949-126">Farið í **Skattur \> Óbeinir skattar \> Staðgreiðsluskattur \> Endurheimtanlegt vottorð** og veljið **Fyrirspurn** til að skoða uppfærðar færslulínur sem eru með nýju vottorðanúmerin á síðunni **Vottorðafærslur**.</span><span class="sxs-lookup"><span data-stu-id="52949-126">Go to **Tax \> Indirect taxes \> Withholding tax \> Recoverable certificate**, and select **Inquiry** to view the updated transaction lines that have the new certificate numbers on the **Certificate transactions** page.</span></span>

    <span data-ttu-id="52949-127">[![Færslusíða vottorðs](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span><span class="sxs-lookup"><span data-stu-id="52949-127">[![Certificate transactions page](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span></span>
