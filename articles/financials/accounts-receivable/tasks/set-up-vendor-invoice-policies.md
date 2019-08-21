---
title: Setja upp reglur lánardrottnareikninga
description: Þetta efni útskýrir hvernig á að setja upp reikninga fyrir lánardrottna í Dynamics 365 for Finance and Operations.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 328aafd16496fdbb963c9aa40a5c13005be7a382
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842810"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="729f4-103">Setja upp reglur lánardrottnareikninga</span><span class="sxs-lookup"><span data-stu-id="729f4-103">Set up vendor invoice policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="729f4-104">Þetta efni útskýrir hvernig á að setja upp reikninga fyrir lánardrottna í Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="729f4-104">This topic explains how to set up vendor invoice policies in Dynamics 365 for Finance and Operatoins.</span></span> <span data-ttu-id="729f4-105">Reikningsreglur lánardrottins eru keyrðar þegar reikningur lánardrottins er bókaður með því að nota síðuna fyrir reikning Lánardrottins og þegar síðan fyrir brot á reikningsreglum lánardrottins er opnuð.</span><span class="sxs-lookup"><span data-stu-id="729f4-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="729f4-106">Einnig er hægt að skilgreina verkflæði fyrir reikning lánardrottins til að keyra reikningsreglur lánardrottins í hvert skipti sem er sendur er reikning til verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="729f4-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="729f4-107">Reikningsreglur lánardrottins eiga ekki við reikninga sem voru stofnaðar í komubók eða reikningabók.</span><span class="sxs-lookup"><span data-stu-id="729f4-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="729f4-108">Sannprófun á reikningsjöfnun notar ekki reikningsreglur lánardrottins, en er í staðinn sett upp á síðunni færibreytur viðskiptaskulda.</span><span class="sxs-lookup"><span data-stu-id="729f4-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="729f4-109">Þessi skráning notar sýnigögn USMF fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="729f4-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="729f4-110">hlutverk viðskiptaskuldastjóri eða aðalbókari myndi framkvæma þessi skrefum.</span><span class="sxs-lookup"><span data-stu-id="729f4-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="729f4-111">Áður en hafist er handa þarf að ganga úr skugga um að skilgreiningarlykill reikningsjöfnunar sé valinn.</span><span class="sxs-lookup"><span data-stu-id="729f4-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="729f4-112">Undirbúa stofnun stefna um reikninga lánardrottins</span><span class="sxs-lookup"><span data-stu-id="729f4-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="729f4-113">Farðu í **Skoðunarrúðu > Kerfiseiningar > Viðskiptaskuldir > Uppsetning > Færibreytur viðskiptaskulda**.</span><span class="sxs-lookup"><span data-stu-id="729f4-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="729f4-114">Veldu flipann **Staðfesting reiknings**.</span><span class="sxs-lookup"><span data-stu-id="729f4-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="729f4-115">Veldu eða hreinsaðu gátreitinn **uppfæra sjálfvirkt stöðu fyrirsögn reiknings**.</span><span class="sxs-lookup"><span data-stu-id="729f4-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="729f4-116">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="729f4-116">Select **OK**.</span></span>
5. <span data-ttu-id="729f4-117">Í reitnum **Bóka reikning með misræmi** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="729f4-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="729f4-118">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="729f4-118">Close the page.</span></span>
7. <span data-ttu-id="729f4-119">Farðu Í **Skoðunarrúðu > Einingar > Viðskiptaskuldir > Regluuppsetning > Reikningrelgur lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="729f4-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="729f4-120">Velja **færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="729f4-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="729f4-121">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="729f4-121">Select **Add**.</span></span>
10. <span data-ttu-id="729f4-122">Lokið síðunni til að fara aftur á heimasíðuna.</span><span class="sxs-lookup"><span data-stu-id="729f4-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="729f4-123">Stofna stefnureglugerðir fyrir reikninga lánardrottins</span><span class="sxs-lookup"><span data-stu-id="729f4-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="729f4-124">Farðu Í **Skoðunarrúðu > Einingar > Viðskiptaskuldir > Regluuppsetning > Reglugerðir reiknings lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="729f4-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="729f4-125">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="729f4-125">Select **New**.</span></span>
3. <span data-ttu-id="729f4-126">Færið inn gildi í reitina **Heiti reglu** og **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="729f4-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="729f4-127">Í reitnum **Fyrirspurnarheiti** veldu fellivalmyndina til að opna leitina og veldu síðan viðeigandi skrá.</span><span class="sxs-lookup"><span data-stu-id="729f4-127">In the **Query name** field, select the drop-down button to open the lookup, then selec the desired record.</span></span>
5. <span data-ttu-id="729f4-128">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="729f4-128">Select **Save**.</span></span>
6. <span data-ttu-id="729f4-129">Lokið síðunni til að fara aftur á heimasíðuna.</span><span class="sxs-lookup"><span data-stu-id="729f4-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="729f4-130">Skilgreina stefna fyrir reikning lánardrottins</span><span class="sxs-lookup"><span data-stu-id="729f4-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="729f4-131">Farðu Í **Skoðunarrúðu > Einingar > Viðskiptaskuldir > Regluuppsetning > Reikningrelgur lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="729f4-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="729f4-132">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="729f4-132">Select **New**.</span></span>
3. <span data-ttu-id="729f4-133">Færið inn gildi í reitina **Heiti** og **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="729f4-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="729f4-134">Útvíkka eða draga saman hlutann **fyrirtækisregla**.</span><span class="sxs-lookup"><span data-stu-id="729f4-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="729f4-135">Í trénu skal velja **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="729f4-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="729f4-136">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="729f4-136">Select **Add**.</span></span>
7. <span data-ttu-id="729f4-137">Útvíkka eða draga saman hlutann **stefnuregla**.</span><span class="sxs-lookup"><span data-stu-id="729f4-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="729f4-138">Veldu **stefnureglu**.</span><span class="sxs-lookup"><span data-stu-id="729f4-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="729f4-139">í reitnum **Lýsing stefnuregla** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="729f4-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="729f4-140">Velja **Síu**.</span><span class="sxs-lookup"><span data-stu-id="729f4-140">Select **Filter**.</span></span>
11. <span data-ttu-id="729f4-141">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="729f4-141">Select **Add**.</span></span> <span data-ttu-id="729f4-142">Velja virku æskilega skrá.</span><span class="sxs-lookup"><span data-stu-id="729f4-142">Select the desired record.</span></span>
12. <span data-ttu-id="729f4-143">Í reitunum **Tafla**, **Afleidd tafla**, og **Reitur**, veldu eða sláðu inn valkosti í fellivalmyndunum.</span><span class="sxs-lookup"><span data-stu-id="729f4-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="729f4-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="729f4-144">Close the page.</span></span>
14. <span data-ttu-id="729f4-145">Í reitnum **Skilyrði** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="729f4-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="729f4-146">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="729f4-146">Select **OK**.</span></span>
16. <span data-ttu-id="729f4-147">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="729f4-147">Select **OK**.</span></span>
17. <span data-ttu-id="729f4-148">Lokið síðunum til að fara aftur á heimasíðuna.</span><span class="sxs-lookup"><span data-stu-id="729f4-148">Close the pages to return to the home page.</span></span>

