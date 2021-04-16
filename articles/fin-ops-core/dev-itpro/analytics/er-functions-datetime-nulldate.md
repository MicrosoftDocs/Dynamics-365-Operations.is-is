---
title: NULLDATE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NULLDATE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 6ac8da3f18c7793512685d52dd64a9bd55bfb8fc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746844"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="d1a09-103">NULLDATE ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="d1a09-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1a09-104">Aðgerðin `NULLDATE` skilar *Dagsetningar*-gildi sem táknar **núll** dagsetningu (1. janúar, 1900).</span><span class="sxs-lookup"><span data-stu-id="d1a09-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1a09-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="d1a09-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="d1a09-106">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="d1a09-106">Return values</span></span>

<span data-ttu-id="d1a09-107">*Dagsetning*</span><span class="sxs-lookup"><span data-stu-id="d1a09-107">*Date*</span></span>

<span data-ttu-id="d1a09-108">Dagsetningargildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="d1a09-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="d1a09-109">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="d1a09-109">Example 1</span></span>

<span data-ttu-id="d1a09-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` skilar **núll** dagsetningu, 1. janúar, 1900, sem **"1900-01-01"**, byggt á tilgreindu sérsniðnu sniði.</span><span class="sxs-lookup"><span data-stu-id="d1a09-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="d1a09-111">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="d1a09-111">Example 2</span></span>

<span data-ttu-id="d1a09-112">Segðin `IF( Invoice.DocumentDate = NULLDATE(), true, false)` skilar **True** þegar gildið í reitnum **DocumentDate** er jafnt og **núll** dagsetning.</span><span class="sxs-lookup"><span data-stu-id="d1a09-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="d1a09-113">Í þessu dæmi er **Invoice** gagnagjafi rafrænnar skýrslugerðar (ER) fyrir gerðina **Fjármála-/töfluskrá** og vísar til CustInvoiceJour-töflunnar.</span><span class="sxs-lookup"><span data-stu-id="d1a09-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d1a09-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d1a09-114">Additional resources</span></span>

[<span data-ttu-id="d1a09-115">Dagsetningar og tímavirkni</span><span class="sxs-lookup"><span data-stu-id="d1a09-115">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]