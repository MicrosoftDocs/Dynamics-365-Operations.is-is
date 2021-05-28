---
title: TDS-útreikningur á reikningum af síðu reiknings með frjálsum texta
description: Í þessu efnisatriði er útskýrt hvernig á að reikna út skatt sem dreginn er frá upprunalegri greiðslu (TDS) á reikningum með því að nota síðu reiknings með frjálsum texta.
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
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023334"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a><span data-ttu-id="1ba66-103">TDS-útreikningur á reikningum af síðu reiknings með frjálsum texta</span><span class="sxs-lookup"><span data-stu-id="1ba66-103">TDS calculation on invoices from the Free text invoice page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ba66-104">Í þessu efnisatriði er útskýrt hvernig á að reikna út skatt sem dreginn er frá upprunalegri greiðslu (TDS) á reikningum með því að nota síðuna **Reikningur með frjálsum texta**.</span><span class="sxs-lookup"><span data-stu-id="1ba66-104">This topic explains how to calculate Tax Deducted at Source (TDS) on invoices by using the **Free text invoice** page.</span></span>

1. <span data-ttu-id="1ba66-105">Fara í **Viðskiptakröfur \> Reikningar \> Allir reikningar með frjálsum texta**.</span><span class="sxs-lookup"><span data-stu-id="1ba66-105">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>

    <span data-ttu-id="1ba66-106">[![Síða reiknings með frjálsum texta](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span><span class="sxs-lookup"><span data-stu-id="1ba66-106">[![Free text invoice page](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span></span>

2. <span data-ttu-id="1ba66-107">Veljið **Nýr** til að stofna nýjan reikning með frjálsum texta og færið inn nauðsynlegar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="1ba66-107">Select **New** to create a free text invoice, and enter the required details.</span></span>
3. <span data-ttu-id="1ba66-108">Veljið flipann **Reikningur**. Í hlutanum **Staðgreiðsluskattsflokkur** sýnir reiturinn **Eðli skattgreiðanda** eðli skattgreiðendaflokks viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="1ba66-108">Select the **Invoice** tab. In the **Withholding tax group** section, the **Nature of assessee** field shows the nature of assessee category of the customer.</span></span>
4. <span data-ttu-id="1ba66-109">Í reitnum **TDS-flokkur** skal yfirfara og breyta sjálfgefnum TDS-flokki sem er skilgreindur fyrir viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="1ba66-109">In the **TDS group** field, review or change the default TDS group that is defined for the customer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1ba66-110">Þegar gildi er valið í reitnum **TDS-flokkur** verður reiturinn **TCS-flokkur** óaðgengilegur.</span><span class="sxs-lookup"><span data-stu-id="1ba66-110">When you select a value in the **TDS group** field, the **TCS group** field becomes unavailable.</span></span> <span data-ttu-id="1ba66-111">TDS er aðeins reiknað ef valkosturinn **Reikna staðgreiðsluskatt** er stilltur á **Já** fyrir viðskiptavininn á síðunni **Allir viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="1ba66-111">TDS is calculated only if the **Calculate withholding tax** option is set to **Yes** for the customer on the **All customers** page.</span></span>

5. <span data-ttu-id="1ba66-112">Í flipanum **Skattaupplýsingar**, í hlutanum **Upplýsingar um fyrirtæki**, í reitnum **Heiti**, skal velja heiti fyrirtækis fyrir aukaaðsetur sem hefur verið sett upp fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="1ba66-112">On the **Tax information** tab, in the **Company information** section, in the **Name** field, select the company name for an alternate address that has been set up for the company.</span></span>

    <span data-ttu-id="1ba66-113">Í hlutanum **Staðgreiðsluskattur** sýnir reiturinn **Skattlykilnúmer (TAN)** skattlykilnúmer (TAN) fyrir valið fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="1ba66-113">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the tax account number (TAN) for the selected company.</span></span>

6. <span data-ttu-id="1ba66-114">Í flipanum **Reikningslínur** skal stofna reikningslínur og færa inn nauðsynlegar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="1ba66-114">On the **Invoice lines** tab, create invoice lines, and enter the required details.</span></span>

    <span data-ttu-id="1ba66-115">Í hlutanum **Staðgreiðsluskattsflokkur** sýnir reiturinn **Skattlykilnúmer (TAN)** TAN og reiturinn **TDS-flokkur** sýnir TDS-flokkinn.</span><span class="sxs-lookup"><span data-stu-id="1ba66-115">In the **Withholding tax group** section, the **Tax Account Number (TAN)** field shows the TAN, and the **TDS group** field shows the TDS group.</span></span>

7. <span data-ttu-id="1ba66-116">Veljið **Staðgreiðsluskattur** til að opna síðuna **Tímabundnar staðgreiðsluskattsfærslur**.</span><span class="sxs-lookup"><span data-stu-id="1ba66-116">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="1ba66-117">Efri hluti þessarar síðu hefur eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="1ba66-117">The upper part of this page has the following fields:</span></span>

    - <span data-ttu-id="1ba66-118">**Upphæð staðgreiðsluskatts samtals** - Samtals TDS sem var reiknað út fyrir færsluna fyrir TDS-flokkinn.</span><span class="sxs-lookup"><span data-stu-id="1ba66-118">**Withholding tax amount in total** – The total TDS that was calculated for the transaction for the TDS group.</span></span>
    - <span data-ttu-id="1ba66-119">**Gildi** - Heildarprósenta sem var notuð til að reikna út TDS fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="1ba66-119">**Value** – The total percentage that was used to calculate TDS for the transaction.</span></span> <span data-ttu-id="1ba66-120">Heildarprósentan er byggð á formúlunni sem er skilgreind fyrir TDS-skattkóða og hengd við TDS-flokkinn.</span><span class="sxs-lookup"><span data-stu-id="1ba66-120">The total percentage is based on the formula that is defined for the TDS tax codes and attached to the TDS group.</span></span>
    - <span data-ttu-id="1ba66-121">**Samtals leiðrétt upphæð staðgreiðsluskatts** – Leiðrétt heildarupphæð TDS fyrir alla skattkóða í TDS-flokknum.</span><span class="sxs-lookup"><span data-stu-id="1ba66-121">**Adjusted withholding tax amount in total** – The total adjusted TDS amount for all tax codes in the TDS group.</span></span>
    - <span data-ttu-id="1ba66-122">**TDS** – Valinn gátreitur gefur til kynna að TDS-flokkurinn er hengdur við færsluna.</span><span class="sxs-lookup"><span data-stu-id="1ba66-122">**TDS** – A selected checkbox indicates that a TDS group is attached to the transaction.</span></span>

    <span data-ttu-id="1ba66-123">Reitirnir í flipunum **Yfirlit**, **Almennt** og **Leiðrétting** sýna reiknaða upphæð TDS og upplýsingar um leiðrétta TDS-upphæð fyrir hvern TDS-skattkóða sem er hengdur við TDS-flokkinn.</span><span class="sxs-lookup"><span data-stu-id="1ba66-123">The fields on the **Overview**, **General**, and **Adjustment** tabs show the calculated TDS amount and details of the adjusted TDS amount for each TDS tax code that is attached to the TDS group.</span></span>

8. <span data-ttu-id="1ba66-124">Veljið **Mörk** til að opna síðuna **Mörk** þar sem hægt er að fara yfir hámarkið sem er skilgreint fyrir TDS-skatthluta sem er hengdur við tiltekinn TDS-skattkóða.</span><span class="sxs-lookup"><span data-stu-id="1ba66-124">Select **Threshold** to open the **Threshold** page, where you can review the threshold limit that is defined for the TDS tax component that is attached to a specific TDS tax code.</span></span>
9. <span data-ttu-id="1ba66-125">Veldu **Formúluhönnuður** til að opna síðuna **Formúluhönnuður** þar sem hægt er að fara yfir formúluna sem er skilgreind fyrir tiltekinn TDS-skattkóða.</span><span class="sxs-lookup"><span data-stu-id="1ba66-125">Select **Formula designer** to open the **Formula designer** page, where you can review the formula that is defined for a specific TDS tax code.</span></span>
10. <span data-ttu-id="1ba66-126">Bóka textareikning.</span><span class="sxs-lookup"><span data-stu-id="1ba66-126">Post the free text invoice.</span></span> <span data-ttu-id="1ba66-127">TDS-upphæðin sem reiknuð er fyrir reikning með frjálsum texta er bókuð á lykil viðskiptakrafa sem er skilgreindur fyrir hvern TDS-skattkóða í TDS-flokknum.</span><span class="sxs-lookup"><span data-stu-id="1ba66-127">The TDS amount that is calculated for the free text invoice is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="1ba66-128">Lyklar viðskiptakrafa fyrir TDS-skattkóða eru skilgreindir á síðunni **Staðgreiðsluskattskóðar**.</span><span class="sxs-lookup"><span data-stu-id="1ba66-128">The receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>
11. <span data-ttu-id="1ba66-129">Veljið **Bókaður staðgreiðsluskattur** til að opna síðuna **Staðgreiðsluskattsfærslur**.</span><span class="sxs-lookup"><span data-stu-id="1ba66-129">Select **Posted withholding tax** to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="1ba66-130">Reiturinn **Gildi** sýnir heildarprósentuna sem var notuð til að reikna út TDS fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="1ba66-130">The **Value** field shows the total percentage that was used to calculate TDS for the transaction.</span></span>

    <span data-ttu-id="1ba66-131">Reitirnir í flipunum **Yfirlit**, **Almennt** og **Upphæð** sýna TDS-upphæðirnar sem voru reiknaðar í reikningslínunum.</span><span class="sxs-lookup"><span data-stu-id="1ba66-131">The fields on the **Overview**, **General**, and **Amount** tabs show the TDS amounts that were calculated on the invoice lines.</span></span>

12. <span data-ttu-id="1ba66-132">Farið yfir upplýsingar um útreikning TDS fyrir hvern TDS-skattkóða sem hengdur er við TDS-flokkinn.</span><span class="sxs-lookup"><span data-stu-id="1ba66-132">Review the TDS calculation information for each TDS tax code that is attached to the TDS group.</span></span>
