---
title: Skilgreina Dataverse-samþættingu
description: Þú getur kveikt eða slökkt á samþættingu á milli Microsoft Dataverse og Dynamics 365 Human Resources. Einnig er hægt að skoða samstillingarupplýsingar, hreinsa rakningargögn og endursamstilla töflu til að úrræðaleita vandamál með gögn milli umhverfanna tveggja.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 38c42469e62bf5457d0281540325a6c56a5f930f
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113010"
---
# <a name="configure-dataverse-integration"></a><span data-ttu-id="f96f5-104">Skilgreina Dataverse-samþættingu</span><span class="sxs-lookup"><span data-stu-id="f96f5-104">Configure Dataverse integration</span></span>

<span data-ttu-id="f96f5-105">Þú getur kveikt eða slökkt á samþættingu á milli Microsoft Dataverse og Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f96f5-105">You can turn integration between Microsoft Dataverse and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="f96f5-106">Einnig er hægt að skoða samstillingarupplýsingar, hreinsa rakningargögn og endursamstilla töflu til að úrræðaleita vandamál með gögn milli umhverfanna tveggja.</span><span class="sxs-lookup"><span data-stu-id="f96f5-106">You can also view the synchronization details, clear tracking data, and resync a table to help troubleshoot data issues between the two environments.</span></span>

