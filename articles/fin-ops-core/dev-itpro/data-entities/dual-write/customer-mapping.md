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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 36716c302d86bc5715798bf4cf4899f666d0872c
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997455"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="66777-103">Samþættur aðalviðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="66777-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="66777-104">Hægt er að ná góðum tökum á gögnum viðskiptavina í fleiri en einu Dynamics 365 forriti.</span><span class="sxs-lookup"><span data-stu-id="66777-104">Customer data can be mastered in more than one Dynamics 365 application.</span></span> <span data-ttu-id="66777-105">Til dæmis getur viðskiptavinaskrá átt uppruna sinn í söluaðgerðum í Dynamics 365 Sales (líkanadrifnu forriti í Dynamics 365), eða færsla getur átt uppruna sinn í smásöluaðgerðum í Dynamics 365 Commerce (forriti í Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="66777-105">For example, a customer record can originate though sales activity in Dynamics 365 Sales (a model-driven app in Dynamics 365), or a record can originate through retail activity in Dynamics 365 Commerce (a Finance and Operations app).</span></span> <span data-ttu-id="66777-106">Óháð því hvaðan viðskiptavinagögnin eiga uppruna sinn eru þau samofin bak við tjöldin.</span><span class="sxs-lookup"><span data-stu-id="66777-106">No matter where where the customer data originates, it is integrated behind the scenes.</span></span> <span data-ttu-id="66777-107">Innbyggður viðskiptavinameistari veitir þér sveigjanleika til að ná góðum tökum á gögnum viðskiptavina í hvaða Dynamics 365 forriti sem er og gefur yfirgripsmikla sýn yfir viðskiptavininn í Dynamics 365 forritssvítunni.</span><span class="sxs-lookup"><span data-stu-id="66777-107">Integrated customer master gives you the flexibility to master customer data in any Dynamics 365 application and provides a comprehensive view of the customer across the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="66777-108">Gagnaflæði viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="66777-108">Customer data flow</span></span>

<span data-ttu-id="66777-109">*Viðskiptavinur* er vel skilgreint hugtak í forritum.</span><span class="sxs-lookup"><span data-stu-id="66777-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="66777-110">Þess vegna felur samþætting gagna viðskiptavina bara í sér að samræma viðskiptavinahugtakið milli forritanna tveggja.</span><span class="sxs-lookup"><span data-stu-id="66777-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="66777-111">Eftirfarandi skýringarmynd sýnir gagnaflæði viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="66777-111">The following illustration shows the customer data flow.</span></span>

![Gagnaflæði viðskiptavinar](media/dual-write-customer-data-flow.png)

<span data-ttu-id="66777-113">Viðskiptavini er hægt að flokka í stórum dráttum í tvær gerðir: viðskiptamenn/fyrirtækjaviðskiptavini og neytendur/endanotendur.</span><span class="sxs-lookup"><span data-stu-id="66777-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="66777-114">Þessar tvær tegundir viðskiptavina eru geymdar og meðhöndlaðar á annan hátt í Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="66777-114">These two types of customers are stored and handled differently in Finance and Operations and Common Data Service.</span></span>

<span data-ttu-id="66777-115">Í Finance and Operations eru bæði viðskiptavinir verslunar/fyrirtækis og neytendur/endanotendur í einni töflu sem nefnist **CustTable** (CustCustomerV3Entity) og eru flokkaðir út frá **Gerð** eigindar.</span><span class="sxs-lookup"><span data-stu-id="66777-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="66777-116">(Ef **Gerð** er stillt á **Fyrirtæki** er viðskiptavinurinn viðskiptamaður/fyrirtækjaviðskiptavinur og ef **Gerð** er stillt á **Einstaklingur** er viðskiptavinurinn neytandi/notandi.) Aðalupplýsingar tengiliða eru meðhöndlaðar í gegnum SMMContactPersonEntity eininguna.</span><span class="sxs-lookup"><span data-stu-id="66777-116">(If **Type** is set to **Organization** , the customer is a commercial/organizational customer, and if **Type** is set to **Person** , the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="66777-117">Í Common Data Service eru viðskiptaenn/fyrirtækjaviðskiptavinir þjálfaðir í lykileiningunni og eru auðkenndir sem viðskiptavinir þegar eigindin **Gerð vensla** er stillt á **Viðskiptavinur**.</span><span class="sxs-lookup"><span data-stu-id="66777-117">In Common Data Service, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="66777-118">Bæði neytendur/notendur og tengiliður eiga fulltrúa fyrir tengiliðinn.</span><span class="sxs-lookup"><span data-stu-id="66777-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="66777-119">Til að veita skýran aðskilnað milli neytenda/endanotanda og tengiliðs er einingin **Hafðu samband** með Boole-flöggun sem er nefnd **Seljanlegt**.</span><span class="sxs-lookup"><span data-stu-id="66777-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="66777-120">Þegar **Seljanlegt** er **Satt** er tengiliðurinn neytandi/notandi og hægt er að búa til tilvitnanir og pantanir fyrir þann tengilið.</span><span class="sxs-lookup"><span data-stu-id="66777-120">When **Sellable** is **True** , the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="66777-121">Þegar **Seljanlegt** er **Rangt** er tengiliðurinn er bara aðaltengiliður viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="66777-121">When **Sellable** is **False** , the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="66777-122">Þegar tengiliður sem ekki er seljanlegur tekur þátt í tilboði eða pöntunarferli er **Seljanlegt** stillt á **Satt** til að merkja tengiliðinn sem seljanlegan tengilið.</span><span class="sxs-lookup"><span data-stu-id="66777-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="66777-123">Tengiliður sem hefur orðið seljanlegur tengiliður er áfram seljanlegur tengiliður.</span><span class="sxs-lookup"><span data-stu-id="66777-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="66777-124">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="66777-124">Templates</span></span>

<span data-ttu-id="66777-125">Viðskiptavinagögn innihalda allar upplýsingar um viðskiptavininn, svo sem viðskiptavinahópinn, heimilisföng, tengiliðaupplýsingar, greiðslusnið, reikningssnið og vildarstöðu.</span><span class="sxs-lookup"><span data-stu-id="66777-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="66777-126">Safn af einingakortum virka saman á meðan samskipti við viðskiptavini eru í gangi, eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="66777-126">A collection of entity maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="66777-127">Finance and Operations-smáforrit</span><span class="sxs-lookup"><span data-stu-id="66777-127">Finance and Operations apps</span></span> | <span data-ttu-id="66777-128">Önnur Dynamics 365 forrit</span><span class="sxs-lookup"><span data-stu-id="66777-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="66777-129">Lýsing</span><span class="sxs-lookup"><span data-stu-id="66777-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="66777-130">Tengiliðir fyrir skuldatryggingu V2</span><span class="sxs-lookup"><span data-stu-id="66777-130">CDS Contacts V2</span></span>             | <span data-ttu-id="66777-131">tengiliðir</span><span class="sxs-lookup"><span data-stu-id="66777-131">contacts</span></span>                        | <span data-ttu-id="66777-132">Þetta sniðmát samstillir allar aðal-, aðrar og þriðju tengiliðaupplýsingar, bæði fyrir viðskiptavini og framleiðendur.</span><span class="sxs-lookup"><span data-stu-id="66777-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="66777-133">Viðskiptavinaflokkar</span><span class="sxs-lookup"><span data-stu-id="66777-133">Customer groups</span></span>             | <span data-ttu-id="66777-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="66777-134">msdyn_customergroups</span></span>            | <span data-ttu-id="66777-135">Þetta sniðmát samstillir upplýsingar um hóp viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="66777-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="66777-136">Greiðslumáti viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="66777-136">Customer payment method</span></span>     | <span data-ttu-id="66777-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="66777-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="66777-138">Þetta sniðmát samstillir upplýsingar um greiðslumáta viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="66777-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="66777-139">Viðskiptavinir V3</span><span class="sxs-lookup"><span data-stu-id="66777-139">Customers V3</span></span>                | <span data-ttu-id="66777-140">lyklar</span><span class="sxs-lookup"><span data-stu-id="66777-140">accounts</span></span>                        | <span data-ttu-id="66777-141">Þetta sniðmát samstillir aðalupplýsingar viðskiptavina fyrir viðskiptamenn og fyrirtækjaviðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="66777-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="66777-142">Viðskiptavinir V3</span><span class="sxs-lookup"><span data-stu-id="66777-142">Customers V3</span></span>                | <span data-ttu-id="66777-143">tengiliðir</span><span class="sxs-lookup"><span data-stu-id="66777-143">contacts</span></span>                        | <span data-ttu-id="66777-144">Þetta sniðmát samstillir aðalgögn viðskiptavina fyrir neytendur og endanotendur.</span><span class="sxs-lookup"><span data-stu-id="66777-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="66777-145">Viðskeyti nafna</span><span class="sxs-lookup"><span data-stu-id="66777-145">Name affixes</span></span>                | <span data-ttu-id="66777-146">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="66777-146">msdyn_nameaffixes</span></span>               | <span data-ttu-id="66777-147">Þetta sniðmát samstillir tilvísunargögn nafnaviðskeyta, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="66777-147">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="66777-148">Greiðsludagalínur CDS V2</span><span class="sxs-lookup"><span data-stu-id="66777-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="66777-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="66777-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="66777-150">Þetta sniðmát samstillir tilvísunargögn greiðsludagalína, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="66777-150">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="66777-151">Greiðsludagar CDS</span><span class="sxs-lookup"><span data-stu-id="66777-151">Payment days CDS</span></span>            | <span data-ttu-id="66777-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="66777-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="66777-153">Þetta sniðmát samstillir tilvísunargögn greiðsludaga, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="66777-153">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="66777-154">Greiðsluáætlunarlínur</span><span class="sxs-lookup"><span data-stu-id="66777-154">Payment schedule lines</span></span>      | <span data-ttu-id="66777-155">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="66777-155">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="66777-156">Samstillir tilvísunargögn greiðsluáætlunarlína, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="66777-156">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="66777-157">Greiðsluáætlun</span><span class="sxs-lookup"><span data-stu-id="66777-157">Payment schedule</span></span>            | <span data-ttu-id="66777-158">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="66777-158">msdyn_paymentschedules</span></span>          | <span data-ttu-id="66777-159">Þetta sniðmát samstillir tilvísunargögn greiðsluáætlunar, bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="66777-159">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="66777-160">Greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="66777-160">Terms of payment</span></span>            | <span data-ttu-id="66777-161">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="66777-161">msdyn_paymentterms</span></span>              | <span data-ttu-id="66777-162">Þetta sniðmát samstillir tilvísunargögn greiðsluskilmála (skilmála greiðslu), bæði fyrir viðskiptavini og lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="66777-162">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

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
