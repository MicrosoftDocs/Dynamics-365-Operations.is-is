---
title: "POS forritið og stillingar notandatungumáls"
description: "Þetta efnisatriði lýsir hvernig á að breyta tungumálastillingum í Cloud POS og Retail Modern POS (MPOS)."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cabb63aea0da4b264aec8e0cc4d43b3e1014e71b
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="pos-application-and-user-language-settings"></a><span data-ttu-id="f5568-103">POS forritið og stillingar notandatungumáls</span><span class="sxs-lookup"><span data-stu-id="f5568-103">POS application and user language settings</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="f5568-104">Þetta efnisatriði lýsir hvernig á að breyta tungumálastillingum í Cloud POS og Retail Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="f5568-104">This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.</span></span>

<a name="overview"></a><span data-ttu-id="f5568-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="f5568-105">Overview</span></span>
========

<span data-ttu-id="f5568-106">Retail Modern POS (MPOS) og Cloud POS styður umhverfi þar sem stillingar tungumáls og þýðinga kunna að vera mismunandi milli stillinga verslunar og notanda.</span><span class="sxs-lookup"><span data-stu-id="f5568-106">Retail Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="f5568-107">Til dæmis gæti verslunin verið staðsett á svæði þar sem enska er algengust meðal viðskiptavina þeirra, en sumir starfsmenn kjósa heldur að nota forritið með frönskum þýðingum.</span><span class="sxs-lookup"><span data-stu-id="f5568-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="f5568-108">Gagnamál</span><span class="sxs-lookup"><span data-stu-id="f5568-108">Data language</span></span>
<span data-ttu-id="f5568-109">Óháð stillingum notanda munu MPOS- og Cloud POS alltaf nota tungumálastillingar verslunar til að ákvarða þýðingar sem eru notaðar fyrir gögn.</span><span class="sxs-lookup"><span data-stu-id="f5568-109">Regardless of the user’s settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="f5568-110">Þetta mun tryggja að notendur og viðskiptavinir hafi samræmda reynslu.</span><span class="sxs-lookup"><span data-stu-id="f5568-110">This will ensure that all users and customers will have a consistent experience.</span></span>  <span data-ttu-id="f5568-111">Dæmi um gögn eru:</span><span class="sxs-lookup"><span data-stu-id="f5568-111">Examples of data include:</span></span>

-   <span data-ttu-id="f5568-112">Vörur</span><span class="sxs-lookup"><span data-stu-id="f5568-112">Products</span></span>
-   <span data-ttu-id="f5568-113">Eigindi og gildi</span><span class="sxs-lookup"><span data-stu-id="f5568-113">Attributes and values</span></span>
-   <span data-ttu-id="f5568-114">Flokkaheiti</span><span class="sxs-lookup"><span data-stu-id="f5568-114">Category names</span></span>
-   <span data-ttu-id="f5568-115">Prentaðar eða senda færslukvittanir í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="f5568-115">Printed or emailed transaction receipts</span></span>
-   <span data-ttu-id="f5568-116">Heiti greiðsluhátta</span><span class="sxs-lookup"><span data-stu-id="f5568-116">Payment method names</span></span>
-   <span data-ttu-id="f5568-117">Línubirting skilaboða</span><span class="sxs-lookup"><span data-stu-id="f5568-117">Line display messages</span></span>

<span data-ttu-id="f5568-118">Tungumál verslunarinnar verður einnig notað fyrir aðalinnskráningarskjá POS, þar sem notandinn er ekki þekktur áður en hann skráir sig inn.</span><span class="sxs-lookup"><span data-stu-id="f5568-118">The store’s language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="f5568-119">Ef þýðing er ekki tiltæk fyrir tungumálið verslunarinnar mun POS snúa aftur í tungumál fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="f5568-119">If a translation is not available for the store’s language, the POS will revert to the company’s language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="f5568-120">Skilgreining tungumálastillingar verslunarinnar</span><span class="sxs-lookup"><span data-stu-id="f5568-120">Configuring the store’s language setting</span></span>

