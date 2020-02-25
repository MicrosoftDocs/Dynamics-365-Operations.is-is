---
title: Skilgreina Common Data Service-samþættingu
description: Þú getur kveikt eða slökkt á samþættingu á milli Common Data Service og tilviks af Microsoft Dynamics 365 Human Resources. Þú getur einnig skoðað upplýsingar um samstillingu, hreinsað mælingargögn og endurstillt eining til að hjálpa til við að leysa úr gögnum á milli umhverfanna tveggja.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009384"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="eaac3-104">Skilgreina Common Data Service-samþættingu</span><span class="sxs-lookup"><span data-stu-id="eaac3-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="eaac3-105">Þú getur kveikt eða slökkt á samþættingu á milli Common Data Service og tilviks af Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="eaac3-105">You can turn integration between Common Data Service and an instance of Microsoft Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="eaac3-106">Þú getur einnig skoðað upplýsingar um samstillingu, hreinsað mælingargögn og endurstillt eining til að hjálpa til við að leysa úr gögnum á milli umhverfanna tveggja.</span><span class="sxs-lookup"><span data-stu-id="eaac3-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="eaac3-107">Þegar þú slekkur á samþættingu geta notendur gert breytingar á starfsmannahaldi eða Common Data Service, en þessar breytingar eru ekki samstilltar milli umhverfisins tveggja.</span><span class="sxs-lookup"><span data-stu-id="eaac3-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="eaac3-108">Sjálfgefið er annaðhvort er slökkt eða kveikt á samþættingu Human Resources og Common Data Service slökkt eða slökkt, allt eftir tilvist sýnigagna í umhverfinu:</span><span class="sxs-lookup"><span data-stu-id="eaac3-108">By default, integration between Human Resources and Common Data Service is turned either off or on, depending on the presence of demo data in the environments:</span></span>

- <span data-ttu-id="eaac3-109">**Slökkt** fyrir nýtt umhverfi sem inniheldur ekki kynningargögn</span><span class="sxs-lookup"><span data-stu-id="eaac3-109">**Off** for new environments that don't include demo data</span></span>
- <span data-ttu-id="eaac3-110">**Kveikt** fyrir nýtt umhverfi sem inniheldur kynningargögn</span><span class="sxs-lookup"><span data-stu-id="eaac3-110">**On** for new environments that include demo data</span></span>

<span data-ttu-id="eaac3-111">Nýtt umhverfi sem inniheldur prufugögn mun byrja að samstilla gögn þegar þeim er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="eaac3-111">New environments that include demo data will start to sync data when they are provisioned.</span></span>

