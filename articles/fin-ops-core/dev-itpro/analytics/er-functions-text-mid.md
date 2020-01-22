---
title: MID ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin MID í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: e178b01740954b46e2afbd2a2be6200a652a18c0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915603"
---
# <span data-ttu-id="c7ca7-103"><a name="MID">MID ER aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="c7ca7-103"><a name="MID">MID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7ca7-104">Aðgerðin `MID` skilar *strengjagildi* sem sýnir tilgreindan fjölda staftákna frá tilteknum streng, með upphafi í tilgreindri stöðu.</span><span class="sxs-lookup"><span data-stu-id="c7ca7-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7ca7-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="c7ca7-105">Syntax</span></span>

```
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="c7ca7-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="c7ca7-106">Arguments</span></span>

<span data-ttu-id="c7ca7-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="c7ca7-107">`text`: *String*</span></span>

<span data-ttu-id="c7ca7-108">Gildið *Strengur* sem tilgreinir textann sem á að skila staftáknum úr.</span><span class="sxs-lookup"><span data-stu-id="c7ca7-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="c7ca7-109">`starting position`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="c7ca7-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="c7ca7-110">Gildið *Heiltala* sem tilgreinir staðsetningu fyrsta stafsins sem þarf að skila úr tilgreindum texta.</span><span class="sxs-lookup"><span data-stu-id="c7ca7-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="c7ca7-111">`number of characters`: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="c7ca7-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="c7ca7-112">Gildið *Heiltala* sem tilgreinir fjölda stafa sem þarf að skila, frá tilgreindri upphafsstöðu.</span><span class="sxs-lookup"><span data-stu-id="c7ca7-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="c7ca7-113">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="c7ca7-113">Return values</span></span>

<span data-ttu-id="c7ca7-114">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="c7ca7-114">*String*</span></span>

<span data-ttu-id="c7ca7-115">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="c7ca7-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c7ca7-116">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="c7ca7-116">Usage notes</span></span>

<span data-ttu-id="c7ca7-117">Ef gildi frumbreytunnar `starting position` er lægra en 0 (núll) eru stafirnir sem er skilað taldir frá fyrstu stöðu í tilgreindum streng.</span><span class="sxs-lookup"><span data-stu-id="c7ca7-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="c7ca7-118">Ef gildi frumbreytunnar `starting position` er lengra en tilgreindur strengur er tómum streng skilað.</span><span class="sxs-lookup"><span data-stu-id="c7ca7-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="c7ca7-119">Dæmi</span><span class="sxs-lookup"><span data-stu-id="c7ca7-119">Example</span></span>

<span data-ttu-id="c7ca7-120">`MID ("Sample", 2, 3)` skilar **"amp"**.</span><span class="sxs-lookup"><span data-stu-id="c7ca7-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7ca7-121">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c7ca7-121">Additional resources</span></span>

[<span data-ttu-id="c7ca7-122">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="c7ca7-122">Text functions</span></span>](er-functions-category-text.md)
