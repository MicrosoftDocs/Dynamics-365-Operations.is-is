---
title: Setja upp altækan staðgreiðsluskatt
description: Þetta efnisatriði telur upp skrefin fyrir uppsetningu altæks staðgreiðsluskatts fyrir sölu og innkaup.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 00c472e90f4926c52ffe9b19661e68cbfa6bd493
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204834"
---
# <a name="set-up-global-withholding-tax"></a><span data-ttu-id="6c004-103">Setja upp altækan staðgreiðsluskatt</span><span class="sxs-lookup"><span data-stu-id="6c004-103">Set up global withholding tax</span></span>

<span data-ttu-id="6c004-104">Þetta efnisatriði telur upp skrefin fyrir uppsetningu altæks staðgreiðsluskatts fyrir sölu og innkaup.</span><span class="sxs-lookup"><span data-stu-id="6c004-104">This topic lists the steps for setting up global withholding tax for sales and purchases.</span></span> 

1. <span data-ttu-id="6c004-105">Setjið upp staðgreiðsluskatt yfirvalda á síðunni **Yfirvöld staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="6c004-105">Set up withholding tax authorities on the **Withholding tax authorities** page.</span></span>

2. <span data-ttu-id="6c004-106">Setjið upp jöfnunartímabil staðgreiðsluskatts á síðunni **Jöfnunartímabil staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="6c004-106">Set up withholding settlement periods on the **Withholding tax settlement periods** page.</span></span>

3. <span data-ttu-id="6c004-107">Setjið upp fjárhagsbókunarflokk staðgreiðsluskatts á síðunni **Staðgreiðsluskattur > Fjárhagsbókunarflokkur**.</span><span class="sxs-lookup"><span data-stu-id="6c004-107">Set up withholding ledger posting group on the **Withholding tax > ledger posting group** page.</span></span>

   > [!Note] 
   >
   > <span data-ttu-id="6c004-108">Lykillinn **Staðgreiðsluskattur** verður úthlutað með aðallykli með **Bókunargerð** fyrir staðgreiðsluskatt.</span><span class="sxs-lookup"><span data-stu-id="6c004-108">**Withholding tax** account will be assigned with a main account with **Posting type** of Withholding tax.</span></span> <span data-ttu-id="6c004-109">Lyklinum **Mótlykill staðgreiðsluskatts** verður úthlutað með aðallykli með **Bókunargerð** fyrir „Mótlykil staðgreiðsluskatts“.</span><span class="sxs-lookup"><span data-stu-id="6c004-109">**Withholding tax offset** account will also be assigned with a main account with **Posting type** "Withholding tax offset".</span></span> <span data-ttu-id="6c004-110">Farið í **Almennur fjárhagur > Bókhaldslykill > Lyklar > Aðallyklar**, setjið upp **Bókunargerð** í undirskjámyndinni **Villuleit bókunar** fyrir aðallyklana.</span><span class="sxs-lookup"><span data-stu-id="6c004-110">Go to **General ledger > Chart of accounts > Accounts > Main accounts**, set up the **Posting type** in the **Posting validation** sub-form for the main accounts.</span></span>

4. <span data-ttu-id="6c004-111">Setjið upp kóða staðgreiðsluskatts á síðunni **Staðgreiðsluskattskóðar**.</span><span class="sxs-lookup"><span data-stu-id="6c004-111">Set up withholding tax codes on the **Withholding tax codes** page.</span></span>

5. <span data-ttu-id="6c004-112">Setjið upp flokka staðgreiðsluskatts á síðunni **Staðgreiðsluskattsflokkar**.</span><span class="sxs-lookup"><span data-stu-id="6c004-112">Set up withholding tax groups on the **Withholding tax groups** page.</span></span>

6. <span data-ttu-id="6c004-113">Setjið upp tekjugerðir staðgreiðsluskatts á síðunni **Tekjugerðir** **staðgreiðsluskatts**.</span><span class="sxs-lookup"><span data-stu-id="6c004-113">Set up withholding tax revenue types on the **Withholding tax revenue** **types** page.</span></span>

7. <span data-ttu-id="6c004-114">Setjið upp flokka staðgreiðsluskatts á síðunni **Staðgreiðsluskattflokkar vöru** fyrir vöru eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="6c004-114">Set up withholding tax groups on the **Item withholding tax groups** page for an item or service.</span></span>

8. <span data-ttu-id="6c004-115">Setjið upp **Lágmarksupphæð reiknings** á síðunni **Færibreytur fjárhags > Staðgreiðsluskattur**.</span><span class="sxs-lookup"><span data-stu-id="6c004-115">Set up **Minimum invoice amount** on the **General ledger parameters > Withholding tax** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]