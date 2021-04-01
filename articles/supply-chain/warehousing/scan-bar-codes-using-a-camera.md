---
title: Skanna strikamerki með myndavél í vöruhúsaforriti
description: Þetta efnisatriði útskýrir hvernig eigi að setja upp vöruhúsaforritið til að skanna strikamerki með því að nota myndavél á fartæki.
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 28a49736f43bd2d3bfd4c6856f2f87079a005ba2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239303"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-app"></a><span data-ttu-id="2e944-103">Skanna strikamerki með myndavél í vöruhúsaforriti</span><span class="sxs-lookup"><span data-stu-id="2e944-103">Scan bar codes using a camera in the warehouse app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e944-104">Þetta efnisatriði útskýrir hvernig eigi að setja upp vöruhúsaforritið til að skanna strikamerki með því að nota myndavél á fartæki.</span><span class="sxs-lookup"><span data-stu-id="2e944-104">This topic explains how to set up the warehouse app to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="2e944-105">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="2e944-105">Prerequisites</span></span>
<span data-ttu-id="2e944-106">Til að nota þessa aðgerð þarf að vera með útgáfu 1.2.0.0 af vöruhúsaforrit uppsetta og tækið þitt verður að vera með myndavél.</span><span class="sxs-lookup"><span data-stu-id="2e944-106">To use this feature, you need to have version 1.2.0.0 of the warehouse app installed, and your device must have a camera.</span></span> <span data-ttu-id="2e944-107">Þegar forritið er opnað eftir uppfærslu mun forritið biðja um leyfi til að nota myndavélina.</span><span class="sxs-lookup"><span data-stu-id="2e944-107">When you open the app after updating, you will be prompted to allow the app to use the camera.</span></span> <span data-ttu-id="2e944-108">Ef tækið er ekki með myndavél mun engin beiðni koma upp og ekki verður hægt að nota myndavélina sem skanna.</span><span class="sxs-lookup"><span data-stu-id="2e944-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="2e944-109">Setja upp</span><span class="sxs-lookup"><span data-stu-id="2e944-109">Setup</span></span>
<span data-ttu-id="2e944-110">Í skjástillingum vöruhúsaforrits er hægt að velja hvort eigi að nota myndavélina til að skanna strikamerki.</span><span class="sxs-lookup"><span data-stu-id="2e944-110">In the Display settings of the warehouse application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="2e944-111">Ef þú virkjar **Nota myndavél sem skanna** getur þú notað myndavélina fyrir öll ílagssvæði sem eru með æskilegan ílagsham stilltan á **Skönnun**.</span><span class="sxs-lookup"><span data-stu-id="2e944-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="2e944-112">Til að stjórna því hvort ílagssvæði eigi að vera skannanlegt skal á síðunni **Reitaheiti vöruhúsaforrits** stilla **Æskilegan ílagsham** á **Skönnun**.</span><span class="sxs-lookup"><span data-stu-id="2e944-112">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="2e944-113">Þegar þessi valkostur er valinn er hægt að nota myndavél sem skanna í vöruhúsaforritinu.</span><span class="sxs-lookup"><span data-stu-id="2e944-113">When this option is selected, a camera can be used for scanning in the warehouse app.</span></span> <span data-ttu-id="2e944-114">Upplýsingar um hvernig eigi að skilgreina svæðaheita í vöruhúsi er hægt að finna í [Skilgreina svæðaheiti forrits í vöruhúsaforriti](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="2e944-114">For information about how to configure app field names in Warehousing, see [Configure app field names in warehouse app](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="2e944-115">Studd snið strikamerkja</span><span class="sxs-lookup"><span data-stu-id="2e944-115">Supported bar code formats</span></span>
<span data-ttu-id="2e944-116">Algengustu snið strikamerkja eru studd, þ.á.m. kóði 128, kóði 39, kóði 93, EAN-8, EAN-13, UPC-E, UPC-A og QR kóðar.</span><span class="sxs-lookup"><span data-stu-id="2e944-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="2e944-117">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="2e944-117">Navigation</span></span>
<span data-ttu-id="2e944-118">Myndavélasíðan mun ræsast fyrir allar síður þar sem ílagssvæðið er með æskilegan ílagsham stilltan á skönnun. Þegar þú ert á síðu myndavélar skaltu nota eftirfarandi valmöguleika til að fletta:</span><span class="sxs-lookup"><span data-stu-id="2e944-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="2e944-119">Smellt er á hnappinn Til baka til að fara aftur á verk- og upplýsingasíðuna.</span><span class="sxs-lookup"><span data-stu-id="2e944-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="2e944-120">Smellt er á blýantinn á verk- og upplýsingasíðunni til að fara á síðuna þar sem hægt er að færa innsláttinn inn handvirkt.</span><span class="sxs-lookup"><span data-stu-id="2e944-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="2e944-121">Smellt er á myndavélina á verk- og upplýsingasíðunni til að fara aftur á myndavélasíðuna.</span><span class="sxs-lookup"><span data-stu-id="2e944-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="2e944-122">Verk- og upplýsingasíða</span><span class="sxs-lookup"><span data-stu-id="2e944-122">Task and details page</span></span> | <span data-ttu-id="2e944-123">Myndavélasíða</span><span class="sxs-lookup"><span data-stu-id="2e944-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![Síðan Dæmi um verkupplýsingar myndavélarskönnunar](./media/camera-scanning-example-task-detail-page50.png)          | ![Minni síða myndavélar dæmi um myndavélarskönnun](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="2e944-126">Þegar smellt er á myndavélahnappinn á myndavélasíðunni mun hún sýnast deyfð á meðan reynt er að auðkenna strikamerki.</span><span class="sxs-lookup"><span data-stu-id="2e944-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="2e944-127">Ef ekki er hægt að auðkenna strikamerki innan 5 sekúndna mun ferlið renna út á tíma og myndavélahnappurinn verður aftur tiltækur.</span><span class="sxs-lookup"><span data-stu-id="2e944-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="2e944-128">Þá er aftur hægt að skanna strikamerki.</span><span class="sxs-lookup"><span data-stu-id="2e944-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="2e944-129">Þegar myndavél er beint að strikamerki skal staðsetja strikamerkið innan hornklofanna til að fá sem bestar niðurstöðu.</span><span class="sxs-lookup"><span data-stu-id="2e944-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="2e944-130">Þegar tekst að skanna strikamerki er unnið úr niðurstöðunni og þér verður vísað yfir á næsta skref.</span><span class="sxs-lookup"><span data-stu-id="2e944-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="2e944-131">Ef næsta skref inniheldur annað ílagssvæði með æskilegan ílagsham stilltan á skönnun mun myndavélasíðan ræsast á ný.</span><span class="sxs-lookup"><span data-stu-id="2e944-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="2e944-132">Ef næsta skref er ekki skönnunarsvæði mun myndavélasíðan ekki ræsast.</span><span class="sxs-lookup"><span data-stu-id="2e944-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]