---
title: "Taka þyngd og rúmmál gáms með í hleðslu"
description: "Í þessu efnisatriði er lýst hvernig eigi að setja upp og nota virkni til að taka með þyngd gáms og rúmtak í farmi."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5b0d8c8a3985d1f49a493615b3c69a9dbe65635f
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="include-container-weight-and-volume-on-load"></a><span data-ttu-id="f2511-103">Taka þyngd og rúmmál gáms með í hleðslu</span><span class="sxs-lookup"><span data-stu-id="f2511-103">Include container weight and volume on load</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2511-104">Virkni til aðtaka með taka með þyngd gáms og rúmtak í hleðslu gefur skýrt fram heildarþyngd og rúmmál gáma og vöru sem fer í farm.</span><span class="sxs-lookup"><span data-stu-id="f2511-104">The functionality for including the container weight and volume on a load gives a clear representation of the total weight and volume of containers and items that are going on a load.</span></span>

<span data-ttu-id="f2511-105">Farmur inniheldur eina sendingu eða margar sendingar og þessar sendingar innihalda mismunandi vörur sem tilheyra einum söluáfangi eða mörgum sölufyrirmælum.</span><span class="sxs-lookup"><span data-stu-id="f2511-105">A load contains a single shipment or multiple shipments, and these shipments contain distinct items that belong to a single sales order or multiple sales orders.</span></span> <span data-ttu-id="f2511-106">Vörurnar eru geymdar í ílát, gámi og gámum er hlaðið í farm.</span><span class="sxs-lookup"><span data-stu-id="f2511-106">The items are stored inside a container, and containers are loaded on a load.</span></span> <span data-ttu-id="f2511-107">Vörur sem ekki eru inni í gámi geta einnig verið hlit af farmi.</span><span class="sxs-lookup"><span data-stu-id="f2511-107">Items that are outside a container can also be part of a load.</span></span> <span data-ttu-id="f2511-108">Byggt á þessum skilyrðum, reiknar kerfið gildi fyrir þyngd og rúmmál í farminum með því að taka tillit til þyngdar og rúmmáls bæði gáma og hluta.</span><span class="sxs-lookup"><span data-stu-id="f2511-108">Based on these conditions, the system calculates values for the weight and volume on the load by considering the weight and volume of both containers and items.</span></span>

<span data-ttu-id="f2511-109">Ef reiknuð gildi eru ekki nákvæm, getur þú breytt þeim með því að slá inn raunveruleg gildi fyrir þyngd og rúmmál í farminum.</span><span class="sxs-lookup"><span data-stu-id="f2511-109">If the calculated values aren’t precise, you can adjust them by entering the actual values for the weight and volume on the load.</span></span> <span data-ttu-id="f2511-110">Gildin fyrir þyngd og rúmmál eru notuð í flutningsstjórnunarferlum.</span><span class="sxs-lookup"><span data-stu-id="f2511-110">The values for the weight and volume are used in transportation management processes.</span></span> <span data-ttu-id="f2511-111">Til dæmis eru gildin notuð á vinnusvæði leiðar þar sem þau hjálpa til við að skilgreina hraða og leið fyrir farma, og þau eru einnig notuð við flutningstilboð og innskráningu ökumanns.</span><span class="sxs-lookup"><span data-stu-id="f2511-111">For example, the values are used in the rate route workbench, where they help define the rate and route for loads, and they are also used for transportation tenders and driver check-in.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="f2511-112">Þar sem það á við</span><span class="sxs-lookup"><span data-stu-id="f2511-112">Where it applies</span></span>

<span data-ttu-id="f2511-113">Virknin til að taka með þyngd og rúmmál gáms í farmi gildir í flutningsstjórnunarferli, svo sem vinnusvæði leiðar, flutningstilboðum og innskráningu ökumanns.</span><span class="sxs-lookup"><span data-stu-id="f2511-113">The functionality for including the container weight and volume on a load applies in transportation management processes, such as the rate route workbench, transportation tenders, and driver check-in.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="f2511-114">Hvernig er það sett upp</span><span class="sxs-lookup"><span data-stu-id="f2511-114">How it is set up</span></span>

<span data-ttu-id="f2511-115">Fjöldi gáma sem koma til greina fyrir farm er reiknað út frá þyngd og rúmmáli gáms og nýtingarhlutfalli gáms.</span><span class="sxs-lookup"><span data-stu-id="f2511-115">The number of containers that should be considered for a load is calculated based on the weight and volume of the container, and on the percentage of the container is used.</span></span>

-   <span data-ttu-id="f2511-116">Til að stilla þyngd og rúmmál fyrir gám skal smella á  **Vöruhúsastjórnun** \> **Uppsetning** \> **Gámar** \> **Gámagerð**.</span><span class="sxs-lookup"><span data-stu-id="f2511-116">To set the weight and volume for a container, click **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>

-   <span data-ttu-id="f2511-117">Til að stilla gámanýtingarhlutfallið, smelltu á **Vöruhúsastjórnun** \> **Uppsetning** \> **Gámar** \> **Gámaflokkar** og sláðu síðan inn gildi í reitinn **Nýtingarhlutfall gáms**.</span><span class="sxs-lookup"><span data-stu-id="f2511-117">To set the container utilization percentage, click **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**, and then enter a value in the **Container utilization percentage** field.</span></span>

