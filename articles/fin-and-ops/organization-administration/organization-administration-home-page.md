---
title: "Fyrirtækisstjórnun – heimasíða"
description: "Þetta efnisatriði vísar á tilföng sem munu hjálpa til við að nota Microsoft Dynamics 365 for Finance and Operations í fyrirtækinu."
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: a2c1d846527eac4db0a043c7f1c51da0e73bd796
ms.contentlocale: is-is
ms.lasthandoff: 03/26/2018

---

# <a name="organization-administration-home-page"></a><span data-ttu-id="fa8dd-103">Fyrirtækisstjórnun – heimasíða</span><span class="sxs-lookup"><span data-stu-id="fa8dd-103">Organization administration home page</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fa8dd-104">Þetta efnisatriði vísar á efni sem mun hjálpa kraftnotendum og stjórnendum að skilgreina Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-104">This topic points to content that will help power users and administrators configure Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="fa8dd-105">Þetta efni mun hjálpa þeim að skilgreina kerfið til að vinna vel og skilvirkt fyrir fyrirtæki þitt og rekstur.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-105">This content will help them configure the system to work smoothly and effectively for your organization and business.</span></span>

<span data-ttu-id="fa8dd-106">Mikið af því efni sem hér er að finna gildir um aðgerðir í einingunni **Stjórnun fyrirtækis**</span><span class="sxs-lookup"><span data-stu-id="fa8dd-106">Much of the content listed here applies to features in the **Organizational administration** module.</span></span> <span data-ttu-id="fa8dd-107">Hins vegar eru nokkrar verkefni, svo sem að búa til og nota skráarsniðmát, sem hægt er að framkvæma í hvaða mát sem er til að hjálpa fyrirtækinu að keyra á skilvirkan hátt.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-107">However, there are a couple of tasks, such as creating and using a record template, that can be performed in any module to help your organization run more efficiently.</span></span> 

<a name="number-sequences"></a><span data-ttu-id="fa8dd-108">Númeraraðir</span><span class="sxs-lookup"><span data-stu-id="fa8dd-108">Number sequences</span></span>
----------------
<span data-ttu-id="fa8dd-109">Númeraraðir eru notaðar til að mynda lesanleg, einkvæm kennimerki fyrir skýrslur aðalgagna og færslur sem krefjast kennimerkja.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-109">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="fa8dd-110">færsla aðalgagna eða færsla sem krefst kennimerkis er vísað til sem *tilvísun*.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-110">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span> <span data-ttu-id="fa8dd-111">Áður en hægt er að stofna nýjar færslur fyrir tilvísun verður að setja upp númeraröð og tengja hana við tilvísunina.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-111">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span>

-   [<span data-ttu-id="fa8dd-112">Yfirlit yfir númeraröð</span><span class="sxs-lookup"><span data-stu-id="fa8dd-112">Number sequence overview</span></span>](number-sequence-overview.md)
-   <span data-ttu-id="fa8dd-113">[Setja upp númeraraðir með því að nota leiðsagnarforrit](tasks/set-up-number-sequences-wizard.md) (verkefnaleiðbeiningar)</span><span class="sxs-lookup"><span data-stu-id="fa8dd-113">[Set up number sequences by using a wizard](tasks/set-up-number-sequences-wizard.md) (Task guide)</span></span>
-   <span data-ttu-id="fa8dd-114">[Setja upp númeraröð á einstaklingsgrundvelli](tasks/set-up-number-sequences-individual-basis.md) (verkefnaleiðbeiningar)</span><span class="sxs-lookup"><span data-stu-id="fa8dd-114">[Set up number sequences on an individual basis](tasks/set-up-number-sequences-individual-basis.md) (Task guide)</span></span>

## <a name="organizations"></a><span data-ttu-id="fa8dd-115">Fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="fa8dd-115">Organizations</span></span>
<span data-ttu-id="fa8dd-116">Fyrirtæki er hópur af fólki sem eru að vinna saman að því að framkvæma viðskiptaferli eða ná markmiði.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-116">An organization is a group of people who are working together to carry out a business process or achieve a goal.</span></span> <span data-ttu-id="fa8dd-117">Stigveldi fyrirtækis standa fyrir vensl á milli fyrirtækja sem þú ert með saman í rekstri.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-117">Organizational hierarchies represent the relationships between the organizations that make up your business.</span></span>

