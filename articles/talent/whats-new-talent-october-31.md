---
title: Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (31. október 2018)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d6942f8e4dc86f18a081b347df0567b1358a87ab
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/19/2019
ms.locfileid: "858791"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-31-2018"></a><span data-ttu-id="8fc15-103">Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (31. október 2018)</span><span class="sxs-lookup"><span data-stu-id="8fc15-103">What's new or changed in Dynamics 365 for Talent Core HR (October 31, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8fc15-104">**Smíði 8.1.2031**</span><span class="sxs-lookup"><span data-stu-id="8fc15-104">**Build 8.1.2031**</span></span>

<span data-ttu-id="8fc15-105">Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Core HR.</span><span class="sxs-lookup"><span data-stu-id="8fc15-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="create-links-from-talent-to-finance-and-operations"></a><span data-ttu-id="8fc15-106">Búa til tengla frá Talent að Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8fc15-106">Create links from Talent to Finance and Operations</span></span>
<span data-ttu-id="8fc15-107">Þessi nýja leiðsöguvirkni gerir þér kleift að tengja frá Talent til Finance and Operations, sem gefur þér beina leiðsögn í síður Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8fc15-107">This new navigation functionality allows you to link from Talent to Finance and Operations, giving you direct navigation into Finance and Operations pages.</span></span> <span data-ttu-id="8fc15-108">Þegar tenglar eru grunnstilltir er hægt að tilgreina heiti og hóp tengilsins, þar sem tengilinn ætti að liggja yfir í Talent og marksíðuna sem á að opnast í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8fc15-108">When links are configured, you can specify the name and group of the link, where the link should surface in Talent, and the target page to be opened within Finance and Operations.</span></span>

#### <a name="coming-soon"></a><span data-ttu-id="8fc15-109">Væntanlegt</span><span class="sxs-lookup"><span data-stu-id="8fc15-109">Coming soon</span></span>
<span data-ttu-id="8fc15-110">Svæðasamhengi verður bætt við í framtíðinni til að leyfa beina leiðsögn í samsvarandi skrár í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8fc15-110">Field context will be added in the future to allow for direct navigation to corresponding records in Finance and Operations.</span></span> <span data-ttu-id="8fc15-111">Til dæmis getur þú notað **Tengja svæði** til að veita samhengi til að fara beint á tiltekins starfsmanns eða stöðu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8fc15-111">For example, you can use **Link to field** to provide the context to navigate directly to a specific employee or position in Finance and Operations.</span></span>

### <a name="configure-target-systems"></a><span data-ttu-id="8fc15-112">Grunnstilla markkerfi</span><span class="sxs-lookup"><span data-stu-id="8fc15-112">Configure target systems</span></span>

<span data-ttu-id="8fc15-113">Í Talent geta kerfisstjórar skilgreint tengla sem birtast á vinnusvæði kerfisstjórnunar.</span><span class="sxs-lookup"><span data-stu-id="8fc15-113">In Talent, system administrators can define links that will be surfaced through the System Administration workspace.</span></span> <span data-ttu-id="8fc15-114">Hluti af grunnstillingunni er Finance and Operations umhverfið sem þú vilt fara til sem „mark“ tengilsins.</span><span class="sxs-lookup"><span data-stu-id="8fc15-114">Part of the configuration is the Finance and Operations environments that you would like to navigate to as the "target" of the link.</span></span> <span data-ttu-id="8fc15-115">Þú gerir þetta með því að gefa markkerfinu nafn og gefa vefslóðina á umhverfi Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8fc15-115">You do this by giving the target system a name and providing the URL of the Finance and Operations environment.</span></span> <span data-ttu-id="8fc15-116">Hér er dæmi um vefslóð Finance and Operations sem þú myndir veita: https://devax00124aos.cloud.test.dynamics.com/.</span><span class="sxs-lookup"><span data-stu-id="8fc15-116">Here is an example of a Finance and Operations URL that you would provide: https://devax00124aos.cloud.test.dynamics.com/.</span></span> <span data-ttu-id="8fc15-117">Eftir að þú hefur stillt markkerfi þín, getur þú skilgreint tenglana þína.</span><span class="sxs-lookup"><span data-stu-id="8fc15-117">After you have configured your target systems,  you can define your links.</span></span>

### <a name="configure-links"></a><span data-ttu-id="8fc15-118">Samskipa tengla</span><span class="sxs-lookup"><span data-stu-id="8fc15-118">Configure links</span></span>

