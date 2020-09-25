---
title: QRCODE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin QRCODE í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: f634976d83fb4066a953b7ab09c963214415e29b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743759"
---
# <a name="qrcode-er-function"></a><span data-ttu-id="08c83-103">QRCODE ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="08c83-103">QRCODE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08c83-104">Aðgerðin `QRCODE` skilar *Íláts*-gildi sem sýnir Quick Response Code (QR-kóða) myndar fyrir tiltekinn streng á tvíundarsniði.</span><span class="sxs-lookup"><span data-stu-id="08c83-104">The `QRCODE` function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span>

## <a name="syntax"></a><span data-ttu-id="08c83-105">Málskipun</span><span class="sxs-lookup"><span data-stu-id="08c83-105">Syntax</span></span>

```vb
QRCODE (text)
```

## <a name="arguments"></a><span data-ttu-id="08c83-106">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="08c83-106">Arguments</span></span>

<span data-ttu-id="08c83-107">`text`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="08c83-107">`text`: *String*</span></span>

<span data-ttu-id="08c83-108">Gildið *Strengur* sem táknar upprunalega textann.</span><span class="sxs-lookup"><span data-stu-id="08c83-108">A *String* value that represents the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="08c83-109">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="08c83-109">Return values</span></span>

<span data-ttu-id="08c83-110">*Hólf*</span><span class="sxs-lookup"><span data-stu-id="08c83-110">*Container*</span></span>

<span data-ttu-id="08c83-111">Tvíundarstraumurinn sem myndast.</span><span class="sxs-lookup"><span data-stu-id="08c83-111">The resulting binary stream.</span></span>

## <a name="example"></a><span data-ttu-id="08c83-112">Dæmi</span><span class="sxs-lookup"><span data-stu-id="08c83-112">Example</span></span>

<span data-ttu-id="08c83-113">Þú getur stillt rafræn skýrslugerð (ER) snið til að búa til útgagnaskjal í Microsoft Office snið (Excel-vinnubækur eða Word-skjöl) með því að nota fyrirfram skilgreint sniðmát.</span><span class="sxs-lookup"><span data-stu-id="08c83-113">You can configure an Electronic reporting (ER) format to generate an outbound document in Microsoft Office format (Excel workbooks or Word documents) by using a predefined template.</span></span> <span data-ttu-id="08c83-114">Þetta sniðmát getur innihaldið hlutinn **Mynd** (Excel-vinnubók) eða **Myndstjórnun** (Word-skjal) sem staðgengil fyrir mynd QR-kóða.</span><span class="sxs-lookup"><span data-stu-id="08c83-114">This template may contain a **Picture** object (Excel workbook) or a **Picture Content Control** (Word document) as a placeholder for a QR code image.</span></span> <span data-ttu-id="08c83-115">Þú verður að bæta við stillt ER-snið þættinum **Hólf** sem verður notaður til að fylla inn í þennan staðgengil.</span><span class="sxs-lookup"><span data-stu-id="08c83-115">You need to add to the configured ER format a **Cell** element that will be used to fill this placeholder in.</span></span> <span data-ttu-id="08c83-116">Til að tilgreina hvaða upplýsingar verða geymdar í QR-kóða þarf að skilgreina bindingu fyrir þennan þátt **Hólf**.</span><span class="sxs-lookup"><span data-stu-id="08c83-116">To specify what information will be stored in a QR code, you need to define a binding for this **Cell** element.</span></span> <span data-ttu-id="08c83-117">Til dæmis er hægt að stilla slíka bindingu sem inniheldur eftirfarandi segð:</span><span class="sxs-lookup"><span data-stu-id="08c83-117">For example, you can configure such binding as containing the following expression:</span></span>

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

<span data-ttu-id="08c83-118">Þegar þú keyrir uppsett ER-snið er textagildið í reitnum **LabelText** í gagnagjafanum **model.ListOfShelfLabels** notað til að mynda mynd QR-kóða.</span><span class="sxs-lookup"><span data-stu-id="08c83-118">When you run the configured ER format, the text value of the **LabelText** field of the **model.ListOfShelfLabels** data source will be used to generate a QR code image.</span></span> <span data-ttu-id="08c83-119">Þessi mynd kemur í stað staðgengils fyrir mynd QR-kóða í skjalasniðmátinu sem er notað til að búa til skjal á útleið.</span><span class="sxs-lookup"><span data-stu-id="08c83-119">This image will replace a QR code image placeholder in the document template using to generate an outbound document.</span></span> <span data-ttu-id="08c83-120">Þegar þessi mynd af mynduðu skjali er skönnuð skilar hún textanum sem var tekinn úr reitnum **LabelText** í gagnagjafanum **model.ListOfShelfLabels**.</span><span class="sxs-lookup"><span data-stu-id="08c83-120">When this image of the generated document is scanned, it returns the text that was taken from the **LabelText** field of the **model.ListOfShelfLabels** data source.</span></span> <span data-ttu-id="08c83-121">Nánari upplýsingar er að finna í [Felldu inn myndir og form í skjöl sem þú myndar með því að nota ER](electronic-reporting-embed-images-shapes.md)</span><span class="sxs-lookup"><span data-stu-id="08c83-121">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="08c83-122">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="08c83-122">Additional resources</span></span>

[<span data-ttu-id="08c83-123">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="08c83-123">Text functions</span></span>](er-functions-category-text.md)
