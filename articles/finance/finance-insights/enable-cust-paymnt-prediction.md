---
title: Virkja greiðsluspár viðskiptavinar (forskoðun)
description: Þetta efnisatriði útskýrir hvernig á að kveikja á og skilgreina eiginleika greiðsluspár viðskiptavinar í fjármálainnsýn.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: e10aa9342ec9f089ef8ecec5e1221a31c580fc87
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644994"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="c3525-103">Virkja greiðsluspár viðskiptavinar (forskoðun)</span><span class="sxs-lookup"><span data-stu-id="c3525-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="c3525-104">Þetta efnisatriði útskýrir hvernig á að kveikja á og skilgreina eiginleika greiðsluspár viðskiptavinar í fjármálainnsýn.</span><span class="sxs-lookup"><span data-stu-id="c3525-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="c3525-105">Kveikt er á aðgerðinni á vinnusvæðinu **Eiginleikastjórnun** og skilgreiningarstillingar eru slegnar inn á síðunni **Færibreytur fjármálainnsýnar**.</span><span class="sxs-lookup"><span data-stu-id="c3525-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="c3525-106">Þetta efnisatriði inniheldur einnig upplýsingar sem geta aðstoðað þig við að nota eiginleikann á skilvirkan hátt.</span><span class="sxs-lookup"><span data-stu-id="c3525-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="c3525-107">Áður en eftirfarandi skrefum er lokið skal ganga úr skugga um að ljúka undirbúningsskrefunum í efnisatriðinu [Skilgreining fyrir fjármál](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="c3525-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="c3525-108">Notaðu upplýsingar úr umhverfissíðunni í Microsoft Dynamics Lifecycle Services (LCS) til að tengjast aðaltilviki Azure SQL fyrir þetta umhverfi.</span><span class="sxs-lookup"><span data-stu-id="c3525-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="c3525-109">Keyrið eftirfarandi Transact-SQL (T-SQL) skipun til að kveikja á flugi fyrir sandkassaumhverfa.</span><span class="sxs-lookup"><span data-stu-id="c3525-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="c3525-110">(Hugsanlega þarf að kveikja á aðgangi að IP-tölu notanda í LCS áður en hægt er að fjartengjast við AOS \[Application Object Server\].)</span><span class="sxs-lookup"><span data-stu-id="c3525-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > <span data-ttu-id="c3525-111">Ef verið er að setja upp Microsoft Dynamics 365 Finance sem Service Fabric-uppsetningu er hægt að sleppa þessu skrefi.</span><span class="sxs-lookup"><span data-stu-id="c3525-111">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="c3525-112">Fjármögnunarteymið ætti nú þegar að hafa kveikt á forútgáfunni fyrir þig.</span><span class="sxs-lookup"><span data-stu-id="c3525-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="c3525-113">Ef þú sérð ekki eiginleikann á vinnusvæðinu **Eiginleikastjórnun** eða ef vandamál koma upp þegar reynt er að kveikja á honum skal hafa samband við <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="c3525-113">If you don't see the feature in the **Feature management** workspace, or if experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="c3525-114">Kveikja á innsýnareiginleika greiðslu viðskiptavinar:</span><span class="sxs-lookup"><span data-stu-id="c3525-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="c3525-115">Opna skal **Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="c3525-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="c3525-116">Leitaðu að eiginleikanum sem heitir **Innsýn í greiðslu viðskiptavinar (forskoðun)**.</span><span class="sxs-lookup"><span data-stu-id="c3525-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="c3525-117">Veldu **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="c3525-117">Select **Enable now**.</span></span>

    <span data-ttu-id="c3525-118">Kveikt er á eiginleikanum innsýn í greiðslu viðskiptavinar og hann er tilbúin til skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="c3525-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="c3525-119">Skilgreina innsýnareiginleika greiðslu viðskiptavinar:</span><span class="sxs-lookup"><span data-stu-id="c3525-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="c3525-120">Opnaðu **Skuldir og innheimta \> Uppsetning \> Fjármálainnsýn \> Færibreytur fjármálainnsýnar**.</span><span class="sxs-lookup"><span data-stu-id="c3525-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="c3525-121">[![Síða færibreyta fjármálainnsýnar áður en eiginleikinn er skilgreindur](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="c3525-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="c3525-122">Á síðunni **Færibreytur fjármálainnsýnar** á flipanum **Innsýn í greiðslu viðskiptavinar** skal velja tengilinn **Skoða gagnareitina sem eru notaðir í spálíkaninu** til að opna síðuna **Gagnareitir fyrir spálíkan**.</span><span class="sxs-lookup"><span data-stu-id="c3525-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="c3525-123">Þar er hægt að skoða sjálfgefinn lista yfir svæði sem eru notuð til að stofna spálíkan gervigreindar (AI) fyrir greiðsluspár viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="c3525-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="c3525-124">Til að nota sjálfgefna lista yfir reiti til að búa til spálíkanið skal loka síðunni **Gagnareitir fyrir spálíkan** og síðan á síðunni **Færibreytur fjármálainnsýnar** stilla valkostinn **Virkja eiginleika** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="c3525-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="c3525-125">Tilgreinið færslutímabil „mjög seint“ til að skilgreina hvað spáramminn **Mjög seint** þýðir fyrir fyrirtækið þitt.</span><span class="sxs-lookup"><span data-stu-id="c3525-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="c3525-126">Fyrir hvern opinn reikning spáir kerfið því að líkur á greiðslu í þremur römmum: **Á réttum tíma**, **Seint** og **Mjög seint**.</span><span class="sxs-lookup"><span data-stu-id="c3525-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="c3525-127">**Á tíma** - Þessi rammi inniheldur reiðslur sem áætlað er að verði greiddar á eða fyrir gjalddaga færslunnar.</span><span class="sxs-lookup"><span data-stu-id="c3525-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="c3525-128">**Seint** - Þessi rammi inniheldur greiðslur sem áætlað er að verði greiddar eftir gjalddaga færslunnar en fyrir tímabilið sem telst mjög á eftir áætlun.</span><span class="sxs-lookup"><span data-stu-id="c3525-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="c3525-129">**Mjög seint** – Þessi rammi innheldur greiðslur sem spáð er að verði borgaðar eftir upphafsdag færslutímabilsins „mjög seint“.</span><span class="sxs-lookup"><span data-stu-id="c3525-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="c3525-130">Þegar færslutímabilinu „mjög seint“ er breytt og **Breyta viðmiðunarmörkum fyrir seint** er valið eftir að spálíkan gervigreindar fyrir greiðslur viðkiptavinar hefur verið stofnað, er fyrirliggjandi spálíkani eytt og nýtt líkan stofnað.</span><span class="sxs-lookup"><span data-stu-id="c3525-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="c3525-131">Nýja spálíkanið flytur færslur yfir í tímabilið „mjög seint“ miðað við stillingarnar sem voru slegnar inn til að skilgreina það.</span><span class="sxs-lookup"><span data-stu-id="c3525-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="c3525-132">Þegar búið er að skilgreina færslutímabilið „mjög seint“ skal velja **Stofna spálíkan** til að stofna spálíkanið.</span><span class="sxs-lookup"><span data-stu-id="c3525-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="c3525-133">Hlutinn **Spálíkan** á síðunni **Færibreytur fjármálainnsýnar** sýnir stöðu spálíkansins.</span><span class="sxs-lookup"><span data-stu-id="c3525-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="c3525-134">Á meðan spálíkanið er stofnað er hægt að velja **Endurstilla stofnun spálíkans** hvenær sem er til að endurræsa ferlið.</span><span class="sxs-lookup"><span data-stu-id="c3525-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="c3525-135">Eiginleikinn hefur nú verið skilgreindur og er tilbúinn til notkunar.</span><span class="sxs-lookup"><span data-stu-id="c3525-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="c3525-136">Þegar lokið er við að kveikja á og skilgreina eiginleikann og spálíkanið hefur verið stofnað og er í gangi sýnir hlutinn **Gerð spálíkans** á síðunni **Færibreytur fjármálainnsýnar** nákvæmni líkansins, eins og sýnt er á eftirfarandi skýringarmynd.</span><span class="sxs-lookup"><span data-stu-id="c3525-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="c3525-137">[![Nákvæmni spálíkans á síðunni Færibreytur fjármálainnsýnar](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="c3525-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="c3525-138">Upplýsingar um losun</span><span class="sxs-lookup"><span data-stu-id="c3525-138">Release details</span></span>

<span data-ttu-id="c3525-139">Almenn forskoðun Fjármálainnsýnar er í boði til prufuuppsetningar í Bandaríkjunum, Evrópu og Bretlandi.</span><span class="sxs-lookup"><span data-stu-id="c3525-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="c3525-140">Microsoft bætir smátt og smátt við stuðningi fyrir fleiri svæði.</span><span class="sxs-lookup"><span data-stu-id="c3525-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="c3525-141">Aðeins er hægt og aðeins skal kveikja á eiginleikum almennrar forskoðunar í tveggja laga sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="c3525-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="c3525-142">Uppsetningar- og gervigreindarlíkön sem eru stofnuð í sandkassaumhverfi eru ekki hægt að flytja yfir í vinnsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="c3525-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="c3525-143">Frekari upplýsingar er að finna í [Viðbótarnotkunarskilmálum fyrir Microsoft Dynamics 365 forskoðanir](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span><span class="sxs-lookup"><span data-stu-id="c3525-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="c3525-144">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="c3525-144">Privacy notice</span></span>

<span data-ttu-id="c3525-145">Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.</span><span class="sxs-lookup"><span data-stu-id="c3525-145">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>