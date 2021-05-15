---
title: Vörusýnishorn gæðastjórnunar
description: Í þessu efnisatriði er lýst hvernig á að setja upp sýnatöku vöru.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 495bef32d63738e367167ee69f2028bc77945cc4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956692"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="ce7e9-103">Vörusýnishorn gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="ce7e9-103">Quality management item sampling</span></span>

<span data-ttu-id="ce7e9-104">Sýnataka vöru er notuð sem hluti af gæðatengingu.</span><span class="sxs-lookup"><span data-stu-id="ce7e9-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="ce7e9-105">Hún skilgreinir magn núverandi efnislegra birgða sem þarf að skoða.</span><span class="sxs-lookup"><span data-stu-id="ce7e9-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="ce7e9-106">Sýnatökur geta verið byggðar á föstu magni, prósentu eða heillri númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="ce7e9-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="ce7e9-107">Uppsetning vörusýna</span><span class="sxs-lookup"><span data-stu-id="ce7e9-107">Set up item sampling</span></span>

<span data-ttu-id="ce7e9-108">Fylgið þessum skrefum til að setja upp sýnatöku vöru.</span><span class="sxs-lookup"><span data-stu-id="ce7e9-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="ce7e9-109">Farið í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Vörusýnishorn**.</span><span class="sxs-lookup"><span data-stu-id="ce7e9-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="ce7e9-110">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="ce7e9-110">Select **New**.</span></span>
1. <span data-ttu-id="ce7e9-111">Í reitinn **Sýnataka vöru** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ce7e9-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="ce7e9-112">Sláið inn gildi í reitnum **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="ce7e9-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="ce7e9-113">Í reitnum **Gildi** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="ce7e9-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="ce7e9-114">Þetta gildi tengist gildi fyrir tilgreint magn sem er valið í aðliggjandi reit.</span><span class="sxs-lookup"><span data-stu-id="ce7e9-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="ce7e9-115">Í hlutanum **Vinna úr** skal velja gátreitinn **Alger stöðvun** ef á að stöðva á alla lotuna eða magn pöntunarlínu ef próf mistekst.</span><span class="sxs-lookup"><span data-stu-id="ce7e9-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="ce7e9-116">Ef þessi gátreitur er hreinsaður verða aðeins vörur í gæðapöntuninni stöðvaðar ef próf mistekst.</span><span class="sxs-lookup"><span data-stu-id="ce7e9-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="ce7e9-117">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="ce7e9-117">Select **Save**.</span></span>
1. <span data-ttu-id="ce7e9-118">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ce7e9-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="ce7e9-119">Eiginleikinn *Gæðastjórnun fyrir vöruhúsaferli* bætir við nokkrum nýjum möguleikum fyrir vörusýnatöku.</span><span class="sxs-lookup"><span data-stu-id="ce7e9-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="ce7e9-120">Það bætir við hugmyndinni um *umfang vörusýnatöku* og gerir þér kleift að skilgreina heila númeraplötu sem tilgreint magn.</span><span class="sxs-lookup"><span data-stu-id="ce7e9-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="ce7e9-121">Ef þú hefur kveikt á þessum eiginleika skaltu skoða [Gæðastjórnun fyrir vöruhúsaferli](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="ce7e9-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
