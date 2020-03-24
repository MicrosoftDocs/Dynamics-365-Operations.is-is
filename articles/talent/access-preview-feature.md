---
title: Vinna með eiginleika
description: Þetta efnisatriði lýsir því hvernig stjórnandi getur virkjað forskoðunareiginleika í Microsoft Dynamics 365 Talent og listar þá eiginleika sem eru nú þegar virkjaðir fyrir forskoðun.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.1.0, Talent
ms.openlocfilehash: d818e9e04ce88e5ab285ef8176334809447fb477
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124797"
---
# <a name="manage-features"></a><span data-ttu-id="b40c3-103">Vinna með eiginleika</span><span class="sxs-lookup"><span data-stu-id="b40c3-103">Manage features</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b40c3-104">Sem hluti af samfelldri kynningu okkar á afkastagetu mannauðsstjórnunar fyrir Microsoft Dynamics 365 Human Resources, viljum við að viðskiptavinir upplifi nýja eiginleika eins fljótt og auðið er.</span><span class="sxs-lookup"><span data-stu-id="b40c3-104">As part of our continuous rollout of human capital management (HCM) capabilities for Microsoft Dynamics 365 Human Resources, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="b40c3-105">Stjórnendur geta séð og notað forskoðunareiginleika í umhverfi sínu.</span><span class="sxs-lookup"><span data-stu-id="b40c3-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="b40c3-106">Þessar eiginleikar eru næstum tilbúnir til almenns framboðs og hafa farið í gegnum víðtækar prófanir.</span><span class="sxs-lookup"><span data-stu-id="b40c3-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="b40c3-107">Við erum bara að falast eftir lokaumsögnum viðskiptavina og fullgildingu áður en við gefum þá út fyrir almenning.</span><span class="sxs-lookup"><span data-stu-id="b40c3-107">We're just looking for a final round of customer feedback and validation before we release them for general availability.</span></span>