<span data-ttu-id="fa8dd-118">Áður en að fyrirtæki og stigveldi fyrirtækis eru sett upp í Finance and Operations , skaltu gæta þess að skipuleggja hvernig fyrirtækið mun þróast.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-118">Before you set up organizations and organization hierarchies in Finance and Operations, make sure that you plan how your business will be modeled.</span></span> <span data-ttu-id="fa8dd-119">Fyrirtækjalíkan hefur töluverð áhrif á innleiðingu á Finance and Operations og í viðskiptaferlum.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-119">The organization model has a significant effect on the implementation of Finance and Operations and on business processes.</span></span>

-   [<span data-ttu-id="fa8dd-120">Fyrirtæki og fyrirtækjastigveldi</span><span class="sxs-lookup"><span data-stu-id="fa8dd-120">Organizations and organizational hierarchies</span></span>](organizations-organizational-hierarchies.md)
-   [<span data-ttu-id="fa8dd-121">Skipuleggja fyrirtækjastigveldi</span><span class="sxs-lookup"><span data-stu-id="fa8dd-121">Plan your organizational hierarchy</span></span>](plan-organizational-hierarchy.md)
-   <span data-ttu-id="fa8dd-122">[Stofna stigveldi fyrirtækis](tasks/create-organization-hierarchy.md) (verkefnaleiðbeiningar)</span><span class="sxs-lookup"><span data-stu-id="fa8dd-122">[Create an organization hierarchy](tasks/create-organization-hierarchy.md) (Task guide)</span></span>
-   <span data-ttu-id="fa8dd-123">[Stofna lögaðila](tasks/create-legal-entity.md) (verkefnaleiðbeiningar)</span><span class="sxs-lookup"><span data-stu-id="fa8dd-123">[Create a legal entity](tasks/create-legal-entity.md) (Task guide)</span></span>
-   <span data-ttu-id="fa8dd-124">[Stofna rekstrareiningu](tasks/create-operating-unit.md) (verkefnaleiðbeiningar)</span><span class="sxs-lookup"><span data-stu-id="fa8dd-124">[Create an operating unit](tasks/create-operating-unit.md) (Task guide)</span></span>

## <a name="address-books"></a><span data-ttu-id="fa8dd-125">Aðsetursbækur</span><span class="sxs-lookup"><span data-stu-id="fa8dd-125">Address books</span></span>
<span data-ttu-id="fa8dd-126">Altæk aðsetursbók er miðlæg geymsla fyrir aðalgögn sem verður að geyma fyrir alla innri og ytri einstaklinga og fyrirtæki sem fyrirtækið hefur samskipti við.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-126">The global address book is a centralized repository for master data that must be stored for all internal and external persons and organizations that the company interacts with.</span></span> <span data-ttu-id="fa8dd-127">Gögnin sem tengjast tengdum skrám innihalda nafn, heimilisfang og upplýsingar um aðila.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-127">The data that is associated with party records includes the party's name, address, and contact information.</span></span> 

<span data-ttu-id="fa8dd-128">Þegar Búið er að stofna altæka aðsetursbók, er hægt að stofna viðbótar aðsetursbækur sem þörf er á, svo sem aðskilda aðsetursbókar fyrir hvert fyrirtæki í þínu samsteypu eða fyrir hverja atvinnugrein.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-128">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> 

-   [<span data-ttu-id="fa8dd-129">Altæk aðsetursbók</span><span class="sxs-lookup"><span data-stu-id="fa8dd-129">Global address book</span></span>](overview-global-address-book.md)
-   [<span data-ttu-id="fa8dd-130">Áætlun um uppsetningu altækrar aðsetursbókar og annarra aðsetursbóka</span><span class="sxs-lookup"><span data-stu-id="fa8dd-130">Plan how to configure the global address book and additional address books</span></span>](plan-configuration-global-address-book-additional-address-books.md)
- [<span data-ttu-id="fa8dd-131">Skilgreina altæku aðsetursbókina</span><span class="sxs-lookup"><span data-stu-id="fa8dd-131">Configure the global address book</span></span>](tasks/configure-global-address-book.md)
-   [<span data-ttu-id="fa8dd-132">Algengar spurningar um aðsetursbækur</span><span class="sxs-lookup"><span data-stu-id="fa8dd-132">Address books FAQ</span></span>](qa-address-books.md)


