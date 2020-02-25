---
title: Stækka Talent með Power Apps og Power Automate
description: Þessi grein lýsir sumum dæmum um atburðarás stækkunarhæfni fyrir Microsoft Dynamics 365 Talent - Attract sem notar Microsoft Power Apps og Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 1051fa4db16bb94cc9d60a91fc3637d7e5305cc2
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029912"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="05f94-103">Stækka Talent með Power Apps og Power Automate</span><span class="sxs-lookup"><span data-stu-id="05f94-103">Extend Talent with Power Apps and Power Automate</span></span>

<span data-ttu-id="05f94-104">Þessi grein lýsir sumum dæmum um atburðarás stækkunarhæfni fyrir Microsoft Dynamics 365 Talent: Attract sem notar Microsoft Power Apps og Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="05f94-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent: Attract that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="05f94-105">Hægt er að flytja lausnapakkann sem tengist hverju dæmi inn í Power Apps-umhverfið.</span><span class="sxs-lookup"><span data-stu-id="05f94-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="05f94-106">Síðan er hægt að nota pakkana annaðhvort sem leiðarvísi eða sem upphafspunkta til að innleiða atburðarásir sem eiga við um fyrirtækið þitt.</span><span class="sxs-lookup"><span data-stu-id="05f94-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05f94-107">Ef þú vilt nota sniðmátin og forritið sem lýst er í þessari grein „eins og það er“, skaltu vera viss um að prófa þau til að ganga úr skugga um þau nái utan um allar atburðarásirnar sem tengjast innleiðingunni þinni.</span><span class="sxs-lookup"><span data-stu-id="05f94-107">If you want to use the templates and app that are described in this article "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="05f94-108">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="05f94-108">Prerequisites</span></span>

- <span data-ttu-id="05f94-109">Til að flytja inn pakka verða notendur að hafa heimildina **Umhverfishönnuður**.</span><span class="sxs-lookup"><span data-stu-id="05f94-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="05f94-110">Til að flytja forrit út eða inn verða notendur að hafa Power Apps Plan 2 leyfi eða Power Apps Plan 2 prufuleyfi.</span><span class="sxs-lookup"><span data-stu-id="05f94-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="05f94-111">Power Automate - Skjámynd Connect</span><span class="sxs-lookup"><span data-stu-id="05f94-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="05f94-112">Sniðmátið **Power Automate - Skjámynd Connect** er hægt að nota til að lesa gögn úr Microsoft Forms og vista þau í einingunni Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="05f94-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="05f94-113">Þetta sniðmát er hægt að framlengja þannig að hægt sé að nota það í öðrum atburðarásum.</span><span class="sxs-lookup"><span data-stu-id="05f94-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="05f94-114">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="05f94-114">Here are some examples:</span></span>

- <span data-ttu-id="05f94-115">Sækja mat á umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="05f94-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="05f94-116">Sækja niðurstöður úr spurningalistum námskeiðs.</span><span class="sxs-lookup"><span data-stu-id="05f94-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="05f94-117">Taka saman safn af viðtalsspurningum fyrir mannauðsstjóra.</span><span class="sxs-lookup"><span data-stu-id="05f94-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="05f94-118">Sækja mat umsækjanda á viðtalsferlinu</span><span class="sxs-lookup"><span data-stu-id="05f94-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="05f94-119">Í Microsoft Dynamics 365: Attract er hægt að nota skjámyndir í umsækjendagátt, þar sem umsækjendur fylla út upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="05f94-119">In Microsoft Dynamics 365: Attract, you can use forms in the candidate portal, where candidates fill in details.</span></span> <span data-ttu-id="05f94-120">Einnig er hægt að fella inn skjámyndir sem verkþætti í starfssniðmáti.</span><span class="sxs-lookup"><span data-stu-id="05f94-120">You can also embed forms as activities in a job template.</span></span>

