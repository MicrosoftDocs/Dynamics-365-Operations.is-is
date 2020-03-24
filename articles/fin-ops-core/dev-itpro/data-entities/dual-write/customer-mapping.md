---
title: Samþættur aðalviðskiptavinur
description: Þetta efni lýsir samþættingu viðskiptavinaupplýsinga milli Finance and Operations og Common Data Service.
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
ms.openlocfilehash: 269346d38eeb3812c352d16f9d50fbcd09307c12
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124590"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="21a75-103">Samþættur aðalviðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="21a75-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="21a75-104">Það er dæmigert að skrár viðskiptavina nái tökum á fleiri en einu forriti.</span><span class="sxs-lookup"><span data-stu-id="21a75-104">It's typical for customer records to be mastered in more than one application.</span></span> <span data-ttu-id="21a75-105">Til dæmis getur sölustarfsemi komið með viðskiptamannaskrár í gegnum söluforrit og rafræn viðskipti eða smásala geta komið með viðskiptavinaskrár í gegnum forritið Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="21a75-105">For example, sales activity can bring in commercial customer records through a Sales application, and e-Commerce or retail sales can bring in customer records through a Finance and Operations application.</span></span> <span data-ttu-id="21a75-106">Óháð því hvaðan viðskiptavinaskráin er upprunnin, þá er hún samþætt bak við tjöldin þvert á forritamörk og mismun á innviðum.</span><span class="sxs-lookup"><span data-stu-id="21a75-106">Regardless of where the customer record originates, it's integrated behind the scenes across application boundaries and infrastructure differences.</span></span> <span data-ttu-id="21a75-107">Að ná tökum á samþættum viðskiptavini hjálpar til við að takast á við margvíslega atburðarás og veitir yfirgripsmikla sýn á viðskiptavininn í Dynamics 365 forritasvítunni.</span><span class="sxs-lookup"><span data-stu-id="21a75-107">Integrated customer mastering helps handle multi-mastering scenarios and provides a comprehensive view of the customer to the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="21a75-108">Gagnaflæði viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="21a75-108">Customer data flow</span></span>

<span data-ttu-id="21a75-109">*Viðskiptavinur* er vel skilgreint hugtak í forritum.</span><span class="sxs-lookup"><span data-stu-id="21a75-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="21a75-110">Þess vegna felur samþætting gagna viðskiptavina bara í sér að samræma viðskiptavinahugtakið milli forritanna tveggja.</span><span class="sxs-lookup"><span data-stu-id="21a75-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="21a75-111">Eftirfarandi skýringarmynd sýnir gagnaflæði viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="21a75-111">The following illustration shows the customer data flow.</span></span>

![Gagnaflæði viðskiptavinar](media/dual-write-customer-data-flow.png)

<span data-ttu-id="21a75-113">Viðskiptavini er hægt að flokka í stórum dráttum í tvær gerðir: viðskiptamenn/fyrirtækjaviðskiptavini og neytendur/endanotendur.</span><span class="sxs-lookup"><span data-stu-id="21a75-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="21a75-114">Þessar tvær tegundir viðskiptavina eru geymdar og meðhöndlaðar á annan hátt í Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="21a75-114">These two types of customers are stored and handled differently in Finance and Operations and Common Data Service.</span></span>

