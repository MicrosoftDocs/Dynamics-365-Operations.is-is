---
title: Stækka Talent með Power Apps og Power Automate
description: Þessi grein lýsir sumum dæmum um atburðarás stækkunarhæfni fyrir Microsoft Dynamics 365 Human Resources sem notar Microsoft Power Apps og Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core;Experience Apps;Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1c5bc0776174960af6cb8a62f00e3fd7d56b1676
ms.sourcegitcommit: 58d7133ae9909fa205730e3cf4c7fd5a1d5d0b75
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/10/2020
ms.locfileid: "3793612"
---
# <a name="extend-with-power-apps-and-power-automate"></a><span data-ttu-id="5954e-103">Stækka með Power Apps og Power Automate</span><span class="sxs-lookup"><span data-stu-id="5954e-103">Extend with Power Apps and Power Automate</span></span>

<span data-ttu-id="5954e-104">Þessi grein lýsir sumum dæmum um atburðarás stækkunarhæfni fyrir Microsoft Dynamics 365 Human Resources sem notar Microsoft Power Apps og Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="5954e-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Human Resources that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="5954e-105">Hægt er að flytja lausnapakkann sem tengist hverju dæmi inn í Power Apps-umhverfið.</span><span class="sxs-lookup"><span data-stu-id="5954e-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="5954e-106">Síðan er hægt að nota pakkana annaðhvort sem leiðarvísi eða sem upphafspunkta til að innleiða atburðarásir sem eiga við um fyrirtækið þitt.</span><span class="sxs-lookup"><span data-stu-id="5954e-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5954e-107">Ef þú vilt nota sniðmátin og forritin sem lýst er í þessu efnisatriði „eins og það er“, skaltu vera viss um að prófa þau til að ganga úr skugga um þau nái utan um allar atburðarásirnar sem tengjast innleiðingunni þinni.</span><span class="sxs-lookup"><span data-stu-id="5954e-107">If you want to use the templates and apps that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5954e-108">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="5954e-108">Prerequisites</span></span>

- <span data-ttu-id="5954e-109">Til að flytja inn pakka verða notendur að hafa heimildina **Umhverfishönnuður**.</span><span class="sxs-lookup"><span data-stu-id="5954e-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="5954e-110">Til að flytja forrit út eða inn verða notendur að hafa Power Apps Plan 2 leyfi eða Power Apps Plan 2 prufuleyfi.</span><span class="sxs-lookup"><span data-stu-id="5954e-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="integration-with-office-365-power-automate"></a><span data-ttu-id="5954e-111">Samþætting við Office 365, Power Automate</span><span class="sxs-lookup"><span data-stu-id="5954e-111">Integration with Office 365, Power Automate</span></span>

<span data-ttu-id="5954e-112">Forritið **Samþætting við Office 365** er hægt að nota til að draga út upplýsingar um hóp fyrir innskráða notendur úr Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="5954e-112">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="5954e-113">Í henni er vísað til starfsmanna í Human Resources til að draga út kennitegundir starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="5954e-113">It references workers in Human Resources to extract employee identification types.</span></span> <span data-ttu-id="5954e-114">Stjórnendur geta athugað lokadaga kennigerða starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="5954e-114">Managers can check expiration dates of employee ID types.</span></span> <span data-ttu-id="5954e-115">Þeir geta einnig sent tölvupóst áminningu ef kennitölu starfsmanns er að renna út.</span><span class="sxs-lookup"><span data-stu-id="5954e-115">They can also send an email reminder if the employee ID type is expiring.</span></span> <span data-ttu-id="5954e-116">Power Automate samþættist við Power Apps til að senda þessa áminningu.</span><span class="sxs-lookup"><span data-stu-id="5954e-116">Power Automate integrates with Power Apps to send this reminder.</span></span> <span data-ttu-id="5954e-117">Staðfesting verður send aftur til Power Apps frá Power Automate þegar áminningin er send.</span><span class="sxs-lookup"><span data-stu-id="5954e-117">Confirmation will be sent back to Power Apps from Power Automate when the reminder is sent.</span></span> <span data-ttu-id="5954e-118">Auðkenningargerðir innihalda ökuskírteini, vegabréf og önnur ásættanleg skilríki.</span><span class="sxs-lookup"><span data-stu-id="5954e-118">Identification types include driver's license, passport, and other acceptable forms of ID.</span></span>

<span data-ttu-id="5954e-119">Þú getur lengt þetta forrit fyrir aðrar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="5954e-119">You can extend this app for other scenarios.</span></span> <span data-ttu-id="5954e-120">Til dæmis er hægt að nota það til að sýna upplýsingar um frí hóps, viðburði dagatals og alla viðburði sem tengjast hópnum.</span><span class="sxs-lookup"><span data-stu-id="5954e-120">For example, you can use it to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="5954e-121">Til að hlaða niður forritnu **Samþætting við Office 365, Power Automate** skal fara í [Samþætting við Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) í Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="5954e-121">To download the **Integration with Office 365, Power Automate** app, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="5954e-122">Power Automate - SQL Connect og framkvæmd</span><span class="sxs-lookup"><span data-stu-id="5954e-122">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="5954e-123">Sniðmátið **Power Automate - SQL Connect og framkvæmd** tengist við Microsoft SQL Server og virkjar keyrslu á SQL-fyrirspurnum.</span><span class="sxs-lookup"><span data-stu-id="5954e-123">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="5954e-124">Þrátt fyrir að þetta sniðmát lesi og uppfærir SQL töflur, geturðu lengt það og notað það fyrir aðrar sviðsmyndir.</span><span class="sxs-lookup"><span data-stu-id="5954e-124">Although this template reads and updates SQL tables, you can extend it and use it for other scenarios.</span></span> <span data-ttu-id="5954e-125">Til dæmis er hægt að nota það til að fylla út millistigsvistunartöflu í Common Data Service með skrám úr SQL-þjóni, og til að gera reglubundna samstillingu á millistigsvistunartöflu með því að nota stigvaxandi færslu úr SQL-þjóni.</span><span class="sxs-lookup"><span data-stu-id="5954e-125">For example, you can use it to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="5954e-126">Háþróaður fyrirspurn er samþætt með flæði til að gera gagnaflutning og stigvaxandi ýtingu möguleg.</span><span class="sxs-lookup"><span data-stu-id="5954e-126">Advanced Query is integrated with Flow to enable Data transformation and incremental push.</span></span>

<span data-ttu-id="5954e-127">Til að hlaða niður sniðmátinu **Power Automate - SQL Connect og framkvæmd** skal fara í [Power Automate - SQL Connect og framkvæmd](https://go.microsoft.com/fwlink/?linkid=2081789) í Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="5954e-127">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5954e-128">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="5954e-128">Additional resources</span></span>

[<span data-ttu-id="5954e-129">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="5954e-129">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>