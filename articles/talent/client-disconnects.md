---
title: Talent-biðlari aftengist
description: Þetta efnisatriði útskýrir hvað eigi að gera ef viðskiptamaður aftengist umhverfi sínu og veit ekki hvers vegna.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 885e2d743cd2b01588546327840508f6f7e95958
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518235"
---
# <a name="talent-client-disconnects"></a><span data-ttu-id="e1992-103">Talent-biðlari aftengist</span><span class="sxs-lookup"><span data-stu-id="e1992-103">Talent client disconnects</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e1992-104">**Umhverfisupplýsingar**</span><span class="sxs-lookup"><span data-stu-id="e1992-104">**Environment details**</span></span> 

<span data-ttu-id="e1992-105">Þetta vandamál getur komið upp í öllum umhverfum.</span><span class="sxs-lookup"><span data-stu-id="e1992-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="e1992-106">**Einkenni**</span><span class="sxs-lookup"><span data-stu-id="e1992-106">**Symptom**</span></span> 

<span data-ttu-id="e1992-107">Viðskiptamaður aftengist umhverfi sínu og veit ekki hvers vegna.</span><span class="sxs-lookup"><span data-stu-id="e1992-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="e1992-108">Viðskiptamaður fær eitt af eftirfarandi villuboðum:</span><span class="sxs-lookup"><span data-stu-id="e1992-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="e1992-109">Tengingin hefur rofnað.</span><span class="sxs-lookup"><span data-stu-id="e1992-109">We've lost your connection.</span></span> <span data-ttu-id="e1992-110">Smellið á „Loka“ til að halda áfram vinnu.</span><span class="sxs-lookup"><span data-stu-id="e1992-110">Click Close to continue working.</span></span>
- <span data-ttu-id="e1992-111">Tenging virðist hafa rofnað við netkerfi, smellið á „Reyna aftur“ til að reyna aftur.</span><span class="sxs-lookup"><span data-stu-id="e1992-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="e1992-112">**Rautt flagg**</span><span class="sxs-lookup"><span data-stu-id="e1992-112">**Red flag**</span></span>

<span data-ttu-id="e1992-113">Þetta vandamál kemur oft upp þegar notendur eru á innleiðingarstiginu, þegar þeir eru að bera saman upplýsingar þvert yfir framleiðslu og prófunarumhverfi, og gleyma því að þeir eru flakka frá einni lotu til annarrar.</span><span class="sxs-lookup"><span data-stu-id="e1992-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="e1992-114">Ef notendur eru á þessu stigi eru mestar líkur á þessu vandamáli.</span><span class="sxs-lookup"><span data-stu-id="e1992-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="e1992-115">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="e1992-115">**Issue**</span></span> 

<span data-ttu-id="e1992-116">**Tegundir vafra:** Google Chrome, Internet Explorer og Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e1992-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="e1992-117">Verkvangur Microsoft Dynamics 365 for Talent aftengir notendur þegar tvær mismunandi lotur eru opnar á sama tíma fyrir sama notanda í sömu tegund af vafra.</span><span class="sxs-lookup"><span data-stu-id="e1992-117">The Microsoft Dynamics 365 for Talent platform disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="e1992-118">(Til dæmis er notandi A að skoða bæði umhverfi 1 og umhverfi 2 í Chrome.) Það skiptir ekki máli hvort notendur opni aðra vafraglugga eða aðra flipa.</span><span class="sxs-lookup"><span data-stu-id="e1992-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="e1992-119">Talent aftengir eina af lotunum ef sömu notandaskilríki eru notuð til að skrá sig inn í bæði umhverfi 1 og umhverfi 2 á sama tíma og í sömu tegund af vafra.</span><span class="sxs-lookup"><span data-stu-id="e1992-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Talent disconnects one of the sessions.</span></span>

<span data-ttu-id="e1992-120">**Lausn**</span><span class="sxs-lookup"><span data-stu-id="e1992-120">**Solution**</span></span>

<span data-ttu-id="e1992-121">Gangið úr skugga um að aðeins eitt umhverfi í einu sé opið fyrir tiltekna tegund vafra.</span><span class="sxs-lookup"><span data-stu-id="e1992-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="e1992-122">Notendur geta opnað margar lotur í sama umhverfinu (sem sagt marga flipa í sama vafranum).</span><span class="sxs-lookup"><span data-stu-id="e1992-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="e1992-123">Notendur sem vilja hoppa á milli tveggja umhverfa á sama tíma ættu að opna umhverfin í ólíkum tegundum vafra.</span><span class="sxs-lookup"><span data-stu-id="e1992-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="e1992-124">(Til dæmis getur notandi A skoðað umhverfi 1 í Chrome og umhverfi 2 í Microsoft Edge.)</span><span class="sxs-lookup"><span data-stu-id="e1992-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>