<span data-ttu-id="8fc15-119">Hver tengill sem er búin til mun hafa eftirfarandi upplýsingar skilgreind.</span><span class="sxs-lookup"><span data-stu-id="8fc15-119">Each link that is created will have the following information defined.</span></span>

- <span data-ttu-id="8fc15-120">Tengill - Heiti tengilsins, aðeins notað til auðkenningar.</span><span class="sxs-lookup"><span data-stu-id="8fc15-120">Link - Name of the link, used for identification only.</span></span>

- <span data-ttu-id="8fc15-121">Virkja þennan tengil - Stilltu á **Já** ef þú vilt birta tengilinn til notenda Talent.</span><span class="sxs-lookup"><span data-stu-id="8fc15-121">Enable this Link - Set to **Yes** if you want to display the link to users of Talent.</span></span>

- <span data-ttu-id="8fc15-122">Sýna nafn - Skilgreina nafnið sem mun birtast sem tengill við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8fc15-122">Display name - Define the name that will appear as a link to Finance and Operations.</span></span> <span data-ttu-id="8fc15-123">Þessi gögn eru ekki þýdd eins og stendur.</span><span class="sxs-lookup"><span data-stu-id="8fc15-123">This data is currently is not translated.</span></span>

- <span data-ttu-id="8fc15-124">Birta tengil á skjámynd - Veldu hvaða síðu þú vilt birta tengilinn á.</span><span class="sxs-lookup"><span data-stu-id="8fc15-124">Surface link on form - Choose which page you would like to display the link on.</span></span>

- <span data-ttu-id="8fc15-125">Hópur - Hópa er ekki krafist, en ef þú vilt skipuleggja tengla þína með hópum skaltu velja núverandi hóp eða búa til nýjan með því að nota **Hópur** reitinn.</span><span class="sxs-lookup"><span data-stu-id="8fc15-125">Group - Groups are not required, but if you want to organize your links using groups, select an existing group or create a new one using the **Group** field.</span></span>

- <span data-ttu-id="8fc15-126">Markkerfi - Veldu markkerfi sem var búið til með því að nota **Stilla markkkerfi** valkost.</span><span class="sxs-lookup"><span data-stu-id="8fc15-126">Target system - Select the target system that was created using the **Configure target system** option.</span></span> <span data-ttu-id="8fc15-127">Þetta verður umhverfi Finance and Operations sem verður notað þegar vafrað er með því að nota tengilinn.</span><span class="sxs-lookup"><span data-stu-id="8fc15-127">This will be the Finance and Operations environment that will be used when navigating by using the link.</span></span>

- <span data-ttu-id="8fc15-128">Notaðu núverandi fyrirtæki notanda - Veldu **Já** ef þú vilt nota samhengi núverandi fyrirtækis notandans þegar þú vafrar í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8fc15-128">Use user's current Company - Select **Yes** if you would like to use the User's current company context when navigating to Finance and Operations.</span></span> <span data-ttu-id="8fc15-129">Ef **Nei** er valið geturðu valið fyrirtækið sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="8fc15-129">If **No** is selected, then you can select the company that should be used.</span></span>

- <span data-ttu-id="8fc15-130">Markvalmyndaratriði - Sláðu inn valmyndaratriðið úr Finance and Operations sem tengilinn ætti að nota þegar þú vafrar.</span><span class="sxs-lookup"><span data-stu-id="8fc15-130">Target menu item - Enter the menu item from Finance and Operation that the link should use when navigating.</span></span> <span data-ttu-id="8fc15-131">Valmyndaratriði sem þú getur farið beint á til eru tiltæk.</span><span class="sxs-lookup"><span data-stu-id="8fc15-131">Menu items that you can directly navigate to are available.</span></span> <span data-ttu-id="8fc15-132">Til að finna valmyndaratriðið sem þarf, opnaðu Finance and Operations og opnaðu síðuna sem er mark leiðsagnarinnar.</span><span class="sxs-lookup"><span data-stu-id="8fc15-132">To find the menu item required, open Finance and Operations and open the page that is the target of the navigation.</span></span> <span data-ttu-id="8fc15-133">Afritaðu valmyndaratriðið úr vefslóðinni.</span><span class="sxs-lookup"><span data-stu-id="8fc15-133">Copy the menu item from the URL.</span></span> <span data-ttu-id="8fc15-134">Til dæmis, ef þú vilt að tengilinn fari með þig á starfsmannalistann í Finance and Operations skaltu slá inn gildið sem birtist eftir "& mi" í vefslóðinni.</span><span class="sxs-lookup"><span data-stu-id="8fc15-134">For example, if you want the link to take you to the employee list in Finance and Operations, enter the value that appears after the "&mi" in the URL.</span></span> <span data-ttu-id="8fc15-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="8fc15-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span></span> <span data-ttu-id="8fc15-136">Valmyndaratriðið til að vafra um listasíðu starfsmannsins í þessu dæmi er: HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="8fc15-136">The menu item to navigate to the employee list page in this example is: HcmWorkerListPage_Employees.</span></span>

