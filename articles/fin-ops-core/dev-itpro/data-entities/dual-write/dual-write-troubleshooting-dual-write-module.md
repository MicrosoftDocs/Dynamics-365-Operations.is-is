---
title: Úrræðaleit vegna vandamála tvöfaldrar skráningar í Finance and Operations forritum
description: Þetta efni veitir bilanaleit sem getur hjálpað þér að laga vandamál með tvískrifunareiningunni í forritum Finance and Operations.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 46f561d3cddf1a94ff71e284e8085ff86d678600
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754063"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a><span data-ttu-id="a997c-103">Úrræðaleit vegna vandamála tvöfaldrar skráningar í Finance and Operations forritum</span><span class="sxs-lookup"><span data-stu-id="a997c-103">Troubleshoot dual-write issues in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a997c-104">Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a997c-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="a997c-105">Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál með **tvískrifunareiningunni** í forritum Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a997c-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a997c-106">Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda.</span><span class="sxs-lookup"><span data-stu-id="a997c-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="a997c-107">Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.</span><span class="sxs-lookup"><span data-stu-id="a997c-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="a997c-108">Ekki er hægt að hlaða einingu tvískiptrar skriftar í Finance and Operations-forritinu</span><span class="sxs-lookup"><span data-stu-id="a997c-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="a997c-109">Ef þú getur ekki opnað síðuna **Tvöfalt skrif** með því að velja reitinn **Tvöfalt skrif** á vinnusvæðinu **Gagnastjórnun** liggur gagnasamstillingarónustan líklega niðri.</span><span class="sxs-lookup"><span data-stu-id="a997c-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="a997c-110">Búðu til stuðningseðil til að biðja um endurræsingu gagnasamstillingarþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="a997c-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-table-map"></a><span data-ttu-id="a997c-111">Villa þegar reynt er að búa til nýtt töflukort</span><span class="sxs-lookup"><span data-stu-id="a997c-111">Error when you try to create a new table map</span></span>

<span data-ttu-id="a997c-112">**Nauðsynlegar innskráningarupplýsingar til að laga vandann:** Sami notandi og setti upp tvískipt skrif.</span><span class="sxs-lookup"><span data-stu-id="a997c-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="a997c-113">Þú gætir fengið eftirfarandi villuboð þegar þú reynir að stilla nýja töflu fyrir tvískipt skrif.</span><span class="sxs-lookup"><span data-stu-id="a997c-113">You might receive the following error message when you try to configure a new table for dual-write.</span></span> <span data-ttu-id="a997c-114">Eini notandinn sem getur búið til vörpun er notandinn sem setti upp tengingu tvískiptrar skrifa.</span><span class="sxs-lookup"><span data-stu-id="a997c-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="a997c-115">*Kóði svörunarstöðu bendir ekki til árangurs: 401 (Óheimilt)*</span><span class="sxs-lookup"><span data-stu-id="a997c-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="a997c-116">Villa þegar þú opnar tvískipt notendaviðmót</span><span class="sxs-lookup"><span data-stu-id="a997c-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="a997c-117">Þú gætir fengið eftirfarandi villuboð þegar þú reynir að komast í tvískipt skrif úr vinnusvæðinu **Gagnastjórnun**:</span><span class="sxs-lookup"><span data-stu-id="a997c-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="a997c-118">*login.microsoftonline.com neitaði að tengjast.*</span><span class="sxs-lookup"><span data-stu-id="a997c-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="a997c-119">Til að laga málið, skráðu þig inn með því að nota InPrivate glugga í Microsoft Edge, huliðsglugga í Chromium, eða huliðsglugga í Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="a997c-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="a997c-120">Þú verður einnig að opna eða hreinsa smákökur frá þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="a997c-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a><span data-ttu-id="a997c-121">Villa þegar tengt er við umhverfi fyrir tvöfalda skráningu eða nýrri töfluvörpun er bætt við</span><span class="sxs-lookup"><span data-stu-id="a997c-121">Error when you link the environment for dual-write or add a new table mapping</span></span>

