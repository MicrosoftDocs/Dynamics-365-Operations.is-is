---
title: Bæta svæðum við Excel-vinnubók til að breyta smásölufærslum
description: Þetta efnisatriði lýsir því hvernig á að bæta svæðum við Microsoft Excel-vinnubók til að hægt sé að breyta smásölufærslum í Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
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
ms.openlocfilehash: 8ea5483ff1eea8922ffeb9e65768a0e5eab28890
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797696"
---
# <a name="add-fields-to-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="5f35e-103">Bæta svæðum við Excel-vinnubók til að breyta smásölufærslum</span><span class="sxs-lookup"><span data-stu-id="5f35e-103">Add fields to an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f35e-104">Þetta efnisatriði lýsir því hvernig á að bæta svæðum við Microsoft Excel-vinnubók til að hægt sé að breyta smásölufærslum í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5f35e-104">This topic describes how to add fields to a Microsoft Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5f35e-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="5f35e-105">Overview</span></span>

<span data-ttu-id="5f35e-106">Um leið og Excel-skrá er búin til í því skyni að breyta smásölufærslum er skráin útfyllt af sjálfgefnum svæðum.</span><span class="sxs-lookup"><span data-stu-id="5f35e-106">When you generate an Excel file so that you can edit retail transactions, the file is filled with some default fields.</span></span> <span data-ttu-id="5f35e-107">Þegar svæði sem þarf að uppfæra er ekki sjálfgefið sýnilegt í Excel-skránni sem var búin til er hægt að bæta svæðinu við.</span><span class="sxs-lookup"><span data-stu-id="5f35e-107">If a field that must be updated isn't visible by default in the generated Excel file, you can add it.</span></span>

## <a name="add-fields-to-a-worksheet-in-an-excel-workbook"></a><span data-ttu-id="5f35e-108">Bæta svæðum við vinnublað í Excel-vinnubók</span><span class="sxs-lookup"><span data-stu-id="5f35e-108">Add fields to a worksheet in an Excel workbook</span></span>

<span data-ttu-id="5f35e-109">Fylgja skal eftirfarandi skrefum til að bæta svæðum við Excel-vinnubók til að hægt sé að breyta smásölufærslum.</span><span class="sxs-lookup"><span data-stu-id="5f35e-109">To add fields to an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="5f35e-110">Sækið og opnið Excel-skrána á síðunni **Yfirlit**, á síðunni **Smásölufærslur** eða reitinn **Bilanir við villuleit í færslu** á vinnusvæðinu **Fjármál verslunar**.</span><span class="sxs-lookup"><span data-stu-id="5f35e-110">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="5f35e-111">Smellið á **Hönnun**.</span><span class="sxs-lookup"><span data-stu-id="5f35e-111">Select **Design**.</span></span>
1. <span data-ttu-id="5f35e-112">Veljið blýantstákn töflu að eigin vali og síðan svæði að eigin vali á listanum yfir tiltæk svæði.</span><span class="sxs-lookup"><span data-stu-id="5f35e-112">Select the pencil symbol for the desired table, and then, in the list of available fields, find and select the field that you want to add.</span></span>
1. <span data-ttu-id="5f35e-113">Smellið á **Bæta við** og smellið síðan á **Uppfæra**.</span><span class="sxs-lookup"><span data-stu-id="5f35e-113">Select **Add**, and then select **Update**.</span></span> <span data-ttu-id="5f35e-114">Hægt er að breyta uppröðun svæðanna.</span><span class="sxs-lookup"><span data-stu-id="5f35e-114">You can reorder fields.</span></span>
1. <span data-ttu-id="5f35e-115">Þegar uppfærslunni er lokið skal smella á **Uppfæra** til að ná í gögnin fyrir nýja dálkinn.</span><span class="sxs-lookup"><span data-stu-id="5f35e-115">After the update is completed, select **Refresh** to fetch the data for the new column.</span></span>

<span data-ttu-id="5f35e-116">Nýja svæðið og gögnin fyrir svæðið ættu að vera tiltæk til breytinga í Excel.</span><span class="sxs-lookup"><span data-stu-id="5f35e-116">The new field and data for it should now be available for editing in Excel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5f35e-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="5f35e-117">Additional resources</span></span>

[<span data-ttu-id="5f35e-118">Breyta og endurskoða færslur staðgreiðslu við afhendingu og stjórnun reiðufjár</span><span class="sxs-lookup"><span data-stu-id="5f35e-118">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="5f35e-119">Breyta og endurskoða netpöntun og ósamstilltar færslur pöntunar viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="5f35e-119">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="5f35e-120">Breyta fjárhagsvíddum fyrir smásölufærslur</span><span class="sxs-lookup"><span data-stu-id="5f35e-120">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="5f35e-121">Stofna Excel-vinnubók til að breyta smásölufærslum</span><span class="sxs-lookup"><span data-stu-id="5f35e-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]