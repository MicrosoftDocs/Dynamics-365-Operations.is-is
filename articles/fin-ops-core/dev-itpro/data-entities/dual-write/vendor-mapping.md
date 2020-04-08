---
title: Samþætt vinna með lánardrottinssniðmát
description: Þetta efni lýsir samþættingu lánardrottnagagna milli forrita Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 2442a6869daac22a435c1a7504b93ea4b5c14747
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019834"
---
# <a name="integrated-vendor-master"></a><span data-ttu-id="c0cbe-103">Samþætt vinna með lánardrottinssniðmát</span><span class="sxs-lookup"><span data-stu-id="c0cbe-103">Integrated vendor master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="c0cbe-104">Hugtakið *Lánardrottinn* á við birgðasamtök eða einkaeigu sem er hluti af aðfangakeðjuferlinu og veitir vörur fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-104">The term *vendor* refers to a supplier organization or a sole proprietor that is part of the supply chain process, and that supplies goods for the business.</span></span> <span data-ttu-id="c0cbe-105">Þó að *Lánardrottinn* sé rótgróið hugtak í forritum Finance and Operations er hugtakið lánardrottinn ekki til í öðrum forritum Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-105">Although *vendor* is an established concept in Finance and Operations apps, a vendor concept doesn't exist in other Dynamics 365 apps.</span></span> <span data-ttu-id="c0cbe-106">Þess í stað, yfirhlaða sum fyrirtæki lykileininguna til að geyma bæði viðskiptavinaupplýsingar og upplýsingar um lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-106">Instead, some businesses overload the Account entity to store both customer information and vendor information.</span></span> <span data-ttu-id="c0cbe-107">Önnur fyrirtæki nota sérsniðið lánardrottinshugtak.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-107">Other businesses use a custom vendor concept.</span></span> <span data-ttu-id="c0cbe-108">Common Data Service samþætting styður bæði þessa hönnun.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-108">Common Data Service integration supports both these designs.</span></span> <span data-ttu-id="c0cbe-109">Þess vegna geturðu virkjað aðra hvora hönnunina, allt eftir aðstæðum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-109">Therefore, you can enable either of the designs, depending on your business scenario.</span></span>

<span data-ttu-id="c0cbe-110">Sameining gagna lánardrottins milli forrita Finance and Operations og annarra forrita Dynamics 365 gerir þér kleift að ná góðum tökum á gögnunum.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-110">Integration of vendor data between Finance and Operations apps and other Dynamics 365 apps lets you multi-master the data.</span></span> <span data-ttu-id="c0cbe-111">Óháð því hvaðan lánardrottnagögnin eru upprunnin, þá eru þau samþætt bak við tjöldin þvert á forritamörk og mismun á innviðum.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-111">Regardless of where the vendor data originates, it's integrated behind the scenes across application boundaries and infrastructure differences.</span></span> 

### <a name="vendor-data-flow"></a><span data-ttu-id="c0cbe-112">Gagnaflæði lánardrottins</span><span class="sxs-lookup"><span data-stu-id="c0cbe-112">Vendor data flow</span></span>

<span data-ttu-id="c0cbe-113">Ef þú vilt nota önnur forrit Dynamics 365 við stjórnun lánardrottins og þú vilt einangra upplýsingar seljanda frá upplýsingum viðskiptavinarins, geturðu notað nýja lánardrottinshönnunina.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-113">If you want to use other Dynamics 365 apps for vendor mastering, and you want to isolate vendor information from customer information, you can use the new vendor design.</span></span>

![Gagnaflæði lánardrottins](media/dual-write-vendor-data-flow.png)

<span data-ttu-id="c0cbe-115">Ef þú vilt nota önnur forrit Dynamics 365 við stjórnun lánardrottins og þú vilt halda áfram að nota lyklaeininguna til að geyma upplýsingar lánardrottins geturðu notað nýju útvíkkuðu lánardrottinshönnunina.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-115">If you want to use other Dynamics 365 apps for vendor mastering, and you want to continue to use the Account entity to store vendor information, you can use the new extended vendor design.</span></span> <span data-ttu-id="c0cbe-116">Í þessari hönnun eru útvíkkaðar upplýsingar um lánardrottinn, svo sem lánardrottnahópinn og bókunarforstillingar lánardrottins, geymdar í smáatriðum lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-116">In this design, extended vendor information, such as the vendor group and vendor posting profile, are stored in the vendor detail.</span></span>

