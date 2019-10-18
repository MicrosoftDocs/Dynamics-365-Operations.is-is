---
title: Skilgreindu tölvupóststillingar í Microsoft Dynamics 365 Talent - Attract
description: Þetta efni útskýrir hvernig á að skilgreina stillingar fyrir tölvupóst sem er sendur af Microsoft Dynamcis 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c891a36f01d36774bd921475fa5995d207cd2d51
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008663"
---
# <a name="configure-email-settings"></a><span data-ttu-id="c94a1-103">Skilgreina tölvupóststillingar</span><span class="sxs-lookup"><span data-stu-id="c94a1-103">Configure email settings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c94a1-104">Vörumerki þitt kemur á trausti og hjálpar þér að byggja upp samband við umsækjendur áður en þeir sækja um stöður hjá þér.</span><span class="sxs-lookup"><span data-stu-id="c94a1-104">Your brand establishes trust and helps you build a relationship with candidates before they even apply for your positions.</span></span> <span data-ttu-id="c94a1-105">Jákvæð upplifun á vörumerki laðar hæfileikaríkt fólk að og eykur hollustu núverandi starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="c94a1-105">Positive brand perception attracts top talent and increases the loyalty of existing employees.</span></span> <span data-ttu-id="c94a1-106">Microsoft Dynamics 365 Talent: Attract gerir þér kleift að skilgreina tölvupóst svo að hann endurspegli vörumerki fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="c94a1-106">Microsoft Dynamics 365 Talent: Attract lets you configure emails so that they reflect your company's brand.</span></span> <span data-ttu-id="c94a1-107">Þess vegna er hægt að veita samræmda upplifun starfsumsækjenda þegar þeir fara fram í gegnum umsóknarferlið.</span><span class="sxs-lookup"><span data-stu-id="c94a1-107">Therefore, you can provide a consistent experience to job candidates as they progress through the application process.</span></span>

<span data-ttu-id="c94a1-108">Attract gerir þér kleift að framkvæma þessar aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="c94a1-108">Attract lets you perform these actions:</span></span>

- <span data-ttu-id="c94a1-109">Skilgreindu tölvupóststillingar þannig að fyrirtækjareikningur hjá tölvupóstþjónustu Microsoft Exchange sé notaður.</span><span class="sxs-lookup"><span data-stu-id="c94a1-109">Configure email settings so that your company's Microsoft Exchange email service account is used.</span></span> <span data-ttu-id="c94a1-110">Þannig vita umsækjendur að tölvupósturinn kemur frá fyrirtækinu þínu.</span><span class="sxs-lookup"><span data-stu-id="c94a1-110">In this way, candidates know that the emails are coming from your company.</span></span> <span data-ttu-id="c94a1-111">Til dæmis geturðu skilgreint stillingarnar þannig að umsækjendur fá tölvupósta frá `recruiting@contoso.com` í staðinn fyrir `contoso@microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="c94a1-111">For example, you can configure your settings so that candidates receive emails from `recruiting@contoso.com` instead of `contoso@microsoft.com`.</span></span>
- <span data-ttu-id="c94a1-112">Búðu til samræmd vörumerki fyrir öll tölvupóstssamskipti þín með því að setja altæka hausinn og fótinn fyrir tölvupóstsniðmát.</span><span class="sxs-lookup"><span data-stu-id="c94a1-112">Create consistent branding for all your email communications by setting a global header and footer for email templates.</span></span> 

> [!NOTE]
> <span data-ttu-id="c94a1-113">Til að skilgreina Attract þannig að það noti fyrirtækjareikning tölvupóstþjónustunnar til að senda tölvupóst þarftu að nota viðbótina Alhliða ráðningar.</span><span class="sxs-lookup"><span data-stu-id="c94a1-113">To configure Attract so that it uses your company's email service account to send email, you need the Comprehensive hiring add-on.</span></span>

## <a name="connect-an-email-service-account"></a><span data-ttu-id="c94a1-114">Tengja tölvupóstþjónustureikning</span><span class="sxs-lookup"><span data-stu-id="c94a1-114">Connect an email service account</span></span>

<span data-ttu-id="c94a1-115">Með því að tengja tölvupóstþjónustureikning við fyrirtækið þitt geturðu búið til vörumerkta tölvupóstupplifun fyrir starfsumsækjendur.</span><span class="sxs-lookup"><span data-stu-id="c94a1-115">By connecting your company's email service account, you can create a branded email experience for your job candidates.</span></span> <span data-ttu-id="c94a1-116">Ef þú tengir fyrirtækjareikninginn þinn ekki notar Attract sjálfgefna tölvupóstsþjónustu Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c94a1-116">If you don't connect your company account, Attract uses the default Microsoft-branded email service account.</span></span>

