---
title: Skrá endurheimtanlegt vottorðanúmer TDS
description: Í þessu efnisatriði er útskýrt hvernig á að nota síðu endurheimtanlegs vottorðs til að skrá vottorðanúmerin og dagsetningarnar fyrir TDS-vottorð sem eru móttekin fyrir tiltekinn lánardrottin, viðskiptavin eða fjárhag.
author: kailiang
mms.date: 02/12/2021
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
ms.openlocfilehash: b501c331cccc6d030f36d0a13ba0a6a13c08c733
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023314"
---
# <a name="record-tds-recoverable-certificate-numbers"></a><span data-ttu-id="7e49f-103">Skrá endurheimtanlegt vottorðanúmer TDS</span><span class="sxs-lookup"><span data-stu-id="7e49f-103">Record TDS recoverable certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e49f-104">Í þessu efnisatriði er útskýrt hvernig á að nota síðuna **Endurheimtanleg vottorð** til að skrá vottorðanúmerin og dagsetningarnar fyrir TDS-vottorð sem eru móttekin fyrir tiltekinn lánardrottin, viðskiptavin eða fjárhag.</span><span class="sxs-lookup"><span data-stu-id="7e49f-104">This topic explains how to use the **Recoverable certificates** page to record the certificate numbers and dates for Tax Deducted at Source (TDS) certificates that are received for a specific vendor, customer, or ledger.</span></span> <span data-ttu-id="7e49f-105">Til að uppfæra vottorðanúmer og dagsetningar TDS sem er skráð fyrir TDS-færslur á þessari síðu skal nota síðuna **Uppfæra vottorð** (**Fjárhagur \> Reglubundið \> Staðgreiðsluskattur \> Uppfæra vottorð**).</span><span class="sxs-lookup"><span data-stu-id="7e49f-105">To update the TDS certificate numbers and dates that are recorded for TDS transactions on this page, use the **Update certificate** page (**General ledger \> Periodic \> Withholding tax \> Update certificate**).</span></span> <span data-ttu-id="7e49f-106">Þegar búið er að uppfæra númer TDS-vottorða skal loka þeim.</span><span class="sxs-lookup"><span data-stu-id="7e49f-106">After you've finished updating TDS certificate numbers, close them.</span></span>

<span data-ttu-id="7e49f-107">Fylgið þessum skrefum til að skrá númer og dagsetningar TDS-vottorða.</span><span class="sxs-lookup"><span data-stu-id="7e49f-107">Follow these steps to record the TDS certificate numbers and dates.</span></span>

