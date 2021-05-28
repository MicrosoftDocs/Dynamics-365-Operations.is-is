---
title: Setja upp staðgreiðsluskattskóða fyrir TDS-skattgerð
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp skattkóða fyrir skatt sem dreginn er frá í uppruna (TDS).
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
ms.openlocfilehash: d56a23f7af7633e1761a8a7c48f71381d6f14df2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023340"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a><span data-ttu-id="31927-103">Setja upp staðgreiðsluskattskóða fyrir TDS-skattgerð</span><span class="sxs-lookup"><span data-stu-id="31927-103">Set up withholding tax codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31927-104">Í þessu efnisatriði er útskýrt hvernig á að setja upp skattkóða fyrir skatt sem dreginn er frá í uppruna (TDS).</span><span class="sxs-lookup"><span data-stu-id="31927-104">This topic explains how to set up tax codes for Tax Deducted at Source (TDS).</span></span>

1. <span data-ttu-id="31927-105">Farið í **Skattur \> Óbeinir skattar \> Staðgreiðsluskattur \> Staðgreiðsluskattskóðar**.</span><span class="sxs-lookup"><span data-stu-id="31927-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax codes**.</span></span>

    <span data-ttu-id="31927-106">[![Síða staðgreiðsluskattskóða](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span><span class="sxs-lookup"><span data-stu-id="31927-106">[![Withholding tax codes page](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span></span>

2. <span data-ttu-id="31927-107">Á aðgerðasvæðinu skal velja **Nýtt** til að stofna staðgreiðsluskattskóa fyrir TDS og færa inn nauðsynlegar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="31927-107">On the Action Pane, select **New** to create a withholding tax code for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="31927-108">Á flýtiflipanum **Almennt** í reitnum **Tegund skatts** er **TDS** valið til að flokka skattkóðann sem TDS-skattkóða.</span><span class="sxs-lookup"><span data-stu-id="31927-108">On the **General** FastTab, in the **Tax type** field, select **TDS** to categorize the tax code as a TDS tax code.</span></span>
4. <span data-ttu-id="31927-109">Í reitnum **Jöfnunartímabil** skal velja jöfnunartímabilið fyrir TDS-skattkóðann.</span><span class="sxs-lookup"><span data-stu-id="31927-109">In the **Settlement period** field, select the TDS settlement period for the TDS tax code.</span></span>
5. <span data-ttu-id="31927-110">Í svæðinu **Aðallykill** skal velja fjárhagslykilinn sem bóka á TDS-upphæðina í.</span><span class="sxs-lookup"><span data-stu-id="31927-110">In the **Main account** field, select the ledger account that the TDS amount should be posted to.</span></span>
6. <span data-ttu-id="31927-111">Í reitnum **Viðskiptakröfur** skal velja þann kröfureikning sem bóka á TDS-upphæðina sem dregin er frá í sölufærslum á.</span><span class="sxs-lookup"><span data-stu-id="31927-111">In the **Receivable account** field, select the receivable account that the TDS amount that is deducted in sales transactions should be posted to.</span></span>

    <span data-ttu-id="31927-112">Reiturinn **Uppruni** er sjálfkrafa stilltur á **Prósenta af brúttó upphæð** og ekki er hægt að breyta gildinu.</span><span class="sxs-lookup"><span data-stu-id="31927-112">The **Origin** field is automatically set to **Percentage of gross amount**, and the value can't be changed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="31927-113">Ekki er hægt að stilla uppruna á **Prósenta af nettó upphæð** fyrir skattkóða af TDS-skatttegund.</span><span class="sxs-lookup"><span data-stu-id="31927-113">You can't set the origin to **Percentage of net amount** for tax codes of the TDS tax type.</span></span>

7. <span data-ttu-id="31927-114">Í reitnum **Hluti staðgreiðsluskatts** skal velja TDS-skatthluta fyrir TDS-skattkóðann.</span><span class="sxs-lookup"><span data-stu-id="31927-114">In the **Withholding tax component** field, select the TDS tax component for the TDS tax code.</span></span>
8. <span data-ttu-id="31927-115">Á aðgerðasvæðinu skal velja **Gildi** til að opna síðuna **Gildi staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="31927-115">On the Action Pane, select **Values** to open the **Withholding tax values** page.</span></span>
9. <span data-ttu-id="31927-116">Í reitnum **Frá dagsetningu** skal færa inn upphafsdagsetningu TDS-gildisins.</span><span class="sxs-lookup"><span data-stu-id="31927-116">In the **From date** field, enter the start date for the TDS value.</span></span> <span data-ttu-id="31927-117">Í reitinn **Til dagsetningar** skal slá inn lokadagsetningu.</span><span class="sxs-lookup"><span data-stu-id="31927-117">In the **To date** field, enter the end date.</span></span>

    > [!NOTE]
    > <span data-ttu-id="31927-118">Reitirnir **Lægri mörk**, **Efri mörk** og **Útiloka %** eru ekki í boði fyrir skattkóða af TDS-skattategund.</span><span class="sxs-lookup"><span data-stu-id="31927-118">The **Minimum limit**, **Upper limit**, and **Exclude %** fields aren't available for tax codes of the TDS tax type.</span></span>

10. <span data-ttu-id="31927-119">Í reitinn **Gildi** skal færa inn prósentu TDS fyrir TDS-skattkóðann.</span><span class="sxs-lookup"><span data-stu-id="31927-119">In the **Value** field, enter the percentage of TDS for the TDS tax code.</span></span>
11. <span data-ttu-id="31927-120">Lokið síðunni **Gildi staðgreiðsluskatts** til að snúa aftur á síðuna **Síða staðgreiðsluskattskóðar**.</span><span class="sxs-lookup"><span data-stu-id="31927-120">Close the **Withholding tax values** page to return to the **Withholding tax codes** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="31927-121">Hnappurinn **Takmarkanir** á síðunni **Staðgreiðsluskattkóðar** er ekki í boði fyrir skattkóða af tegund TDS-skatts.</span><span class="sxs-lookup"><span data-stu-id="31927-121">The **Limits** button on the **Withholding tax codes** page isn't available for tax codes of the TDS tax type.</span></span>

12. <span data-ttu-id="31927-122">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="31927-122">Close the page.</span></span>