<span data-ttu-id="05f94-121">Þegar umsækjandi sendir inn eyðublað, sækir Microsoft Power Automate innsent eyðublaðið, les gögnin og geymir þau í Common Data Service-einingunni.</span><span class="sxs-lookup"><span data-stu-id="05f94-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="05f94-122">Til að sækja sniðmátið **Power Automate - Skjámynd Connect** og sérsniðna skipulagseiningu skal fara í [Power Automate - Skjámynd Connect](https://go.microsoft.com/fwlink/?linkid=2081988) í Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="05f94-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="05f94-123">Power Automate – SharePoint samþætting</span><span class="sxs-lookup"><span data-stu-id="05f94-123">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="05f94-124">Hægt er að nota sniðmátið **Power Automate – SharePoint samþætting** til að lesa gögn úr Microsoft SharePoint-lista, bera listann saman við reitagildi fyrir allar Common Data Service-einingar og senda niðurstöður samanburðar sem tilkynningapóst.</span><span class="sxs-lookup"><span data-stu-id="05f94-124">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="05f94-125">Fyrirtæki gæti verið með einhverja hæfni sem þarf nauðsynlega að uppfylla.</span><span class="sxs-lookup"><span data-stu-id="05f94-125">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="05f94-126">Þessa hæfni er hægt að geyma í SharePoint sem SharePoint-lista.</span><span class="sxs-lookup"><span data-stu-id="05f94-126">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="05f94-127">Þegar umsækjandi sækir um eitthvað starf þar sem ákveðin hæfni er tekin fram er tilkynningapóstur sendur ef góð samsvörun er milli hæfni umsækjanda og hæfninnar sem geymd er í SharePoint.</span><span class="sxs-lookup"><span data-stu-id="05f94-127">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="05f94-128">Þannig er fyllt hraðar upp í stöður sem þarf nauðsynlega að ráða í, því að tilkynningarnar hjálpa ráðningaraðilum að endurráða umsækjendur innan fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="05f94-128">This helps fill positions that are urgently required faster, because the notifications help recruiters cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="05f94-129">Hægt er að stækka þetta sniðmát svo nota megi það fyrir atburðarás sem hefur með SharePoint-samþættingu að gera.</span><span class="sxs-lookup"><span data-stu-id="05f94-129">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="05f94-130">Til að hlaða niður sniðmátinu **Power Automate - SharePoint samþætting** skal fara í [Power Automate - SharePoint samþætting](https://go.microsoft.com/fwlink/?linkid=2082109) í Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="05f94-130">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="05f94-131">Tilvísunforrit</span><span class="sxs-lookup"><span data-stu-id="05f94-131">Referral App</span></span>

<span data-ttu-id="05f94-132">Hægt er að nota tilvísunarforritið til að bæta við umbjóðendum í sameiginlegt hæfileikasafn.</span><span class="sxs-lookup"><span data-stu-id="05f94-132">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="05f94-133">Tilvísandi getur fært inn **Fornafn**, **Eftirnafn**, **Netfang** og **Slóð í LinkedIn** við framlagningu umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="05f94-133">The referrer can enter **Firstname**, **Lastname**, **Email**, and **LinkedIn URL** when submitting a candidate.</span></span> <span data-ttu-id="05f94-134">Lýsigögn umsækjandans eru síðan fyllt út með upplýsingum tilvísunaraðila.</span><span class="sxs-lookup"><span data-stu-id="05f94-134">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="05f94-135">Hægt er að fella þetta forrit inn í starfsmannaþjónustuna til að senda tilvísanir, eða nota það sem tengil á fyrirtækjagáttina og keyra það sem sjálfstætt forrit.</span><span class="sxs-lookup"><span data-stu-id="05f94-135">You can embed this app in Employee self service for submitting referrals, or you can use it as a hyperlink in the corporate portal and run it as a stand-alone app.</span></span>

<span data-ttu-id="05f94-136">Til að sækja **forritið Referral** ferðu í [Dynamics 365 Talent viðbótarlausnina: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) í Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="05f94-136">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) on the Microsoft Download Center.</span></span> <span data-ttu-id="05f94-137">Þú getur flutt þetta forrit inn og sérsniðið það til að bæta við viðbótarvirkni.</span><span class="sxs-lookup"><span data-stu-id="05f94-137">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="05f94-138">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="05f94-138">Additional resources</span></span>

[<span data-ttu-id="05f94-139">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="05f94-139">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[<span data-ttu-id="05f94-140">Flytja forrit á milli leigjenda og umhverfa</span><span class="sxs-lookup"><span data-stu-id="05f94-140">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
