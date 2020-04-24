---
title: Setja upp vöruhús fyrir flutningspantanir
description: Þetta efnisatriði lýsir því hvernig hægt er að setja upp vöruhús fyrir flutningspantanir.
author: Mirzaab
manager: tfehr
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: aa5786df72f87da992f1020bbaaa1c2185adf043
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216713"
---
# <a name="set-up-warehouses-for-transfer-orders"></a><span data-ttu-id="63ac7-103">Setja upp vöruhús fyrir flutningspantanir</span><span class="sxs-lookup"><span data-stu-id="63ac7-103">Set up warehouses for transfer orders</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63ac7-104">Nota má vöruhúsastig til að búa til þrepun sem styður pantanir á milli vöruhúsa.</span><span class="sxs-lookup"><span data-stu-id="63ac7-104">You can use warehouse levels to create a hierarchy that supports transfer orders between warehouses.</span></span> <span data-ttu-id="63ac7-105">Miðað við þessa uppsetningu, reiknar aðalröðun vöruþörf á stöku vöruhúsaþrepi og gefur út flutningstillögur frá úthlutuðu upprunavöruhúsi til að uppfylla þær.</span><span class="sxs-lookup"><span data-stu-id="63ac7-105">Based on this setup, master scheduling calculates item requirements at the individual warehouse level and generates planned transfer orders from an assigned source warehouse to fulfill them.</span></span>

1.  <span data-ttu-id="63ac7-106">Smella á **Birgðastjórnun > Uppsetning > Birgðasundurliðun > Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="63ac7-106">Click **Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>

2.  <span data-ttu-id="63ac7-107">Velja vöruhúsið sem fylla skal á.</span><span class="sxs-lookup"><span data-stu-id="63ac7-107">Select the warehouse that you want to refill.</span></span>

3.  <span data-ttu-id="63ac7-108">Í flýtiflipanum **Aðaláætlanagerð** skal velja gátreitinn **Enduráfylling**.</span><span class="sxs-lookup"><span data-stu-id="63ac7-108">On the **Master planning** FastTab, select the **Refilling** check box.</span></span>

4.  <span data-ttu-id="63ac7-109">Á svæðinu **Aðalvöruhús** skal velja vöruhúsið sem á að úthluta sem vöruhús fyrir endurhleðslu.</span><span class="sxs-lookup"><span data-stu-id="63ac7-109">In the **Main warehouse** field, select the warehouse that you want to assign as the refilling warehouse.</span></span> <span data-ttu-id="63ac7-110">Aðalröðun reiknar út flutningsþörf fyrir valið vöruhús og býr til áætlaða flutningspöntun úr úthlutaða **Aðalvöruhúsinu**.</span><span class="sxs-lookup"><span data-stu-id="63ac7-110">Master scheduling calculates a transfer requirement for the selected warehouse and generates a planned transfer order from the assigned **Main warehouse**.</span></span>
   
    > [!NOTE]
    > <P><span data-ttu-id="63ac7-111">Ef þú hreinsar gátreitinn <STRONG>Enduráfylling</STRONG> er völdu vöruhúsi úthlutað vöruhúsastigi í tengslum við <STRONG>Aðalvöruhús</STRONG>, en <STRONG>Aðalvöruhús</STRONG> er ekki uppsett sem vöruhús fyrir endurhleðslu.</span><span class="sxs-lookup"><span data-stu-id="63ac7-111">If you clear the <STRONG>Refilling</STRONG> check box, the selected warehouse is assigned a warehouse level in regard to the <STRONG>Main warehouse</STRONG>, but the <STRONG>Main warehouse</STRONG> is not set up as a refilling warehouse.</span></span></P>

5.  <span data-ttu-id="63ac7-112">Síðiunni er lokað til að nota nýju uppsetninguna.</span><span class="sxs-lookup"><span data-stu-id="63ac7-112">Close the page to apply the new setup.</span></span>


> [!TIP]
> <P><span data-ttu-id="63ac7-113">Ef úthluta á vöruhúsi fyrir enduráfyllingu verður fyrst að setja upp vöruhúsið sem geymsluvídd á síðunni <STRONG>Geymsluvíddarflokkar</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="63ac7-113">If you want to assign a warehouse for refilling, you must first set up the warehouse as a storage dimension on the <STRONG>Storage dimension groups</STRONG> page.</span></span> <span data-ttu-id="63ac7-114">Á þessari síðu skal velja reitinn <STRONG>Virkt</STRONG> og reitinn <STRONG>Þekjuáætlun eftir vídd</STRONG> fyrir vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="63ac7-114">On this page, select the <STRONG>Active</STRONG> field and the <STRONG>Coverage plan by dimension</STRONG> field for the warehouse.</span></span></P>

## <a name="set-up-transport-lead-time"></a><span data-ttu-id="63ac7-115">Setja upp afhendingartíma flutnings</span><span class="sxs-lookup"><span data-stu-id="63ac7-115">Set up transport lead time</span></span>

<span data-ttu-id="63ac7-116">Þú verður einnig að setja upp afhendingartíma flutnings milli vöruhúsanna á síðunni **Flutningsdagar**.</span><span class="sxs-lookup"><span data-stu-id="63ac7-116">You must also set up the transport lead time between the warehouses on the **Transport days** page.</span></span> 
1. <span data-ttu-id="63ac7-117">Fara í **Birgðastjórnun > Uppsetning > Dreifing > Flutningsdagar**.</span><span class="sxs-lookup"><span data-stu-id="63ac7-117">Go to **Inventory management > Setup > Distribution > Transport days**.</span></span>
2. <span data-ttu-id="63ac7-118">Í reitnum **Viðtökustaður** skal velja **vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="63ac7-118">In the **Receiving point** field, select **warehouse**.</span></span>
3. <span data-ttu-id="63ac7-119">Veljið **Sendingarvöruhús**, **Viðtökuvöruhús** og **Flutningsdagar**.</span><span class="sxs-lookup"><span data-stu-id="63ac7-119">Select the **Shipping warehouse**, **Receiving warehouse**, and **Transport days**.</span></span> 
4. <span data-ttu-id="63ac7-120">(Valfrjálst) Einnig er hægt að stilla flutningstíma, fer allt eftir flutningsmáta, undir flipanum **Flutningsdagar eftir flutningsmáta**.</span><span class="sxs-lookup"><span data-stu-id="63ac7-120">(Optional) You can also set transport time, depending on the mode of delivery, under the **Transport days per mode of delivery** tab.</span></span>
