---
title: Algengar spurningar um verkflæði
description: Þetta efnisatriði svarar algengum spurningum um verkflæðiskerfið í Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adcc9bbc422a3fddfd51d248daf95c0da6d4c9bb
ms.sourcegitcommit: 8cf77e9171d6cad8ae6c8bfad9e4f9a46fef6d23
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/19/2019
ms.locfileid: "1689001"
---
# <a name="workflow-faq"></a><span data-ttu-id="34a7d-103">Algengar spurningar um verkflæði</span><span class="sxs-lookup"><span data-stu-id="34a7d-103">Workflow FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34a7d-104">Þetta efnisatriði svarar algengum spurningum um verkflæðiskerfið í Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="34a7d-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="34a7d-105">Hvers vegna koma margar tilkynningar þegar vinnulið er hafnað?</span><span class="sxs-lookup"><span data-stu-id="34a7d-105">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="34a7d-106">Þegar vinnulið er hafnað er honum lokið sem höfnuðum.</span><span class="sxs-lookup"><span data-stu-id="34a7d-106">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="34a7d-107">Annar vinnuliður er stofnaður og honum er úthlutað á upphaflegan aðila.</span><span class="sxs-lookup"><span data-stu-id="34a7d-107">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="34a7d-108">Þetta þýðir að tilkynning er send á upphaflegan aðila vegna hafnaðs vinnuliðar og aðskilin tilkynning send á notandann sem fær úthlutaðan nýja vinnuliðinn „beiðni um breytingu“.</span><span class="sxs-lookup"><span data-stu-id="34a7d-108">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="34a7d-109">Hver tilkynning er fyrir mismunandi vinnulið, en líkindin geta valdið ruglingi.</span><span class="sxs-lookup"><span data-stu-id="34a7d-109">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="34a7d-110">Við erum að skoða leiðir til að bæta þetta í framtíðarútgáfu.</span><span class="sxs-lookup"><span data-stu-id="34a7d-110">We are looking at ways to improve this in a future release.</span></span>

