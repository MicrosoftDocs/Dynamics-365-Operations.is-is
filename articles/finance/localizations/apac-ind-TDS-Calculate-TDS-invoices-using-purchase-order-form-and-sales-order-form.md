---
title: Reikna út TDS-reikninga með skjámynd innkaupapöntunar eða sölupöntunar
description: Í þessu efnisatriði eru talin upp skrefin fyrir útreikning á TDS fyrir ýmsar gerðir reikninga.
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
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023318"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a><span data-ttu-id="2e5e6-103">Reikna út TDS-reikninga með skjámynd innkaupapöntunar eða sölupöntunar</span><span class="sxs-lookup"><span data-stu-id="2e5e6-103">Calculate TDS invoices using purchase order form and sales order form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e5e6-104">Í þessu efnisatriði eru talin upp skrefin fyrir útreikning á TDS fyrir ýmsar gerðir reikninga með síðunum **Innkaupapöntun**, **Innkaupabók**, **Standandi pöntun** og **Sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on various types of invoices using the **Purchase order**, **Purchase journal**, **Blanket order**, and **Sales order** pages.</span></span>

1. <span data-ttu-id="2e5e6-105">Stofnið innkaupapöntun, innkaupabók, standandi innkaupapöntun eða sölupöntun með síðunni sem gefin er upp.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-105">Create a purchase order, purchase journal, purchase blanket order, or a sales order using the page listed.</span></span> <span data-ttu-id="2e5e6-106">Færið inn nauðsynlegar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-106">Enter the required details.</span></span>

2. <span data-ttu-id="2e5e6-107">Veljið flipann **Uppsetning** til að skoða eðli skattgreiðanda fyrir lánardrottin eða viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-107">Select the **Setup** tab to view the nature of the assessee of the vendor or customer.</span></span> <span data-ttu-id="2e5e6-108">Þessar upplýsingar eru taldar upp í reitnum **Eðli skattgreiðanda** undir reitahópnum **Staðgreiðsluskattsflokkur**.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-108">This information is listed in the **Nature of assessee** field, under the **Withholding tax group** field group.</span></span>

3. <span data-ttu-id="2e5e6-109">Í reitnum **TDS-flokkur** skal skoða eða breyta sjálfgefnum TDS-flokki sem skilgreindur er fyrir lánardrottin eða viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-109">In the **TDS group** field, view or modify the default TDS group defined for the vendor or customer.</span></span>

   > [!NOTE]
   > <span data-ttu-id="2e5e6-110">Reiturinn **TDS-flokkur** er ekki í boði þegar TDS-flokkur er valinn í reitnum **TDS-flokkur**.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-110">The **TCS group** field isn't available when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="2e5e6-111">TDS er aðeins reiknað ef gátreiturinn **Reikna staðgreiðsluskatt** er valinn fyrir lánardrottin eða viðskiptavin á síðunni **Allir lánardrottnar** eða **Allir viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-111">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** page.</span></span>  

4. <span data-ttu-id="2e5e6-112">Stofnið vörulínur í flipanum **Línur** og færið inn nauðsynlegar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-112">Create item lines on the **Lines** tab and enter the required details.</span></span>

5. <span data-ttu-id="2e5e6-113">Veljið flipann **Uppsetning** (línustig) til að skoða eða breyta TDS-flokknum sem skilgreindur er á hausastigi.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-113">Select the **Setup** tab (line-level) to view or change the TDS group defined at the header-level.</span></span> <span data-ttu-id="2e5e6-114">TDS-flokkurinn birtist í reitnum **TDS-flokkur** sem er undir reitahópnum **Staðgreiðsluskattsflokkur**.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-114">The TDS group is displayed in the **TDS group** field, which is under the **Withholding tax group** field group.</span></span>

6. <span data-ttu-id="2e5e6-115">Veljið flipann **Skattaupplýsingar** og veljið önnur aðsetur sem eru sett upp fyrir heiti fyrirtækis sem sýnt er í þessum reit.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-115">Select the **Tax information** tab and select alternate addresses that are set up for the company name that's displayed in this field.</span></span> <span data-ttu-id="2e5e6-116">Heiti fyrirtækis er sýnt í reitnum **Heiti** sem er undir reitahópnum **Upplýsingar um fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-116">The company name is displayed in the **Name** field, which is under the **Company information** field group.</span></span> 

   <span data-ttu-id="2e5e6-117">TAN fyrir valið heiti fyrirtækis er sýnt í reitnum **Skattlykilnúmer** (**TAN**) undir reitahópnum **Staðgreiðsluskattur**.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-117">The TAN of the selected company name is displayed in the **Tax Account Number** (**TAN**) field, under the **Withholding tax** field group.</span></span> 