- <span data-ttu-id="8fc15-137">Tengill við gagnaveitu - Veldu veitu gagnanna sem tengilinn vísar til.</span><span class="sxs-lookup"><span data-stu-id="8fc15-137">Link to data source - Select the source of data that the link is referencing.</span></span> <span data-ttu-id="8fc15-138">Algengustu veitur eins og **Starfskraftur** og **Staða** eru tiltækar.</span><span class="sxs-lookup"><span data-stu-id="8fc15-138">The most common sources like **Worker** and **Position** are available.</span></span>

- <span data-ttu-id="8fc15-139">Tengill í svæði - (væntanlegt á næstunni) Val á þessu svæði leyfir að fara beint frá einni færslu Talent í staka færslu í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8fc15-139">Link to field - (Coming soon) This field selection will allow for direct navigation from a single record in Talent to a single record in Finance and Operations.</span></span>

### <a name="access-to-links"></a><span data-ttu-id="8fc15-140">Aðgangur að tenglum</span><span class="sxs-lookup"><span data-stu-id="8fc15-140">Access to links</span></span>

<span data-ttu-id="8fc15-141">Kerfisstjórar munu sjá nýstofnaða tengla á skilgreindum síðum, jafnvel þótt **Virkja þennan tengil** valkost sé stillt á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="8fc15-141">System administrators will see the newly created links on the defined pages even if the **Enable this link** option is set to **No**.</span></span> <span data-ttu-id="8fc15-142">Þetta er hægt að nota til að prófa tengla áður en þau eru flutt til annarra starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="8fc15-142">This can be used for testing links prior to surfacing them to other employees.</span></span> <span data-ttu-id="8fc15-143">Öll önnur hlutverk sjá eingöngu grunnstillta tengla eftir að **Virkja þennan tengil** valkostur er stilltur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="8fc15-143">All other roles will only see the configured links after the **Enable this link** option is set to **Yes**.</span></span> <span data-ttu-id="8fc15-144">Starfsmenn sem hafa aðgang að síðum þar sem tenglarnir birtast munu hafa aðgang að tenglum.</span><span class="sxs-lookup"><span data-stu-id="8fc15-144">Employees who have access to the pages in which the links are surfaced will have access to the links.</span></span>

<span data-ttu-id="8fc15-145">Notendur geta einnig haft öryggisréttindi innan Finance and Operations sem eru skilgreindar til að fá aðgang að síðum Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8fc15-145">Users can also have security rights within Finance and Operations defined to access the pages in Finance and Operations.</span></span> <span data-ttu-id="8fc15-146">Ef það gerist ekki birtist öryggissvargluggi þegar tengilinn er notaður.</span><span class="sxs-lookup"><span data-stu-id="8fc15-146">If they don't, a security dialog box will be displayed when using the link.</span></span>


## <a name="other-changesfixes"></a><span data-ttu-id="8fc15-147">Aðrar breytingar/lagfæringar</span><span class="sxs-lookup"><span data-stu-id="8fc15-147">Other changes/fixes</span></span>

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a><span data-ttu-id="8fc15-148">Ekki er hægt að úthluta stöðum með framtíðardagsetningu til nýrrar starfsmanns</span><span class="sxs-lookup"><span data-stu-id="8fc15-148">Positions with a future start date cannot be assigned to a new employee</span></span>

<span data-ttu-id="8fc15-149">Breytingar hafa verið gerðar til að heimila úthlutanir á framtíðardagsettum stöðum til starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="8fc15-149">Changes have been made to allow employee assignments to future-dated positions.</span></span> <span data-ttu-id="8fc15-150">Stöður sem hafa upphafsdagana í framtíðinni er hægt að velja og úthlutun til starfsmanns verður gerður þegar vinnsla er vistuð eða lokið (ef vinnuflæði er virkt).</span><span class="sxs-lookup"><span data-stu-id="8fc15-150">Positions that have start dates in the future can be selected and the employee assignment will be made upon save or completion of the workflow (if the workflow is enabled).</span></span>

