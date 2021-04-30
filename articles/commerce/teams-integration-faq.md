---
title: Algengar spurningar um samþættingu Dynamics 365 Commerce og Microsoft Teams
description: Þetta efnisatriði veitir svör við algengum spurningum um samþættingu Microsoft Dynamics 365 Commerce og Microsoft Teams.
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
ms.openlocfilehash: bf9aebb1c8ba7cf4fee3f0471a10872de1e23ce6
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908857"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a><span data-ttu-id="c6aba-103">Algengar spurningar um samþættingu Dynamics 365 Commerce og Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c6aba-103">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c6aba-104">Þetta efnisatriði veitir svör við algengum spurningum um samþættingu Microsoft Dynamics 365 Commerce og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="c6aba-104">This topic provides answers to frequently asked questions regarding Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a><span data-ttu-id="c6aba-105">Hver í verslun verður eigandi teymis við úthlutun Teams úr Commerce?</span><span class="sxs-lookup"><span data-stu-id="c6aba-105">Who in the store becomes an owner of a team while provisioning Teams from Commerce?</span></span> 

<span data-ttu-id="c6aba-106">Öllum verslunarstjórum er sjálfkrafa bætt við sem eigendum í samsvarandi teymishóp þannig að þeir geti framkvæmt aðgerðir eins og að bæta við einkarás og bæta við eða eyða meðlimum.</span><span class="sxs-lookup"><span data-stu-id="c6aba-106">All store managers are automatically added as owners to the corresponding team group so that they can perform operations such as adding a private channel and adding or deleting members.</span></span> 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a><span data-ttu-id="c6aba-107">Hvernig úthluta ég starfsmanni hlutverki „samskiptastjóra“ í Commerce Headquarters?</span><span class="sxs-lookup"><span data-stu-id="c6aba-107">How do I assign the "communications manager" role to an employee in Commerce headquarters?</span></span> 

<span data-ttu-id="c6aba-108">Samskiptastjórar í Microsoft Teams hafa getu til að búa til og birta verkefnalista.</span><span class="sxs-lookup"><span data-stu-id="c6aba-108">Communication managers in Microsoft Teams have the ability to create and publish task lists.</span></span> <span data-ttu-id="c6aba-109">Starfsmenn fyrirtækis sem þurfa að gerast samskiptastjórar verða að hafa fengið úthlutað hlutverkinu „stjórnandi smásöluverks“ í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="c6aba-109">Organization employees who need to become communication managers must have the "retail task manager" role assigned to them in Commerce headquarters.</span></span>

<span data-ttu-id="c6aba-110">Fylgið þessum skrefum til að úthluta hlutverki stjórnanda smásölu á starfsmann í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="c6aba-110">To assign the retail task manager role to an employee in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="c6aba-111">Farðu í **Retail og Commerce \> Starfsmenn \> Notendur**.</span><span class="sxs-lookup"><span data-stu-id="c6aba-111">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="c6aba-112">Velja starfsmann.</span><span class="sxs-lookup"><span data-stu-id="c6aba-112">Select an employee.</span></span>
1. <span data-ttu-id="c6aba-113">Á flýtiflipanum **Hlutverk notanda** velurðu **Úthluta hlutverkum**.</span><span class="sxs-lookup"><span data-stu-id="c6aba-113">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="c6aba-114">Í valmyndinni **Úthluta hlutverkum til notanda** velurðu hlutverkið **Stjórnandi smásöluverks** og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c6aba-114">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a><span data-ttu-id="c6aba-115">Hvernig býð ég upp á upphleðslu á ákveðnu fyrirtækjastigveldi í Microsoft Teams?</span><span class="sxs-lookup"><span data-stu-id="c6aba-115">How do I make a specific organization hierarchy available to upload into Microsoft Teams?</span></span>

<span data-ttu-id="c6aba-116">Í Commerce Headquarters tengist sérhvert stigveldi fyrirtækis að minnsta kosti einum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="c6aba-116">In Commerce headquarters, every organization's hierarchy is associated with one or more purposes.</span></span> <span data-ttu-id="c6aba-117">Gangið úr skugga um að stigveldið sem ætlunin er að úthluta í Microsoft Teams hafi tilganginn **Skýrslugerð smásölu** tengdan við eins og sýnt er í eftirfarandi myndadæmi.</span><span class="sxs-lookup"><span data-stu-id="c6aba-117">Make sure the hierarchy that you want to provision into Microsoft Teams has the **Retail reporting** purpose associated with it, as shown in the following example image.</span></span> 

