---
title: Framlengja gagnaeiningar tiltækra birgða
description: Í þessu efnisatriði er að finna dæmi sem sýnir hvernig á að bæta stækkuðum reitum við yfirlit INVENTORSITEONHANDENTITY and INVENTWAREHOUSEONHANDENTITY þannig að möguleikar gagnaeininga lagerbirgða geti virkað með stækkuninni.
author: sherry-zheng
manager: tfehr
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e3bf3a7d48b0aa3e48845882be0ee86da17ed040
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430404"
---
# <a name="extend-inventory-on-hand-data-entities"></a><span data-ttu-id="14d57-103">Framlengja gagnaeiningar tiltækra birgða</span><span class="sxs-lookup"><span data-stu-id="14d57-103">Extend inventory on-hand data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14d57-104">Microsoft Dynamics 365 Supply Chain Management býður upp á eiginleika [stækkunarhæfni](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) sem gera kleift að [bæta reitum við töflur í gegnum stækkun](../../fin-ops-core/dev-itpro/extensibility/add-field-extension).</span><span class="sxs-lookup"><span data-stu-id="14d57-104">Microsoft Dynamics 365 Supply Chain Management provides [extensibility](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) features that let you [add fields to tables through extension](../../fin-ops-core/dev-itpro/extensibility/add-field-extension).</span></span> <span data-ttu-id="14d57-105">Í þessu efnisatriði er að finna dæmi sem sýnir hvernig á að bæta stækkuðum reitum við yfirlit `INVENTORSITEONHANDENTITY` og `INVENTWAREHOUSEONHANDENTITY` þannig að möguleikar gagnaeininga lagerbirgða geti virkað með stækkuninni.</span><span class="sxs-lookup"><span data-stu-id="14d57-105">This topic provides an example that shows how to add extended fields to the `INVENTORSITEONHANDENTITY` and `INVENTWAREHOUSEONHANDENTITY` views, so that the capabilities of the inventory on-hand data entities can work with the extensions.</span></span> <span data-ttu-id="14d57-106">Frekari upplýsingar um gagnaeiningar er að finna í [Yfirlit gagnastjórnunar](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="14d57-106">For more information about data entities, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="14d57-107">Hér er listi yfir sumar gagnaeiningar lagerbirgðanna:</span><span class="sxs-lookup"><span data-stu-id="14d57-107">Here is a list of some of the inventory on-hand data entities:</span></span>
>
> - <span data-ttu-id="14d57-108">Birgðir á lager eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="14d57-108">Inventory on-hand by site</span></span>
> - <span data-ttu-id="14d57-109">Birgðir á lager eftir staðsetningu V2</span><span class="sxs-lookup"><span data-stu-id="14d57-109">Inventory on-hand by site V2</span></span>
> - <span data-ttu-id="14d57-110">Birgðir á lager eftir vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="14d57-110">Inventory on-hand by warehouse</span></span>
> - <span data-ttu-id="14d57-111">Birgðir á lager eftir vöruhúsi v2</span><span class="sxs-lookup"><span data-stu-id="14d57-111">Inventory on-hand by warehouse v2</span></span>

<span data-ttu-id="14d57-112">Eftir að reitum hefur verið bætt við töflurnar sem eru notaðar af `inventSiteOnHandView`-yfirlitinu, þarf að samstilla vélina þannig að stækkanirnar verði þekktar á réttan hátt.</span><span class="sxs-lookup"><span data-stu-id="14d57-112">After you add fields to tables that are used by the `inventSiteOnHandView` view, you must sync the engine so that the extensions are correctly recognized.</span></span>

1. <span data-ttu-id="14d57-113">Stækkið `InventSiteOnHandView`-yfirlitið með því að bæta við stækkuðum reit.</span><span class="sxs-lookup"><span data-stu-id="14d57-113">Extend the `InventSiteOnHandView` view by adding the extension field.</span></span>
1. <span data-ttu-id="14d57-114">Stækkið `InventSiteOnHandAggregatedView`-yfirlitið með stækkuðum reitum.</span><span class="sxs-lookup"><span data-stu-id="14d57-114">Extend the `InventSiteOnHandAggregatedView` view with the extension fields.</span></span>
1. <span data-ttu-id="14d57-115">Stækkið `InventSiteOnHandAggregatedViewBuilder` viewBuilder-klasann með því að breyta `getExtensionFields()`-aðferðinni.</span><span class="sxs-lookup"><span data-stu-id="14d57-115">Extend the `InventSiteOnHandAggregatedViewBuilder` viewBuilder class by modifying the `getExtensionFields()` method.</span></span> <span data-ttu-id="14d57-116">Á þennan hátt er gömlum yfirlitsreitum varpað í nýja yfirlitsreiti þegar samstilling viewBuilder er keyrð.</span><span class="sxs-lookup"><span data-stu-id="14d57-116">In this way, you map old view fields to new view fields when viewBuilder synchronization is run.</span></span>

<span data-ttu-id="14d57-117">Til dæmis hefur eftirfarandi fjórum reitum verið bætt við `InventTable`-töfluna í gegnum stækkun:</span><span class="sxs-lookup"><span data-stu-id="14d57-117">For example, you've added the following four fields to the `InventTable` table through extension:</span></span>

- <span data-ttu-id="14d57-118">Sérstilltur reitur 1</span><span class="sxs-lookup"><span data-stu-id="14d57-118">Custom field 1</span></span>
- <span data-ttu-id="14d57-119">Sérstilltur reitur 2</span><span class="sxs-lookup"><span data-stu-id="14d57-119">Custom field 2</span></span>
- <span data-ttu-id="14d57-120">Sérstilltur reitur 3</span><span class="sxs-lookup"><span data-stu-id="14d57-120">Custom field 3</span></span>
- <span data-ttu-id="14d57-121">Sérstilltur reitur 4</span><span class="sxs-lookup"><span data-stu-id="14d57-121">Custom field 4</span></span>

<span data-ttu-id="14d57-122">Í tilfellinu þarf að breyta `getExtensionFields()`-aðferðinni á eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="14d57-122">In the case, you must modify the `getExtensionFields()` method in the following way.</span></span>

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

<span data-ttu-id="14d57-123">Eftir að þessum skrefum er lokið er hægt að stækka gagnaeiningarnar fyrir birgðir á lager eftir svæði og birgðir á lager eftir vöruhúsi með því að bæta nýju reitunum við.</span><span class="sxs-lookup"><span data-stu-id="14d57-123">After you complete these steps, you can extend the inventory on-hand by site and inventory on-hand by warehouse data entities by adding the new fields.</span></span> <span data-ttu-id="14d57-124">Á þennan hátt er tryggt að stækkuðu reitirnir verði þekktir og hafðir með við gagnaflutning sem notar þessar gagnaeiningar.</span><span class="sxs-lookup"><span data-stu-id="14d57-124">In this way, you ensure that the extended fields are recognized and included during data migration that uses those data entities.</span></span>