<span data-ttu-id="b40c3-108">Þetta efnisatriði lýsir því hvernig hægt er að virkja forskoðunareiginleika og lista þá eiginleika sem eru nú þegar tiltækir fyrir forskoðun.</span><span class="sxs-lookup"><span data-stu-id="b40c3-108">This topic describes how you can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="b40c3-109">Þessi listi verður uppfærð þegar eiginleikar eru gefnar út til almenns framboðs og þegar nýjar eiginleikar eru gefnar út til forskoðunar.</span><span class="sxs-lookup"><span data-stu-id="b40c3-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="b40c3-110">Engin tilkynning er send þegar nýjar eiginleikar eru gefin út til forskoðunar.</span><span class="sxs-lookup"><span data-stu-id="b40c3-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="b40c3-111">Notendur munu bara byrja að sjá eiginleikana.</span><span class="sxs-lookup"><span data-stu-id="b40c3-111">Users will just start to see the features.</span></span> <span data-ttu-id="b40c3-112">Frekari upplýsingar um nýja eiginleika í Talent er að finna í [Nýjungar eða breytingar í Dynamics 365 Talent](./whats-new.md) og [Dynamics 365 og Power Platform útgáfuupplýsingar](https://docs.microsoft.com/business-applications-release-notes).</span><span class="sxs-lookup"><span data-stu-id="b40c3-112">For more information about new features in Talent, see [What's new or changed in Dynamics 365 Talent](./whats-new.md) and [Dynamics 365 and Power Platform Release Notes](https://docs.microsoft.com/business-applications-release-notes).</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="b40c3-113">Virkja eða slökkva á forskoðunareiginleikum</span><span class="sxs-lookup"><span data-stu-id="b40c3-113">Enable or disable preview features</span></span>

<span data-ttu-id="b40c3-114">Til að fá aðgang að forskoðunareiginleikum þarf fyrst að virkja þá í umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="b40c3-114">To access preview features, you must first enable them in your environment.</span></span> <span data-ttu-id="b40c3-115">Að kveikja eða slökkva á forskoðunareiginleikum fer eftir hverju umhverfi fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="b40c3-115">Enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b40c3-116">Þegar kveikt er á stillingunni **Forskoðunareiginleikar** virkjast forskoðunareiginleikar fyrir alla notendur í fyrirtækinu þínu sem eru í því umhverfi.</span><span class="sxs-lookup"><span data-stu-id="b40c3-116">When you turn on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="b40c3-117">Þegar slökkt er á stillingunni, gerirðu forskoðunareiginleika óvirka og óaðgengilega fyrir notendur þína.</span><span class="sxs-lookup"><span data-stu-id="b40c3-117">When you turn off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="b40c3-118">Forskoðunareiginleikar hafa takmarkaðan stuðning í Talent.</span><span class="sxs-lookup"><span data-stu-id="b40c3-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="b40c3-119">Þeir gætu notað færri persónuverndar- og öryggisráðstafanir og þær eru ekki innifalin í þjónustustigssamningi Talent (SLA).</span><span class="sxs-lookup"><span data-stu-id="b40c3-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement (SLA).</span></span> <span data-ttu-id="b40c3-120">Þú ættir ekki að nota forskoðunareiginleika til að vinna úr persónulegum gögnum (það er, einhverjum upplýsingum sem þú þekkist á) eða að vinna úr öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi.</span><span class="sxs-lookup"><span data-stu-id="b40c3-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="attract"></a><span data-ttu-id="b40c3-121">Attract</span><span class="sxs-lookup"><span data-stu-id="b40c3-121">Attract</span></span>

1. <span data-ttu-id="b40c3-122">Skrá inn á Microsoft Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="b40c3-122">Sign in to Microsoft Dynamics 365 Talent: Attract.</span></span>
2. <span data-ttu-id="b40c3-123">Í **Uppsetning** valmyndinni (táknið fyrir gír) efst í hægra horninu skaltu velja **Stjórnstöð**.</span><span class="sxs-lookup"><span data-stu-id="b40c3-123">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span>
3. <span data-ttu-id="b40c3-124">Í flipanum **Eiginleikastjórnun** skal velja valkostinn við hliðina á **Forskoðunareiginleikar** þannig að hann verður blár og það segir **Kveikt**.</span><span class="sxs-lookup"><span data-stu-id="b40c3-124">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue and says **On**.</span></span>

    ![Virkja forskoðunareiginleika í Attract](./media/attract-enable-preview-features.png)

4. <span data-ttu-id="b40c3-126">Veldu eða hættu við val á einstökum forskoðunareiginleikum.</span><span class="sxs-lookup"><span data-stu-id="b40c3-126">Select or cancel the selection of individual preview features.</span></span> <span data-ttu-id="b40c3-127">Ef þú gerir ekkert eru allir forskoðunareiginleikar virkjaðir.</span><span class="sxs-lookup"><span data-stu-id="b40c3-127">If you do nothing, all available preview features are enabled.</span></span>
5. <span data-ttu-id="b40c3-128">Endurræstu vafrann þinn til að byrja að sjá nýja eiginleikana.</span><span class="sxs-lookup"><span data-stu-id="b40c3-128">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="b40c3-129">Allir notendur sem eru þegar skráðir inn munu sjá eiginleikana næst þegar þeir skrá sig inn, eða þeir geta endurræst vafrann til að sjá eiginleikana strax.</span><span class="sxs-lookup"><span data-stu-id="b40c3-129">Any users who are already signed in will see the features the next time they sign in, or they can refresh their browser to see the features immediately.</span></span>

> [!NOTE]
> <span data-ttu-id="b40c3-130">Sumir forskoðunareiginleikar gætu þurft ítarlegri grunnstillingu.</span><span class="sxs-lookup"><span data-stu-id="b40c3-130">Some preview features might require additional configuration.</span></span> <span data-ttu-id="b40c3-131">Fylgdu tenglunum við hliðina á forskoðunareiginleika til að ljúka uppsetningu hans.</span><span class="sxs-lookup"><span data-stu-id="b40c3-131">Follow the links next to the preview feature to complete the setup for it.</span></span>

## <a name="feedback"></a><span data-ttu-id="b40c3-132">Ábendingar</span><span class="sxs-lookup"><span data-stu-id="b40c3-132">Feedback</span></span>

<span data-ttu-id="b40c3-133">Við viljum heyra um reynslu þína á einhverjum þessara forskoðunareiginleika.</span><span class="sxs-lookup"><span data-stu-id="b40c3-133">We want to hear from you about your experience with any of these preview features.</span></span> <span data-ttu-id="b40c3-134">Við hvetjum þig til að senda reglulega viðbrögð þín á eftirfarandi vefsvæði þegar þú notar þessar eða einhverjar aðrar eiginleika:</span><span class="sxs-lookup"><span data-stu-id="b40c3-134">We encourage you to regularly post your feedback on the following sites as you use these or any other features:</span></span>

- <span data-ttu-id="b40c3-135">[Samfélag](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – Þessi síða er frábær auðlind þar sem notendur geta rætt um notkunartilfelli, spyrja spurninga og fá samfélagsaðstoð.</span><span class="sxs-lookup"><span data-stu-id="b40c3-135">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="b40c3-136">Láttu okkur vita af eiginleikum sem þú vilt sjá í vörunni eða breytingum sem þér finnst eiga að gera á núverandi eiginleikum.</span><span class="sxs-lookup"><span data-stu-id="b40c3-136">Let us know about features that you want to see in the product, or let us know about any changes you think we should make to existing features.</span></span> <span data-ttu-id="b40c3-137">Stinga upp á hugmyndum um vöru á eftirfarandi síðum:</span><span class="sxs-lookup"><span data-stu-id="b40c3-137">Suggest product ideas on the following sites:</span></span>

    - [<span data-ttu-id="b40c3-138">Hugmyndir um Attract</span><span class="sxs-lookup"><span data-stu-id="b40c3-138">Attract ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="b40c3-139">Hugmyndir um Onboard</span><span class="sxs-lookup"><span data-stu-id="b40c3-139">Onboard ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

<span data-ttu-id="b40c3-140">Gakktu úr skugga um að persónuupplýsingar (allar upplýsingar sem þú gætir þekkst á) fylgi ekki með í athugasemdum þínum eða umsögnum um vörur.</span><span class="sxs-lookup"><span data-stu-id="b40c3-140">Make sure that you don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="b40c3-141">Samansafnaðar upplýsingar kunna að vera greindar frekar og verða ekki notaðar til að svara beiðnum samkvæmt gildandi lögum um persónuvernd.</span><span class="sxs-lookup"><span data-stu-id="b40c3-141">Collected information might be analyzed further and isn't used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="b40c3-142">Persónuleg gögn sem er safnað sérstaklega með þessum forritum er háð [Yfirlýsing Microsoft um persónuvernd](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="b40c3-142">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="b40c3-143">Vistaðu slóðina á þetta efnisatriði og skoðaðu oft aftur til að halda þér upplýstri/upplýstum um nýjar forskoðunareiginleikar þegar við gefum þá út.</span><span class="sxs-lookup"><span data-stu-id="b40c3-143">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>

## <a name="see-also"></a><span data-ttu-id="b40c3-144">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="b40c3-144">See also</span></span>

- [<span data-ttu-id="b40c3-145">Prófaðu eða keyptu Talent-forrit</span><span class="sxs-lookup"><span data-stu-id="b40c3-145">Try or buy Talent apps</span></span>](https://dynamics.microsoft.com/talent/overview/)
- [<span data-ttu-id="b40c3-146">Nýjungar eða breytingar í Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="b40c3-146">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="b40c3-147">Útgáfuáætlanir</span><span class="sxs-lookup"><span data-stu-id="b40c3-147">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="b40c3-148">Fá aðstoð fyrir Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="b40c3-148">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
