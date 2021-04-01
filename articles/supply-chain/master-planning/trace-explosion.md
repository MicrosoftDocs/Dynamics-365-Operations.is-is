---
title: Nota rakningu fyrir niðurbrot
description: Þessi grein útskýrir hvernig hægt er að nota rakningu til að kanna orsakir á bak við niðurstöðu niðurbrots pöntunar.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 677b62055d71ee7ba1419fc2d7e6738b9438cb16
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216154"
---
# <a name="use-tracing-for-explosion"></a><span data-ttu-id="4cb82-103">Nota rakningu fyrir niðurbrot</span><span class="sxs-lookup"><span data-stu-id="4cb82-103">Use tracing for explosion</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4cb82-104">Þessi grein útskýrir hvernig hægt er að nota rakningu til að kanna orsakir á bak við niðurstöðu niðurbrots pöntunar.</span><span class="sxs-lookup"><span data-stu-id="4cb82-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="4cb82-105">Með því að gera rakningu, er°hægt að skoða upplýsingar um þætti sem höfðu áhrif á útkomu niðurbrots ákveðinnar pöntunar.</span><span class="sxs-lookup"><span data-stu-id="4cb82-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="4cb82-106">Eftirfarandi dæmi sýna hvernig hægt er að nota rakningarupplýsingarnar.</span><span class="sxs-lookup"><span data-stu-id="4cb82-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="4cb82-107">Skoða tengsl milli aðgerða í áætlaðum pöntunum til að betrumbæta framboðskeðju og birgðafrátekningar.</span><span class="sxs-lookup"><span data-stu-id="4cb82-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="4cb82-108">Skoða tengsl við pantanir sem þegar hafa verið samþykktar.</span><span class="sxs-lookup"><span data-stu-id="4cb82-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="4cb82-109">Hægt er að leggja áherslu á sjálfkrafa staðfestingu afleiddra þarfa og þannig forgangsraða pöntunum á réttari hátt.</span><span class="sxs-lookup"><span data-stu-id="4cb82-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="4cb82-110">Herma eftir niðurstöðum áætlunargerðar til að ákvarða hvort færibreytur áætlanagerðar eru ákjósanlegar.</span><span class="sxs-lookup"><span data-stu-id="4cb82-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="4cb82-111">Tilgreina hvernig upplýsingar, svo sem framleiðsludagsetningar, magn og forgangur fyrir pöntun var ákvarðaður.</span><span class="sxs-lookup"><span data-stu-id="4cb82-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="4cb82-112">Hægt er að skoða upplýsingar um framvirka samninga og aðgerðir fyrir valda pöntun.</span><span class="sxs-lookup"><span data-stu-id="4cb82-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="4cb82-113">Á v **Niðurbrot** síðunni er hægt að sjá upplýsingar um rakningu í flipanum **Útskýring** í efri rúðunni.</span><span class="sxs-lookup"><span data-stu-id="4cb82-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="4cb82-114">Rakning á sér stað þegar pöntun er brotin niður.</span><span class="sxs-lookup"><span data-stu-id="4cb82-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="4cb82-115">Til að hefja rakningu fyrir pöntun, smellið á **Uppfæra**, og veljið því næst gátreitinn **Leyfa rakningu**.</span><span class="sxs-lookup"><span data-stu-id="4cb82-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="4cb82-116">Hægt er að nota svæðið **Finna texta** til að leita að sérstökum upplýsingum í kladdanum.</span><span class="sxs-lookup"><span data-stu-id="4cb82-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="4cb82-117">Leitarniðurstöður eru auðkenndar í trénu.</span><span class="sxs-lookup"><span data-stu-id="4cb82-117">Search results are highlighted in the tree.</span></span>

<a name="additional-resources"></a><span data-ttu-id="4cb82-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4cb82-118">Additional resources</span></span>
--------

[<span data-ttu-id="4cb82-119">Yfirlit aðaláætlana</span><span class="sxs-lookup"><span data-stu-id="4cb82-119">Master plans overview</span></span>](master-plans.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]