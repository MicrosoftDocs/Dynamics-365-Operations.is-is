---
title: Sölustaðarforrit (POS) og stillingar notandatungumáls
description: Þetta efnisatriði lýsir hvernig á að breyta tungumálastillingum í Cloud POS og Modern POS (MPOS).
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0c5087ee04030a76aef774871b88b7970391723c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804382"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a><span data-ttu-id="87d74-103">Sölustaðarforrit (POS) og stillingar notandatungumáls</span><span class="sxs-lookup"><span data-stu-id="87d74-103">Point of sale (POS) application and user language settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="87d74-104">Þetta efnisatriði lýsir hvernig á að breyta tungumálastillingum í Cloud POS og Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="87d74-104">This topic describes how to change language settings in Modern POS (MPOS) and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="87d74-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="87d74-105">Overview</span></span>
<span data-ttu-id="87d74-106">Modern POS (MPOS) og Cloud POS styður umhverfi þar sem stillingar tungumáls og þýðinga kunna að vera mismunandi milli stillinga verslunar og notanda.</span><span class="sxs-lookup"><span data-stu-id="87d74-106">Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="87d74-107">Til dæmis gæti verslunin verið staðsett á svæði þar sem enska er algengust meðal viðskiptavina þeirra, en sumir starfsmenn kjósa heldur að nota forritið með frönskum þýðingum.</span><span class="sxs-lookup"><span data-stu-id="87d74-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="87d74-108">Gagnamál</span><span class="sxs-lookup"><span data-stu-id="87d74-108">Data language</span></span>

<span data-ttu-id="87d74-109">Óháð stillingum notanda munu MPOS og Cloud POS alltaf nota tungumálastillingar verslunar til að ákvarða þýðingar sem eru notaðar fyrir gögn.</span><span class="sxs-lookup"><span data-stu-id="87d74-109">Regardless of the user's settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="87d74-110">Þetta mun tryggja að notendur og viðskiptavinir hafi samræmda reynslu.</span><span class="sxs-lookup"><span data-stu-id="87d74-110">This will ensure that all users and customers will have a consistent experience.</span></span> <span data-ttu-id="87d74-111">Dæmi um gögn eru:</span><span class="sxs-lookup"><span data-stu-id="87d74-111">Examples of data include:</span></span>

- <span data-ttu-id="87d74-112">Vörur</span><span class="sxs-lookup"><span data-stu-id="87d74-112">Products</span></span>
- <span data-ttu-id="87d74-113">Eigindi og gildi</span><span class="sxs-lookup"><span data-stu-id="87d74-113">Attributes and values</span></span>
- <span data-ttu-id="87d74-114">Flokkaheiti</span><span class="sxs-lookup"><span data-stu-id="87d74-114">Category names</span></span>
- <span data-ttu-id="87d74-115">Prentaðar eða senda færslukvittanir í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="87d74-115">Printed or emailed transaction receipts</span></span>
- <span data-ttu-id="87d74-116">Heiti greiðsluhátta</span><span class="sxs-lookup"><span data-stu-id="87d74-116">Payment method names</span></span>
- <span data-ttu-id="87d74-117">Línubirting skilaboða</span><span class="sxs-lookup"><span data-stu-id="87d74-117">Line display messages</span></span>

<span data-ttu-id="87d74-118">Tungumál verslunarinnar verður einnig notað fyrir aðalinnskráningarskjá POS, þar sem notandinn er ekki þekktur áður en hann skráir sig inn.</span><span class="sxs-lookup"><span data-stu-id="87d74-118">The store's language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="87d74-119">Ef þýðing er ekki tiltæk fyrir tungumál verslunarinnar mun POS snúa aftur í tungumál fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="87d74-119">If a translation is not available for the store's language, the POS will revert to the company's language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="87d74-120">Skilgreining tungumálastillingar verslunarinnar</span><span class="sxs-lookup"><span data-stu-id="87d74-120">Configuring the store's language setting</span></span>

<span data-ttu-id="87d74-121">Tungumálastillingar verslunarinnar eru stilltar í **Allar verslanir** á síðunni **Verslun** undir **Almennt &gt; Svæðisstillingar &gt; Tungumál**.</span><span class="sxs-lookup"><span data-stu-id="87d74-121">The store's language setting is set from **All stores** on the **Store** page under **General &gt; Regional Settings &gt; Language**.</span></span> <span data-ttu-id="87d74-122">Nota skal fellilista til að velja tungumál fyrir hverja verslun.</span><span class="sxs-lookup"><span data-stu-id="87d74-122">Use the drop-down list to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="87d74-123">Tungumál notandaviðmóts</span><span class="sxs-lookup"><span data-stu-id="87d74-123">User interface language</span></span>

