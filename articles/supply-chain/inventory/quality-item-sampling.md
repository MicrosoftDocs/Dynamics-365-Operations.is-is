---
title: Vörusýnishorn gæðastjórnunar
description: Í þessu efnisatriði er lýst hvernig á að setja upp sýnatöku vöru.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae8bfd329ca0d7c30adcd93a759ee6bea7b76278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022229"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="f6039-103">Vörusýnishorn gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="f6039-103">Quality management item sampling</span></span>

<span data-ttu-id="f6039-104">Sýnataka vöru er notuð sem hluti af gæðatengingu.</span><span class="sxs-lookup"><span data-stu-id="f6039-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="f6039-105">Hún skilgreinir magn núverandi efnislegra birgða sem þarf að skoða.</span><span class="sxs-lookup"><span data-stu-id="f6039-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="f6039-106">Sýnatökur geta verið byggðar á föstu magni, prósentu eða heillri númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="f6039-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="f6039-107">Uppsetning vörusýna</span><span class="sxs-lookup"><span data-stu-id="f6039-107">Set up item sampling</span></span>

<span data-ttu-id="f6039-108">Fylgið þessum skrefum til að setja upp sýnatöku vöru.</span><span class="sxs-lookup"><span data-stu-id="f6039-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="f6039-109">Farið í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Vörusýnishorn**.</span><span class="sxs-lookup"><span data-stu-id="f6039-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="f6039-110">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f6039-110">Select **New**.</span></span>
1. <span data-ttu-id="f6039-111">Í reitinn **Sýnataka vöru** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f6039-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="f6039-112">Sláið inn gildi í reitnum **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="f6039-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="f6039-113">Í reitnum **Gildi** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f6039-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="f6039-114">Þetta gildi tengist gildi fyrir tilgreint magn sem er valið í aðliggjandi reit.</span><span class="sxs-lookup"><span data-stu-id="f6039-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="f6039-115">Í hlutanum **Vinna úr** skal velja gátreitinn **Alger stöðvun** ef á að stöðva á alla lotuna eða magn pöntunarlínu ef próf mistekst.</span><span class="sxs-lookup"><span data-stu-id="f6039-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="f6039-116">Ef þessi gátreitur er hreinsaður verða aðeins vörur í gæðapöntuninni stöðvaðar ef próf mistekst.</span><span class="sxs-lookup"><span data-stu-id="f6039-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="f6039-117">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f6039-117">Select **Save**.</span></span>
1. <span data-ttu-id="f6039-118">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f6039-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="f6039-119">Eiginleikinn *Gæðastjórnun fyrir vöruhúsaferli* bætir við nokkrum nýjum möguleikum fyrir vörusýnatöku.</span><span class="sxs-lookup"><span data-stu-id="f6039-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="f6039-120">Það bætir við hugmyndinni um *umfang vörusýnatöku* og gerir þér kleift að skilgreina heila númeraplötu sem tilgreint magn.</span><span class="sxs-lookup"><span data-stu-id="f6039-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="f6039-121">Ef þú hefur kveikt á þessum eiginleika skaltu skoða [Gæðastjórnun fyrir vöruhúsaferli](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="f6039-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
