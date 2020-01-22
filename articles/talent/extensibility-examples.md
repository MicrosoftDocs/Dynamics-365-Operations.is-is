---
title: Stækka Talent með Power Apps og Power Automate
description: Þetta efnisatriði lýsir sumum dæmum um atburðarás stækkunarhæfni fyrir Microsoft Dynamics 365 Talent sem notar Microsoft Power Apps og Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 6c8a583a93c2ceb70d8c3b0e0047e2bf2047b56d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898318"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="469ef-103">Stækka Talent með Power Apps og Power Automate</span><span class="sxs-lookup"><span data-stu-id="469ef-103">Extend Talent with Power Apps and Power Automate</span></span>

<span data-ttu-id="469ef-104">Þetta efnisatriði lýsir sumum dæmum um atburðarás stækkunarhæfni fyrir Microsoft Dynamics 365 Talent sem notar Microsoft Power Apps og Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="469ef-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="469ef-105">Hægt er að flytja lausnapakkann sem tengist hverju dæmi inn í Power Apps-umhverfið.</span><span class="sxs-lookup"><span data-stu-id="469ef-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="469ef-106">Síðan er hægt að nota pakkana annaðhvort sem leiðarvísi eða sem upphafspunkta til að innleiða atburðarásir sem eiga við um fyrirtækið þitt.</span><span class="sxs-lookup"><span data-stu-id="469ef-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="469ef-107">Ef þú vilt nota sniðmátin og forritið sem lýst er í þessu efnisatriði „eins og það er“, skaltu vera viss um að prófa þau til að ganga úr skugga um þau nái utan um allar atburðarásirnar sem tengjast innleiðingunni þinni.</span><span class="sxs-lookup"><span data-stu-id="469ef-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="469ef-108">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="469ef-108">Prerequisites</span></span>

- <span data-ttu-id="469ef-109">Til að flytja inn pakka verða notendur að hafa heimildina **Umhverfishönnuður**.</span><span class="sxs-lookup"><span data-stu-id="469ef-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="469ef-110">Til að flytja forrit út eða inn verða notendur að hafa Power Apps Plan 2 leyfi eða Power Apps Plan 2 prufuleyfi.</span><span class="sxs-lookup"><span data-stu-id="469ef-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="469ef-111">Power Automate - Skjámynd Connect</span><span class="sxs-lookup"><span data-stu-id="469ef-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="469ef-112">Sniðmátið **Power Automate - Skjámynd Connect** er hægt að nota til að lesa gögn úr Microsoft Forms og vista þau í einingunni Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="469ef-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="469ef-113">Þetta sniðmát er hægt að framlengja þannig að hægt sé að nota það í öðrum atburðarásum.</span><span class="sxs-lookup"><span data-stu-id="469ef-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="469ef-114">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="469ef-114">Here are some examples:</span></span>

- <span data-ttu-id="469ef-115">Sækja mat á umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="469ef-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="469ef-116">Sækja niðurstöður úr spurningalistum námskeiðs.</span><span class="sxs-lookup"><span data-stu-id="469ef-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="469ef-117">Taka saman safn af viðtalsspurningum fyrir mannauðsstjóra.</span><span class="sxs-lookup"><span data-stu-id="469ef-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="469ef-118">Sækja mat umsækjanda á viðtalsferlinu</span><span class="sxs-lookup"><span data-stu-id="469ef-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="469ef-119">Í Microsoft Dynamics 365: Attract, skjámyndir geta birst í umsækjendagátt og umsækjendur geta fyllt út upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="469ef-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="469ef-120">Einnig er hægt að fella inn skjámyndir sem verkþætti í starfssniðmáti.</span><span class="sxs-lookup"><span data-stu-id="469ef-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="469ef-121">Þegar umsækjandi sendir inn eyðublað, sækir Microsoft Power Automate innsent eyðublaðið, les gögnin og geymir þau í Common Data Service-einingunni.</span><span class="sxs-lookup"><span data-stu-id="469ef-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="469ef-122">Til að sækja sniðmátið **Power Automate - Skjámynd Connect** og sérsniðna skipulagseiningu skal fara í [Power Automate - Skjámynd Connect](https://go.microsoft.com/fwlink/?linkid=2081988) í Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="469ef-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-power-apps"></a><span data-ttu-id="469ef-123">Hefja og draga út færibreytur sem sendar eru í Power Apps</span><span class="sxs-lookup"><span data-stu-id="469ef-123">Initiate and Extract Parameters Passed to Power Apps</span></span>

