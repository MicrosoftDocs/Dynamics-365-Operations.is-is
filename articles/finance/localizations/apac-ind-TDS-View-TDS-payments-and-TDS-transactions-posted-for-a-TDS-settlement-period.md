---
title: Skoða bókaðar TDS-greiðslur og færslur fyrir TDS-jöfnunartímabil
description: Þetta efnisatriði útskýrir hvernig á að skoða greiðslur skatts sem dreginn er frá í uppruna (TDS) og færslur sem voru bókaðar fyrir jöfnunartímabil.
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 2bada42073e46c69101e6d31f3328a2eeb95f880
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023321"
---
# <a name="view-posted-tds-payments-and-transactions-for-a-tds-settlement-period"></a><span data-ttu-id="07979-103">Skoða bókaðar TDS-greiðslur og færslur fyrir TDS-jöfnunartímabil</span><span class="sxs-lookup"><span data-stu-id="07979-103">View posted TDS payments and transactions for a TDS settlement period</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07979-104">Þetta efnisatriði útskýrir hvernig á að skoða greiðslur skatts sem dreginn er frá í uppruna (TDS) og færslur sem voru bókaðar fyrir jöfnunartímabil.</span><span class="sxs-lookup"><span data-stu-id="07979-104">This topic explains how to view the Tax Deducted at Source (TDS) payments and transactions that were posted for a settlement period.</span></span>

1. <span data-ttu-id="07979-105">Farið í **Skattur \> Óbeinir skattar \> Staðgreiðsluskattur \> Jöfnunartímabil staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="07979-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="07979-106">[![Jöfnunartímabilssíða staðgreiðsluskatts](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)</span><span class="sxs-lookup"><span data-stu-id="07979-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)</span></span>

2. <span data-ttu-id="07979-107">Á síðunni **Uppgjörstímabil staðgreiðslu skatta** velur þú **Uppgjörstímabil staðgreiðslu** til að opna síðuna **Staðgreiðslu skatta** þar sem hægt er að skoða TDS-uppgjör sem gerð voru fyrir tiltekið TDS-jöfnunartímabil.</span><span class="sxs-lookup"><span data-stu-id="07979-107">On the **Withholding tax settlement periods** page, select **Withholding tax payments** to open the **Withholding tax payments** page, where you can view the TDS settlements that were made for a specific TDS settlement period.</span></span>

    <span data-ttu-id="07979-108">Flipinn **Yfirlit** sýnir eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="07979-108">The **Overview** tab shows the following information:</span></span>

    - <span data-ttu-id="07979-109">**Dagsetning** – Dagsetning TDS uppgjörs.</span><span class="sxs-lookup"><span data-stu-id="07979-109">**Date** – The date of TDS settlement.</span></span>
    - <span data-ttu-id="07979-110">**Fylgiskjal** – Fylgiskjalsnúmer TDS-jöfnunarfærslunnar.</span><span class="sxs-lookup"><span data-stu-id="07979-110">**Voucher** – The voucher number of the TDS settlement transaction.</span></span>
    - <span data-ttu-id="07979-111">**Gerð skatts** – Gerð skatts sem uppgjörsferlið er keyrt fyrir.</span><span class="sxs-lookup"><span data-stu-id="07979-111">**Tax type** – The tax type that the settlement process is run for.</span></span>
    - <span data-ttu-id="07979-112">**Skattlykilnúmer (TAN)** – Skattlykilnúmer (TAN) bókaðarar TDS-færslu.</span><span class="sxs-lookup"><span data-stu-id="07979-112">**Tax Account Number (TAN)** – The Tax Account Number (TAN) of the settled TDS transaction.</span></span>
    - <span data-ttu-id="07979-113">**Jöfnunartímabil** – Jöfnunartímabilið sem TDS uppgjörsferlið er keyrt fyrir.</span><span class="sxs-lookup"><span data-stu-id="07979-113">**Settlement period** – The settlement period that the TDS settlement process is run for.</span></span>
    - <span data-ttu-id="07979-114">**Frá dagsetning** – Upphafsdagur jöfnunartímabilsins.</span><span class="sxs-lookup"><span data-stu-id="07979-114">**From date** – The start date of the settlement period.</span></span>
    - <span data-ttu-id="07979-115">**Til dagsetningar** – Lokadagsetning jöfnunartímabilsins.</span><span class="sxs-lookup"><span data-stu-id="07979-115">**To date** – The end date of the settlement period.</span></span>
    - <span data-ttu-id="07979-116">**Greiðsluútgáfa staðgreiðsluskatts** – Útgáfa greiðslu staðgreiðsluskatts: **Upprunaleg**, **Nýjustu leiðréttingar** eða **Heildarlisti**.</span><span class="sxs-lookup"><span data-stu-id="07979-116">**Withholding tax payment version** – The version of the withholding tax payment: **Original**, **Latest corrections**, or **Total list**.</span></span>

5. <span data-ttu-id="07979-117">Veldu **skjámynd** til að skoða fylgiskjalsfærslur fyrir TDS-færsluna.</span><span class="sxs-lookup"><span data-stu-id="07979-117">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
6. <span data-ttu-id="07979-118">Veljið **Staðgreiðsluskattsfærslur** til að skoða upplýsingar um mismunandi TDS-færslur sem voru gerðar upp fyrir tiltekið tímabil í jöfnunartímabili.</span><span class="sxs-lookup"><span data-stu-id="07979-118">Select **Withholding tax transactions** to view the details of the TDS transactions that were settled for a specific period during a settlement period.</span></span> <span data-ttu-id="07979-119">Veldu **skjámynd** til að skoða fylgiskjalsfærslur fyrir TDS-færsluna.</span><span class="sxs-lookup"><span data-stu-id="07979-119">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span> <span data-ttu-id="07979-120">Veljið  **Staðgreiðsluskattshlutar** til að skoða TDS sem var reiknað fyrir hvern TDS-skattaþátt fyrir ákveðinn TDS-skattkóða.</span><span class="sxs-lookup"><span data-stu-id="07979-120">Select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>
7. <span data-ttu-id="07979-121">Lokið síðunni **Greiðslur staðgreiðsluskatts** til að snúa aftur á síðuna **Jöfnunartímabilssíða staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="07979-121">Close the **Withholding tax payments** page to return to the **Withholding tax settlement periods** page.</span></span>
8. <span data-ttu-id="07979-122">Veljið **Staðgreiðsluskattsfærslur** til að skoða upplýsingar um mismunandi TDS-færslur sem voru gerðar upp fyrir tímabilið.</span><span class="sxs-lookup"><span data-stu-id="07979-122">Select **Withholding tax transactions** to view the details of the TDS transactions that were settled for the settlement period.</span></span>
