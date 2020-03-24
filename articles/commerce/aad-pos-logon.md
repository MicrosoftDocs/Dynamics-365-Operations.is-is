---
title: Virkja Azure Active Directory sannvottun fyrir POS innskráningu
description: Þetta efni útskýrir hvernig á að stilla innskráningarupplifunina fyrir Microsoft Dynamics 365 Commerce sölustað (POS) þannig að hún noti Azure Active Directory auðkenningu.
author: boycezhu
manager: annbe
ms.date: 03/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: f030e8382627191dd32d855e15432fc85dca4bbd
ms.sourcegitcommit: 1789a78de1cbeac19d96767812df653a191c67e9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/05/2020
ms.locfileid: "3100381"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="6fea8-103">Virkja Azure Active Directory sannvottun fyrir POS innskráningu</span><span class="sxs-lookup"><span data-stu-id="6fea8-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="6fea8-104">Margir viðskiptavinir sem nota Microsoft Dynamics 365 Commerce nota einnig aðra Microsoft-skýjaþjónustu og þeir gætu notað Azure Active Directory (Azure AD) til að stjórna notendaskilríkjum fyrir þessa þjónustu.</span><span class="sxs-lookup"><span data-stu-id="6fea8-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="6fea8-105">Í þeim tilvikum gætu viðskiptavinirnir viljað nota sama Azure AD reikninginn yfir forrit.</span><span class="sxs-lookup"><span data-stu-id="6fea8-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="6fea8-106">Þetta efni útskýrir hvernig á að stilla innskráningarupplifun sölustaðar (POS) í Commerce til að nota Azure AD auðkenningu.</span><span class="sxs-lookup"><span data-stu-id="6fea8-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="6fea8-107">Skilgreina Azure AD sannvottun</span><span class="sxs-lookup"><span data-stu-id="6fea8-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="6fea8-108">Til að gera Azure AD tiltækt sem sannvottunaraðferð fyrir POS innskráningu fyrir verslun, verður þú að skilgreina stillingarnar á virkni sniðs verslunarinnar og nota þær stillingar á POS viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="6fea8-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="6fea8-109">Til að skilgreina virknireglu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="6fea8-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="6fea8-110">Fara í **Retail og Commerce** \> **Uppsetning rásar** \> **Uppsetning sölustaðar** \> **Forstillingar sölustaðar** \> **Virknireglur**.</span><span class="sxs-lookup"><span data-stu-id="6fea8-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="6fea8-111">Veldu virkniregluna sem á að breyta.</span><span class="sxs-lookup"><span data-stu-id="6fea8-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="6fea8-112">Á flýtiflipanum **Aðgerðir**, í hlutanum **Innskráning starfsmanna í POS**, breytirðu gildi í reitnum **Sannvottunaraðferð innskráningar** úr **Persónuskilríki og lykilorð** í **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="6fea8-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="6fea8-113">Sjálfgefið eru allar virknireglur nota **Persónuskilríki og lykilorð** sem POS sannvottunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="6fea8-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="6fea8-114">Þess vegna verður þú að breyta gildi í reitnum **Sannvottunaraðferð innskráningar** ef þú vilt nota Azure AD.</span><span class="sxs-lookup"><span data-stu-id="6fea8-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="6fea8-115">Þessi breyting hefur áhrif á sérhverja smásöluverslun sem er tengd við valdar virkniforstillingar.</span><span class="sxs-lookup"><span data-stu-id="6fea8-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="6fea8-116">Fylgdu þessum skrefum til að beita stillingunum til POS viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="6fea8-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="6fea8-117">Farðu í **Retail og Commerce** \> **Upplýsingatækni í Retail og Commerce** \> **Dreifingaráætlun**.</span><span class="sxs-lookup"><span data-stu-id="6fea8-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="6fea8-118">Keyrðu dreifingaráætlunina **1070** (**Stilling rásar**).</span><span class="sxs-lookup"><span data-stu-id="6fea8-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="6fea8-119">Azure AD sannvottun krefst internettengingar.</span><span class="sxs-lookup"><span data-stu-id="6fea8-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="6fea8-120">Það virkar ekki þegar POS er í stillingu án nettengingar.</span><span class="sxs-lookup"><span data-stu-id="6fea8-120">It won't work when POS is in offline mode.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="6fea8-121">Tengja við Azure AD reikning hjá starfsmanni</span><span class="sxs-lookup"><span data-stu-id="6fea8-121">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="6fea8-122">Áður en starfsmaður verslunar getur notað Azure AD til að skrá sig inn í POS forritið verður Azure AD-reikningurinn að vera tengdur þeim starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="6fea8-122">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="6fea8-123">Til að tengja Azure AD-reikning við starfsmann skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="6fea8-123">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="6fea8-124">Farðu í **Retail og Commerce** \> **Starfsmenn** \> **Starfsfólk**.</span><span class="sxs-lookup"><span data-stu-id="6fea8-124">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="6fea8-125">Opnaðu upplýsingasíðuna fyrir starfskraft.</span><span class="sxs-lookup"><span data-stu-id="6fea8-125">Open the details page for a worker.</span></span>
1. <span data-ttu-id="6fea8-126">Í aðgerðarúðunni á flipanum **Commerce** í flokknum **Ytra kenni** skal velja **Tengja fyrirliggjandi kenni**.</span><span class="sxs-lookup"><span data-stu-id="6fea8-126">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="6fea8-127">Í valmyndinni **Nota fyrirliggjandi ytra kenni** velurðu **Leita með tölvupósti**, slærð inn Azure AD-netfangið og veldu síðan **Leita**.</span><span class="sxs-lookup"><span data-stu-id="6fea8-127">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="6fea8-128">Veldu Azure AD-reikninginn sem er skilað og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6fea8-128">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="6fea8-129">Reitirnir **Samheiti**, **UPN** og **Ytra undirkennimerki** á flipanum **Commerce** á upplýsingasíðu starfsmannsins verður fylltur út.</span><span class="sxs-lookup"><span data-stu-id="6fea8-129">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6fea8-130">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6fea8-130">Additional resources</span></span>

[<span data-ttu-id="6fea8-131">Setja upp aukna innskráningarvirkni fyrir MPOS og sölukerfi í skýinu</span><span class="sxs-lookup"><span data-stu-id="6fea8-131">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="6fea8-132">Stofna virknireglu fyrir smásölu</span><span class="sxs-lookup"><span data-stu-id="6fea8-132">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="6fea8-133">Skilgreina starfsmann</span><span class="sxs-lookup"><span data-stu-id="6fea8-133">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
