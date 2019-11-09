---
title: Haga ráðningarferlum
description: Þessi skrá lýsir hugmyndinni sem ráðningaraðilar geta nota til að rekja skref í ráðningarferli, þar með talið viðleitni til að auglýsa opnar stöður og ráða umsækjendur, rekja upplýsingar um umsækjandann og umsóknina, taka viðtöl við umsækjendur og að velja einn eða fleiri umsækjendur að fylla opnar stöður í fyrirtækinu.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfdc1295e0b82672576acdf8e2756dbb36612f8b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190742"
---
# <a name="manage-recruiting-processes"></a><span data-ttu-id="16259-103">Haga ráðningarferlum</span><span class="sxs-lookup"><span data-stu-id="16259-103">Manage recruiting processes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16259-104">Þetta efnisatriðilýsir hugmyndinni sem ráðningaraðilar geta nota til að rekja skref í ráðningarferli, þar með talið viðleitni til að auglýsa opnar stöður og ráða umsækjendur, rekja upplýsingar um umsækjandann og umsóknina, taka viðtöl við umsækjendur og að velja einn eða fleiri umsækjendur að fylla opnar stöður í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="16259-104">This topic describes a concept that recruiters can use to track the steps in a recruiting process, including efforts to advertise open positions and recruit applicants, tracking applicant and application information, interviewing applicants, and selecting one or more candidates to fill the open positions in your organization.</span></span>

## <a name="overview"></a><span data-ttu-id="16259-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="16259-105">Overview</span></span>

<span data-ttu-id="16259-106">Ráðningarverk hjálpa til við að skipuleggja skref er lokið við að fylla opnar stöður í lögaðila.</span><span class="sxs-lookup"><span data-stu-id="16259-106">Recruitment projects can help you organize the steps you'll complete when filling open positions in a legal entity.</span></span> <span data-ttu-id="16259-107">Umsækjandi er sá einstaklingur sem sækir um starf innan fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="16259-107">An applicant is a person who applies for employment to your enterprise.</span></span> <span data-ttu-id="16259-108">Umsóknin er yfirlýsing umsækjanda um áhuga á að starfa hjá fyrirtækinu og gæti verið bundin ráðningarverki til að sýna áhuga á tiltekinni stöðu.</span><span class="sxs-lookup"><span data-stu-id="16259-108">An application is an applicant's expression of interest in being employed by a company and may be tied to a recruitment project to express interest in a specific opening.</span></span> <span data-ttu-id="16259-109">Stakur umsækjandi getur haft margar umsóknir innan sama lögaðila eða í mörgum fyrirtækjum í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="16259-109">A single applicant may have multiple applications within the same legal entity or across multiple companies in your organization.</span></span>

## <a name="recruitment-projects"></a><span data-ttu-id="16259-110">Ráðningarverk</span><span class="sxs-lookup"><span data-stu-id="16259-110">Recruitment projects</span></span>

<span data-ttu-id="16259-111">Ráðningarverk leyfa ráðningaraðilum að rekja framvindu gegn fyllingu einna eða fleiri opinna staða.</span><span class="sxs-lookup"><span data-stu-id="16259-111">Recruitment projects allow recruiters to track progress against filling one or more open positions.</span></span> <span data-ttu-id="16259-112">Ráðningarverkið auðkennir deild og vinnslu sem eitt eða fleiri stöður eru opin fyrir.</span><span class="sxs-lookup"><span data-stu-id="16259-112">The recruitment project identifies the department and job for which one or more positions are open.</span></span> <span data-ttu-id="16259-113">Ráðningarverk rekja einnig eftirfarandi upplýsingar um opnar stöður:</span><span class="sxs-lookup"><span data-stu-id="16259-113">Recruitment projects also track following information for open positions:</span></span>

- <span data-ttu-id="16259-114">Nákvæmur fjöldi opinna staða</span><span class="sxs-lookup"><span data-stu-id="16259-114">The specific number of open positions</span></span>
- <span data-ttu-id="16259-115">Ráðningarstjóri og annar tengiliður fyrir stöðuna</span><span class="sxs-lookup"><span data-stu-id="16259-115">The hiring manager and an alternative contact for the position</span></span>
- <span data-ttu-id="16259-116">Dagsetningin þegar tillagan var samþykkt.</span><span class="sxs-lookup"><span data-stu-id="16259-116">The date that the requisition was approved</span></span>
- <span data-ttu-id="16259-117">Tímamörk umsóknar</span><span class="sxs-lookup"><span data-stu-id="16259-117">The application deadline</span></span>
- <span data-ttu-id="16259-118">Áætlaður upphafsdagur</span><span class="sxs-lookup"><span data-stu-id="16259-118">The estimated start date</span></span>

