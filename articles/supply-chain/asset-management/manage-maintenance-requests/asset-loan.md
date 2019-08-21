---
title: Eignarlán
description: Þetta efni lýsir því hvernig á að skrá lán á eignir í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8680241b1300aceda3280893982a1eff3d2e09e0
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847483"
---
# <a name="asset-loans"></a><span data-ttu-id="aff33-103">Eignarlán</span><span class="sxs-lookup"><span data-stu-id="aff33-103">Asset loans</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="aff33-104">Ef fyrirtæki þitt fær eignir til viðgerðar- eða viðhaldsstarfa frá annaðhvort innri staðsetningu eða viðskiptavinum og ef þú lánar eignir tímabundið til þessara staða eða viðskiptavina getur eignastýring rakið eignalánin.</span><span class="sxs-lookup"><span data-stu-id="aff33-104">If your company receives assets for repair or maintenance jobs from either internal locations or customers, and if you temporarily loan assets to those locations or customers, Asset Management can track the asset loans.</span></span>

## <a name="register-asset-loans-on-a-maintenance-request"></a><span data-ttu-id="aff33-105">Skráðu eignarlán á viðhaldsbeiðni</span><span class="sxs-lookup"><span data-stu-id="aff33-105">Register asset loans on a maintenance request</span></span>

1. <span data-ttu-id="aff33-106">Veldu **Eignastýring** \> **Sameiginlegt** \> **Viðhaldsbeiðnir** \> **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="aff33-106">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="aff33-107">Veldu viðhaldsbeiðni til að skrá eignarlán í og veldu síðan **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="aff33-107">Select the maintenance request to register an asset loan on, and then select **Edit**.</span></span>
3. <span data-ttu-id="aff33-108">Á síðunni **Beiðni** velurðu **Senda lánseign**.</span><span class="sxs-lookup"><span data-stu-id="aff33-108">On the **Request** page, select **Send loan asset**.</span></span>
4. <span data-ttu-id="aff33-109">Veldu eignina og sláðu inn áætlaðan skiladag.</span><span class="sxs-lookup"><span data-stu-id="aff33-109">Select the asset, and enter the expected return date.</span></span>
5. <span data-ttu-id="aff33-110">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="aff33-110">Select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="aff33-111">Þú getur aðeins sent lánaeign ef eign af sömu eignategund er tiltæk.</span><span class="sxs-lookup"><span data-stu-id="aff33-111">You can send a loan asset only if an asset of the same asset type is available.</span></span>
> - <span data-ttu-id="aff33-112">Eignin sem þú lánar verður að vera með eignalíftímastöðu sem gerir kleift að hún sé notuð sem lánaeign, svo sem **InStorage**.</span><span class="sxs-lookup"><span data-stu-id="aff33-112">The asset that you loan must have an asset lifecycle state that allows it to be used as a loan asset, such as **InStorage**.</span></span> <span data-ttu-id="aff33-113">Þegar eignalánið er skráð, er líftímastaða eignarinnar sjálfkrafa uppfærð í t.d. **OnLoan**.</span><span class="sxs-lookup"><span data-stu-id="aff33-113">When the asset loan is registered, the asset lifecycle state of the asset is automatically updated to, for example, **OnLoan**.</span></span>

<span data-ttu-id="aff33-114">Til að skoða lista yfir allar eignir sem þú hefur lánað til annarra staða eða viðskiptavina skaltu velja **Eignastýring** \> **Sameiginlegt** \> **Eignalán** \> **Öll eignalán**.</span><span class="sxs-lookup"><span data-stu-id="aff33-114">To view a list of all the assets that you've loaned to other locations or customers, select **Asset management** \> **Common** \> **Asset loan** \> **All asset loans**.</span></span> <span data-ttu-id="aff33-115">Ef gátreiturinn **Klárað** er valinn fyrir eign hefur eignin verið skráð sem skilað til fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="aff33-115">If the **Ended** check box is selected for an asset, the asset has been registered as returned to your company.</span></span>

![Mynd 1](media/06-manage-maintenance-requests.png)

<span data-ttu-id="aff33-117">Á síðunni **Virk eignalán** geturðu skoðað lista yfir allar lánaeignir sem hefur ekki enn verið skilað til fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="aff33-117">On the **Active asset loans** page, you can view a list of all the loan assets that haven't yet been returned to your company.</span></span>

## <a name="register-loan-assets-as-returned"></a><span data-ttu-id="aff33-118">Skráðu lánaeignir sem skilað er</span><span class="sxs-lookup"><span data-stu-id="aff33-118">Register loan assets as returned</span></span>

1. <span data-ttu-id="aff33-119">Veldu **Eignastýring** \> **Sameiginlegt** \> **Eignalán** \> **Virk eignalán**.</span><span class="sxs-lookup"><span data-stu-id="aff33-119">Select **Asset management** \> **Common** \> **Asset loan** \> **Active asset loans**.</span></span>
2. <span data-ttu-id="aff33-120">Veldu eignalánið sem á að skrá sem skilað og veldu síðan **Skila eignaláni**.</span><span class="sxs-lookup"><span data-stu-id="aff33-120">Select the asset loan to register as returned, and then select **Return asset loan**.</span></span>
3. <span data-ttu-id="aff33-121">Í reitnum **Skilað** skaltu slá inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="aff33-121">In the **Returned** field, enter the date and time.</span></span>
4. <span data-ttu-id="aff33-122">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="aff33-122">Select **OK**.</span></span>
5. <span data-ttu-id="aff33-123">Endurnærðu **Virk eignalán** listasíðu og taktu eftir því að eignalánið birtist ekki lengur á listanum.</span><span class="sxs-lookup"><span data-stu-id="aff33-123">Refresh the **Active asset loans** list page, and notice that the asset loan no longer appears in the list.</span></span>
