---
title: Skilgreina Common Data Service-samþættingu
description: Þú getur kveikt eða slökkt á samþættingu á milli Common Data Service og Dynamics 365 Human Resources. Þú getur einnig skoðað upplýsingar um samstillingu, hreinsað mælingargögn og endurstillt eining til að hjálpa til við að leysa úr gögnum á milli umhverfanna tveggja.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
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
ms.openlocfilehash: 7aad8217d48917d6855046a6810fe994f5564d94
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431315"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="d3bb6-104">Skilgreina Common Data Service-samþættingu</span><span class="sxs-lookup"><span data-stu-id="d3bb6-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="d3bb6-105">Þú getur kveikt eða slökkt á samþættingu á milli Common Data Service og Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-105">You can turn integration between Common Data Service and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="d3bb6-106">Þú getur einnig skoðað upplýsingar um samstillingu, hreinsað mælingargögn og endurstillt eining til að hjálpa til við að leysa úr gögnum á milli umhverfanna tveggja.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="d3bb6-107">Þegar þú slekkur á samþættingu geta notendur gert breytingar á starfsmannahaldi eða Common Data Service, en þessar breytingar eru ekki samstilltar milli umhverfisins tveggja.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="d3bb6-108">Sjálfgefið er að slökktu sé á samþættingu gagna milli Human Resources og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-108">By default, integration between Human Resources and Common Data Service is turned off.</span></span>

