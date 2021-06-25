---
title: Virkja greiðsluspár viðskiptavinar (forskoðun)
description: Þetta efnisatriði útskýrir hvernig á að kveikja á og skilgreina eiginleika greiðsluspár viðskiptavinar í fjármálainnsýn.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ae957f592ad9a1237817fec5d4172295f9a53020
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222587"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="ad976-103">Virkja greiðsluspár viðskiptavinar (forskoðun)</span><span class="sxs-lookup"><span data-stu-id="ad976-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ad976-104">Þetta efnisatriði útskýrir hvernig á að kveikja á og skilgreina eiginleika greiðsluspár viðskiptavinar í fjármálainnsýn.</span><span class="sxs-lookup"><span data-stu-id="ad976-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="ad976-105">Kveikt er á aðgerðinni á vinnusvæðinu **Eiginleikastjórnun** og skilgreiningarstillingar eru slegnar inn á síðunni **Færibreytur fjármálainnsýnar**.</span><span class="sxs-lookup"><span data-stu-id="ad976-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="ad976-106">Þetta efnisatriði inniheldur einnig upplýsingar sem geta aðstoðað þig við að nota eiginleikann á skilvirkan hátt.</span><span class="sxs-lookup"><span data-stu-id="ad976-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="ad976-107">Áður en eftirfarandi skrefum er lokið skal ganga úr skugga um að ljúka undirbúningsskrefunum í efnisatriðinu [Skilgreining fyrir fjármál](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="ad976-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="ad976-108">Notaðu upplýsingar úr umhverfissíðunni í Microsoft Dynamics Lifecycle Services (LCS) til að tengjast aðaltilviki Azure SQL fyrir þetta umhverfi.</span><span class="sxs-lookup"><span data-stu-id="ad976-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="ad976-109">Keyrið eftirfarandi Transact-SQL (T-SQL) skipun til að kveikja á flugi fyrir sandkassaumhverfa.</span><span class="sxs-lookup"><span data-stu-id="ad976-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="ad976-110">(Hugsanlega þarf að kveikja á aðgangi að IP-tölu notanda í LCS áður en hægt er að fjartengjast við AOS \[Application Object Server\].)</span><span class="sxs-lookup"><span data-stu-id="ad976-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('PayPredEnableFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="ad976-111">Sleppið þessu skrefi ef notuð er útgáfa 10.0.20 eða nýrri eða ef notuð er uppsetning Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="ad976-111">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="ad976-112">Fjármögnunarteymið ætti nú þegar að hafa kveikt á forútgáfunni fyrir þig.</span><span class="sxs-lookup"><span data-stu-id="ad976-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="ad976-113">Ef þú sérð ekki eiginleikann á vinnusvæðinu **Eiginleikastjórnun** eða ef vandamál koma upp þegar reynt er að kveikja á honum skal hafa samband við <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="ad976-113">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span> 

2. <span data-ttu-id="ad976-114">Kveikja á innsýnareiginleika greiðslu viðskiptavinar:</span><span class="sxs-lookup"><span data-stu-id="ad976-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="ad976-115">Opna skal **Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="ad976-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="ad976-116">Leitaðu að eiginleikanum sem heitir **Innsýn í greiðslu viðskiptavinar (forskoðun)**.</span><span class="sxs-lookup"><span data-stu-id="ad976-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="ad976-117">Veldu **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="ad976-117">Select **Enable now**.</span></span>

    <span data-ttu-id="ad976-118">Kveikt er á eiginleikanum innsýn í greiðslu viðskiptavinar og hann er tilbúin til skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="ad976-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="ad976-119">Skilgreina innsýnareiginleika greiðslu viðskiptavinar:</span><span class="sxs-lookup"><span data-stu-id="ad976-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="ad976-120">Opnaðu **Skuldir og innheimta \> Uppsetning \> Fjármálainnsýn \> Færibreytur fjármálainnsýnar**.</span><span class="sxs-lookup"><span data-stu-id="ad976-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="ad976-121">[![Síða færibreyta fjármálainnsýnar áður en eiginleikinn er skilgreindur](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="ad976-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="ad976-122">Á síðunni **Færibreytur fjármálainnsýnar** á flipanum **Innsýn í greiðslu viðskiptavinar** skal velja tengilinn **Skoða gagnareitina sem eru notaðir í spálíkaninu** til að opna síðuna **Gagnareitir fyrir spálíkan**.</span><span class="sxs-lookup"><span data-stu-id="ad976-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="ad976-123">Þar er hægt að skoða sjálfgefinn lista yfir svæði sem eru notuð til að stofna spálíkan gervigreindar (AI) fyrir greiðsluspár viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="ad976-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="ad976-124">Til að nota sjálfgefna lista yfir reiti til að búa til spálíkanið skal loka síðunni **Gagnareitir fyrir spálíkan** og síðan á síðunni **Færibreytur fjármálainnsýnar** stilla valkostinn **Virkja eiginleika** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="ad976-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="ad976-125">Tilgreinið færslutímabil „mjög seint“ til að skilgreina hvað spáramminn **Mjög seint** þýðir fyrir fyrirtækið þitt.</span><span class="sxs-lookup"><span data-stu-id="ad976-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="ad976-126">Fyrir hvern opinn reikning spáir kerfið því að líkur á greiðslu í þremur römmum: **Á réttum tíma**, **Seint** og **Mjög seint**.</span><span class="sxs-lookup"><span data-stu-id="ad976-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="ad976-127">**Á tíma** - Þessi rammi inniheldur reiðslur sem áætlað er að verði greiddar á eða fyrir gjalddaga færslunnar.</span><span class="sxs-lookup"><span data-stu-id="ad976-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="ad976-128">**Seint** - Þessi rammi inniheldur greiðslur sem áætlað er að verði greiddar eftir gjalddaga færslunnar en fyrir tímabilið sem telst mjög á eftir áætlun.</span><span class="sxs-lookup"><span data-stu-id="ad976-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="ad976-129">**Mjög seint** – Þessi rammi innheldur greiðslur sem spáð er að verði borgaðar eftir upphafsdag færslutímabilsins „mjög seint“.</span><span class="sxs-lookup"><span data-stu-id="ad976-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="ad976-130">Þegar færslutímabilinu „mjög seint“ er breytt og **Breyta viðmiðunarmörkum fyrir seint** er valið eftir að spálíkan gervigreindar fyrir greiðslur viðkiptavinar hefur verið stofnað, er fyrirliggjandi spálíkani eytt og nýtt líkan stofnað.</span><span class="sxs-lookup"><span data-stu-id="ad976-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="ad976-131">Nýja spálíkanið flytur færslur yfir í tímabilið „mjög seint“ miðað við stillingarnar sem voru slegnar inn til að skilgreina það.</span><span class="sxs-lookup"><span data-stu-id="ad976-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="ad976-132">Þegar búið er að skilgreina færslutímabilið „mjög seint“ skal velja **Stofna spálíkan** til að stofna spálíkanið.</span><span class="sxs-lookup"><span data-stu-id="ad976-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="ad976-133">Hlutinn **Spálíkan** á síðunni **Færibreytur fjármálainnsýnar** sýnir stöðu spálíkansins.</span><span class="sxs-lookup"><span data-stu-id="ad976-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="ad976-134">Á meðan spálíkanið er stofnað er hægt að velja **Endurstilla stofnun spálíkans** hvenær sem er til að endurræsa ferlið.</span><span class="sxs-lookup"><span data-stu-id="ad976-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="ad976-135">Eiginleikinn hefur nú verið skilgreindur og er tilbúinn til notkunar.</span><span class="sxs-lookup"><span data-stu-id="ad976-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="ad976-136">Þegar lokið er við að kveikja á og skilgreina eiginleikann og spálíkanið hefur verið stofnað og er í gangi sýnir hlutinn **Gerð spálíkans** á síðunni **Færibreytur fjármálainnsýnar** nákvæmni líkansins, eins og sýnt er á eftirfarandi skýringarmynd.</span><span class="sxs-lookup"><span data-stu-id="ad976-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="ad976-137">[![Nákvæmni spálíkans á síðunni Færibreytur fjármálainnsýnar](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="ad976-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="ad976-138">Upplýsingar um losun</span><span class="sxs-lookup"><span data-stu-id="ad976-138">Release details</span></span>

<span data-ttu-id="ad976-139">Almenn forskoðun Fjármálainnsýnar er í boði til prufuuppsetningar í Bandaríkjunum, Evrópu og Bretlandi.</span><span class="sxs-lookup"><span data-stu-id="ad976-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="ad976-140">Microsoft bætir smátt og smátt við stuðningi fyrir fleiri svæði.</span><span class="sxs-lookup"><span data-stu-id="ad976-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="ad976-141">Aðeins er hægt og aðeins skal kveikja á eiginleikum almennrar forskoðunar í tveggja laga sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="ad976-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="ad976-142">Uppsetningar- og gervigreindarlíkön sem eru stofnuð í sandkassaumhverfi eru ekki hægt að flytja yfir í vinnsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="ad976-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="ad976-143">Frekari upplýsingar er að finna í [Viðbótarnotkunarskilmálum fyrir Microsoft Dynamics 365 forskoðanir](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span><span class="sxs-lookup"><span data-stu-id="ad976-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