![Útvíkkað gagnaflæði lánardrottins](media/dual-write-vendor-detail.jpg)

<span data-ttu-id="c0cbe-118">Tengiliðsupplýsingar lánardrottins líkjast tengiliðsupplýsingum viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-118">Vendor contact information resembles customer contact information.</span></span> <span data-ttu-id="c0cbe-119">Bak við tjöldin eru upplýsingar tengiliðar vistaðar og sóttar frá sömu einingum.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-119">Behind the scenes, the contact person's information is stored and retrieved from the same entities.</span></span>

## <a name="templates"></a><span data-ttu-id="c0cbe-120">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="c0cbe-120">Templates</span></span>

<span data-ttu-id="c0cbe-121">Lánardrottnagögn innihalda allar upplýsingar um lánardrottinn, svo sem lánardrottnahópinn, heimilisföng, tengiliðaupplýsingar, greiðslusnið og reikningssnið.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-121">Vendor data includes all information about the vendor, such as the vendor group, addresses, contact information, payment profile, and invoice profile.</span></span> <span data-ttu-id="c0cbe-122">Safn af einingakortum virka saman á meðan samskipti við lánardrottna eru í gangi, eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-122">A collection of entity maps work together during vendor data interaction, as shown in the following table.</span></span>

<span data-ttu-id="c0cbe-123">Finance and Operations-smáforrit</span><span class="sxs-lookup"><span data-stu-id="c0cbe-123">Finance and Operations apps</span></span> | <span data-ttu-id="c0cbe-124">Önnur Dynamics 365 forrit</span><span class="sxs-lookup"><span data-stu-id="c0cbe-124">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="c0cbe-125">Lýsing</span><span class="sxs-lookup"><span data-stu-id="c0cbe-125">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="c0cbe-126">Lánardrottinn V2</span><span class="sxs-lookup"><span data-stu-id="c0cbe-126">Vendor V2</span></span>               | <span data-ttu-id="c0cbe-127">Reikningur</span><span class="sxs-lookup"><span data-stu-id="c0cbe-127">Account</span></span> | <span data-ttu-id="c0cbe-128">Fyrirtæki sem nota lyklaeininguna til að geyma upplýsingar um lánardrottna geta haldið áfram að nota hana á sama hátt.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-128">Businesses that use the Account entity to store vendor information can continue to use it in the same way.</span></span> <span data-ttu-id="c0cbe-129">Þau geta einnig nýtt sér yfirlýsta virkni lánardrottins sem kemur vegna samþættingar forrita Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-129">They can also take advantage of the explicit vendor functionality that is coming because of Finance and Operations apps integration.</span></span>
<span data-ttu-id="c0cbe-130">Lánardrottinn V2</span><span class="sxs-lookup"><span data-stu-id="c0cbe-130">Vendor V2</span></span>               | <span data-ttu-id="c0cbe-131">Msdyn\_vendors</span><span class="sxs-lookup"><span data-stu-id="c0cbe-131">Msdyn\_vendors</span></span> | <span data-ttu-id="c0cbe-132">Fyrirtæki sem nota sérsniðna lausn fyrir lánardrottna geta nýtt sér hugtakið tilbúinn lánardrottinn sem er kynntur til sögunnar í Common Data Service vegna samþættingar forrita Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-132">Businesses that use a custom solution for vendors can take advantage of the out-of-box vendor concept that is being introduced in Common Data Service because of Finance and Operations apps integration.</span></span> 
<span data-ttu-id="c0cbe-133">Lánardrottnaflokkar</span><span class="sxs-lookup"><span data-stu-id="c0cbe-133">Vendor groups</span></span> | <span data-ttu-id="c0cbe-134">msdyn_vendorgroups</span><span class="sxs-lookup"><span data-stu-id="c0cbe-134">msdyn_vendorgroups</span></span> | <span data-ttu-id="c0cbe-135">Þetta sniðmát samstillir upplýsingar um hóp lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-135">This template synchronizes vendor group information.</span></span>
<span data-ttu-id="c0cbe-136">Greiðsluháttur lánardrottins</span><span class="sxs-lookup"><span data-stu-id="c0cbe-136">Vendor payment method</span></span> | <span data-ttu-id="c0cbe-137">msdyn_vendorpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="c0cbe-137">msdyn_vendorpaymentmethods</span></span> | <span data-ttu-id="c0cbe-138">Þetta sniðmát samstillir upplýsingar um greiðslumáta lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-138">This template synchronizes vendor payment method information.</span></span>
<span data-ttu-id="c0cbe-139">Tengiliðir fyrir skuldatryggingu V2</span><span class="sxs-lookup"><span data-stu-id="c0cbe-139">CDS Contacts V2</span></span>             | <span data-ttu-id="c0cbe-140">tengiliðir</span><span class="sxs-lookup"><span data-stu-id="c0cbe-140">contacts</span></span>                        | <span data-ttu-id="c0cbe-141">[Tengiliða](customer-mapping.md#cds-contacts-v2-to-contacts)-sniðmátið samstillir allar aðal-, aðrar og þriðju tengiliðaupplýsingar, bæði fyrir viðskiptavini og framleiðendur.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-141">The [contacts](customer-mapping.md#cds-contacts-v2-to-contacts) template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="c0cbe-142">Greiðsluáætlunarlínur</span><span class="sxs-lookup"><span data-stu-id="c0cbe-142">Payment schedule lines</span></span>      | <span data-ttu-id="c0cbe-143">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="c0cbe-143">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="c0cbe-144">[Greiðsluáætlunarlínu](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines)-sniðmátið samstillir tilvísunargögn greiðsluáætlunar, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-144">The [payment schedule lines](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) template synchronizes reference data for customers and vendors.</span></span>
<span data-ttu-id="c0cbe-145">Greiðsluáætlun</span><span class="sxs-lookup"><span data-stu-id="c0cbe-145">Payment schedule</span></span>            | <span data-ttu-id="c0cbe-146">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="c0cbe-146">msdyn_paymentschedules</span></span>          | <span data-ttu-id="c0cbe-147">[Greiðsluáætlana](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules)-sniðmátið samstillir tilvísunargögn greiðsluáætlunar, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-147">The [payment schedules](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="c0cbe-148">Greiðsludagalínur CDS V2</span><span class="sxs-lookup"><span data-stu-id="c0cbe-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="c0cbe-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="c0cbe-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="c0cbe-150">[Greiðsludagalínu](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines)-sniðmátið samstillir tilvísunargögn greiðsludagalína fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-150">The [payment day lines](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) template synchronizes payment day lines reference data for customers and vendors.</span></span>
<span data-ttu-id="c0cbe-151">Greiðsludagar CDS</span><span class="sxs-lookup"><span data-stu-id="c0cbe-151">Payment days CDS</span></span>            | <span data-ttu-id="c0cbe-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="c0cbe-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="c0cbe-153">[Greiðsludagar](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays)-sniðmátið samstillir tilvísunargögn greiðsludaga, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-153">The [payment days](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="c0cbe-154">Greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="c0cbe-154">Terms of payment</span></span>            | <span data-ttu-id="c0cbe-155">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="c0cbe-155">msdyn_paymentterms</span></span>              | <span data-ttu-id="c0cbe-156">[Greiðsluskilmála](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms)-sniðmátið samstillir tilvísunargögn greiðsluskilmála (skilmála greiðslu), bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-156">The [terms of payment](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) template synchronizes payment terms reference data, for both customers and vendors.</span></span>
<span data-ttu-id="c0cbe-157">Viðskeyti nafna</span><span class="sxs-lookup"><span data-stu-id="c0cbe-157">Name affixes</span></span>                | <span data-ttu-id="c0cbe-158">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="c0cbe-158">msdyn_nameaffixes</span></span>               | <span data-ttu-id="c0cbe-159">[Heitisviðskeytis](customer-mapping.md#name-affixes-to-msdyn_nameaffixes)-sniðmátið samstillir tilvísunargögn nafnaviðskeyta, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="c0cbe-159">The [name affixes](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) template synchronizes name affixes reference data, for both customers and vendors.</span></span>

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]