<span data-ttu-id="21a75-115">Í Finance and Operations eru bæði viðskiptamenn/fyrirtækjaviðskiptamenn og neytendur/endanotendur þjálfaðir í að ná tökum á einni töflu sem er nefnd **CustTable** (CustomerCustomerV3Entity), og þeir eru flokkaðir eftir eigindinu **Gerð**.</span><span class="sxs-lookup"><span data-stu-id="21a75-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustomerCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="21a75-116">(Ef **Gerð** er stillt á **Fyrirtæki** er viðskiptavinurinn viðskiptamaður/fyrirtækjaviðskiptavinur og ef **Gerð** er stillt á **Einstaklingur** er viðskiptavinurinn neytandi/notandi.) Aðalupplýsingar tengiliða eru meðhöndlaðar í gegnum SMMContactPersonEntity eininguna.</span><span class="sxs-lookup"><span data-stu-id="21a75-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="21a75-117">Í Common Data Service eru viðskiptaenn/fyrirtækjaviðskiptavinir þjálfaðir í lykileiningunni og eru auðkenndir sem viðskiptavinir þegar eigindin **Gerð vensla** er stillt á **Viðskiptavinur**.</span><span class="sxs-lookup"><span data-stu-id="21a75-117">In Common Data Service, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="21a75-118">Bæði neytendur/notendur og tengiliður eiga fulltrúa fyrir tengiliðinn.</span><span class="sxs-lookup"><span data-stu-id="21a75-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="21a75-119">Til að veita skýran aðskilnað milli neytenda/endanotanda og tengiliðs er einingin **Hafðu samband** með Boole-flöggun sem er nefnd **Seljanlegt**.</span><span class="sxs-lookup"><span data-stu-id="21a75-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="21a75-120">Þegar **Seljanlegt** er **Satt** er tengiliðurinn neytandi/notandi og hægt er að búa til tilvitnanir og pantanir fyrir þann tengilið.</span><span class="sxs-lookup"><span data-stu-id="21a75-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="21a75-121">Þegar **Seljanlegt** er **Rangt** er tengiliðurinn er bara aðaltengiliður viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="21a75-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="21a75-122">Þegar tengiliður sem ekki er seljanlegur tekur þátt í tilboði eða pöntunarferli er **Seljanlegt** stillt á **Satt** til að merkja tengiliðinn sem seljanlegan tengilið.</span><span class="sxs-lookup"><span data-stu-id="21a75-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="21a75-123">Tengiliður sem hefur orðið seljanlegur tengiliður er áfram seljanlegur tengiliður.</span><span class="sxs-lookup"><span data-stu-id="21a75-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="21a75-124">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="21a75-124">Templates</span></span>

