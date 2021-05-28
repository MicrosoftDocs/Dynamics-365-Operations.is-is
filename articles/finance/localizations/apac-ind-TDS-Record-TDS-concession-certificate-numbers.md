---
title: Skrá vottorðanúmer TDS-skattaívilnunar
description: Í þessu efnisatriði er útskýrt hvernig á að skrá númer skattfrádráttarskírteinis á heimildarskírteini (TDS) sem eru gefin út til lánardrottna.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023316"
---
# <a name="record-tds-concession-certificate-numbers"></a><span data-ttu-id="ee8b8-103">Skrá vottorðanúmer TDS-skattaívilnunar</span><span class="sxs-lookup"><span data-stu-id="ee8b8-103">Record TDS concession certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee8b8-104">Í þessu efnisatriði er útskýrt hvernig á að skrá númer skattfrádráttarskírteinis á heimildarskírteini (TDS) sem eru gefin út til lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="ee8b8-104">This topic explains how to record the Tax Deducted at Source (TDS) concession certificate numbers that are issued to vendors.</span></span>

1. <span data-ttu-id="ee8b8-105">Farið í **Skattur \> Óbeinir skattar \> Staðgreiðsluskattur \> Ívilnanir staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="ee8b8-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax concessions**.</span></span>
2. <span data-ttu-id="ee8b8-106">Í reitnum **Skattgerð** skal velja **TDS** til að setja upp ívilnunarvottorð fyrir skattgerð TDS.</span><span class="sxs-lookup"><span data-stu-id="ee8b8-106">In the **Tax type** field, select **TDS** to record concession certificates for the TDS tax type.</span></span>
3. <span data-ttu-id="ee8b8-107">Í flipanum **Yfirlit** skal velja **Alt+N** til að stofna línu.</span><span class="sxs-lookup"><span data-stu-id="ee8b8-107">On the **Overview** tab, select **Alt+N** to create a line.</span></span>

    <span data-ttu-id="ee8b8-108">[![Haus nýju línunnar](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span><span class="sxs-lookup"><span data-stu-id="ee8b8-108">[![Header of the new line](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span></span>

4. <span data-ttu-id="ee8b8-109">Í reitnum **Staðgreiðsluskattskóði** skal velja TDS-skattkóða sem ívilnunarvottorð eru gefin út fyrir.</span><span class="sxs-lookup"><span data-stu-id="ee8b8-109">In the **Withholding tax code** field, select the TDS tax code that the vendor concession certificates are issued for.</span></span> <span data-ttu-id="ee8b8-110">Reiturinn **Heiti staðgreiðsluskattskóða** sýnir heiti TDS-skattkóðans.</span><span class="sxs-lookup"><span data-stu-id="ee8b8-110">The **Withholding tax code name** field shows the name of the TDS tax code.</span></span>
5. <span data-ttu-id="ee8b8-111">Í reitunum **Frá dagsetningu** og **Til dagsetningar** skal skilgreina gildistímabil fyrir ívilnunarvottorðið sem notar TDS skattkóðann til að reikna út TDS fyrir lánardrottinn á sérstökum grunni.</span><span class="sxs-lookup"><span data-stu-id="ee8b8-111">In the **From date** and **To date** fields, define the period of validity for the concession certificate that uses the TDS tax code to calculate TDS for the vendor on a concessional basis.</span></span>
6. <span data-ttu-id="ee8b8-112">Í reitinn **Athugasemdir** eru færðar inn athugasemdir.</span><span class="sxs-lookup"><span data-stu-id="ee8b8-112">In the **Remarks** field, enter any remarks.</span></span>
7. <span data-ttu-id="ee8b8-113">Í reitinn **kafli** er færður inn lagakaflakóðinn sem TDS-ivilnunarvottorðið er notað undir.</span><span class="sxs-lookup"><span data-stu-id="ee8b8-113">In the **Section** field, enter the legal section code that the TDS concession certificate is availed under.</span></span>

    <span data-ttu-id="ee8b8-114">Ef kaflakóðinn er 197 birtist gildið „A“ bæði í dálknum „Ástæða fyrir engum frádrætti/lægri frádrætti“ í eyðublaði 26Q og dálknum „Ástæða fyrir engum frádrætti/lægri frádrætti/hæækun (ef einhver er)“ í eyðublaði 27Q.</span><span class="sxs-lookup"><span data-stu-id="ee8b8-114">If the section code is 197, the value "A" appears in both the "Reason for non-deduction/lower deduction" column in Form 26Q and the "Reason for non-deduction/lower deduction/grossing up (if any)" column in Form 27Q.</span></span> <span data-ttu-id="ee8b8-115">Ef kaflakóðinn er 197A birtist gildið „B“ á báðum þessum stöðum.</span><span class="sxs-lookup"><span data-stu-id="ee8b8-115">If the section code is 197A, the value "B" appears in both those places.</span></span>

8. <span data-ttu-id="ee8b8-116">Veldu **Vottorð** flýtiflipann til að skrá vottorðsskírteini TDS-ívilnunar fyrir lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="ee8b8-116">Select the **Certificate** FastTab to record TDS concession certificate numbers for vendors.</span></span>
9. <span data-ttu-id="ee8b8-117">Í svæðinu **Lánardrottinsreikningur** er valinn lánardrottinsreikningur sem TDS-ívilnunarvottorðið er gefið út fyrir.</span><span class="sxs-lookup"><span data-stu-id="ee8b8-117">In the **Vendor account** field, select the vendor account that the TDS concession certificate is issued for.</span></span>
10. <span data-ttu-id="ee8b8-118">Í reitunum **Frá dagsetningu** og **Til dagsetningar** skal skilgreina gildistímabil TDS-ívilnanavottorðsins.</span><span class="sxs-lookup"><span data-stu-id="ee8b8-118">In the **From date** and **To date** fields, define the period of validity for the TDS concession certificate.</span></span>

    <span data-ttu-id="ee8b8-119">Útreikningur TDS á ívilnunargrunni er byggður á tímabilinu þegar vottorðið er stofnað fyrir lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="ee8b8-119">The calculation of TDS on a concessional basis is based on the period when the certificate is created for the vendor.</span></span>

11. <span data-ttu-id="ee8b8-120">Í reitnum **Vottorð** skal færa inn númer vottorð TDS-ívilnana.</span><span class="sxs-lookup"><span data-stu-id="ee8b8-120">In the **Certificate** field, enter the TDS concession certificate number.</span></span>

    <span data-ttu-id="ee8b8-121">[![Vottorðsflýtiflipi](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span><span class="sxs-lookup"><span data-stu-id="ee8b8-121">[![Certificate FastTab](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span></span>

12. <span data-ttu-id="ee8b8-122">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ee8b8-122">Close the page.</span></span>
