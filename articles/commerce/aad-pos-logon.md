---
title: Virkja Azure Active Directory sannvottun fyrir POS innskráningu
description: Þetta efni útskýrir hvernig á að stilla innskráningarupplifunina fyrir Microsoft Dynamics 365 Commerce sölustað (POS) þannig að hún noti Azure Active Directory auðkenningu.
author: boycezhu
manager: annbe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d6073a04814adf8237b4caa952b31b011f4b34bf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982741"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="9a140-103">Virkja Azure Active Directory sannvottun fyrir POS innskráningu</span><span class="sxs-lookup"><span data-stu-id="9a140-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="9a140-104">Margir viðskiptavinir sem nota Microsoft Dynamics 365 Commerce nota einnig aðra Microsoft-skýjaþjónustu og þeir gætu notað Azure Active Directory (Azure AD) til að stjórna notendaskilríkjum fyrir þessa þjónustu.</span><span class="sxs-lookup"><span data-stu-id="9a140-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="9a140-105">Í þeim tilvikum gætu viðskiptavinirnir viljað nota sama Azure AD reikninginn yfir forrit.</span><span class="sxs-lookup"><span data-stu-id="9a140-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="9a140-106">Þetta efni útskýrir hvernig á að stilla innskráningarupplifun sölustaðar (POS) í Commerce til að nota Azure AD auðkenningu.</span><span class="sxs-lookup"><span data-stu-id="9a140-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="9a140-107">Skilgreina Azure AD sannvottun</span><span class="sxs-lookup"><span data-stu-id="9a140-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="9a140-108">Til að gera Azure AD tiltækt sem sannvottunaraðferð fyrir POS innskráningu fyrir verslun, verður þú að skilgreina stillingarnar á virkni sniðs verslunarinnar og nota þær stillingar á POS viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="9a140-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="9a140-109">Til að skilgreina virknireglu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="9a140-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="9a140-110">Fara í **Retail og Commerce** \> **Uppsetning rásar** \> **Uppsetning sölustaðar** \> **Forstillingar sölustaðar** \> **Virknireglur**.</span><span class="sxs-lookup"><span data-stu-id="9a140-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="9a140-111">Veldu virkniregluna sem á að breyta.</span><span class="sxs-lookup"><span data-stu-id="9a140-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="9a140-112">Á flýtiflipanum **Aðgerðir**, í hlutanum **Innskráning starfsmanna í POS**, breytirðu gildi í reitnum **Sannvottunaraðferð innskráningar** úr **Persónuskilríki og lykilorð** í **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="9a140-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="9a140-113">Sjálfgefið eru allar virknireglur nota **Persónuskilríki og lykilorð** sem POS sannvottunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="9a140-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="9a140-114">Þess vegna verður þú að breyta gildi í reitnum **Sannvottunaraðferð innskráningar** ef þú vilt nota Azure AD.</span><span class="sxs-lookup"><span data-stu-id="9a140-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="9a140-115">Þessi breyting hefur áhrif á sérhverja smásöluverslun sem er tengd við valdar virkniforstillingar.</span><span class="sxs-lookup"><span data-stu-id="9a140-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="9a140-116">Fylgdu þessum skrefum til að beita stillingunum til POS viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="9a140-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="9a140-117">Farðu í **Retail og Commerce** \> **Upplýsingatækni í Retail og Commerce** \> **Dreifingaráætlun**.</span><span class="sxs-lookup"><span data-stu-id="9a140-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="9a140-118">Keyrðu dreifingaráætlunina **1070** (**Stilling rásar**).</span><span class="sxs-lookup"><span data-stu-id="9a140-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="9a140-119">Azure AD sannvottun krefst internettengingar.</span><span class="sxs-lookup"><span data-stu-id="9a140-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="9a140-120">Það virkar ekki þegar POS er í stillingu án nettengingar.</span><span class="sxs-lookup"><span data-stu-id="9a140-120">It won't work when POS is in offline mode.</span></span>
> 
> <span data-ttu-id="9a140-121">Sem stendur styður aðgerðin **Hnekking stjórnanda** ekki Azure AD sem sannvottunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="9a140-121">Currently, the **Manager override** function doesn't support Azure AD as an authentication method.</span></span> <span data-ttu-id="9a140-122">Krafist er notandakennis og aðgangsorðs jafnvel þótt Azure AD er skilgreint sem sannvottunaraðferðin fyrir innskráningu sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="9a140-122">An operator ID and password are required even if Azure AD is configured as the authentication method for POS sign-in.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="9a140-123">Tengja við Azure AD reikning hjá starfsmanni</span><span class="sxs-lookup"><span data-stu-id="9a140-123">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="9a140-124">Áður en starfsmaður verslunar getur notað Azure AD til að skrá sig inn í POS forritið verður Azure AD-reikningurinn að vera tengdur þeim starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="9a140-124">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="9a140-125">Til að tengja Azure AD-reikning við starfsmann skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="9a140-125">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="9a140-126">Farðu í **Retail og Commerce** \> **Starfsmenn** \> **Starfsfólk**.</span><span class="sxs-lookup"><span data-stu-id="9a140-126">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="9a140-127">Opnaðu upplýsingasíðuna fyrir starfskraft.</span><span class="sxs-lookup"><span data-stu-id="9a140-127">Open the details page for a worker.</span></span>
1. <span data-ttu-id="9a140-128">Í aðgerðarúðunni á flipanum **Commerce** í flokknum **Ytra kenni** skal velja **Tengja fyrirliggjandi kenni**.</span><span class="sxs-lookup"><span data-stu-id="9a140-128">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="9a140-129">Í valmyndinni **Nota fyrirliggjandi ytra kenni** velurðu **Leita með tölvupósti**, slærð inn Azure AD-netfangið og veldu síðan **Leita**.</span><span class="sxs-lookup"><span data-stu-id="9a140-129">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="9a140-130">Veldu Azure AD-reikninginn sem er skilað og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9a140-130">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="9a140-131">Reitirnir **Samheiti**, **UPN** og **Ytra undirkennimerki** á flipanum **Commerce** á upplýsingasíðu starfsmannsins verður fylltur út.</span><span class="sxs-lookup"><span data-stu-id="9a140-131">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

