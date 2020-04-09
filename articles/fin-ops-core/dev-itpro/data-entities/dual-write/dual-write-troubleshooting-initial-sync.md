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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172715"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="3c509-103">Úrræðaleit vandamála við fyrstu samstillingu</span><span class="sxs-lookup"><span data-stu-id="3c509-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="3c509-104">Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3c509-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="3c509-105">Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem kunna að koma upp við upphaflega samstillingu.</span><span class="sxs-lookup"><span data-stu-id="3c509-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="3c509-106">Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda.</span><span class="sxs-lookup"><span data-stu-id="3c509-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="3c509-107">Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.</span><span class="sxs-lookup"><span data-stu-id="3c509-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="3c509-108">Athugaðu hvort fyrstu samstillingarvillur eru í forriti Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3c509-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="3c509-109">Eftir að þú hefur gert kortlagningarsniðmát virkt ætti staða korta að vera **Í keyrslu**.</span><span class="sxs-lookup"><span data-stu-id="3c509-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="3c509-110">Ef staðan er **Ekki í gangi** geta villur komið upp við fyrstu samstillingu.</span><span class="sxs-lookup"><span data-stu-id="3c509-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="3c509-111">Til að skoða villurnar velurðu flipann **Upphaflegar samstillingarupplýsingar** á síðunni **Tvöfalt skrif**.</span><span class="sxs-lookup"><span data-stu-id="3c509-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Flipi upphafssamstillingar](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="3c509-113">Þú getur ekki lokið fyrstu samstillingu: 400 Bad Request</span><span class="sxs-lookup"><span data-stu-id="3c509-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="3c509-114">**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="3c509-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="3c509-115">Þú gætir fengið eftirfarandi villuboð þegar þú reynir að keyra vörpun og upphafssamstillingu:</span><span class="sxs-lookup"><span data-stu-id="3c509-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="3c509-116">*Fjartengdi þjónninn skilaði villu: (400) Bad Request.), AX export encountered an error*</span><span class="sxs-lookup"><span data-stu-id="3c509-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="3c509-117">Hér er dæmi um full villuboð.</span><span class="sxs-lookup"><span data-stu-id="3c509-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="3c509-118">Ef þessi villa kemur stöðugt fram og þú getur ekki klárað fyrstu samstillingu, fylgdu þessum skrefum til að laga málið.</span><span class="sxs-lookup"><span data-stu-id="3c509-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="3c509-119">Skráðu þig inn á sýndarvélina (VM) fyrir forrit Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3c509-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="3c509-120">Opnaðu stjórnborð Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3c509-120">Open Microsoft Management Console.</span></span> 
3. <span data-ttu-id="3c509-121">Í glugganum **Þjónusta** skaltu ganga úr skugga um að Microsoft Dynamics 365 rammaþjónusta gagnainnflutnings-útflutnings er í gangi.</span><span class="sxs-lookup"><span data-stu-id="3c509-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="3c509-122">Endurræstu það ef það hefur verið stöðvað, vegna þess að fyrsta samstillinga krefst þess.</span><span class="sxs-lookup"><span data-stu-id="3c509-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="3c509-123">Upphafleg samstillingarvilla: 403 Forbidden</span><span class="sxs-lookup"><span data-stu-id="3c509-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="3c509-124">Þú gætir fengið eftirfarandi villuboð við fyrstu samstillingu:</span><span class="sxs-lookup"><span data-stu-id="3c509-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="3c509-125">*(\[Forbidden\], Fjartengdi þjónninn skilaði villu: (403) Forbidden.), AX export encountered an error*</span><span class="sxs-lookup"><span data-stu-id="3c509-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="3c509-126">Til að laga úr vandamálið skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="3c509-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="3c509-127">Innskráning í forritið Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3c509-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="3c509-128">Á síðunni **Azure Active Directory forrit** eyðirðu **DtAppID** biðlaranum og bætir honum síðan við aftur.</span><span class="sxs-lookup"><span data-stu-id="3c509-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Listi yfir Azure AD forrit](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a><span data-ttu-id="3c509-130">Sjálf-tilvísun mistök við fyrstu samstillingu</span><span class="sxs-lookup"><span data-stu-id="3c509-130">Self-reference failures during initial synchronization</span></span>

<span data-ttu-id="3c509-131">Þú gætir fengið villuboð sem líkjast eftirfarandi dæmi ef einhver af vörpunum þínum hefur sjálfsvísanir:</span><span class="sxs-lookup"><span data-stu-id="3c509-131">You might receive an error message that resembles the following example if any of your mappings have self-references:</span></span>

<span data-ttu-id="3c509-132">*Á Vendors V2, eftirfarandi villa: Record Id: new record, ErrorMessage: Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup value was not found: CN-001. Prófaðu þessa slóð til að athuga hvort tilvísunargögn eru til staðar: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span><span class="sxs-lookup"><span data-stu-id="3c509-132">*On the Vendors V2, the following error: Record Id: new record, ErrorMessage: Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup value was not found: CN-001. Try this URL(s) to check if the reference data exists: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span></span>

<span data-ttu-id="3c509-133">Þessi tegund af villu á sér stað við fyrstu samstillingu varpana sem hafa sjálftilvísanir.</span><span class="sxs-lookup"><span data-stu-id="3c509-133">This type of error occurs during initial synchronization of mappings that have self-references.</span></span> <span data-ttu-id="3c509-134">Í dæminu á undan vísar reiturinn reikningslykill til lánadrottinseiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="3c509-134">In the preceding example, the field invoice account references the vendor entity.</span></span>

<span data-ttu-id="3c509-135">Til að laga málið gætirðu þurft að keyra vörpunina tvisvar áður en fyrsta samstilling tekst.</span><span class="sxs-lookup"><span data-stu-id="3c509-135">To fix the issue, you might have to run the mapping two times before the initial synchronization is successful.</span></span>

