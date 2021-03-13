---
title: Hættuleg efni
description: Þetta efni veitir upplýsingar um skjöl um hættuleg efni og upplýsingar sem eru geymdar í umhverfinu þínu.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 156cd4ec3a1d1a08ba43832a93fde0d4f22ac2ed
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007642"
---
# <a name="hazardous-materials"></a><span data-ttu-id="85fca-103">Hættuleg efni</span><span class="sxs-lookup"><span data-stu-id="85fca-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="85fca-104">Upplýsingar um hættuleg efni eru sett upp í upplýsingastjórnun afuðar.</span><span class="sxs-lookup"><span data-stu-id="85fca-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="85fca-105">Þessi eining veitir einnig skjöl sem hægt er að prenta með vörugeymslu.</span><span class="sxs-lookup"><span data-stu-id="85fca-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="85fca-106">Þegar þú sendir efni sem eru flokkuð sem hættuleg vara verður að fylgja viðbótar pappírsvinnu með sendingum.</span><span class="sxs-lookup"><span data-stu-id="85fca-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="85fca-107">Virkni hættulegra efna skulum við geyma viðskiptavini um flokkunarupplýsingar og tengjast þeim til að gefa út hluti.</span><span class="sxs-lookup"><span data-stu-id="85fca-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="85fca-108">Þessar upplýsingar er síðan hægt að nota til að undirbúa flutningsgögn.</span><span class="sxs-lookup"><span data-stu-id="85fca-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85fca-109">Eiginleikar hættulegra efna í Microsoft Dynamics 365 Supply Chain Management bjóða upp á safn af gagnlegum reitum afurðarupplýsinga og tengdrar virkni sem getur hjálpað til við að skrá og vísa í upplýsingar sem tengjast hættulegum afurðum þínum.</span><span class="sxs-lookup"><span data-stu-id="85fca-109">The hazardous materials features in Microsoft Dynamics 365 Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="85fca-110">Þessir eiginleikar geta einnig hjálpað þér að hanna og prenta afhendingarskjöl sem innihalda einhverjar sömu upplýsingar um öll hættuleg efni sem þú ert að afhenda.</span><span class="sxs-lookup"><span data-stu-id="85fca-110">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="85fca-111">Kerfið mun hins vegar ekki láta þig sjálfkrafa fylgja eftir öllum viðeigandi reglugerðum í landinu eða svæðinu þínu.</span><span class="sxs-lookup"><span data-stu-id="85fca-111">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="85fca-112">Þótt þessum verkfærum sé ætlað að hjálpa til við að fylgja sameiginlegum reglugerðum eru þær hvorki nægilegar út af fyrir sig né tryggja að svo verði gert.</span><span class="sxs-lookup"><span data-stu-id="85fca-112">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="85fca-113">Fyrirtækið þitt ber ábyrgð á því að gera sér grein fyrir öllum viðeigandi reglugerðum og gera allar nauðsynlegar ráðstafanir til að fylgja þeim eftir.</span><span class="sxs-lookup"><span data-stu-id="85fca-113">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

<span data-ttu-id="85fca-114">Áður en þú getur notað þessa aðgerð er eftirfarandi uppsetning nauðsynleg:</span><span class="sxs-lookup"><span data-stu-id="85fca-114">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="85fca-115">**Vöruupplýsingastjórnun:** Settu upp kóða sem hægt er að nota á útgefnar vörur.</span><span class="sxs-lookup"><span data-stu-id="85fca-115">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="85fca-116">**Vöruhúsastjórnun:** Notaðu viðbótar sendingargögn til að prenta upplýsingar um sendingu.</span><span class="sxs-lookup"><span data-stu-id="85fca-116">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="85fca-117">Afurðaupplýsingastjórnun</span><span class="sxs-lookup"><span data-stu-id="85fca-117">Product information management</span></span>

<span data-ttu-id="85fca-118">Í vöruupplýsingastjórnun er að finna úrval af uppsetningarborðum þar sem þú getur bætt viðmiðunarupplýsingunum sem eru að finna í lista yfir hættulegan varning fyrir flutninga á vegum, í lofti og á sjó.</span><span class="sxs-lookup"><span data-stu-id="85fca-118">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="85fca-119">Hér eru sumar reglurgerðir sem oft er vísað í:</span><span class="sxs-lookup"><span data-stu-id="85fca-119">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="85fca-120">**ADR** - Reglugerðir sem tengjast alþjóðlegum flutningi á hættulegum farmi á vegum</span><span class="sxs-lookup"><span data-stu-id="85fca-120">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="85fca-121">**CFR 49** - Reglugerðir í Sameinuðu þjóðunum um flutning hættulegs vara</span><span class="sxs-lookup"><span data-stu-id="85fca-121">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="85fca-122">**IMDG** - Alþjóðlega sjávarhættulegu vörurnar (IMDG) kóðinn</span><span class="sxs-lookup"><span data-stu-id="85fca-122">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="85fca-123">**IATA** - Alþjóðlega flugsamgöngusamtökin (IATA) reglugerðir um hættulegan varning</span><span class="sxs-lookup"><span data-stu-id="85fca-123">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="85fca-124">Hver þessara reglugerða hefur lista yfir hættulegan varning sem inniheldur tilvísunarnúmer.</span><span class="sxs-lookup"><span data-stu-id="85fca-124">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="85fca-125">Listarnir fyrir hverja tegund flutninga eru sameinaðir í sameiginlegum alþjóðlegum flokkunum.</span><span class="sxs-lookup"><span data-stu-id="85fca-125">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="85fca-126">Supply Chain Management veitir tilvísunartöflu fyrir sameiginlega kóða í þessum listum.</span><span class="sxs-lookup"><span data-stu-id="85fca-126">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="85fca-127">Hver listi hefur einnig nokkra einstaka kóða sem hægt er að skilgreina.</span><span class="sxs-lookup"><span data-stu-id="85fca-127">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="85fca-128">Til að byrja að stilla þessar upplýsingar skaltu búa til reglugerð sem þú getur notað til að stilla upphafsbreyturnar.</span><span class="sxs-lookup"><span data-stu-id="85fca-128">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="85fca-129">Vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="85fca-129">Warehouse management</span></span>

<span data-ttu-id="85fca-130">Þegar sending er unnin er hægt að prenta nokkrar nýjar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="85fca-130">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="85fca-131">Þessar skýrslur nota upplýsingarnar sem þú settir upp í stjórnun vöruupplýsinga.</span><span class="sxs-lookup"><span data-stu-id="85fca-131">These reports use the information that you set up in Product information management.</span></span>