> [!NOTE]
> <span data-ttu-id="9a140-132">Þegar skrá starfsmanns er uppfærð, til dæmis ef nýr Azure AD-reikningur er tengdur við, aðgangsorði er breytt eða aðsetursbók starfsmanns er uppfærð, er mælt með því að keyra dreifingaráætlun **1060** (**Starfsfólk**) til að samstilla nýjustu upplýsingar um starfsfólk við rásina.</span><span class="sxs-lookup"><span data-stu-id="9a140-132">After a worker record is updated, for example if a new Azure AD account is associated, a password is changed, or an employee address book is updated, it’s recommended that you run **1060** (**Staff**) distribution schedule to synchronize the latest staff information to the channel.</span></span> <span data-ttu-id="9a140-133">Þannig getur forrit sölustaðar sótt réttar upplýsingar fyrir sannvottun notanda og athugun heimildar.</span><span class="sxs-lookup"><span data-stu-id="9a140-133">That way, the POS application can fetch the correct data for user authentication and authorization check.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9a140-134">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9a140-134">Additional resources</span></span>

[<span data-ttu-id="9a140-135">Setja upp aukna innskráningarvirkni fyrir MPOS og Cloud POS</span><span class="sxs-lookup"><span data-stu-id="9a140-135">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="9a140-136">Stofna virknireglu fyrir smásölu</span><span class="sxs-lookup"><span data-stu-id="9a140-136">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="9a140-137">Skilgreina starfsmann</span><span class="sxs-lookup"><span data-stu-id="9a140-137">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
