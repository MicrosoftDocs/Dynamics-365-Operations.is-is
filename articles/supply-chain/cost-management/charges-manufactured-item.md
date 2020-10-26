---
title: Birta gjöld fyrir framleidda vöru
description: Fastur kostnaður framleiddrar vöru endurspeglar uppsetningartíma og íhlutina sem eru með föstu magni eða fastri rýrnunartölu.
author: AndersGirke
manager: tfehr
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: c5e0175e5743c800d8f04723d03ae503cff3a67a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975898"
---
# <a name="display-charges-for-a-manufactured-item"></a><span data-ttu-id="4be6b-103">Birta gjöld fyrir framleidda vöru</span><span class="sxs-lookup"><span data-stu-id="4be6b-103">Display charges for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4be6b-104">Fastur kostnaður framleiddrar vöru endurspeglar uppsetningartíma og íhlutina sem eru með föstu magni eða fastri rýrnunartölu.</span><span class="sxs-lookup"><span data-stu-id="4be6b-104">The constant costs of a manufactured item reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span>

<span data-ttu-id="4be6b-105">Hægt er að birta reiknaða upphæð kostnaðar vöru með einingarkostnaði vörunnar.</span><span class="sxs-lookup"><span data-stu-id="4be6b-105">The calculated amount of an item's charges can be displayed with the item's unit costs.</span></span> <span data-ttu-id="4be6b-106">Gjöldin birtast stundum í tveimur reitum en birtast ekki sem hluti af einingarkostnaði vörunnar.</span><span class="sxs-lookup"><span data-stu-id="4be6b-106">However, the charges are sometimes displayed as separate fields, and they are not included in the item's unit costs.</span></span> <span data-ttu-id="4be6b-107">Þegar gjöld birtast sem sérstök svæði birtir eitt svæði heildarupphæð gjalda og annað svæði birtir þá lotustærð kostnaðar sem var notuð til að afskrifa upphæðina.</span><span class="sxs-lookup"><span data-stu-id="4be6b-107">When the charges appear as separate fields, one field displays the total amount of charges, and another field displays the costing lot size that is used to amortize the amount.</span></span> <span data-ttu-id="4be6b-108">Síðan Vöruverð birtir t.d. gjöld sem tvö aðskilin svæði.</span><span class="sxs-lookup"><span data-stu-id="4be6b-108">The Item price page, for example, displays the charges as two separate fields.</span></span> <span data-ttu-id="4be6b-109">Síðan Lokið birtir hins vegar heildarkostnað á einingu og afksriftarkostnað sem er innifalinn í einingarkostnaðinum.</span><span class="sxs-lookup"><span data-stu-id="4be6b-109">However, the Complete page displays the item's total cost per unit, and the amortized costs are included in the unit costs.</span></span>

<span data-ttu-id="4be6b-110">Gjöld framleiddrar vöru eru alltaf í einingarkostnaði vegna staðlaðs kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="4be6b-110">The charges for a manufactured item are always included in the item's unit cost for standard cost purposes.</span></span> <span data-ttu-id="4be6b-111">Þau má einnig hafa með í áætluðum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="4be6b-111">They can optionally be included for planned cost purposes.</span></span> <span data-ttu-id="4be6b-112">Regla í kostnaðarútgáfunni sér til þess að gjöld eru höfð með í kostnaði framleiddrar vöru.</span><span class="sxs-lookup"><span data-stu-id="4be6b-112">A policy in the costing version enforces the inclusion of charges in the cost of a manufactured item.</span></span> <span data-ttu-id="4be6b-113">Þegar kostnaðarfærsla vöru er gerð virk uppfærast gjöld fyrir grunnkostnaðarupplýsingar vörunnar, eins og þær birtast á síðunni Vörukostnaður.</span><span class="sxs-lookup"><span data-stu-id="4be6b-113">When you activate an item's cost record, you update the charges for the item's base cost information, which is displayed in the Item price page.</span></span> <span data-ttu-id="4be6b-114">Gjöldin birtast í tveimur svæðum en birtast ekki sem hluti af einingarkostnaði vörunnar.</span><span class="sxs-lookup"><span data-stu-id="4be6b-114">The charges are displayed as two separate fields, and they are not included in the item's unit cost.</span></span> <span data-ttu-id="4be6b-115">Í hvert sinn sem færslan er gerð virk uppfærast upplýsingar um grunnkostnað vörunnar, jafnvel þó að virkjunin endurspegli önnur svæði.</span><span class="sxs-lookup"><span data-stu-id="4be6b-115">Each activation updates the item's base cost information, even if the activation reflects different sites.</span></span> <span data-ttu-id="4be6b-116">Upplýsingar um grunnkostnað ætti því að skoða sem tilvísunarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="4be6b-116">Therefore, you should view the base cost information as reference information.</span></span>