<span data-ttu-id="16259-119">Ráðningarverkið inniheldur **Starfsauglýsinguna** sem er notuð í **Sjálfsafgreiðsla starfsmanns** til að auglýsa stöðurnar.</span><span class="sxs-lookup"><span data-stu-id="16259-119">The recruitment project contains the **Job ad** used on the **Employee self service** to advertise the opening.</span></span> <span data-ttu-id="16259-120">Til að birta starfsmönnum stöðurnar verður ráðningarverkið að hafa **Starfsauglýsinguna**, reitinn **Birta í sjálfsafgreiðslu starfsmanns** stilltan á Já, **Tímamörk umsóknar** verður að vera stillt á dagsetningu í framtíðinni, og ráðningarverkið verður að hafa í **staða Verks** byrjað.</span><span class="sxs-lookup"><span data-stu-id="16259-120">To display the opening to employees, the recruitment project must have a **Job ad**, the **Display on employee self service** field must be set to Yes, the **Application deadline** must be set to a future date, and the recruitment project must have a **Project status** of Started.</span></span> <span data-ttu-id="16259-121">Í eftirfarandi töflu er listi yfir möguleg ráðningarverk verkstöðu og lýsingu þeirra.</span><span class="sxs-lookup"><span data-stu-id="16259-121">The following table lists the possible recruitment project statuses and their description.</span></span>

| <span data-ttu-id="16259-122">Staða</span><span class="sxs-lookup"><span data-stu-id="16259-122">Status</span></span>    | <span data-ttu-id="16259-123">Gefur til kynna að...</span><span class="sxs-lookup"><span data-stu-id="16259-123">Indicates that…</span></span>                                                                         |
|-----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16259-124">Raðað</span><span class="sxs-lookup"><span data-stu-id="16259-124">Scheduled</span></span> | <span data-ttu-id="16259-125">Ráðningarvinna er undirbúin.</span><span class="sxs-lookup"><span data-stu-id="16259-125">Recruiting efforts are being prepared.</span></span> <span data-ttu-id="16259-126">Ráðningar hafa ekki enn hafist fyrir þetta verk.</span><span class="sxs-lookup"><span data-stu-id="16259-126">Recruiting has not yet started for this project.</span></span> |
| <span data-ttu-id="16259-127">Hafin</span><span class="sxs-lookup"><span data-stu-id="16259-127">Started</span></span>   | <span data-ttu-id="16259-128">Umsóknir eru nú verið samþykktar fyrir á auglýstar stöður í þessu verki.</span><span class="sxs-lookup"><span data-stu-id="16259-128">Applications are now being accepted for the openings in this project.</span></span>                   |
| <span data-ttu-id="16259-129">Lokið</span><span class="sxs-lookup"><span data-stu-id="16259-129">Finished</span></span>  | <span data-ttu-id="16259-130">Allar auglýstar stöður fyrir þetta verk hafa verið fylltar.</span><span class="sxs-lookup"><span data-stu-id="16259-130">All openings for this project have been filled.</span></span>                                         |
| <span data-ttu-id="16259-131">Hætt við</span><span class="sxs-lookup"><span data-stu-id="16259-131">Canceled</span></span>  | <span data-ttu-id="16259-132">Ráðning hefur verið afturkölluð fyrir þetta verk.</span><span class="sxs-lookup"><span data-stu-id="16259-132">Recruiting has been canceled for this project.</span></span>                                          |

<span data-ttu-id="16259-133">Ráðningaraðilar geta einnig skráð fyrir **Miðla** sem notaðir voru til að auglýsa stöður gegnum ytri miðla, auk þess að rekja **Þróun** gagnvart verki eða umsóknum.</span><span class="sxs-lookup"><span data-stu-id="16259-133">Recruiters can also record the **Media** used to advertise the opening through external outlets as well as track **Developments** against the project or applications.</span></span>

## <a name="applicants"></a><span data-ttu-id="16259-134">Umsækjendur</span><span class="sxs-lookup"><span data-stu-id="16259-134">Applicants</span></span>

