---
title: Samþættur aðalviðskiptavinur
description: Þetta efni lýsir samþættingu viðskiptavinaupplýsinga milli Finance and Operations og Dataverse.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 801538e320ca78b0cc55bb4e4b8a80d38b9b48d6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685640"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="e90e3-103">Samþættur aðalviðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="e90e3-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="e90e3-104">Hægt er að ná góðum tökum á gögnum viðskiptavina í fleiri en einu Dynamics 365 forriti.</span><span class="sxs-lookup"><span data-stu-id="e90e3-104">Customer data can be mastered in more than one Dynamics 365 application.</span></span> <span data-ttu-id="e90e3-105">Til dæmis getur viðskiptavinarlína átt uppruna í söluverkþætti í Dynamics 365 Sales (líkanaknúið forrit í Dynamics 365) eða þá að lína getur átt uppruna sinn í smásöluaðgerð Dynamics 365 Commerce (Finance and Operations-forrit).</span><span class="sxs-lookup"><span data-stu-id="e90e3-105">For example, a customer row can originate though sales activity in Dynamics 365 Sales (a model-driven app in Dynamics 365), or a row can originate through retail activity in Dynamics 365 Commerce (a Finance and Operations app).</span></span> <span data-ttu-id="e90e3-106">Óháð því hvaðan viðskiptavinagögnin eiga uppruna sinn eru þau samofin bak við tjöldin.</span><span class="sxs-lookup"><span data-stu-id="e90e3-106">No matter where where the customer data originates, it is integrated behind the scenes.</span></span> <span data-ttu-id="e90e3-107">Innbyggður viðskiptavinameistari veitir þér sveigjanleika til að ná góðum tökum á gögnum viðskiptavina í hvaða Dynamics 365 forriti sem er og gefur yfirgripsmikla sýn yfir viðskiptavininn í Dynamics 365 forritssvítunni.</span><span class="sxs-lookup"><span data-stu-id="e90e3-107">Integrated customer master gives you the flexibility to master customer data in any Dynamics 365 application and provides a comprehensive view of the customer across the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="e90e3-108">Gagnaflæði viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="e90e3-108">Customer data flow</span></span>

<span data-ttu-id="e90e3-109">*Viðskiptavinur* er vel skilgreint hugtak í forritum.</span><span class="sxs-lookup"><span data-stu-id="e90e3-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="e90e3-110">Þess vegna felur samþætting gagna viðskiptavina bara í sér að samræma viðskiptavinahugtakið milli forritanna tveggja.</span><span class="sxs-lookup"><span data-stu-id="e90e3-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="e90e3-111">Eftirfarandi skýringarmynd sýnir gagnaflæði viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="e90e3-111">The following illustration shows the customer data flow.</span></span>

![Gagnaflæði viðskiptavinar](media/dual-write-customer-data-flow.png)

<span data-ttu-id="e90e3-113">Viðskiptavini er hægt að flokka í stórum dráttum í tvær gerðir: viðskiptamenn/fyrirtækjaviðskiptavini og neytendur/endanotendur.</span><span class="sxs-lookup"><span data-stu-id="e90e3-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="e90e3-114">Þessar tvær tegundir viðskiptavina eru geymdar og meðhöndlaðar á annan hátt í Finance and Operations og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e90e3-114">These two types of customers are stored and handled differently in Finance and Operations and Dataverse.</span></span>

<span data-ttu-id="e90e3-115">Í Finance and Operations eru bæði viðskiptavinir verslunar/fyrirtækis og neytendur/endanotendur í einni töflu sem nefnist **CustTable** (CustCustomerV3Entity) og eru flokkaðir út frá **Gerð** eigindar.</span><span class="sxs-lookup"><span data-stu-id="e90e3-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="e90e3-116">(Ef **Gerð** er stillt á **Fyrirtæki** er viðskiptavinurinn viðskiptamaður/fyrirtækjaviðskiptavinur og ef **Gerð** er stillt á **Einstaklingur** er viðskiptavinurinn neytandi/notandi.) Aðalupplýsingar tengiliða eru meðhöndlaðar í gegnum SMMContactPersonEntity eininguna.</span><span class="sxs-lookup"><span data-stu-id="e90e3-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="e90e3-117">Í Dataverse eru viðskiptaenn/fyrirtækjaviðskiptavinir þjálfaðir í lykileiningunni og eru auðkenndir sem viðskiptavinir þegar eigindin **Gerð vensla** er stillt á **Viðskiptavinur**.</span><span class="sxs-lookup"><span data-stu-id="e90e3-117">In Dataverse, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="e90e3-118">Bæði neytendur/notendur og tengiliður eiga fulltrúa fyrir tengiliðinn.</span><span class="sxs-lookup"><span data-stu-id="e90e3-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="e90e3-119">Til að veita skýran aðskilnað milli neytenda/endanotanda og tengiliðs er einingin **Hafðu samband** með Boole-flöggun sem er nefnd **Seljanlegt**.</span><span class="sxs-lookup"><span data-stu-id="e90e3-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="e90e3-120">Þegar **Seljanlegt** er **Satt** er tengiliðurinn neytandi/notandi og hægt er að búa til tilvitnanir og pantanir fyrir þann tengilið.</span><span class="sxs-lookup"><span data-stu-id="e90e3-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="e90e3-121">Þegar **Seljanlegt** er **Rangt** er tengiliðurinn er bara aðaltengiliður viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="e90e3-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="e90e3-122">Þegar tengiliður sem ekki er seljanlegur tekur þátt í tilboði eða pöntunarferli er **Seljanlegt** stillt á **Satt** til að merkja tengiliðinn sem seljanlegan tengilið.</span><span class="sxs-lookup"><span data-stu-id="e90e3-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="e90e3-123">Tengiliður sem hefur orðið seljanlegur tengiliður er áfram seljanlegur tengiliður.</span><span class="sxs-lookup"><span data-stu-id="e90e3-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="e90e3-124">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="e90e3-124">Templates</span></span>