<span data-ttu-id="eaac3-112">Þú gætir viljað slökkva á samþættingu við þessar aðstæður:</span><span class="sxs-lookup"><span data-stu-id="eaac3-112">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="eaac3-113">Þú ert að fylla út gögn í gegnum Data Management Framework og verður að flytja gögnin inn nokkrum sinnum til að koma þeim í rétt ástand.</span><span class="sxs-lookup"><span data-stu-id="eaac3-113">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="eaac3-114">Það eru vandamál með gögn í annaðhvort Human Resources eða Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="eaac3-114">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="eaac3-115">Ef slökkt er á samþættingu geturðu eytt skrá í einu umhverfi án þess að eyða því í hinu.</span><span class="sxs-lookup"><span data-stu-id="eaac3-115">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="eaac3-116">Þegar þú kveikir aftur á samþættingu verður skráin í umhverfinu þar sem henni var ekki eytt samstillt aftur við umhverfið þar sem henni var eytt.</span><span class="sxs-lookup"><span data-stu-id="eaac3-116">When you turn integration back on, the record in the environment where it wasn't deleted will be synced back to the environment where it was deleted.</span></span> <span data-ttu-id="eaac3-117">Samstilling hefst næst þegar runuvinnslan **Common Data Service samstilling missti af beiðni samstillingar** keyrir.</span><span class="sxs-lookup"><span data-stu-id="eaac3-117">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="eaac3-118">Þegar þú slekkur á samþættingu gagna, vertu viss um að þú breytir ekki sömu skránni í báðum umhverfunum.</span><span class="sxs-lookup"><span data-stu-id="eaac3-118">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="eaac3-119">Þegar þú kveikir aftur á samþættingu verður skráin sem þú breyttir síðast samstillt.</span><span class="sxs-lookup"><span data-stu-id="eaac3-119">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="eaac3-120">Þess vegna, ef þú gerðir ekki sömu breytingar á skránni í báðum umhverfunum, getur gagnatap orðið.</span><span class="sxs-lookup"><span data-stu-id="eaac3-120">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="eaac3-121">Aðgangur að Common Data Service sameiningarsíðu</span><span class="sxs-lookup"><span data-stu-id="eaac3-121">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="eaac3-122">Í mannauðssíðunni þar sem þú vilt skoða eða stilla stillingar fyrir samþættingu við Common Data Service, veldu reitinn **Kerfisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="eaac3-122">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="eaac3-123">[![Reiturinn Kerfisstjórnun](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="eaac3-123">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="eaac3-124">Veldu flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="eaac3-124">Select the **Links** tab.</span></span>

    <span data-ttu-id="eaac3-125">[![Tegnlaflipi](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="eaac3-125">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="eaac3-126">Undir **Sameiningar**, veldu **Common Data Service stillingar**.</span><span class="sxs-lookup"><span data-stu-id="eaac3-126">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="eaac3-127">[![Common Data Service skilgreiningartengill](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="eaac3-127">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="eaac3-128">Kveiktu eða slökktu á samþættingu gagna milli mannauðs og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="eaac3-128">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="eaac3-129">Til að kveikja á samþættingu skaltu stilla valkostinn **Virkja samþættingu við Common Data Service** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="eaac3-129">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="eaac3-130">Þegar þú kveikir á samþættingu verða gögn samstillt næst þegar runuvinnslan **Common Data Service samstilling missti af beiðni samstillingar** keyrir.</span><span class="sxs-lookup"><span data-stu-id="eaac3-130">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="eaac3-131">Öll gögn ættu að vera tiltæk eftir að runuvinnsla er lokið.</span><span class="sxs-lookup"><span data-stu-id="eaac3-131">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="eaac3-132">Til að slökkva á samþættingu skaltu stilla valkostinn á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="eaac3-132">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="eaac3-133">[![Kveikt eða slökkt á Common Data Service samþættingu](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="eaac3-133">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="eaac3-134">Skoða upplýsingar um gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="eaac3-134">View data integration details</span></span>

<span data-ttu-id="eaac3-135">Á flýtiflipanum **Stjórnun** á síðunni **Common Data Service samþætting** er hægt að sjá hvernig skrár eru tengdar saman milli Human Resources og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="eaac3-135">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="eaac3-136">Til að skoða skrár fyrir einingu velurðu aðilann í reitnum **Heiti CDS einingar**.</span><span class="sxs-lookup"><span data-stu-id="eaac3-136">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="eaac3-137">Taflan sýnir allar færslur sem eru tengdar völdum einingum.</span><span class="sxs-lookup"><span data-stu-id="eaac3-137">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="eaac3-138">[![Skoða færslur fyrir einingu](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="eaac3-138">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="eaac3-139">Ekki eru allar einingar Common Data Service eru sem stendur skráðar.</span><span class="sxs-lookup"><span data-stu-id="eaac3-139">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="eaac3-140">Aðeins einingar sem styðja notkun sérsniðinna reita birtast í töflunni.</span><span class="sxs-lookup"><span data-stu-id="eaac3-140">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="eaac3-141">Nýjar einingar verða tiltækar með stöðugu losun Human Resources.</span><span class="sxs-lookup"><span data-stu-id="eaac3-141">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="eaac3-142">Taflan inniheldur eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="eaac3-142">The grid includes the following fields:</span></span>

- <span data-ttu-id="eaac3-143">**CDS-einingaheiti** - Heiti öryggiseiningarinnar í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="eaac3-143">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="eaac3-144">**Tilvísun CDS einingar** - Kennimerkið sem Common Data Service notar til að bera kennsl á skrá.</span><span class="sxs-lookup"><span data-stu-id="eaac3-144">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="eaac3-145">Þetta gildi jafngildir Human Resources gildinu **RecId**.</span><span class="sxs-lookup"><span data-stu-id="eaac3-145">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="eaac3-146">Þú getur fundið kennimerki þegar þú opnar Common Data Service einingu í Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="eaac3-146">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="eaac3-147">**Einingaheiti Human Resources** - Einingin sem síðast samstillti gögn við Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="eaac3-147">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="eaac3-148">Einingin getur haft annaðhvort Common Data Service forskeyti eða annað forskeyti.</span><span class="sxs-lookup"><span data-stu-id="eaac3-148">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="eaac3-149">**Tilvísun Human Resources** - Gildið **RecId** sem er tengt skránni í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="eaac3-149">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="eaac3-150">**Var eytt úr CDS** - Gildi sem gefur til kynna hvort skránni hafi verið eytt úr Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="eaac3-150">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="eaac3-151">Fjarlægðu tengsl skrárinnar í Human Resources úr Common Data Service</span><span class="sxs-lookup"><span data-stu-id="eaac3-151">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="eaac3-152">Ef þú lendir í vandræðum við samstillingu gagna milli mannauðs og Common Data Service, gætirðu verið fær um að leysa þau með því að hreinsa mælingarnar og láta endurstilla rakningartöfluna.</span><span class="sxs-lookup"><span data-stu-id="eaac3-152">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="eaac3-153">Ef þú fjarlægir tenginguna og breytir síðan eða eyðir skrá í Common Data Service, breytingarnar verða ekki samstilltar við Human Resources.</span><span class="sxs-lookup"><span data-stu-id="eaac3-153">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="eaac3-154">Ef þú gerir breytingar á Human Resources verður ný rekja rakningarskrá til og færslan uppfærð í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="eaac3-154">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="eaac3-155">Til að fjarlægja tengsl skrár milli mannauðs og Common Data Service, veldu eininguna í reitnum **Heiti CDS einingar** og veldu síðan **Hreinsa rakningarupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="eaac3-155">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="eaac3-156">[![Hreinsun rakningarupplýsinga](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="eaac3-156">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="eaac3-157">Sjá næstu aðferð til að keyra fulla samstillingu á einingunni eftir að þú hefur eytt mælingunni.</span><span class="sxs-lookup"><span data-stu-id="eaac3-157">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="eaac3-158">Samstilltu eining milli Human Resources og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="eaac3-158">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="eaac3-159">Notaðu þessa aðferð ef breytingar eru frá Common Data Service tekur of langan tíma að birtast í Human Resources, eða ef þú verður að endurnýja mælingarborðið eftir að þú hefur hreinsað mælingarnar.</span><span class="sxs-lookup"><span data-stu-id="eaac3-159">Use this procedure if changes from Common Data Service are taking too long to appear in Human Resources, or if you must refresh the tracking table after you clear the tracking.</span></span>

- <span data-ttu-id="eaac3-160">Til að keyra fulla samstillingu á aðila milli mannauðs og Common Data Service, veldu eininguna í reitnum **Heiti CDS einingar** og veldu síðan **Samstilla núna**.</span><span class="sxs-lookup"><span data-stu-id="eaac3-160">To run a full synchronization on an entity between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Sync now**.</span></span>

<span data-ttu-id="eaac3-161">[![Keyri fulla samstillingu](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="eaac3-161">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


