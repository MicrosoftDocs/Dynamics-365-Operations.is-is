---
title: SPLITLISTBYLIMIT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin SPLITLISTBYLIMIT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: eb492560a453ec59bb82d24dd6717f409bd8b257
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745546"
---
# <a name="splitlistbylimit-er-function"></a><span data-ttu-id="32041-103">SPLITLISTBYLIMIT ER-aðgerð</span><span class="sxs-lookup"><span data-stu-id="32041-103">SPLITLISTBYLIMIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32041-104">Aðgerðin `SPLITLISTBYLIMIT` skiptir upp tilteknum lista í nýjan lista yfir undirlista (runur).</span><span class="sxs-lookup"><span data-stu-id="32041-104">The `SPLITLISTBYLIMIT` function splits the specified list into a new list of sublists (batches).</span></span> <span data-ttu-id="32041-105">Fjöldi skráninga í hverri lotu er reiknaður með virkum hætti.</span><span class="sxs-lookup"><span data-stu-id="32041-105">The number of records in each batch is dynamically calculated.</span></span> <span data-ttu-id="32041-106">Aðgerðin skilar síðan niðurstöðunni sem nýju *Skráalista*-gildi sem samanstendur af rununum.</span><span class="sxs-lookup"><span data-stu-id="32041-106">The function then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="32041-107">Málskipun</span><span class="sxs-lookup"><span data-stu-id="32041-107">Syntax</span></span>

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a><span data-ttu-id="32041-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="32041-108">Arguments</span></span>

<span data-ttu-id="32041-109">`list`: *Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="32041-109">`list`: *Record list*</span></span>

<span data-ttu-id="32041-110">Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.</span><span class="sxs-lookup"><span data-stu-id="32041-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="32041-111">`limit value`: *Heiltala* eða *Raun*</span><span class="sxs-lookup"><span data-stu-id="32041-111">`limit value`: *Integer* or *Real*</span></span>

<span data-ttu-id="32041-112">Hámarksgildið fyrir mörkin sem eru notuð til að skipta upprunalegu listanum í runur.</span><span class="sxs-lookup"><span data-stu-id="32041-112">The maximum value of the limit that is used to split the original list into batches.</span></span>

<span data-ttu-id="32041-113">`limit source`: *Reitur*</span><span class="sxs-lookup"><span data-stu-id="32041-113">`limit source`: *Field*</span></span>

<span data-ttu-id="32041-114">Gild slóð á reit af gerðinni *Heiltala* eða *Raun* í tilgreindum lista.</span><span class="sxs-lookup"><span data-stu-id="32041-114">The valid path of a field of the *Integer* or *Real* type in the specified list.</span></span> <span data-ttu-id="32041-115">Gildi þessa reits skilgreinir skrefið sem heildarupphæðin er aukin á.</span><span class="sxs-lookup"><span data-stu-id="32041-115">The value of this field defines the step that the total sum is increased on.</span></span>

## <a name="return-values"></a><span data-ttu-id="32041-116">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="32041-116">Return values</span></span>

<span data-ttu-id="32041-117">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="32041-117">*Record list*</span></span>

<span data-ttu-id="32041-118">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="32041-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="32041-119">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="32041-119">Usage notes</span></span>

<span data-ttu-id="32041-120">Listi yfir runur sem er skilað inniheldur eftirfarandi þætti:</span><span class="sxs-lookup"><span data-stu-id="32041-120">The list of batches that is returned contains the following elements:</span></span>

- <span data-ttu-id="32041-121">**Gildi**: *Listi*</span><span class="sxs-lookup"><span data-stu-id="32041-121">**Value**: *List*</span></span>

    <span data-ttu-id="32041-122">Listi yfir skrár sem tilheyra núverandi runu.</span><span class="sxs-lookup"><span data-stu-id="32041-122">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="32041-123">**BatchNumber**: *Heiltala*</span><span class="sxs-lookup"><span data-stu-id="32041-123">**BatchNumber**: *Integer*</span></span>

    <span data-ttu-id="32041-124">Númer gildandi runu í skiluðum lista.</span><span class="sxs-lookup"><span data-stu-id="32041-124">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="32041-125">Markinu er ekki beitt á staka vöru á upprunalega listanum ef upprunamarkið fer yfir skilgreind mörk.</span><span class="sxs-lookup"><span data-stu-id="32041-125">The limit isn't applied to a single item of the original list if the limit source exceeds the defined limit.</span></span>

## <a name="example"></a><span data-ttu-id="32041-126">Dæmi</span><span class="sxs-lookup"><span data-stu-id="32041-126">Example</span></span>

<span data-ttu-id="32041-127">Eftirfarandi skýringarmynd sýnir snið rafrænnar skýrslugerðar (ER).</span><span class="sxs-lookup"><span data-stu-id="32041-127">The following illustration shows an Electronic reporting (ER) format.</span></span>

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

<span data-ttu-id="32041-128">Eftirfarandi skýringarmynd sýnir gagnagjafana sem eru notaðir fyrir sniðið.</span><span class="sxs-lookup"><span data-stu-id="32041-128">The following illustration shows the data sources that are used for the format.</span></span>

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

<span data-ttu-id="32041-129">Eftirfarandi mynd sýnir niðurstöðuna þegar sniðið er keyrt.</span><span class="sxs-lookup"><span data-stu-id="32041-129">The following illustration shows the result when the format is run.</span></span> <span data-ttu-id="32041-130">Í þessu tilviki er úttakið flatur listi yfir vörutegundir.</span><span class="sxs-lookup"><span data-stu-id="32041-130">In this case, the output is a flat list of commodity items.</span></span>

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

<span data-ttu-id="32041-131">Í eftirfarandi myndum hefur sama sniðið verið breytt þannig að það birtir listann yfir vörutegundir í runum ef ein runa verður að innihalda vörutegundir og heildarþyngdin ætti ekki að fara yfir hámarkið 9.</span><span class="sxs-lookup"><span data-stu-id="32041-131">In the following illustrations, the same format has been adjusted so that it presents the list of commodity items in batches if a single batch must include commodities and the total weight should not exceed a limit of 9.</span></span>

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

<span data-ttu-id="32041-132">Eftirfarandi mynd sýnir niðurstöðurnar þegar stillt snið er keyrt.</span><span class="sxs-lookup"><span data-stu-id="32041-132">The following illustration shows the result when the adjusted format is run.</span></span>

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> <span data-ttu-id="32041-133">Mark er ekki beitt á síðasta hlut í upprunalistanum, vegna þess að gildi (**11**) mörkum upprunans (**þyngd**) fer yfir skilgreind mörk (**9**).</span><span class="sxs-lookup"><span data-stu-id="32041-133">The limit isn't applied to the last item of the original list, because the value (**11**) of the limit source (**weight**) exceeds the defined limit (**9**).</span></span> <span data-ttu-id="32041-134">Til að hunsa undirlista við skýrslumyndun skal nota annaðhvort aðgerðina `WHERE` eða segðina **Virkjað** í samsvarandi sniðmátsþætti, eftir því sem þarf.</span><span class="sxs-lookup"><span data-stu-id="32041-134">To ignore sublists during report generation, use either the `WHERE` function or the **Enabled** expression of the corresponding format element, as you require.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32041-135">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="32041-135">Additional resources</span></span>

[<span data-ttu-id="32041-136">Listavirkni</span><span class="sxs-lookup"><span data-stu-id="32041-136">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]