---
title: Úrræðaleit vandamál með tvískrifaðan einingunni í forritum Finance and Operations
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
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172761"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="58d4a-103">Úrræðaleit vandamál með tvískrifaðan einingunni í forritum Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="58d4a-103">Troubleshoot issues with the Dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="58d4a-104">Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="58d4a-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="58d4a-105">Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál með **tvískrifunareiningunni** í forritum Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="58d4a-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58d4a-106">Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda.</span><span class="sxs-lookup"><span data-stu-id="58d4a-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="58d4a-107">Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.</span><span class="sxs-lookup"><span data-stu-id="58d4a-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="58d4a-108">Þú getur ekki hlaðið tvíritunar eininguna í forriti Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="58d4a-108">You can't load the Dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="58d4a-109">Ef þú getur ekki opnað síðuna **Tvöfalt skrif** með því að velja reitinn **Tvöfalt skrif** á vinnusvæðinu **Gagnastjórnun** liggur gagnasamstillingarónustan líklega niðri.</span><span class="sxs-lookup"><span data-stu-id="58d4a-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="58d4a-110">Búðu til stuðningseðil til að biðja um endurræsingu gagnasamstillingarþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="58d4a-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a><span data-ttu-id="58d4a-111">Villa þegar þú reynir að búa til nýja vörpun eininga</span><span class="sxs-lookup"><span data-stu-id="58d4a-111">Error when you try to create a new entity mapping</span></span>

<span data-ttu-id="58d4a-112">**Nauðsynleg skilríki til að laga vandann:** Azure AD leigjandastjóri</span><span class="sxs-lookup"><span data-stu-id="58d4a-112">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="58d4a-113">Þú gætir fengið eftirfarandi villuboð þegar þú reynir að stilla nýja einingu fyrir tvískipt skrifun:</span><span class="sxs-lookup"><span data-stu-id="58d4a-113">You might receive the following error message when you try to configure a new entity for dual-write:</span></span>

<span data-ttu-id="58d4a-114">*Kóði svörunarstöðu bendir ekki til árangurs: 401 (Óheimilt)*</span><span class="sxs-lookup"><span data-stu-id="58d4a-114">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>

<span data-ttu-id="58d4a-115">Þessi villa kemur upp vegna þess að aðeins Azure AD leigjandi getur bætt við nýrri vörpun eininga.</span><span class="sxs-lookup"><span data-stu-id="58d4a-115">This error occurs because only an Azure AD tenant admin can add a new entity mapping.</span></span>

<span data-ttu-id="58d4a-116">Til að laga málið, skráðu þig inn á forrit Finance and Operations sem Azure AD stjórnandaleigjandi.</span><span class="sxs-lookup"><span data-stu-id="58d4a-116">To fix the issue, sign in to the Finance and Operations app as an Azure AD admin tenant.</span></span> <span data-ttu-id="58d4a-117">Þú verður líka að fara á web.PowerApps.com og staðfesta tenginguna.</span><span class="sxs-lookup"><span data-stu-id="58d4a-117">You must also go to web.PowerApps.com and revalidate your connection.</span></span>

## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="58d4a-118">Villa þegar þú opnar tvískipt notendaviðmót</span><span class="sxs-lookup"><span data-stu-id="58d4a-118">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="58d4a-119">Þú gætir fengið eftirfarandi villuboð þegar þú reynir að komast í tvískipt skrif úr vinnusvæðinu **Gagnastjórnun**:</span><span class="sxs-lookup"><span data-stu-id="58d4a-119">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="58d4a-120">*login.microsoftonline.com neitaði að tengjast.*</span><span class="sxs-lookup"><span data-stu-id="58d4a-120">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="58d4a-121">Til að laga málið, skráðu þig inn með því að nota InPrivate glugga í Microsoft Edge, huliðsglugga í Chromium, eða huliðsglugga í Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="58d4a-121">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="58d4a-122">Þú verður einnig að opna eða hreinsa smákökur frá þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="58d4a-122">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="58d4a-123">Villa þegar þú tengir umhverfið fyrir tvískipt skrif eða bætir við nýrri vörpun eininga</span><span class="sxs-lookup"><span data-stu-id="58d4a-123">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="58d4a-124">**Nauðsynleg skilríki til að laga vandann:** Azure AD leigjandastjóri</span><span class="sxs-lookup"><span data-stu-id="58d4a-124">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="58d4a-125">Þú gætir lent í eftirfarandi villu þegar þú tengir eða býrð til kort:</span><span class="sxs-lookup"><span data-stu-id="58d4a-125">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="58d4a-126">*Svörunarstaðakóði bendir ekki til árangurs: 403 (tokenexchange).<br> Auðkenni fundar: \<lotuauðkenni þitt\><br> Auðkenni rótareksturs: \<auðkenni rótarstarfseminnar\>*</span><span class="sxs-lookup"><span data-stu-id="58d4a-126">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="58d4a-127">Þessi villa getur komið fram ef þú hefur ekki nægar heimildir til að tengja tvöfalt skrif eða búa til kort.</span><span class="sxs-lookup"><span data-stu-id="58d4a-127">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="58d4a-128">Þú verður að nota Azure AD leigjandastjórareikning til að tengja umhverfi og bæta við nýjum vörpunum eininga.</span><span class="sxs-lookup"><span data-stu-id="58d4a-128">You must use an Azure AD tenant admin account to link environments and add new entity mappings.</span></span> <span data-ttu-id="58d4a-129">Eftir uppsetningu geturðu samt notað reikning sem ekki er stjórnandi til að fylgjast með stöðu og breyta vörpunum.</span><span class="sxs-lookup"><span data-stu-id="58d4a-129">However, after setup, you can use a non-admin account to monitor status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="58d4a-130">Villa þegar þú hættir við vörpun einingar</span><span class="sxs-lookup"><span data-stu-id="58d4a-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="58d4a-131">Þú gætir fengið eftirfarandi villuboð þegar þú reynir að stöðva varpanir einingarinnar:</span><span class="sxs-lookup"><span data-stu-id="58d4a-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="58d4a-132">*\[Forbidden\], \[{"staða":403,"uppruni":"","skilaboð":"Villa úr táknskiptum: Notanda er ekki heimild að fara í tengingu dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span><span class="sxs-lookup"><span data-stu-id="58d4a-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="58d4a-133">Þessi villa kemur upp þegar tengt umhverfi Common Data Service er ekki í boði.</span><span class="sxs-lookup"><span data-stu-id="58d4a-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="58d4a-134">Til að laga málið, stofnaðu miða fyrir Data Integration teymið.</span><span class="sxs-lookup"><span data-stu-id="58d4a-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="58d4a-135">Festu netsporið svo að gagnasamstillingarteymið geti merkt kortin sem **Ekki í gangi** í bakvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="58d4a-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>
