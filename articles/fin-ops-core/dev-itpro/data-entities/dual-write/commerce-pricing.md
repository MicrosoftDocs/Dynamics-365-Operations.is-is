---
title: Notið Dynamics 365 Commerce-verðlagningarkerfi ásamt Dynamics 365 Sales
description: Þetta efnisatriði lýsir því hvernig á að nota verðvél Microsoft Dynamics 365 Commerce til að stofna sölutilboð í Dynamics 365 Sales.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: 364cc5adf0358ffa952750149ad31d62cbd35e87
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751435"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a><span data-ttu-id="8e0ed-103">Notið Dynamics 365 Commerce-verðlagningarkerfi ásamt Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="8e0ed-103">Use the Dynamics 365 Commerce pricing engine with Dynamics 365 Sales</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8e0ed-104">Þetta efnisatriði lýsir því hvernig á að nota verðvél Microsoft Dynamics 365 Commerce til að stofna sölutilboð í Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="8e0ed-104">This topic describes how to use the Microsoft Dynamics 365 Commerce pricing engine to create sales quotations in Dynamics 365 Sales.</span></span>

<span data-ttu-id="8e0ed-105">Dynamics 365 Commerce -Verðlagningarvélin styður flestar aðstæður smásöluviðskipta til neytanda (B2C), svo sem verðlagningu á verslunarstigi, verðlagningar miðað við tengsl og vildarverð, blönduðum afslætti, magnafslætti og þröskuldarafslætti.</span><span class="sxs-lookup"><span data-stu-id="8e0ed-105">The Dynamics 365 Commerce pricing engine supports most business-to-consumer (B2C) pricing scenarios, such as store-level pricing, affiliation-based and loyalty-based pricing, mix-and-match discounts, quantity discounts, and threshold discounts.</span></span> <span data-ttu-id="8e0ed-106">Verðlagningarvélin notar flóknar reglur til að ákvarða besta verðið fyrir tiltekið tilboð eða pöntun.</span><span class="sxs-lookup"><span data-stu-id="8e0ed-106">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span>

<span data-ttu-id="8e0ed-107">Þegar þú notar [Tvöfalda skráningu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) eru þrír valmöguleikar fyrir verðþarfir.</span><span class="sxs-lookup"><span data-stu-id="8e0ed-107">When you use [dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), you have three options for your pricing needs.</span></span> <span data-ttu-id="8e0ed-108">Hægt er að nota fasta verðlagningu sem kemur úr verðlistanum í Dynamics 365 Sales, verðlagningarvélinni í Dynamics 365 Supply Chain Management eða verðlagningarvélinni í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8e0ed-108">You can use the static pricing that comes from the price list in Dynamics 365 Sales, the pricing engine in Dynamics 365 Supply Chain Management, or the pricing engine in Dynamics 365 Commerce.</span></span> <span data-ttu-id="8e0ed-109">Á meðal þessara valkosta hentar Commerce-verðlagningarvélin best fyrir B2C-aðstæður.</span><span class="sxs-lookup"><span data-stu-id="8e0ed-109">Among these options, the Commerce pricing engine is best suited to B2C scenarios.</span></span>

## <a name="use-the-commerce-pricing-engine-in-sales"></a><span data-ttu-id="8e0ed-110">Nota Commerce-vélverðlagningarvélina við sölu</span><span class="sxs-lookup"><span data-stu-id="8e0ed-110">Use the Commerce pricing engine in Sales</span></span>

> [!NOTE]
> <span data-ttu-id="8e0ed-111">Eins og stendur er einungis hægt að nota Commerce-verðlagningarvél fyrir tilboðsgerð við sölu.</span><span class="sxs-lookup"><span data-stu-id="8e0ed-111">Currently, the Commerce pricing engine can be used only for quotation creation in the Sales.</span></span> <span data-ttu-id="8e0ed-112">Samþætting sölupantana við verðlagningu í Commerce er ekki enn tiltæk.</span><span class="sxs-lookup"><span data-stu-id="8e0ed-112">Sales order integration with the Commerce pricing engine isn't yet available.</span></span>

<span data-ttu-id="8e0ed-113">Þegar notendur búa til tilboð við sölu afritar rammi tvöfaldrar skráningar upplýsingar um tilboðið í Commerce.</span><span class="sxs-lookup"><span data-stu-id="8e0ed-113">When users initiate a quotation in Sales, the dual-write framework copies the quotation details to Commerce.</span></span> <span data-ttu-id="8e0ed-114">Allar breytingar á fyrirliggjandi tilboðslínum eða öllum nýbættum tilboðslínum í Sales eru afritaðar í Commerce.</span><span class="sxs-lookup"><span data-stu-id="8e0ed-114">Any changes to existing quotation lines or any newly added quotation lines in Sales are copied to Commerce.</span></span> <span data-ttu-id="8e0ed-115">Þegar notendur vilja nota Commerce-verðlagningarvél til að verðleggja tilboðið geta þeir valið **Verðtilboð** til að uppfæra verð tilboðsins miðað við Commerce-verðlagningarvélina.</span><span class="sxs-lookup"><span data-stu-id="8e0ed-115">When users want to use the Commerce pricing engine to price the quotation, they can select **Price quote** to update the prices of the quotation, based on the Commerce pricing engine.</span></span> <span data-ttu-id="8e0ed-116">Verð eru þá sjálfkrafa uppfærð í bæði Sales og Commerce.</span><span class="sxs-lookup"><span data-stu-id="8e0ed-116">Prices are then automatically updated in both Sales and Commerce.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8e0ed-117">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="8e0ed-117">Prerequisites</span></span>

- <span data-ttu-id="8e0ed-118">Áður en hægt er að nota Commerce-verðlagningarvél í sölu þarf að fylgja skrefunum í [Viðfang til sjóðstreymis við tvöfalda skráningu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span><span class="sxs-lookup"><span data-stu-id="8e0ed-118">Before you can use the Commerce pricing engine in Sales, you must follow the steps in [Prospect-to-cash in dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span></span>
- <span data-ttu-id="8e0ed-119">Þú verður að slökkva á mati verðsamnings fyrir handvirkan innslátt með því að fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="8e0ed-119">You must turn off trade agreement evaluation for manual entry by following these steps:</span></span>

    1. <span data-ttu-id="8e0ed-120">Í Commerce umhverfinu skal fara í **Viðskiptakröfur \> Uppsetning \> Færibreytur viðskiptakröfu**.</span><span class="sxs-lookup"><span data-stu-id="8e0ed-120">In your Commerce environment, go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    1. <span data-ttu-id="8e0ed-121">Á flipanum **Verð**, á flpianum fyrir **Mat verðsamnings** skal hreinsa gátreitinn **Handvirk færsla** .</span><span class="sxs-lookup"><span data-stu-id="8e0ed-121">On the **Prices** tab, on the **Trade agreement evaluation** FastTab, clear the **Manual entry** check box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e0ed-122">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8e0ed-122">Additional resources</span></span>

[<span data-ttu-id="8e0ed-123">Viðfang til sjóðstreymis í tvískiptingu</span><span class="sxs-lookup"><span data-stu-id="8e0ed-123">Prospect-to-cash in dual-write</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]