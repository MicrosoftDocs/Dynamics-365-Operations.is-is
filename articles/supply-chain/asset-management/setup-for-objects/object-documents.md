---
title: Eignaskjöl
description: Þetta efni skýrir eignaskjöl í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectDocument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f8bcae99a96ccd83dc4543b1c56007a4263a19b
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021680"
---
# <a name="asset-documents"></a><span data-ttu-id="6a742-103">Eignaskjöl</span><span class="sxs-lookup"><span data-stu-id="6a742-103">Asset documents</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6a742-104">Þetta efni skýrir eignaskjöl í eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="6a742-104">This topic explains asset documents in Asset Management.</span></span>

<span data-ttu-id="6a742-105">Í eignastýringu geturðu sett upp skjöl þannig að þau tengjast sjálfkrafa starfstegundum, eignaframleiðendum, eignategundum eða eignum til dæmis.</span><span class="sxs-lookup"><span data-stu-id="6a742-105">In Asset Management, you can set up documents so that they are automatically related to job types, asset manufacturers, asset types, or assets, for example.</span></span> <span data-ttu-id="6a742-106">Þessi virkni er gagnleg þegar uppfærðar útgáfur skjala eru gefnar út.</span><span class="sxs-lookup"><span data-stu-id="6a742-106">This functionality is useful when updated document versions are released.</span></span> <span data-ttu-id="6a742-107">Í því tilfelli þarftu bara að setja uppfærða skjalið á staðalstaðinn sem þú notar fyrir þig Supplu Chain Management skjöl og hengdu skjalið við eignaskjalaskrána sem þú hefur búið til.</span><span class="sxs-lookup"><span data-stu-id="6a742-107">In that case, you just have to put the updated document in the standard location that you use for your Supply Chain Management documents, and attach the document to the asset document record that you've created.</span></span> <span data-ttu-id="6a742-108">Síðan er hægt að nálgast uppfærða skjalið frá **Allar eignir**, **Virkar eignir**, **Virku eignir mínar**, **Allar vinnupantanir**, og **Virk störf til pöntunar** valmyndaratriðin.</span><span class="sxs-lookup"><span data-stu-id="6a742-108">The updated document can then be accessed from the **All assets**, **Active assets**, **My active assets**, **All work orders**, and **Active work order jobs** menu items.</span></span> <span data-ttu-id="6a742-109">Ferlið til að hengja skjöl við eignaskjalaskrá notar staðlaða skjal meðhöndlunarkerfisins.</span><span class="sxs-lookup"><span data-stu-id="6a742-109">The process for attaching documents to an asset document record uses the standard document handling system.</span></span>

<span data-ttu-id="6a742-110">**Dæmi 1:** Skjal sem tengist starfstegund gæti lýst verklagi fyrir þá starfstegund.</span><span class="sxs-lookup"><span data-stu-id="6a742-110">**Example 1:** A document that is related to a job type might describe a procedure for that job type.</span></span>

<span data-ttu-id="6a742-111">**Dæmi 2:** Skjal sem er tengt samsetningu eignategundar, framleiðanda og líkans gæti verið staðlaða handbók fyrir valið líkan eignaframleiðanda.</span><span class="sxs-lookup"><span data-stu-id="6a742-111">**Example 2:** A document that is related to a combination of an asset type, manufacturer, and model might be the standard manual for the selected asset manufacturer model.</span></span>

## <a name="create-asset-document-relation"></a><span data-ttu-id="6a742-112">Stofna tengsl eignaskjals</span><span class="sxs-lookup"><span data-stu-id="6a742-112">Create asset document relation</span></span>

