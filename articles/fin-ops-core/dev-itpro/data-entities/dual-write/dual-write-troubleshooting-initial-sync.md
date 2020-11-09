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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 4d0ca1fb4b7a4964194516544686b6bb7d26e76c
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997327"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="b6931-103">Úrræðaleit vandamála við fyrstu samstillingu</span><span class="sxs-lookup"><span data-stu-id="b6931-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b6931-104">Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b6931-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="b6931-105">Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem kunna að koma upp við upphaflega samstillingu.</span><span class="sxs-lookup"><span data-stu-id="b6931-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6931-106">Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda.</span><span class="sxs-lookup"><span data-stu-id="b6931-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="b6931-107">Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.</span><span class="sxs-lookup"><span data-stu-id="b6931-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="b6931-108">Athugaðu hvort fyrstu samstillingarvillur eru í forriti Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b6931-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="b6931-109">Eftir að þú hefur gert kortlagningarsniðmát virkt ætti staða korta að vera **Í keyrslu**.</span><span class="sxs-lookup"><span data-stu-id="b6931-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="b6931-110">Ef staðan er **Ekki í gangi** geta villur komið upp við fyrstu samstillingu.</span><span class="sxs-lookup"><span data-stu-id="b6931-110">If the status is **Not running** , errors occurred during initial synchronization.</span></span> <span data-ttu-id="b6931-111">Til að skoða villurnar velurðu flipann **Upphaflegar samstillingarupplýsingar** á síðunni **Tvöfalt skrif**.</span><span class="sxs-lookup"><span data-stu-id="b6931-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Villa í flipa upphaflegra samstillingarupplýsinga](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="b6931-113">Þú getur ekki lokið fyrstu samstillingu: 400 Bad Request</span><span class="sxs-lookup"><span data-stu-id="b6931-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="b6931-114">**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="b6931-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="b6931-115">Þú gætir fengið eftirfarandi villuboð þegar þú reynir að keyra vörpun og upphafssamstillingu:</span><span class="sxs-lookup"><span data-stu-id="b6931-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="b6931-116">*(\[Villa í beiðni\], fjartengdur þjónn skilaði villu: (400) Villa í beiðni.), villa kom upp í AX útflutningi*</span><span class="sxs-lookup"><span data-stu-id="b6931-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="b6931-117">Hér er dæmi um full villuboð.</span><span class="sxs-lookup"><span data-stu-id="b6931-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="b6931-118">Ef þessi villa kemur stöðugt fram og þú getur ekki klárað fyrstu samstillingu, fylgdu þessum skrefum til að laga málið.</span><span class="sxs-lookup"><span data-stu-id="b6931-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="b6931-119">Skráðu þig inn á sýndarvélina (VM) fyrir forrit Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b6931-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="b6931-120">Opnaðu stjórnborð Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b6931-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="b6931-121">Í glugganum **Þjónusta** skaltu ganga úr skugga um að Microsoft Dynamics 365 rammaþjónusta gagnainnflutnings-útflutnings er í gangi.</span><span class="sxs-lookup"><span data-stu-id="b6931-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="b6931-122">Endurræstu það ef það hefur verið stöðvað, vegna þess að fyrsta samstillinga krefst þess.</span><span class="sxs-lookup"><span data-stu-id="b6931-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="b6931-123">Upphafleg samstillingarvilla: 403 Forbidden</span><span class="sxs-lookup"><span data-stu-id="b6931-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="b6931-124">Þú gætir fengið eftirfarandi villuboð við fyrstu samstillingu:</span><span class="sxs-lookup"><span data-stu-id="b6931-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="b6931-125">*(\[Forbidden\], Fjartengdi þjónninn skilaði villu: (403) Forbidden.), AX export encountered an error*</span><span class="sxs-lookup"><span data-stu-id="b6931-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="b6931-126">Til að laga úr vandamálið skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="b6931-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="b6931-127">Innskráning í forritið Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b6931-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="b6931-128">Á síðunni **Azure Active Directory forrit** eyðirðu **DtAppID** biðlaranum og bætir honum síðan við aftur.</span><span class="sxs-lookup"><span data-stu-id="b6931-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![DtAppID-biðlari á lista yfir Azure AD-forrit](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="b6931-130">Villur sjálfstilvísunar eða hringtilvísunar við fyrstu samstillingu</span><span class="sxs-lookup"><span data-stu-id="b6931-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="b6931-131">Hugsanlega birtast villuboð ef einhver vörpun er með tilvísanir í sjálfa sig eða hringtilvísanir.</span><span class="sxs-lookup"><span data-stu-id="b6931-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="b6931-132">Villurnar falla í þessa flokka:</span><span class="sxs-lookup"><span data-stu-id="b6931-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="b6931-133">Villur í einingavörpuninni Lánardrottinn V2–to–msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="b6931-133">Errors in the Vendors V2–to–msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="b6931-134">Villur í einingavörpuninni Viðskiptavinir V3–to–Accounts</span><span class="sxs-lookup"><span data-stu-id="b6931-134">Errors in the Customers V3–to–Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="b6931-135">Leysa villur í einingavörpuninni Lánardrottinn V2–to–msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="b6931-135">Resolve errors in the Vendors V2–to–msdyn_vendors entity mapping</span></span>

<span data-ttu-id="b6931-136">Villur upphaflegrar samstillingar gætu komið upp fyrir vörpun **Lánardrottnar V2** í **msdyn\_lánardrottnar** ef einingarnar eru með fyrirliggjandi færslur þar sem eru gildi í reitunum **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="b6931-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the entities have existing records where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="b6931-137">Þessar villur koma upp vegna þess að **InvoiceVendorAccountNumber** er reitur sem vísar í sjálfan sig og **PrimaryContactPersonId** er hringtilvísun í vörpun lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="b6931-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="b6931-138">Villuboðin sem koma upp verða á eftirfarandi formi.</span><span class="sxs-lookup"><span data-stu-id="b6931-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="b6931-139">*Ekki tókst að leysa úr guid fyrir reitinn: \<field\>. Uppflettingin fannst ekki: \<value\>. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="b6931-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="b6931-140">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="b6931-140">Here are some examples:</span></span>

- <span data-ttu-id="b6931-141">*Ekki tókst að leysa úr guid fyrir reitinn: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Uppflettingin fannst ekki: 000056. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="b6931-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="b6931-142">*Ekki tókst að leysa úr guid fyrir reitinn: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Uppflettingin fannst ekki: V24-1. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="b6931-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="b6931-143">Ef einhverjir lánardrottnar í einingu lánardrottins eru með gildi í reitunum **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** skal fylgja þessum skrefum til að ljúka upphaflegu samstillingunni.</span><span class="sxs-lookup"><span data-stu-id="b6931-143">If any records in the vendor entity have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="b6931-144">Í Finance and Operations-forritinu skal eyða reitunum **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** úr vörpuninni og vista síðan vörpunina.</span><span class="sxs-lookup"><span data-stu-id="b6931-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="b6931-145">Á vörpunarsíðu tvöfaldra skrifa fyrir **Lánardrottnar V2 (msdyn)\_lánardrottnar** , í flipanum **Einingavarpanir** , í vinstri síunni, skal velja **Finance and Operations apps.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="b6931-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)** , on the **Entity mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="b6931-146">Í hægri síunni skal velja **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="b6931-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="b6931-147">Leitið að **primarycontactperson** til að finna upprunareitinn **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="b6931-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source field.</span></span>
    3. <span data-ttu-id="b6931-148">Veljið **Aðgerðir** og veljið svo **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="b6931-148">Select **Actions** , and then select **Delete**.</span></span>

        ![Eyða reitnum PrimaryContactPersonId](media/vend_selfref3.png)

    4. <span data-ttu-id="b6931-150">Endurtakið þessi skref til að eyða reitnum **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="b6931-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** field.</span></span>

        ![Eyða reitnum InvoiceVendorAccountNumber](media/vend-selfref4.png)

    5. <span data-ttu-id="b6931-152">Vistið breytingarnar í vörpunina.</span><span class="sxs-lookup"><span data-stu-id="b6931-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="b6931-153">Slökkvið á rakningu breytinga fyrir eininguna **Lánardrottnar V2**.</span><span class="sxs-lookup"><span data-stu-id="b6931-153">Turn off change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="b6931-154">Á vinnusvæðinu **Gagnastjórnun** skal velja reitinn **Gagnaeiningar**.</span><span class="sxs-lookup"><span data-stu-id="b6931-154">In the **Data management** workspace, select the **Data entities** tile.</span></span>
    2. <span data-ttu-id="b6931-155">Veljið eininguna **Lánardrottnar V2**.</span><span class="sxs-lookup"><span data-stu-id="b6931-155">Select the **Vendors V2** entity.</span></span>
    3. <span data-ttu-id="b6931-156">Á aðgerðasvæðinu skal velja **Valkostir** og síðan velja **Breytingarakning**.</span><span class="sxs-lookup"><span data-stu-id="b6931-156">On the Action Pane, select **Options** , and then select **Change tracking**.</span></span>

        ![Valkostur breytingarakningar valinn](media/selfref_options.png)

    4. <span data-ttu-id="b6931-158">Veljið **Gera breytingarakningu óvirka**.</span><span class="sxs-lookup"><span data-stu-id="b6931-158">Select **Disable Change Tracking**.</span></span>

        ![Gera breytingarakningu óvirka valið](media/selfref_tracking.png)

