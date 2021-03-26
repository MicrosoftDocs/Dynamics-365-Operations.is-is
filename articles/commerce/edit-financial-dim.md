---
title: Breytið fjárhagsvíddum fyrir smásölufærslur
description: Þetta efnisatriði lýsir því hvernig á að breyta fjárhagsvíddum fyrir smásölufærslur í Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4d4b7e383ca2089ee98e70d23ccd890d0e6a86c5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221799"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="f83f4-103">Breytið fjárhagsvíddum fyrir smásölufærslur</span><span class="sxs-lookup"><span data-stu-id="f83f4-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f83f4-104">Þetta efnisatriði lýsir því hvernig á að breyta fjárhagsvíddum fyrir smásölufærslur í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f83f4-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="f83f4-105">Breyta fjárhagsvíddum</span><span class="sxs-lookup"><span data-stu-id="f83f4-105">Edit financial dimensions</span></span>

<span data-ttu-id="f83f4-106">Fylgið eftirfarandi skrefum til að breyta fjárhagsvíddum fyrir smásölufærslur í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="f83f4-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f83f4-107">Opnið síðuna **Fjárhagsvíddarskilgreining fyrir samþættingu forrita**.</span><span class="sxs-lookup"><span data-stu-id="f83f4-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="f83f4-108">Veljið virku færsluna **Samþætting sjálfgefinna vídda**.</span><span class="sxs-lookup"><span data-stu-id="f83f4-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="f83f4-109">Athugið flýtiflipann **Fjárhagsvíddir** og gangið úr skugga um að allar víddir sem á að breyta í Excel-vinnublaðinu séu til staðar á listanum **Val**.</span><span class="sxs-lookup"><span data-stu-id="f83f4-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="f83f4-110">Frekari upplýsingar eru í [Gagnaeiningar](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span><span class="sxs-lookup"><span data-stu-id="f83f4-110">For more information, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span></span>
1. <span data-ttu-id="f83f4-111">Sækið og opnið Excel-skrána á síðunni **Yfirlit**, á síðunni **Smásölufærslur** eða reitinn **Bilanir við villuleit í færslu** á vinnusvæðinu **Fjármál verslunar**.</span><span class="sxs-lookup"><span data-stu-id="f83f4-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="f83f4-112">Veljið **Hönnun** til að breyta fjárhagsvídd færslunnar og smellið síðan á blýantstáknið við hlið raðarinnar **Færsla (sannprófanleg)**.</span><span class="sxs-lookup"><span data-stu-id="f83f4-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="f83f4-113">Leitið að og veljið svæðið **FinancialDimensionDisplayValue**, veljið haushluta Excel-vinnublaðsins og síðan **Bæta við merki**.</span><span class="sxs-lookup"><span data-stu-id="f83f4-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="f83f4-114">Velja skal hólf fyrir neðan hólfið sem valið var í fyrra skrefi, velja **Bæta við gildi** og síðan **Uppfæra**.</span><span class="sxs-lookup"><span data-stu-id="f83f4-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="f83f4-115">Fjárhagsvíddunum er bætt við Excel-vinnublaðið og síðan er hægt að gera breytingar á þeim og birta þær.</span><span class="sxs-lookup"><span data-stu-id="f83f4-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="f83f4-116">Til að breyta víddunum í færslulínunum skal velja röðina **Sölufærslur (sannprófanlegar)**, velja blýantstáknið og síðan endurtaka skref 6 og 7.</span><span class="sxs-lookup"><span data-stu-id="f83f4-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="f83f4-117">Til að breyta víddunum í greiðslulínunum skal velja röðina **Greiðslufærslur (sannprófanlegar)**, velja blýantstáknið og síðan endurtaka skref 6 og 7.</span><span class="sxs-lookup"><span data-stu-id="f83f4-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f83f4-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f83f4-118">Additional resources</span></span>

[<span data-ttu-id="f83f4-119">Breyta og endurskoða færslur staðgreiðslu við afhendingu og stjórnun reiðufjár</span><span class="sxs-lookup"><span data-stu-id="f83f4-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="f83f4-120">Breyta og endurskoða netpöntun og ósamstilltar færslur pöntunar viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="f83f4-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="f83f4-121">Stofna Excel-vinnubók til að breyta smásölufærslum</span><span class="sxs-lookup"><span data-stu-id="f83f4-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="f83f4-122">Bæta svæðum við Excel-vinnubók til að breyta smásölufærslum</span><span class="sxs-lookup"><span data-stu-id="f83f4-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]