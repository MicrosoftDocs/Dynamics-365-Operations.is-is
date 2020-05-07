---
title: Leysa úr vandamálum við einingu fyrir tvöföld skrif í Finance and Operations-forritum
description: Þetta efni veitir bilanaleit sem getur hjálpað þér að laga vandamál með tvískrifunareiningunni í forritum Finance and Operations.
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
ms.openlocfilehash: 853791d5ffc1d92b9fbafa2acc13cd5543c38196
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275534"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="206a2-103">Leysa úr vandamálum við einingu fyrir tvöföld skrif í Finance and Operations-forritum</span><span class="sxs-lookup"><span data-stu-id="206a2-103">Troubleshoot issues with the dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="206a2-104">Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="206a2-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="206a2-105">Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál með **tvískrifunareiningunni** í forritum Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="206a2-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="206a2-106">Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda.</span><span class="sxs-lookup"><span data-stu-id="206a2-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="206a2-107">Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.</span><span class="sxs-lookup"><span data-stu-id="206a2-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="206a2-108">Ekki er hægt að hlaða einingu tvískiptrar skriftar í Finance and Operations-forritinu</span><span class="sxs-lookup"><span data-stu-id="206a2-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="206a2-109">Ef þú getur ekki opnað síðuna **Tvöfalt skrif** með því að velja reitinn **Tvöfalt skrif** á vinnusvæðinu **Gagnastjórnun** liggur gagnasamstillingarónustan líklega niðri.</span><span class="sxs-lookup"><span data-stu-id="206a2-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="206a2-110">Búðu til stuðningseðil til að biðja um endurræsingu gagnasamstillingarþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="206a2-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-map"></a><span data-ttu-id="206a2-111">Villa þegar þú reynir að búa til nýtt einingakort</span><span class="sxs-lookup"><span data-stu-id="206a2-111">Error when you try to create a new entity map</span></span>

<span data-ttu-id="206a2-112">**Nauðsynlegar innskráningarupplýsingar til að laga vandann:** Sami notandi og setti upp tvískipt skrif.</span><span class="sxs-lookup"><span data-stu-id="206a2-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="206a2-113">Þú gætir fengið eftirfarandi villuboð þegar þú reynir að stilla nýja einingu fyrir tvískipt skrif.</span><span class="sxs-lookup"><span data-stu-id="206a2-113">You might receive the following error message when you try to configure a new entity for dual-write.</span></span> <span data-ttu-id="206a2-114">Eini notandinn sem getur búið til vörpun er notandinn sem setti upp tengingu tvískiptrar skrifa.</span><span class="sxs-lookup"><span data-stu-id="206a2-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="206a2-115">*Kóði svörunarstöðu bendir ekki til árangurs: 401 (Óheimilt)*</span><span class="sxs-lookup"><span data-stu-id="206a2-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="206a2-116">Villa þegar þú opnar tvískipt notendaviðmót</span><span class="sxs-lookup"><span data-stu-id="206a2-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="206a2-117">Þú gætir fengið eftirfarandi villuboð þegar þú reynir að komast í tvískipt skrif úr vinnusvæðinu **Gagnastjórnun**:</span><span class="sxs-lookup"><span data-stu-id="206a2-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="206a2-118">*login.microsoftonline.com neitaði að tengjast.*</span><span class="sxs-lookup"><span data-stu-id="206a2-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="206a2-119">Til að laga málið, skráðu þig inn með því að nota InPrivate glugga í Microsoft Edge, huliðsglugga í Chromium, eða huliðsglugga í Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="206a2-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="206a2-120">Þú verður einnig að opna eða hreinsa smákökur frá þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="206a2-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="206a2-121">Villa þegar þú tengir umhverfið fyrir tvískipt skrif eða bætir við nýrri vörpun eininga</span><span class="sxs-lookup"><span data-stu-id="206a2-121">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="206a2-122">**Nauðsynlegt hlutverk til að laga vandann:** Kerfisstjóri í bæði Finance and Operations-forritum og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="206a2-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="206a2-123">Þú gætir lent í eftirfarandi villu þegar þú tengir eða býrð til kort:</span><span class="sxs-lookup"><span data-stu-id="206a2-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="206a2-124">*Svörunarstaðakóði bendir ekki til árangurs: 403 (tokenexchange).<br> Auðkenni fundar: \<lotuauðkenni þitt\><br> Auðkenni rótareksturs: \<auðkenni rótarstarfseminnar\>*</span><span class="sxs-lookup"><span data-stu-id="206a2-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="206a2-125">Þessi villa getur komið fram ef þú hefur ekki nægar heimildir til að tengja tvöfalt skrif eða búa til kort.</span><span class="sxs-lookup"><span data-stu-id="206a2-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="206a2-126">Þessi villa getur einnig komið upp ef Common Data Service-umhverfið var endurstillt án þess að aftengja tvískipt skrif.</span><span class="sxs-lookup"><span data-stu-id="206a2-126">This error can also occur if the Common Data Service environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="206a2-127">Sérhver notandi með hlutverk kerfisstjóra í bæði Finance and Operations-forritum og Common Data Service getur tengt umhverfin.</span><span class="sxs-lookup"><span data-stu-id="206a2-127">Any user with system administrator role in both Finance and Operations apps and Common Data Service can link the environments.</span></span> <span data-ttu-id="206a2-128">Eingöngu notandinn sem setti upp tengingu tvískiptra skrifa getur bætt við nýjum einingavörpunum.</span><span class="sxs-lookup"><span data-stu-id="206a2-128">Only the user who setup the dual-write connection can add new entity maps.</span></span> <span data-ttu-id="206a2-129">Eftir uppsetningu getur allir notendur með hlutverk kerfisstjóra fylgst með stöðunni og breytt vörpununum.</span><span class="sxs-lookup"><span data-stu-id="206a2-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="206a2-130">Villa þegar þú hættir við vörpun einingar</span><span class="sxs-lookup"><span data-stu-id="206a2-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="206a2-131">Þú gætir fengið eftirfarandi villuboð þegar þú reynir að stöðva varpanir einingarinnar:</span><span class="sxs-lookup"><span data-stu-id="206a2-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="206a2-132">*\[Forbidden\], \[{"staða":403,"uppruni":"","skilaboð":"Villa úr táknskiptum: Notanda er ekki heimild að fara í tengingu dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span><span class="sxs-lookup"><span data-stu-id="206a2-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="206a2-133">Þessi villa kemur upp þegar tengt umhverfi Common Data Service er ekki í boði.</span><span class="sxs-lookup"><span data-stu-id="206a2-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="206a2-134">Til að laga málið, stofnaðu miða fyrir Data Integration teymið.</span><span class="sxs-lookup"><span data-stu-id="206a2-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="206a2-135">Festu netsporið svo að gagnasamstillingarteymið geti merkt kortin sem **Ekki í gangi** í bakvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="206a2-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-an-entity-mapping"></a><span data-ttu-id="206a2-136">Villa við að reyna að hefja vörpun eininga</span><span class="sxs-lookup"><span data-stu-id="206a2-136">Error while trying to start an entity mapping</span></span>