3. <span data-ttu-id="b6931-160">Keyrið upphaflega samstillingu fyrir vörpunina **Lánardrottnar V2 (msdyn\_lánardrottnar)**.</span><span class="sxs-lookup"><span data-stu-id="b6931-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="b6931-161">Upphafleg samstilling ætti að keyra með góðum árangri án nokkurra villna.</span><span class="sxs-lookup"><span data-stu-id="b6931-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="b6931-162">Keyrið upphaflega samstillingu fyrir vörpunina **CDS tengiliðir V2 (tengiliðir)**.</span><span class="sxs-lookup"><span data-stu-id="b6931-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="b6931-163">Samstilla verður þessa vörpun ef á að samstilla reit aðaltengiliða í einingu lánardrottins, því einnig þarf að gera upphaflega samstillingu fyrir tengiliðafærslurnar.</span><span class="sxs-lookup"><span data-stu-id="b6931-163">You must sync this mapping if you want to sync the primary contact field on the vendors entity, because initial synchronization must also be done for the contact records.</span></span>
5. <span data-ttu-id="b6931-164">Bætið reitunum **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** aftur við vörpunina **Lánardrottnar V2 (msdyn\_lánardrottnar)** og vistið síðan vörpunina.</span><span class="sxs-lookup"><span data-stu-id="b6931-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="b6931-165">Keyrið upphaflega samstillingu aftur fyrir vörpunina **Lánardrottnar V2 (msdyn\_lánardrottnar)**.</span><span class="sxs-lookup"><span data-stu-id="b6931-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="b6931-166">Slökkt er á rakningu breytinga og verða því allar færslur samstilltar.</span><span class="sxs-lookup"><span data-stu-id="b6931-166">Because change tracking is turned off, all the records will be synced.</span></span>
7. <span data-ttu-id="b6931-167">Kveikið aftur á rakningu breytinga fyrir eininguna **Lánardrottnar V2**.</span><span class="sxs-lookup"><span data-stu-id="b6931-167">Turn change tracking back on for the **Vendors V2** entity.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="b6931-168">Leysa úr villum í einingavörpuninni Viðskiptavinir V3–to–Accounts</span><span class="sxs-lookup"><span data-stu-id="b6931-168">Resolve errors in the Customers V3–to–Accounts entity mapping</span></span>

