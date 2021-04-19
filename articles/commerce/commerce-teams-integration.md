---
title: Dynamics 365 Commerce og Microsoft Teams samþættingaryfirlit
description: Þetta efnisatriði sýnir yfirlit yfir Microsoft Dynamics 365 Commerce og Microsoft Teams samþættingu.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3b7872757815d4eec0393e8b1c8c6ff5467e9473
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842681"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a><span data-ttu-id="ef6d2-103">Dynamics 365 Commerce og Microsoft Teams samþættingaryfirlit</span><span class="sxs-lookup"><span data-stu-id="ef6d2-103">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="ef6d2-104">Þetta efnisatriði sýnir yfirlit yfir Microsoft Dynamics 365 Commerce og Microsoft Teams samþættingu.</span><span class="sxs-lookup"><span data-stu-id="ef6d2-104">This topic presents an overview of Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="ef6d2-105">Dynamics 365 Commerce samþættist við Teams til að auðvelda viðskiptavinum og starfsmönnum þeirra að bæta framleiðni með því að samstilla verkstjórnun milli forritanna tveggja.</span><span class="sxs-lookup"><span data-stu-id="ef6d2-105">Dynamics 365 Commerce is integrating with Teams to help customers and their employees improve productivity by synchronizing task management between the two applications.</span></span> <span data-ttu-id="ef6d2-106">Hnökralaus verkstjórnunin sem samþætting Commerce og Teams býður upp á gerir verslunarstjórum og starfsmönnum kleift að búa til verklista, úthluta verkum á margar verslanir og rekja stöðu verka yfir verslanir úr öðru hvoru forritinu.</span><span class="sxs-lookup"><span data-stu-id="ef6d2-106">The seamless task management that Commerce and Teams integration provides lets store managers and employees create task lists, assign tasks to multiple stores, and track the status of tasks across stores, from either application.</span></span>

<span data-ttu-id="ef6d2-107">Samþætting Commerce og Teams er í boði frá og með Commerce útgáfu 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="ef6d2-107">Commerce and Teams integration is available as of the Commerce version 10.0.18 release.</span></span>

## <a name="key-features"></a><span data-ttu-id="ef6d2-108">Lykileiginleikar</span><span class="sxs-lookup"><span data-stu-id="ef6d2-108">Key features</span></span>

<span data-ttu-id="ef6d2-109">Hér eru nokkrir af helstu eiginleikunum sem samþætting Commerce og Microsoft Teams býður upp á:</span><span class="sxs-lookup"><span data-stu-id="ef6d2-109">Here are some of the key features that the Commerce and Microsoft Teams integration provides:</span></span>

- <span data-ttu-id="ef6d2-110">Úthluta Teams með því að nýta sér vel skilgreindar upplýsingar frá Commerce, t.d. skipulagseiningar fyrirtækis og upplýsingar um verslanir, starfsmenn, heimildir og yfirsýn viðskipta.</span><span class="sxs-lookup"><span data-stu-id="ef6d2-110">Provision Teams by taking advantage of well-defined information from Commerce, such as the organizational structure and information about stores, workers, permissions, and business context.</span></span>
- <span data-ttu-id="ef6d2-111">Samstilla breytingar sem eru í gangi á auðveldan hátt (til dæmis viðbót nýrra verslana eða ráðning nýrra starfsmanna) milli Commerce og Teams, en halda Commerce sem aðaluppruna á skipulagsgögnum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="ef6d2-111">Easily synchronize ongoing changes (for example, the addition of new stores or hiring of new employees) between Commerce and Teams, but keep Commerce as the master source of organizational structure data.</span></span>
- <span data-ttu-id="ef6d2-112">Samþætta verkstjórnun milli Commerce og Teams til að auðvelda starfsfólki verslunar, verslunarstjórum, svæðisstjórum og samskiptastjórum að sjá um verkstjórnun úr öðru hvoru forritinu.</span><span class="sxs-lookup"><span data-stu-id="ef6d2-112">Integrate task management between Commerce and Teams to help store workers, store managers, regional managers, and communications managers handle task management from either application.</span></span>