![Dæmi um tilgang fyrirtækjastigveldis í Commerce Headquarters](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a><span data-ttu-id="c6aba-119">Hvernig geri ég starfsmönnum smásöluverslunar kleift að skrá sig inn á sölustað Commerce með Azure Active Directory (Azure AD)?</span><span class="sxs-lookup"><span data-stu-id="c6aba-119">How do I enable retail store workers to sign in to Commerce point of sale (POS) using Azure Active Directory (Azure AD)?</span></span>

<span data-ttu-id="c6aba-120">Upplýsingar um hvernig á að skilgreina innskráningarupplifun sölustaðar Commerce til að nota Azure AD sannvotun er að finna í [Virkja Azure Active Directory sannvottun fyrir POS innskráningu](aad-pos-logon.md).</span><span class="sxs-lookup"><span data-stu-id="c6aba-120">For information about how to configure the Commerce POS sign-in experience to use Azure AD authentication, see [Enable Azure Active Directory authentication for POS sign-in](aad-pos-logon.md).</span></span>

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a><span data-ttu-id="c6aba-121">Hvernig varpa ég verslunum og samsvarandi teymum í Commerce Headquarters ef fyrirtækið mitt hefur þegar stofnað teymi í Microsoft Teams?</span><span class="sxs-lookup"><span data-stu-id="c6aba-121">How do I map stores and corresponding teams in Commerce headquarters if my organization has already created teams in Microsoft Teams?</span></span>

<span data-ttu-id="c6aba-122">Upplýsingar um hvernig á að varpa verslunum og teymum ef fyrirliggjandi teymi eru til staðar er að finna í [Varpa verslunum og samsvarandi teymum ef fyrirtækið þitt er með fyrirliggjandi teymi í Microsoft Teams](map-stores-existing-teams.md).</span><span class="sxs-lookup"><span data-stu-id="c6aba-122">For information on how to map stores and teams if there are pre-existing teams, see [Map stores and corresponding teams if your organization has pre-existing teams in Microsoft Teams](map-stores-existing-teams.md).</span></span>

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a><span data-ttu-id="c6aba-123">Hvernig hreinsa ég lykil Microsoft Graph API sem geymdur er í lotugeymslu?</span><span class="sxs-lookup"><span data-stu-id="c6aba-123">How do I clear the Microsoft Graph API token stored in the session storage?</span></span>

<span data-ttu-id="c6aba-124">Notandi sem hefur skráð sig inn á sölustað með Azure Active Directory (Azure AD) reikningi ætti að skrá sig út af sölustað eða loka forritinu til að hreinsa lotugeymsluna.</span><span class="sxs-lookup"><span data-stu-id="c6aba-124">A user who has signed in to the point of sale (POS) with an Azure Active Directory (Azure AD) account should sign out from the POS or close the application to clear the session storage.</span></span> 

> [!TIP]
> <span data-ttu-id="c6aba-125">Mælt er með að starfsmenn verslunar venji sig á að læsa alltaf afgreiðslukassanum eða skrái sig út úr lotu þegar þeir eru ekki að nota afgreiðslukassann.</span><span class="sxs-lookup"><span data-stu-id="c6aba-125">A recommended best practice is to always have store workers lock the POS terminal or sign out from a session when not using the terminal.</span></span> 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a><span data-ttu-id="c6aba-126">Hvað gerist ef verslun er ekki með verslunarstjóra?</span><span class="sxs-lookup"><span data-stu-id="c6aba-126">What happens if a store doesn't have store managers?</span></span>

<span data-ttu-id="c6aba-127">Ef verslun er ekki með stjórnendur verður teymishópur ekki stofnaður fyrri verslunina eða í Teams.</span><span class="sxs-lookup"><span data-stu-id="c6aba-127">If a store doesn't have managers, a team group will not be created for the store or in Teams.</span></span> 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a><span data-ttu-id="c6aba-128">Hvað gerist ef verslunarstjóri yfirgefur fyrirtækið?</span><span class="sxs-lookup"><span data-stu-id="c6aba-128">What happens if a store manager leaves the company?</span></span>

<span data-ttu-id="c6aba-129">Allir sem eru með hlutverk eiganda geta bætt við nýjum verslunarstjóra í Commerce Headquarters og endurúthlutað Teams þannig að nýi stjórnandinn fái nauðsynleg réttindi í Teams fyrir hópinn.</span><span class="sxs-lookup"><span data-stu-id="c6aba-129">Anyone with the owner role can add a new store manager in Commerce headquarters and reprovision Teams so that the new manager will have the necessary privileges in Teams for the group.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="c6aba-130">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c6aba-130">Additional resources</span></span>

[<span data-ttu-id="c6aba-131">Dynamics 365 Commerce og Microsoft Teams samþættingaryfirlit</span><span class="sxs-lookup"><span data-stu-id="c6aba-131">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="c6aba-132">Gera Dynamics 365 Commerce og Microsoft Teams samþættingu virka</span><span class="sxs-lookup"><span data-stu-id="c6aba-132">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="c6aba-133">Ákvæði Microsoft Teams frá Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c6aba-133">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="c6aba-134">Samstilla verkstjórnun á milli Microsoft Teams og Dynamics 365 Commerce sölustaðar</span><span class="sxs-lookup"><span data-stu-id="c6aba-134">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="c6aba-135">Stjórna notandahlutverkum í Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c6aba-135">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="c6aba-136">Varpa verslunum og teymum ef fyrirliggjandi teymi eru í Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c6aba-136">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)