<span data-ttu-id="16259-135">Umsækjandi er sá einstaklingur sem sækir um starf í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="16259-135">An applicant is a person who applies for a job in your enterprise.</span></span> <span data-ttu-id="16259-136">Umsækjendur eru samnýttar á milli allra lögaðila í samstæðunni, sem veitir stóran hóp af færu fólki til að leita í.</span><span class="sxs-lookup"><span data-stu-id="16259-136">Applicants are shared among all legal entities in your organization giving you a large pool of talent to search from.</span></span> <span data-ttu-id="16259-137">Hægt er að viðhalda færni, meðmælum, og beiðnum um aðlögun og persónulegum upplýsingum fyrir umsækjendur.</span><span class="sxs-lookup"><span data-stu-id="16259-137">You can maintain competencies, references, accommodation requests, and personal information for applicants.</span></span> <span data-ttu-id="16259-138">Þegar færsla umsækjanda er stofnuð, tengiliðafærslu fyrir umsækjanda er stofnuð í altæku aðsetursbókinni.</span><span class="sxs-lookup"><span data-stu-id="16259-138">When you create an applicant record, a person record for that applicant is created in the global address book.</span></span> <span data-ttu-id="16259-139">Hægt er að nota síðuna **Umsækjandi** til að uppfæra eftirfarandi altækar aðsetursbókarupplýsingar fyrir einstaklinga sem eru umsækjendur:</span><span class="sxs-lookup"><span data-stu-id="16259-139">You can use the **Applicant** page to update the following global address book information for people who are applicants:</span></span>

- <span data-ttu-id="16259-140">Upplýsingar um aðsetur</span><span class="sxs-lookup"><span data-stu-id="16259-140">Address information</span></span>
- <span data-ttu-id="16259-141">Tengslaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="16259-141">Contact information</span></span>
- <span data-ttu-id="16259-142">Auðkennisupplýsingar</span><span class="sxs-lookup"><span data-stu-id="16259-142">Identification information</span></span>
- <span data-ttu-id="16259-143">Upplýsingar um nafn</span><span class="sxs-lookup"><span data-stu-id="16259-143">Name details</span></span>
- <span data-ttu-id="16259-144">Persónulegar upplýsingar</span><span class="sxs-lookup"><span data-stu-id="16259-144">Personal information</span></span>

## <a name="applications"></a><span data-ttu-id="16259-145">Hugbúnaður</span><span class="sxs-lookup"><span data-stu-id="16259-145">Applications</span></span>

<span data-ttu-id="16259-146">Hægt er að skrá upplýsingar úr mótteknum starfsumsóknum í skjámyndinni **Umsókn**.</span><span class="sxs-lookup"><span data-stu-id="16259-146">You can record information from employment applications that you receive in the **Application** page.</span></span> <span data-ttu-id="16259-147">Umsóknin er yfirlýsing umsækjanda um áhuga á auglýstri stöðu í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="16259-147">The application is the applicant's expression of interest in a job opening in your organization.</span></span> <span data-ttu-id="16259-148">Til að stofna umsókn þarf umsækjandinn að vera þegar til sem umsækjandi eða einstaklingur í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="16259-148">To create an application, the applicant must already exist as an applicant or person in your system.</span></span>

<span data-ttu-id="16259-149">Starfsumsóknir sem umsækjendur senda á vefnum eru annaðhvort umbeðnar umsóknir sem voru færðar inn sem svar við starfsauglýsingu eða óumbeðnar umsóknir.</span><span class="sxs-lookup"><span data-stu-id="16259-149">Employment applications submitted by applicants on the web are either solicited applications that were entered in response to a job ad, or are unsolicited applications.</span></span> <span data-ttu-id="16259-150">Umbeðnar umsóknir eru sjálfkrafa tengdar ráðningarverkinu þaðan sem auglýsingin var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="16259-150">Solicited applications are automatically associated with the recruitment project that the job ad was created from.</span></span> <span data-ttu-id="16259-151">Óumbeðnar umsóknir eru tengdar ráðningarverki nu sem tilgreint er á svæðinu **Ráðningarverk** á síðunni **Færibreytur mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="16259-151">Unsolicited applications are associated with the recruitment project that is specified in the **Recruitment** area of the **Human resources parameters** page.</span></span>

### <a name="application-status"></a><span data-ttu-id="16259-152">Staða umsóknar</span><span class="sxs-lookup"><span data-stu-id="16259-152">Application status</span></span>

<span data-ttu-id="16259-153">Staða umsóknar gefur til kynna hvar umsókn er í ráðningarferlinu.</span><span class="sxs-lookup"><span data-stu-id="16259-153">The application status indicates where an application is in the recruitment process.</span></span> <span data-ttu-id="16259-154">Í eftirfarandi töflu er listi yfir mögulegar stöður umsókna og lýsingu þeirra.</span><span class="sxs-lookup"><span data-stu-id="16259-154">The following table lists the possible application statuses and their description.</span></span>

