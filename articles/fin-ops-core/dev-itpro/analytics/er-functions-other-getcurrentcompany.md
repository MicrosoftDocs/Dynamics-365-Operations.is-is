---
title: GETCURRENTCOMPANY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin GETCURRENTCOMPANY í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e3c164c6d54d8387eed5018219da5fd82c765c8
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744123"
---
# <a name="getcurrentcompany-er-function"></a><span data-ttu-id="d1889-103">GETCURRENTCOMPANY ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="d1889-103">GETCURRENTCOMPANY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1889-104">Aðgerðin `GETCURRENTCOMPANY` skilar *strengja*-gildi sem sýnir kóðann fyrir lögaðilann (fyrirtæki) sem notandi er skráður inn á.</span><span class="sxs-lookup"><span data-stu-id="d1889-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1889-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="d1889-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="d1889-106">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="d1889-106">Return values</span></span>

<span data-ttu-id="d1889-107">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="d1889-107">*String*</span></span>

<span data-ttu-id="d1889-108">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="d1889-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d1889-109">Dæmi</span><span class="sxs-lookup"><span data-stu-id="d1889-109">Example</span></span>

<span data-ttu-id="d1889-110">`GETCURRENTCOMPANY ()` skilar **USMF** fyrir notanda sem er skráður inn á **Contoso Entertainment System USA** fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="d1889-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d1889-111">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d1889-111">Additional resources</span></span>

[<span data-ttu-id="d1889-112">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="d1889-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
