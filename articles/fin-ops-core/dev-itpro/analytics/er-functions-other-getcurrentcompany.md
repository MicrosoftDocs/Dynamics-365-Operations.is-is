---
title: GETCURRENTCOMPANY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin GETCURRENTCOMPANY í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fcb5ef2f218a85bab25f830db583343504c46e98
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567545"
---
# <a name="getcurrentcompany-er-function"></a><span data-ttu-id="7a697-103">GETCURRENTCOMPANY ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="7a697-103">GETCURRENTCOMPANY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a697-104">Aðgerðin `GETCURRENTCOMPANY` skilar *strengja*-gildi sem sýnir kóðann fyrir lögaðilann (fyrirtæki) sem notandi er skráður inn á.</span><span class="sxs-lookup"><span data-stu-id="7a697-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a697-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="7a697-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="7a697-106">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="7a697-106">Return values</span></span>

<span data-ttu-id="7a697-107">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="7a697-107">*String*</span></span>

<span data-ttu-id="7a697-108">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="7a697-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="7a697-109">Dæmi</span><span class="sxs-lookup"><span data-stu-id="7a697-109">Example</span></span>

<span data-ttu-id="7a697-110">`GETCURRENTCOMPANY ()` skilar **USMF** fyrir notanda sem er skráður inn á **Contoso Entertainment System USA** fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="7a697-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7a697-111">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7a697-111">Additional resources</span></span>

[<span data-ttu-id="7a697-112">Other (lénsértæk virkni fyrir viðskipti)</span><span class="sxs-lookup"><span data-stu-id="7a697-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]