## <a name="workflow"></a><span data-ttu-id="fa8dd-133">Verkflæði</span><span class="sxs-lookup"><span data-stu-id="fa8dd-133">Workflow</span></span>
<span data-ttu-id="fa8dd-134">Verkflæði  er kerfi sem var uppsett með Finance and Operations og má nota við gerð einstaks verkflæðis, eða viðskiptaferla.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-134">Workflow is a system that is installed with Finance and Operations that you can use to create individual workflows, or business processes.</span></span> <span data-ttu-id="fa8dd-135">Það skilgreinir hvernig skjal flæðir eða hreyfist gegnum kerfið með því að sýna hver verður að ljúka verki, taka ákvörðun eða samþykkja skjal.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-135">When you create a workflow, you specify how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> 

-   [<span data-ttu-id="fa8dd-136">Yfirlit yfir verkflæði</span><span class="sxs-lookup"><span data-stu-id="fa8dd-136">Workflow overview</span></span>](overview-workflow-system.md)
-   [<span data-ttu-id="fa8dd-137">Verkflæðiseiningar</span><span class="sxs-lookup"><span data-stu-id="fa8dd-137">Workflow elements</span></span>](workflow-elements.md)
-   [<span data-ttu-id="fa8dd-138">Verkflæðisaðgerðir</span><span class="sxs-lookup"><span data-stu-id="fa8dd-138">Workflow actions</span></span>](workflow-actions.md)
-   [<span data-ttu-id="fa8dd-139">Verkflæði stofnað</span><span class="sxs-lookup"><span data-stu-id="fa8dd-139">Create a workflow</span></span>](create-workflow.md)

## <a name="electronic-signatures"></a><span data-ttu-id="fa8dd-140">Rafrænar undirskriftir</span><span class="sxs-lookup"><span data-stu-id="fa8dd-140">Electronic signatures</span></span>
<span data-ttu-id="fa8dd-141">Rafræn undirskrift staðfestir deili á þeim aðila sem er í þann mund að hefja eða samþykkja ferli.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-141">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="fa8dd-142">Innan sumra atvinnugreina er rafræn undirskrift jafn bindandi að lögum og handskrifuð.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-142">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span> <span data-ttu-id="fa8dd-143">Reglur kveða á um rafrænar undirskriftir innan ýmissa atvinnugreina sem eru háðar opinberum reglugerðum, svo sem við lyfja-, matvæla- og drykkjarvöruframleiðslu og í flugvéla- og geimiðnaði og varnariðnaði.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-143">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span>

<span data-ttu-id="fa8dd-144">Hægt er að nota rafrænar undirskriftir fyrir mikilvæg viðskiptaferli í Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-144">In Finance and Operations, you can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="fa8dd-145">Rafrænar undirskriftir eru innbyggður hluti sumra ferla.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-145">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="fa8dd-146">Hægt er að búa til kröfur um rafrænar undirskriftir fyrir hvaða gagnagrunn eða svæði sem er.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-146">You can also create custom signature requirements for any database table and field.</span></span>

-   [<span data-ttu-id="fa8dd-147">Yfirlit yfir rafræna undirskrift</span><span class="sxs-lookup"><span data-stu-id="fa8dd-147">Electronic signature overview</span></span>](electronic-signature-overview.md)
-   <span data-ttu-id="fa8dd-148">[Uppsetning rafræna undirskrifta](tasks/set-up-electronic-signatures.md) (verkefnaleiðbeiningar)</span><span class="sxs-lookup"><span data-stu-id="fa8dd-148">[Set up electronic signatures](tasks/set-up-electronic-signatures.md) (Task guide)</span></span>