<span data-ttu-id="b6931-169">Villur upphaflegrar samstillingar gætu komið upp fyrir vörpun **Viðskiptavinir V3** í **Lyklar** ef einingarnar eru með fyrirliggjandi færslur þar sem eru gildi í reitunum **ContactPersonID** og **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="b6931-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the entities have existing records where there are values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="b6931-170">Þessar villur koma upp vegna þess að **InvoiceAccount** er reitur sem vísar í sjálfan sig og **ContactPersonID** er hringtilvísun í vörpun lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="b6931-170">These errors occur because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="b6931-171">Villuboðin sem koma upp verða á eftirfarandi formi.</span><span class="sxs-lookup"><span data-stu-id="b6931-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="b6931-172">*Ekki tókst að leysa úr guid fyrir reitinn: \<field\>. Uppflettingin fannst ekki: \<value\>. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="b6931-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="b6931-173">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="b6931-173">Here are some examples:</span></span>

- <span data-ttu-id="b6931-174">*Ekki tókst að leysa úr guid fyrir reitinn: primarycontactid.msdyn\_contactpersonid. Uppflettingin fannst ekki: 000056. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="b6931-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="b6931-175">*Ekki tókst að leysa úr guid fyrir reitinn: msdyn\_billingaccount.accountnumber. Uppflettingin fannst ekki: 1206-1. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="b6931-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="b6931-176">Ef einhverjar færslur í einingu viðskiptavinar eru með gildi í reitunum **ContactPersonID** og **InvoiceAccount** skal fylgja þessum skrefum til að ljúka upphaflegu samstillingunni.</span><span class="sxs-lookup"><span data-stu-id="b6931-176">If any records in the customer entity have values in the **ContactPersonID** and **InvoiceAccount** fields, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="b6931-177">Hægt er að nota þessa nálgun fyrir allar tilbúnar einingar á borð við **Lyklar** og **Tengiliðir**.</span><span class="sxs-lookup"><span data-stu-id="b6931-177">You can use this approach for any out-of-box entities, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="b6931-178">Í Finance and Operations-forritinu skal eyða reitunum **ContactPersonID** og **InvoiceAccount** úr vörpuninni **Viðskiptavinir V3 (lyklar)** og síðan vista hana.</span><span class="sxs-lookup"><span data-stu-id="b6931-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** fields from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="b6931-179">Á vörpunarsíðu tvöfaldra skrifa fyrir **Viðskiptavinir V3 (lyklar)** , á flipanum **Einingavarpanir** , á vinstri síunni, skal velja **Finance and Operations apps.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="b6931-179">On the dual-write mapping page for **Customers V3 (accounts)** , on the **Entity mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="b6931-180">Í hægri síunni skal velja **Common Data Service.Account**.</span><span class="sxs-lookup"><span data-stu-id="b6931-180">In the right filter, select **Common Data Service.Account**.</span></span>
    2. <span data-ttu-id="b6931-181">Leitið að **contactperson** til að finna upprunareitinn **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="b6931-181">Search for **contactperson** to find the **ContactPersonID** source field.</span></span>
    3. <span data-ttu-id="b6931-182">Veljið **Aðgerðir** og veljið svo **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="b6931-182">Select **Actions** , and then select **Delete**.</span></span>

        ![Reitnum ContactPersonID eytt](media/cust_selfref3.png)

    4. <span data-ttu-id="b6931-184">Endurtakið þessi skref til að eyða reitnum **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="b6931-184">Repeat these steps to delete the **InvoiceAccount** field.</span></span>

        ![Reitnum InvoiceAccount eytt](media/cust_selfref4.png)

    5. <span data-ttu-id="b6931-186">Vistið breytingarnar í vörpunina.</span><span class="sxs-lookup"><span data-stu-id="b6931-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="b6931-187">Slökkvið á rakningu breytinga fyrir eininguna **Viðskiptavinir V3**.</span><span class="sxs-lookup"><span data-stu-id="b6931-187">Turn off change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="b6931-188">Á vinnusvæðinu **Gagnastjórnun** skal velja reitinn **Gagnaeiningar**.</span><span class="sxs-lookup"><span data-stu-id="b6931-188">In the **Data management** workspace, select the **Data entities** tile.</span></span>
    2. <span data-ttu-id="b6931-189">Veljið eininguna **Viðskiptavinir V3**.</span><span class="sxs-lookup"><span data-stu-id="b6931-189">Select the **Customers V3** entity.</span></span>
    3. <span data-ttu-id="b6931-190">Á aðgerðasvæðinu skal velja **Valkostir** og síðan velja **Breytingarakning**.</span><span class="sxs-lookup"><span data-stu-id="b6931-190">On the Action Pane, select **Options** , and then select **Change tracking**.</span></span>

        ![Valkostur breytingarakningar valinn](media/selfref_options.png)

    4. <span data-ttu-id="b6931-192">Veljið **Gera breytingarakningu óvirka**.</span><span class="sxs-lookup"><span data-stu-id="b6931-192">Select **Disable Change Tracking**.</span></span>

        ![Gera breytingarakningu óvirka valið](media/selfref_tracking.png)