### <a name="new-employee-cannot-be-assigned-existing-position"></a><span data-ttu-id="8fc15-151">Nýjum starfsmanni getur ekki verið úthlutað núverandi stöðu</span><span class="sxs-lookup"><span data-stu-id="8fc15-151">New employee cannot be assigned existing position</span></span>

<span data-ttu-id="8fc15-152">Breytingar hafa verið gerðar þannig að ný starfsmannaverkefni geti nú verið úthlutað núverandi stöðu.</span><span class="sxs-lookup"><span data-stu-id="8fc15-152">Changes have been made so new employee assignment can now be assigned to existing positions.</span></span>

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a><span data-ttu-id="8fc15-153">Starfsaldursdagsetning/Staðsetning skrifstofu hverfa þegar upphafsdagur atvinnu er í fortíðinni og skráin er vistuð</span><span class="sxs-lookup"><span data-stu-id="8fc15-153">Seniority date/Office location disappears when the employment start date is in the past and the record is saved</span></span>

<span data-ttu-id="8fc15-154">Breytingar hafa verið gerðar til að leiðrétta sýnileika **Starfsaldursdagsetningar** og **Staðsetningar skrifstofu** þegar breytingar eru gerðar á fyrri starfsmönnum.</span><span class="sxs-lookup"><span data-stu-id="8fc15-154">Changes have been made to correct the visibilty of the **Senority date** and **Office location** when saving changes for past employees.</span></span>

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a><span data-ttu-id="8fc15-155">Ekki er hægt að slá inn gögn fyrir framtíðardagsetta atvinnu á starfsmannasíðunni</span><span class="sxs-lookup"><span data-stu-id="8fc15-155">Can't enter data for future-dated employments on the worker page</span></span>

<span data-ttu-id="8fc15-156">Atvinnugögn fyrir framtíðardagsett fyrirtæki hefur verið gerður óvirkur á aðalstarfsmannasíðunni.</span><span class="sxs-lookup"><span data-stu-id="8fc15-156">Employment data for future-dated employments has been disabled on the main worker page.</span></span> <span data-ttu-id="8fc15-157">Atvinnugögn er hægt að slá inn í gegnum **Stjórnun dagsetninga** síðurnar.</span><span class="sxs-lookup"><span data-stu-id="8fc15-157">Employment data can be entered through the **Date Manager** pages.</span></span> <span data-ttu-id="8fc15-158">Breytingar verða gerðar til viðbótar í útgáfum í framtíðinni til að hægt sé að slá inn atvinnugögn beint inn í verkflæðisferlinu.</span><span class="sxs-lookup"><span data-stu-id="8fc15-158">Additional changes will be made in future releases to enable entering employment data directly during the workflow process.</span></span>

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a><span data-ttu-id="8fc15-159">Bætti ValidFrom og ValidTo við HcmPersonalContactPersonEntity</span><span class="sxs-lookup"><span data-stu-id="8fc15-159">Add ValidFrom and ValidTo to HcmPersonalContactPersonEntity</span></span>

<span data-ttu-id="8fc15-160">Data Management Framework (DMF) einingin HcmPersonalContactPersonEntity hefur verið uppfærð til að innihalda „gildir frá“ og „gildir til“ dagsetningar til virkja tilteknar samþættingaratburðarrásir fríðinda.</span><span class="sxs-lookup"><span data-stu-id="8fc15-160">The Data Management Framework (DMF) entity HcmPersonalContactPersonEntity has been updated to include "valid from" and "valid to" dates to enable certain benefit integration scenarios.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="8fc15-161">Þekkt vandamál</span><span class="sxs-lookup"><span data-stu-id="8fc15-161">Known issue</span></span>
- <span data-ttu-id="8fc15-162">**Vandamál**: Þegar nýtt viðhengi er bætt við starfsmann eru hnapparnir **Nýtt** og **Breyta** skyggðir.</span><span class="sxs-lookup"><span data-stu-id="8fc15-162">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="8fc15-163">**Hjáleið:** Áður en þú opnar viðhengissíðu skaltu ganga úr skugga um að FactBoxes á síðunni **Starfsmenn** séu lokaðir.</span><span class="sxs-lookup"><span data-stu-id="8fc15-163">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="8fc15-164">Ef upplýsingareitirnir eru lokaðir þegar síðan **Starfskraftar** er hlaðið inn verða viðhengishnapparnir gerðir virkir.</span><span class="sxs-lookup"><span data-stu-id="8fc15-164">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="8fc15-165">(Þetta vandamál verður lagað í næstu verkvangsuppfærslu.)</span><span class="sxs-lookup"><span data-stu-id="8fc15-165">(This issue will be fixed in the next platform update.)</span></span>