## <a name="case-management"></a><span data-ttu-id="fa8dd-149">Málastjórnun</span><span class="sxs-lookup"><span data-stu-id="fa8dd-149">Case management</span></span>
<span data-ttu-id="fa8dd-150">Eftir áætlun, rakningu og greina tilvikum, getur þróa skilvirkar úrlausnir sem hægt er að nota fyrir úthreyfingar svipuð.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-150">By planning, tracking, and analyzing cases, you can develop efficient resolutions that can be used for similar issues.</span></span> <span data-ttu-id="fa8dd-151">Til dæmis, þegar þjónustufulltrúar eða starfsmenn almennra starfsmanna búa til mál geta þau fundið upplýsingar í fræðslugreinum til að hjálpa þeim að vinna með eða leysa mál á skilvirkan hátt.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-151">For example, when customer service representatives or Human Resources generalists create cases, they can find information in knowledge articles to help them work with or resolve a case more efficiently.</span></span> 

-   [<span data-ttu-id="fa8dd-152">Málastjórnunaryfirlit</span><span class="sxs-lookup"><span data-stu-id="fa8dd-152">Case management overview</span></span>](cases.md)
-   [<span data-ttu-id="fa8dd-153">Skilgreining öryggis, vinnsla og flokka mála</span><span class="sxs-lookup"><span data-stu-id="fa8dd-153">Configure case security, processes, and categories</span></span>](plan-case-management.md)

## <a name="record-templates"></a><span data-ttu-id="fa8dd-154">Færslusniðmát</span><span class="sxs-lookup"><span data-stu-id="fa8dd-154">Record templates</span></span>
<span data-ttu-id="fa8dd-155">Færslusniðmát geta hjálpað til við að stofna færslur hraðar.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-155">Record templates can help you to create records more quickly.</span></span> <span data-ttu-id="fa8dd-156">Hægt er að stofna færslusniðmát til að gildi í svæði sem er oft notað ekki þurfa að slá inn sérstaklega fyrir hverja ný færsla.</span><span class="sxs-lookup"><span data-stu-id="fa8dd-156">You can create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> 

-   [<span data-ttu-id="fa8dd-157">Færslusniðmát</span><span class="sxs-lookup"><span data-stu-id="fa8dd-157">Record templates</span></span>](record-templates.md)
- <span data-ttu-id="fa8dd-158">[Stofna færslusniðmát til að auðvelda gagnaskráning](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Verkefnaleiðbeiningar)</span><span class="sxs-lookup"><span data-stu-id="fa8dd-158">[Create a record template to facilitate data entry](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Task guide)</span></span>
- <span data-ttu-id="fa8dd-159">[Nota færslusniðmát til að búa til nýja færslu](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md)(Verkefnaleiðbeiningar)</span><span class="sxs-lookup"><span data-stu-id="fa8dd-159">[Use a record template to create a new record](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Task guide)</span></span>

## <a name="general-organization-administration"></a><span data-ttu-id="fa8dd-160">Almenn stjórnun fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="fa8dd-160">General organization administration</span></span>
-   <span data-ttu-id="fa8dd-161">[Breyta borða eða merki fyrirtækis](../get-started/tasks/change-banner-or-logo.md) (verkefnaleiðbeiningar)</span><span class="sxs-lookup"><span data-stu-id="fa8dd-161">[Change the banner or logo](../get-started/tasks/change-banner-or-logo.md) (Task guide)</span></span>
- [<span data-ttu-id="fa8dd-162">Stilla skjalastjórnun</span><span class="sxs-lookup"><span data-stu-id="fa8dd-162">Configure document management</span></span>](configure-document-management.md)
- [<span data-ttu-id="fa8dd-163">Skilgreining og sending tölvupósts</span><span class="sxs-lookup"><span data-stu-id="fa8dd-163">Configure and send email</span></span>](configure-email.md)
-   [<span data-ttu-id="fa8dd-164">Dagsetningar-/tímagögn og tímabelti</span><span class="sxs-lookup"><span data-stu-id="fa8dd-164">Date/time data and time zones</span></span>](date-time-zones.md)