<span data-ttu-id="469ef-124">Sniðmátið **Hefja og draga út færibreytur sem sendar eru til Power Apps** er hægt að nota sem upphafspunkt fyrir allar atburðarásir Power Apps sem miðast við Attract.</span><span class="sxs-lookup"><span data-stu-id="469ef-124">The **Initiate and Extract Parameters Passed to Power Apps** template can be used as a starting point for any Power Apps scenario that is specific to Attract.</span></span> <span data-ttu-id="469ef-125">Það inniheldur allar sjálfgefnu færibreyturnar sem sendar til Attract, t.d. **Starfsumsókn**, **Auðkenni umsækjanda** og **Auðkenni starfs**.</span><span class="sxs-lookup"><span data-stu-id="469ef-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="469ef-126">Hægt er að nota þetta sniðmát til að sækja skjámynd fyrir mat á umsækjanda svo að ráðningarstjóri geti skoðað matið sem umsækjandi fyllti út.</span><span class="sxs-lookup"><span data-stu-id="469ef-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="469ef-127">Forrit sem eru búin til með því að nota Power Apps geta verið felld inn í starfssniðmátið í Attract.</span><span class="sxs-lookup"><span data-stu-id="469ef-127">Apps that are created by using Power Apps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="469ef-128">Til að hlaða niður sniðmátinu **Hefja og draga út færibreytur sem sendar eru í Power Apps** og sérsniðna skipulagseiningu skal fara í [Hefja og draga út færibreytur sem sendar eru í Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) í Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="469ef-128">To download the **Initiate and Extract Parameters Passed to Power Apps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="469ef-129">Samþætting með Office 365</span><span class="sxs-lookup"><span data-stu-id="469ef-129">Integration with Office 365</span></span>

<span data-ttu-id="469ef-130">Forritið **Samþætting við Office 365** er hægt að nota til að draga út upplýsingar um hóp fyrir innskráða notendur úr Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="469ef-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="469ef-131">Það vísar í starfskrafta í Talent til að draga út upplýsingar um inn- og útstimplun og færslur undantekninga.</span><span class="sxs-lookup"><span data-stu-id="469ef-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="469ef-132">Upplýsingar um inn- og útstimplun eru geymdar í sérsniðnum Common Data Service-einingum.</span><span class="sxs-lookup"><span data-stu-id="469ef-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="469ef-133">Gert er ráð fyrir að þessar upplýsingar séu fylltar inn úr kerfum þriðja aðila í gegnum samþættingu.</span><span class="sxs-lookup"><span data-stu-id="469ef-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="469ef-134">Þetta forrit er hægt að stækka þannig að hægt sé að nota það í öðrum atburðarásum.</span><span class="sxs-lookup"><span data-stu-id="469ef-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="469ef-135">Til dæmis er hægt að nota það til að sýna upplýsingar um frí hóps, viðburði dagatals og alla viðburði sem tengjast hópnum.</span><span class="sxs-lookup"><span data-stu-id="469ef-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="469ef-136">Til að hlaða niður forritinu **Samþætting við Office 365** og sérsniðnu skipulagseininguna skal fara í [Samþætting við Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) í Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="469ef-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--email-notification"></a><span data-ttu-id="469ef-137">Power Automate – Tölvupósttilkynning</span><span class="sxs-lookup"><span data-stu-id="469ef-137">Power Automate – Email Notification</span></span>

<span data-ttu-id="469ef-138">Sniðmátið **Power Automate - Tilkynning í tölvupósti** er hægt að nota í atburðarásum tölvupóststilkynningar.</span><span class="sxs-lookup"><span data-stu-id="469ef-138">The **Power Automate – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="469ef-139">Hægt er að nota það til að ræsa tilkynningapósta til umsækjenda sem ráðningarhópurinn hafnar einhvern tímann á stigi ráðningarferlis.</span><span class="sxs-lookup"><span data-stu-id="469ef-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="469ef-140">Hægt er að stækka sniðmátið til að fylgjast með breytingum á stigi umsækjanda í gegnum ráðningarferlið, og til að senda tilkynningapósta á ráðningarhóp og umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="469ef-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="469ef-141">Almennt, fyrir einingar sem eru geymdar í Common Data Service, er hægt að setja upp flæði til að senda tilkynningar á viðburðum sem eiga sér stað í Core HR, Attract eða Onboard.</span><span class="sxs-lookup"><span data-stu-id="469ef-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Onboard.</span></span>

