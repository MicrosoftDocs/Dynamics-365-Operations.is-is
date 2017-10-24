---
title: "Stjórnun og stofnun afurðategunda"
description: "Þetta efnisatriði lýsir viðbótum sem hafa verið gerðar á stjórnunarupplifun fyrir afurðarflokka. Þessar viðbætur gera stjórnendum smásölu kleift að sýna fylgni milli stigveldis smásöluafurða og upplýsingar um losaðar afurðir."
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: 
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 6b9afb40b68b672514c083d99efbc9bd098dd561
ms.openlocfilehash: b158ff5b277c125e0aa158c071007ed8a0f25482
ms.contentlocale: is-is
ms.lasthandoff: 10/03/2017

---

# <a name="product-category-management-and-creation"></a><span data-ttu-id="196d3-104">Stjórnun og stofnun afurðategunda</span><span class="sxs-lookup"><span data-stu-id="196d3-104">Product category management and creation</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="196d3-105">Viðbætur sem hafa verið gerðar á stjórnunarupplifun fyrir smásöluafurðaflokka gera stjórnendum smásölu kleift að sýna fylgni milli stigveldis smásöluafurða og upplýsingar um losaðar afurðir.</span><span class="sxs-lookup"><span data-stu-id="196d3-105">Enhancements that have been made to the management experience for Retail product categories let merchandising managers have a correlation between Retail product hierarchy and released product details.</span></span> <span data-ttu-id="196d3-106">Til að skoða þessar viðbætur skal fara í vinnusvæðið **Flokkar og stjórnun vöru**  og velja  **stigveldi smásöluafurðar** til að opna síðuna **Ný bygging tegundar smásöluafurðar**.</span><span class="sxs-lookup"><span data-stu-id="196d3-106">To view these enhancements, in the **Category & product management**  workspace, select **Retail product hierarchy** to open the **New structure of Retail product category** page.</span></span> 

<span data-ttu-id="196d3-107">Í fyrri útgáfum var eiginleikum voru skipt í Helstu eiginleika vöru og smásölueiginleika voru, á grundvelli umfangs notkunareiginleika.</span><span class="sxs-lookup"><span data-stu-id="196d3-107">In previous releases, product properties were divided into Basic product properties and Retail product properties, based on the scope of their applicability.</span></span> <span data-ttu-id="196d3-108">Eiginleikar smásöluafurðar voru *altækir*.</span><span class="sxs-lookup"><span data-stu-id="196d3-108">Retail product properties were *global*.</span></span> <span data-ttu-id="196d3-109">M.ö.o., fyrir hvern eiginleiki afurðar er sama gildi deilt með öllum lögaðilum.</span><span class="sxs-lookup"><span data-stu-id="196d3-109">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="196d3-110">Helstu eiginleikar afurðar voru *sértækir fyrir hvern lögaðila*.</span><span class="sxs-lookup"><span data-stu-id="196d3-110">Basic product properties were *legal entity–specific*.</span></span> <span data-ttu-id="196d3-111">M.ö.o., tiltekinn eiginleiki afurðar gat verið mismunandi eftir lögaðilum, eftir sértækum viðskiptakröfum.</span><span class="sxs-lookup"><span data-stu-id="196d3-111">In other words, a given product property might differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="196d3-112">Með þessum viðbótum höldum við áfram, fyrir eiginleika afurða í flokknum smásöluafurð, að greina sundur reitina eftir notkunareiginleikum þeirra í hópa til að endurspegla byggingu skjámyndar fyrir upplýsingar um losaðar afurðir.</span><span class="sxs-lookup"><span data-stu-id="196d3-112">With these enhancements, for product properties in the Retail product category, we continue to separate the fields, based on their applicability within a group, to reflect the released product details form structure.</span></span>

<span data-ttu-id="196d3-113">Hægt er að skipta á milli stjórnunar á eiginleikum tiltekinna lögaðila sem eiga við alla lögaðila og stjórnunar eiginleika sem eru sértækir fyrir tiltekinn lögaðila.</span><span class="sxs-lookup"><span data-stu-id="196d3-113">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="196d3-114">Veldu bara **Skoða/breyta fyrir alla lögaðila** eða **Skoða/breyta fyrir tiltekinn lögaðila** eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="196d3-114">Just select **View/Edit for all legal entities** or **View/Edit for a specific legal entity** as you require.</span></span>

<span data-ttu-id="196d3-115">Stjórnendur smásölu geta einnig skilgreit sjálfgildi fyrir viðbótarsett eiginleika afurðar fyrir einstakar tegundir.</span><span class="sxs-lookup"><span data-stu-id="196d3-115">Merchandising managers can also define default values for an additional set of product properties at the level of an individual category.</span></span> <span data-ttu-id="196d3-116">Þessi eiginleikagildi erfast milli afurða með hliðsjón af tengslum þeirra við tegund á þeim tíma sem vara var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="196d3-116">These property values are inherited by a product, based on their association with a category at the time of product creation.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="196d3-117">Veldu eiginleika til að uppfæra afurðir af skjámyndinni tegund smásöluafurðar</span><span class="sxs-lookup"><span data-stu-id="196d3-117">Select properties to update products from the Retail product category form</span></span>

<span data-ttu-id="196d3-118">Nota má rökræna flokkunareiginleika til að velja hvaða uppfærðu eiginleika afurða eigi að senda til tengdra afurða.</span><span class="sxs-lookup"><span data-stu-id="196d3-118">You can use logical grouping properties to select which updated product properties should be pushed to associated products.</span></span>

<span data-ttu-id="196d3-119">Stjórnendur smásölu geta breytt þessum arfgengu eiginleikum afurða fyrir hverja afurð til að mæta tilteknum viðskiptakröfum.</span><span class="sxs-lookup"><span data-stu-id="196d3-119">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>

