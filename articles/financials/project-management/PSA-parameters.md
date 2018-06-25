---
title: "Samþættingarfæribreytur Project Service Automation"
description: "Þú getur stillt hvernig gögn eiga að vera sjálfgefin við samþættingu Project Service Automation við Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 32f7f70c5b1071cef5a3360ccc09fa2d95fbf9a9
ms.contentlocale: is-is
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation-integration-parameters"></a><span data-ttu-id="c6b01-103">Samþættingarfæribreytur Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c6b01-103">Project Service Automation integration parameters</span></span>

<span data-ttu-id="c6b01-104">Á síðunni **Samþættingarfæribreytur Project Service Automation** getur þú stillt hvernig gögn eiga að vera sjálfgefin við samþættingu Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c6b01-104">On the **Project Service Automation integration parameters** page, you can configure how data should default when integrating Project Service Automation with Finance and Operations.</span></span> <span data-ttu-id="c6b01-105">Eftirfarandi verður að vera uppsett svo takist að samstilla verk frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c6b01-105">The following must be set up for projects to be successfully synchronized from Project Service Automation in Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="c6b01-106">Samþætting verkefna fyrir verk, flokkar kostnaðarfærslna, áætlaður tími, kostnaðaráætlun og virknilæsing er í boði í Dynamics 365 for Finance and Operations útgáfu 8.0.</span><span class="sxs-lookup"><span data-stu-id="c6b01-106">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>