| <span data-ttu-id="16259-155">Staða</span><span class="sxs-lookup"><span data-stu-id="16259-155">Status</span></span>    | <span data-ttu-id="16259-156">Gefur til kynna að...</span><span class="sxs-lookup"><span data-stu-id="16259-156">Indicates that…</span></span>                                                                           |
|-----------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="16259-157">Móttekið</span><span class="sxs-lookup"><span data-stu-id="16259-157">Received</span></span>  | <span data-ttu-id="16259-158">Dagsetningin þegar umsóknin var móttekin.</span><span class="sxs-lookup"><span data-stu-id="16259-158">The application was received.</span></span>                                                             |
| <span data-ttu-id="16259-159">Staðfest</span><span class="sxs-lookup"><span data-stu-id="16259-159">Confirmed</span></span> | <span data-ttu-id="16259-160">Tilkynning er send til umsækjanda til að staðfesta móttöku umsóknarinnar.</span><span class="sxs-lookup"><span data-stu-id="16259-160">A notice can be sent to the applicant to confirm receipt of their application.</span></span>            |
| <span data-ttu-id="16259-161">Viðtal</span><span class="sxs-lookup"><span data-stu-id="16259-161">Interview</span></span> | <span data-ttu-id="16259-162">Hægt er að senda boð um að koma í viðtal til umsækjandans.</span><span class="sxs-lookup"><span data-stu-id="16259-162">An interview invitation can be sent to the applicant.</span></span>                                     |
| <span data-ttu-id="16259-163">Höfnun</span><span class="sxs-lookup"><span data-stu-id="16259-163">Rejection</span></span> | <span data-ttu-id="16259-164">Hægt er að senda höfnunarbréf til umsækjandans.</span><span class="sxs-lookup"><span data-stu-id="16259-164">A rejection letter can be sent to the applicant.</span></span>                                          |
| <span data-ttu-id="16259-165">Hætt við</span><span class="sxs-lookup"><span data-stu-id="16259-165">Canceled</span></span>  | <span data-ttu-id="16259-166">Hægt er að senda staðfestingu um afturköllun til umsækjandans.</span><span class="sxs-lookup"><span data-stu-id="16259-166">A withdrawal confirmation can be sent to the applicant.</span></span> <span data-ttu-id="16259-167">Þessari stöðu er úthlutað handvirkt.</span><span class="sxs-lookup"><span data-stu-id="16259-167">This status is assigned manually.</span></span> |
| <span data-ttu-id="16259-168">Ráðin(n)</span><span class="sxs-lookup"><span data-stu-id="16259-168">Employed</span></span>  | <span data-ttu-id="16259-169">Hægt er að senda atvinnutilboð til umsækjandans.</span><span class="sxs-lookup"><span data-stu-id="16259-169">An employment offer can be sent to the applicant.</span></span>                                         |

### <a name="correspondence-actions"></a><span data-ttu-id="16259-170">Samskiptaaðgerðir</span><span class="sxs-lookup"><span data-stu-id="16259-170">Correspondence actions</span></span>

<span data-ttu-id="16259-171">Samskiptaaðgerð **Umsóknar** ákvarðar sniðmát skjals eða tölvupóstsniðmát sem notað er til að eiga samskipti við umsækjandann sem sendi inn umsóknina.</span><span class="sxs-lookup"><span data-stu-id="16259-171">An **Application's** correspondence action determines the document or e-mail template that you use to communicate with the applicant who submitted the application.</span></span> <span data-ttu-id="16259-172">Hægt er að tengja **Bókamerki umsókna** við samskiptaaðgerðir til að leyfa að gildi séu notuð af síðunum Umsókn, Umsækjandi, Viðtal og Ráðningarverk í samskiptum við umsækjendur.</span><span class="sxs-lookup"><span data-stu-id="16259-172">You can associate **Application bookmarks** with correspondence actions to allow you to use values from the Application, Applicant, Interview, and Recruitment project pages in your communications with applicants.</span></span> <span data-ttu-id="16259-173">Hægt er að stofna **Tölvupóstsniðmát umsókna** fyrir samskiptaaðgerðir til að senda skjótan tölvupóst til umsækjenda sem hafa umsókn með tiltekna samsetningu á stöðu og samskiptaaðgerð.</span><span class="sxs-lookup"><span data-stu-id="16259-173">**Application e-mail templates** can be created for the correspondence actions to quickly send e-mails to applicants who have an application with a certain status and correspondence action combination.</span></span> <span data-ttu-id="16259-174">Til dæmis gætirðu sent staðfestingartölvupóst til allra umsækjenda með **stöðuna** Móttekið **samskiptaaðgerðina** Móttekið.</span><span class="sxs-lookup"><span data-stu-id="16259-174">For example, you may send a Confirmation e-mail to all Applications with a **Status** of Received and a **Correspondence action** of Received.</span></span> <span data-ttu-id="16259-175">Þegar tölvupósturinn hefur verið sendur þarf að uppfæra sjálfkrafa stöðu umsókna.</span><span class="sxs-lookup"><span data-stu-id="16259-175">After sending the e-mail, you have the option to automatically update the status of the applications.</span></span>