<span data-ttu-id="f5568-121">Tungumálastillingar verslunarinnar eru stilltar í **Allar smásöluverslanir** á síðunni **Smásöluverslun** undir **Almennt&gt; Svæðisstillingar &gt; Tungumál.</span><span class="sxs-lookup"><span data-stu-id="f5568-121">The store’s language setting is set from **All retail stores** on the **Retail Store** page under **General &gt; Regional Settings &gt; Language.</span></span> <span data-ttu-id="f5568-122">** Nota skal fellilista til að velja tungumál fyrir hverja verslun.</span><span class="sxs-lookup"><span data-stu-id="f5568-122">**Use the drop down to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="f5568-123">Tungumál notandaviðmóts</span><span class="sxs-lookup"><span data-stu-id="f5568-123">User interface language</span></span>
<span data-ttu-id="f5568-124">Tungumálastilling POS notanda ákvarðar þýðingarnar sem eru notaðar í notandaviðmóti forritsins.</span><span class="sxs-lookup"><span data-stu-id="f5568-124">The POS user’s language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="f5568-125">Það tekur til allra merkja, valmynda og lista sem teljast ekki vera gögn.</span><span class="sxs-lookup"><span data-stu-id="f5568-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="f5568-126">Ein undantekning er textinn sem birtist á hnappahnitum POS.</span><span class="sxs-lookup"><span data-stu-id="f5568-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="f5568-127">Hnappahnit styðja ekki þýðingar, svo þau munu ætíð sýna textann eins og hann er skilgreindur á hnappnum.</span><span class="sxs-lookup"><span data-stu-id="f5568-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="f5568-128">Til að styðja þýdda hnappa, verður að að afrita og vinna með aðskilin hnappahnit og úthluta þeim á notendur eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="f5568-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="f5568-129">Skilgreining tungumálastillingar notanda</span><span class="sxs-lookup"><span data-stu-id="f5568-129">Configuring the user’s language setting</span></span>

<span data-ttu-id="f5568-130">Tungumálastilling POS notanda er stillt í **Allir starfsmenn** á síðunni **Starfsmaður** undir **Smásala &gt; Tungumál**.</span><span class="sxs-lookup"><span data-stu-id="f5568-130">The POS user’s language setting is set from **All workers** on the **Worker** page under **Retail &gt; Language**.</span></span>  <span data-ttu-id="f5568-131">Hún er ekki stillt á fliptanum Aðalforstillingu.  Þessi stilling er ekki notuð af POS.</span><span class="sxs-lookup"><span data-stu-id="f5568-131">It is not set on the main Profile tab.  This setting is not used by POS.</span></span> <span data-ttu-id="f5568-132">Ef tungumál notanda er ekki stillt eða það er stillt á tungumál þar sem þýðingar eru ekki tiltækar, mun Sölustaðnum snúa til baka í tungumál verslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="f5568-132">If the user’s language is not set or it is set to a language where translations are not available, the POS will revert to the store’s language.</span></span>  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f5568-133">** **</span><span class="sxs-lookup"><span data-stu-id="f5568-133">** **</span></span>       | <span data-ttu-id="f5568-134">**UI-tungumál** ** **</span><span class="sxs-lookup"><span data-stu-id="f5568-134">**UI language** ** **</span></span>      | <span data-ttu-id="f5568-135">**Gagnamál (afurðir, snið kvittunar, línuskjá o.s.frv.)**</span><span class="sxs-lookup"><span data-stu-id="f5568-135">**Data language (products, receipt formats, line display, etc.)**</span></span> |
| <span data-ttu-id="f5568-136">**Fyrirtæki**</span><span class="sxs-lookup"><span data-stu-id="f5568-136">**Company**</span></span> | <span data-ttu-id="f5568-137">Sjálfgefinn</span><span class="sxs-lookup"><span data-stu-id="f5568-137">Default</span></span>                    | <span data-ttu-id="f5568-138">Sjálfgefinn</span><span class="sxs-lookup"><span data-stu-id="f5568-138">Default</span></span>                                                           |
| <span data-ttu-id="f5568-139">**Verslun**</span><span class="sxs-lookup"><span data-stu-id="f5568-139">**Store**</span></span>   | <span data-ttu-id="f5568-140">Hnekkir fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="f5568-140">Overrides company</span></span>          | <span data-ttu-id="f5568-141">Hnekkir fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="f5568-141">Overrides company</span></span>                                                 |
| <span data-ttu-id="f5568-142">**Notandi**</span><span class="sxs-lookup"><span data-stu-id="f5568-142">**User**</span></span>    | <span data-ttu-id="f5568-143">Hnekkir verslun eða fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="f5568-143">Overrides store or company</span></span> | <span data-ttu-id="f5568-144">Aldrei</span><span class="sxs-lookup"><span data-stu-id="f5568-144">Never</span></span>                                                             |