## <a name="prerequisites-for-using-integration-features"></a><span data-ttu-id="ef6d2-113">Forsendur fyrir notkun samþættingareiginleika</span><span class="sxs-lookup"><span data-stu-id="ef6d2-113">Prerequisites for using integration features</span></span>

<span data-ttu-id="ef6d2-114">Eftirfarandi skilyrði verða að vera til staðar áður en hægt er að nota Microsoft Teams samþættingareiginleika:</span><span class="sxs-lookup"><span data-stu-id="ef6d2-114">The following prerequisites must be in place before you can start to use Microsoft Teams integration features:</span></span>

- <span data-ttu-id="ef6d2-115">Microsoft 365 Business Standard License (þetta leyfi nær yfir Teams.)</span><span class="sxs-lookup"><span data-stu-id="ef6d2-115">Microsoft 365 Business Standard License (This license includes Teams.)</span></span>
- <span data-ttu-id="ef6d2-116">Azure Active Directory (Azure AD ) reikningar fyrir alla stjórnendur og starfsmenn í verslun</span><span class="sxs-lookup"><span data-stu-id="ef6d2-116">Azure Active Directory (Azure AD) accounts for all store managers and workers</span></span>
- <span data-ttu-id="ef6d2-117">Sölustaðakerfi (POS) sem eru grunnstillt með Azure AD sannvottun</span><span class="sxs-lookup"><span data-stu-id="ef6d2-117">Point of sale (POS) systems that are configured with Azure AD authentication</span></span>

## <a name="conceptual-architecture"></a><span data-ttu-id="ef6d2-118">Hugmyndahönnun</span><span class="sxs-lookup"><span data-stu-id="ef6d2-118">Conceptual architecture</span></span>

<span data-ttu-id="ef6d2-119">Eftirfarandi mynd sýnir hugmyndahönnun samþættingar Dynamics 365 Commerce og Microsoft Teams með því að nota verslun í San Francisco sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="ef6d2-119">The following illustration shows the conceptual architecture of Dynamics 365 Commerce and Microsoft Teams integration, using a San Francisco store as an example.</span></span> <span data-ttu-id="ef6d2-120">Bæði forritin Teams og Commerce á sölustað nota Microsoft Planner sem gagnageymslu þannig að verk sem gefin eru út í Teams koma til með að birtast í forriti sölustaðar og tilfallandi verkefni sem verslunarstjórar búa til í forriti sölustaðar birtast í Teams, sem leiðir til þægilegrar upplifunar í verkstjórnun á milli forritanna.</span><span class="sxs-lookup"><span data-stu-id="ef6d2-120">Both Teams and the Commerce POS application use Microsoft Planner as a repository so that tasks published from Teams appear in the POS application and ad hoc tasks created by store managers in the POS application appear in Teams, resulting in a seamless task management experience between the applications.</span></span>    

![Yfirlit yfir hönnun samþættingar Commerce og Teams](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="ef6d2-122">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ef6d2-122">Additional resources</span></span>

[<span data-ttu-id="ef6d2-123">Gera Dynamics 365 Commerce og Microsoft Teams samþættingu virka</span><span class="sxs-lookup"><span data-stu-id="ef6d2-123">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="ef6d2-124">Ákvæði Microsoft Teams frá Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ef6d2-124">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="ef6d2-125">Samstilla verkstjórnun á milli Microsoft Teams og Dynamics 365 Commerce sölustaðar</span><span class="sxs-lookup"><span data-stu-id="ef6d2-125">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="ef6d2-126">Stjórna notandahlutverkum í Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ef6d2-126">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="ef6d2-127">Varpa verslunum og teymum ef fyrirliggjandi teymi eru í Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ef6d2-127">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="ef6d2-128">Algengar spurningar um samþættingu Dynamics 365 Commerce og Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ef6d2-128">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