<span data-ttu-id="469ef-142">Til að hlaða niður sniðmátinu **Power Automate - Tilkynning í tölvupósti** skal fara í [Power Automate - Tilkynning í tölvupósti](https://go.microsoft.com/fwlink/?linkid=2082103) í Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="469ef-142">To download the **Power Automate – Email Notification** template, go to [Power Automate – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="469ef-143">Power Automate - SQL Connect og framkvæmd</span><span class="sxs-lookup"><span data-stu-id="469ef-143">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="469ef-144">Sniðmátið **Power Automate - SQL Connect og framkvæmd** tengist við Microsoft SQL Server og virkjar keyrslu á SQL-fyrirspurnum.</span><span class="sxs-lookup"><span data-stu-id="469ef-144">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="469ef-145">Þótt þetta sniðmát sé hannað til að lesa og uppfæra SQL-töflur, er hægt að stækka það til að nota við aðrar kringumstæður.</span><span class="sxs-lookup"><span data-stu-id="469ef-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="469ef-146">Til dæmis er hægt að nota það til að fylla út millistigsvistunartöflu í Common Data Service með skrám úr SQL-þjóni, og til að gera reglubundna samstillingu á millistigsvistunartöflu með því að nota stigvaxandi færslu úr SQL-þjóni.</span><span class="sxs-lookup"><span data-stu-id="469ef-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="469ef-147">Til að hlaða niður sniðmátinu **Power Automate - SQL Connect og framkvæmd** skal fara í [Power Automate - SQL Connect og framkvæmd](https://go.microsoft.com/fwlink/?linkid=2081789) í Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="469ef-147">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="469ef-148">Power Automate – SharePoint samþætting</span><span class="sxs-lookup"><span data-stu-id="469ef-148">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="469ef-149">Hægt er að nota sniðmátið **Power Automate – SharePoint samþætting** til að lesa gögn úr Microsoft SharePoint-lista, bera listann saman við reitagildi fyrir allar Common Data Service-einingar og senda niðurstöður samanburðar sem tilkynningapóst.</span><span class="sxs-lookup"><span data-stu-id="469ef-149">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="469ef-150">Fyrirtæki gæti verið með einhverja hæfni sem þarf nauðsynlega að uppfylla.</span><span class="sxs-lookup"><span data-stu-id="469ef-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="469ef-151">Þessa hæfni er hægt að geyma í SharePoint sem SharePoint-lista.</span><span class="sxs-lookup"><span data-stu-id="469ef-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="469ef-152">Þegar umsækjandi sækir um eitthvað starf þar sem ákveðin hæfni er tekin fram er tilkynningapóstur sendur ef góð samsvörun er milli hæfni umsækjanda og hæfninnar sem geymd er í SharePoint.</span><span class="sxs-lookup"><span data-stu-id="469ef-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="469ef-153">Þannig er fyllt hraðar upp í stöður sem þarf nauðsynlega að ráða í, því að tilkynningarnar hjálpa ráðningaraðilum að ná til og endurráða umsækjendur innan fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="469ef-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="469ef-154">Hægt er að stækka þetta sniðmát svo nota megi það fyrir atburðarás sem hefur með SharePoint-samþættingu að gera.</span><span class="sxs-lookup"><span data-stu-id="469ef-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="469ef-155">Til að hlaða niður sniðmátinu **Power Automate - SharePoint samþætting** skal fara í [Power Automate - SharePoint samþætting](https://go.microsoft.com/fwlink/?linkid=2082109) í Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="469ef-155">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="469ef-156">Tilvísunforrit</span><span class="sxs-lookup"><span data-stu-id="469ef-156">Referral App</span></span>
<span data-ttu-id="469ef-157">Hægt er að nota tilvísunarforritið til að bæta við umbjóðendum í sameiginlegt hæfileikasafn.</span><span class="sxs-lookup"><span data-stu-id="469ef-157">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="469ef-158">Tilvísandi getur fært inn **Fornafn**, **Eftirnafn**, **Netfang** og **Slóð í LinkedIn** við framlagningu umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="469ef-158">The referrer can enter **Firstname**, **Lastname**, **Email**, and **Linkedln URL** when submitting a candidate.</span></span> <span data-ttu-id="469ef-159">Lýsigögn umsækjandans eru síðan fyllt út með upplýsingum tilvísunaraðila.</span><span class="sxs-lookup"><span data-stu-id="469ef-159">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="469ef-160">Hægt er að fella þetta forrit inn í starfsmannaþjónustuna (ESS) til að senda tilvísanir, eða nota það sem tengil á fyrirtækjagáttina og keyrt sem sjálfstætt forrit.</span><span class="sxs-lookup"><span data-stu-id="469ef-160">You can embed this app in Employee self-service (ESS) for submitting referrals, or you can be use it as a hyperlink in the Corporate Portal and run as a stand-alone app.</span></span>

<span data-ttu-id="469ef-161">Til að sækja **forritið Referral** ferðu í [Dynamics 365 Talent viðbótarlausnina: Referral App](https://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) í Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="469ef-161">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) on the Microsoft Download Center.</span></span> <span data-ttu-id="469ef-162">Þú getur flutt þetta forrit inn og sérsniðið það til að bæta við viðbótarvirkni.</span><span class="sxs-lookup"><span data-stu-id="469ef-162">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="469ef-163">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="469ef-163">Additional resources</span></span>

[<span data-ttu-id="469ef-164">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="469ef-164">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="469ef-165">Flytja forrit á milli leigjenda og umhverfa</span><span class="sxs-lookup"><span data-stu-id="469ef-165">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