1. <span data-ttu-id="c94a1-117">Veldu **Stillingar** (gírtáknið efst í hægra horni síðunnar) og veldu síðan **Stjórnandamiðstöð**.</span><span class="sxs-lookup"><span data-stu-id="c94a1-117">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="c94a1-118">Á flipanum **Tölvupóstsstillingar**, undir **Tölvupóstsþjónustureikningar**, skaltu velja **Tengja fyrirtækjareikning**.</span><span class="sxs-lookup"><span data-stu-id="c94a1-118">On the **Email settings** tab, under **Email service accounts**, select **Connect a company account**.</span></span>

    ![Tengi póstþjónustu fyrirtækisins í Attract](./media/attract-admin-email-service-accounts.png)

    <span data-ttu-id="c94a1-120">Nánari upplýsingar um hvernig á að búa til sameiginlegan tölvupóstreikning er að finna í [Sameiginlegum pósthólfum í Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="c94a1-120">For more information about how to create a shared email account, see [Shared mailboxes in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span></span>

3. <span data-ttu-id="c94a1-121">Í innskráningarglugganum í Microsoft skaltu skrá þig inn með því að nota persónuskilríki fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="c94a1-121">In the Microsoft sign-in window, sign in by using your corporate credentials.</span></span>
4. <span data-ttu-id="c94a1-122">Ef þú hefur ekki enn sett upp þjónustureikning fyrir tölvupóst eða ef þú vilt bæta nýjum við skaltu velja **Bæta við nýjum þjónustureikningi** og slá síðan netfangið þitt inn.</span><span class="sxs-lookup"><span data-stu-id="c94a1-122">If you haven't yet set up an email service account, or if you want to add a new one, select **Add new service account**, and then enter your email information.</span></span> <span data-ttu-id="c94a1-123">Ef þú hefur þegar sett upp þjónustureikning fyrir tölvupóst sem þú vilt nota skaltu velja hann.</span><span class="sxs-lookup"><span data-stu-id="c94a1-123">If you've already set up the email service account that you want to use, select it.</span></span>

<span data-ttu-id="c94a1-124">Þegar póstþjónustureikningurinn þinn hefur verið skilgreindur sérðu hann skráðan undir **Póstþjónustureikningar**.</span><span class="sxs-lookup"><span data-stu-id="c94a1-124">When your email service account is successfully configured, you will see it listed under **Email service accounts**.</span></span>

## <a name="disconnect-an-email-service-account"></a><span data-ttu-id="c94a1-125">Aftengja póstþjónustureikning</span><span class="sxs-lookup"><span data-stu-id="c94a1-125">Disconnect an email service account</span></span>

<span data-ttu-id="c94a1-126">Ef þú vilt hætta að nota lén fyrirtækisins í tölvupóstsamskiptum gegnum Attract er hægt að aftengja póstþjónustureikning.</span><span class="sxs-lookup"><span data-stu-id="c94a1-126">If you want to stop using your company's domain in email communications through Attract, you can disconnect an email service account.</span></span>

1. <span data-ttu-id="c94a1-127">Veldu **Stillingar** (gírtáknið efst í hægra horni síðunnar) og veldu síðan **Stjórnandamiðstöð**.</span><span class="sxs-lookup"><span data-stu-id="c94a1-127">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="c94a1-128">Á flipanum **Tölvupóststillingar**, undir **Póstþjónustureikningar**, skaltu velja hnappinn **Meira** (þrír lóðréttir punktar) við hliðina á póstþjónustureikningnum sem þú vilt aftengja.</span><span class="sxs-lookup"><span data-stu-id="c94a1-128">On the **Email settings** tab, under **Email service accounts**, select the **More** button (three vertical dots) next to the email service account that you want to disconnect.</span></span>
3. <span data-ttu-id="c94a1-129">Veldu **Aftengja tölvupóstreikning**.</span><span class="sxs-lookup"><span data-stu-id="c94a1-129">Select **Disconnect email account**.</span></span>

    ![Aftengi póstþjónustureikning fyrirtækisins](./media/attract-admin-disconnect-email-account.png)

4. <span data-ttu-id="c94a1-131">Þegar þú færð kvaðningu um að staðfesta aðgerðina skaltu velja **Aftengja**.</span><span class="sxs-lookup"><span data-stu-id="c94a1-131">When you're prompted to confirm the operation, select **Disconnect**.</span></span>

    ![Staðfesti aftengingu á póstþjónustureikningi fyrirtækisins](./media/attract-admin-email-confirm-disconnect.png)

<span data-ttu-id="c94a1-133">Ef þú tengir ekki annan tölvupóstþjónustureikning munu tölvupóstar sem eru sendir úr Attract nota sjálfgefinn tölvupóstreikning fyrir Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c94a1-133">If you don't connect a different email service account, emails that are sent from Attract will use the default Microsoft-branded email service account.</span></span>

## <a name="configure-email-template-settings"></a><span data-ttu-id="c94a1-134">Sskilgreindu sniðmátsstillingar tölvupósts</span><span class="sxs-lookup"><span data-stu-id="c94a1-134">Configure email template settings</span></span>

<span data-ttu-id="c94a1-135">Þú getur hlaðið inn mynd af merki fyrirtækisins og öðrum upplýsingum sem vörumerkjahaus fyrir tölvupóstinn þinn.</span><span class="sxs-lookup"><span data-stu-id="c94a1-135">You can upload an image of your company's logo and other information as a branded header for your emails.</span></span> <span data-ttu-id="c94a1-136">Þú getur einnig veitt tengla á persónuverndarstefnu og notkunarskilmála í síðufæti í tölvupósti.</span><span class="sxs-lookup"><span data-stu-id="c94a1-136">You can also provide links to your privacy policy and terms of use in email footers.</span></span>

> [!NOTE]
> <span data-ttu-id="c94a1-137">Þú verður að fylgja öllum gildandi lögum í landi þínu eða landsvæði og einnig þess lands eða landsvæðis sem gilda um viðtakanda tölvupóstsins.</span><span class="sxs-lookup"><span data-stu-id="c94a1-137">You must comply with all applicable laws of your country or region, and also the country or region that governs the email recipient.</span></span> <span data-ttu-id="c94a1-138">Þessi lög fela í sér reglur um ruslpóst.</span><span class="sxs-lookup"><span data-stu-id="c94a1-138">These laws include anti-spam regulations.</span></span>

1. <span data-ttu-id="c94a1-139">Veldu **Stillingar** (gírtáknið efst í hægra horni síðunnar) og veldu síðan **Stjórnandamiðstöð**.</span><span class="sxs-lookup"><span data-stu-id="c94a1-139">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="c94a1-140">Á flipanum **Tölvupóststillingar** undir **Stillingar fyrir sniðmát tölvupósts** skaltu draga myndina sem þú vilt nota sem tölvupósthaus inn í myndareitinn eða smella í myndareitinn til að leita að skránni.</span><span class="sxs-lookup"><span data-stu-id="c94a1-140">On the **Email settings** tab, under **Email template settings**, drag the image that you want to use as your email header into the image box, or click in the image box to browse for the file.</span></span> <span data-ttu-id="c94a1-141">Til að skipta um núverandi mynd verðurðu fyrst að velja **Fjarlægja** við hliðina á henni.</span><span class="sxs-lookup"><span data-stu-id="c94a1-141">To replace an existing image, you must first select **Remove** next to it.</span></span> <span data-ttu-id="c94a1-142">Myndin verður að vera JPEG, JPG, PNG eða SVG-skrá.</span><span class="sxs-lookup"><span data-stu-id="c94a1-142">The image must be a JPEG, JPG, PNG, or SVG file.</span></span> <span data-ttu-id="c94a1-143">Ráðlögð myndastærð er á milli 25 og 800 dílar á breidd og á bilinu 25 til 150 dílar á hæð.</span><span class="sxs-lookup"><span data-stu-id="c94a1-143">The recommended size for images is between 25 and 800 pixels wide, and between 25 and 150 pixels high.</span></span> <span data-ttu-id="c94a1-144">Hámarksskráarstærð fyrir hausinn er 1 megabæti (MB).</span><span class="sxs-lookup"><span data-stu-id="c94a1-144">The maximum file size for the header is 1 megabyte (MB).</span></span>

    ![Bætir við mynd fyrir tölvupósthöfuð fyrirtækisins](./media/attract-admin-email-header.png)

3. <span data-ttu-id="c94a1-146">Undir **Persónuverndarstefna vegna samskipta** gefurðu upp tengil á persónuverndarstefnu fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="c94a1-146">Under **Your Privacy policy for communications**, provide a link to your company's privacy policy.</span></span> <span data-ttu-id="c94a1-147">Undir **Skilmálar vegna samskipta** gefurðu upp tengil á notkunarskilmála fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="c94a1-147">Under **Your Terms and conditions for communication**, provide a link to your company's terms of use.</span></span>

    ![Bætir tenglum við persónuverndarstefnu fyrirtækisins og notkunarskilmála fyrir síðufót í tölvupósti](./media/attract-admin-email-footer.png)

4. <span data-ttu-id="c94a1-149">Veldu **Vista** til að vista stillingar tölvupóstsniðmátsins.</span><span class="sxs-lookup"><span data-stu-id="c94a1-149">Select **Save** to save your email template settings.</span></span>