| <span data-ttu-id="c6b01-107">**Flipi**</span><span class="sxs-lookup"><span data-stu-id="c6b01-107">**Tab**</span></span>                      | <span data-ttu-id="c6b01-108">**Svæði**</span><span class="sxs-lookup"><span data-stu-id="c6b01-108">**Field**</span></span>                          | <span data-ttu-id="c6b01-109">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="c6b01-109">**Description**</span></span>                    |
|------------------------------|------------------------------------|--------------------------------|
| <span data-ttu-id="c6b01-110">**Almennt**</span><span class="sxs-lookup"><span data-stu-id="c6b01-110">**General**</span></span>                  | <span data-ttu-id="c6b01-111">**Sjálfgefin verkgerð**</span><span class="sxs-lookup"><span data-stu-id="c6b01-111">**Default project type**</span></span>               | <span data-ttu-id="c6b01-112">Veldu sjálfgefið fyrir **Gerð verks** sem er þegar verk eru samstillt frá Project Service Automation ef þú hefur ekki gefið upp sjálfgefið gildi í samþættingarsniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="c6b01-112">Select the default for **Project type**, which is when projects are synchronized from Project Service Automation if you have not provided a default value in the integration template.</span></span> <span data-ttu-id="c6b01-113">Við samstillingu munu ný verk hafa **Gerð verks** stillt á þetta gildi og hægt er að uppfæra þegar verksamningslínurnar eru samstilltar frá Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c6b01-113">During synchronization, new projects will have the **Project type** set to this value and may be updated when the project contract lines are synchronized from Project Service Automation.</span></span>               |
| <span data-ttu-id="c6b01-114">**Almennt**</span><span class="sxs-lookup"><span data-stu-id="c6b01-114">**General**</span></span>                  | <span data-ttu-id="c6b01-115">**Tímaflokkur**</span><span class="sxs-lookup"><span data-stu-id="c6b01-115">**Time category**</span></span>                      | <span data-ttu-id="c6b01-116">Veldu sjálfgefið fyrir **Tímaflokk** sem er þegar tímaáætlanir eru samstilltar frá Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c6b01-116">Select the default for **Time category**, which is when hour estimates are synchronized from Project Service Automation.</span></span> <span data-ttu-id="c6b01-117">Við samstillingu munu nýjar tímaspár verks í Finance and Operations hafa **Flokkinn** stilltan á þetta gildi þegar tímaáætlanir og rauntími eru samstilltir frá Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c6b01-117">During synchronization, new project hour forecasts in Finance and Operations will have the **Category** set to this value when the hour estimates and hour actuals are synchronized from Project Service Automation.</span></span>   |
| <span data-ttu-id="c6b01-118">**Almennt**</span><span class="sxs-lookup"><span data-stu-id="c6b01-118">**General**</span></span>                  | <span data-ttu-id="c6b01-119">**Tegund þóknunar**</span><span class="sxs-lookup"><span data-stu-id="c6b01-119">**Fee category**</span></span>                       | <span data-ttu-id="c6b01-120">Veldu sjálfgefið fyrir **Þóknunarflokk** sem er þegar raunupphæðir þóknunar eru samstilltar frá Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c6b01-120">Select the default for **Fee category**, which is when fee actuals are synchronized from Project Service Automation.</span></span> <span data-ttu-id="c6b01-121">Við samstillingu munu nýjar þóknunarfærslur í Finance and Operations hafa **Flokkinn** stilltan á þetta gildi þegar raunupphæðir þóknunar eru samstilltar frá Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c6b01-121">During synchronization, new fee transactions in Finance and Operations will have the **Category** set to this value when the fee actuals are synchronized from Project Service Automation.</span></span>          |
| <span data-ttu-id="c6b01-122">**Sjálfgildi verkflokks**</span><span class="sxs-lookup"><span data-stu-id="c6b01-122">**Project group defaults**</span></span>   | <span data-ttu-id="c6b01-123">**Gerð verks**</span><span class="sxs-lookup"><span data-stu-id="c6b01-123">**Project type**</span></span> | <span data-ttu-id="c6b01-124">Smelltu á **Ný** til að bæta við línu þar sem þú getur valið verkgerðina þar sem á að stilla sjálfgefna verkflokkinn.</span><span class="sxs-lookup"><span data-stu-id="c6b01-124">Click **New** to add a row where you can select the project type for which to set the default project group.</span></span> <span data-ttu-id="c6b01-125">Hægt er að velja tiltekna verkgerð aðeins einu sinni í skilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="c6b01-125">A specific project type can be selected only once in the configuration.</span></span>              
|                              | <span data-ttu-id="c6b01-126">**Verkflokkur**</span><span class="sxs-lookup"><span data-stu-id="c6b01-126">**Project group**</span></span>          | <span data-ttu-id="c6b01-127">Veldu sjálfgefna verkflokkinn fyrir tiltekna verkgerð.</span><span class="sxs-lookup"><span data-stu-id="c6b01-127">Select the default project group for the specified project type.</span></span> <span data-ttu-id="c6b01-128">Þegar ný verk eru samstillt frá Project Service Automation mun **Verkflokkurinn** vera sjálfgefinn á grundvelli verkgerðarinnar ef þú hefur ekki gefið upp sjálfgefið gildi í samþættingarsniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="c6b01-128">When new projects are synced from Project Service Automation, the **Project group** will be the default based on the project type if you have not provided a default value in the integration template.</span></span>  |
| <span data-ttu-id="c6b01-129">**Sjálfgefnar gerðir reiknings**</span><span class="sxs-lookup"><span data-stu-id="c6b01-129">**Billing type defaults**</span></span>    | <span data-ttu-id="c6b01-130">**Reikningsfærsluflokkur**</span><span class="sxs-lookup"><span data-stu-id="c6b01-130">**Billing type**</span></span> | <span data-ttu-id="c6b01-131">Smelltu á **Ný** til að bæta við línu þar sem þú getur valið reikningsgerðina þar sem á að stilla sjálfgefinn línueiginleika.</span><span class="sxs-lookup"><span data-stu-id="c6b01-131">Click **New** to add a row where you can select the billing type for which to set the default line property.</span></span> <span data-ttu-id="c6b01-132">Hægt er að velja tiltekna reikningsgerð aðeins einu sinni í skilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="c6b01-132">A specific billing type can be selected only once in the configuration.</span></span>          |
|                              | <span data-ttu-id="c6b01-133">**Línueiginleiki**</span><span class="sxs-lookup"><span data-stu-id="c6b01-133">**Line property**</span></span>| <span data-ttu-id="c6b01-134">Veldu sjálfgefinn línueiginleika fyrir tilgreinda reikningsgerð.</span><span class="sxs-lookup"><span data-stu-id="c6b01-134">Select the default line property for the specified billing type.</span></span> <span data-ttu-id="c6b01-135">Þegar nýjar tímaáætlanir, nýjar kostnaðaráætlanir eða nýjar rauntölur eru samstilltar frá Project Service Automation verður **Línueiginleikinn** sjálfgefinn á grundvelli reikningsgerðarinnar.</span><span class="sxs-lookup"><span data-stu-id="c6b01-135">When new hour estimates, new expense estimates, or new actuals are synced from Project Service Automation, the **Line property** will be the default based on the billing type.</span></span>          |
| <span data-ttu-id="c6b01-136">**Aðgerðarlæsing**</span><span class="sxs-lookup"><span data-stu-id="c6b01-136">**Functionality locking**</span></span>    |                   | <span data-ttu-id="c6b01-137">Veldu aðgerðina til að slökkva á Finance and Operations fyrir verk og samninga sem koma frá Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c6b01-137">Select the functionality to disable in Finance and Operations for projects and contracts that originated from Project Service Automation.</span></span> <span data-ttu-id="c6b01-138">Til dæmis getur þú valið að slökkva á möguleikanum til að breyta samningum og verkum, búa til sundurliðun verkþátta og slá inn vinnukort í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c6b01-138">For example, you can choose to turn off the ability to edit contracts and projects, create work breakdown structures, and enter timesheets in Finance and Operations.</span></span> <span data-ttu-id="c6b01-139">Bókhaldstengdir reitir verða áfram virkir, jafnvel þótt þeir séu ekki tiltækir samkvæmt færibreytustillingunni.</span><span class="sxs-lookup"><span data-stu-id="c6b01-139">Accounting-related fields will continue to be enabled, even if they are made unavailable by the parameter setting.</span></span> <span data-ttu-id="c6b01-140">Að sjálfgefnu verða allar aðgerðir virkjaðar.</span><span class="sxs-lookup"><span data-stu-id="c6b01-140">By default, all functionality will be enabled.</span></span>           |