<span data-ttu-id="87d74-124">Tungumálastilling POS notanda ákvarðar þýðingarnar sem eru notaðar í notandaviðmóti forritsins.</span><span class="sxs-lookup"><span data-stu-id="87d74-124">The POS user's language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="87d74-125">Það tekur til allra merkja, valmynda og lista sem teljast ekki vera gögn.</span><span class="sxs-lookup"><span data-stu-id="87d74-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="87d74-126">Ein undantekning er textinn sem birtist á hnappahnitum POS.</span><span class="sxs-lookup"><span data-stu-id="87d74-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="87d74-127">Hnappahnit styðja ekki þýðingar, svo þau munu ætíð sýna textann eins og hann er skilgreindur á hnappnum.</span><span class="sxs-lookup"><span data-stu-id="87d74-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="87d74-128">Til að styðja þýdda hnappa, verður að að afrita og vinna með aðskilin hnappahnit og úthluta þeim á notendur eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="87d74-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="87d74-129">Skilgreining tungumálastillingar notanda</span><span class="sxs-lookup"><span data-stu-id="87d74-129">Configuring the user's language setting</span></span>

<span data-ttu-id="87d74-130">Tungumálastilling POS notanda er stillt í **Allir starfsmenn** á síðunni **Starfsmaður** undir **Retail og Commerce &gt; Tungumál**.</span><span class="sxs-lookup"><span data-stu-id="87d74-130">The POS user's language setting is set from **All workers** on the **Worker** page under **Retail and Commerce &gt; Language**.</span></span> <span data-ttu-id="87d74-131">Hún er ekki stillt á flipa Aðalforstillingar. Þessi stilling er ekki notuð af POS.</span><span class="sxs-lookup"><span data-stu-id="87d74-131">It is not set on the main Profile tab. This setting is not used by POS.</span></span> <span data-ttu-id="87d74-132">Ef tungumál notanda er ekki stillt eða það er stillt á tungumál þar sem þýðingar eru ekki tiltækar, mun sölustaðurinn fara aftur í tungumál verslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="87d74-132">If the user's language is not set or it is set to a language where translations are not available, the POS will revert to the store's language.</span></span>

|             | <span data-ttu-id="87d74-133">UI-tungumál</span><span class="sxs-lookup"><span data-stu-id="87d74-133">UI language</span></span>                | <span data-ttu-id="87d74-134">Gagnamál (afurðir, snið kvittunar, línuskjá o.s.frv.)</span><span class="sxs-lookup"><span data-stu-id="87d74-134">Data language (products, receipt formats, line display, etc.)</span></span> |
|-------------|----------------------------|---------------------------------------------------------------|
| <span data-ttu-id="87d74-135">**Fyrirtæki**</span><span class="sxs-lookup"><span data-stu-id="87d74-135">**Company**</span></span> | <span data-ttu-id="87d74-136">Sjálfgefinn</span><span class="sxs-lookup"><span data-stu-id="87d74-136">Default</span></span>                    | <span data-ttu-id="87d74-137">Sjálfgefinn</span><span class="sxs-lookup"><span data-stu-id="87d74-137">Default</span></span>                                                       |
| <span data-ttu-id="87d74-138">**Verslun**</span><span class="sxs-lookup"><span data-stu-id="87d74-138">**Store**</span></span>   | <span data-ttu-id="87d74-139">Hnekkir fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="87d74-139">Overrides company</span></span>          | <span data-ttu-id="87d74-140">Hnekkir fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="87d74-140">Overrides company</span></span>                                             |
| <span data-ttu-id="87d74-141">**Notandi**</span><span class="sxs-lookup"><span data-stu-id="87d74-141">**User**</span></span>    | <span data-ttu-id="87d74-142">Hnekkir verslun eða fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="87d74-142">Overrides store or company</span></span> | <span data-ttu-id="87d74-143">Aldrei</span><span class="sxs-lookup"><span data-stu-id="87d74-143">Never</span></span>                                                         |


[!INCLUDE[footer-include](../includes/footer-banner.md)]