<span data-ttu-id="206a2-137">Þú gætir fengið villu eins og eftirfarandi þegar þú reynir að stilla þessa stöðu vörpunar á **Í gangi**:</span><span class="sxs-lookup"><span data-stu-id="206a2-137">You might receive an error like the following when you try to set that state of a mapping to **Running**:</span></span>

<span data-ttu-id="206a2-138">*Ekki tókst að ljúka upphaflegir samstillingu gagna. Villa: tvískipt skrif tókust ekki - skráning viðbótar mistókst: Get ekki búið til lýsigögn fyrir uppflettingu tvískiptra skrifa. Tilvísun í villuhlut ekki stillt á tilvik hlutar.*</span><span class="sxs-lookup"><span data-stu-id="206a2-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="206a2-139">Lagfæringin á þessari villu fer eftir orsök villunnar:</span><span class="sxs-lookup"><span data-stu-id="206a2-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="206a2-140">Ef vörpunin er með háðar varpanir skaltu ganga úr skugga um að virkja háðar varpanir fyrir þessa einingavörpun.</span><span class="sxs-lookup"><span data-stu-id="206a2-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this entity mapping.</span></span>
+ <span data-ttu-id="206a2-141">Hugsanlega vantar í vörpunina reiti upprunastaðar eða viðtökustaðar.</span><span class="sxs-lookup"><span data-stu-id="206a2-141">The mapping might be missing source or destination fields.</span></span> <span data-ttu-id="206a2-142">Ef það vantar reit í Finance and Operations-forritið skaltu fylgja eftirfarandi skrefum í hlutanum [Vandamál vegna einingareiti sem vanar í varpanir](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span><span class="sxs-lookup"><span data-stu-id="206a2-142">If a field in the Finance and Operations app is missing, then follow the steps in the section [Missing entity fields issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span></span> <span data-ttu-id="206a2-143">Ef reit vantar í Common Data Service skaltu smella á hnappinn **Endurhlaða einingar** í vörpununum svo reitirnir fyllist sjálfkrafa út í vörpuninni.</span><span class="sxs-lookup"><span data-stu-id="206a2-143">If a field in Common Data Service is missing, then click **Refresh entities** button on the mapping so that the fields are automatically populated back into the mapping.</span></span>