<span data-ttu-id="a997c-122">**Nauðsynlegt hlutverk til að laga vandann:** Kerfisstjóri í bæði Finance and Operations-forritum og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a997c-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="a997c-123">Þú gætir lent í eftirfarandi villu þegar þú tengir eða býrð til kort:</span><span class="sxs-lookup"><span data-stu-id="a997c-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="a997c-124">*Stöðukóði svars gefur ekki til kynna að hafi tekist: 403 (tokenexchange).<br> Lotukenni: \<your session id\><br> Kenni rótarvirkni: \<your root activity id\>*</span><span class="sxs-lookup"><span data-stu-id="a997c-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="a997c-125">Þessi villa getur komið fram ef þú hefur ekki nægar heimildir til að tengja tvöfalt skrif eða búa til kort.</span><span class="sxs-lookup"><span data-stu-id="a997c-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="a997c-126">Þessi villa getur einnig komið upp ef Dataverse-umhverfið var endurstillt án þess að aftengja tvískipt skrif.</span><span class="sxs-lookup"><span data-stu-id="a997c-126">This error can also occur if the Dataverse environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="a997c-127">Sérhver notandi með hlutverk kerfisstjóra í bæði Finance and Operations-forritum og Dataverse getur tengt umhverfin.</span><span class="sxs-lookup"><span data-stu-id="a997c-127">Any user with system administrator role in both Finance and Operations apps and Dataverse can link the environments.</span></span> <span data-ttu-id="a997c-128">Eingöngu notandinn sem setti upp tengingu tvöfaldrar skráningar getur bætt við nýjum töfluvörpunum.</span><span class="sxs-lookup"><span data-stu-id="a997c-128">Only the user who setup the dual-write connection can add new table maps.</span></span> <span data-ttu-id="a997c-129">Eftir uppsetningu getur allir notendur með hlutverk kerfisstjóra fylgst með stöðunni og breytt vörpununum.</span><span class="sxs-lookup"><span data-stu-id="a997c-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-table-mapping"></a><span data-ttu-id="a997c-130">Villa þegar töfluvörpun er stöðvuð</span><span class="sxs-lookup"><span data-stu-id="a997c-130">Error when you stop the table mapping</span></span>

<span data-ttu-id="a997c-131">Þú gætir fengið eftirfarandi villuboð þegar þú reynir að stöðva töfluvörpunina:</span><span class="sxs-lookup"><span data-stu-id="a997c-131">You might receive the following error message when you try to stop the table mappings:</span></span>

<span data-ttu-id="a997c-132">*\[Forbidden\], \[{"staða":403,"uppruni":"","skilaboð":"Villa úr táknskiptum: Notanda er ekki heimild að fara í tengingu dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span><span class="sxs-lookup"><span data-stu-id="a997c-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="a997c-133">Þessi villa kemur upp þegar tengt umhverfi Dataverse er ekki í boði.</span><span class="sxs-lookup"><span data-stu-id="a997c-133">This error occurs when the linked Dataverse environment isn't available.</span></span>

<span data-ttu-id="a997c-134">Til að laga málið, stofnaðu miða fyrir Data Integration teymið.</span><span class="sxs-lookup"><span data-stu-id="a997c-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="a997c-135">Festu netsporið svo að gagnasamstillingarteymið geti merkt kortin sem **Ekki í gangi** í bakvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="a997c-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-a-table-mapping"></a><span data-ttu-id="a997c-136">Villa við að reyna að hefja töfluvörpun</span><span class="sxs-lookup"><span data-stu-id="a997c-136">Error while trying to start a table mapping</span></span>

<span data-ttu-id="a997c-137">Þú gætir fengið villu eins og eftirfarandi þegar þú reynir að stilla þessa stöðu vörpunar á **Í gangi**:</span><span class="sxs-lookup"><span data-stu-id="a997c-137">You might receive an error like the following when you try to set that state of a mapping to **Running**:</span></span>

<span data-ttu-id="a997c-138">*Ekki tókst að ljúka upphaflegir samstillingu gagna. Villa: tvískipt skrif tókust ekki - skráning viðbótar mistókst: Get ekki búið til lýsigögn fyrir uppflettingu tvískiptra skrifa. Tilvísun í villuhlut ekki stillt á tilvik hlutar.*</span><span class="sxs-lookup"><span data-stu-id="a997c-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="a997c-139">Lagfæringin á þessari villu fer eftir orsök villunnar:</span><span class="sxs-lookup"><span data-stu-id="a997c-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="a997c-140">Ef vörpunin er með háðar varpanir skaltu ganga úr skugga um að virkja háðar varpanir fyrir þessa töfluvörpun.</span><span class="sxs-lookup"><span data-stu-id="a997c-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this table mapping.</span></span>
+ <span data-ttu-id="a997c-141">Hugsanlega vantar í vörpunina dálka upprunastaðar eða viðtökustaðar.</span><span class="sxs-lookup"><span data-stu-id="a997c-141">The mapping might be missing source or destination columns.</span></span> <span data-ttu-id="a997c-142">Ef það vantar dálk í Finance and Operations-forritið skaltu fylgja eftirfarandi skrefum í hlutanum [Vandamál vegna töfludálka sem vantar í varpanir](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps).</span><span class="sxs-lookup"><span data-stu-id="a997c-142">If a column in the Finance and Operations app is missing, then follow the steps in the section [Missing table columns issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps).</span></span> <span data-ttu-id="a997c-143">Ef dálk vantar í Dataverse skal smella á hnappinn **Uppfæra töflur** í vörpununum svo dálkarnir fyllist sjálfkrafa út í vörpuninni.</span><span class="sxs-lookup"><span data-stu-id="a997c-143">If a column in Dataverse is missing, then click **Refresh tables** button on the mapping so that the columns are automatically populated back into the mapping.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]