<span data-ttu-id="21a75-125">Viðskiptavinagögn innihalda allar upplýsingar um viðskiptavininn, svo sem viðskiptavinahópinn, heimilisföng, tengiliðaupplýsingar, greiðslusnið, reikningssnið og vildarstöðu.</span><span class="sxs-lookup"><span data-stu-id="21a75-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="21a75-126">Safn af einingakortum virka saman á meðan samskipti við viðskiptavini eru í gangi, eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="21a75-126">A collection of entity maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="21a75-127">Finance and Operations-smáforrit</span><span class="sxs-lookup"><span data-stu-id="21a75-127">Finance and Operations apps</span></span> | <span data-ttu-id="21a75-128">Önnur Dynamics 365 forrit</span><span class="sxs-lookup"><span data-stu-id="21a75-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="21a75-129">Lýsing</span><span class="sxs-lookup"><span data-stu-id="21a75-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="21a75-130">Tengiliðir fyrir skuldatryggingu V2</span><span class="sxs-lookup"><span data-stu-id="21a75-130">CDS Contacts V2</span></span>             | <span data-ttu-id="21a75-131">tengiliðir</span><span class="sxs-lookup"><span data-stu-id="21a75-131">contacts</span></span>                        | <span data-ttu-id="21a75-132">Þetta sniðmát samstillir allar aðal-, aðrar og þriðju tengiliðaupplýsingar, bæði fyrir viðskiptavini og framleiðendur.</span><span class="sxs-lookup"><span data-stu-id="21a75-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="21a75-133">Viðskiptavinaflokkar</span><span class="sxs-lookup"><span data-stu-id="21a75-133">Customer groups</span></span>             | <span data-ttu-id="21a75-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="21a75-134">msdyn_customergroups</span></span>            | <span data-ttu-id="21a75-135">Þetta sniðmát samstillir upplýsingar um hóp viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="21a75-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="21a75-136">Greiðslumáti viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="21a75-136">Customer payment method</span></span>     | <span data-ttu-id="21a75-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="21a75-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="21a75-138">Þetta sniðmát samstillir upplýsingar um greiðslumáta viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="21a75-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="21a75-139">Viðskiptavinir V3</span><span class="sxs-lookup"><span data-stu-id="21a75-139">Customers V3</span></span>                | <span data-ttu-id="21a75-140">lyklar</span><span class="sxs-lookup"><span data-stu-id="21a75-140">accounts</span></span>                        | <span data-ttu-id="21a75-141">Þetta sniðmát samstillir aðalupplýsingar viðskiptavina fyrir viðskiptamenn og fyrirtækjaviðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="21a75-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="21a75-142">Viðskiptavinir V3</span><span class="sxs-lookup"><span data-stu-id="21a75-142">Customers V3</span></span>                | <span data-ttu-id="21a75-143">tengiliðir</span><span class="sxs-lookup"><span data-stu-id="21a75-143">contacts</span></span>                        | <span data-ttu-id="21a75-144">Þetta sniðmát samstillir aðalgögn viðskiptavina fyrir neytendur og endanotendur.</span><span class="sxs-lookup"><span data-stu-id="21a75-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="21a75-145">Vildarkort</span><span class="sxs-lookup"><span data-stu-id="21a75-145">Loyalty card</span></span>                | <span data-ttu-id="21a75-146">msdyn_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="21a75-146">msdyn_loyaltycards</span></span>              | <span data-ttu-id="21a75-147">Þetta sniðmát samstillir upplýsingar um vildarkort viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="21a75-147">This template synchronizes customer loyalty card information.</span></span>
<span data-ttu-id="21a75-148">Viðskeyti nafna</span><span class="sxs-lookup"><span data-stu-id="21a75-148">Name affixes</span></span>                | <span data-ttu-id="21a75-149">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="21a75-149">msdyn_nameaffixes</span></span>               | <span data-ttu-id="21a75-150">Þetta sniðmát samstillir tilvísunargögn nafnaviðskeyta, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="21a75-150">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="21a75-151">Greiðsludagalínur CDS V2</span><span class="sxs-lookup"><span data-stu-id="21a75-151">Payment day lines CDS V2</span></span>    | <span data-ttu-id="21a75-152">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="21a75-152">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="21a75-153">Þetta sniðmát samstillir tilvísunargögn greiðsludagalína, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="21a75-153">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="21a75-154">Greiðsludagar CDS</span><span class="sxs-lookup"><span data-stu-id="21a75-154">Payment days CDS</span></span>            | <span data-ttu-id="21a75-155">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="21a75-155">msdyn_paymentdays</span></span>               | <span data-ttu-id="21a75-156">Þetta sniðmát samstillir tilvísunargögn greiðsludaga, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="21a75-156">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="21a75-157">Greiðsluáætlunarlínur</span><span class="sxs-lookup"><span data-stu-id="21a75-157">Payment schedule lines</span></span>      | <span data-ttu-id="21a75-158">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="21a75-158">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="21a75-159">Samstillir tilvísunargögn greiðsluáætlunarlína, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="21a75-159">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="21a75-160">Greiðsluáætlun</span><span class="sxs-lookup"><span data-stu-id="21a75-160">Payment schedule</span></span>            | <span data-ttu-id="21a75-161">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="21a75-161">msdyn_paymentschedules</span></span>          | <span data-ttu-id="21a75-162">Þetta sniðmát samstillir tilvísunargögn greiðsluáætlunar, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="21a75-162">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="21a75-163">Greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="21a75-163">Terms of payment</span></span>            | <span data-ttu-id="21a75-164">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="21a75-164">msdyn_paymentterms</span></span>              | <span data-ttu-id="21a75-165">Þetta sniðmát samstillir tilvísunargögn greiðsluskilmála (skilmála greiðslu), bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="21a75-165">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
