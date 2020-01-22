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
ms.openlocfilehash: a0b4c93a4705cd0e382b9b6c7af1d199beeceabe
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915994"
---
# <span data-ttu-id="18e0d-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="18e0d-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18e0d-104">Aðgerðin `GETCURRENTCOMPANY` skilar *strengja*-gildi sem sýnir kóðann fyrir lögaðilann (fyrirtæki) sem notandi er skráður inn á.</span><span class="sxs-lookup"><span data-stu-id="18e0d-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="18e0d-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="18e0d-105">Syntax</span></span>

```
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="18e0d-106">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="18e0d-106">Return values</span></span>

<span data-ttu-id="18e0d-107">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="18e0d-107">*String*</span></span>

<span data-ttu-id="18e0d-108">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="18e0d-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="18e0d-109">Dæmi</span><span class="sxs-lookup"><span data-stu-id="18e0d-109">Example</span></span>

<span data-ttu-id="18e0d-110">`GETCURRENTCOMPANY ()` skilar **USMF** fyrir notanda sem er skráður inn á **Contoso Entertainment System USA** fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="18e0d-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18e0d-111">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="18e0d-111">Additional resources</span></span>

[<span data-ttu-id="18e0d-112">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="18e0d-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