## <a name="application-routing"></a><span data-ttu-id="16259-176">Leiðir umsókna</span><span class="sxs-lookup"><span data-stu-id="16259-176">Application routing</span></span>

<span data-ttu-id="16259-177">Ef nokkrir starfsmenn þurfa að skoða umsóknina er hægt að nota síðuna **Leiðir umsókna** til að stofna dreifingarlista starfsmanna svo að hægt sé að stjórna ferlinu.</span><span class="sxs-lookup"><span data-stu-id="16259-177">If an application must be reviewed by several workers, you can use the **Application routing** page to create a worker circulation list in order to manage the process.</span></span>

## <a name="interviews"></a><span data-ttu-id="16259-178">Viðtöl</span><span class="sxs-lookup"><span data-stu-id="16259-178">Interviews</span></span>

<span data-ttu-id="16259-179">**Viðtöl við umsækjendur** má áætla af síðunni **Umsóknir**.</span><span class="sxs-lookup"><span data-stu-id="16259-179">**Applicant interviews** can be scheduled from the **Applications** page.</span></span> <span data-ttu-id="16259-180">Nota skal hnappinn **Senda upplýsingar um fund** til að senda dagatalsskrár með upplýsingum um áætlað viðtal við umsækjanda og tengslaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="16259-180">Use the **Send meeting information** button to send a calendar file with the interview schedule information to the applicant and interviewer.</span></span>

## <a name="skill-mapping"></a><span data-ttu-id="16259-181">Hæfnisskrá</span><span class="sxs-lookup"><span data-stu-id="16259-181">Skill mapping</span></span>

<span data-ttu-id="16259-182">**Hæfnisskrá** og **Forstillingar hæfniskráningar** er hægt að nota til að auðkenna umsækjendur sem kunna að vera hæfir í stöðuna.</span><span class="sxs-lookup"><span data-stu-id="16259-182">**Skill mapping** and **Skill mapping profiles** can be used to identify candidates who may be a good fit for an opening.</span></span>

## <a name="hiring-applicants"></a><span data-ttu-id="16259-183">Ráðnir umsækjendur</span><span class="sxs-lookup"><span data-stu-id="16259-183">Hiring applicants</span></span>

<span data-ttu-id="16259-184">Nota skal **Umsóknir** síðu til að ráða umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="16259-184">Use the **Applications** page to hire an applicant.</span></span> <span data-ttu-id="16259-185">Þegar umsækjandi er ráðinn mun umsóknarfærslan fá stöðuna **Ráðinn** og einstaklingsfærsla umsækjandans í altækri aðsetursbók er tengd við nýja skrá starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="16259-185">When you hire an applicant, the application record will have a status of **Employed** and the applicant's global address book person record is associated with the new worker record.</span></span> <span data-ttu-id="16259-186">Breytingar á upplýsingum altækrar aðsetursbókar fyrir nýja færslu starfsmanns eru einnig birtar í færslu umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="16259-186">Modifications to the global address book information for the new worker record are also displayed in the applicant record.</span></span> <span data-ttu-id="16259-187">Þetta getur minnkað gagnainnfærslu ef nýr starfsmaður sækir aldrei um annað starf innan fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="16259-187">This can help reduce data entry if the new worker ever applies for a different job within your enterprise.</span></span> <span data-ttu-id="16259-188">Til að ráða starfsmanni í nýja stöðu, smellið á **Breyta stöðu** í fellilistanum **Umsóknastaða** til að hefja flutningsferlið.</span><span class="sxs-lookup"><span data-stu-id="16259-188">To hire an existing worker into a new position, click **Change position** in the **Application status** drop down to initiate the transfer process.</span></span>