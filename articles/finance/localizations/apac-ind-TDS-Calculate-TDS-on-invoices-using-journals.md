---
title: Reikna út TDS á reikningum með færslubókum
description: Í þessu efnisatriði eru talin upp skrefin fyrir útreikning á TDS fyrir færslubækur.
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
ms.openlocfilehash: d68e1b3a4dc31823ec56a525149f16bdc23c0883
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023342"
---
# <a name="calculate-tds-on-invoices-using-journals"></a><span data-ttu-id="1035d-103">Reikna út TDS á reikningum með færslubókum</span><span class="sxs-lookup"><span data-stu-id="1035d-103">Calculate TDS on invoices using journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1035d-104">Í þessu efnisatriði eru talin upp skrefin fyrir útreikning á TDS fyrir færslubækur.</span><span class="sxs-lookup"><span data-stu-id="1035d-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on journals.</span></span>

<span data-ttu-id="1035d-105">Byrjið á því að opna síðuna **Almennar færslubækur** (**Fjárhag > Færslubókarfærslur > Almennar færslubækur**).</span><span class="sxs-lookup"><span data-stu-id="1035d-105">Begin by opening the **General journals** page (**General ledger > Journal entries > General journals**).</span></span>

<span data-ttu-id="1035d-106">[![Almennar færslubækur](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span><span class="sxs-lookup"><span data-stu-id="1035d-106">[![General journals](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span></span>

1. <span data-ttu-id="1035d-107">Stofnið færslubókarlínur með skjámyndum færslubókar sem eru gefnar upp í töflunni.</span><span class="sxs-lookup"><span data-stu-id="1035d-107">Create journal lines using the journal forms that are listed in the table.</span></span> <span data-ttu-id="1035d-108">Veljið gerð lykils og gerð mótlykils og sláið inn upphæð færslunnar.</span><span class="sxs-lookup"><span data-stu-id="1035d-108">Select the account type and offset account type and enter the amount for the transaction.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="1035d-109">Á síðunni **Færslubókarsamþykkt reiknings** skal velja **Finna fylgiskjöl** og velja reikninga til að reikna út TDS fyrir.</span><span class="sxs-lookup"><span data-stu-id="1035d-109">On the **Invoice approval journal** page, select **Find vouchers** and select invoices to calculate TDS on.</span></span> <span data-ttu-id="1035d-110">Skoðið reikningana sem stofnaðir eru á síðunni **Skráning reiknings** eða síðunni **Finna fylgiskjöl**.</span><span class="sxs-lookup"><span data-stu-id="1035d-110">View the invoices created in the **Invoice register** page or the **Find vouchers** page.</span></span>  

2. <span data-ttu-id="1035d-111">Í flipanum **Almennt** á síðunni **Fylgiskjal færslubókar** skal skoða eða breyta sjálfgefnum TDS-flokki sem skilgreindur er fyrir lánardrottin eða viðskiptavin í reitnum **TDS-flokkur**.</span><span class="sxs-lookup"><span data-stu-id="1035d-111">On the **General** tab of the **Journal voucher** page, view or modify the default TDS group defined for the vendor or customer, in the **TDS group** field.</span></span> <span data-ttu-id="1035d-112">TDS-upphæðin sem er reiknuð út í færslubókarlínum byggir á formúlu sem skilgreind er fyrir TDS-skattkóðana sem gefnir eru upp í reitnum **TDS-flokkur**.</span><span class="sxs-lookup"><span data-stu-id="1035d-112">The TDS amount that's calculated on journal lines is based on the formula defined for the TDS tax codes listed in the **TDS group** field.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="1035d-113">Reiturinn **Staðgreiðsluskattsflokkur** og reiturinn **TCS-flokkur** verða ekki í boði þegar TDS-flokkur er valinn í reitnum **TDS-flokkur**.</span><span class="sxs-lookup"><span data-stu-id="1035d-113">The **Withholding tax group**  field and the **TCS group** field become unavailable when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="1035d-114">Reiturinn **Staðgreiðsluskattsflokkur** er aðeins í boði á síðunni **Almenn færslubók**.</span><span class="sxs-lookup"><span data-stu-id="1035d-114">The **Withholding tax group** field is available only on the **General journal** page.</span></span> <span data-ttu-id="1035d-115">TDS er aðeins reiknað ef gátreiturinn **Reikna staðgreiðsluskatt** er valinn fyrir lánardrottin eða viðskiptavin á síðunum **Allir lánardrottnar** eða **Allir viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="1035d-115">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** pages.</span></span>   

3. <span data-ttu-id="1035d-116">Veljið flipann **Skattaupplýsingar**. Veljið önnur aðsetur fyrirtækis sem sett er upp fyrir fyrirtækið í þessum reit ef á þarf að halda.</span><span class="sxs-lookup"><span data-stu-id="1035d-116">Select the **Tax information** tab. Select the alternate addresses of a company that's set up for the company in this field, if required.</span></span> <span data-ttu-id="1035d-117">Hægt er að skoða heiti fyrirtækis í reitnum **Heiti** sem er undir reitahópnum **Upplýsingar um fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="1035d-117">You can view the company name in the **Name** field, which is under the **Company information** field group.</span></span> 

4. <span data-ttu-id="1035d-118">Skoðið eðli skattgreiðendaflokksins fyrir lánardrottin eða viðskiptavin í reitnum **Eðli skattgreiðanda** sem er undir reitahópnum **Staðgreiðsluskattur**.</span><span class="sxs-lookup"><span data-stu-id="1035d-118">View the nature of assessee category of the vendor or customer in the **Nature of assessee** field, which is under the **Withholding tax** field group.</span></span> <span data-ttu-id="1035d-119">Í reitnum **Skattlykilnúmer** (**TAN**) skal skoða TAN fyrir valið heiti fyrirtækis sem er sýnt.</span><span class="sxs-lookup"><span data-stu-id="1035d-119">In the **Tax Account Number** (**TAN**) field, view the TAN of the selected company name that's displayed.</span></span>  

5. <span data-ttu-id="1035d-120">Veljið **Staðgreiðsluskattur** í valmyndinni **Staðgreiðsluskattur** til að opna síðuna **Tímabundnar staðgreiðsluskattsfærslur**.</span><span class="sxs-lookup"><span data-stu-id="1035d-120">Select **Withholding tax** in **Withholding tax** menu to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="1035d-121">Eftirfarandi reitir eru sýndir í efri rúðunni á síðunni **Tímabundnar staðgreiðsluskattsfærslur**.</span><span class="sxs-lookup"><span data-stu-id="1035d-121">The following fields are displayed on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="1035d-122">**Upphæð staðgreiðsluskatts samtals** - Samtals TDS reiknað út fyrir færsluna fyrir TDS-flokkinn.</span><span class="sxs-lookup"><span data-stu-id="1035d-122">**Withholding tax amount in total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="1035d-123">**Gildi** - Heildarprósenta notuð til að reikna út TDS fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="1035d-123">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="1035d-124">Heildarprósentan er byggð á formúlunni sem er skilgreind fyrir TDS-skattkóða sem hengdir eru við TDS-flokkinn.</span><span class="sxs-lookup"><span data-stu-id="1035d-124">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="1035d-125">**Samtals leiðrétt upphæð staðgreiðsluskatts** - Leiðrétt heildarupphæð TDS fyrir alla skattkóða í TDS-flokknum.</span><span class="sxs-lookup"><span data-stu-id="1035d-125">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="1035d-126">**TDS** - Ef valið er TDS-flokkur hengdur við færsluna.</span><span class="sxs-lookup"><span data-stu-id="1035d-126">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

  <span data-ttu-id="1035d-127">Reitirnir í flipunum **Yfirlit**, **Almennt** og **Leiðrétting** á síðunni **Tímabundnar staðgreiðsluskattsfærslur** sýna upplýsingar um reiknaða TDS-upphæð og leiðrétta TDS-upphæð fyrir hvern TDS-skattkóða sem hengdur er við TDS-flokkinn.</span><span class="sxs-lookup"><span data-stu-id="1035d-127">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

6. <span data-ttu-id="1035d-128">Veljið **Mörk** til að opna síðuna **Mörk**.</span><span class="sxs-lookup"><span data-stu-id="1035d-128">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="1035d-129">Skoðið mörkin og undantekningarmörkin sem skilgreind eru fyrir TDS-skattþáttinn sem hengdur er við tiltekinn TDS-skattkóða á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="1035d-129">View the threshold limit and exception threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

   <span data-ttu-id="1035d-130">Veljið **Formúluhönnuður** til að opna skjámyndina **Formúluhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="1035d-130">Select **Formula designer** to open the **Formula designer** form.</span></span> <span data-ttu-id="1035d-131">Skoðið formúluna sem er skilgreind fyrir tiltekinn TDS-skattkóða á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="1035d-131">View the formula defined for a specific TDS tax code in this page.</span></span> <span data-ttu-id="1035d-132">Lokið síðunum **Formúluhönnuður** og **Tímabundnar staðgreiðsluskattsfærslur** til að fara aftur á síðuna **Fylgiskjal færslubókar**.</span><span class="sxs-lookup"><span data-stu-id="1035d-132">Close the **Formula designer** and **Temporary withholding tax transactions** pages to return to the **Journal voucher** page.</span></span>

8. <span data-ttu-id="1035d-133">Færið inn aðrar áskildar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="1035d-133">Enter the other required details.</span></span> <span data-ttu-id="1035d-134">Villuleita og bóka færslubók.</span><span class="sxs-lookup"><span data-stu-id="1035d-134">Validate and post the journal.</span></span> <span data-ttu-id="1035d-135">TDS-upphæðin sem er reiknuð í innkaupareikningum er bókuð á lykil viðskiptaskulda.</span><span class="sxs-lookup"><span data-stu-id="1035d-135">The TDS amount that's calculated on purchase invoices is posted to the payable account.</span></span> <span data-ttu-id="1035d-136">TDS-upphæðin sem reiknuð er fyrir innkaupareikninga er bókuð á lykil viðskiptakrafa sem er skilgreindur fyrir hvern TDS-skattkóða í TDS-skattflokknum.</span><span class="sxs-lookup"><span data-stu-id="1035d-136">The TDS amount that's calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="1035d-137">Lyklar viðskiptaskulda er viðskiptakrafa fyrir TDS-skattkóða eru skilgreindir á síðunni **Staðgreiðsluskattskóðar**.</span><span class="sxs-lookup"><span data-stu-id="1035d-137">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

9. <span data-ttu-id="1035d-138">Veljið **Bókaður staðgreiðsluskattur** til að opna síðuna **Staðgreiðsluskattsfærslur**.</span><span class="sxs-lookup"><span data-stu-id="1035d-138">Select **Posted withholding tax** to open the **Withholding** **tax** **transactions** page.</span></span> <span data-ttu-id="1035d-139">Í reitnum **Gildi** er heildarprósentan sem er notuð til að reikna út TDS fyrir færsluna sýnd.</span><span class="sxs-lookup"><span data-stu-id="1035d-139">In the **Value** field, the total percentage used to calculate TDS for the transaction is displayed.</span></span>

   <span data-ttu-id="1035d-140">Reitirnir í flipunum **Yfirlit**, **Almennt** og **Upphæð** á síðunni Tímabundnar staðgreiðsluskattsfærslur sýna upplýsingar um reiknaða TDS-upphæð og leiðrétta TDS-upphæð fyrir hvern TDS-skattkóða sem hengdur er við TDS-flokkinn.</span><span class="sxs-lookup"><span data-stu-id="1035d-140">The fields on the **Overview**, **General**, and **Amount** tabs in the Withholding tax transactions page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>
