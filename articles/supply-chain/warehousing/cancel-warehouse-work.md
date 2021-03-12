---
title: Hætta við vinnu í vörugeymslu fyrir meðhöndlun frávika
description: Þetta efnisatriði lýsir virkni Hætta við vinnu sem gerir vöruhússtjórum kleift að meðhöndla lokaða vinnu.
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ae4062401cd5be2371c45642b78bf3708b04f664
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001199"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a><span data-ttu-id="ce146-103">Hætta við vinnu í vörugeymslu fyrir meðhöndlun frávika</span><span class="sxs-lookup"><span data-stu-id="ce146-103">Cancel warehouse work for exception handling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce146-104">Virknin Hætta við vinnu í Microsoft Dynamics 365 Supply Chain Management leyfir stjórnanda að hætta við tiltekna vöruhúsavinnu sem er í gangi en henni er lokað af kerfinu eða ekki hægt að ljúka því vegna sérstakra aðstæðna.</span><span class="sxs-lookup"><span data-stu-id="ce146-104">The Cancel work functionality in Microsoft Dynamics 365 Supply Chain Management lets the admin user cancel specific warehouse work that is currently in progress, but that is blocked by the system or can't be completed because of exceptional circumstances.</span></span> <span data-ttu-id="ce146-105">Þessi virkni er aðlaðandi og öruggur valkostur við SQL leiðréttingarforskriftir sem laga ósamræmd gögn.</span><span class="sxs-lookup"><span data-stu-id="ce146-105">This functionality is an attractive and secure alternative to SQL corrective scripts that fix inconsistent data.</span></span> <span data-ttu-id="ce146-106">En þó að þessara forskrifta sé venjulega krafist af fagfólki í upplýsingatækni, þá geta notendur í fyrirtækinu notað virknina Hætta við vinnu sem hafa stjórnunarréttindi.</span><span class="sxs-lookup"><span data-stu-id="ce146-106">However, whereas these scripts are typically requested from IT professionals, the Cancel work functionality can be used by users in the company who have admin rights.</span></span>

<span data-ttu-id="ce146-107">Þú getur fengið aðgang að virkni Hætta við vinnu í **Vöruhúsastjórnun** \> **Reglubundin verkefni** \> **Hreinsið upp \> Hætt við vinnu**.</span><span class="sxs-lookup"><span data-stu-id="ce146-107">You can access the Cancel work functionality at **Warehouse management** \> **Periodic tasks** \> **Clean up \> Cancel work**.</span></span> <span data-ttu-id="ce146-108">Í valmyndinni **Hætta við vinnu** tilgreinirðu vinnukenni sem á að hætta við og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ce146-108">In the **Cancel work** dialog box, specify the work ID of the work to cancel, and then select **OK**.</span></span>

## <a name="warehouse-work-that-can-be-canceled"></a><span data-ttu-id="ce146-109">Vöruhúsavinnsla sem hægt er að hætta við</span><span class="sxs-lookup"><span data-stu-id="ce146-109">Warehouse work that can be canceled</span></span>

<span data-ttu-id="ce146-110">Meðan á vöruhússaðgerðum stendur gæti starfskraftur lent í aðstæðum þar sem viðkomandi hefur skráð magn sem tiltekið af geymslustað yfir á notendastað sinn, en þá getur viðkomandi ekki skráð söluaðgerðina.</span><span class="sxs-lookup"><span data-stu-id="ce146-110">During warehouse picking operations, a worker might encounter situations where they have registered quantities as picked from a storage location to their user location, but then they can't register the put operation.</span></span> <span data-ttu-id="ce146-111">Ósamræmd gögn um vöruhús eru oft, en ekki alltaf, ástæðan fyrir því að vinna er lokuð.</span><span class="sxs-lookup"><span data-stu-id="ce146-111">Inconsistent warehouse data is often, but not always, the reason why work is blocked.</span></span>

<span data-ttu-id="ce146-112">Ólíkt venjulegri Hætta við virkni sem hægt er að nálgast með því að nota hnappinn **Hætta við** á vinnuhausnum krefst virknin Hætta við vinnu þess ekki að síðasta vinnulínan sé vinnulína af gerðinni **tiltekt**.</span><span class="sxs-lookup"><span data-stu-id="ce146-112">Unlike the regular Cancel functionality that can be accessed by using the **Cancel** button on the work header, the Cancel work functionality doesn't require that the last completed work line be a work line of the **put** type.</span></span> <span data-ttu-id="ce146-113">Með öðrum orðum, fyrir virkni Hætta við vinnu, er hægt að keyra afbókunarrök jafnvel þótt vörumagn á vinnulínu sé á notendastað.</span><span class="sxs-lookup"><span data-stu-id="ce146-113">In other words, for the Cancel work functionality, cancellation logic can be run even if the item quantity on a work line is in a user location.</span></span>

> [!NOTE]
> <span data-ttu-id="ce146-114">Fyrir vinnu sem verður að hætta við af rekstrarástæðum verða notendur vöruhúss að halda áfram að nota venjulegu virknina Hætta við á vinnusíðunni.</span><span class="sxs-lookup"><span data-stu-id="ce146-114">For work that must be canceled for operational reasons, warehouse users must continue to use the regular Cancel functionality on the work page.</span></span>

<span data-ttu-id="ce146-115">Aðeins er hægt að hætta við vinnu af gerðinni **Sala**, **Flutningsútgáfa**, **Tiltekt hráefnis** eða **Áfylling** með því að nota virknina Hætta við vinnu.</span><span class="sxs-lookup"><span data-stu-id="ce146-115">Only work of the **Sales**, **Transfer issue**, **Raw material picking**, or **Replenishment** type can be canceled by using the Cancel work functionality.</span></span> <span data-ttu-id="ce146-116">Afturköllunarrök verða ekki keyrð fyrir frátektarvinnu frysts hráefnis eða vinnu sem hægt er að hætta við með því að nota venjulega Hætta við virkni (sjá fyrri athugasemd).</span><span class="sxs-lookup"><span data-stu-id="ce146-116">Cancellation logic won't be run for frozen raw material picking work or work that can be canceled by using the regular Cancel functionality (see the preceding note).</span></span>

<span data-ttu-id="ce146-117">Til að opna verkið hættir kerfið öllum vinnulínum sem eftir eru og lagfærir vöruhúsgögnin sem eru tengd vinnukenninu sem notandinn tilgreindi.</span><span class="sxs-lookup"><span data-stu-id="ce146-117">To unblock the work, the system cancels any remaining work lines and fixes the warehouse data that is associated with the work ID that the user specified.</span></span> <span data-ttu-id="ce146-118">Allar venjulegar aðgerðir meðhöndlunar í vöruhúsi sem fela í sér vörumagn sem verða fyrir áhrifum geta síðan haldið áfram.</span><span class="sxs-lookup"><span data-stu-id="ce146-118">Any regular warehouse-handling operations that involve the affected item quantity can then resume.</span></span>

<span data-ttu-id="ce146-119">Til að setja vöruna á tiltekinn stað eftir að vinnunni er aflýst, verður notandinn að nota birgðahreyfingu eða magnleiðréttingaraðgerð í fartæki.</span><span class="sxs-lookup"><span data-stu-id="ce146-119">To put the affected item in a specific location after the work is canceled, the user must use an inventory movement or quantity adjustment operation on a mobile device.</span></span>