1. <span data-ttu-id="6a742-113">Veldu **Eignastýring** \> **Uppsetning** \> **Eignaskjöl**.</span><span class="sxs-lookup"><span data-stu-id="6a742-113">Select **Asset management** \> **Setup** \> **Asset documents**.</span></span>
2. <span data-ttu-id="6a742-114">Veldu **Nýtt** til að búa til skrá eignaskjals.</span><span class="sxs-lookup"><span data-stu-id="6a742-114">Select **New** to create an asset document record.</span></span>
3. <span data-ttu-id="6a742-115">Það fer eftir hversu sértækt þú vilt að skjalatengslin séu en gerðu viðeigandi val í einum eða fleiri eftirfarandi reita: **Eignagerð**, **Framleiðandi**, **Líkan**, **Eign**, **Starfsflokkur**, **Starfsgerð**, **Atvinnugerðafbrigði**, og **Vinnsluþörf**.</span><span class="sxs-lookup"><span data-stu-id="6a742-115">Depending on how specific you want the document relation to be, make relevant selections in one or more of the following fields: **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement**.</span></span> <span data-ttu-id="6a742-116">Valkostirnir sem eru í boði í **Atvinnugerðafbrigði** og **Starfsskylda** reitirnir fara eftir vali þínu í reitnum **Atvinnugerð**.</span><span class="sxs-lookup"><span data-stu-id="6a742-116">The options that are available in the **Job type variant** and **Job requirement** fields depend on your selection in the **Job type** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6a742-117">Þegar kerfið leitar að skjölum sem ættu að tengjast eign eða verkpöntun fer Eignastjórn í gegnum allar eignaskjalaskrár til að athuga hvort mögulegt sé samsvörun.</span><span class="sxs-lookup"><span data-stu-id="6a742-117">When the system searches for documents that should be related to an asset or a work order, Asset Management goes through all asset document records to check for a possible match.</span></span> <span data-ttu-id="6a742-118">Það athugar alltaf sértækustu samsetninguna fyrst.</span><span class="sxs-lookup"><span data-stu-id="6a742-118">It always checks the most specific combination first.</span></span> <span data-ttu-id="6a742-119">Með öðrum orðum, Eignastjórnun kannar fyrst hvort samsvörun finnist fyrir reitinn **Vinnsluþörf**.</span><span class="sxs-lookup"><span data-stu-id="6a742-119">In other words, Asset Management first checks for a match for the **Job requirement** field.</span></span> <span data-ttu-id="6a742-120">Ef engin samsvörun er fundin, skoðar hún hvort samsvörun sé fyrir reitinn **Atvinnugerðafbrigði**.</span><span class="sxs-lookup"><span data-stu-id="6a742-120">If no match is found, it checks for a match for the **Job type variant** field.</span></span> <span data-ttu-id="6a742-121">Ef engin samsvörun er fundin, skoðar hún hvort samsvörun sé fyrir reitinn **Vinnslugerð** og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="6a742-121">If no match is found, it checks for a match for the **Job type** field, and so on.</span></span> <span data-ttu-id="6a742-122">Eins og þú sérð á skipulagi síðunnar **Eignaskjöl** þýðir þessi hegðun að til að finna sértækustu samsetninguna, þá velur eignastjórnun hverja skrá frá hægri til vinstri fyrir leik.</span><span class="sxs-lookup"><span data-stu-id="6a742-122">As you can see in the layout of the **Asset documents** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="6a742-123">Nokkur skjöl gætu verið tengd eign eða verkpöntun.</span><span class="sxs-lookup"><span data-stu-id="6a742-123">Several documents might be related to an asset or a work order.</span></span> <span data-ttu-id="6a742-124">Þú getur breytt þjónustustiginu í viðhaldsbeiðni eða vinnupöntun eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="6a742-124">You can edit the service level on a maintenance request or a work order as you require.</span></span>

4. <span data-ttu-id="6a742-125">Veldu **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="6a742-125">Select **Attachments**.</span></span> <span data-ttu-id="6a742-126">Staðalsíðan **Meðhöndlun skjala** birtist.</span><span class="sxs-lookup"><span data-stu-id="6a742-126">The standard **Document handling** page appears.</span></span>
5. <span data-ttu-id="6a742-127">Settu upp skjölin eða athugasemdirnar sem eiga að fylgja skránni yfir eigna skjalið.</span><span class="sxs-lookup"><span data-stu-id="6a742-127">Set up the documents or notes that should be attached to the asset document record.</span></span> <span data-ttu-id="6a742-128">Eftir að þú hefur fest skjöl við **Viðhengi** reiturinn sýnir fjölda skjala sem tengjast skránni.</span><span class="sxs-lookup"><span data-stu-id="6a742-128">After you attach documents, the **Attachments** field shows the number of documents that are related to the record.</span></span>