7. <span data-ttu-id="2e5e6-118">Veljið **Staðgreiðsluskattur** til að opna síðuna **Tímabundnar staðgreiðsluskattsfærslur**.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-118">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="2e5e6-119">Skoðið eftirfarandi reiti í efri rúðunni á síðunni **Tímabundnar staðgreiðsluskattsfærslur**.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-119">View the following fields on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="2e5e6-120">**Upphæð** **skatta** **upphæðar** **í** **alls** - Samtals TDS reiknað út fyrir færsluna fyrir TDS-flokkinn.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-120">**Withholding** **tax** **amount** **in** **total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="2e5e6-121">**Gildi** - Heildarprósenta notuð til að reikna út TDS fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-121">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="2e5e6-122">Heildarprósentan er byggð á formúlunni sem er skilgreind fyrir TDS-skattkóða sem hengdir eru við TDS-flokkinn.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-122">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="2e5e6-123">**Samtals leiðrétt upphæð staðgreiðsluskatts** - Leiðrétt heildarupphæð TDS fyrir alla skattkóða í TDS-flokknum.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-123">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="2e5e6-124">**TDS** - Ef valið er TDS-flokkur hengdur við færsluna.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-124">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

<span data-ttu-id="2e5e6-125">Reitirnir í flipunum **Yfirlit**, **Almennt** og **Leiðrétting** á síðunni **Tímabundnar staðgreiðsluskattsfærslur** sýna upplýsingar um reiknaða TDS-upphæð og leiðrétta TDS-upphæð fyrir hvern TDS-skattkóða sem hengdur er við TDS-flokkinn.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-125">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

8. <span data-ttu-id="2e5e6-126">Veljið **Mörk** til að opna síðuna **Mörk**.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-126">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="2e5e6-127">Skoðið mörkin sem skilgreind eru fyrir TDS-skattþáttinn sem hengdur er við tiltekinn TDS-skattkóða á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-127">View the threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

9. <span data-ttu-id="2e5e6-128">Veljið **Formúluhönnuður** til að opna síðuna **Formúluhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-128">Select **Formula designer** to open the **Formula designer** page.</span></span> <span data-ttu-id="2e5e6-129">Skoðið formúluna sem er skilgreind fyrir tiltekinn TDS-skattkóða á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-129">View the formula that is defined for a specific TDS tax code on this page.</span></span> 

10. <span data-ttu-id="2e5e6-130">Senda reikninginn.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-130">Post the invoice.</span></span> <span data-ttu-id="2e5e6-131">TDS-upphæðin sem reiknuð er fyrir innkaupareikninga er bókuð á lykil viðskiptaskulda og TDS-upphæðin sem reiknuð er fyrir sölureikninga er bókuð á lykil viðskiptakrafa sem er skilgreindur fyrir hvern TDS-skattkóða í TDS-skattflokknum.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-131">The TDS amount calculated on purchase invoices is posted to the payable account and the TDS amount calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="2e5e6-132">Lyklar viðskiptaskulda er viðskiptakrafa fyrir TDS-skattkóða eru skilgreindir á síðunni **Staðgreiðsluskattskóðar**.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-132">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

11. <span data-ttu-id="2e5e6-133">Veljið hnappinn **Fyrirspurn** hnappinn **> Reikningur > Bókaður staðgreiðsluskattur** til að opna síðuna **Staðgreiðsluskattsfærslur**.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-133">Select **Inquiry** button **> Invoice > Posted withholding tax** button to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="2e5e6-134">Þú getur skoðað heildarprósentuna sem notuð er til að reikna út TDS fyrir viðskiptin í reitnum **Gildi**</span><span class="sxs-lookup"><span data-stu-id="2e5e6-134">You can view the total percentage used to calculate TDS for the transaction in the **Value** field.</span></span>

<span data-ttu-id="2e5e6-135">Reitirnir í flipanum **Yfirlit**, **Almennt** og **Upphæð** á síðunni **Staðgreiðsluskattsfærslur** sýna upplýsingar um útreikning TDS fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-135">The fields on the **Overview**, **General**, and **Amount** tabs on the **Withholding tax transactions** page display the information of TDS calculated for the transaction.</span></span> <span data-ttu-id="2e5e6-136">Skoðið upplýsingar um útreikning TDS fyrir hvern TDS-skattkóða sem hengdur er við TDS-flokkinn.</span><span class="sxs-lookup"><span data-stu-id="2e5e6-136">View the TDS calculation information for each TDS tax code attached to the TDS group.</span></span>