<span data-ttu-id="e90e3-125">Viðskiptavinagögn innihalda allar upplýsingar um viðskiptavininn, svo sem viðskiptavinahópinn, heimilisföng, tengiliðaupplýsingar, greiðslusnið, reikningssnið og vildarstöðu.</span><span class="sxs-lookup"><span data-stu-id="e90e3-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="e90e3-126">Safn af töflukortum vinna saman í gagnasamskiptum viðskiptavinar, eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="e90e3-126">A collection of table maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="e90e3-127">Finance and Operations-smáforrit</span><span class="sxs-lookup"><span data-stu-id="e90e3-127">Finance and Operations apps</span></span> | <span data-ttu-id="e90e3-128">Önnur Dynamics 365 forrit</span><span class="sxs-lookup"><span data-stu-id="e90e3-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="e90e3-129">Lýsing</span><span class="sxs-lookup"><span data-stu-id="e90e3-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="e90e3-130">Tengiliðir fyrir skuldatryggingu V2</span><span class="sxs-lookup"><span data-stu-id="e90e3-130">CDS Contacts V2</span></span>             | <span data-ttu-id="e90e3-131">tengiliðir</span><span class="sxs-lookup"><span data-stu-id="e90e3-131">contacts</span></span>                        | <span data-ttu-id="e90e3-132">Þetta sniðmát samstillir allar aðal-, aðrar og þriðju tengiliðaupplýsingar, bæði fyrir viðskiptavini og framleiðendur.</span><span class="sxs-lookup"><span data-stu-id="e90e3-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="e90e3-133">Viðskiptavinaflokkar</span><span class="sxs-lookup"><span data-stu-id="e90e3-133">Customer groups</span></span>             | <span data-ttu-id="e90e3-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="e90e3-134">msdyn_customergroups</span></span>            | <span data-ttu-id="e90e3-135">Þetta sniðmát samstillir upplýsingar um hóp viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="e90e3-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="e90e3-136">Greiðslumáti viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="e90e3-136">Customer payment method</span></span>     | <span data-ttu-id="e90e3-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="e90e3-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="e90e3-138">Þetta sniðmát samstillir upplýsingar um greiðslumáta viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="e90e3-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="e90e3-139">Viðskiptavinir V3</span><span class="sxs-lookup"><span data-stu-id="e90e3-139">Customers V3</span></span>                | <span data-ttu-id="e90e3-140">lyklar</span><span class="sxs-lookup"><span data-stu-id="e90e3-140">accounts</span></span>                        | <span data-ttu-id="e90e3-141">Þetta sniðmát samstillir aðalupplýsingar viðskiptavina fyrir viðskiptamenn og fyrirtækjaviðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="e90e3-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="e90e3-142">Viðskiptavinir V3</span><span class="sxs-lookup"><span data-stu-id="e90e3-142">Customers V3</span></span>                | <span data-ttu-id="e90e3-143">tengiliðir</span><span class="sxs-lookup"><span data-stu-id="e90e3-143">contacts</span></span>                        | <span data-ttu-id="e90e3-144">Þetta sniðmát samstillir aðalgögn viðskiptavina fyrir neytendur og endanotendur.</span><span class="sxs-lookup"><span data-stu-id="e90e3-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="e90e3-145">Viðskeyti nafna</span><span class="sxs-lookup"><span data-stu-id="e90e3-145">Name affixes</span></span>                | <span data-ttu-id="e90e3-146">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="e90e3-146">msdyn_nameaffixes</span></span>               | <span data-ttu-id="e90e3-147">Þetta sniðmát samstillir tilvísunargögn nafnaviðskeyta, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="e90e3-147">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="e90e3-148">Greiðsludagalínur CDS V2</span><span class="sxs-lookup"><span data-stu-id="e90e3-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="e90e3-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="e90e3-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="e90e3-150">Þetta sniðmát samstillir tilvísunargögn greiðsludagalína, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="e90e3-150">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="e90e3-151">Greiðsludagar CDS</span><span class="sxs-lookup"><span data-stu-id="e90e3-151">Payment days CDS</span></span>            | <span data-ttu-id="e90e3-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="e90e3-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="e90e3-153">Þetta sniðmát samstillir tilvísunargögn greiðsludaga, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="e90e3-153">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="e90e3-154">Greiðsluáætlunarlínur</span><span class="sxs-lookup"><span data-stu-id="e90e3-154">Payment schedule lines</span></span>      | <span data-ttu-id="e90e3-155">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="e90e3-155">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="e90e3-156">Samstillir tilvísunargögn greiðsluáætlunarlína, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="e90e3-156">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="e90e3-157">Greiðsluáætlun</span><span class="sxs-lookup"><span data-stu-id="e90e3-157">Payment schedule</span></span>            | <span data-ttu-id="e90e3-158">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="e90e3-158">msdyn_paymentschedules</span></span>          | <span data-ttu-id="e90e3-159">Þetta sniðmát samstillir tilvísunargögn greiðsluáætlunar, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="e90e3-159">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="e90e3-160">Greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="e90e3-160">Terms of payment</span></span>            | <span data-ttu-id="e90e3-161">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="e90e3-161">msdyn_paymentterms</span></span>              | <span data-ttu-id="e90e3-162">Þetta sniðmát samstillir tilvísunargögn greiðsluskilmála (skilmála greiðslu), bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="e90e3-162">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
