---
title: Hættuleg efni
description: Þetta efni veitir upplýsingar um skjöl um hættuleg efni og upplýsingar sem eru geymdar í umhverfinu þínu.
author: lachlancashMS
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 443d2eb545b2b7592e27ae037009720db0a71997
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092546"
---
# <a name="hazardous-materials"></a><span data-ttu-id="73e84-103">Hættuleg efni</span><span class="sxs-lookup"><span data-stu-id="73e84-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73e84-104">Upplýsingar um hættuleg efni eru sett upp í upplýsingastjórnun afuðar.</span><span class="sxs-lookup"><span data-stu-id="73e84-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="73e84-105">Þessi eining veitir einnig skjöl sem hægt er að prenta með vörugeymslu.</span><span class="sxs-lookup"><span data-stu-id="73e84-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="73e84-106">Þegar þú sendir efni sem eru flokkuð sem hættuleg vara verður að fylgja viðbótar pappírsvinnu með sendingum.</span><span class="sxs-lookup"><span data-stu-id="73e84-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="73e84-107">Virkni hættulegra efna skulum við geyma viðskiptavini um flokkunarupplýsingar og tengjast þeim til að gefa út hluti.</span><span class="sxs-lookup"><span data-stu-id="73e84-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="73e84-108">Þessar upplýsingar er síðan hægt að nota til að undirbúa flutningsgögn.</span><span class="sxs-lookup"><span data-stu-id="73e84-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73e84-109">Til að hjálpa til við að stjórna sendingum af hættulegum varningi, Microsoft Dynamics 365 Supply Chain Management gerir þér kleift að setja upp viðbótarviðmiðunarupplýsingar sem tengjast vörum.</span><span class="sxs-lookup"><span data-stu-id="73e84-109">To help manage shipments of dangerous goods, Microsoft Dynamics 365 Supply Chain Management lets you set up additional reference information that is related to products.</span></span> <span data-ttu-id="73e84-110">Þú getur einnig sett upp fleiri sendingar skjöl.</span><span class="sxs-lookup"><span data-stu-id="73e84-110">You can also set up additional shipment documents.</span></span> <span data-ttu-id="73e84-111">Hins vegar er kerfið ekki sjálfkrafa í samræmi við reglugerðir lands eða lands.</span><span class="sxs-lookup"><span data-stu-id="73e84-111">However, the system isn't automatically compliant with your country's or region's regulations.</span></span> <span data-ttu-id="73e84-112">Í staðinn er það tæki sem getur hjálpað heildarforritinu þínu.</span><span class="sxs-lookup"><span data-stu-id="73e84-112">Instead, it's a tool that can help your overall program.</span></span>

<span data-ttu-id="73e84-113">Áður en þú getur notað þessa aðgerð er eftirfarandi uppsetning nauðsynleg:</span><span class="sxs-lookup"><span data-stu-id="73e84-113">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="73e84-114">**Vöruupplýsingastjórnun:** Settu upp kóða sem hægt er að nota á útgefnar vörur.</span><span class="sxs-lookup"><span data-stu-id="73e84-114">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="73e84-115">**Vöruhúsastjórnun:** Notaðu viðbótar sendingargögn til að prenta upplýsingar um sendingu.</span><span class="sxs-lookup"><span data-stu-id="73e84-115">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="73e84-116">Afurðaupplýsingastjórnun</span><span class="sxs-lookup"><span data-stu-id="73e84-116">Product information management</span></span>

<span data-ttu-id="73e84-117">Í vöruupplýsingastjórnun er að finna úrval af uppsetningarborðum þar sem þú getur bætt viðmiðunarupplýsingunum sem eru að finna í lista yfir hættulegan varning fyrir flutninga á vegum, í lofti og á sjó.</span><span class="sxs-lookup"><span data-stu-id="73e84-117">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="73e84-118">Hér eru sumar reglurgerðir sem oft er vísað í:</span><span class="sxs-lookup"><span data-stu-id="73e84-118">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="73e84-119">**ADR** - Reglugerðir sem tengjast alþjóðlegum flutningi á hættulegum farmi á vegum</span><span class="sxs-lookup"><span data-stu-id="73e84-119">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="73e84-120">**CFR 49** - Reglugerðir í Sameinuðu þjóðunum um flutning hættulegs vara</span><span class="sxs-lookup"><span data-stu-id="73e84-120">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="73e84-121">**IMDG** - Alþjóðlega sjávarhættulegu vörurnar (IMDG) kóðinn</span><span class="sxs-lookup"><span data-stu-id="73e84-121">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="73e84-122">**IATA** - Alþjóðlega flugsamgöngusamtökin (IATA) reglugerðir um hættulegan varning</span><span class="sxs-lookup"><span data-stu-id="73e84-122">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="73e84-123">Hver þessara reglugerða hefur lista yfir hættulegan varning sem inniheldur tilvísunarnúmer.</span><span class="sxs-lookup"><span data-stu-id="73e84-123">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="73e84-124">Listarnir fyrir hverja tegund flutninga eru sameinaðir í sameiginlegum alþjóðlegum flokkunum.</span><span class="sxs-lookup"><span data-stu-id="73e84-124">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="73e84-125">Supply Chain Management veitir tilvísunartöflu fyrir sameiginlega kóða í þessum listum.</span><span class="sxs-lookup"><span data-stu-id="73e84-125">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="73e84-126">Hver listi hefur einnig nokkra einstaka kóða sem hægt er að skilgreina.</span><span class="sxs-lookup"><span data-stu-id="73e84-126">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="73e84-127">Til að byrja að stilla þessar upplýsingar skaltu búa til reglugerð sem þú getur notað til að stilla upphafsbreyturnar.</span><span class="sxs-lookup"><span data-stu-id="73e84-127">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="73e84-128">Vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="73e84-128">Warehouse management</span></span>

<span data-ttu-id="73e84-129">Þegar sending er unnin er hægt að prenta nokkrar nýjar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="73e84-129">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="73e84-130">Þessar skýrslur nota upplýsingarnar sem þú settir upp í stjórnun vöruupplýsinga.</span><span class="sxs-lookup"><span data-stu-id="73e84-130">These reports use the information that you set up in Product information management.</span></span>