> [!NOTE]
> <span data-ttu-id="f96f5-107">Frekari upplýsingar um Dataverse (áður Common Data Service) og uppfærslur á hugtökum er að finna í [Hvað er Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="f96f5-107">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="f96f5-108">Þegar þú slekkur á samþættingu geta notendur gert breytingar á starfsmannahaldi eða Dataverse, en þessar breytingar eru ekki samstilltar milli umhverfisins tveggja.</span><span class="sxs-lookup"><span data-stu-id="f96f5-108">When you turn off integration, users can make changes in Human Resources or Dataverse, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="f96f5-109">Sjálfgefið er að slökktu sé á samþættingu gagna milli Human Resources og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f96f5-109">By default, integration between Human Resources and Dataverse is turned off.</span></span>

<span data-ttu-id="f96f5-110">Þú gætir viljað slökkva á samþættingu við þessar aðstæður:</span><span class="sxs-lookup"><span data-stu-id="f96f5-110">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="f96f5-111">Þú ert að fylla út gögn í gegnum Data Management Framework og verður að flytja gögnin inn nokkrum sinnum til að koma þeim í rétt ástand.</span><span class="sxs-lookup"><span data-stu-id="f96f5-111">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="f96f5-112">Það eru vandamál með gögn í annaðhvort Human Resources eða Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f96f5-112">There are issues with data in either Human Resources or Dataverse.</span></span> <span data-ttu-id="f96f5-113">Ef slökkt er á samþættingu geturðu eytt skrá í einu umhverfi án þess að eyða því í hinu.</span><span class="sxs-lookup"><span data-stu-id="f96f5-113">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="f96f5-114">Þegar þú kveikir aftur á samþættingu samstillist skráin í umhverfinu þar sem henni var ekki eytt við umhverfið þar sem henni var eytt.</span><span class="sxs-lookup"><span data-stu-id="f96f5-114">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="f96f5-115">Samstilling hefst næst þegar runuvinnslan **Dataverse samstilling missti af beiðni samstillingar** keyrir.</span><span class="sxs-lookup"><span data-stu-id="f96f5-115">Synchronization begins the next time the **Dataverse integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="f96f5-116">Þegar þú slekkur á samþættingu gagna, vertu viss um að þú breytir ekki sömu skránni í báðum umhverfunum.</span><span class="sxs-lookup"><span data-stu-id="f96f5-116">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="f96f5-117">Þegar þú kveikir aftur á samþættingu verður skráin sem þú breyttir síðast samstillt.</span><span class="sxs-lookup"><span data-stu-id="f96f5-117">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="f96f5-118">Þess vegna, ef þú gerðir ekki sömu breytingar á skránni í báðum umhverfunum, getur gagnatap orðið.</span><span class="sxs-lookup"><span data-stu-id="f96f5-118">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-dataverse-integration-page"></a><span data-ttu-id="f96f5-119">Aðgangur að Dataverse sameiningarsíðu</span><span class="sxs-lookup"><span data-stu-id="f96f5-119">Access the Dataverse integration page</span></span>

1. <span data-ttu-id="f96f5-120">Í mannauðssíðunni þar sem þú vilt skoða eða stilla stillingar fyrir samþættingu við Dataverse, veldu reitinn **Kerfisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="f96f5-120">In the Human Resources instance where you want to view or configure settings for the integration with Dataverse, select the **System administration** tile.</span></span>

    <span data-ttu-id="f96f5-121">[![Reiturinn Kerfisstjórnun](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="f96f5-121">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="f96f5-122">Veldu flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="f96f5-122">Select the **Links** tab.</span></span>

    <span data-ttu-id="f96f5-123">[![Tegnlaflipi](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="f96f5-123">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="f96f5-124">Undir **Sameiningar**, veldu **Dataverse stillingar**.</span><span class="sxs-lookup"><span data-stu-id="f96f5-124">Under **Integrations**, select **Dataverse configuration**.</span></span>

    <span data-ttu-id="f96f5-125">[![Dataverse skilgreiningartengill](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span><span class="sxs-lookup"><span data-stu-id="f96f5-125">[![Dataverse configuration link](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a><span data-ttu-id="f96f5-126">Kveiktu eða slökktu á samþættingu gagna milli mannauðs og Dataverse</span><span class="sxs-lookup"><span data-stu-id="f96f5-126">Turn data integration between Human Resources and Dataverse on or off</span></span>

- <span data-ttu-id="f96f5-127">Til að kveikja á samþættingu skal stilla valkostinn **Virkja Dataverse-samþættingu** á **Já** á síðunni **Microsoft Dataverse-samþætting**.</span><span class="sxs-lookup"><span data-stu-id="f96f5-127">To turn on integration, set the **Enable Dataverse integration** option to **Yes** on the **Microsoft Dataverse integration** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f96f5-128">Þegar þú kveikir á samþættingu verða gögn samstillt næst þegar runuvinnslan **Dataverse samstilling missti af beiðni samstillingar** keyrir.</span><span class="sxs-lookup"><span data-stu-id="f96f5-128">When you turn on integration, data will be synced the next time that the **Dataverse integration missed request sync** batch job runs.</span></span> <span data-ttu-id="f96f5-129">Öll gögn ættu að vera tiltæk eftir að runuvinnsla er lokið.</span><span class="sxs-lookup"><span data-stu-id="f96f5-129">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="f96f5-130">Til að slökkva á samþættingu skaltu stilla valkostinn á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="f96f5-130">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="f96f5-131">[![Kveikt eða slökkt á Dataverse samþættingu](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span><span class="sxs-lookup"><span data-stu-id="f96f5-131">[![Turning the Dataverse integration on or off](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span></span>

> [!WARNING]
> <span data-ttu-id="f96f5-132">Við mælum eindregið með því að slökkva á Dataverse-samþættingu þegar gagnasamþættingarverk er framkvæmt.</span><span class="sxs-lookup"><span data-stu-id="f96f5-132">We strongly recommend turning off Dataverse integration while performing data migration tasks.</span></span> <span data-ttu-id="f96f5-133">Stórar upphleðslur gagna geta haft umtalsverð áhrif á afköst.</span><span class="sxs-lookup"><span data-stu-id="f96f5-133">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="f96f5-134">Til dæmis getur upphleðsla á 2000 starfsmönnum tekið nokkrar klukkustundir þegar kveikt er á samþættingu, og innan við klukkustund þegar slökkt er á henni.</span><span class="sxs-lookup"><span data-stu-id="f96f5-134">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="f96f5-135">Tölurnar sem gefnar eru upp í þessu dæmi eru til sýnis eingöngu.</span><span class="sxs-lookup"><span data-stu-id="f96f5-135">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="f96f5-136">Tíminn sem það nákvæmlega tekur að flytja inn færslur getur verið mjög breytilegur vegna ýmissa þátta.</span><span class="sxs-lookup"><span data-stu-id="f96f5-136">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="f96f5-137">Skoða upplýsingar um gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="f96f5-137">View data integration details</span></span>

<span data-ttu-id="f96f5-138">Í flýtiflipanum **Stjórnun** á síðunni **Microsoft Dataverse-samþætting** er hægt að sjá hvernig línur eru tengdar saman milli Human Resources og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f96f5-138">On the **Administration** FastTab of the **Microsoft Dataverse integration** page, you can see how rows are linked together between Human Resources and Dataverse.</span></span>

- <span data-ttu-id="f96f5-139">Til að skoða línur fyrir töflu skal velja töfluna í reitnum **Dataverse-tafla**.</span><span class="sxs-lookup"><span data-stu-id="f96f5-139">To view the rows for a table, select the table in the **Dataverse table** field.</span></span> <span data-ttu-id="f96f5-140">Hnitanetið sýnir allar línur sem eru tengdar við valda töflu.</span><span class="sxs-lookup"><span data-stu-id="f96f5-140">The grid shows all the rows that are linked to the selected table.</span></span>

> [!NOTE]
> <span data-ttu-id="f96f5-141">Ekki eru allar Dataverse-töflur á listanum sem stendur.</span><span class="sxs-lookup"><span data-stu-id="f96f5-141">Not all Dataverse tables are currently listed.</span></span> <span data-ttu-id="f96f5-142">Aðeins töflur sem styðja notkun sérstilltra reita birtast í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="f96f5-142">Only tables that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="f96f5-143">Nýjar töflur verða fáanlegar með áframhaldandi útgáfum Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f96f5-143">New tables become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="f96f5-144">Taflan inniheldur eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="f96f5-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="f96f5-145">**Dataverse-tafla** – Heiti töflunnar í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f96f5-145">**Dataverse table** – The name of the table in Dataverse.</span></span>
- <span data-ttu-id="f96f5-146">**Dataverse-töflutilvísun** – Kennið sem Dataverse notar til að auðkenna færslu.</span><span class="sxs-lookup"><span data-stu-id="f96f5-146">**Dataverse table reference** – The identifier that Dataverse uses to identify a record.</span></span> <span data-ttu-id="f96f5-147">Þetta gildi jafngildir Human Resources gildinu **RecId**.</span><span class="sxs-lookup"><span data-stu-id="f96f5-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="f96f5-148">Kennið er hægt að finna þegar Dataverse-taflan í Microsoft Excel er opnuð.</span><span class="sxs-lookup"><span data-stu-id="f96f5-148">You can find the identifier when you open the Dataverse table in Microsoft Excel.</span></span>
- <span data-ttu-id="f96f5-149">**Einingarheiti Human Resources** – Eining Human Resources sem síðast samstillti gögn við Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f96f5-149">**Human Resources entity name** – The Human Resources entity that last synced data to Dataverse.</span></span> <span data-ttu-id="f96f5-150">Einingin getur haft annaðhvort Dataverse forskeyti eða annað forskeyti.</span><span class="sxs-lookup"><span data-stu-id="f96f5-150">The entity can have either the Dataverse prefix or another prefix.</span></span>
- <span data-ttu-id="f96f5-151">**Tilvísun Human Resources** - Gildið **RecId** sem er tengt skránni í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f96f5-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="f96f5-152">**Eytt úr Dataverse** – Gildi sem segir til um hvort línu var eytt úr Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f96f5-152">**Deleted from Dataverse** – A value that indicates whether the row was deleted from Dataverse.</span></span>

> [!NOTE]
> <span data-ttu-id="f96f5-153">Færslur í Human Resources samsvara línum í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f96f5-153">Records in Human Resources correspond to rows in Dataverse.</span></span>

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a><span data-ttu-id="f96f5-154">Fjarlægja tengingu á færslu Human Resources úr Dataverse-línu</span><span class="sxs-lookup"><span data-stu-id="f96f5-154">Remove the association of a Human Resources record from a Dataverse row</span></span>

<span data-ttu-id="f96f5-155">Ef þú lendir í vandræðum við samstillingu gagna milli mannauðs og Dataverse, gætirðu verið fær um að leysa þau með því að hreinsa mælingarnar og láta endurstilla rakningartöfluna.</span><span class="sxs-lookup"><span data-stu-id="f96f5-155">If you experience issues during data synchronization between Human Resources and Dataverse, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="f96f5-156">Ef tenging er fjarlægð og línu síðan breytt eða henni eytt í Dataverse verða breytingarnar ekki samstilltar við Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f96f5-156">If you remove the association, and then change or delete a row in Dataverse, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="f96f5-157">Ef gerðar eru breytingar á Human Resources verður ný rakningarfærsla stofnuð og línan verður uppfærð í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f96f5-157">If you make changes in Human Resources, a new tracking record is created, and the row is updated in Dataverse.</span></span>

- <span data-ttu-id="f96f5-158">Til að fjarlægja tengingu á færslu Human Resources og Dataverse-línu skal velja töfluna í reitnum **Dataverse-tafla** og síðan velja **Hreinsa rakningarupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="f96f5-158">To remove the association of a Human Resources record and a Dataverse row, select the table in the **Dataverse table** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="f96f5-159">[![Hreinsun rakningarupplýsinga](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="f96f5-159">[![Clearing tracking information](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span></span>

<span data-ttu-id="f96f5-160">Til að keyra fulla samstillingu á töflunni eftir að rakning er hreinsuð skal sjá næsta skref.</span><span class="sxs-lookup"><span data-stu-id="f96f5-160">To run a full synchronization on the table after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-a-table-between-human-resources-and-dataverse"></a><span data-ttu-id="f96f5-161">Samstilla töflu á milli Human Resources og Dataverse</span><span class="sxs-lookup"><span data-stu-id="f96f5-161">Sync a table between Human Resources and Dataverse</span></span>

<span data-ttu-id="f96f5-162">Notaðu þetta ferli þegar:</span><span class="sxs-lookup"><span data-stu-id="f96f5-162">Use this procedure when:</span></span>

- <span data-ttu-id="f96f5-163">Breytingar úr Dataverse taka of langan tíma að birtast í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f96f5-163">Changes from Dataverse take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="f96f5-164">Þú verður að endurræsa rakningartöfluna þegar þú hefur eytt rakningunni.</span><span class="sxs-lookup"><span data-stu-id="f96f5-164">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="f96f5-165">Til að keyra fulla samstillingu á töflu milli Human Resources og Dataverse:</span><span class="sxs-lookup"><span data-stu-id="f96f5-165">To run a full synchronization on a table between Human Resources and Dataverse:</span></span>

1. <span data-ttu-id="f96f5-166">Veljið töfluna í reitnum **Dataverse-tafla**.</span><span class="sxs-lookup"><span data-stu-id="f96f5-166">Select the table in the **Dataverse table** field.</span></span>

2. <span data-ttu-id="f96f5-167">Veldu **Samstilla núna**.</span><span class="sxs-lookup"><span data-stu-id="f96f5-167">Select **Sync now**.</span></span>

<span data-ttu-id="f96f5-168">[![Keyri fulla samstillingu](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="f96f5-168">[![Running a full synchronization](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="f96f5-169">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f96f5-169">See also</span></span>

[<span data-ttu-id="f96f5-170">Dataverse töflur</span><span class="sxs-lookup"><span data-stu-id="f96f5-170">Dataverse tables</span></span>](hr-developer-entities.md)<br>
[<span data-ttu-id="f96f5-171">Skilgreina Dataverse-sýndartöflur</span><span class="sxs-lookup"><span data-stu-id="f96f5-171">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="f96f5-172">Algengar spurningar um sýndartöflur Human Resources</span><span class="sxs-lookup"><span data-stu-id="f96f5-172">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="f96f5-173">Hvað er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="f96f5-173">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="f96f5-174">Hugtakauppfærslur</span><span class="sxs-lookup"><span data-stu-id="f96f5-174">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)