3. <span data-ttu-id="b6931-194">Keyrið upphaflega samstillingu fyrir vörpunina **Viðskiptavinir V3 (Lyklar)**.</span><span class="sxs-lookup"><span data-stu-id="b6931-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="b6931-195">Upphafleg samstilling ætti að keyra með góðum árangri án nokkurra villna.</span><span class="sxs-lookup"><span data-stu-id="b6931-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="b6931-196">Keyrið upphaflega samstillingu fyrir vörpunina **CDS tengiliðir V2 (tengiliðir)**.</span><span class="sxs-lookup"><span data-stu-id="b6931-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b6931-197">Tvær varpanir eru með sama heitið.</span><span class="sxs-lookup"><span data-stu-id="b6931-197">There are two maps that have the same name.</span></span> <span data-ttu-id="b6931-198">Verið viss um að velja þá vörpun sem er með eftirfarandi lýsingu í flipanum **Upplýsingar** : **Sniðmát tvöfaldra skrifa fyrir samstillingu milli FO.CDS Tengiliður lánardrottins V2 og CDS.Contacts. Þarfnast nýs pakka \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="b6931-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="b6931-199">Bætið reitunum **InvoiceAccount** og **ContactPersonID** aftur við vörpunina **Viðskiptavinir V3 (Lyklar)** og vistið hana síðan.</span><span class="sxs-lookup"><span data-stu-id="b6931-199">Add the **InvoiceAccount** and **ContactPersonId** fields back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="b6931-200">Nú eru báðir reitirnir **InvoiceAccount** og **ContactPersonId** aftur orðnir hluti af samstillingarsniði í beinni.</span><span class="sxs-lookup"><span data-stu-id="b6931-200">Both the **InvoiceAccount** field and the **ContactPersonId** field are now part of live synchronization mode again.</span></span> <span data-ttu-id="b6931-201">Í næsta skrefi verður gerð upphafleg samstilling fyrir þessa reiti.</span><span class="sxs-lookup"><span data-stu-id="b6931-201">In the next step, you will do the initial synchronization for these fields.</span></span>
6. <span data-ttu-id="b6931-202">Keyrið aftur upphaflega samstillingu fyrir vörpunina **Viðskiptavinir V3 (Lyklar)**.</span><span class="sxs-lookup"><span data-stu-id="b6931-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="b6931-203">Vegna þess að slökkt er á breytingarakningu, verða gögnin fyrir **InvoiceAccount** og **ContactPersonId** samstillt úr Finance and Operations-forritinu við Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b6931-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Common Data Service.</span></span>
7. <span data-ttu-id="b6931-204">Til að samstilla gögnin fyrir **InvoiceAccount** og **ContactPersonId** úr Common Data Service við forritið Finance and Operations þarf að nota gagnasamþættingarverk.</span><span class="sxs-lookup"><span data-stu-id="b6931-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="b6931-205">Í Power Apps skal stofna gagnasamþættingarverk á milli eininganna **Sales.Account** og **Finance and Operations apps.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="b6931-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="b6931-206">Gagnastefnan verður að vera frá Common Data Service til Finance and Operations forritsins.</span><span class="sxs-lookup"><span data-stu-id="b6931-206">The data direction must be from Common Data Service to the Finance and Operations app.</span></span> <span data-ttu-id="b6931-207">Þar sem **InvoiceAccount** er ný eigind í tvöföldum skrifum gætirðu viljað sleppa upphaflegri samstillingu fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="b6931-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="b6931-208">Nánari upplýsingar er að finna í [Sameina gögn í Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="b6931-208">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="b6931-209">Eftirfarandi skýringarmynd sýnir verk sem uppfærir **CustomerAccount** og **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="b6931-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![Gagnasamþættingarver til að uppfæra CustomerAccount og ContactPersonId](media/cust_selfref6.png)

    2. <span data-ttu-id="b6931-211">Bætið skilyrði fyrirtækis við síuna Common Data Service megin þannig að einungis færslur sem passa við síuskilyrði verða uppfærðar í Finance and Operations-forritinu.</span><span class="sxs-lookup"><span data-stu-id="b6931-211">Add the company criteria in the filter on the Common Data Service side, so that only records that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="b6931-212">Til að bæta við síu skal velja síuhnappinn.</span><span class="sxs-lookup"><span data-stu-id="b6931-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="b6931-213">Því næst, í svarglugganum **Breyta fyrirspurn** er hægt að bæta við síufyrirspurn á borð við **\_msdyn\_fyrirtæki\_gildi jafngildir „\<guid\>“**.</span><span class="sxs-lookup"><span data-stu-id="b6931-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="b6931-214">[ATHUGASEMD] Ef síuhnappurinn er ekki til staðar skal stofna þjónustubeiðni til að biðja gagnasamþættingarteymið um að virkja síugetu leigjandans.</span><span class="sxs-lookup"><span data-stu-id="b6931-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="b6931-215">Ef ekki er slegin inn síufyrirspurn fyrir **\_msdyn\_fyrirtæki\_gildi** verða allar færslurnar samstilltar.</span><span class="sxs-lookup"><span data-stu-id="b6931-215">If you don't enter a filter query for **\_msdyn\_company\_value** , all the records will be synced.</span></span>

        ![Síufyrirspurn bætt við](media/cust_selfref7.png)

    <span data-ttu-id="b6931-217">Upphaflegri samstillingu færslna er nú lokið.</span><span class="sxs-lookup"><span data-stu-id="b6931-217">The initial synchronization of the records is now completed.</span></span>

8. <span data-ttu-id="b6931-218">Í forritinu Finance and Operations skal kveikja aftur á rakningu breytinga fyrir eininguna **Viðskiptavinir V3**.</span><span class="sxs-lookup"><span data-stu-id="b6931-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** entity.</span></span>
