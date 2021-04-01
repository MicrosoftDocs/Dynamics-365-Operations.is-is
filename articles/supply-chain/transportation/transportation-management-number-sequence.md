---
title: Númeraröð flutningsstjórnunar
description: Í þessu efnisatriði er lýst hvernig eigi að setja upp númeraraðir fyrir flutningsstjórnun.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cc19110f481c11ab28532d69a4689c1db048f6c3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233368"
---
# <a name="transportation-management-number-sequence"></a><span data-ttu-id="68ff1-103">Númeraröð flutningsstjórnunar</span><span class="sxs-lookup"><span data-stu-id="68ff1-103">Transportation management number sequence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68ff1-104">Notaðu síðuna **Númeraraðir** í flutningsstjórnunareiningunni til að setja upp ýmsar Pro-tölur.</span><span class="sxs-lookup"><span data-stu-id="68ff1-104">Use the **Number sequences** page in the transportation management module to set up various pro numbers.</span></span> <span data-ttu-id="68ff1-105">Pro-tölur eru notaðar af flutningsaðilum til að skipuleggja og rekja framvindu hverrar sendingar.</span><span class="sxs-lookup"><span data-stu-id="68ff1-105">Pro numbers are used by carriers to organize and track the progress of each shipment.</span></span>

## <a name="create-a-number-sequence-for-a-pro-number"></a><span data-ttu-id="68ff1-106">Búa til númeraröð fyrir Pro-númer</span><span class="sxs-lookup"><span data-stu-id="68ff1-106">Create a number sequence for a pro number</span></span>

<span data-ttu-id="68ff1-107">Gerðu eftirfarandi til að búa til númeraröð fyrir Pro-númer:</span><span class="sxs-lookup"><span data-stu-id="68ff1-107">To create a number sequence for a pro number, do the following:</span></span>

1. <span data-ttu-id="68ff1-108">Opnið **Flutningsstjórnun \> Uppsetning \> Flutningsaðilar \> Númeraraðir**.</span><span class="sxs-lookup"><span data-stu-id="68ff1-108">Go to **Transportation management \> Setup \> Carriers \> Number sequences**.</span></span>
1. <span data-ttu-id="68ff1-109">Velja skal **Nýtt** til að búa til nýja númeraröð.</span><span class="sxs-lookup"><span data-stu-id="68ff1-109">Select **New** to create a new number sequence.</span></span>
1. <span data-ttu-id="68ff1-110">Færið inn einkvæmt kenni og lýsandi heiti fyrir númeraröðina.</span><span class="sxs-lookup"><span data-stu-id="68ff1-110">Enter a unique ID and descriptive name for the number sequence.</span></span>
1. <span data-ttu-id="68ff1-111">Á svæðinu **Gerð númeraraðar** er *Pro-númer* eini valkosturinn.</span><span class="sxs-lookup"><span data-stu-id="68ff1-111">In the **Number sequence type** field, *Pro number* is the only option.</span></span>
1. <span data-ttu-id="68ff1-112">Í reitnum **Vartala**, er *Vartala* eini valkosturinn og er settur upp sem almenn vél.</span><span class="sxs-lookup"><span data-stu-id="68ff1-112">In the **Check digit** field, *Check digit* is the only option and is set up as a generic engine.</span></span>
1. <span data-ttu-id="68ff1-113">Á flipanum **Röð** skal veita upplýsingar um röðina.</span><span class="sxs-lookup"><span data-stu-id="68ff1-113">On the **Sequence** FastTab, provide information about the sequence.</span></span>
1. <span data-ttu-id="68ff1-114">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="68ff1-114">Close the page.</span></span>

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a><span data-ttu-id="68ff1-115">Tengja númeraröð við farmflytjanda</span><span class="sxs-lookup"><span data-stu-id="68ff1-115">Link a number sequence to a shipping carrier</span></span>

<span data-ttu-id="68ff1-116">Til að tengja númeraröð við flutningsaðila skal gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="68ff1-116">To link a number sequence to a carrier, do the following:</span></span>

1. <span data-ttu-id="68ff1-117">Opnið **Flutningsstjórnun \> Uppsetning \> Flutningsaðilar \> Farmflytjendur**.</span><span class="sxs-lookup"><span data-stu-id="68ff1-117">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="68ff1-118">Velja farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="68ff1-118">Select a shipping carrier.</span></span>
1. <span data-ttu-id="68ff1-119">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="68ff1-119">Select **Edit**.</span></span>
1. <span data-ttu-id="68ff1-120">Á flýtiflipanum **Yfirlit** skaltu velja kost á svæðinu **Pro-númeraröð**.</span><span class="sxs-lookup"><span data-stu-id="68ff1-120">On the **Overview** FastTab, select an option in the **Pro number sequence** field.</span></span>
1. <span data-ttu-id="68ff1-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="68ff1-121">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]