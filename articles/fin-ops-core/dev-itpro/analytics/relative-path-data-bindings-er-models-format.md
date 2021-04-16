---
title: Notaðu viðeigandi slóð í gagnabindingum ER-líkana og sniða
description: Í rafrænu skýrsluverkfæri er hægt að skilgreina skipulag rafræns sniðs og lýsa því síðan hvernig á að fylla þetta út.
author: NickSelin
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 141d58c2183c386584b0b974f4997e7a81ef3109
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749987"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a><span data-ttu-id="414d4-103">Notaðu viðeigandi slóð í gagnabindingum ER-líkana og sniða</span><span class="sxs-lookup"><span data-stu-id="414d4-103">Use a relative path in data bindings of ER models and formats</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="414d4-104">Verkfærið Rafræn skýrslugerð (ER) gerir notendum kleift að skilgreina skipulag á rafrænu sniði og lýsa síðan hvernig fylla skal út þetta skipulag með því að nota gögn og reiknirit sem eru til í forritinu.</span><span class="sxs-lookup"><span data-stu-id="414d4-104">The Electronic reporting (ER) tool lets users define electronic format structures and then describe how those structures should be filled by using data and algorithms that exist in the application.</span></span> <span data-ttu-id="414d4-105">Frekari upplýsingar er að finna í [Stofna skilgreiningar rafrænnar skýrslugerðar (ER)](electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="414d4-105">For more information, see [Create Electronic reporting (ER) configurations](electronic-reporting-configuration.md).</span></span> <span data-ttu-id="414d4-106">Til að tilgreina gagnaflæði til að sækja gögn úr Finance and Operations og nota þau til að búa til rafrænt skjal þarftu að gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="414d4-106">To specify the data flow for retrieving Finance and Operations data and using it to generate  an electronic document, you need to do the following:</span></span>

