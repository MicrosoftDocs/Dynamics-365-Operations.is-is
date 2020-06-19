---
title: Úrræðaleit vandamála við fyrstu samstillingu
description: Þetta efni veitir bilanaleit sem getur hjálpað þér að laga vandamál sem kunna að koma upp við upphaflega samstillingu.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
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
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410082"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="0c934-103">Úrræðaleit vandamála við fyrstu samstillingu</span><span class="sxs-lookup"><span data-stu-id="0c934-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c934-104">Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0c934-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="0c934-105">Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem kunna að koma upp við upphaflega samstillingu.</span><span class="sxs-lookup"><span data-stu-id="0c934-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0c934-106">Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda.</span><span class="sxs-lookup"><span data-stu-id="0c934-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="0c934-107">Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.</span><span class="sxs-lookup"><span data-stu-id="0c934-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="0c934-108">Athugaðu hvort fyrstu samstillingarvillur eru í forriti Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0c934-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="0c934-109">Eftir að þú hefur gert kortlagningarsniðmát virkt ætti staða korta að vera **Í keyrslu**.</span><span class="sxs-lookup"><span data-stu-id="0c934-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="0c934-110">Ef staðan er **Ekki í gangi** geta villur komið upp við fyrstu samstillingu.</span><span class="sxs-lookup"><span data-stu-id="0c934-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="0c934-111">Til að skoða villurnar velurðu flipann **Upphaflegar samstillingarupplýsingar** á síðunni **Tvöfalt skrif**.</span><span class="sxs-lookup"><span data-stu-id="0c934-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Flipi upphafssamstillingar](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="0c934-113">Þú getur ekki lokið fyrstu samstillingu: 400 Bad Request</span><span class="sxs-lookup"><span data-stu-id="0c934-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="0c934-114">**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="0c934-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="0c934-115">Þú gætir fengið eftirfarandi villuboð þegar þú reynir að keyra vörpun og upphafssamstillingu:</span><span class="sxs-lookup"><span data-stu-id="0c934-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="0c934-116">*Fjartengdi þjónninn skilaði villu: (400) Bad Request.), AX export encountered an error*</span><span class="sxs-lookup"><span data-stu-id="0c934-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="0c934-117">Hér er dæmi um full villuboð.</span><span class="sxs-lookup"><span data-stu-id="0c934-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="0c934-118">Ef þessi villa kemur stöðugt fram og þú getur ekki klárað fyrstu samstillingu, fylgdu þessum skrefum til að laga málið.</span><span class="sxs-lookup"><span data-stu-id="0c934-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="0c934-119">Skráðu þig inn á sýndarvélina (VM) fyrir forrit Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0c934-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="0c934-120">Opnaðu stjórnborð Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0c934-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="0c934-121">Í glugganum **Þjónusta** skaltu ganga úr skugga um að Microsoft Dynamics 365 rammaþjónusta gagnainnflutnings-útflutnings er í gangi.</span><span class="sxs-lookup"><span data-stu-id="0c934-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="0c934-122">Endurræstu það ef það hefur verið stöðvað, vegna þess að fyrsta samstillinga krefst þess.</span><span class="sxs-lookup"><span data-stu-id="0c934-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="0c934-123">Upphafleg samstillingarvilla: 403 Forbidden</span><span class="sxs-lookup"><span data-stu-id="0c934-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="0c934-124">Þú gætir fengið eftirfarandi villuboð við fyrstu samstillingu:</span><span class="sxs-lookup"><span data-stu-id="0c934-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="0c934-125">*(\[Forbidden\], Fjartengdi þjónninn skilaði villu: (403) Forbidden.), AX export encountered an error*</span><span class="sxs-lookup"><span data-stu-id="0c934-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="0c934-126">Til að laga úr vandamálið skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="0c934-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="0c934-127">Innskráning í forritið Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0c934-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="0c934-128">Á síðunni **Azure Active Directory forrit** eyðirðu **DtAppID** biðlaranum og bætir honum síðan við aftur.</span><span class="sxs-lookup"><span data-stu-id="0c934-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Listi yfir Azure AD forrit](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="0c934-130">Villur sjálfstilvísunar eða hringtilvísunar við fyrstu samstillingu</span><span class="sxs-lookup"><span data-stu-id="0c934-130">Self-reference or circular-reference failures during initial synchronization</span></span>

<span data-ttu-id="0c934-131">Hugsanlega birtast villuboð ef einhver vörpun er með tilvísanir í sjálfa sig eða hringtilvísanir.</span><span class="sxs-lookup"><span data-stu-id="0c934-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="0c934-132">Villurnar falla í þessa flokka:</span><span class="sxs-lookup"><span data-stu-id="0c934-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="0c934-133">Einingavörpun lánardrottna V2 í msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="0c934-133">Vendors V2 to msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="0c934-134">Einingavörpun viðskiptavina V3 til lykla</span><span class="sxs-lookup"><span data-stu-id="0c934-134">Customers V3 to Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="0c934-135">Leysa úr villu í einingavörpun lánardrottna V2 til msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="0c934-135">Resolve an error in Vendors V2 to msdyn_vendors entity mapping</span></span>

<span data-ttu-id="0c934-136">Hugsanlega rekstu á eftirfarandi villur upphaflegrar samstillingar í vörpuninni **Lánardrottnar V2** í **msdyn_vendors** ef einingarnar eru með fyrirliggjandi færslum með gildi í reitunum **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="0c934-136">You might run into the following initial sync errors on the **Vendors V2** to **msdyn_vendors** mapping if the entities have existing records with values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="0c934-137">Þetta er vegna þess að **InvoiceVendorAccountNumber** er reitur sem vísar í sjálfan sig og **PrimaryContactPersonId** er hringtilvísun í vörpun lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="0c934-137">This because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="0c934-138">*Ekki tókst að leysa úr guid fyrir reitinn: <field>. Uppflettingin fannst ekki: <value>. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="0c934-138">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

<span data-ttu-id="0c934-139">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="0c934-139">Here are a couple of examples:</span></span>

- <span data-ttu-id="0c934-140">*Ekki tókst að leysa úr guid fyrir reitinn: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Uppflettingin fannst ekki: 000056. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="0c934-140">*Couldn't resolve the guid for the field: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="0c934-141">*Ekki tókst að leysa úr guid fyrir reitinn: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Uppflettingin fannst ekki: V24-1. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span><span class="sxs-lookup"><span data-stu-id="0c934-141">*Couldn't resolve the guid for the field: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span></span>

<span data-ttu-id="0c934-142">Ef til eru færslur með gildum í þessum reitum í einingu lánardrottins skal fylgja skrefunum í hlutanum hér á eftir til að ljúka upphaflegu samstillingunni.</span><span class="sxs-lookup"><span data-stu-id="0c934-142">If you have records with values in these fields in the vendor entity follow the steps in the below section to complete initial sync successfully.</span></span>

1. <span data-ttu-id="0c934-143">Í Finance and Operations-forritinu skal eyða reitunum **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** úr vörpuninni og vista breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="0c934-143">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping and save the changes.</span></span>

    1. <span data-ttu-id="0c934-144">Farið á vörpunarsíðu tvöfaldra skrifa fyrir **Lánardrottnar V2 (msdyn_vendors)** og veljið flipann **Einingavarpanir**. Í vinstri síunni skal velja **Finance and Operations apps.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="0c934-144">Navigate to the dual-write mapping page for **Vendors V2 (msdyn_vendors)**, and select the **Entity mappings** tab. In the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="0c934-145">Í hægri síunni skal velja **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="0c934-145">In the right filter, select **Sales.Vendor**.</span></span>

    2. <span data-ttu-id="0c934-146">Leitið að **primarycontactperson** til að finna upprunareitinn **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="0c934-146">Search for **primarycontactperson** to find the source field **PrimaryContactPersonId**.</span></span>
    
    3. <span data-ttu-id="0c934-147">Smellið á hnappinn **Aðgerðir** og veljið **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="0c934-147">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![sjálfs- eða hringtilvísun 3](media/vend_selfref3.png)
    
    4. <span data-ttu-id="0c934-149">Endurtakið til að eyða **InvoiceVendorAccountNumber** svæðinu.</span><span class="sxs-lookup"><span data-stu-id="0c934-149">Repeat to delete the **InvoiceVendorAccountNumber** field.</span></span>
    
        ![sjálfs- eða hringtilvísun 4](media/vend-selfref4.png)
    
    5. <span data-ttu-id="0c934-151">Vistið breytingar á vörpun.</span><span class="sxs-lookup"><span data-stu-id="0c934-151">Save the mapping changes.</span></span>

2. <span data-ttu-id="0c934-152">Slökkvið á rakningu breytinga fyrir eininguna **Lánardrottnar V2**.</span><span class="sxs-lookup"><span data-stu-id="0c934-152">Disable the change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="0c934-153">Farið í **Gagnastjórnun \> Gagnaeiningar**.</span><span class="sxs-lookup"><span data-stu-id="0c934-153">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="0c934-154">Veljið eininguna **Lánardrottnar V2**.</span><span class="sxs-lookup"><span data-stu-id="0c934-154">Select the **Vendors V2** entity.</span></span>
    
    3. <span data-ttu-id="0c934-155">Smellið á **Valkostir** í valmyndastikunni og síðan **Rakning breytinga**.</span><span class="sxs-lookup"><span data-stu-id="0c934-155">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![sjálfs- eða hringtilvísun 5](media/selfref_options.png)
    
    4. <span data-ttu-id="0c934-157">Smellið á **Gera breytingarakningu óvirka**.</span><span class="sxs-lookup"><span data-stu-id="0c934-157">Click **Disable Change Tracking**.</span></span>
    
        ![sjálfs- eða hringtilvísun 6](media/selfref_tracking.png)

3. <span data-ttu-id="0c934-159">Keyrið fyrstu samstillingu vörpunarinnar **Lánardrottnar V2 (msdyn_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="0c934-159">Run the initial sync of **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="0c934-160">Upphafleg samstilling ætti að keyra með góðum árangri án nokkurra villna.</span><span class="sxs-lookup"><span data-stu-id="0c934-160">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="0c934-161">Keyrið fyrstu samstillingu fyrir vörpunina **CDS tengiliðir V2 (tengiliðir)**.</span><span class="sxs-lookup"><span data-stu-id="0c934-161">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="0c934-162">Samstilla verður þessa vörpun ef óskað er eftir að samstilla reiti aðaltengiliða í einingu lánardrottna því að tengiliðafærslur verða einnig að vera samstilltar upphaflega.</span><span class="sxs-lookup"><span data-stu-id="0c934-162">You must sync this mapping if you want to sync primary contact field on vendors entity as the contacts records also need to be initial synced.</span></span>

5. <span data-ttu-id="0c934-163">Bætið reitunum **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** aftur við vörpunina **Lánardrottnar V2 (msdyn_vendors)** og vistið vörpunina.</span><span class="sxs-lookup"><span data-stu-id="0c934-163">Add the fields **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** back to the **Vendors V2 (msdyn_vendors)** mapping and save the mapping.</span></span>

6. <span data-ttu-id="0c934-164">Keyrið aftur fyrstu samstillingu fyrir vörpunina **Lánardrottnar V2 (msdyn_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="0c934-164">Run the initial sync again for the **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="0c934-165">Allar færslur verða samstilltar því að rakning breytinga er óvirk.</span><span class="sxs-lookup"><span data-stu-id="0c934-165">All the records will be synced, because change tracking is disabled.</span></span>

7. <span data-ttu-id="0c934-166">Kveikið á rakningu breytinga fyrir eininguna **Lánardrottnar V2**.</span><span class="sxs-lookup"><span data-stu-id="0c934-166">Enable change tracking for the **Vendors V2** entity.</span></span>

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="0c934-167">Leysið úr villu í Einingavörpun viðskiptavina V3 til lykla</span><span class="sxs-lookup"><span data-stu-id="0c934-167">Resolve an error in Customers V3 to Accounts entity mapping</span></span>

<span data-ttu-id="0c934-168">Hugsanlega rekstu á eftirfarandi villur upphaflegrar samstillingar í vörpuninni **Lánardrottnar V3** í **Lyklar** ef einingarnar eru með fyrirliggjandi færslum með gildi í reitunum **ContactPersonID** og **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="0c934-168">You might run into the following initial sync errors on the **Customers V3** to **Accounts** mapping if the entities have existing records with values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="0c934-169">Þetta er vegna þess að **InvoiceAccount** er reitur sem vísar í sjálfan sig og **ContactPersonID** er hringtilvísun í vörpun lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="0c934-169">This because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="0c934-170">*Ekki tókst að leysa úr guid fyrir reitinn: <field>. Uppflettingin fannst ekki: <value>. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="0c934-170">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

- <span data-ttu-id="0c934-171">*Ekki tókst að leysa úr guid fyrir reitinn: primarycontactid.msdyn_contactpersonid. Uppflettingin fannst ekki: 000056. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="0c934-171">*Couldn't resolve the guid for the field: primarycontactid.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="0c934-172">*Ekki tókst að leysa úr guid fyrir reitinn: msdyn_billingaccount.accountnumber. Uppflettingin fannst ekki: 1206-1. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span><span class="sxs-lookup"><span data-stu-id="0c934-172">*Couldn't resolve the guid for the field: msdyn_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span></span>

<span data-ttu-id="0c934-173">Ef til eru færslur með gildum í þessum reitum í einingu viðskiptavinar skal fylgja skrefunum í hlutanum hér á eftir til að ljúka upphaflegu samstillingunni.</span><span class="sxs-lookup"><span data-stu-id="0c934-173">If you have records with values in these fields in the customer entity follow the steps in the below section to complete initial sync successfully.</span></span> <span data-ttu-id="0c934-174">Hægt er að nota þessa nálgun fyrir allar tilbúnar einingar á borð við Lyklar og Tengiliðir.</span><span class="sxs-lookup"><span data-stu-id="0c934-174">You can use this approach for any out-of-the-box entities such Accounts and Contacts.</span></span>

1. <span data-ttu-id="0c934-175">Í Finance and Operations-forritinu skal eyða reitunum **ContactPersonID** og **InvoiceAccount** úr vörpuninni **Viðskiptavinir V3 (lyklar)** og vista hana.</span><span class="sxs-lookup"><span data-stu-id="0c934-175">In the Finance and Operations app, delete the fields **ContactPersonID** and **InvoiceAccount** from the **Customers V3 (accounts)** mapping and save the mapping.</span></span>

    1. <span data-ttu-id="0c934-176">Farið á vörpunarsíðu tvöfaldra skrifa fyrir **Viðskiptavinir V3 (lyklar)** og veljið flipann **Einingavarpanir**. Í vinstri síunni skal velja **Finance and Operations apps.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="0c934-176">Navigate to the dual-write mapping page for **Customers V3 (accounts)**, select the **Entity mappings** tab. In the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="0c934-177">Í hægri síunni skal velja **Common Data Service.Account**.</span><span class="sxs-lookup"><span data-stu-id="0c934-177">In the right filter, select **Common Data Service.Account**.</span></span>

    2. <span data-ttu-id="0c934-178">Leitið að **contactperson** til að finna upprunareitinn **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="0c934-178">Search for **contactperson** to find the source field **ContactPersonID**.</span></span>
    
    3. <span data-ttu-id="0c934-179">Smellið á hnappinn **Aðgerðir** og veljið **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="0c934-179">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![sjálfs- eða hringtilvísun 3](media/cust_selfref3.png)
    
    4. <span data-ttu-id="0c934-181">Endurtakið til að eyða **InvoiceAccount** svæðinu.</span><span class="sxs-lookup"><span data-stu-id="0c934-181">Repeat to delete the **InvoiceAccount** field.</span></span>
    
        ![sjálfs- eða hringtilvísun](media/cust_selfref4.png)
    
    5. <span data-ttu-id="0c934-183">Vistið breytingar á vörpun.</span><span class="sxs-lookup"><span data-stu-id="0c934-183">Save the mapping changes.</span></span>

2. <span data-ttu-id="0c934-184">Slökkvið á rakningu breytinga fyrir eininguna **Viðskiptavinir V3**.</span><span class="sxs-lookup"><span data-stu-id="0c934-184">Disable the change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="0c934-185">Farið í **Gagnastjórnun \> Gagnaeiningar**.</span><span class="sxs-lookup"><span data-stu-id="0c934-185">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="0c934-186">Veljið eininguna **Viðskiptavinir V3**.</span><span class="sxs-lookup"><span data-stu-id="0c934-186">Select the **Customers V3** entity.</span></span>
    
    3. <span data-ttu-id="0c934-187">Smellið á **Valkostir** í valmyndastikunni og síðan **Rakning breytinga**.</span><span class="sxs-lookup"><span data-stu-id="0c934-187">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![sjálfs- eða hringtilvísun 5](media/selfref_options.png)
    
    4. <span data-ttu-id="0c934-189">Smellið á **Gera breytingarakningu óvirka**.</span><span class="sxs-lookup"><span data-stu-id="0c934-189">Click **Disable Change Tracking**.</span></span>
    
        ![sjálfs- eða hringtilvísun 6](media/selfref_tracking.png)

3. <span data-ttu-id="0c934-191">Keyrið fyrstu samstillingu fyrir vörpunina **Viðskiptavinir V3 (Lyklar)**.</span><span class="sxs-lookup"><span data-stu-id="0c934-191">Run the initial sync for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="0c934-192">Upphafleg samstilling ætti að keyra með góðum árangri án nokkurra villna.</span><span class="sxs-lookup"><span data-stu-id="0c934-192">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="0c934-193">Keyrið fyrstu samstillingu fyrir vörpunina **CDS tengiliðir V2 (tengiliðir)**.</span><span class="sxs-lookup"><span data-stu-id="0c934-193">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="0c934-194">Það eru tvær varpanir með sama heitinu.</span><span class="sxs-lookup"><span data-stu-id="0c934-194">There are 2 maps with the same name.</span></span> <span data-ttu-id="0c934-195">Veljið þá með lýsinguna **Sniðmát tvöfaldra skrifa fyrir samstillingu FO.CDS Tengiliðir lánardrottins V2 við CDS.Contacts. Þarfnast nýs pakka \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="0c934-195">Select the one with the description **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span> <span data-ttu-id="0c934-196">í flipanum **Lýsing** fyrir vörpunina.</span><span class="sxs-lookup"><span data-stu-id="0c934-196">on the **Details** tab of the map.</span></span>

5. <span data-ttu-id="0c934-197">Bætið reitunum **InvoiceAccount** og **ContactPersonID** aftur við vörpunina **Viðskiptavinir V3 (Lyklar)** og vistið hana.</span><span class="sxs-lookup"><span data-stu-id="0c934-197">Add the fields **InvoiceAccount** and **ContactPersonId** back to the **Customers V3 (Accounts)** mapping and save the mapping.</span></span> <span data-ttu-id="0c934-198">Nú eru báðir reitirnir **InvoiceAccount** og **ContactPersonID** aftur orðnir hluti af samstillingarsniði í beinni.</span><span class="sxs-lookup"><span data-stu-id="0c934-198">Now, both the **InvoiceAccount** field and the **ContactPersonId** field are again part of live sync mode.</span></span> <span data-ttu-id="0c934-199">Í næsta skrefi er lokið við upphaflegu samstillinguna fyrir þessa reiti.</span><span class="sxs-lookup"><span data-stu-id="0c934-199">In the next step, you complete the initial sync for these fields.</span></span>

6. <span data-ttu-id="0c934-200">Keyrið aftur fyrstu samstillingu fyrir vörpunina **Viðskiptavinir V3 (Lyklar)**.</span><span class="sxs-lookup"><span data-stu-id="0c934-200">Run the initial sync again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="0c934-201">Vegna þess að breytingarakning er óvirk mun keyrsla samstillingar samstilla gögnin fyrir **InvoiceAccount** og **ContactPersonID** úr Finance and Operations-forritinu við Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0c934-201">Because change tracking is disabled, running the sync will sync the data for **InvoiceAccount** and **ContactPersonId** from the Finance and Operations app to Common Data Service.</span></span>

7. <span data-ttu-id="0c934-202">Til að samstilla gögnin fyrir **InvoiceAccount** og **ContactPersonId** úr Common Data Service við Finance and Operations er notað gagnasamþættingarverk.</span><span class="sxs-lookup"><span data-stu-id="0c934-202">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations, you use a data integration project.</span></span>

    1. <span data-ttu-id="0c934-203">Í Power Apps skal stofna gagnasamþættingarverk á milli eininganna **Sales.Account** og **Finance and Operations apps.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="0c934-203">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="0c934-204">Gagnastefnan verður að vera frá Common Data Service til Finance and Operations forritsins.</span><span class="sxs-lookup"><span data-stu-id="0c934-204">The data direction must be from Common Data Service to the Finance and Operations app.</span></span>  <span data-ttu-id="0c934-205">Þar sem **InvoiceAccount** er ný eigind í tvöföldum skrifum gætirðu viljað sleppa upphaflegri samstillingu fyrir þessa eigind.</span><span class="sxs-lookup"><span data-stu-id="0c934-205">Because **InvoiceAccount** is a new attribute in dual-write, you may want to skip initial sync for this attribute.</span></span> <span data-ttu-id="0c934-206">Nánari upplýsingar er að finna í [Sameina gögn í Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="0c934-206">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="0c934-207">Eftirfarandi mynd sýnir verk sem uppfærir **CustomerAccount** og **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="0c934-207">The following image shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![sjálfs- eða hringtilvísun](media/cust_selfref6.png)

    2. <span data-ttu-id="0c934-209">Bætið skilyrði fyrirtækis við síuna Common Data Service megin því að einungis færslurnar sem passa við síuskilyrði verða uppfærðar í Finance and Operations-forritinu.</span><span class="sxs-lookup"><span data-stu-id="0c934-209">Add the company criteria in the filter on Common Data Service side, because only the records that match filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="0c934-210">Til að bæta við síu skal smella á síutáknið.</span><span class="sxs-lookup"><span data-stu-id="0c934-210">To add a filter, click the filter icon.</span></span> <span data-ttu-id="0c934-211">Í svarglugganum **Breyta fyrirspurn** er hægt að bæta við síufyrirspurn eins og **_msdyn_company_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="0c934-211">In the **Edit query** dialog, you can add a filter query like **_msdyn_company_value eq '\<guid\>'**.</span></span> <span data-ttu-id="0c934-212">Ef síutáknið er ekki til staðar skal stofna þjónustubeiðni til að biðja gagnasamþættingarteymið um að virkja síugetu leigjandans.</span><span class="sxs-lookup"><span data-stu-id="0c934-212">If the filter icon is not present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span> <span data-ttu-id="0c934-213">Ef ekki er færð inn síufyrirspurn fyrir **_msdyn_company_value** verða allar færslurnar samstilltar.</span><span class="sxs-lookup"><span data-stu-id="0c934-213">If you do not enter a filter query for **_msdyn_company_value**, then all the records are synced.</span></span>

        ![sjálfs- eða hringtilvísun](media/cust_selfref7.png)

        <span data-ttu-id="0c934-215">Þetta lýkur fyrstu samstillingu færslnanna.</span><span class="sxs-lookup"><span data-stu-id="0c934-215">This completes the initial sync of the records.</span></span>

8. <span data-ttu-id="0c934-216">Kveikið á rakningu breytinga fyrir eininguna **Viðskiptavinir V3** í Finance and Operations-forritinu.</span><span class="sxs-lookup"><span data-stu-id="0c934-216">Enable change tracking for the **Customers V3** entity in the Finance and Operations app.</span></span>

