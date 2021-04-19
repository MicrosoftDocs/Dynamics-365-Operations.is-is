---
title: Skanna strikamerki með myndavél í farsímaforriti vöruhúsakerfis
description: Þetta efnisatriði útskýrir hvernig eigi að setja upp farsímaforrit vöruhúsakerfis til að skanna strikamerki með því að nota myndavél á fartæki.
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831219"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="4fa71-103">Skanna strikamerki með myndavél í farsímaforriti vöruhúsakerfis</span><span class="sxs-lookup"><span data-stu-id="4fa71-103">Scan bar codes using a camera in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fa71-104">Þetta efnisatriði útskýrir hvernig eigi að setja upp farsímaforrit vöruhúsakerfis til að skanna strikamerki með því að nota myndavél á fartæki.</span><span class="sxs-lookup"><span data-stu-id="4fa71-104">This topic explains how to set up the Warehouse Management mobile app to scan bar codes using a camera on a mobile device.</span></span>

## <a name="setup"></a><span data-ttu-id="4fa71-105">Setja upp</span><span class="sxs-lookup"><span data-stu-id="4fa71-105">Setup</span></span>

<span data-ttu-id="4fa71-106">Í skjástillingum farsímaforrits vöruhúsakerfis er hægt að velja hvort eigi að nota myndavélina til að skanna strikamerki.</span><span class="sxs-lookup"><span data-stu-id="4fa71-106">In the display settings of the Warehouse Management mobile app, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="4fa71-107">Ef þú virkjar **Nota myndavél sem skanna** getur þú notað myndavélina fyrir öll ílagssvæði sem eru með æskilegan ílagsham stilltan á **Skönnun**.</span><span class="sxs-lookup"><span data-stu-id="4fa71-107">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span>

<span data-ttu-id="4fa71-108">Til að stjórna því hvort ílagssvæði eigi að vera skannanlegt skal á síðunni **Reitaheiti vöruhúsaforrits** stilla **Æskilegan ílagsham** á **Skönnun**.</span><span class="sxs-lookup"><span data-stu-id="4fa71-108">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="4fa71-109">Þegar þessi valkostur er valinn er hægt að nota myndavél sem skanna í farsímaforrit vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="4fa71-109">When this option is selected, a camera can be used for scanning in the Warehouse Management mobile app.</span></span> <span data-ttu-id="4fa71-110">Frekari upplýsingar eru í [Skilgreina reiti fyrir farsímaforrit vöruhúsakerfis](configure-app-field-names-priorities-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="4fa71-110">For more information, see [Configure fields for the Warehouse Management mobile app](configure-app-field-names-priorities-warehouse.md).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="4fa71-111">Studd snið strikamerkja</span><span class="sxs-lookup"><span data-stu-id="4fa71-111">Supported bar code formats</span></span>

<span data-ttu-id="4fa71-112">Algengustu snið strikamerkja eru studd, þ.á.m. kóði 128, kóði 39, kóði 93, EAN-8, EAN-13, UPC-E, UPC-A og QR kóðar.</span><span class="sxs-lookup"><span data-stu-id="4fa71-112">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span>

## <a name="navigation"></a><span data-ttu-id="4fa71-113">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="4fa71-113">Navigation</span></span>

<span data-ttu-id="4fa71-114">Myndavélasíðan mun ræsast fyrir allar síður þar sem færslureiturinn er með **Æskilega inntaksstilingu** stillta á *Skönnun*. Þegar þú ert á síðu myndavélar skaltu nota eftirfarandi valmöguleika til að fletta:</span><span class="sxs-lookup"><span data-stu-id="4fa71-114">The camera page will be initiated on each page where the input field has its **Preferred input mode** set to *Scanning*, when you are on the camera page use the following options to navigate:</span></span>

- <span data-ttu-id="4fa71-115">Bakkhnappurinn er valinn til að fara aftur á **verk- og upplýsingasíðuna**.</span><span class="sxs-lookup"><span data-stu-id="4fa71-115">Select the back button to go back to the **Task and details** page.</span></span>
- <span data-ttu-id="4fa71-116">Veljið blýantinn á **verk- og upplýsingasíðunni** til að fara á síðuna þar sem hægt er að færa innsláttinn inn handvirkt.</span><span class="sxs-lookup"><span data-stu-id="4fa71-116">Select the pencil on the **Task and details** page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="4fa71-117">Valin er myndavélin á **Verk- og upplýsingasíða** til að fara aftur á myndavélasíðuna.</span><span class="sxs-lookup"><span data-stu-id="4fa71-117">Select the camera on the **Task and details** page to go back to the camera page.</span></span>

<span data-ttu-id="4fa71-118">Þegar myndavélahnappurinn er valinn á myndavélasíðunni mun hann sýnast deyfður á meðan reynt er að auðkenna strikamerki.</span><span class="sxs-lookup"><span data-stu-id="4fa71-118">On the camera page, when you select the camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="4fa71-119">Ef ekki er hægt að auðkenna strikamerki innan 5 sekúndna mun ferlið renna út á tíma og myndavélahnappurinn verður aftur tiltækur.</span><span class="sxs-lookup"><span data-stu-id="4fa71-119">If a bar code is not identified within 5 seconds, the process will time out and the camera button will become available again.</span></span> <span data-ttu-id="4fa71-120">Þá er aftur hægt að skanna strikamerki.</span><span class="sxs-lookup"><span data-stu-id="4fa71-120">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="4fa71-121">Þegar myndavél er beint að strikamerki skal staðsetja strikamerkið innan hornklofanna til að fá sem bestar niðurstöðu.</span><span class="sxs-lookup"><span data-stu-id="4fa71-121">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="4fa71-122">Þegar tekst að skanna strikamerki er unnið úr niðurstöðunni og þér verður vísað yfir á næsta skref.</span><span class="sxs-lookup"><span data-stu-id="4fa71-122">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="4fa71-123">Ef næsta skref inniheldur annað ílagssvæði með æskilegan ílagsham stilltan á skönnun mun myndavélasíðan ræsast á ný.</span><span class="sxs-lookup"><span data-stu-id="4fa71-123">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="4fa71-124">Ef næsta skref er ekki skönnunarsvæði mun myndavélasíðan ekki ræsast.</span><span class="sxs-lookup"><span data-stu-id="4fa71-124">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]