<span data-ttu-id="d3bb6-109">Þú gætir viljað slökkva á samþættingu við þessar aðstæður:</span><span class="sxs-lookup"><span data-stu-id="d3bb6-109">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="d3bb6-110">Þú ert að fylla út gögn í gegnum Data Management Framework og verður að flytja gögnin inn nokkrum sinnum til að koma þeim í rétt ástand.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-110">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="d3bb6-111">Það eru vandamál með gögn í annaðhvort Human Resources eða Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-111">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="d3bb6-112">Ef slökkt er á samþættingu geturðu eytt skrá í einu umhverfi án þess að eyða því í hinu.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-112">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="d3bb6-113">Þegar þú kveikir aftur á samþættingu samstillist skráin í umhverfinu þar sem henni var ekki eytt við umhverfið þar sem henni var eytt.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-113">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="d3bb6-114">Samstilling hefst næst þegar runuvinnslan **Common Data Service samstilling missti af beiðni samstillingar** keyrir.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-114">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="d3bb6-115">Þegar þú slekkur á samþættingu gagna, vertu viss um að þú breytir ekki sömu skránni í báðum umhverfunum.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-115">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="d3bb6-116">Þegar þú kveikir aftur á samþættingu verður skráin sem þú breyttir síðast samstillt.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-116">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="d3bb6-117">Þess vegna, ef þú gerðir ekki sömu breytingar á skránni í báðum umhverfunum, getur gagnatap orðið.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-117">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="d3bb6-118">Aðgangur að Common Data Service sameiningarsíðu</span><span class="sxs-lookup"><span data-stu-id="d3bb6-118">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="d3bb6-119">Í mannauðssíðunni þar sem þú vilt skoða eða stilla stillingar fyrir samþættingu við Common Data Service, veldu reitinn **Kerfisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-119">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="d3bb6-120">[![Reiturinn Kerfisstjórnun](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="d3bb6-120">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="d3bb6-121">Veldu flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-121">Select the **Links** tab.</span></span>

    <span data-ttu-id="d3bb6-122">[![Tegnlaflipi](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="d3bb6-122">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="d3bb6-123">Undir **Sameiningar**, veldu **Common Data Service stillingar**.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-123">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="d3bb6-124">[![Common Data Service skilgreiningartengill](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="d3bb6-124">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="d3bb6-125">Kveiktu eða slökktu á samþættingu gagna milli mannauðs og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d3bb6-125">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="d3bb6-126">Til að kveikja á samþættingu skaltu stilla valkostinn **Virkja samþættingu við Common Data Service** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-126">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d3bb6-127">Þegar þú kveikir á samþættingu verða gögn samstillt næst þegar runuvinnslan **Common Data Service samstilling missti af beiðni samstillingar** keyrir.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-127">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="d3bb6-128">Öll gögn ættu að vera tiltæk eftir að runuvinnsla er lokið.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-128">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="d3bb6-129">Til að slökkva á samþættingu skaltu stilla valkostinn á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-129">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="d3bb6-130">[![Kveikt eða slökkt á Common Data Service samþættingu](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="d3bb6-130">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="d3bb6-131">Skoða upplýsingar um gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="d3bb6-131">View data integration details</span></span>

<span data-ttu-id="d3bb6-132">Á flýtiflipanum **Stjórnun** á síðunni **Common Data Service samþætting** er hægt að sjá hvernig skrár eru tengdar saman milli Human Resources og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-132">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="d3bb6-133">Til að skoða skrár fyrir einingu velurðu aðilann í reitnum **Heiti CDS einingar**.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-133">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="d3bb6-134">Taflan sýnir allar færslur sem eru tengdar völdum einingum.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-134">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="d3bb6-135">[![Skoða færslur fyrir einingu](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="d3bb6-135">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="d3bb6-136">Ekki eru allar einingar Common Data Service eru sem stendur skráðar.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-136">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="d3bb6-137">Aðeins einingar sem styðja notkun sérsniðinna reita birtast í töflunni.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-137">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="d3bb6-138">Nýjar einingar verða tiltækar með stöðugu losun Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-138">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="d3bb6-139">Taflan inniheldur eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="d3bb6-139">The grid includes the following fields:</span></span>

- <span data-ttu-id="d3bb6-140">**CDS-einingaheiti** - Heiti öryggiseiningarinnar í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-140">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="d3bb6-141">**Tilvísun CDS einingar** - Kennimerkið sem Common Data Service notar til að bera kennsl á skrá.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-141">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="d3bb6-142">Þetta gildi jafngildir Human Resources gildinu **RecId**.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-142">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="d3bb6-143">Þú getur fundið kennimerki þegar þú opnar Common Data Service einingu í Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-143">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="d3bb6-144">**Einingaheiti Human Resources** - Einingin sem síðast samstillti gögn við Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-144">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="d3bb6-145">Einingin getur haft annaðhvort Common Data Service forskeyti eða annað forskeyti.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-145">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="d3bb6-146">**Tilvísun Human Resources** - Gildið **RecId** sem er tengt skránni í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-146">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="d3bb6-147">**Var eytt úr CDS** - Gildi sem gefur til kynna hvort skránni hafi verið eytt úr Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-147">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="d3bb6-148">Fjarlægðu tengsl skrárinnar í Human Resources úr Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d3bb6-148">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="d3bb6-149">Ef þú lendir í vandræðum við samstillingu gagna milli mannauðs og Common Data Service, gætirðu verið fær um að leysa þau með því að hreinsa mælingarnar og láta endurstilla rakningartöfluna.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-149">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="d3bb6-150">Ef þú fjarlægir tenginguna og breytir síðan eða eyðir skrá í Common Data Service, breytingarnar verða ekki samstilltar við Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-150">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="d3bb6-151">Ef þú gerir breytingar á Human Resources verður ný rekja rakningarskrá til og færslan uppfærð í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-151">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="d3bb6-152">Til að fjarlægja tengsl skrár milli mannauðs og Common Data Service, veldu eininguna í reitnum **Heiti CDS einingar** og veldu síðan **Hreinsa rakningarupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-152">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="d3bb6-153">[![Hreinsun rakningarupplýsinga](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="d3bb6-153">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="d3bb6-154">Sjá næstu aðferð til að keyra fulla samstillingu á einingunni eftir að þú hefur eytt mælingunni.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-154">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="d3bb6-155">Samstilltu eining milli Human Resources og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d3bb6-155">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="d3bb6-156">Notaðu þetta ferli þegar:</span><span class="sxs-lookup"><span data-stu-id="d3bb6-156">Use this procedure when:</span></span>

- <span data-ttu-id="d3bb6-157">Breytingar úr Common Data Service taka of langan tíma að birtast í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-157">Changes from Common Data Service take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="d3bb6-158">Þú verður að endurræsa rakningartöfluna þegar þú hefur eytt rakningunni.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-158">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="d3bb6-159">Til að keyra fulla samstillingu á einingu milli Human Resources og Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="d3bb6-159">To run a full synchronization on an entity between Human Resources and Common Data Service:</span></span>

1. <span data-ttu-id="d3bb6-160">Veldu einingu í reitnum **Heiti CDS-einingar**.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-160">Select the entity in the **CDS entity name** field.</span></span>

2. <span data-ttu-id="d3bb6-161">Veldu **Samstilla núna**.</span><span class="sxs-lookup"><span data-stu-id="d3bb6-161">Select **Sync now**.</span></span>

<span data-ttu-id="d3bb6-162">[![Keyri fulla samstillingu](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="d3bb6-162">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