## <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="34a7d-111">Afhverju eru útflutningar á verkflæðum að mistakast?</span><span class="sxs-lookup"><span data-stu-id="34a7d-111">Why are my workflow exports failing?</span></span>
<span data-ttu-id="34a7d-112">Sem stendur eru takmörk á eiginleikanum fyrir útflutning verkflæðis sem koma í veg fyrir að heiti verkflæða séu lengri en 48 stafir.</span><span class="sxs-lookup"><span data-stu-id="34a7d-112">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="34a7d-113">Að nota heiti sem er lengra en 48 stafir getur leitt til villunnar „Þjónn gat ekki sannvottað beiðnina“ og/eða komið í veg fyrir að skrá verði flutt út án skráargerðar.</span><span class="sxs-lookup"><span data-stu-id="34a7d-113">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="34a7d-114">Eftirfarandi bloggfærsla veitir frekari upplýsingar [Úrræðaleit fyrir útflutning verkflæðis](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="34a7d-114">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a><span data-ttu-id="34a7d-115">Getur sendandi verkflæðis einnig samþykkt verkflæðið?</span><span class="sxs-lookup"><span data-stu-id="34a7d-115">Can the submitter of a workflow also approve the workflow?</span></span>
<span data-ttu-id="34a7d-116">Já, sendandi verkflæðis getur einnig samþykkt verkflæðið ef það er stillt þannig.</span><span class="sxs-lookup"><span data-stu-id="34a7d-116">Yes, a submitter of a workflow can also approve the workflow if it is configured that way.</span></span> <span data-ttu-id="34a7d-117">Til að koma í veg fyrir þessa hegðun skaltu stilla **Færibreytur verkflæðis > Almennar > Samþykktaraðili > Afturkalla heimild innsendingaraðila** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="34a7d-117">To prevent this behavior, set **Workflow parameters > General > Approver > Disallow approval by submitter** to **Yes**.</span></span>

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a><span data-ttu-id="34a7d-118">Get ég bætt við viðvörunum í verkflæði til að veita notendum tilkynningar?</span><span class="sxs-lookup"><span data-stu-id="34a7d-118">Can I add alerts to workflows to provide notifications to users?</span></span>
<span data-ttu-id="34a7d-119">Hér eru nokkrur lykilatriði til að hafa í huga varðandi viðbót viðvarana í verkflæði til að veita tilkynningar:</span><span class="sxs-lookup"><span data-stu-id="34a7d-119">Here are a few key areas to note about adding alerts to workflows to provide notifications:</span></span>
- <span data-ttu-id="34a7d-120">Viðvörun á móti kerfum verkflæðistilkynninga</span><span class="sxs-lookup"><span data-stu-id="34a7d-120">Alerts versus workflow notification mechanisms</span></span>
    - <span data-ttu-id="34a7d-121">Hægt er að setja upp viðvörun fyrir skráarbreytingar.</span><span class="sxs-lookup"><span data-stu-id="34a7d-121">Alerts can be set up for record changes.</span></span> <span data-ttu-id="34a7d-122">Verkflæði breyta skrám, þannig að hægt er að setja upp viðvörun sem tengist skráarskiptum vegna verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="34a7d-122">Workflows change records, so it's possible to set up an alert related to a record change caused by a workflow.</span></span> <span data-ttu-id="34a7d-123">Hins vegar, þar sem verkflæða hafa mismunandi innbyggða tilkynningavalkosti er notkun viðvarana ekki tilvalin.</span><span class="sxs-lookup"><span data-stu-id="34a7d-123">However, because workflows have different built-in notification options, using alerts isn’t ideal.</span></span>
- <span data-ttu-id="34a7d-124">Staðlaðar tilkynningar úr verkflæði</span><span class="sxs-lookup"><span data-stu-id="34a7d-124">Standard notifications from workflows</span></span> 
    - <span data-ttu-id="34a7d-125">Verkflæði hafa innbyggðar tilkynningar í tölvupósti.</span><span class="sxs-lookup"><span data-stu-id="34a7d-125">Workflows have built in email notifications.</span></span> <span data-ttu-id="34a7d-126">Viðskiptavinur getur stillt tilkynningarnar þannig að notendum sé sendur tölvupóstur.</span><span class="sxs-lookup"><span data-stu-id="34a7d-126">A customer can configure the notifications so that the users are sent emails.</span></span> <span data-ttu-id="34a7d-127">Þessar tilkynningar leiða ekki til skilaboða úr aðgerðarmiðstöð fyrir notendur.</span><span class="sxs-lookup"><span data-stu-id="34a7d-127">Those notifications don’t result in Action Center messages for users.</span></span>
    - <span data-ttu-id="34a7d-128">Í framtíðaruppfærslu munum við bæta við skilaboðum aðgerðarmiðstöðvar þannig að notanda sé úthlutað verkflæði.</span><span class="sxs-lookup"><span data-stu-id="34a7d-128">In a future update we will be adding an Action Center message so a user is assigned a workflow work item.</span></span> 
- <span data-ttu-id="34a7d-129">Tilkynningum bætt við verkflæði</span><span class="sxs-lookup"><span data-stu-id="34a7d-129">Adding notifications to workflows</span></span>
    - <span data-ttu-id="34a7d-130">Skilaboð aðgerðarmiðstöðvar geta verið stofnuð fyrir tiltekna notendur, eins og silkaboð stofnuð í verkflæði í X ++.</span><span class="sxs-lookup"><span data-stu-id="34a7d-130">Action Center messages can be created for specific users, such as a message created from a workflow in X++.</span></span>
    - <span data-ttu-id="34a7d-131">[Verkflæði hafa viðskiptatilvik](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) sem viðskiptavinurinn gæti notað til að kveikja á flæði, hafa þær tilkynningar sem þeir leita að.</span><span class="sxs-lookup"><span data-stu-id="34a7d-131">[Workflows have Business Events](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) that the customer could use to trigger Flows have the notifications that they are looking for.</span></span>   

<span data-ttu-id="34a7d-132">Í stuttu máli, ef notandi fær ekki rétta tilkynningu frá aðgerðamiðstöðinni þegar honum er úthlutað verkflæðisliður, þá notar hann [Viðskiptatilvik verkflæðis](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) með Microsoft Flow til að veita viðbótar eða mismunandi tilkynningar.</span><span class="sxs-lookup"><span data-stu-id="34a7d-132">In summary, if a user does not get the proper notification from the Action Center when they are assigned a workflow work item, then leverage [Workflow Business Events](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) with Microsoft Flow to provide additional or different notifications.</span></span>