1. <span data-ttu-id="7e49f-108">Opnið **Skattur \> Óbeinn skattur \> Staðgreiðsluskattur \> Endurheimtanleg vottorð**.</span><span class="sxs-lookup"><span data-stu-id="7e49f-108">Go to **Tax \> Indirect tax \> Withholding tax \> Recoverable certificates**.</span></span>

    <span data-ttu-id="7e49f-109">[![Síða endurheimtanlegra vottorða](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span><span class="sxs-lookup"><span data-stu-id="7e49f-109">[![Recoverable certificates page](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span></span> 

2. <span data-ttu-id="7e49f-110">Á síðunni **Endurheimtanleg vottorð**, í reitnum **Skattgerð**, skal velja **TDS**.</span><span class="sxs-lookup"><span data-stu-id="7e49f-110">On the **Recoverable certificates** page, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="7e49f-111">Veljið **Ný** til að stofna nýja skrá.</span><span class="sxs-lookup"><span data-stu-id="7e49f-111">Select **New** to create a record.</span></span>
4. <span data-ttu-id="7e49f-112">Í reitnum **Númer vottorðs** skal færa inn númer TDS-vottorðs.</span><span class="sxs-lookup"><span data-stu-id="7e49f-112">In the **Certificate number** field, enter the TDS certificate number.</span></span>
5. <span data-ttu-id="7e49f-113">Í reitnum **Lykilgerð** skal velja gerð lykils sem TDS-vottorð er móttekið fyrir: **Lánardrottinn**, **Viðskiptavinur** eða **Fjárhagur**.</span><span class="sxs-lookup"><span data-stu-id="7e49f-113">In the **Account type** field, select the type of account that the TDS certificate is received for: **Vendor**, **Customer**, or **Ledger**.</span></span>
6. <span data-ttu-id="7e49f-114">Í reitnum **Lykill** skal velja númer lánardrottna-, viðskiptavina- eða fjárhagslykils eftir því hvaða gerð lykils er valin.</span><span class="sxs-lookup"><span data-stu-id="7e49f-114">In the **Account** field, select the vendor, customer, or ledger account number, depending on the account type that you selected.</span></span> <span data-ttu-id="7e49f-115">Reiturinn **Heiti** sýnir heiti lánardrottna-, viðskiptavina- eða fjárhagslykils.</span><span class="sxs-lookup"><span data-stu-id="7e49f-115">The **Name** field shows the name of the vendor, customer, or ledger account.</span></span>
7. <span data-ttu-id="7e49f-116">Í reitinn **Upphæð vottorðs** skal færa inn upphæð TDS-vottorðs.</span><span class="sxs-lookup"><span data-stu-id="7e49f-116">In the **Certificate amount** field, enter the amount of the TDS certificate.</span></span>
8. <span data-ttu-id="7e49f-117">Í reitinn **Dagsetning** skal færa inn dagsetningu vottorðs fyrir númer vottorðs.</span><span class="sxs-lookup"><span data-stu-id="7e49f-117">In the **Date** field, enter the certificate date for the certificate number.</span></span>
9. <span data-ttu-id="7e49f-118">Veljið **Fyrirspurnir** til að opna síðuna **Færslur vottorðs** þar sem hægt er að skoða TDS-færslurnar sem númer og dagsetning TDS-vottorðs eru uppfærð fyrir.</span><span class="sxs-lookup"><span data-stu-id="7e49f-118">Select **Inquiries** to open the **Certificate transactions** page, where you can view the TDS transactions that the TDS certificate number and date are updated for.</span></span> <span data-ttu-id="7e49f-119">Þessar upplýsingar er hægt að uppfæra á síðunni **Uppfæra vottorð** (**Skattur \> Skattskýrslur \> Staðgreiðsluskattur \> Uppfæra vottorð**).</span><span class="sxs-lookup"><span data-stu-id="7e49f-119">This information can be updated on the **Update certificate** page (**Tax \> Declarations \> Withholding tax \> Update certificate**).</span></span>

    <span data-ttu-id="7e49f-120">Síðan **Uppfæra vottorð** sýnir eftirfarandi upplýsingar fyrir hverja TDS-færslu:</span><span class="sxs-lookup"><span data-stu-id="7e49f-120">The **Update certificate** page shows the following information for each TDS transaction:</span></span>

    - <span data-ttu-id="7e49f-121">**Dagsetning** – Bókunardagsetning TDS-færslunnar.</span><span class="sxs-lookup"><span data-stu-id="7e49f-121">**Date** – The posting date of the TDS transaction.</span></span>
    - <span data-ttu-id="7e49f-122">**Fylgiskjal** – Fylgiskjalsnúmer TDS-færslunnar.</span><span class="sxs-lookup"><span data-stu-id="7e49f-122">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="7e49f-123">**Uppruni** – Einingin sem TDS-færslan var stofnuð í.</span><span class="sxs-lookup"><span data-stu-id="7e49f-123">**Source** – The module that the TDS transaction was created in.</span></span>
    - <span data-ttu-id="7e49f-124">**Lykill** – Númer lánardrottna-, viðskiptavina- eða fjárhagslykils sem TDS-færslan var stofnuð fyrir.</span><span class="sxs-lookup"><span data-stu-id="7e49f-124">**Account** – The vendor, customer, or ledger account number that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="7e49f-125">**Heiti** – Heiti lánardrottna-, viðskiptavina- eða fjárhagslykils sem TDS-færslan var stofnuð fyrir.</span><span class="sxs-lookup"><span data-stu-id="7e49f-125">**Name** – The name of the vendor, customer, or ledger account that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="7e49f-126">**Upphæð** – Upphæð reiknings sem TDS var reiknað fyrir.</span><span class="sxs-lookup"><span data-stu-id="7e49f-126">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="7e49f-127">**Skattupphæð** – TDS-skattupphæð sem reiknuð var fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="7e49f-127">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>
    - <span data-ttu-id="7e49f-128">**Dagsetning vottorðs** – Dagsetning TDS-vottorðs sem var uppfært fyrir TDS-færsluna.</span><span class="sxs-lookup"><span data-stu-id="7e49f-128">**Certificate date** – The TDS certificate date that was updated for the TDS transaction.</span></span>
    - <span data-ttu-id="7e49f-129">**Númer vottorðs** – Númer TDS-vottorðs sem var uppfært fyrir TDS-færsluna.</span><span class="sxs-lookup"><span data-stu-id="7e49f-129">**Certificate number** – TDS certificate number that was updated for the TDS transaction.</span></span>

10. <span data-ttu-id="7e49f-130">Á síðunni **Endurheimtanleg vottorð** skal velja gátreitinn **Lokað** til að loka númeri TDS-vottorðs þegar búið er að uppfæra það fyrir TDS-færslur á síðunni **Uppfæra vottorð**.</span><span class="sxs-lookup"><span data-stu-id="7e49f-130">On the **Recoverable certificates** page, select the **Closed** check box to close the TDS certificate number after you've finished updating it for TDS transactions on the **Update certificate** page.</span></span>

    <span data-ttu-id="7e49f-131">Til að velja gátreitinn **Lokað** fyrir allar færslur á síðunni skal velja **Merkja allt**.</span><span class="sxs-lookup"><span data-stu-id="7e49f-131">To select the **Closed** check box for all records on the page, select **Mark all**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e49f-132">Númer TDS-vottorða sem gátreiturinn **Lokað** er valinn fyrir eru ekki í boði á síðunni **Uppfæra vottorð**.</span><span class="sxs-lookup"><span data-stu-id="7e49f-132">TDS certificate numbers that the **Closed** check box is selected for aren't available on the **Update certificate** page.</span></span>