- <span data-ttu-id="414d4-107">Binda skilgreindar gagnaveitur við einingar fyrir tilgreint lénsháð [gagnalíkan](general-electronic-reporting.md#data-model-and-model-mapping-components).</span><span class="sxs-lookup"><span data-stu-id="414d4-107">Bind configured data sources to elements of the designed domain-specific [data model](general-electronic-reporting.md#data-model-and-model-mapping-components).</span></span> <span data-ttu-id="414d4-108">Skipulag líkans og valdir gagnagjafar kunna að vera hluti af flóknu stigveldisskipulagi.</span><span class="sxs-lookup"><span data-stu-id="414d4-108">The model structure and selected data sources might be part of a complex hierarchical structure.</span></span> <span data-ttu-id="414d4-109">Vegna þessa geta endanleg bindingar verið mjög stórar og innihaldið margar einingar af mismunandi gerðum (til dæmis vensl, töflur og aðferðir).</span><span class="sxs-lookup"><span data-stu-id="414d4-109">Because of this, final bindings can be quite large and contain many elements of different types (for example, relations, tables, and methods,).</span></span> <span data-ttu-id="414d4-110">Bindingarnar geta orðið minna læsilegar og nokkuð flóknar yfirferðar og skilnings, sérstaklega fyrir aðra en eigendur.</span><span class="sxs-lookup"><span data-stu-id="414d4-110">The bindings can become less readable and quite complex to review and understand, especially for non-owners.</span></span> 
- <span data-ttu-id="414d4-111">Binda gagnalíkanseiningar við [snið](general-electronic-reporting.md#FormatComponentOutbound) íhluti til að skilgreina hvaða gögn verða fyllt úr gagnalíkaninu á frálagið.</span><span class="sxs-lookup"><span data-stu-id="414d4-111">Bind data model elements with [format](general-electronic-reporting.md#FormatComponentOutbound) components to define what data will be populated from the data model to the generated format’s output.</span></span>

<span data-ttu-id="414d4-112">Til að bæta notagildi vörpunarhönnuða rafrænnar skýrslugerðar er búið að gefa út eiginleikann [tengd slóð](er-formula-language.md#relative-path).</span><span class="sxs-lookup"><span data-stu-id="414d4-112">To improve usability of ER mapping designers, the [relative path](er-formula-language.md#relative-path) feature has been released.</span></span> <span data-ttu-id="414d4-113">Sjálfgefið er að slökkt sé á framsetningarvalkosti viðkomandi slóðar fyrir öll ný tilvik forritsins þar sem ER-hönnunarreynsla er virkjuð (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service).</span><span class="sxs-lookup"><span data-stu-id="414d4-113">By default, the relative path representation option is turned on for any new instance of the application where ER design experience is enabled (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service).</span></span> <span data-ttu-id="414d4-114">Við innleiddum færibreytu viðkomandi slóðar þannig að notendur geta haldið áfram að nota alla slóðina þegar unnið er með þessa kynningu á ER-bindingum.</span><span class="sxs-lookup"><span data-stu-id="414d4-114">We implemented the relative path parameter so that users can keep using the full path when work with this presentation of ER bindings.</span></span>

<span data-ttu-id="414d4-115">[![Færibreytur notanda](./media/relative-path-01.png)](./media/relative-path-01.png)</span><span class="sxs-lookup"><span data-stu-id="414d4-115">[![User parameters](./media/relative-path-01.png)](./media/relative-path-01.png)</span></span>

 
<span data-ttu-id="414d4-116">Þegar slökkt er á notkunarfæribreytum viðkomandi slóðar kemur einn @ stafur í stað slóðar á yfirvöru í bindingu núverandi líkanareiningar.</span><span class="sxs-lookup"><span data-stu-id="414d4-116">When the relative path usage parameter is turned on, a single @ character replaces the path to the parent item in the binding of the current model element.</span></span> <span data-ttu-id="414d4-117">Öll bindandi slóðin verður styttri, sem gerir alla vörpunina augljósari og auðveldari í skilningi.</span><span class="sxs-lookup"><span data-stu-id="414d4-117">The entire binding path becomes shorter, which makes the entire mapping more obvious and easier to understand.</span></span> <span data-ttu-id="414d4-118">Í flestum tilfellum þarf ekki frekari skrun í ER-hönnuði til að skoða allar bindingar gagnalíkansins.</span><span class="sxs-lookup"><span data-stu-id="414d4-118">In most cases, no additional scrolling is required in the ER designer to view all the bindings of the data model.</span></span>

<span data-ttu-id="414d4-119">[![Hönnun fyrir vörpun gagnalíkans](./media/relative-path-02.png)](./media/relative-path-02.png)</span><span class="sxs-lookup"><span data-stu-id="414d4-119">[![Model mapping designer](./media/relative-path-02.png)](./media/relative-path-02.png)</span></span>
 
<span data-ttu-id="414d4-120">Þegar þú byrjar uppsetningu á nýrri ER-segð þarftu aðeins að slá inn einn staf til að skilgreina bindingu við reit yfirvörunnar.</span><span class="sxs-lookup"><span data-stu-id="414d4-120">When you start designing a new ER expression, you need to enter only one character to define a binding to a field of the parent item.</span></span>

<span data-ttu-id="414d4-121">[![Formúluhönnuður](./media/relative-path-03.png)](./media/relative-path-03.png)</span><span class="sxs-lookup"><span data-stu-id="414d4-121">[![Formula designer](./media/relative-path-03.png)](./media/relative-path-03.png)</span></span>
 
<span data-ttu-id="414d4-122">Þegar þú ákveður að breyta gagnagjafa yfiratriðis með algildri slóðarnotkun þarftu endurbinda þessi líkansatriði, ásamt öllum földuðum atriðum, í nýjan gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="414d4-122">When you decide to change the data source of the parent model item, with absolute path usage, you have to manually rebind this model item, as well as all nested items, to a new data source.</span></span> <span data-ttu-id="414d4-123">Þegar slökkt er á notkun viðkomandi slóðar og þú velur nýjam gagnagjafa til að binda við yfiratriði, er þér boðið upp á valkost til að tengja sjálfkrafa allar faldaðar einingar þessa yfiratriðis með einum smelli.</span><span class="sxs-lookup"><span data-stu-id="414d4-123">When relative path usage is turned on, and you select a new data source to be bound to a parent item, you are offered an option to automatically rebind all nested elements of this parent item with one click.</span></span>

<span data-ttu-id="414d4-124">[![Skilaboðin Skipta um slóð sem er þegar til staðar](./media/relative-path-04.png)](./media/relative-path-04.png)</span><span class="sxs-lookup"><span data-stu-id="414d4-124">[![Replace existing path message](./media/relative-path-04.png)](./media/relative-path-04.png)</span></span>
 
<span data-ttu-id="414d4-125">Ef þú staðfestir endurheimt á földuðum atriðum verður nýtt yfiratriði sett í slóð hvers faldaðs atriðis sem inniheldur fyrirliggjandi yfiratriði.</span><span class="sxs-lookup"><span data-stu-id="414d4-125">If you confirm rebinding of nested items, the new parent item will be placed to the path of each nested item containing the existing parent item.</span></span>
<span data-ttu-id="414d4-126">Þessi eiginleiki brýtur ekki eldra samhæfi ER-rammans.</span><span class="sxs-lookup"><span data-stu-id="414d4-126">This feature does not break the backward compatibility of the ER framework.</span></span> <span data-ttu-id="414d4-127">Allar áður uppsettar ER-skilgreiningar munu virka með þessum nýja eiginleika og engar uppfærslur eða umreikningar verða nauðsynleg.</span><span class="sxs-lookup"><span data-stu-id="414d4-127">All previously designed ER configurations will work with this new feature, and no upgrades or conversions are required.</span></span>

> [!NOTE]
> <span data-ttu-id="414d4-128">Allar breytingar sem eru kynntar með fjöldabreytingum á bindingum faldaðra eininga í líkanavörpunum eru rétt vistaðar í skilgreiningar-delta (rakningu breytinga).</span><span class="sxs-lookup"><span data-stu-id="414d4-128">All changes that are introduced by mass modification of bindings of nested elements in model mappings are correctly saved in a configuration delta (trace of changes).</span></span> <span data-ttu-id="414d4-129">Þetta gerir viðskiptavinum kleift að endurreikna grunn afleiddrar útgáfu líkanavarpana í nýja grunnútgáfu af því sem hefur verið breytt með því að nota þennan nýja eiginleika.</span><span class="sxs-lookup"><span data-stu-id="414d4-129">This allows customers to rebase their derived version of model mappings to any new base version of it that has been modified by using this new feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="414d4-130">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="414d4-130">Additional resources</span></span>

[<span data-ttu-id="414d4-131">Formúlutungumál rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="414d4-131">ER formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]