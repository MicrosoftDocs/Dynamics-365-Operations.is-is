---
title: "Skanna strikamerki með myndavél í Dynamics 365 for Finance and Operations - Vöruhús"
description: "Þetta efnisatriði útskýrir hvernig eigi að setja upp Dynamics 365 for Finance and Operations - Vöruhús til að skanna strikamerki með myndavél á fartæki."
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e78d0a82d3ca66a6912ea1a9517296ca241edf1c
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---

# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a><span data-ttu-id="e2e77-103">Skanna strikamerki með myndavél í Dynamics 365 for Finance and Operations - Vöruhús</span><span class="sxs-lookup"><span data-stu-id="e2e77-103">Scan bar codes using a camera in Dynamics 365 for Finance and Operations – Warehousing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2e77-104">Þetta efnisatriði útskýrir hvernig eigi að setja upp Dynamics 365 for Finance and Operations - Vöruhús til að skanna strikamerki með myndavél á fartæki.</span><span class="sxs-lookup"><span data-stu-id="e2e77-104">This topic explains how to set up Dynamics 365 for Finance and Operations – Warehousing to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="e2e77-105">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="e2e77-105">Prerequisites</span></span>
<span data-ttu-id="e2e77-106">Til að nota þessa aðgerð þarf að vera með útgáfu 1.2.0.0 af Vöruhúsi uppsetta og tækið þitt verður að vera með myndavél.</span><span class="sxs-lookup"><span data-stu-id="e2e77-106">To use this feature, you need to have version 1.2.0.0 of Warehousing installed, and your device must have a camera.</span></span> <span data-ttu-id="e2e77-107">Þegar forritið er opnað eftir uppfærslu mun Dynamics 365 for Finance and Operations – Vöruhúsaforritið biðja um leyfi til að nota myndavélina.</span><span class="sxs-lookup"><span data-stu-id="e2e77-107">When you open the app after updating, you will be prompted to allow the Dynamics 365 for Finance and Operations – Warehousing application to use the camera.</span></span> <span data-ttu-id="e2e77-108">Ef tækið er ekki með myndavél mun engin beiðni koma upp og ekki verður hægt að nota myndavélina sem skanna.</span><span class="sxs-lookup"><span data-stu-id="e2e77-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="e2e77-109">Setja upp</span><span class="sxs-lookup"><span data-stu-id="e2e77-109">Setup</span></span>
<span data-ttu-id="e2e77-110">Í skjástillingum vöruhúsaforrits er hægt að velja hvort eigi að nota myndavélina til að skanna strikamerki.</span><span class="sxs-lookup"><span data-stu-id="e2e77-110">In the Display settings of the Warehousing application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="e2e77-111">Ef þú virkjar **Nota myndavél sem skanna** getur þú notað myndavélina fyrir öll ílagssvæði sem eru með æskilegan ílagsham stilltan á **Skönnun**.</span><span class="sxs-lookup"><span data-stu-id="e2e77-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="e2e77-112">Til að stjórna því hvort ílagssvæði eigi að vera skannanlegt skal á síðunni **Svæðisheiti vöruhúsaforrits** í Dynamics 365 for Finance and Operations stilla **Æskilegan ílagsham** á **Skönnun**.</span><span class="sxs-lookup"><span data-stu-id="e2e77-112">To control whether an input field should be scannable, on the **Warehouse app field names** page in Dynamics 365 for Finance and Operations, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="e2e77-113">Þegar þessi valkostur er valinn er hægt að nota myndavél sem skanna í vöruhúsaforritinu.</span><span class="sxs-lookup"><span data-stu-id="e2e77-113">When this option is selected, a camera can be used for scanning in the Warehousing app.</span></span> <span data-ttu-id="e2e77-114">Upplýsingar um hvernig eigi að skilgreina svæðaheita í vöruhúsi er hægt að finna í [Skilgreina svæðaheiti forrits í vöruhúsaforriti](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="e2e77-114">For information about how to configure app field names in Warehousing, see [Configure app field names in Warehousing app](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="e2e77-115">Studd snið strikamerkja</span><span class="sxs-lookup"><span data-stu-id="e2e77-115">Supported bar code formats</span></span>
<span data-ttu-id="e2e77-116">Algengustu snið strikamerkja eru studd, þ.á.m. kóði 128, kóði 39, kóði 93, EAN-8, EAN-13, UPC-E, UPC-A og QR kóðar.</span><span class="sxs-lookup"><span data-stu-id="e2e77-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="e2e77-117">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="e2e77-117">Navigation</span></span>
<span data-ttu-id="e2e77-118">Myndavélasíðan mun ræsast fyrir allar síður þar sem ílagssvæðið er með æskilegan ílagsham stilltan á skönnun. Þegar þú ert á síðu myndavélar skaltu nota eftirfarandi valmöguleika til að fletta:</span><span class="sxs-lookup"><span data-stu-id="e2e77-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="e2e77-119">Smellt er á hnappinn Til baka til að fara aftur á verk- og upplýsingasíðuna.</span><span class="sxs-lookup"><span data-stu-id="e2e77-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="e2e77-120">Smellt er á blýantinn á verk- og upplýsingasíðunni til að fara á síðuna þar sem hægt er að færa innsláttinn inn handvirkt.</span><span class="sxs-lookup"><span data-stu-id="e2e77-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="e2e77-121">Smellt er á myndavélina á verk- og upplýsingasíðunni til að fara aftur á myndavélasíðuna.</span><span class="sxs-lookup"><span data-stu-id="e2e77-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="e2e77-122">Verk- og upplýsingasíða</span><span class="sxs-lookup"><span data-stu-id="e2e77-122">Task and details page</span></span> | <span data-ttu-id="e2e77-123">Myndavélasíða</span><span class="sxs-lookup"><span data-stu-id="e2e77-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![myndavél-skönnun-dæmi-verk-upplýsinga-síða](./media/camera-scanning-example-task-detail-page50.png)          | ![myndavél-skönnun-dæmi-myndavél-síða-minni](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="e2e77-126">Þegar smellt er á myndavélahnappinn á myndavélasíðunni mun hún sýnast deyfð á meðan reynt er að auðkenna strikamerki.</span><span class="sxs-lookup"><span data-stu-id="e2e77-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="e2e77-127">Ef ekki er hægt að auðkenna strikamerki innan 5 sekúndna mun ferlið renna út á tíma og myndavélahnappurinn verður aftur tiltækur.</span><span class="sxs-lookup"><span data-stu-id="e2e77-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="e2e77-128">Þá er aftur hægt að skanna strikamerki.</span><span class="sxs-lookup"><span data-stu-id="e2e77-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="e2e77-129">Þegar myndavél er beint að strikamerki skal staðsetja strikamerkið innan hornklofanna til að fá sem bestar niðurstöðu.</span><span class="sxs-lookup"><span data-stu-id="e2e77-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="e2e77-130">Þegar tekst að skanna strikamerki er unnið úr niðurstöðunni og þér verður vísað yfir á næsta skref.</span><span class="sxs-lookup"><span data-stu-id="e2e77-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="e2e77-131">Ef næsta skref inniheldur annað ílagssvæði með æskilegan ílagsham stilltan á skönnun mun myndavélasíðan ræsast á ný.</span><span class="sxs-lookup"><span data-stu-id="e2e77-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="e2e77-132">Ef næsta skref er ekki skönnunarsvæði mun myndavélasíðan ekki ræsast.</span><span class="sxs-lookup"><span data-stu-id="e2e77-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>


