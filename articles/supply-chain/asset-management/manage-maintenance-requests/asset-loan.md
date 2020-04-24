---
title: Eignarlán
description: Þetta efni lýsir því hvernig á að skrá lán á eignir í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 07472188051aea7084142cc417c6d725462cf4f9
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205254"
---
# <a name="asset-loans"></a><span data-ttu-id="a6cfa-103">Eignarlán</span><span class="sxs-lookup"><span data-stu-id="a6cfa-103">Asset loans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a6cfa-104">Ef fyrirtæki þitt fær eignir til viðgerðar- eða viðhaldsstarfa frá annaðhvort innri staðsetningu eða viðskiptavinum og ef þú lánar eignir tímabundið til þessara staða eða viðskiptavina getur eignastýring rakið eignalánin.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-104">If your company receives assets for repair or maintenance jobs from either internal locations or customers, and if you temporarily loan assets to those locations or customers, Asset Management can track the asset loans.</span></span>

## <a name="register-asset-loans-on-a-maintenance-request"></a><span data-ttu-id="a6cfa-105">Skráðu eignarlán á viðhaldsbeiðni</span><span class="sxs-lookup"><span data-stu-id="a6cfa-105">Register asset loans on a maintenance request</span></span>

1. <span data-ttu-id="a6cfa-106">Veldu **Eignastýring** \> **Sameiginlegt** \> **Viðhaldsbeiðnir** \> **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-106">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="a6cfa-107">Veldu viðhaldsbeiðni til að skrá eignarlán í og veldu síðan **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-107">Select the maintenance request to register an asset loan on, and then select **Edit**.</span></span>
3. <span data-ttu-id="a6cfa-108">Á síðunni **Beiðni** velurðu **Senda lánseign**.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-108">On the **Request** page, select **Send loan asset**.</span></span>
4. <span data-ttu-id="a6cfa-109">Veldu eignina og sláðu inn áætlaðan skiladag.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-109">Select the asset, and enter the expected return date.</span></span>
5. <span data-ttu-id="a6cfa-110">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-110">Select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="a6cfa-111">Þú getur aðeins sent lánaeign ef eign af sömu eignategund er tiltæk.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-111">You can send a loan asset only if an asset of the same asset type is available.</span></span>
> - <span data-ttu-id="a6cfa-112">Eignin sem þú lánar verður að vera með eignalíftímastöðu sem gerir kleift að hún sé notuð sem lánaeign, svo sem **InStorage**.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-112">The asset that you loan must have an asset lifecycle state that allows it to be used as a loan asset, such as **InStorage**.</span></span> <span data-ttu-id="a6cfa-113">Þegar eignalánið er skráð, er líftímastaða eignarinnar sjálfkrafa uppfærð í t.d. **OnLoan**.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-113">When the asset loan is registered, the asset lifecycle state of the asset is automatically updated to, for example, **OnLoan**.</span></span>

<span data-ttu-id="a6cfa-114">Til að skoða lista yfir allar eignir sem þú hefur lánað til annarra staða eða viðskiptavina skaltu velja **Eignastýring** \> **Sameiginlegt** \> **Eignalán** \> **Öll eignalán**.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-114">To view a list of all the assets that you've loaned to other locations or customers, select **Asset management** \> **Common** \> **Asset loan** \> **All asset loans**.</span></span> <span data-ttu-id="a6cfa-115">Ef gátreiturinn **Klárað** er valinn fyrir eign hefur eignin verið skráð sem skilað til fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-115">If the **Ended** check box is selected for an asset, the asset has been registered as returned to your company.</span></span>

![Vinna með viðhaldsbeiðnir](media/06-manage-maintenance-requests.png)

<span data-ttu-id="a6cfa-117">Á síðunni **Virk eignalán** geturðu skoðað lista yfir allar lánaeignir sem hefur ekki enn verið skilað til fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-117">On the **Active asset loans** page, you can view a list of all the loan assets that haven't yet been returned to your company.</span></span>

## <a name="register-loan-assets-as-returned"></a><span data-ttu-id="a6cfa-118">Skráðu lánaeignir sem skilað er</span><span class="sxs-lookup"><span data-stu-id="a6cfa-118">Register loan assets as returned</span></span>

1. <span data-ttu-id="a6cfa-119">Veldu **Eignastýring** \> **Sameiginlegt** \> **Eignalán** \> **Virk eignalán**.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-119">Select **Asset management** \> **Common** \> **Asset loan** \> **Active asset loans**.</span></span>
2. <span data-ttu-id="a6cfa-120">Veldu eignalánið sem á að skrá sem skilað og veldu síðan **Skila eignaláni**.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-120">Select the asset loan to register as returned, and then select **Return asset loan**.</span></span>
3. <span data-ttu-id="a6cfa-121">Í reitnum **Skilað** skaltu slá inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-121">In the **Returned** field, enter the date and time.</span></span>
4. <span data-ttu-id="a6cfa-122">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-122">Select **OK**.</span></span>
5. <span data-ttu-id="a6cfa-123">Endurnærðu **Virk eignalán** listasíðu og taktu eftir því að eignalánið birtist ekki lengur á listanum.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-123">Refresh the **Active asset loans** list page, and notice that the asset loan no longer appears in the list.</span></span>
