---
title: Nýtt notendaviðmót skjala í viðskiptaskjalastjórnun
description: Í þessu efnisatriði er að finna upplýsingar um hvernig á að nota nýja notandaviðmót skjalsins í eiginleikastjórnun viðskiptaskjala fyrir rafræn skýrslugerð.
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7f8099f2f6872c34c30de918a6fc5fd27bcde958
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565711"
---
# <a name="new-document-user-interface-in-business-document-management"></a><span data-ttu-id="44838-103">Nýtt notandaviðmót fyrir skjöl í stjórnun viðskiptaskjala</span><span class="sxs-lookup"><span data-stu-id="44838-103">New document user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44838-104">Business Document Management leyfir notendum að breyta sniðmátum viðskiptaskjala með Microsoft 365-þjónustu eða viðeigandi Microsoft Office skjáborðsforriti.</span><span class="sxs-lookup"><span data-stu-id="44838-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="44838-105">Breytingar gætu innihaldið hönnunarbreytingar eða nýjar dreifingar, eða notendur gætu bætt við frátökutákni til að innihalda viðbótargögn án þess að þurfa að breyta kóðanum.</span><span class="sxs-lookup"><span data-stu-id="44838-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="44838-106">Nánari upplýsingar um hvernig á að vinna með skjalastjórnun viðskipta, sjá [Yfirlit yfir stjórnun viðskiptaskjala](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="44838-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="44838-107">Nýja notendaviðmót skjalanna (UI) er skýrara og þægilegra í notkun.</span><span class="sxs-lookup"><span data-stu-id="44838-107">The new document user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="44838-108">Svæðið **Viðskiptaskjal** sýnir aðeins sniðmát sem eru í boði fyrir núverandi þjónustuaðila.</span><span class="sxs-lookup"><span data-stu-id="44838-108">The **Business document** area shows only the templates that are available for the current provider.</span></span>

<span data-ttu-id="44838-109">Hnappurinn **Nýtt skjal** gerir notendum kleift að búa til og breyta sniðmáti í rafrænni skýrslugerð (ER) sniði sem annar veitandi veitir.</span><span class="sxs-lookup"><span data-stu-id="44838-109">The **New document** button lets users create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="44838-110">Í dæminu í þessu efni er veitan Microsoft.</span><span class="sxs-lookup"><span data-stu-id="44838-110">In the example in this topic, the provider is Microsoft.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="44838-111">Gerðu nýja skjalið UI í viðskiptaskjalastjórnun tiltækt</span><span class="sxs-lookup"><span data-stu-id="44838-111">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="44838-112">Til að byrja að nota nýja skjalið UI í viðskiptaskjalastjórnun verður þú að kveikja á eiginleikanum **Office-lík notandaviðmótsreynsla fyrir skjalastjórnun** á vinnusvæðinu **Stjórnun eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="44838-112">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="44838-113">Fylgdu þessum skrefum til að kveikja á þessum eiginleika fyrir alla lögaðila.</span><span class="sxs-lookup"><span data-stu-id="44838-113">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="44838-114">Á vinnusvæðinu **Stjórnun eiginleika**, á flipanum **Nýtt**, velurðu eiginleikann **Office-lík notandaviðmótsreynsla fyrir skjalastjórnun** á listanum.</span><span class="sxs-lookup"><span data-stu-id="44838-114">In the **Feature management** workspace, on the **New** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="44838-115">Veldu **Virkja núna** til að kveikja á völdum eiginleika.</span><span class="sxs-lookup"><span data-stu-id="44838-115">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="44838-116">Endurnýjaðu síðuna til að fá aðgang að nýja eiginleikanum.</span><span class="sxs-lookup"><span data-stu-id="44838-116">Refresh the page to access the new feature.</span></span>

### <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="44838-117">Breyta sniðmátum sem eru í eigu annarra veitenda</span><span class="sxs-lookup"><span data-stu-id="44838-117">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="44838-118">Í vinnusvæðinu **Stjórnun viðskiptaskjala** velurðu **Nýtt skjal**.</span><span class="sxs-lookup"><span data-stu-id="44838-118">In the **Business document management** workspace, select **New document**.</span></span>

    ![Vinnusvæðið Yfirlit yfir stjórnun viðskiptaskjala](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="44838-120">Veldu skjalið til að nota sem sniðmát í valmyndinni og veldu síðan **Stofna skjal**.</span><span class="sxs-lookup"><span data-stu-id="44838-120">In the dialog box, select the document to use as a template, and then select **Create document**.</span></span>

    ![Gluggi viðskiptaskjala](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="44838-122">Í nýja glugganum, í reitnum **Titill**, breytirðu titlinum eins og þú þarfnast.</span><span class="sxs-lookup"><span data-stu-id="44838-122">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="44838-123">Titiltextinn er notaður til að nefna nýju skilgreiningu ER-sniðsins sem er sjálfkrafa búin til.</span><span class="sxs-lookup"><span data-stu-id="44838-123">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="44838-124">Drög að þessari skilgreiningu (**Afrit af skýrslu viðskiptamannareiknings með frjálsum texta (GER)**) sem munu innihalda breytt sniðmát og verða notuð til að keyra þetta ER-snið fyrir núverandi notanda.</span><span class="sxs-lookup"><span data-stu-id="44838-124">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="44838-125">Hið óbreytta upprunalega sniðmát úr grunnstillingu ER-sniðsins notað til að keyra þetta ER-snið fyrir alla aðra notendur.</span><span class="sxs-lookup"><span data-stu-id="44838-125">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="44838-126">Í reitnum **Heiti** breytirðu heiti fyrstu endurskoðunar á breyttu sniðmátinu sem verður sjálfkrafa stofnað.</span><span class="sxs-lookup"><span data-stu-id="44838-126">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="44838-127">Í reitnum **Athugasemd** skaltu uppfæra athugasemdinar fyrir breytanlega endurskoðun sem verður sjálfkrafa stofnuð.</span><span class="sxs-lookup"><span data-stu-id="44838-127">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="44838-128">Veldu **Í lagi** til að staðfesta upphaf breytingarferilsins.</span><span class="sxs-lookup"><span data-stu-id="44838-128">Select **OK** to confirm the start of the editing process.</span></span>

    ![Gluggi skjalagerðar](./media/BDM_overview_new_template3.png)

<span data-ttu-id="44838-130">Hnappurinn **Nýtt skjal** er notaður til að búa til og breyta sniðmáti á ER-sniði sem annar veitandi veitir.</span><span class="sxs-lookup"><span data-stu-id="44838-130">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="44838-131">Í þessu dæmi er veitan Microsoft.</span><span class="sxs-lookup"><span data-stu-id="44838-131">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="44838-132">Þegar þú velur **Nýtt skjal** geturðu skoðað öll sniðmát sem eru í eigu núverandi og annarra veitenda.</span><span class="sxs-lookup"><span data-stu-id="44838-132">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="44838-133">Eftir að þú velur sniðmátið verður það opnað fyrir breytingar.</span><span class="sxs-lookup"><span data-stu-id="44838-133">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="44838-134">Síðan verður breytt sniðmátið geymt í nýrri skilgreiningu á ER-sniði sem er sjálfkrafa mynduð.</span><span class="sxs-lookup"><span data-stu-id="44838-134">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

<span data-ttu-id="44838-135">Fyrir frekari upplýsingar, sjá [Yfirlit yfir stjórnun viðskiptaskjala](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="44838-135">For more information, see [Business document management overview](er-business-document-management.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]